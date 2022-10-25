debian10安装docker，参考https://blog.csdn.net/zhupengfei/article/details/102739901

安装mysql，参考https://hub.docker.com/_/mysql
```
docker pull mysql
docker exec -it mysql mysql -u root -proot`
docker run --name mysql -e MYSQL_ROOT_PASSWORD=root -d mysql:latest
```

docker安装redis
```bash
# 拉取镜像
docker pull redis:latest
# 运行容器
docker run --name=redis-server -p 6379:6379 -d redis:latest
# 进入容器
docker exec -it  redis-server  /bin/bash
# 进入redis
redis-cli
```

docker运行rabbitmq
```
docker pull rabbitmq:3-management
docker run -d --hostname my-rabbit --name some-rabbit -p 15672:15672  -p 5672:5672 -e RABBITMQ_DEFAULT_USER=user -e RABBITMQ_DEFAULT_PASS=password rabbitmq:3-management
```
