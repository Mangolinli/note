
## 如何在服务器上进入PostgreSql执行SQL

```sh
# 1. 切换postgres 用户 进入
sudo su - mango
psql
# 2. sudo 直接进入
sudo -u postgres psql
```

## PostgreSql 创建用户和DB

```postgresql

# 创建用户
CREATE USER '用户名' WITH PASSWORD '用户密码';
# 创建DB
CREATE DATABASE 'xxxdb' OWNER '用户名';
# 将xxxdb的权限授予用户
GRANT ALL PRIVILEGES ON DATABASE 'xxxdb' TO '用户名';
```

## PostgreSql 查看用户和DB

```postgresql
# 查看所有用户
select * from pg_user;

# 查看所有DB
SELECT * FROM pg_database;
```

## PostgreSql 更改密码

```postgresql
# 修改密码
ALTER USER '用户名' WITH PASSWORD '新密码';
```
### PostgreSql更换用数据库
```postgresql
# 先进入postgres超级用户

\c mangodb;
```


