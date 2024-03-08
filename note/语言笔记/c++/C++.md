# C++

### 基本知识

+ .cpp文件只能用g++命令
+ .c文件用gcc命令
+ 头文件:后缀为.h，主要是定义和声明之类的，比如类的定义，常量定义
  源文件：后缀.cpp，主要是实现之类的，比如类方法的实现
  资源文件：主要是你用到的一些程序代码以外的东西，比如图片之类，或者菜单、工具栏之类的定义之类
+ 注释：     先CTRL+K，然后CTRL+C

  取消注释： 先CTRL+K，然后CTRL+U

### 1.第一课

### 2.自学

####  1.**条件表达式** 

操作数1 ？操作数2 ： 操作数3

首先对操作数1求值，其值非0时，表达式的值位操作数2 的值，否则位操作数3的值。按右结合。

#### 2.递归函数：

调用自身的[函数](https://link.zhihu.com/?target=https%3A//www)称为递归函数。

```c++
void recurse()
{
    ... .. ...
    recurse();
    ... .. ...
}

int main()
{
    ... .. ...
    recurse();
    ... .. ...
}
```



```c++
#include <iostream>//列子求n的阶乘
using namespace std;
int factorial(int);
int main() {
    int n;
    cout << "输入一个数字来查找阶乘: ";
    cin >> n;
    cout << "数字 " << n << " 的阶乘= " << factorial(n);
    return 0;
}
int factorial(int n) {
    if (n > 1) {
        return n * factorial(n - 1);
    }
    else {
        return 1;
    }
}
```



#### 3.清空输出界面   

```c++
 system("cls");
 system("");
```

#### 4.预处理指令

```c++
#include<文件名>
#include"文件名“
```

#### 5.extern多文件程序使用全局变量

```c++
//file1.cpp
int global;

//file2.cpp
extern int global;
```

存储器说明符extern告诉编译器，变量global或者在同一个文件中稍后定义，或者在另一个文件中定义。编译器会通知连接程序去查找global的说明位置。

#### 6.setw用法

+ setw（） 用于控制输出之间的间隔

---

(1)s和a之间有7个空格，cout<<'s'<<setw(8)<<'a'<<endl;的意思是s后面输出8个字符，其中a占一个字符，剩余7个字符用空格填充。

(2)setw()默认填充的内容为空格，可以setfill()设置其他字符填充。

(3)setw（）默认为右对齐。

(4)左对齐。

``` c++
	cout << std::left<< std::setw(5) << "1" << endl;
	cout << std::left<< std::setw(5) << "10" << endl;
	cout << std::left<< std::setw(5) << "100" <<endl;
```



---

#### 7.流操作算子的使用方法

| 流操纵算子          | 作  用                                                       |        |
| ------------------- | ------------------------------------------------------------ | ------ |
| *dec                | 以十进制形式输出整数                                         | 常用   |
| hex                 | 以十六进制形式输出整数                                       |        |
| oct                 | 以八进制形式输出整数                                         |        |
| fixed               | 以普通小数形式输出浮点数                                     |        |
| scientific          | 以科学计数法形式输出浮点数                                   |        |
| left                | 左对齐，即在宽度不足时将填充字符添加到右边                   |        |
| *right              | 右对齐，即在宽度不足时将填充字符添加到左边                   |        |
| setbase(b)          | 设置输出整数时的进制，b=8、10 或 16                          |        |
| setw(w)             | 指定输出宽度为 w 个字符，或输人字符串时读入 w 个字符         |        |
| setfill(c)          | 在指定输出宽度的情况下，输出的宽度不足时用字符 c 填充（默认情况是用空格填充） |        |
| setprecision(n)     | 设置输出浮点数的精度为 n。  在使用非 fixed 且非 scientific 方式输出的情况下，n 即为有效数字最多的位数，如果有效数字位数超过 n，则小数部分四舍五人，或自动变为科学计 数法输出并保留一共 n 位有效数字。  在使用 fixed 方式和 scientific 方式输出的情况下，n 是小数点后面应保留的位数。 |        |
| setiosflags(flag)   | 将某个输出格式标志置为 1                                     |        |
| resetiosflags(flag) | 将某个输出格式标志置为 0                                     |        |
| boolapha            | 把 true 和 false 输出为字符串                                | 不常用 |
| *noboolalpha        | 把 true 和 false 输出为 0、1                                 |        |
| showbase            | 输出表示数值的进制的前缀                                     |        |
| *noshowbase         | 不输出表示数值的进制.的前缀                                  |        |
| showpoint           | 总是输出小数点                                               |        |
| *noshowpoint        | 只有当小数部分存在时才显示小数点                             |        |
| showpos             | 在非负数值中显示 +                                           |        |
| *noshowpos          | 在非负数值中不显示 +                                         |        |
| *skipws             | 输入时跳过空白字符                                           |        |
| noskipws            | 输入时不跳过空白字符                                         |        |
| uppercase           | 十六进制数中使用 A~E。若输出前缀，则前缀输出 0X，科学计数法中输出 E |        |
| *nouppercase        | 十六进制数中使用 a~e。若输出前缀，则前缀输出 0x，科学计数法中输出 e。 |        |
| internal            | 数值的符号（正负号）在指定宽度内左对齐，数值右对 齐，中间由填充字符填充。 |        |

 

使用这些算子的方法是将算子用 << 和 cout 连用。例如：

```
cout << hex << 12 << "," << 24;
```

这条语句的作用是指定以十六进制形式输出后面两个数，因此输出结果是：
c, 18

#### 8.easyx.h文件

+ 创建窗口 initgraph（）；括号里写界面的长和宽。
+ setbkcolor();设置背景颜色，括号里写颜色英文的大写
+ RGB(); 调色版括号里分别写red，green，blue的参数
+ 载入音乐

##### 9.malloc和new之间的区别

malloc/free和new/delete的区别\nmalloc/free和new/delete的共同点是：都是从堆上申请空间，并且需要用户手动释放。\n\n不同的地方是：\n\nmalloc和free是函数，new和delete是操作符\nmalloc申请的空间不会初始化，new可以初始化\nmalloc申请空间时，需要手动计算空间大小并传递，new只需在其后跟上空间的类型即可\nmalloc的返回值为void*, 在使用时必须强转，new不需要，因为new后跟的是空间的类型\nmalloc申请空间失败时，返回的是NULL，因此使用时必须判空，new不需要，但是new需要捕获异常\n申请自定义类型对象时，malloc/free只会开辟空间，不会调用构造函数与析构函数，而new在申请空间\n后会调用构造函数完成对象的初始化，delete在释放空间前会调用析构函数完成空间中资源的清理\nnew/delete比malloc和free的效率稍微低点，因为new/delete的底层封装了malloc/free

### 3.命名空间

#### 1.标准命名空间

+ C++标准头文件

iostream  iomanip  limit  fstream  string  typeinfo   stdexcept

+ C语言标准头文件

stdio.h  manth.h  asser.h  string.h  ctype.h

#### 2.定义命名空间

namespace 标识符

{ 语句序列 }

```c++
class SameName {//class关键字用于定义类类型
    ...
};

//lib1.h
namespace lib1
class SameName{
    .....
};
//lib2.h
namespace lib2
class SameName{
    .....
};


#include"lib1.h"
#include"lib2.h"
void UseSameName(){
	lib1::SameName one;//使用lib1库中定义的类
    lib2::SameName two;//使用lib2库中定义的类
}
```

#### 3.使用命名空间

using namespace 命名空间；

或 using 命名空间：：元素；

```c++
#include<iostream>
using namespace std;
namespace A
{
    viod f(){
        
    }
}
```

### 4.数组





### 5. 结构体

+ 用户可以自定义类型。

#### 1.原型.列子

```c++
#include<iostream>
#include<sting>
struct Student
{
	//成员列表
    string name;
    int age;
    int score;
}s3;//定义结构体，顺便创建结构体变量s3
//通过学生类型创建具体学生
//struct Student s1
struct Student s1;
//给s1属于赋值通过，访问结构体变量中的属性
s1.name = "张三";
s1.age = 18;
s1.score = 100;
//struct Stdent s2 = {李四，19，99}

```

#### 2.结构体数组和指针

``` c++
//结构体数组
struct student arr[3]=
{
    {"张三"，18，80}，
    {"李四"，19，90}，
    {"小黄"，20，100}
}；
```

``` c++
//结构体指针
struct student s = {"张三"，18，100}；
struct stduent *p = &s;//struct可以省略。
cout<<"姓名："<<p->name<<"年龄："<<p->age;
//通过结构体指针访问结构体中的属性，需要利用'->'。
```

``` c++
//结构体中嵌套结构体
struct student
{
    int age;
    string name;
    int score;
};
  struct teacher
  {
   	int id;
      string name;
      stdent stu[50];
};

```



#### 3.注意点

+ 1.结构体通过小标点.进行访问结构体里的元素。
+ 2.结构体的指针通过->符号来访问元素。

```c++
//在Teacher_加A或B。。。。
string nameSeed = "ABCDE";
tArray[i].tname = "Teacher_";
tarray[i].tname += nameSeed[i];

```



#### 4.结构体做函数参数

+ 作用：将结构体作为参数向函数中转递；
+ 方式1：值传递
+ 方式2：地址传递

``` c++
struct stdent
{
    string name;
    int age;
    int score;
};
int main(){
    struct student s;
    s.name = "张三";
    s.age = 20;
    s.age = 85;
    printfstudent1(s);
    printfstudent2(&s);
}
//值传递不改变参数
void printfstdent1(struct student s){
cout<<"子函数中"；
}
//地址传递,可以减少内存，可以改变参数
void printfstudent2(struct student *p){
cout<<"2";
}
```

### 6.字符串的比较

定义：**字符比较（character comparison）是指按照字典次序对单个字符或字符串进行比较大小的操作，一般都是以ASCII码值的大小作为字符比较的标准。**

#### 1.注意点

+ 1.**两个不同长度的字符串进行比较时，不是长的字符串就一定大**。如字符串s1为ABCE，字符串s2为ABCDEF。对 s1 与 s2 进行比较时，s1 的第4个字符是`E`，s2 的第4个字符是D，而D < E，所以s1 > s2。尽管 s2 比s1长。
+ 2.**当字符串有空格时，空格也参加比较**。如s1为 b ook(表示空格)，s2 为book，显示-79，故s1 < s2。
+ 3.**大写字母和小写字母的ASCII代码值是有区别的**，所以，yes> YEs。
+ 4.当字符串全部用英文字母的大写(或小写)组成时，字符串的大小顺序和它们在字典中的顺序相同
+ 5.**由汉字组成的字符串可以参加比较**。如李红< 王军。它们的大小实际是由其拼音构成的字符串的大小来决定的。上例即：LIHONG < WANGJUN。

#### 2.使用方法

+ 1.可以使用String类的**compareTo()**方法来实现。该方法用于判断一个字符串是大于、等于还是小于另一个字符串，返回int类型的差值。判断字符串大小的依据是它们在字典中的顺序。

``` c++
String s1 = "abc";
String s2 = "efg";
System.out.println(s1.compareTo(s2));
```

### 7.随机数

#### 1、线性同余法说明

+ 线性同余方法是目前应用广泛的伪随机数生成算法，其基本思想是通过对前一个数进行线性运算并取模从而得到下一个数，递归公式为：
  xn+1=(axn+c)　　mod(m)
  yn+1=xn+1/m
  其中a称为乘数，c称为增量，m称为模数，当a=0时为和同余法，当c=0时为乘同余法，c≠0时为混合同余法。 乘数、增量和模数的选取可以多种多样，只要保证产生的随机数有较好的均匀性和随机性即可，一般采用m=2km=2k混合同余法。
  + 线性同余法的最大周期是m，但一般情况下会小于m。要使周期达到最大，应该满足以下条件：
    (1) c和m互质；
    (2) m的所有质因子的积能整除a-1；
    (3) 若m是4的倍数，则a-1也是；
    (4) a，c，x0x0（初值，一般即种子）都比m小；
    (5) a，c是正整数。
  + 线性同余方法速度快，如果对乘数和模数进行适当的选择，可以满足用于评价一个随机数产生器的3 种准则：
    (1)这个函数应该是一个完整周期的产生函数。也就是说，这个函数应该在重复之前产生出0 到m之间的所有数；
    (2)产生的序列应该看起来是随机的；
    (3)这个函数应该用32bit 算术高效实现。

#### 2.例子

``` c++
function A=fangzheng3(a,c,m,x)
A=zeros(1000,1);
n=1;
while n<=1000
    n=n+1;
    x=rem((a*x+c),m);  %%rem(x,y):求整除x/y的余数
    y=x/m;
    A(n-1,1)=y;
End
```

#### 3.rand()和srand()函数的用法

##### 1、rand()

+ rand()函数用来产生随机数，但是，rand()的内部实现是用线性同余法实现的，是伪随机数，由于周期较长，因此在一定范围内可以看成是随机的。

+ rand()会返回一个范围在0到RAND_MAX（32767）之间的伪随机数（整数）。

+ 在调用rand()函数之前，可以使用srand()函数设置随机数种子，如果没有设置随机数种子，rand()函数在调用时，自动设计随机数种子为1。随机种子相同，每次产生的随机数也会相同。

+ rand()函数需要的头文件是：<stdlib.h>

+ rand()函数原型：int rand(void);

+ 使用rand()函数产生1-100以内的随机整数：int number1 = rand() % 100;

+ 使用时注意

  ``` c++
  #include<ctime>
  srand(unsigned int)time(NULL);
  int random = rand()%60;//0~59
  int random = rand()%60 + 40;//40~99
  ```

  

​	

##### 2、srand()

srand()函数需要的头文件仍然是：<stdlib.h>

srand()函数原型：void srand (usigned int seed);

srand()用来设置rand()产生随机数时的随机数种子。参数seed是整数，通常可以利用time(0)或geypid(0)的返回值作为seed。

使用rand()和srand()产生1-100以内的随机整数:srand(time(0));

    int number1 = rand() % 100;

##### 3、使用rand()和srand()产生指定范围内的随机整数的方法

“模除+加法”的方法

因为，对于任意数，0<=rand()%(n-m+1)<=n-m

因此，0+m<=rand()%(n-m+1)+m<=n-m+m

因此，如要产生[m,n]范围内的随机数num，可用：

int num=rand()%(n-m+1)+m;

其中的rand()%(n-m+1)+m算是一个公式，记录一下方便以后查阅。

比如产生10~30的随机整数：

srand(time(0));

int a = rand() % (21)+10

### 8.指针

#### 1.空指针

定义：指针变量指向内存中编号为0的空间

用途：初始化指针变量

注意：空指针指向的内存是不可以访问的

+ 如果对空指针使用delete运算符，系统将忽略该操作，不会出现异常。所以内存被释放后，也应该把指针指向空，表示没有指向任何地址。
+ int *p = NULL;  或int *p = 0; 

#### 2.野指针

+ 定义：指针变量指向非法的内存空间。
+ 注意：避免出现野指针。

#### 3.const修饰指针

+ const int *p = &a;//常量指针

  特点：**指针的指向可以修改，但是指针指向的值不可以改。**

+ int * const p = &a;//指针常量

  特点：**指针的指向不可以改，指针指向的值可以改。**

+ const int * const p = &a;

  特点：指针的指向和指向的值都不可以改。

+ 谁在前面谁不能改。



### 9.排序的五种方法

#### 1.冒泡排序

+ 适用于数据比较少的时候

```c++
public static void bubbleSort(int arr[]){
//判断数组为空或为一个元素的情况，即边界检查
    if(arr == null || arr.length < 2){
	return;
    }
    //规定每次俩俩比较的末尾元素的位置，最多为数组的最后位置
    for(int ebd = arr.length - 1; end > 0; end--){
		for(int i = 0; i < end; i++){
            if(arr[i] > arr[i + 1]){
				swap(arr[i],arr[i+ 1]);
            }
        }
    }
}
pubilc static viod swap(int arr[], int i, int j){
	int temp = arr[i];
    arr[i] = arr[j];
    arr[j] = temp;
}
```

``` c++
//外循环优化
int[] array = new int[] {5,2,3,9,4};
/*外循环为排序趟数，array.length个数进行array.length-1趟 */
for(int i=0;i<array.length-1;i++){
    boolean isSwap=false;
    /*内循环为每趟比较的次数，第i趟比较array.length-i次 */
    for(int j=0;j<array.length-1-i;j++){
        /*相邻元素比较，若满足条件则交换（升序为左大于右，降序反之） */
        if(array[j]>array[j+1]){
            int temp=array[j];
            array[j]=array[j+1];
            array[j+1]=temp;
            isSwap=true;
        }
        /*查看每趟比较后的数组元素*/
        System.out.println("第 "+(i+1)+" 趟，第 "+(j+1)+" 次比较后的结果：");
        for(int k=0;k<array.length;k++){
            System.out.print(array[k]+" ");
        }
        System.out.println();
    }
    /*如果没有交换过元素，则已经有序，不再进行接下来的比较*/
    if(!isSwap){
        break;
    }
}

//内循环优化
int[ ] array = new int[ ]{5,2,3,7,9};
int position = array.length - 1;
/*外循环为排序趟数，array.length个数进行array.length-1趟 */
for(int i = 0;i<array.length-1;i++){
    boolean isSwap = false;
    /*用来记录最后一次交换的位置*/
    int newPosition = 0;
    /*内循环为每趟比较的次数，第i趟比较array.length-i次 */
    for(int j = 0;j<position;j++){
        /*相邻元素比较，若满足条件则交换（升序为左大于右，降序反之） */
        if(array[j]>array[j+1]){
            int temp = array[j];
            array[j] = array[j+1];
            array[j+1] = temp;
            isSwap = true;
            /*记录最后一次交换的位置*/
            newPosition = j;
        }
        /*查看每趟比较后的数组元素*/
        System.out.println("第 "+(i+1)+" 趟，第 "+(j+1)+" 次比较后的结果：");
        for(int k = 0;k<array.length;k++){
            System.out.print(array[k]+" ");
        }
        System.out.println();
    }
    /*如果没有交换过元素，则已经有序，不再进行接下来的比较*/
    if(!isSwap){
        break;
    }
    /*下趟比较所需要比较到的位置*/
    position = newPosition;
}
```

```c++
//双向遍历（双向冒泡排序，鸡尾酒排序）
static void bubbleSort(int[] array) {
    int arrayLength = array.length;
    int preIndex = 0;
    int backIndex = arrayLength - 1;
    while(preIndex < backIndex) {
        preSort(array, arrayLength, preIndex);
        preIndex++;
        if (preIndex >= backIndex) {
            break;
        }
        backSort(array, backIndex);
        backIndex--;
    }
}

// 从前向后排序
static void preSort(int[] array, int length, int preIndex) {
    for (int i = preIndex + 1; i < length; i++) {
        if (array[preIndex] > array[i]) {
            swap(array, preIndex, i);
        }
    }
}

// 从后向前排序
static void backSort(int[] array, int backIndex) {
    for (int i = backIndex - 1; i >= 0; i--) {
        if (array[i] > array[backIndex]) {
            swap(array, i, backIndex);
        }
    }
}

static void swap (int[] arr, int i, int j) {
    int temp = arr[i];
    arr[i] = arr[j];
    arr[j] = temp;
}
```



#### 2.选择排序

+ 原理：第一次从待排序的数据元素中选出最小（最大）的一个元素，存放再序列的开始位置，然后再从剩下的未排序元素中寻找最小（最大）元素，继续放在起始位置，直到未排序元素个数为0。

```c++
 public static void selectionSort(int[] arr) {
  /*判断数组为空或为一个元素的情况，即边界检查*/
  if (arr == null || arr.length < 2) {
   return;
  }

  /*每次要进行比较的两个数，的前面那个数的下标*/
  for (int i = 0; i < arr.length - 1; i++) { 
   //min变量保存该趟比较过程中，最小元素所对应的索引，
   //先假设前面的元素为最小元素
   int minIndex = i;
   /*每趟比较，将前面的元素与其后的元素逐个比较*/
   for (int j = i + 1; j < arr.length; j++) {
    //如果后面的元素小，将后面元素的索引极为最小值的索引
    if(arr[j] < arr[minIndex]) {
     minIndex = j;
    }
   }
   //然后交换此次查找到的最小值和原始的最小值
   swap(arr, i, minIndex);
  }
 }

 public static void swap(int[] arr, int i, int j) {
  int tmp = arr[i];
  arr[i] = arr[j];
  arr[j] = tmp;
 }
```

```c++
//同时找出最大最小
 public static void selectionSort(int[] arr) {
  /*判断数组为空或为一个元素的情况，即边界检查*/
  if (arr == null || arr.length < 2) {
   return;
  }

  /*每次要进行比较的两个数，的前面那个数的下标*/
  for (int i = 0; i < arr.length - 1; i++) { 
   //min变量保存该趟比较过程中，最小元素所对应的索引，
   //先假设前面的元素为最小元素
   int minIndex = i;
   /*每趟比较，将前面的元素与其后的元素逐个比较*/
   for (int j = i + 1; j < arr.length; j++) {
    //如果后面的元素小，将后面元素的索引极为最小值的索引
    if(arr[j] < arr[minIndex]) {
     minIndex = j;
    }
   }
   //然后交换此次查找到的最小值和原始的最小值
   swap(arr, i, minIndex);
  }
 }

 public static void swap(int[] arr, int i, int j) {
  int tmp = arr[i];
  arr[i] = arr[j];
  arr[j] = tmp;
 }
```



#### 3.插入排序

+ 将初始数据分为有序部分和无序部分，每一步将一个无序部分的数据插入到前面已经排好序的有序部分中，直到插完所有元素为止。
+ 使用于排序序列元素个数不多且元素基本有序。

```c++
 public static void insertionSort(int[] arr) {
  if (arr == null || arr.length < 2) {
   return;
  }
  
  //每次将从0-i位置的元素进行排序
  for (int i = 1; i < arr.length; i++) { // 0 ~ i 做到有序
   //int j = i - 1; j >= 0表示左边位置的边界条件
   //arr[j] > arr[j + 1]表示最右边的数与相邻数的比较
   //j--表示将这个过程向左推进
   //swap(arr, j, j + 1)表示进行两个相邻数比较时，左边的数大于右边数时，才交换否则不交换
   for (int j = i - 1; j >= 0 && arr[j] > arr[j + 1]; j--) {
    swap(arr, j, j + 1);
   }
  }
 }

 public static void swap(int[] arr, int i, int j) {
  int tmp = arr[i];
  arr[i] = arr[j];
  arr[j] = tmp;
 }

```

``` c++
//折半插入排序
 public static void insertionSort(int[] arr) {
  if (arr == null || arr.length < 2) {
   return;
  }
  
  //每次将从0-i位置的元素进行排序
  for (int i = 1; i < arr.length; i++) { // 0 ~ i 做到有序
   //int j = i - 1; j >= 0表示左边位置的边界条件
   //arr[j] > arr[j + 1]表示最右边的数与相邻数的比较
   //j--表示将这个过程向左推进
   //swap(arr, j, j + 1)表示进行两个相邻数比较时，左边的数大于右边数时，才交换否则不交换
   for (int j = i - 1; j >= 0 && arr[j] > arr[j + 1]; j--) {
    swap(arr, j, j + 1);
   }
  }
 }

 public static void swap(int[] arr, int i, int j) {
  int tmp = arr[i];
  arr[i] = arr[j];
  arr[j] = tmp;
 }
```

```c++
//2-路插入排序
int j, first, last, mid;
/*临时数组*/
int[ ] tempArr =new int[len];        
tempArr[0] = arr[0];
/*first和last分别指临时数组tempArr中排好序的元素的第一个和最后一个位置*/
first = last = 0;       

for(int i = 1; i<len; i++){
    /*j 是调整系数*/
    if(first > last){
        j = len;        
    }else{
        j = 0;
    }
    /*tempArr中间元素的位置*/
    mid = ((first+last+j)/2)%len; 
    /*arr[i]应该插入在tempArr的前半部分*/
    if(arr[i] < tempArr[mid]){      
        /*j指向tempArr数组中的第一个元素*/
        j = first;    
        /*first 前移，取余是为了实现循环数组效果*/
        first = (first-1+len)%len;  
        /*待插元素大于 j 所指元素*/
        while(arr[i] > tempArr[j]){    
            /*j 所指元素前移，取余是为了实现循环数组效果*/
            tempArr[(j-1+len)%len] = tempArr[j];  
            /*j 指向下一个元素*/
            j = j+1;               
        }
        /*移动结束，待插元素插在tempArr[j]前*/
        tempArr[(j-1+len)%len] = arr[i];    
        /*arr[i]应该插入在tempArr的后半部分*/
    }else{   
        /*j指向tempArr数组中的最后一个元素*/
        j = last;    
        /*last后移， 指向插入后的最后一个元素*/
        last++;            
        /*待插元素小于 j 所指元素*/
        while(arr[i] < tempArr[j]){  
            /*j 所指元素后移*/
            tempArr[(j+1)%len] = tempArr[j]; 
            /*j 指向上一个元素*/
            j = (j-1+len)%len;         
        }
        /*移动结束，待插元素插在tempArr[j]后*/
        tempArr[(j+1)%len] = arr[i]; 
    }
}

/*把在tempArr中排好序的元素依次赋给arr*/
for(int i = 0; i < len; i++){                    
    arr[i] = tempArr[(first+i)%len];
}
```



 #### 4.快速排序

+ 每趟排序时选出一个基准值，然后将所有元素与该基准值比较，并按大小分成左右两堆，然后递归执行该过程，直到所有元素都完成排序。

> 1>先从数列中取出一个数作为基准数。
> 2>分区过程，将比这个数大的数全放到它的右边，小于或等于它的数全放到它的左边。
> 3>再对左右区间重复第二步，直到各区间只有一个数。

 ```c++
  public static void quickSort1(int[] arr) {
   if (arr == null || arr.length < 2) {
    return;
   }
   process1(arr, 0, arr.length - 1);
  }
 
  //第一版快排，这一版的时间复杂度为O(n2)
  public static void process1(int[] arr, int L, int R) {
   if (L >= R) {
    return;
   }
   //在[L,R]范围上，根据arr[R]，模仿netherlandsFlag方法，
   //将数组分为三个部分：<=arr[R]的部分，arr[R]本身，>=
   //arr[R]的部分，这样确定了在最终的数组中arr[R]的位置，
   //并返回这个位置
   int M = partition(arr, L, R);
   //接下来只要在左右两侧重复这个过程就行
   process1(arr, L, M - 1);
   process1(arr, M + 1, R);
  }
 
  public static int partition(int[] arr, int L, int R) {
   if (L > R) {
    return -1;
   }
   if (L == R) {
    return L;
   }
   int lessEqual = L - 1;
   int index = L;
   while (index < R) {
    if (arr[index] <= arr[R]) {
     swap(arr, index, ++lessEqual);
    }
    index++;
   }
   swap(arr, ++lessEqual, R);
   return lessEqual;
  }
 
  
  public static void quickSort2(int[] arr) {
   if (arr == null || arr.length < 2) {
    return;
   }
   process2(arr, 0, arr.length - 1);
  }
 
  //第二版快排：相比第一版的区别/优势：在于一次可以确定
  //相等基准值的一个区域，而不再只是一个值
  //第二版的时间复杂度为O(n2)
  public static void process2(int[] arr, int L, int R) {
   if (L >= R) {
    return;
   }
   int[] equalArea = netherlandsFlag(arr, L, R);
   process2(arr, L, equalArea[0] - 1);
   process2(arr, equalArea[1] + 1, R);
  }
  
  //这个方法的目的是按arr[R]为基准值，将arr数组划分为小于基准值、
  //等于基准值、大于基准值三个区域
  
  //在arr[L...R]上，以arr[R]做基准值，在[L...R]范围内，<arr[R]的数
  //都放在左侧，=arr[R]的数放在中间，>arr[R]的数放在右边
  //返回的值为和arr[R]相等的范围的数组
  public static int[] netherlandsFlag(int[] arr, int L, int R) {
   if (L > R) {
    return new int[] { -1, -1 };
   }
   if (L == R) {
    return new int[] { L, R };
   }
   //小于基准值的区域的右边界
   int less = L - 1;
   //大于基准值的区域的左边界
   int more = R;
   int index = L;
   while (index < more) {
    //等于基准值，不做处理，判断下一个数据
    if (arr[index] == arr[R]) {
     index++;
    //当前数小于基准值
    } else if (arr[index] < arr[R]) {
     //将当前值和小于区域右边的一个值交换：swap
     //判断下一个数据：index++
     //小于区域右移：++less（先++是为了完成swap）
     swap(arr, index++, ++less);
    } else {
     //将当前值和大于区域左边的一个值交换：swap
     //大于区域左移：--more（先--是为了完成swap）
     swap(arr, index, --more);
    }
   }
   //因为最开始是把arr[R]作为基准值的，所以在进行接下来的一步之前，
   //arr[R]实际是在大于区域的最右侧的，所以还需要进行一步交换，这样
   //整个数组就成了小于区域、等于区域、大于区域的样子
   swap(arr, more, R);
   //less + 1是等于区域的起始位置，more经过上一步的和arr[R]交换后，
   //就成了等于区域的结束位置
   return new int[] { less + 1, more };
  }
  
 
  public static void quickSort3(int[] arr) {
   if (arr == null || arr.length < 2) {
    return;
   }
   process3(arr, 0, arr.length - 1);
  }
 
  //第三版快排：不再固定去arr[R]，改为去随机位置的值，然后
  //和arr[R]进行交换，接下来的过程就和第二版一样
  
  //第三版的复杂度变化了，是O(nlogn)，该事件复杂度是最终求
  //的是数学上的一个平均期望值
  public static void process3(int[] arr, int L, int R) {
   if (L >= R) {
    return;
   }
   swap(arr, L + (int) (Math.random() * (R - L + 1)), R);
   int[] equalArea = netherlandsFlag(arr, L, R);
   process3(arr, L, equalArea[0] - 1);
   process3(arr, equalArea[1] + 1, R);
  }
 
  public static void swap(int[] arr, int i, int j) {
   int tmp = arr[i];
   arr[i] = arr[j];
   arr[j] = tmp;
  }
 ```



#### 5.希尔排序

```c++
    /*初始化划分增量*/
    int increment = len; 
    int j,temp,low,mid,high;
    /*每次减小增量，直到increment = 1*/
    while (increment > 1){ 
    /*增量的取法之一：除三向下取整+1*/
    increment = increment/3 + 1;
    /*对每个按增量划分后的逻辑分组，进行直接插入排序*/
    for (int i = increment; i < len; ++i) { 
    low = 0;
    high = i-1;
    temp = arr[i];
          while(low <= high){
             mid = (low+high)/2;
             if(arr[mid]>temp){
                 high = mid-1;
             }else{
                 low = mid+1;
             }
          }
          j = i-increment;
       /*移动元素并寻找位置*/
    while(j >= high+1){ 
    arr[j+increment] = arr[j];
    j -= increment;
    } 
    /*插入元素*/
    arr[j+increment] = temp; 
    }
    }
```



+ `const auto& element : array`是一个C++11中的范围for循环语法，也称为基于范围的for循环或foreach循环。它可以遍历一个容器中的所有元素，循环过程中自动获取容器中的元素，并将其存储到指定的变量中。

+ 在这个语法中，`const auto&`是一个类型推断的写法，它可以根据容器中的元素类型自动推断出变量的类型，并且变量是一个常量引用类型。`element`是程序员定义的变量名，它用于在循环体内访问当前遍历到的元素。`array`是要遍历的容器。

+ 此外，由于变量是一个常量引用类型，可以保证循环过程中容器中的元素不会被修改。如果需要修改容器中的元素，可以将`const`关键字删除，从而得到一个非常量引用类型的变量。

+ 这个语法可以替代传统的for循环语法，在某些情况下可以使代码更简洁易读。例如，在上面的示例代码中，我们可以使用范围for循环语法来遍历数组中的所有元素，如下所示：

```c++
cppCopy codefor (const auto& element : array) {
    total += element;
}
```

+ 这段代码的作用是计算数组中所有元素的总和，并且不需要显式地获取数组元素的下标。

### 10.哈希表

