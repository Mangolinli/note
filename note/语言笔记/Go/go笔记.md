### 1. 基本知识
```go
# 注释
//取消单行的
/*
把内容取消掉
*/

# 变量定义eg
var name string = "mango"

# 同时定义多个变量
var(
	name string
	age int
	addr string
)

```
### 2. 小知识点
##### 1. 系统的自动赋值零值
	1. 整形和浮点型变量的默认值为0和0.0
	2. 字符串变量的默认值为空字符串
	3. 布尔型为false
	4. 切片，函数，指针变量的默认值为nill
#### 2.变量的定义
```go
var namr type
# eg
var a, b *int
```
1. var是声明变量的关键字，是固定的写法。
2. name就是变量的名字。
3. type 变量的类型。
#### 3. 内存关系
```go
import "fmt"
# 类型的简单输出
func main(){
	name :="mango"
	age :=18
	fmt.Println(name,age)
	fmt.printf("%T,%T",name,age)//输出变量的类型
}
# 交换变量
var a int = 100
var b int = 200
b,a=a,b
fmt.Println(a,b)
```
	1. 内存地址用%p，整数用%d ，%.3f就是保留3位小数，默认的是6位
	2. %b为输出二进制。
1. 变量匿名，全局变量
```go
func test()(int , int){
	return 100,200
}
func main(){
	a,_:=test()
	fmt.Println(a)
}
```
1. <mark style="background: #FFB86CA6;">\_表示废掉一个值不需要,只需要a，为匿名对象</mark>
2. 一个变量（常量，类型，函数）在程序中都有一定的作用范围，称之为作用域。
3. 全局变量的同时局部也可以定义同样的变量，我们局部会使用局部定义的变量。
#### 4. 常量
```go
func main() {

    const URL string = "www.baidu.com" //显示定义

    const URL2 = "www.baidu.com"       //隐式定义

  
    const a, b, c = 3.14, "mango", false //同时定义多个常量

    fmt.Println(URL)

    fmt.Println(URL2)

    fmt.Println(a, b, c)

}
```
1. iota特殊常量，可以认为是一个可以被编译器修改的常量
2. <mark style="background: #FFB8EBA6;">iota是go语言的常量计数器</mark>
3. iota在const关键字出现时将被重置为0（const内部的第一行之前），const中每新增一行常量声明将使iota计数一次（可以理解为const的索引）
#### 5.类型分类
![[Pasted image 20230925124016.png]]
1. 布尔类型bool （true和false）
2. 数值型
	1. 整形
	2. uint8 无符号8位整型
	3. uint16 /uint32/uint64
	4. int8有符号8位整型		
	5. int16/int32/int64
3. 浮点型
		1. flaot32 IEEE-754 32为浮点型数
		2. flaot64
		3. complex64 32位实数和虚数
		4. complex128 64位实数和虚数
4. 其他类型
		1. byte 类似uint8
		2. rune 类似int32
		3. uintptr无符号整型，用于存放一个指针。
5.  字符串类型
	1. 字符串之间用+进行连接
	2. 转义字符\\比如说\"等等都需要用转义字符才能输出的。
	3. string
6.  类型转换
	1. 强制转换即可
	2. 整形是不能转换为bool类型的

####   6.运算符号
1.  运算符号
	1. 算术运算符 + - \* ++ --
	2. 关系运算符 == != > < >= <= 
	3. 逻辑运算符 && || ！
	4. 位运算符
		1. &：按位与，都是1结果为1，否则为0。
		2. |：按位或，都是0结果为0，否则为1。
		3. ^：按位异或，不同为1，反之为0；
		4. &^：位清空，a&^b:对于b上的每一个数值，如果为 0，则取a对应位上的数值，如果为1，则取0.
		5. <<：左移
		6. >>：右移

1. 键盘输入
```go
fmt.Scanln(&x, &y)
```







#### 7.流程控制
1. if语句
```go
package main

import "fmt"

func main(){
	var a int = 15
	//单只流
	if a > 20{
		fmt.Println("a>20")
	}
	//俩个支流
	if a>=20{
		fmt.Println("a>=20")
	}else{
		fmt.Println("a<20")
	}
	//多个支流
	if a = 20{
		
	}else if a > 20{
		
	}else{
		
	}
	
}
```
2. switch语句
![[Pasted image 20230925231615.png]]
![[Pasted image 20230925233008.png]]

3. fallthrough 贯穿；直通
> switch默认情况下匹配成功以后就不会执行其他的case，如果我们需要执行后面的case，可以使用fallthrough 穿透case使用fallthrough会强制执行后面的case，fallthrough不会判断下一条case的表达式结果是否为true。

![[Pasted image 20230925234926.png]]

4. break终止循环
5. for语句循环(支持三个条件都没有)
```go
func main(){
	for i:=1; i<= 10;i++{
		fmt.Println(i)
	}
}
```
6. continue 结束单次循环，进入下一个循环。
#### 8.string遍历
```go
func main() {

    str := "hello.xuexiangbao"

  

    fmt.Println(str)

    fmt.Println("字符串的长度为", len(str))

  

    fmt.Println("字节打印", str[2])

    fmt.Printf("%c", str[2])

  

}
```
![[Pasted image 20230926001031.png]]
### 3. 函数
#### 1. 什么是函数
> 函数是基本的代码块，用于执行一个任务。
> Go语言最少有个main函数。
> 你可以通过函数来划分不同功能，逻辑上每个函数执行的是指定的任务。
> 函数声明告诉了编译器函数的名称，返回类型，和参数。
![[Pasted image 20230926001736.png]]
> func 函数名（参数，参数，……） 函数调用后的返回值{
> 	函数体：执行一段代码
> 	return 返回结果
> }
### 4.函数的声明和调用
```go
func main() {

    //函数调用

    printfo()

    myprint("haha")

    x, y := swap("xuesheng", "pengyou")

    fmt.Println(x, y)

}


//无参无返回值函数

func printfo() {

    fmt.Println("printinfo")

}


//有一个参数的函数

func myprint(msg string) {

    fmt.Println(msg)

}
  

//有一个返回值

func add(a, b int) int {

    c := a + b

    return c

}


//多个返回值

func swap(x, y string) (string, string) {

    return y, x

}
```
> 形式参数： 定义函数时，用来接收外部传入数据的参数，就是形式参数
> 实际参数：调用函数时，传给形参的实际数据就做实际参数
#### 3. 可变参数
![[Pasted image 20230926003510.png]]
#### 4.参数传递
![[Pasted image 20230926003646.png]]
![[Pasted image 20230926103205.png]]

#### 5. 递归函数
![[Pasted image 20230926103819.png]]
#### 6. defer延迟执行函数。
![[Pasted image 20230926104230.png]]
