# 初始化设置
### 设置姓名和邮箱地址
```git
$ git config --global user.name "Firstname Lastname"
$ git config --global user.email "your.email@example.com"
```
>这个命令会在“./gitconfig”中以如以下形式输出设置文件

```text
[user]
	name = Firstname Lastname
	email = your_email@example.com
```
### 提高命令输出的可读性（给代码添加颜色）
```git
$ git config --global color.ui auto
```
> 这个命令会在“./gitconfig”中添加下面一行

```text
[color]
	ui = auto
```
### 我的github的id
```text
mangolinli
# 我的链接
```
[我的网页](http://github.com/mangolinli)
### 设置SSH Key
