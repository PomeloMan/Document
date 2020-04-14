## Docker
Docker 安装，打包，部署学习

#### 目录
* [Portainer](./Portainer) (<https://www.portainer.io/>)

#### 安装（旧版）
```
yum -y update #升级所有包，改变软件设置和系统设置,系统版本内核都升级
yum -y upgrade #升级所有包，不改变软件设置和系统设置，系统版本升级，内核不改变
yum -y install docker
```

#### 启动
```
systemctl start docker
systemctl enable docker #设置服务自启动
```

#### 指令
```
docker version #查看docker版本
```

#### 卸载
```
sudo yum remove docker \
docker-client \
docker-client-latest \
docker-common \
docker-latest \
docker-latest-logrotate \
docker-logrotate \
docker-engine
```

#### 安装 Docker ce（新版）
```
#安装所需的软件包。yum-artils 提供了 yum-conf-scher 实用程序, 设备映射持久性数据和 lvm2 是设备存储驱动程序所必需的。
yum install -y yum-utils \
device-mapper-persistent-data \
lvm2

#使用以下命令设置稳定的存储库。
yum-config-manager \
--add-repo \
https://download.docker.com/linux/centos/docker-ce.repo

#这些存储库包含在上面的 docker. repo 文件中, 但默认情况下是禁用的。您可以在稳定的存储库旁边启用它们。下面的命令启用夜间存储库。
yum-config-manager --enable docker-ce-nightly

#查看现有的包
yum list docker-ce --showduplicates | sort -r

#安装最新版本的 Docker ce 和容器
yum install docker-ce docker-ce-cli containerd.io

#启动
systemctl start docker
systemctl enable docker
```