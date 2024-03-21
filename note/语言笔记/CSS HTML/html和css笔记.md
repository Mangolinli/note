### 1. 关于网站
1. 结构 （HTML）和 表现（CSS） 和 行为（JavaScript）。

### HTML
+ 全称：HyperText Markup Language(标记语言)
+ 就是一种超级文本
```html
<marquee> 开心就好！</marquee>
//前面<marrquee>是一个标签起始</marquee>是标签结束
//里面的marrquee叫做标签名，中间的“开心就好”叫做标签体
```
![[./picture/20230928004901.png]]
+ 规范小写，但是不分大小写
+ 不是所有的标签都是成对的。比如`<input>`
1. html的属性
	1. `loop=“1”`只循环一次
	2. `bgcolor="green"`背景颜色
	3. `type="password"`密码
	4. ![[Pasted image 20230928010125.png]]
	5. ![[Pasted image 20230928010444.png]]
2. 基本
	1. 注释
		1. 快捷键CTRL+ /或者CTRL+ K+C
		2. ![[Pasted image 20230928020353.png]]
	2. 文档声明
		1. `!DOCTYPE html`
		2. 是一种特殊的网页需要的，必须要有的。
	3. 字符编码
		1. ![[Pasted image 20230928021452.png]]
	4. 设置语言
		1. `<html lang="zh-CN">`
		2. ![[Pasted image 20230928022757.png]]
		3. 生成文件的快捷键shift+！
		4. 快速删除多行CTRL+shift+K
#### HTML笔记
1. **<!DOCTYPE html>** 声明为 HTML5 文档
    1. **<html>** 元素是 HTML 页面的根元素
     2. **<head>** 元素包含了文档的元（meta）数据，如 <meta charset="utf-8"> 定义网页编码格式为 **utf-8**。
     3. **<title>** 元素描述了文档的标题
     4. **<body>** 元素包含了可见的页面内容
     5. **<h1>** 元素定义一个大标题
     6. **<p>** 元素定义一个段落

2. 超链接

    ```html
    <a href="https://www.runoob.com">这是一个链接</a>
    ```

3. 加载图片

  ```	html
  1. <img decoding="async" src="/images/logo.png" width="258" height="39" />
  2. <hr> 标签在 HTML 页面中创建水平线。
  ```


