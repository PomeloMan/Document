## [Portainer](https://www.portainer.io/)
Docker 可视化管理工具

#### 安装
```
docker search portainer #查询当前镜像
docker pull docker.io/portainer/portainer #下载镜像
```

#### 运行
```
docker volume create portainer_data #创建数据目录
docker run -d -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer
```
