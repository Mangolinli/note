### Java Number & Math类
+ 所有的包装类（Integer，Long Byte Double，Float，Short）都是抽象类Number的子类。

| 包装类       | 基本数据类型  |
| --------- | ------- |
| Boolean   | boolean |
| Byte      | byte    |
| Short     | short   |
| Integer   | int     |
| Long      | long    |
| Character | char    |
| Flota     | float   |
| Double    | double  |
![[Pasted image 20240304185415.png]]
+ Number 类属于 java.lang 包。
+ Java 的 Math 包含了用于执行基本数学运算的属性和方法，如初等指数、对数、平方根和三角函数。Math 的方法都被定义为 static 形式，通过 Math 类可以在主函数中直接调用。

| 序号  | 方法与描述                                                                                                                                                                      |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [xxxValue()](https://www.runoob.com/java/number-xxxvalue.html)  <br>将 Number 对象转换为xxx数据类型的值并返回。                                                                            |
| 2   | [compareTo()](https://www.runoob.com/java/number-compareto.html)  <br>将number对象与参数比较。                                                                                      |
| 3   | [equals()](https://www.runoob.com/java/number-equals.html)  <br>判断number对象是否与参数相等。                                                                                         |
| 4   | [valueOf()](https://www.runoob.com/java/number-valueof.html)  <br>返回一个 Number 对象指定的内置数据类型                                                                                  |
| 5   | [toString()](https://www.runoob.com/java/number-tostring.html)  <br>以字符串形式返回值。                                                                                             |
| 6   | [parseInt()](https://www.runoob.com/java/number-parseInt.html)  <br>将字符串解析为int类型。                                                                                          |
| 7   | [abs()](https://www.runoob.com/java/number-abs.html)  <br>返回参数的绝对值。                                                                                                        |
| 8   | [ceil()](https://www.runoob.com/java/number-ceil.html)  <br>返回大于等于( >= )给定参数的的最小整数，类型为双精度浮点型。                                                                              |
| 9   | [floor()](https://www.runoob.com/java/number-floor.html)  <br>返回小于等于（<=）给定参数的最大整数 。                                                                                        |
| 10  | [rint()](https://www.runoob.com/java/number-rint.html)  <br>返回与参数最接近的整数。返回类型为double。                                                                                       |
| 11  | [round()](https://www.runoob.com/java/number-round.html)  <br>它表示**四舍五入**，算法为 Math.floor(x+0.5)，即将原来的数字加上 0.5 后再向下取整，所以，Math.round(11.5) 的结果为12，Math.round(-11.5) 的结果为-11。 |
| 12  | [min()](https://www.runoob.com/java/number-min.html)  <br>返回两个参数中的最小值。                                                                                                     |
| 13  | [max()](https://www.runoob.com/java/number-max.html)  <br>返回两个参数中的最大值。                                                                                                     |
| 14  | [exp()](https://www.runoob.com/java/number-exp.html)  <br>返回自然数底数e的参数次方。                                                                                                   |
| 15  | [log()](https://www.runoob.com/java/number-log.html)  <br>返回参数的自然数底数的对数值。                                                                                                  |
| 16  | [pow()](https://www.runoob.com/java/number-pow.html)  <br>返回第一个参数的第二个参数次方。                                                                                                 |
| 17  | [sqrt()](https://www.runoob.com/java/number-sqrt.html)  <br>求参数的算术平方根。                                                                                                     |
| 18  | [sin()](https://www.runoob.com/java/number-sin.html)  <br>求指定double类型参数的正弦值。                                                                                               |
| 19  | [cos()](https://www.runoob.com/java/number-cos.html)  <br>求指定double类型参数的余弦值。                                                                                               |
| 20  | [tan()](https://www.runoob.com/java/number-tan.html)  <br>求指定double类型参数的正切值。                                                                                               |
| 21  | [asin()](https://www.runoob.com/java/number-asin.html)  <br>求指定double类型参数的反正弦值。                                                                                            |
| 22  | [acos()](https://www.runoob.com/java/number-acos.html)  <br>求指定double类型参数的反余弦值。                                                                                            |
| 23  | [atan()](https://www.runoob.com/java/number-atan.html)  <br>求指定double类型参数的反正切值。                                                                                            |
| 24  | [atan2()](https://www.runoob.com/java/number-atan2.html)  <br>将笛卡尔坐标转换为极坐标，并返回极坐标的角度值。                                                                                     |
| 25  | [toDegrees()](https://www.runoob.com/java/number-todegrees.html)  <br>将参数转化为角度。                                                                                            |
| 26  | [toRadians()](https://www.runoob.com/java/number-toradians.html)  <br>将角度转换为弧度。                                                                                            |
| 27  | [random()](https://www.runoob.com/java/number-random.html)  <br>返回一个随机数。                                                                                                   |

### Java Character类
+ Character 类用于对单个字符进行操作。Character 类在对象中包装一个基本类型 **char** 的值。
+ 将一个char类型的参数传递给需要一个Character类型参数的方法时，那么编译器会自动地将char类型参数转换为Character对象。 这种特征称为装箱，反过来称为拆箱。

| 转义序列 | 描述                                                                                          |
| ---- | ------------------------------------------------------------------------------------------- |
| \t   | 在文中该处插入一个tab键                                                                               |
| \b   | 在文中该处插入一个后退键                                                                                |
| \n   | 在文中该处换行                                                                                     |
| \r   | 在文中该处插入回车                                                                                   |
| \f   | 在文中该处插入换页符                                                                                  |
| \'   | 在文中该处插入单引号                                                                                  |
| \"   | 在文中该处插入双引号                                                                                  |
| \\   | 在文中该处插入反斜杠                                                                                  |
| 序号   | 方法与描述                                                                                       |
| 1    | [isLetter()](https://www.runoob.com/java/character-isletter.html)  <br>是否是一个字母              |
| 2    | [isDigit()](https://www.runoob.com/java/character-isdigit.html)  <br>是否是一个数字字符              |
| 3    | [isWhitespace()](https://www.runoob.com/java/character-iswhitespace.html)  <br>是否是一个空白字符    |
| 4    | [isUpperCase()](https://www.runoob.com/java/character-isuppercase.html)  <br>是否是大写字母        |
| 5    | [isLowerCase()](https://www.runoob.com/java/character-islowercase.html)  <br>是否是小写字母        |
| 6    | [toUpperCase()](https://www.runoob.com/java/character-touppercase.html)  <br>指定字母的大写形式      |
| 7    | [toLowerCase](https://www.runoob.com/java/character-tolowercase.html)()  <br>指定字母的小写形式      |
| 8    | [toString](https://www.runoob.com/java/character-tostring.html)()  <br>返回字符的字符串形式，字符串的长度仅为1 |

### Java String类
+ String 创建的字符串存储在公共池中，而 new 创建的字符串对象在堆上：
```java
String s1 = "Runoob";              // String 直接创建
String s2 = "Runoob";              // String 直接创建
String s3 = s1;                    // 相同引用
String s4 = new String("Runoob");   // String 对象创建
String s5 = new String("Runoob");   // String 对象创建
```
![[Pasted image 20240304191746.png]]
+ 如果需要对字符串做很多修改，那么应该选择使用 [StringBuffer & StringBuilder 类](https://www.runoob.com/java/java-stringbuffer.html "StringBuffer & StringBuilder 类")。
+ String 类的一个访问器方法是 length() 方法，它返回字符串对象包含的字符数。
+ String 类提供了连接两个字符串的方法：
```java
string1.concat(string2);
```
+ 更常用的是使用'+'操作符来连接字符串

| SN(序号) | 方法描述                                                                                                                                                                         |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1      | [char charAt(int index)](https://www.runoob.com/java/java-string-charat.html)  <br>返回指定索引处的 char 值。                                                                          |
| 2      | [int compareTo(Object o)](https://www.runoob.com/java/java-string-compareto.html)  <br>把这个字符串和另一个对象比较。                                                                       |
| 3      | [int compareTo(String anotherString)](https://www.runoob.com/java/java-string-compareto.html)  <br>按字典顺序比较两个字符串。                                                             |
| 4      | [int compareToIgnoreCase(String str)](https://www.runoob.com/java/java-string-comparetoignorecase.html)  <br>按字典顺序比较两个字符串，不考虑大小写。                                            |
| 5      | [String concat(String str)](https://www.runoob.com/java/java-string-concat.html)  <br>将指定字符串连接到此字符串的结尾。                                                                      |
| 6      | [boolean contentEquals(StringBuffer sb)](https://www.runoob.com/java/java-string-contentequals.html)  <br>当且仅当字符串与指定的StringBuffer有相同顺序的字符时候返回真。                              |
| 7      | [static String copyValueOf(char[] data)](https://www.runoob.com/java/java-string-copyvalueof.html)  <br>返回指定数组中表示该字符序列的 String。                                              |
| 8      | [static String copyValueOf(char[] data, int offset, int count)](https://www.runoob.com/java/java-string-copyvalueof.html)  <br>返回指定数组中表示该字符序列的 String。                       |
| 9      | [boolean endsWith(String suffix)](https://www.runoob.com/java/java-string-endswith.html)  <br>测试此字符串是否以指定的后缀结束。                                                              |
| 10     | [boolean equals(Object anObject)](https://www.runoob.com/java/java-string-equals.html)  <br>将此字符串与指定的对象比较。                                                                   |
| 11     | [boolean equalsIgnoreCase(String anotherString)](https://www.runoob.com/java/java-string-equalsignorecase.html)  <br>将此 String 与另一个 String 比较，不考虑大小写。                        |
| 12     | [byte[] getBytes()](https://www.runoob.com/java/java-string-getbytes.html)  <br> 使用平台的默认字符集将此 String 编码为 byte 序列，并将结果存储到一个新的 byte 数组中。                                       |
| 13     | [byte[] getBytes(String charsetName)](https://www.runoob.com/java/java-string-getbytes.html)  <br>使用指定的字符集将此 String 编码为 byte 序列，并将结果存储到一个新的 byte 数组中。                        |
| 14     | [void getChars(int srcBegin, int srcEnd, char[] dst, int dstBegin)](https://www.runoob.com/java/java-string-getchars.html)  <br>将字符从此字符串复制到目标字符数组。                           |
| 15     | [int hashCode()](https://www.runoob.com/java/java-string-hashcode.html)  <br>返回此字符串的哈希码。                                                                                     |
| 16     | [int indexOf(int ch)](https://www.runoob.com/java/java-string-indexof.html)  <br>返回指定字符在此字符串中第一次出现处的索引。                                                                      |
| 17     | [int indexOf(int ch, int fromIndex)](https://www.runoob.com/java/java-string-indexof.html)  <br>返回在此字符串中第一次出现指定字符处的索引，从指定的索引开始搜索。                                            |
| 18     | [int indexOf(String str)](https://www.runoob.com/java/java-string-indexof.html)  <br> 返回指定子字符串在此字符串中第一次出现处的索引。                                                               |
| 19     | [int indexOf(String str, int fromIndex)](https://www.runoob.com/java/java-string-indexof.html)  <br>返回指定子字符串在此字符串中第一次出现处的索引，从指定的索引开始。                                        |
| 20     | [String intern()](https://www.runoob.com/java/java-string-intern.html)  <br> 返回字符串对象的规范化表示形式。                                                                                |
| 21     | [int lastIndexOf(int ch)](https://www.runoob.com/java/java-string-lastindexof.html)  <br> 返回指定字符在此字符串中最后一次出现处的索引。                                                            |
| 22     | [int lastIndexOf(int ch, int fromIndex)](https://www.runoob.com/java/java-string-lastindexof.html)  <br>返回指定字符在此字符串中最后一次出现处的索引，从指定的索引处开始进行反向搜索。                              |
| 23     | [int lastIndexOf(String str)](https://www.runoob.com/java/java-string-lastindexof.html)  <br>返回指定子字符串在此字符串中最右边出现处的索引。                                                        |
| 24     | [int lastIndexOf(String str, int fromIndex)](https://www.runoob.com/java/java-string-lastindexof.html)  <br> 返回指定子字符串在此字符串中最后一次出现处的索引，从指定的索引开始反向搜索。                          |
| 25     | [int length()](https://www.runoob.com/java/java-string-length.html)  <br>返回此字符串的长度。                                                                                          |
| 26     | [boolean matches(String regex)](https://www.runoob.com/java/java-string-matches.html)  <br>告知此字符串是否匹配给定的正则表达式。                                                               |
| 27     | [boolean regionMatches(boolean ignoreCase, int toffset, String other, int ooffset, int len)](https://www.runoob.com/java/java-string-regionmatches.html)  <br>测试两个字符串区域是否相等。 |
| 28     | [boolean regionMatches(int toffset, String other, int ooffset, int len)](https://www.runoob.com/java/java-string-regionmatches.html)  <br>测试两个字符串区域是否相等。                     |
| 29     | [String replace(char oldChar, char newChar)](https://www.runoob.com/java/java-string-replace.html)  <br>返回一个新的字符串，它是通过用 newChar 替换此字符串中出现的所有 oldChar 得到的。                    |
| 30     | [String replaceAll(String regex, String replacement)](https://www.runoob.com/java/java-string-replaceall.html)  <br>使用给定的 replacement 替换此字符串所有匹配给定的正则表达式的子字符串。               |
| 31     | [String replaceFirst(String regex, String replacement)](https://www.runoob.com/java/java-string-replacefirst.html)  <br> 使用给定的 replacement 替换此字符串匹配给定的正则表达式的第一个子字符串。         |
| 32     | [String[] split(String regex)](https://www.runoob.com/java/java-string-split.html)  <br>根据给定正则表达式的匹配拆分此字符串。                                                                  |
| 33     | [String[] split(String regex, int limit)](https://www.runoob.com/java/java-string-split.html)  <br>根据匹配给定的正则表达式来拆分此字符串。                                                      |
| 34     | [boolean startsWith(String prefix)](https://www.runoob.com/java/java-string-startswith.html)  <br>测试此字符串是否以指定的前缀开始。                                                          |
| 35     | [boolean startsWith(String prefix, int toffset)](https://www.runoob.com/java/java-string-startswith.html)  <br>测试此字符串从指定索引开始的子字符串是否以指定前缀开始。                                  |
| 36     | [CharSequence subSequence(int beginIndex, int endIndex)](https://www.runoob.com/java/java-string-subsequence.html)  <br> 返回一个新的字符序列，它是此序列的一个子序列。                             |
| 37     | [String substring(int beginIndex)](https://www.runoob.com/java/java-string-substring.html)  <br>返回一个新的字符串，它是此字符串的一个子字符串。                                                     |
| 38     | [String substring(int beginIndex, int endIndex)](https://www.runoob.com/java/java-string-substring.html)  <br>返回一个新字符串，它是此字符串的一个子字符串。                                        |
| 39     | [char[] toCharArray()](https://www.runoob.com/java/java-string-tochararray.html)  <br>将此字符串转换为一个新的字符数组。                                                                      |
| 40     | [String toLowerCase()](https://www.runoob.com/java/java-string-tolowercase.html)  <br>使用默认语言环境的规则将此 String 中的所有字符都转换为小写。                                                     |
| 41     | [String toLowerCase(Locale locale)](https://www.runoob.com/java/java-string-tolowercase.html)  <br> 使用给定 Locale 的规则将此 String 中的所有字符都转换为小写。                                   |
| 42     | [String toString()](https://www.runoob.com/java/java-string-tostring.html)  <br> 返回此对象本身（它已经是一个字符串！）。                                                                        |
| 43     | [String toUpperCase()](https://www.runoob.com/java/java-string-touppercase.html)  <br>使用默认语言环境的规则将此 String 中的所有字符都转换为大写。                                                     |
| 44     | [String toUpperCase(Locale locale)](https://www.runoob.com/java/java-string-touppercase.html)  <br>使用给定 Locale 的规则将此 String 中的所有字符都转换为大写。                                    |
| 45     | [String trim()](https://www.runoob.com/java/java-string-trim.html)  <br>返回字符串的副本，忽略前导空白和尾部空白。                                                                                |
| 46     | [static String valueOf(primitive data type x)](https://www.runoob.com/java/java-string-valueof.html)  <br>返回给定data type类型x参数的字符串表示形式。                                        |
| 47     | [contains(CharSequence chars)](https://www.runoob.com/java/java-string-contains.html)  <br>判断是否包含指定的字符系列。                                                                    |
| 48     | [isEmpty()](https://www.runoob.com/java/java-string-isempty.html)判断字符串是否为空。                                                                                                  |
### # Java StringBuffer 和 StringBuilder 类
+ 由于 StringBuilder 相较于 StringBuffer 有速度优势，所以多数情况下建议使用 StringBuilder 类。StringBuilder自动增加新的空间，实际空间以增加的最大值为准。
![[Pasted image 20240304192249.png]]
+ StringBuffer 方法

| 序号  | 方法描述                                                                           |
| --- | ------------------------------------------------------------------------------ |
| 1   | public StringBuffer append(String s)  <br>将指定的字符串追加到此字符序列。                     |
| 2   | public StringBuffer reverse()  <br> 将此字符序列用其反转形式取代。                            |
| 3   | public delete(int start, int end)  <br>移除此序列的子字符串中的字符。                         |
| 4   | public insert(int offset, int i)  <br>将 `int` 参数的字符串表示形式插入此序列中。                |
| 5   | insert(int offset, String str)  <br>将 `str` 参数的字符串插入此序列中。                      |
| 6   | replace(int start, int end, String str)  <br>使用给定 `String` 中的字符替换此序列的子字符串中的字符。 |
+  StringBuffer 类的其他常用方法：

| 序号  | 方法描述                                                                                           |
| --- | ---------------------------------------------------------------------------------------------- |
| 1   | int capacity()  <br>返回当前容量。                                                                    |
| 2   | char charAt(int index)  <br>返回此序列中指定索引处的 `char` 值。                                             |
| 3   | void ensureCapacity(int minimumCapacity)  <br>确保容量至少等于指定的最小值。                                  |
| 4   | void getChars(int srcBegin, int srcEnd, char[] dst, int dstBegin)  <br>将字符从此序列复制到目标字符数组 `dst`。 |
| 5   | int indexOf(String str)  <br>返回第一次出现的指定子字符串在该字符串中的索引。                                          |
| 6   | int indexOf(String str, int fromIndex)  <br>从指定的索引处开始，返回第一次出现的指定子字符串在该字符串中的索引。                 |
| 7   | int lastIndexOf(String str)  <br>返回最右边出现的指定子字符串在此字符串中的索引。                                      |
| 8   | int lastIndexOf(String str, int fromIndex)  <br>返回 String 对象中子字符串最后出现的位置。                      |
| 9   | int length()  <br> 返回长度（字符数）。                                                                  |
| 10  | void setCharAt(int index, char ch)  <br>将给定索引处的字符设置为 `ch`。                                     |
| 11  | void setLength(int newLength)  <br>设置字符序列的长度。                                                  |
| 12  | CharSequence subSequence(int start, int end)  <br>返回一个新的字符序列，该字符序列是此序列的子序列。                    |
| 13  | String substring(int start)  <br>返回一个新的 `String`，它包含此字符序列当前所包含的字符子序列。                          |
| 14  | String substring(int start, int end)  <br>返回一个新的 `String`，它包含此序列当前所包含的字符子序列。                   |
| 15  | String toString()  <br>返回此序列中数据的字符串表示形式。                                                       |
更多内容：

- StringBuffer 类：[https://www.runoob.com/manual/jdk11api/java.base/java/lang/StringBuffer.html](https://www.runoob.com/manual/jdk11api/java.base/java/lang/StringBuffer.html)
- StringBuilder 类：[https://www.runoob.com/manual/jdk11api/java.base/java/lang/StringBuilder.html](https://www.runoob.com/manual/jdk11api/java.base/java/lang/StringBuilder.html)


### Java数组
+ 声明数组变量
```java
dataType[] arrayRefVar;   // 首选的方法
或
dataType arrayRefVar[];  // 效果相同，但不是首选方法
```
+ 创建数组
```java
arryRefVar = new dataType[arraySize];
//数组变量的声明，和创建数组
dataType[] arrayRefVar = new dataType[arraySize];
```
- 一、使用 dataType[arraySize] 创建了一个数组。
- 二、把新创建的数组的引用赋值给变量 arrayRefVar。


+ 数组的元素类型和数组的大小都是确定的，所以当处理数组元素时候，我们通常使用基本循环或者 For-Each 循环。
+ For-Each 循环或加强型循环：（就是迭代器循环）
```java
for(type element: array)
{
    System.out.println(element);
}
```
+ 数组可以作为参数传递给方法
```java
public static void printArray(int[] array) {
  for (int i = 0; i < array.length; i++) {
    System.out.print(array[i] + " ");
  }
}
```
+ 数组作为函数的返回值
```java
public static int[] reverse(int[] list) {
  int[] result = new int[list.length];
 
  for (int i = 0, j = result.length - 1; i < list.length; i++, j--) {
    result[j] = list[i];
  }
  return result;
}
```
+ 多维数组
```java
type[][] typeName = new type[typeLength1][typeLength2];

# 注意点
String[][] s = new String[2][];
s[0] = new String[2];
s[1] = new String[3];
s[0][0] = new String("Good");
s[0][1] = new String("Luck");
s[1][0] = new String("to");
s[1][1] = new String("you");
s[1][2] = new String("!");
```
+  Arrays 类
+ java.util.Arrays 类能方便地操作数组，它提供的所有方法都是静态的。

|序号|方法和说明|
|---|---|
|1|**public static int binarySearch(Object[] a, Object key)**  <br>用二分查找算法在给定数组中搜索给定值的对象(Byte,Int,double等)。数组在调用前必须排序好的。如果查找值包含在数组中，则返回搜索键的索引；否则返回 (-(_插入点_) - 1)。|
|2|**public static boolean equals(long[] a, long[] a2)**  <br>如果两个指定的 long 型数组彼此_相等_，则返回 true。如果两个数组包含相同数量的元素，并且两个数组中的所有相应元素对都是相等的，则认为这两个数组是相等的。换句话说，如果两个数组以相同顺序包含相同的元素，则两个数组是相等的。同样的方法适用于所有的其他基本数据类型（Byte，short，Int等）。|
|3|**public static void fill(int[] a, int val)**  <br>将指定的 int 值分配给指定 int 型数组指定范围中的每个元素。同样的方法适用于所有的其他基本数据类型（Byte，short，Int等）。|
|4|**public static void sort(Object[] a)**  <br>对指定对象数组根据其元素的自然顺序进行升序排列。同样的方法适用于所有的其他基本数据类型（Byte，short，Int等）。|

### Java日期时间
| 序号  | 方法和描述                                                                                                                                     |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | **boolean after(Date date)**  <br>若当调用此方法的Date对象在指定日期之后返回true,否则返回false。                                                                  |
| 2   | **boolean before(Date date)**  <br>若当调用此方法的Date对象在指定日期之前返回true,否则返回false。                                                                 |
| 3   | **Object clone( )**  <br>返回此对象的副本。                                                                                                        |
| 4   | **int compareTo(Date date)**  <br>比较当调用此方法的Date对象和指定日期。两者相等时候返回0。调用对象在指定日期之前则返回负数。调用对象在指定日期之后则返回正数。                                       |
| 5   | **int compareTo(Object obj)**  <br>若obj是Date类型则操作等同于compareTo(Date) 。否则它抛出ClassCastException。                                             |
| 6   | **boolean equals(Object date)**  <br>当调用此方法的Date对象和指定日期相等时候返回true,否则返回false。                                                              |
| 7   | **long getTime( )**  <br>返回自 1970 年 1 月 1 日 00:00:00 GMT 以来此 Date 对象表示的毫秒数。                                                               |
| 8   | **int hashCode( )**  <br> 返回此对象的哈希码值。                                                                                                     |
| 9   | **void setTime(long time)**  <br>   <br>用自1970年1月1日00:00:00 GMT以后time毫秒数设置时间和日期。                                                          |
| 10  | **String toString( )**  <br>把此 Date 对象转换为以下形式的 String： dow mon dd hh:mm:ss zzz yyyy 其中： dow 是一周中的某一天 (Sun, Mon, Tue, Wed, Thu, Fri, Sat)。 |
+  获取当前日期时间
```java
import java.util.Date;
  
public class DateDemo {
   public static void main(String[] args) {
       // 初始化 Date 对象
       Date date = new Date();
        
       // 使用 toString() 函数显示日期时间
       System.out.println(date.toString());
   }
}
```
t6[]