####  截图
1. 定义内容
	1. 标签
		 ![[Pasted image 20231105174506.png]]
		 ![[Pasted image 20231105174843.png]]
	2. 引文标签定义
		1![[Pasted image 20231105174854.png]]
	3. 链接语法
		![[Pasted image 20231105180611.png]]
		![[Pasted image 20231105180655.png]]
	4. 图像
		![[Pasted image 20231105184722.png]]
	5. 表格
		![[Pasted image 20231105190625.png]]
		![[Pasted image 20231105191149.png]]
		![[Pasted image 20231105192441.png]]
		![[Pasted image 20231105192514.png]]
	6. 区块内联
		![[Pasted image 20231105192726.png]]
	7. 布局
		1. `div`
		``` html
		<!DOCTYPE html>
		<html>
		<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
		</head>
		<body>
		<div id="container" style="width:500px">

		<div id="header" style="background-color:#FFA500;">
		<h1 style="margin-bottom:0;">主要的网页标题</h1></div>
		
		<div id="menu" style="background-color:#FFD700;height:200px;width:100px;float:left;">
		<b>菜单</b><br>
		HTML<br>
		CSS<br>
		JavaScript</div>
		
		<div id="content" style="background-color:#EEEEEE;height:200px;width:400px;float:left;">
		内容在这里</div>
		
		<div id="footer" style="background-color:#FFA500;clear:both;text-align:center;">
		版权 © runoob.com</div>
		
		</div>
		 
		</body>
		</html>
		```
		2.  `table`
		```html
		<!DOCTYPE html>
		<html>
		<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
		</head>
		<body>
		
		<table width="500" border="0">
		<tr>
		<td colspan="2" style="background-color:#FFA500;">
		<h1>主要的网页标题</h1>
		</td>
		</tr>
		
		<tr>
		<td style="background-color:#FFD700;width:100px;vertical-align:top;">
		<b>菜单</b><br>
		HTML<br>
		CSS<br>
		JavaScript
		</td>
		<td style="background-color:#eeeeee;height:200px;width:400px;vertical-align:top;">
		内容在这里</td>
		</tr>
		
		<tr>
		<td colspan="2" style="background-color:#FFA500;text-align:center;">
		版权 © runoob.com</td>
		</tr>
		</table>
		
		</body>
		</html>
		```
	8. 表单
	![[Pasted image 20231105195220.png]]
	![[Pasted image 20231105195339.png]]
	![[Pasted image 20231105195409.png]]
	 1. 简单的下拉表
	 ```html
	 <!DOCTYPE html>
	<html>
	<head> 
	<meta charset="utf-8"> 
	<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	
	<form action="">
	<select name="cars">
	<option value="volvo">Volvo</option>
	<option value="saab">Saab</option>
	<option value="fiat">Fiat</option>
	<option value="audi">Audi</option>
	</select>
	</form>
	
	</body>
	</html>
	```
	 2. 预选下拉表
	 `<option value="fiat" selected>Fiat</option>`
	 3. 文本域
	 ```html
	 <textarea rows="10" cols="30">
	我是一个文本框。
	</textarea>
	```
	4. 按钮
	```html
	<form action="">
	<input type="button" value="Hello world!">
	</form>
	< !-- 此表单包含两个单选框和一个确认按钮。 --!>
	<form action="demo-form.php" method="get">
	  <input type="radio" name="sex" value="Male"> Male<br>
	  <input type="radio" name="sex" value="Female" checked="checked"> Female<br>
	  <input type="submit" value="提交">
	</form>
	```
	5. 复选框
	```html
	<form action="demo-form.php" method="get">
	  <input type="checkbox" name="vehicle[]" value="Bike"> I have a bike<br>
	  <input type="checkbox" name="vehicle[]" value="Car" checked="checked"> I have a car<br>
	  <input type="submit" value="提交">
	</form>
	```
	6. 从表单发送电子邮件
	```html
	<!DOCTYPE html>
	<html>
	<head> 
	<meta charset="utf-8"> 
	<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	
	<h3>发送邮件到 someone@example.com:</h3>
	
	<form action="MAILTO:someone@example.com" method="post" enctype="text/plain">
	Name:<br>
	<input type="text" name="name" value="your name"><br>
	E-mail:<br>
	<input type="text" name="mail" value="your email"><br>
	Comment:<br>
	<input type="text" name="comment" value="your comment" size="50"><br><br>
	<input type="submit" value="发送">
	<input type="reset" value="重置">
	</form>
	
	</body>
	</html>
	```
	![[Pasted image 20231105200525.png]]
	7. 颜色
	```html
	<p style="background-color:#FFFF00">
	通过十六进制设置背景颜色
	</p>
	
	<p style="background-color:rgb(255,255,0)">
	通过 rgb 值设置背景颜色
	</p>
	
	<p style="background-color:yellow">
	通过颜色名设置背景颜色
	</p>
	```
	8. 脚本
	![[Pasted image 20231105202357.png]]
	9.补录
	![[Pasted image 20231105232324.png]]
	![[Pasted image 20231105235737.png]]

### CSS
+  CSS 指层叠样式表 (**C**ascading **S**tyle **S**heets)
#### 笔记
1. 基本样板
	+ CSS 规则由两个主要的部分构成：选择器，以及一条或多条声明:
	+ 选择器通常是您需要改变样式的 HTML 元素。
	+ 每条声明由一个属性和一个值组成。
	+ 属性（property）是您希望设置的样式属性（style attribute）。每个属性有一个值。属性和值被冒号分开。
	+ 注释是用来解释你的代码，并且可以随意编辑它，浏览器会忽略它。CSS注释以 `/*` 开始, 以 `*/ `结束,
