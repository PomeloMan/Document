## Docker Registry

#### 私有库安装
```
docker pull registry
docker run -d -p 5000:5000 --restart always --name registry registry

#访问web http://ip:5000/v2/_catalog
{"repositories":[]} // 返回数据安装成功
```

#### 配置docker服务访问非安全docker仓库
```
## 在/etc/docker目录下，添加一个daemon.json文件，写上非安全访问的仓库IP:端口号
{"insecure-registries":["49.233.205.236:32768"]}
```

