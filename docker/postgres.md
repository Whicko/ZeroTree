# Docker中使用PostgreSql

## 使用步骤

### 下载PostgreSql镜像

> `Docker Hub` 中提供了官方的 `PostgreSql` 镜像。 可以访问查看自己需要的数据库版本镜像 [hub.docker.com/_/postgres](https://hub.docker.com/_/postgres)  

下载 ```Postgres 12.2``` 镜像

```shell
docker pull postgres:12.2
```

### 创建容器

```shell
docker run --name postgres -e POSTGRES_PASSWORD=postgres -p 5432:5432 -d postgres:12.2
```

在上例中使用 `postgres12.2` 的镜像创建一个名字为 `postgres` 的容器，并且通过设置环境变量 `POSTGRES_PASSWORD` 设置数据库访问密码。同时设置本机5432和容器的5432端口映射。

### 启动容器

```hell
docker start postgres
```

通过 `docker` 的 `start` 命令启动容器，现在就可以访问在 `docker` 中的数据库了。