2.  id 和 class 选择器
	+ id 选择器
	1. id 选择器可以为标有特定 id 的 HTML 元素指定特定的样式。
	2. HTML元素以id属性来设置id选择器,CSS 中 id 选择器以 "#" 来定义。
	```css
	#para1
	{
	    text-align:center;
	    color:red;
	}
	```
	+ class选择器
	1. class 选择器用于描述一组元素的样式，class 选择器有别于id选择器，class可以在多个元素中使用。class 选择器在 HTML 中以 class 属性表示, 在 CSS 中，类选择器以一个点 .号显示。
	2. 你也可以指定特定的 HTML 元素使用 class。在以下实例中, 所有的 p 元素使用 class="center" 让该元素的文本居中:
	```css
	.center {text-align:center;}
	
	p.center {text-align:center;}
	```
3. CSS创建
	+ 外部样式表
		1. 当样式需要应用于很多页面时，外部样式表将是理想的选择。在使用外部样式表的情况下，你可以通过改变一个文件来改变整个站点的外观。每个页面使用 `<link>` 标签链接到样式表。 `<link>` 标签在（文档的）头部：
		```css
		<head>
		<link rel="stylesheet" type="text/css" href="mystyle.css">
		</head>
		```
		2. 浏览器会从文件 mystyle.css 中读到样式声明，并根据它来格式文档。外部样式表可以在任何文本编辑器中进行编辑。文件不能包含任何的 html 标签。样式表应该以 .css 扩展名进行保存。下面是一个样式表文件的例子：
		```css
		hr {color:sienna;}
		p {margin-left:20px;}
		body {background-image:url("/images/back40.gif");}
		```
	+ 内部样式表
		1. 当单个文档需要特殊的样式时，就应该使用内部样式表。你可以使用 `<style>` 标签在文档头部定义内部样式表，就像这样:
		```css
		<head>
		<style>
		hr {color:sienna;}
		p {margin-left:20px;}
		body {background-image:url("images/back40.gif");}
		</style>
		</head>
		```
		2. 内联样式:
			+ 由于要将表现和内容混杂在一起，内联样式会损失掉样式表的许多优势。请慎用这种方法，例如当样式仅需要在一个元素上应用一次时。
			+ 要使用内联样式，你需要在相关的标签内使用样式（style）属性。Style 属性可以包含任何 CSS 属性。本例展示如何改变段落的颜色和左外边距：
			```css
			<p style="color:sienna;margin-left:20px">这是一个段落。</p>
			```
	+ 多重样式
			1. 如果某些属性在不同的样式表中被同样的选择器定义，那么属性值将从更具体的样式表中被继承过来。
			2. 样式表允许以多种方式规定样式信息。
			+ 样式可以规定在单个的 HTML 元素中，在 HTML 页的头元素中，或在一个外部的 CSS 文件中。甚至可以在同一个 HTML 文档内部引用多个外部样式表。
			+ 一般情况下，优先级如下：
				**（内联样式）Inline style > （内部样式）Internal style sheet >（外部样式）External style sheet > 浏览器默认样式**
4. 背景(background)
	![[Pasted image 20231106161804.png]]
5. 文本（Text）
	![[Pasted image 20231106161928.png]]
6. 字体(fonts)
	![[Pasted image 20231106162212.png]]
7. 链接(link)
	![[Pasted image 20231106162251.png]]
8. 列表
	- 无序列表 ul - 列表项标记用特殊图形（如小黑点、小方框等）
	- 有序列表 ol - 列表项的标记有数字或字母
	- ```css
		ul { list-style-image: url('sqpurple.gif'); }
		```
	- ![[Pasted image 20231106162555.png]]
9. 表格(Table)
	+ 指定CSS表格边框，使用border属性。
	+ Width和height属性定义表格的宽度和高度。
	+ 表格中的文本对齐和垂直对齐属性。text-align属性设置水平对齐方式，向左，右，或中心：
10. 盒子模型
	+ 盒子模型![[Pasted image 20231106162808.png]]
	+ 元素的总高度最终计算公式是这样的：
		总元素的高度=高度+顶部填充+底部填充+上边框+下边框+上边距+下边距
