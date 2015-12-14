# docker-tomcat7-use-jndi

## 下载

    ```
    git clone https://github.com/jiaozhu/docker-tomcat7-jndi.git
    ```

## 使用

1. 构建容器依赖于 [docker-oracle-xe-11g](https://github.com/wnameless/docker-oracle-xe-11g)

    ```
    docker run -d -p 49160:22 -p 49161:1521 --name oracle-xe-11g wnameless/oracle-xe-11g
    ```

    ```
    # hostname: localhost
    # port: 49161
    # sid: xe
    # username: system
    # password: oracle
    # Password for SYS & SYSTEM

    - Login by SSH

    $ ssh root@10.6.6.100 -p 49160
    password: admin

    $ docker-machine ip dev
    10.6.6.100
    ```

2. 进入 `conf` 目录，根据环境修改tomcat所需要的配置文件，如 `server.xml`、`context.xml`、`tomcat-users.xml`等

3. 使用docker-compose

    ```
    cd ..
    docker-compose up -d
    docker-compose stop
    docker-compose rm -f
    ```
