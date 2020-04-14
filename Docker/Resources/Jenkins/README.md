## [Jenjins](https://jenkins.io/zh/)
Jenkins是开源CI&CD软件领导者， 提供超过1000个插件来支持构建、部署、自动化， 满足任何项目的需要。

#### 安装
```
$ docker pull jenkins/jenkins:lts
```

#### 运行
```
$ docker run -d --name jenkins -p 9000:9000 -v /home/jenkins:/home/jenkins jenkins/jenkins:lts;
```

#### 查看Jenkins administrator初始密码
```
$ docker ps -a #找到jenkins容器ID
$ docker exec -u 0 -it a0be9d163c23 /bin/bash
$ cat /var/jenkins_home/secrets/initialAdminPassword
```