11. 边框(Border)
	+ 例子
		![[Pasted image 20231106163511.png]]
	+ 例子2
		```html
		<!DOCTYPE html>
		<html>
		<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
		<style>
		p.none {border-style:none;}
		p.dotted {border-style:dotted;}
		p.dashed {border-style:dashed;}
		p.solid {border-style:solid;}
		p.double {border-style:double;}
		p.groove {border-style:groove;}
		p.ridge {border-style:ridge;}
		p.inset {border-style:inset;}
		p.outset {border-style:outset;}
		p.hidden {border-style:hidden;}
		p.mix {border-style: dotted dashed solid double;}
		</style>
		</head>
		
		<body>
		<p class="none">无边框。</p>
		<p class="dotted">虚线边框。</p>
		<p class="dashed">虚线边框。</p>
		<p class="solid">实线边框。</p>
		<p class="double">双边框。</p>
		<p class="groove"> 凹槽边框。</p>
		<p class="ridge">垄状边框。</p>
		<p class="inset">嵌入边框。</p>
		<p class="outset">外凸边框。</p>
		<p class="hidden">隐藏边框。</p>
		<p class="mix">混合边框</p>
		</body>
		
		</html>
		```
		+ 结果：
			![[Pasted image 20231106163641.png]]
	+ 边框宽度
		+ 您可以通过 border-width 属性为边框指定宽度。
		+ 为边框指定宽度有两种方法：可以指定长度值，比如 2px 或 0.1em(单位为 px, pt, cm, em 等)，或者使用 3 个关键字之一，它们分别是 thick 、medium（默认值） 和 thin。
	+ 边框颜色
		 ![[Pasted image 20231106163850.png]]
	+ 边框-单独设置各边
		![[Pasted image 20231106163938.png]]
		![[Pasted image 20231106163948.png]]
	+ 边框-简写属性
		![[Pasted image 20231106164034.png]]
	+ 总结
		![[Pasted image 20231106164116.png]]
12.  CSS 轮廓（outline）
	1.定义
		 ![[Pasted image 20231108170516.png]]
	 2.属性
		 ![[Pasted image 20231108170909.png]]
1. CSS margin(外边距)
	1. 定义
	![[Pasted image 20231108171012.png]]
	2. 可能的值
	![[Pasted image 20231108171107.png]]
	3. 单边外边距属性
		1. 
		```css
		margin-top:100px;
		margin-bottom:100px;
		margin-right:50px;
		margin-left:50px;
		```
		2. 简写属性
		```css
		margin:100px 50px;
		```
		3. 简写的具体属性属于谁？
		![[Pasted image 20231108171405.png]]
	4. 总结：
	![[Pasted image 20231108171447.png]]
14. padding（填充）
	1. 定义
	![[Pasted image 20231108181110.png]]
	2. 可能的值
	![[Pasted image 20231108181153.png]]
	3.属性的简写和上面的margin是一样的。
	![[Pasted image 20231108182349.png]]
15. CSS 分组 和 嵌套 选择器
	1. 分组选择器
	+ 在样式表中有很多具有相同样式的元素。为了尽量减少代码，你可以使用分组选择器。每个选择器用逗号分隔。
		```css
		h1 {
			color:green;
		}
		h2 {
			color:green;
		}
		p {
			color:green;
		}
		# 逗号隔开
		h1,h2,p
		{
			color:green;
		}
		```
	2. 嵌套选择器
	+ 它可能适用于选择器内部的选择器的样式。
		- `p{ }`: 为所有 **p** 元素指定一个样式。
		- `.marked{ }`: 为所有 **class="marked"** 的元素指定一个样式。
		- `.marked p{ }`: 为所有 **class="marked"** 元素内的 **p** 元素指定一个样式。
		- `p.marked{ }`: 为所有 **class="marked"** 的 **p** 元素指定一个样式。
	+ 例子
		```css
		p
		{
		    color:blue;
		    text-align:center;
		}
		.marked
		{
		    background-color:red;
		}
		.marked p
		{
		    color:white;
		}
		p.marked{
		    text-decoration:underline;
		}
		```
1.  尺寸 (Dimension)
	![[Pasted image 20231108183618.png]]
