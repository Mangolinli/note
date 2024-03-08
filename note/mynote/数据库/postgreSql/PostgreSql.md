
[[PostgreSql 用户管理操作]]
[[PostgreSql Linux 配置信息]]

## Linux 上PostgreSql服务操作

```sh
# 启动服务
sudo service postgresql start
# 查看服务状态
sudo service postgresql status
# 重启服务
sudo service postgresql restart
# 停止服务
sudo service postgresql stop
```


### 用psql连接数据库
+ psql是PostgresSQL软件安装目录下的bin路径下的可执行程序
+ -h选项表示host，要连接数据库服务器名或者IP地址：如果要访问的数据库在远端，不在本地服务器上，则这里应该用那台机器的IP地址；如果云服务器的话，则用云服务器商提供的域名字符串即可；
+ -p选项表示port，数据库运行在那个端口上，默认是5432，这个可以在postgres.conf配置文件里修改，但是需要restart数据库才生效。
+ -d选项表示database，我们要连接访问的数据库名。
+ -U选项表示username，我们以那个用户访问数据库。

```shell
# 选择
which psql

```

