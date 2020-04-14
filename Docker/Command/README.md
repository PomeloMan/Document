## [Docker 命令](https://docs.docker.com/engine/reference/commandline/docker/)
Docker CLI的基本命令。

#### 子命令
<font size="2">

|命令|描述|
|:---|:---|
|[docker attach](https://docs.docker.com/engine/reference/commandline/attach/)|将本地标准输入，输出和错误流附加到正在运行的容器|
|[docker build](https://docs.docker.com/engine/reference/commandline/build/)|从Dockerfile构建映像|
|[docker builder](https://docs.docker.com/engine/reference/commandline/builder/)|管理构建|
|[docker checkpoint](https://docs.docker.com/engine/reference/commandline/checkpoint/)|管理检查点|
|[docker commit](https://docs.docker.com/engine/reference/commandline/commit/)|根据容器的更改创建新图像|
|[docker config](https://docs.docker.com/engine/reference/commandline/config/)|管理Docker配置|
|[docker container](https://docs.docker.com/engine/reference/commandline/container/)|管理容器|
|[docker context](https://docs.docker.com/engine/reference/commandline/context/)|管理上下文|
|[docker cp](https://docs.docker.com/engine/reference/commandline/cp/)|在容器和本地文件系统之间复制文件/文件夹|
|[docker create](https://docs.docker.com/engine/reference/commandline/create/)|创建一个新的容器|
|[docker diff](https://docs.docker.com/engine/reference/commandline/diff/)|检查容器文件系统上文件或目录的更改|
|[docker events](https://docs.docker.com/engine/reference/commandline/events/)|从服务器获取实时事件|
|[docker exec](https://docs.docker.com/engine/reference/commandline/exec/)|在正在运行的容器中运行命令|
|[docker export](https://docs.docker.com/engine/reference/commandline/export/)|将容器的文件系统导出为tar存档|
|[docker history](https://docs.docker.com/engine/reference/commandline/history/)|显示图像的历史记录|
|[docker image](https://docs.docker.com/engine/reference/commandline/image/)|管理镜像|
|[docker images](https://docs.docker.com/engine/reference/commandline/images/)|列出镜像|
|[docker import](https://docs.docker.com/engine/reference/commandline/import/)|从tarball导入内容以创建文件系统映像|
|[docker info](https://docs.docker.com/engine/reference/commandline/info/)|显示系统范围的信息|
|[docker inspect](https://docs.docker.com/engine/reference/commandline/inspect/)|返回有关Docker对象的低级信息|
|[docker kill](https://docs.docker.com/engine/reference/commandline/kill/)|杀死一个或多个正在运行的容器|
|[docker load](https://docs.docker.com/engine/reference/commandline/load/)|从tar存档或STDIN加载图像|
|[docker login](https://docs.docker.com/engine/reference/commandline/login/)|登录Docker注册表|
|[docker logout](https://docs.docker.com/engine/reference/commandline/logout/)|从Docker注册表注销|
|[docker logs](https://docs.docker.com/engine/reference/commandline/logs/)|提取容器的日志|
|[docker manifest](https://docs.docker.com/engine/reference/commandline/manifest/)|管理Docker映像清单和清单清单|
|[docker network](https://docs.docker.com/engine/reference/commandline/network/)|管理网络|
|[docker node](https://docs.docker.com/engine/reference/commandline/node/)|管理Swarm节点|
|[docker pause](https://docs.docker.com/engine/reference/commandline/pause/)|暂停一个或多个容器中的所有进程|
|[docker plugin](https://docs.docker.com/engine/reference/commandline/plugin/)|管理插件|
|[docker port](https://docs.docker.com/engine/reference/commandline/port/)|列出端口映射或容器的特定映射|
|[docker ps](https://docs.docker.com/engine/reference/commandline/ps/)|列出容器|
|[docker pull](https://docs.docker.com/engine/reference/commandline/pull/)|从注册表中提取图像或存储库|
|[docker push](https://docs.docker.com/engine/reference/commandline/push/)|将映像或存储库推送到注册表|
|[docker rename](https://docs.docker.com/engine/reference/commandline/rename/)|重命名容器|
|[docker restart](https://docs.docker.com/engine/reference/commandline/restart/)|重新启动一个或多个容器|
|[docker rm](https://docs.docker.com/engine/reference/commandline/rm/)|删除一个或多个容器|
|[docker rmi](https://docs.docker.com/engine/reference/commandline/rmi/)|删除一个或多个镜像|
|[docker run](https://docs.docker.com/engine/reference/commandline/run/)|在新容器中运行命令|
|[docker save](https://docs.docker.com/engine/reference/commandline/save/)|将一个或多个图像保存到tar存档（默认情况下流式传输到STDOUT）|
|[docker search](https://docs.docker.com/engine/reference/commandline/search/)|在Docker Hub中搜索图像|
|[docker secret](https://docs.docker.com/engine/reference/commandline/secret/)|管理Docker机密|
|[docker service](https://docs.docker.com/engine/reference/commandline/service/)|管理服务|
|[docker stack](https://docs.docker.com/engine/reference/commandline/stack/)|管理Docker堆栈|
|[docker start](https://docs.docker.com/engine/reference/commandline/start/)|启动一个或多个已停止的容器|
|[docker stats](https://docs.docker.com/engine/reference/commandline/stats/)|显示实时的容器资源使用情况统计流|
|[docker stop](https://docs.docker.com/engine/reference/commandline/stop/)|停止一个或多个运行中的容器|
|[docker swarm](https://docs.docker.com/engine/reference/commandline/swarm/)|管理群|
|[docker system](https://docs.docker.com/engine/reference/commandline/system/)|管理Docker|
|[docker tag](https://docs.docker.com/engine/reference/commandline/system/)|创建引用了SOURCE_IMAGE的标签TARGET_IMAGE|
|[docker top](https://docs.docker.com/engine/reference/commandline/top/)|显示容器的运行过程|
|[docker trust](https://docs.docker.com/engine/reference/commandline/trust/)|管理对Docker映像的信任|
|[docker unpause](https://docs.docker.com/engine/reference/commandline/unpause/)|取消暂停一个或多个容器中的所有进程|
|[docker update](https://docs.docker.com/engine/reference/commandline/update/)|更新一个或多个容器的配置|
|[docker version](https://docs.docker.com/engine/reference/commandline/version/)|显示Docker版本信息|
|[docker volume](https://docs.docker.com/engine/reference/commandline/volume/)|管理卷|
|[docker wait](https://docs.docker.com/engine/reference/commandline/wait/)|阻塞直到一个或多个容器停止，然后打印其退出代码|

</font>