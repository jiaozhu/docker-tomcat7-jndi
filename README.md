# docker-tomcat7

### 下载

> git clone https://github.com/jiaozhu/docker-tomcat7.git

### 使用

进入 `buildfile` 目录，构建tomcat7镜像

```
cd buildfile
./build-docker.sh
```

使用 `docker-compose`

```
cd ..
docker-compose up
docker-compose stop
docker-compose rm -f
```

