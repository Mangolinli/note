```sh
# mango电脑的内存分配以及用途
/boot (主分区) 这是用于存储引导加载程序和内核文件的空间 2G（Ext4）
/boot/efi 1G

swap 交换分区 16G
/var 逻辑分区 存储系统变化的文件，例如日志文件和数据库 30G（Ext4）
/tmp 逻辑分区 tmp 是 temporary(临时) 的缩写这个目录是用来存放一些临时文件的。 15G（Ext4）
/usr 逻辑分区  usr 是 unix shared resources(共享资源) 的缩写，这是一个非常重要的目录，用户的很多应用程序和文件都放在这个目录下，类似于 windows 下的 program files 目录。 120G（Ext4）
/opt 逻辑分区  用于存放可选的第三方软件 30G（Ext4）
/ 逻辑分区 93.889G(Ext4)
/home 200G
```