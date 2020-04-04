# Docker中使用PostgreSql

## 使用步骤

### 下载PostgreSql镜像

> `Docker Hub` 中提供了官方的 `PostgreSql` 镜像。 可以访问查看自己需要的数据库版本镜像 ![hub.docker.com/_/postgres](https://hub.docker.com/_/postgres)  

下载 ```Postgres 12.2``` 镜像

```shell
docker pull postgres:12.2
```

### 创建容器


```
docker run --name postgres -e POSTGRES_PASSWORD=postgres -p 5432:5432 -d postgres:12.2
```

- POSTGRES_PASSWORD: 设置 `postgres` 数据库链接密码