17. Display(显示) 与 Visibility（可见性）
	1.  隐藏元素 - display:none或visibility:hidden
	+ 隐藏一个元素可以通过把display属性设置为"none"，或把visibility属性设置为"hidden"。但是请注意，这两种方法会产生不同的结果。	
	+ visibility:hidden可以隐藏某个元素，但隐藏的元素仍需占用与未隐藏之前一样的空间。也就是说，该元素虽然被隐藏了，但仍然会影响布局。
	+ display:none可以隐藏某个元素，且隐藏的元素不会占用任何空间。也就是说，该元素不但被隐藏了，而且该元素原本占用的空间也会从页面布局中消失。
	+ 块元素是一个元素，占用了全部宽度，在前后都是换行符。
		块元素的例子：
		- `<h1>`
		- `<p>`
		- `<div>`	
	+ 内联元素只需要必要的宽度，不强制换行。
		内联元素的例子：
		- `<span>`
		- `<a>`
	+ 可以更改内联元素和块元素，反之亦然，可以使页面看起来是以一种特定的方式组合，并仍然遵循web标准。
		+ 下面的示例把列表项显示为内联元素：
		`li {display:inline;}`
		+ 下面的示例把span元素作为块元素：
		`span {display:block;}`
18. Position(定位)
	1. static 定位
		+ HTML 元素的默认值，即没有定位，遵循正常的文档流对象。
		+ 静态定位的元素不会受到 `top, bottom, left, right`影响。
		```css
		div.static {
		    position: static;
		    border: 3px solid #73AD21;
		}
		```
	2. fixed 定位
		+ 元素的位置相对于浏览器窗口是固定位置。
		即使窗口是滚动的它也不会移动：
		```css
		p.pos_fixed
		{
		    position:fixed;
		    top:30px;
		    right:5px;
		}
		```
		+ **注意：** Fixed 定位在 IE7 和 IE8 下需要描述 !DOCTYPE 才能支持。
		+ Fixed定位使元素的位置与文档流无关，因此不占据空间。
		+ Fixed定位的元素和其他元素重叠。
	3. relative 定位
		+ 相对定位元素的定位是相对其正常位置。
		```css
		h2.pos_left
		{
		    position:relative;
		    left:-20px;
		}
		h2.pos_right
		{
		    position:relative;
		    left:20px;
		}
		```
		+ 移动相对定位元素，但它原本所占的空间不会改变。
		```css
		h2.pos_top
		{
		    position:relative;
		    top:-50px;
		}
		```
		+ 相对定位元素经常被用来作为绝对定位元素的容器块。
	4. absolute 定位
		+ 绝对定位的元素的位置相对于最近的已定位父元素，如果元素没有已定位的父元素，那么它的位置相对于`<html>`:
		```css
		h2
		{
			position:absolute;
			left:100px;
			top:150px;
		}
		```
		+ `absolute` 定位使元素的位置与文档流无关，因此不占据空间。
		+ `absolute `定位的元素和其他元素重叠。
	5. sticky 定位
		+ `sticky` 英文字面意思是粘，粘贴，所以可以把它称之为粘性定位。
		+ `position: sticky;` 基于用户的滚动位置来定位。
		+ 粘性定位的元素是依赖于用户的滚动，在 **`position:relative`** 与 **`position:fixed`** 定位之间切换。
		+ 它的行为就像 **`position:relative;`** 而当页面滚动超出目标区域时，它的表现就像 **`position:fixed;`**，它会固定在目标位置。
		+ 元素定位表现为在跨越特定阈值前为相对定位，之后为固定定位。
		+ 这个特定阈值指的是` top`, `right,` `bottom` 或 `left` 之一，换言之，指定` top`, `right`, `bottom` 或` left` 四个阈值其中之一，才可使粘性定位生效。否则其行为与相对定位相同。
		+ **注意:** Internet Explorer, Edge 15 及更早 IE 版本不支持 sticky 定位。 Safari 需要使用 `-webkit- prefix` (查看以下实例)。
	6. 重叠的元素
		+ 元素的定位与文档流无关，所以它们可以覆盖页面上的其它元素z-index属性指定了一个元素的堆叠顺序（哪个元素应该放在前面，或后面）
		+ 一个元素可以有正数或负数的堆叠顺序：
		```css
		img
		{
		    position:absolute;
		    left:0px;
		    top:0px;
		    z-index:-1;
		}
		```
		+ 具有更高堆叠顺序的元素总是在较低的堆叠顺序元素的前面。
		+ **注意：** 如果两个定位元素重叠，没有指定`z - index`，最后定位在HTML代码中的元素将被显示在最前面。
	7. 总结

		|属性|说明|值|CSS|
		|:--|:--|:--|:--|
		|[bottom](https://www.runoob.com/cssref/pr-pos-bottom.html)|定义了定位元素下外边距边界与其包含块下边界之间的偏移。|auto  <br>_length  <br>%  <br>_inherit|2|
		|[clip](https://www.runoob.com/cssref/pr-pos-clip.html)|剪辑一个绝对定位的元素|_shape  <br>_auto  <br>inherit|2|
		|[cursor](https://www.runoob.com/cssref/pr-class-cursor.html)|显示光标移动到指定的类型|_url_  <br>auto  <br>crosshair  <br>default  <br>pointer  <br>move  <br>e-resize  <br>ne-resize  <br>nw-resize  <br>n-resize  <br>se-resize  <br>sw-resize  <br>s-resize  <br>w-resize  <br>text  <br>wait  <br>help|2|
		|[left](https://www.runoob.com/cssref/pr-pos-left.html)|定义了定位元素左外边距边界与其包含块左边界之间的偏移。|auto  <br>_length  <br>%  <br>_inherit|2|
		|[overflow](https://www.runoob.com/cssref/pr-pos-overflow.html)|设置当元素的内容溢出其区域时发生的事情。|auto  <br>hidden  <br>scroll  <br>visible  <br>inherit|2|
		|[overflow-y](https://www.runoob.com/css/cssref/css3-pr-overflow-y.html)|指定如何处理顶部/底部边缘的内容溢出元素的内容区域|auto  <br>hidden  <br>scroll  <br>visible  <br>no-display  <br>no-content|2|
		|[overflow-x](https://www.runoob.com/css/cssref//cssref/css3-pr-overflow-x.html)|指定如何处理右边/左边边缘的内容溢出元素的内容区域|auto  <br>hidden  <br>scroll  <br>visible  <br>no-display  <br>no-content|2|
		|[position](https://www.runoob.com/cssref/pr-class-position.html)|指定元素的定位类型|absolute  <br>fixed  <br>relative  <br>static  <br>inherit|2|
		|[right](https://www.runoob.com/cssref/pr-pos-right.html)|定义了定位元素右外边距边界与其包含块右边界之间的偏移。|auto  <br>_length  <br>%  <br>_inherit|2|
		|[top](https://www.runoob.com/cssref/pr-pos-top.html)|定义了一个定位元素的上外边距边界与其包含块上边界之间的偏移。|auto  <br>_length  <br>%  <br>_inherit|2|
		|[z-index](https://www.runoob.com/cssref/pr-pos-z-index.html)|设置元素的堆叠顺序|_number  <br>_auto  <br>inherit|2|
	
19.  Overflow
		1.  CSS overflow 属性可以控制内容溢出元素框时在对应的元素区间内添加滚动条。
		2. overflow属性有以下值：
		
			|值|描述|
			|---|---|
			|visible|默认值。内容不会被修剪，会呈现在元素框之外。|
			|hidden|内容会被修剪，并且其余内容是不可见的。|
			|scroll|内容会被修剪，但是浏览器会显示滚动条以便查看其余的内容。|
			|auto|如果内容被修剪，则浏览器会显示滚动条以便查看其余的内容。|
			|inherit|规定应该从父元素继承 overflow 属性的值。|
		3. **注意:**overflow 属性只工作于指定高度的块元素上。
		**注意:** 在 OS X Lion ( Mac 系统) 系统上，滚动条默认是隐藏的，使用的时候才会显示 (设置 "overflow:scroll" 也是一样的)。
