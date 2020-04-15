## 创建 Docker TLS 证书

#### 生成证书
```
#相关配置信息
SERVER="49.232.60.163"
HOST="ipomelo.online"
PASSWORD=""
COUNTRY="CN"
STATE="JS"
CITY="WX"
ORGANIZATION="PACT"
ORGANIZATIONAL_UNIT="DEV"
EMAIL="fengchao.z@outlook.com"

###开始生成文件###
echo "start..."

#切换到生产密钥的目录
cd /etc/docker
#生成ca私钥(使用aes256加密)
openssl genrsa -aes256 -passout pass:$PASSWORD  -out ca-key.pem 2048
#生成ca证书，填写配置信息
openssl req -new -x509 -passin "pass:$PASSWORD" -days 3650 -key ca-key.pem -sha256 -out ca.pem -subj "/C=$COUNTRY/ST=$STATE/L=$CITY/O=$ORGANIZATION/OU=$ORGANIZATIONAL_UNIT/CN=$SERVER/emailAddress=$EMAIL"

#生成server证书私钥文件
openssl genrsa -out server-key.pem 2048
#生成server证书签名文件
openssl req -subj "/CN=$SERVER" -sha256 -new -key server-key.pem -out server.csr
#使用CA证书及CA密钥以及上面的server证书请求文件进行签发，生成server自签证书
echo subjectAltName = DNS:$HOST,IP:$SERVER,IP:127.0.0.1 >> extfile.cnf
echo extendedKeyUsage = serverAuth >> extfile.cnf
openssl x509 -req -days 3650 -sha256 -in server.csr -CA ca.pem -CAkey ca-key.pem -passin "pass:$PASSWORD" -CAcreateserial -out server-cert.pem -extfile extfile.cnf

#生成client证书RSA私钥文件
openssl genrsa -out key.pem 2048
#生成client证书请求文件
openssl req -subj '/CN=client' -new -key key.pem -out client.csr

echo extendedKeyUsage = clientAuth > extfile-client.cnf
#生成client自签证书（根据上面的client私钥文件、client证书请求文件生成）
openssl x509 -req -days 3650 -sha256 -in client.csr -CA ca.pem -CAkey ca-key.pem -passin "pass:$PASSWORD" -CAcreateserial -out cert.pem -extfile extfile-client.cnf

#更改密钥权限
chmod 0400 ca-key.pem key.pem server-key.pem
#更改密钥权限
chmod 0444 ca.pem server-cert.pem cert.pem
#删除无用文件
#rm client.csr server.csr

#修改docker启动项/lib/systemd/system/docker.service
#在ExecStart值后面添加:
#--tlsverify \
#--tlscacert=/etc/docker/ca.pem \
#--tlscert=/etc/docker/server-cert.pem \
#--tlskey=/etc/docker/server-key.pem \
#-H tcp://0.0.0.0:2376 \
#-H unix:///var/run/docker.sock \
#echo "---- v修改docker启动项v ----"
#SetOPTS=" /usr/bin/dockerd-current \\
#          --tlsverify \\
#          --tlscacert=/etc/docker/ca.pem \\
#          --tlscert=/etc/docker/server-cert.pem \\
#          --tlskey=/etc/docker/server-key.pem \\
#          -H tcp://0.0.0.0:2376 \\
#          -H unix:///var/run/docker.sock \\ "
#sed  -i "s#^ExecStart.*#& $SetOPTS #" /lib/systemd/system/docker.service
#grep '^ExecStart' /lib/systemd/system/docker.service
#echo "---- ^修改docker启动项^ ----"

#重启Docker
systemctl daemon-reload
systemctl restart docker

echo "end"
###生成结束###
```

#### 修改docker启动项(/lib/systemd/system/docker.service)
```
#在ExecStart值后面添加:
--tlsverify \
--tlscacert=/etc/docker/ca.pem \
--tlscert=/etc/docker/server-cert.pem \
--tlskey=/etc/docker/server-key.pem \
-H tcp://0.0.0.0:2376 \
-H unix:///var/run/docker.sock \
```

#### 重启Docker
```
systemctl daemon-reload
systemctl restart docker
```