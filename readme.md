## docker file learn 

### `docker-compose` 和`Dockerfile` 区别

> - Dockerfile  构建镜像
> - docker-compose 编排容器并启动服务

常用命令：
> - **构建镜像**  
```sh
docker build -t test-docker:tag .
```
> - **启动容器服务** 
 ```sh
 docker-compose up -d
 ```
> - **查看所有容器** 
 ```sh
 docker ps -a 
 ```
> - **删除容器**  
```sh
docker rm  id
```
> - **删除镜像**  
```sh
docker rmi  id
```
