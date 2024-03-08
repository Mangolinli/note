
## pg_hba.conf 配置

```sh
# 1. 允许那些IP使用外部链接
# 1.1. METHOD: (password:明文密码链接, md5: md5加密的密码链接, trust: 无密码链接)
# 1.2. CIDR-ADDRESS: 允许链接的IP (0:0:0:0/0: 任何IPV4)
# 1.3. Type: (host: 使用 TCP/IP 连接)
# TYPE    DATABASE   USER     CIDR-ADDRESS            METHOD  
host   all        all      0:0:0:0/0               password 
```

## postgresql.conf配置

```sh
# *: 监听所有IP
listen_addresses = '*'     # what IP address(es) to listen on;
```
