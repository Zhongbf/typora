

# HTML 基础

## HTML 简介

**什么是HTML？**

HTML 是用来描述网页的一种语言。

- HTML 是超文本标记语言（Hyper Text Markup Language）
- HTML 不是一种编程语言，而是一种标记语言 (markup language)
- 标记语言是一套标记标签 (markup tag)
- HTML 使用标记标签来描述网页

>超文本是什么：
>
>- 可以是有图片、声音、视频等内容，超越了文本的限制
>- 有超链接文本，可以跳转



HTML 文档 = 网页

- HTML 文档描述网页
- HTML 文档包含 HTML 标签和纯文本
- HTML 文档也被称为网页

网页是由图片、文字、声音、视频、超链接等元素构成网站页面。通常以`.htm` 或 `.html`后缀结尾，所以又叫做HTML文件。可以通过浏览器来打开

Web 浏览器的作用是读取 HTML 文档，并以网页的形式显示出它们。浏览器不会显示 HTML 标签，而是使用标签来解释页面的内容



**HTML 版本**

从 Web 诞生早期至今，已经发展出多个 HTML 版本：

| 版本      | 年份 |
| :-------- | :--- |
| HTML      | 1991 |
| HTML+     | 1993 |
| HTML 2.0  | 1995 |
| HTML 3.2  | 1997 |
| HTML 4.01 | 1999 |
| XHTML 1.0 | 2000 |
| HTML5     | 2012 |
| XHTML5    | 2013 |

声明HTML 5

~~~html
<!DOCTYPE html>
~~~

HTML 4.01

~~~html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
"http://www.w3.org/TR/html4/loose.dtd">
~~~



常用的浏览器

常用的五大浏览器

1. Edge浏览器

2. 火狐浏览器

3. 谷歌浏览器

4. Safari 浏览器

5. Opera 浏览器

查看浏览器市场份额网址：https://tongji.baidu.com/data/browser



浏览器内核（渲染引擎）：负责读取网页内容，整理讯息，计算网页的显示和显示页面

| 浏览器              | 内核           | 备注                |
| ------------------- | -------------- | ------------------- |
| firefox             | Gecko          | 火狐浏览器内核      |
| Safari              | Webkit         | 苹果浏览器内核      |
| Edge、chrome、Opera | Blink          | Blink是Webkit的分支 |
| 360、QQ、UC、搜狗   | Blink / Webkit |                     |

1.3 Web 标准

Web 标准是由W3C组织和其他标准化组织制定的一系列标准的集合。W3C（万维网）是国际最著名的标准化组织



浏览器不同，显示的页面和排版有差异。遵循Web标准有许多的优点

1、 让Web 的发展前景更广阔

2、网页在浏览器更兼容

3、更容易被搜索引擎搜索

4、网站容易维护

5、提高浏览速度



Web 标准的构成

主要包括结构（Structure）、表现（Presentation）、和行为（Behavior）

| 标准 | 说明                                                        |
| ---- | ----------------------------------------------------------- |
| 结构 | 结构用于对网页元素进行分类，就是HTML                        |
| 表现 | 表现用于设置网页元素的版式、颜色、大小等外观样式，主要指CSS |
| 行为 | 行为是指网页模型的定义及交互的编写，主要指Javascript        |

Web 标准提出的最佳体验方案：结构、样式、行为分离（就是HTML用HTML文件、CSS用CSS文件、JS用JS文件）







## HTML 编辑器

我们可以使用专业的编辑器来进行开发来增加效率。如DW、Sublime、WebStorm、HBuilder、VS Code

在学习阶段可以使用 Notepad ++ (PC) 或 TextEdit (Mac)

甚至可以使用笔记本来编辑HTML，打开笔记本

~~~html
<!DOCTYPE HTML>
<html>
    <body>
        <h1>第一个网页</h1>
        <p>Hello,world</p>
    </body>
</html
~~~

把文档后缀名保存为`.html`或者`.htm`。然后用浏览器打开就是简单的网页了

**VS Code的使用**

`CTRL +`：放大页面   

`CTRL -`：缩小页面   

`! + Tab`可以快速生成基本结构

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
~~~



## HTML 元素

HTML 文档（网页）是由HTML 元素定义的

HTML元素指从开始标签到结束标签的所有代码，如：`<p>我是一个段落</p>`

**HTML元素语法**

- HTML 元素以开始标签起始，HTML 元素以结束标签终止，这样的标签也叫双标签。如`<p></p>`
- 元素的内容是开始标签与结束标签之间的内容
- 有些 HTML 元素是空内容，这样的标签也叫做单标签。如`<br />`
- 大多数 HTML标签拥有属性

**嵌套的 HTML 元素**

大多数的 HTML 元素可以嵌套

**HTML 元素示例**

~~~html
<html>
    <head>First</head>
    <body>
        <p>this is a paragraph</p>
    </body>
</html>
~~~

`<html>`元素 定义了整个HTML 文档

`<body>`元素定义HTML文档的主题

`<p>`元素定义了一个段落，元素内容是this is a paragraph

**不要忘记结束标签**

即使您忘记了使用结束标签，大多数浏览器也会正确地显示 HTML，但不要依赖这种做法。忘记使用结束标签会产生不可预料的结果或错误。未来的 HTML 版本不允许省略结束标签

**空的 HTML 元素**

`<br />`换行标签就是一个空元素，没有元素内容，空元素是在开始标签中关闭的

单标签不关闭`<br>`也是有效的，但是在 XHTML、XML 以及未来版本的 HTML 中，所有元素都必须被关闭，所有尽量所有的标签都要求关闭

> HTML提示：使用小写标签
>
> HTML 标签对大小写不敏感：<P> 等同于 <p>。许多网站都使用大写的 HTML 标签。
>
> W3School 使用的是小写标签，因为万维网联盟（W3C）在 HTML 4 中推荐使用小写，而在未来 (X)HTML 版本中强制使用小写。



HTML 属性

HTML 标签可以拥有属性。属性提供了有关 HTML 元素的更多的信息。

属性总是以名称/值对的形式出现，比如：name="value"。

属性总是在 HTML 元素的开始标签中规定。

**属性示例**

HTML 链接由 <a> 标签定义。链接的地址在 href 属性中指定：

~~~html
<a href="https://baidu.com">百度</a>
~~~

**为属性值加引号**

属性值应该全部被加引号，常用的是双引号，比如属性值本身就含有双引号，那么您必须使用单引号

~~~html
name=’I am “Jack”‘
~~~

**常用的HTML属性**

| 属性  | 属性值    | 描述                                     |
| ----- | --------- | ---------------------------------------- |
| class | className | 规定元素的类名                           |
| id    | idName    | 规定唯一的id名                           |
| style |           | 规定元素的行内样式（inline style）       |
| title | text      | 规定元素的额外信息（可在工具提示中显示） |



## HTML 标题

标题（Heading）是通过` <h1> - <h6>` 等标签进行定义的。

`<h1>` 定义最大的标题。`<h6>` 定义最小的标题。

~~~html
<h1>一级标题</h1>
<h2>二级标题</h2>
...
<h6>六级标题</h6>
~~~

标题是块级元素，，默认情况下会加粗变大，会在块级元素前后添加空行

**标题很重要**

请确保将 HTML heading 标签只用于标题。不要仅仅是为了产生粗体或大号的文本而使用标题。

搜索引擎使用标题为您的网页的结构和内容编制索引。

因为用户可以通过标题来快速浏览您的网页，所以用标题来呈现文档结构是很重要的。



### HTML 水平线

`<hr /> `标签在 HTML 页面中创建水平线。可用于分隔内容。



## HTML 段落

段落是通过`<p>`标签定义的

~~~html
<p>This is a paragraph</p>
<p>This is another paragraph</p>
~~~

`<p>`是块级元素，浏览器会自动地在段落前后添加空行



### HTML 换行

如果你像在不用新段落地情况下换行，可以使用`<br /`标签，它是一个空元素（单标签），没有结束标签

~~~html
<p>This is<br />a para<br />graph with line breaks</p>
~~~



**`<br>` 还是` <br />`**

- 即使` <br>` 在所有浏览器中的显示都没有问题，使用 `<br />` 也是更长远的保障。
- 在 XHTML、XML 以及未来的 HTML 版本中，不允许使用没有结束标签（闭合标签）的 HTML 元素。



### HTML 输出

HTML 中连续地空格和换行都会算作一个，代码中的所有连续的空行（换行）也被显示为一个空格。



## HTML 样式

style属性可以在HTML 里改变元素的样式

~~~html
<html>
    <body style="background-color:red;font-family:arial">
        <p style="text-align:center">
            This text is center
        </p>
    </body>
</html>
~~~



## HTML 文本格式化

| 标签       | 描述                             |
| ---------- | -------------------------------- |
| `<b>`      | 定义粗体文本                     |
| `<strong>` | 定义重要文本                     |
| `<em>`     | 定义着重文字；浏览器一般当作斜体 |
| `<i>`      | 定义斜体文本，斜体建议用这个     |
| `<del>`    | 删除线；不赞成使用 `<s>`         |
| `<ins>`    | 下划线 ；不赞成使用 `<u>`        |
| `<sub>`    | 定义下标字                       |
| `<sup>`    | 定义上标字                       |

这些标签会呈现出特殊的样式，拥有确切的语义。如果为了让代码更具有语义化，可以使用它们，但是如果想要达到某种样式的情况下，建议使用CSS



## HTML 计算机代码

| 标签     | 描述               |
| -------- | ------------------ |
| `<code>` | 定义计算机代码     |
| `<kbd>`  | 定义键盘码         |
| `<samp>` | 定义计算机代码样本 |
| `<tt>`   | 定义打字机代码     |
| `<var>`  | 定义变量           |
| `<pre>`  | 定义预格式文本     |



## HTML 引用

**短的引用**

`<q>`标签用于短的引用，浏览器会为`<q>`元素包围引号

~~~html
<p>WWF 的目标是：<q>构建人与自然和谐共存的世界。</q></p>
<!--WWF 的目标是“构建人与自然和谐相处的世界。”-->
~~~

**长的引用**

`<blockquote>`标签定义长引用，浏览器通常会对 `<blockquote> `元素进行缩进处理。

~~~html
<p>以下内容引用自 WWF 的网站：</p>
<blockquote cite="http://www.worldwildlife.org/who/index.html">
五十年来，WWF 一直致力于保护自然界的未来。
世界领先的环保组织，WWF 工作于 100 个国家，
并得到美国一百二十万会员及全球近五百万会员的支持。
</blockquote>
~~~

**首字母缩略词**

` <abbr>` 元素定义缩写或首字母缩略语。对缩写进行标记能够为浏览器、翻译系统以及搜索引擎提供有用的信息。

~~~html
<p><abbr title="World Health Organization">WHO</abbr> 成立于 1948 年。</p>
~~~

` <dfn>` 元素定义项目或缩写的定义，可以用addr代替

~~~html
<p><dfn title="World Health Organization">WHO</dfn> 成立于 1948 年。</p>
~~~

**联系信息**

`<address>` 元素定义文档或文章的联系信息（作者/拥有者）。此元素通常以斜体显示。大多数浏览器会在此元素前后添加折行。

~~~html
<address>
Written by Donald Duck.<br> 
Visit us at:<br>
Example.com<br>
Box 564, Disneyland<br>
USA
</address>
~~~

**著作标题**

`<cite>` 元素定义著作的标题。浏览器通常会以斜体显示

~~~html
<p><cite>The Scream</cite> by Edward Munch. Painted in 1893.</p>
~~~

**定义文本方向**

`<bdo>`定义文本方向

~~~html、
<bdo dir="rtl">This text will be written from right to left</bdo>
~~~



## HTML 注释和特殊字符

HTML注释标签`<!-- -->`，注释浏览器不会显示，用来

~~~html
<!-- 在此处写注释 -->
<!-- 
  This is a long comment example. This is a long comment example. This is a long comment 
  This is a long comment example. This is a long comment example. This is a long comment 
-->
~~~

>合理地使用注释可以对未来维护代码产生帮助。

**特殊字符**

| 特殊字符 | 描述     | 字符的代码 |
| -------- | -------- | ---------- |
|          | 空格     | `&nbsp;`   |
| <        | 小于号   | `&lt;`     |
| >        | 大于号   | `&gt;`     |
| &        | 和       | `&amp;`    |
| ￥       | 人民币   | `&yen;`    |
| ©        | 版权     | `&copy;`   |
| ®        | 注册商标 | `&reg;`    |
| ℃        | 摄氏度   | `&deg;`    |
| ±        | 正负号   | `&plusmn;` |
| ✖        | 乘号     | `&times;`  |
| ➗        | 除号     | `&divide;` |
| ^2^      | 平方2    | `&sup2;`   |
| ^3^      | 平方3    | `&sup3;`   |



## HTML 颜色

HTML 颜色的两种方式

1. 十六进制：黑色：`#000000`；白色：`#ffffff`
2. 颜色名

>提示：仅仅有 16 种颜色名被 W3C 的 HTML4.0 标准所支持。它们是：aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, yellow



## HTML CSS

HTML使用CSS有三种方法：

- 外部样式表
- 内部样式表
- 内联样式

**外部样式表**

这是建议使用的方式，可以使HTML和CSS分离，样式表可以被多个页面引用

~~~html
<head>
    <link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
~~~

**内部样式表**

当单个文件需要特别样式时，就可以使用内部样式表。你可以在 head 部分通过 `<style>` 标签定义内部样式表。内部样式表只能被当前页面使用，HTML和CSS在同一个页面，增加维护难度

~~~html
<head>
	<style type="text/css">
        body {background-color: red}
		p {margin-left: 20px}
    </style>
</head>
~~~

**内联样式**

当特殊的样式需要应用到个别元素时，就可以使用内联样式。使用内联样式的方法是在相关的标签中使用样式属性。样式属性可以包含任何 CSS 属性

~~~html
<p style="color:red;margin-left:5px">This is paragrapg</p>
~~~



## HTMl 超链接

使用` <a>` 标签在 HTML 中创建链接

有两种使用` <a>` 标签的方式：

1. 通过使用 href 属性 - 创建指向另一个文档的链接
2. 通过使用 name 属性 - 创建文档内的书签（描点）

~~~html
<a href="url" target="窗口的跳转方式">文本或者图像</a>
~~~

a标签的属性

| 属性   | 作用                                                         |
| ------ | ------------------------------------------------------------ |
| href   | href 属性规定链接的目标                                      |
| target | 指定链接页面打开方式，`_self`是默认值，在当前窗口打开，`_blank`在新窗口打开 |



打开外部链接

~~~html
<a href="https://baidu.com/" target=“_blank”>百度</a>
~~~

打开内部链接

~~~html
<a href="index.html">内部链接</a>
~~~

空链接

~~~html
<a href="#"></a>
~~~

下载链接

~~~html
<a href="a.zip"></a>
~~~

> 提示：
>
> 超链接的地址要用斜杠`/`结尾，不加服务器会自动添加，这样就向服务器请求两次了



**描点链接**

点击链接可以快速定位到页面的某个位置（锚的位置），多数用于大型文档的目录，如百度百科

命名一个锚

~~~html
<a name="1">锚：1111111</a>
<!-- 可以使用 id 属性来替代 name 属性，命名锚同样有效。如果不是 a 标签，必须用 id 属性 -->
<span id="1111">锚：1111111111</span>
~~~

然后在同一个文档中创建指向该锚的链接

~~~html
<a href="#1">1111111</a>
<!-- 在另外的文档创建也可以，锚名称添加到 URL 的末端 -->
<a href="http://www.baidu.com.cn/index.html#tips">111111</a>
~~~



## HTML 图像标签

在 HTML 中，图像由 `<img>` 标签定义。

`<img> `是空标签，意思是说，它只包含属性，并且没有闭合标签。

要在页面上显示图像，你需要使用源属性（src）。src 指 "source"。源属性的值是图像的 URL 地址

~~~html
<img src="url" />
~~~

URL 指存储图片的地址，可以相对地址或绝对地址

图像标签的其他属性：

| 属性   | 属性值   | 说明                               |
| ------ | -------- | ---------------------------------- |
| src    | 图片路径 | 必选                               |
| alt    | 文本     | 替换文本，图片失效时显示的文字     |
| title  | 文本     | 提示文本，鼠标放到图像上显示的文字 |
| width  | 像素     | 设置图像的宽度                     |
| height | 像素     | 设置图像的高度                     |
| border | 像素     | 设置图像的边框                     |



## HTML 表格

1、表格由` <table></table>` 标签来定义，表格用来展示数据，不建议用table来布局

2、表格的的行由`<tr></tr>`标签定义，嵌套在`<table>`标签内

3、每行被分割为若干单元格，由 `<td> `标签定义，嵌套在`<tr>`标签内。字母 td 指表格数据（table data）

4、`<thead>/<tbody>/<tfoot>`对应了表格的3个部分，使表格结构清晰，如果您使用 thead、tfoot 以及 tbody 元素，您就必须使用全部的元素。它们的出现次序是：thead、tfoot、tbody，这样浏览器就可以在收到所有数据前呈现页脚了。您必须在 table 元素内部使用这些标签

~~~html
<table>
    <thead>
    	<tr>
        	<th>姓名</th>
            <th>年龄</th>
        </tr>
    </thead>
    <tbody>
        <tr>
    		<td>Kobe</td>
        	<td>24</td>
    	</tr>
    </tbody>
    <tfoot>
        <tr>
    		<td>&nbsp;</td>
        	<td>&nbsp;</td>
    	</tr>
    </tfoot>
</table>
~~~

> 空单元格：`<td>&nbsp;</td>`

**表格的表头**

`<th>`是表头单元格，也是嵌套在`<tr>`标签内，th（table head）大多数浏览器会把表头显示为粗体居中的文本

~~~html
<table>
    <tr>
    	<th>姓名</th>
        <th>年龄</th>
    </tr>
    <tr>
    	<td>Kobe</td>
        <td>24</td>
    </tr>
</table>
~~~

**表格属性**

一般通过CSS来实现

如果写在HTML里，就要写在在table标签里面

| 属性名      | 属性值              | 说明             |
| ----------- | ------------------- | ---------------- |
| align       | left、center、right | 对齐方式         |
| border      | 0或者1（像素）      | 表格边框         |
| cellpadding | 像素值              | 单元格的内边距， |
| cellspacing | 像素值              | 单元格之间的间距 |
| width       | 像素值或者百分比    | 规定表格的宽度   |

~~~html
<table border=“0”>
    <tr>
    	<th>姓名</th>
        <th>年龄</th>
    </tr>
    <tr>
    	<td>Kobe</td>
        <td>24</td>
    </tr>
</table>
~~~

**合并单元格**
1、找到目标单元格（最左或最上的单元格）

2、合并行用colspan，合并列用rowspan

3、删除多余的单元格

~~~html
<table border="1" cellspacing="0" width="500" height="500">
    <caption>合并单元格</caption>
    <tr>
        <th>name</th>
        <th>age</th>
        <th>gender</th>
    </tr>
    <tr>
        <td>Kobe</td>
        <td colspan="2">24</td>
        <!-- <td>男</td> -->
    </tr>
    <tr>
        <td>Jack</td>
        <td rowspan="2">22</td>
        <td>男</td>
    </tr>
    <tr>
        <td>Aniie</td>
        <!-- <td>6</td> -->
        <td>女</td>
    </tr>
</table>
~~~



## HTML 列表

HTML的列表用来布局，列表分为有序列表、无序列表和自定义列表

**无序列表**

1、无序列表的列表项是无序的、并列的，项目符号是原点，`type=disc`来设置

2、`<ul>`中只能嵌套`<li>`，不能有其他的标签或者文字

3、`<li>`相当于一个容器，可以放其他的标签

4、项目中列表中的默认样式会去除掉，主要用来布局

~~~html
<ul>
	<li>Kobe</li>
    <li>Jack</li>
    <li>Annie</li>
</ul>
~~~

- Kobe
- Jack
- Annie

**有序列表**

用`<ol></ol>`来定义有序列表，`<li></li>`来定义列表项

前面的项目符号是123

~~~html
<ol>
	<li>一</li>
    <li>二</li>
    <li>三</li>
</ol>
1. 一
2. 二
3. 三
~~~



**自定义列表**

自定义列表常用于对项目的解释和描述，没有项目符号

1、用`<dl>`标签定义自定义列表，`<dt>`定义项目，`<dd>`定义项目数据，一起使用

~~~html
<dl>
    <dt>项目1</dt>
    <dd>项目数据1</dd>
    <dd>项目数据2</dd>
</dl>
~~~



## HTML 块元素和内联元素

**块级元素**

大多数 HTML 元素被定义为块级元素（ block level element）或内联元素（inline element）。

块级元素在显示时，通常独占一行，如`<h1>, <p>, <ul>, <table>`

**内联元素（行内元素）**

内联元素在显示时通常不会以新行开始

如：`<b>, <td>, <a>, <img>`



**`<div>`元素和`<span>`元素**

div和span标签没有语义，它是一个盒子，用来布局

` <div>` 元素是块级元素，它是可用于组合其他 HTML 元素的容器。

` <span>` 元素是内联元素，可用作文本的容器。

~~~html
<div>
    <span>1</span>
    <span>2</span>
    <span>3</span>
</div>
<div>4</div>
~~~



## HTML 的 class 和 id

对HTML 元素设置 class 和 id，然后可以为元素设置样式

HTML class 可以重复设置，也可以设置多个

id 属性的值在 HTML 文档中必须是唯一的，id 属性的值区分大小写，id 属性还可用于创建 HTML 书签（锚点）

~~~html
<div class="number">
    <span id="one">1</span>
    <span>2</span>
    <span>3</span>
</div>
<div class="number">4</div>
~~~

class可以用`.number{}`调用

id可以用`#one{}`调用



## HTML 路径

**相对路径**

相对路径指向相对当前页面的文件

~~~html
<img src="../images/picture.jpg" alt=“flower” /> 
~~~

**绝对路径**

绝对路径指一个文件的完整路径，通常是从盘符开始的路径或者完整的网络路径

~~~html
<img src="D:\a\b\c.png" alt="a"/>
<img src="https://www.baidu.com/images/a.png" alt="a" />
~~~



## HTML 头部

HTML 的 `<head>`元素是所有头部元素的容器，`<head>`元素可以包含脚本、样式表

以下标签都可以添加到 head 部分：`<title>、<base>、<link>、<meta>、<script>` 以及 `<style>`

**HTML `<title>`元素**

`<title>`标签定义文档标题，是`<head>`元素必需的

- 定义浏览器工具栏的标题
- 页面被添加到收藏夹时显示的标题
- 显示在搜索引擎中的页面标题

~~~html
<head>
	<title>this is title</title>
</head>
~~~

**HTML `<base>`元素**

`<base>`标签为页面上的所有相对链接规定默认地址或默认的打开方式

这其中包括` <a>、<img>、<link>、<form>` 标签中的 URL

~~~html
<head>
	<base href="https://www.baidu.com/" />
    <base target="_blank" />
</head>
~~~

**HTML `<link>`元素**

`<link>` 标签定义文档与外部资源之间的关系。`<link>` 标签最常用于连接样式表

link 元素是空元素，它仅包含属性，此元素只能存在于 head 部分，不过它可出现任何次数

~~~html
<head>
	<link rel="stylesheet" type="text/css" href="mycss.css" />
</head>
~~~

**HTML `<style>`元素**

`<style>`标签用于为HTML 文档定义样式，type 属性是必需的，定义 style 元素的内容。唯一可能的值是 "text/css"。style 元素位于 head 部分中

~~~html
<head>
	<style type="text/css">
        h1 {color:red}
        p {text-align:center}
    </style>
</head>
~~~

**HTML `<meta>`元素**

 `<meta>`元素可提供有关页面的元信息，比如针对搜索引擎和更新频率的描述和关键词

 `<meta>`元素一定要在 `<head>`元素内部，元数据总是以键值对的形式

针对搜索引擎，定义页面的描述和关键词

~~~html
<head>
    <meta name="description" content="我是一个不错的网站" />
    <meta name="keywords" content="HTML, HTML5， CSS" />
</head>
~~~

**HTML `<script>`元素**

定义网页的脚本

~~~html
<script type="text/javascript">
	document.write("Hello World!")
</script>
~~~



## HTML 布局

**使用 div 元素的HTML布局**

div是没有语义的，相当于一个大盒子。HTML 经常用div + span 来对网页进行布局



**使用HTML 5 的网站布局**

HTML 提供了新的语义元素定义了网页的不同部分，使用对应的标签来布局，代码更具有可读性

HTML 5 语义元素

| 标签    | 描述             |
| ------- | ---------------- |
| header  | 定义了网页的头部 |
| nav     | 定义导航         |
| section | 定义了文档的节   |
| article |                  |
| aside   | 定义侧栏         |
| footer  | 定义底部         |
| details |                  |
| summary |                  |



**table 布局**

以前的网站会使用table来布局，现在基本上不会用了，table是用来展示数据的



## HTML 响应式设计

可以自己通过设计创建响应式设计

使用响应式框架，如Bootstrap



## HTML 5 语义

语义元素可以清楚的向浏览器和开发者描述其意义。

非语义元素：div、span

语义元素：form、table、img



**HTML 5 中的新的语义元素**

HTML 提供了一些新的带有语义的标签，使用它们可以增加代码的可读性，有利于搜索引擎的搜索

| HTML 5 语义标签 | 描述               |
| --------------- | ------------------ |
| header          | 规定文档或节的页眉 |
| nav             |                    |
| section         |                    |
| article         |                    |
| aside           |                    |
| footer          |                    |
| details         |                    |
| figcaption      |                    |
| figure          |                    |
| mian            |                    |
| mark            |                    |
| summary         |                    |
| time            |                    |



## HTML 代码约定

为了使HTML 代码的可读性和扩展性，需要对HTML的编写做出规定

**使用正确的文档类型**

~~~html
<!DOCTYPE html>
~~~

**使用小写元素名**

HTML 5的元素名不区分大小写，但是建议使用小写，很简洁

~~~html
<header></header>
~~~

**关闭所有的 HTML 元素**

HTML 5，有些元素不关闭也会正确显示，如`<p>`、`<br>`

斜杠（/）在 XHTML 和 XML 中是必需的，如果您期望 XML 软件来访问您的页面，保持这个习惯是个好主意

~~~html
<p></p>
<br />
<mate charset="UTF-8" >
~~~

**使用小写属性名**

HTML 5的属性名不区分大小写，但是建议使用小写属性名

~~~html
<div class=""></div>
~~~

**属性值加引号**

HTML5 允许不加引号的属性值，推荐属性值加引号，如果属性值包含值，则必须使用引号

~~~html
<input type="text"  />
~~~

**必需的属性**

对图像使用 alt 属性。当图像无法显示时该属性很重要

请始终定义图像尺寸。这样做会减少闪烁，因为浏览器会在图像加载之前为图像预留空间

~~~html
<img src="html5.gif" alt="HTML5" style="width:128px;height:128px">
~~~

**空格和等号**

但是精简空格更易阅读

~~~html
<link rel="stylesheet" href="styles.css">
~~~

**避免长代码行**

当使用 HTML 编辑器时，通过左右滚动来阅读 HTML 代码很不方便。

请尽量避免代码行超过 80 个字符。

**空行和缩进**

请勿毫无理由地增加空行。

为了提高可读性，请增加空行来分隔大型或逻辑代码块。

为了提高可读性，请增加两个空格的缩进。请勿使用 TAB。

请勿使用没有必要的空行和缩进。没有必要在短的和相关项目之间使用空行，也没有必要缩进每个元素

**不要省略 html 和 body 标签** 

在 HTML5 标准中，能够省略` <html>` 标签和 `<body>` 标签。不推荐省略 `<html> `和 `<body> `标签

**不要省略head标签**

在 HTML5 标准中，`<head>` 标签也能够被省略，不建议

**元数据**

增加需要的元素

**HTML 注释**

短注释应该在单行中书写，并在 `<!-- 之后增加一个空格，在 -->` 之前增加一个空格

**样式表**

使用简单的语法来链接样式表（type属性不是必须的）

~~~html
<link rel="stylesheet" href="styles.css">
~~~

**在 HTML 中加载 JavaScript**

使用简单的语法来加载外部脚本（type 属性不是必需的）

~~~html
<script src="myscript.js">
~~~

**使用小写文件名**

大多数 web 服务器（Apache、Unix）对文件名的大小写敏感

其他 web 服务器（微软，IIS）对大小写不敏感

为了避免这些问题，请始终使用小写文件名

**文件扩展名**

TML 文件名应该使用扩展名 .html（而不是 .htm）

CSS 文件应该使用扩展名 .css。

JavaScript 文件应该使用扩展名 .js



## HTML 特殊符号

在 HTML 中，某些字符是预留的，如果希望正确地显示预留字符，我们必须在 HTML 源代码中使用字符实体

| 显示结果 | 描述              | 实体名称            | 实体编号  |
| :------- | :---------------- | :------------------ | :-------- |
|          | 空格              | `&nbsp;`            | `&#160;`  |
| <        | 小于号            | `&lt;`              | `&#60;`   |
| >        | 大于号            | `&gt;`              | `&#62;`   |
| &        | 和号              | `&amp;`             | `&#38;`   |
| "        | 引号              | `&quot;`            | `&#34;`   |
| '        | 撇号              | `&apos; `(IE不支持) | `&#39;`   |
| ￠       | 分（cent）        | `&cent;`            | `&#162;`  |
| £        | 镑（pound）       | `&pound;`           | `&#163;`  |
| ¥        | 元（yen）         | `&yen;`             | `&#165;`  |
| €        | 欧元（euro）      | `&euro;`            | `&#8364;` |
| §        | 小节              | `&sect;`            | `&#167;`  |
| ©        | 版权（copyright） | `&copy;`            | `&#169;`  |
| ®        | 注册商标          | `&reg;`             | `&#174;`  |
| ™        | 商标              | `&trade;`           | `&#8482;` |
| ×        | 乘号              | `&times;`           | `&#215;`  |
| ÷        | 除号              | `&divide;`          | `&#247;`  |

> 使用实体名而不是数字的好处是，名称易于记忆。不过坏处是，浏览器也许并不支持所有实体名称（对实体数字的支持却很好）



## HTML 字符集

为了正确显示HTML 页面，Web 浏览器必须知道要使用那个字符集

**从 ASCII 到 UTF-8**
ASCII 是第一个字符编码标准。ASCII 定义了 128 种可以在互联网上使用的字符：数字（0-9）、英文字母（A-Z）和一些特殊字符，比如：! $ + - ( ) @ < >。

ISO-8859-1 是 HTML 4 的默认字符集。此字符集支持 256 个不同的字符代码。HTML 4 同时支持 UTF-8。

ANSI（Windows-1252）是原始的 Windows 字符集。 ANSI 与 ISO-8859-1 相同，不同之处在于 ANSI 具有 32 个额外的字符。

HTML5 规范鼓励 Web 开发人员使用 UTF-8 字符集，该字符集涵盖了世界上几乎所有的字符和符号！



**HTML 设置字符集**

指定使用UTF-8

~~~html
<meta charset="UTF-8" />
~~~



# HTML 表单

HTML 表单用于收集用户输入

一个完整的表单由表单域、表单元素（表单控件）和提示信息三部分组成

表单域用`<from>`定义，表单包含表单信息：不同类型的 input 元素、下拉菜单、文本域

~~~html
<!-- 整个form表单就使一个表单域 -->
<form action-"url地址" method=“提交方式” name="表单域名称">
    <div>
        <label for="username">姓名：</label>
        <input type="text" name="username" id="username" placeholder="请输入姓名">
    </div>
</form>
~~~



## 表单属性

form 表单的所有属性：

| 属性           | 属性值       | 作用                                             |
| -------------- | ------------ | ------------------------------------------------ |
| action         | url地址      | 用于接收并处理表单数据的服务器地址，默认当前页面 |
| method         | get/post     | 提交表单的方式，默认的 HTTP 方法是 GET           |
| name           | 名称         | 表单的名称，区分用以页面不同的表单域             |
| target         | _blank/..... | 表单提交后的打开方式                             |
| autocomplete   | on/off       | 提示用户之前输出的内容，默认打开                 |
| novalidate     |              | 规定提交时不应验证表单，默认验证                 |
| enctype        |              | 发送数据前的编码方式                             |
| accept-charset |              | 规定服务器用哪种字符集处理表单数据               |
| rel            |              | 规定链接资源和当前文档之间的关系                 |

~~~html
<form action="./index.php" method="post" name="form1" novalidate="novalidate">
	
</form>
~~~



**enctype**

enctype 属性规定在发送到服务器之前应该如何对表单数据进行编码。

| 属性值                            | 描述                                                       |
| --------------------------------- | ---------------------------------------------------------- |
| application/x-www-form-urlencoded | 在发送前编码所有字符（默认）                               |
| multipart/form-data               | 不对字符编码，在使用包含文件上传控件的表单时，必须使用该值 |
| text/plain                        | 空格转换为 "+" 加号，但不对特殊字符编码                    |





## 表单元素

### input 元素

1、input 元素使最重要的表单元素。有很多类型

input输入表单元素，必填type属性

~~~html
<form>
    姓名：<input type="text" />
    密码：<input type="password" />
    性别：
</form>
~~~

type属性值：

| 属性值   | 说明                                          |
| -------- | --------------------------------------------- |
| text     | 定义单行文本输入字段                          |
| password | 定义密码字段，字符会被掩盖                    |
| radio    | 定义单选按钮，用户只能选一个，name的值要相同  |
| checkout | 定义复选框，多选，name值相同，name = “name[]” |
| button   | 定义按钮                                      |
| file     | 定义输入字段和“浏览”按钮，文件上传            |
| hidden   | 定义隐藏字段                                  |
| image    | 定义图像形式的提交按钮                        |
| reset    | 定义重置按钮                                  |
| submit   | 定义提交按钮，value不填默认是”提交“           |

input的其他属性

| 属性      | 属性值  | 说明                  |
| --------- | ------- | --------------------- |
| name      | 自定义  | 和数据库字段名相同    |
| value     | 自定义  | 规定 input 元素的值。 |
| checked   | checked | 被选中                |
| maxlength | 正整数  | input框字符的最大长度 |

~~~html
<form action="./" method="post">
    <div>
        <label for="username">姓名：</label>
        <input type="text" name="username" id="username" placeholder="请输入姓名">
    </div>
    <div>
        <label for="password">密码：</label>
        <input type="password" name="password" id="password" placeholder="请输入密码">
    </div>
    <div>
        <span for="gender">性别：</span>
        <label for="man">男</label> 
        <input type="radio" name="gender" id="man" value="1" checked="checked">
        <label for="woman">女</label> 
        <input type="radio" name="gender" id="woman" value="0">
    </div>
    <div>
        <span>爱好：</span>
        <label for="basketball">篮球</label>    
        <input type="checkbox" name="hobby[]" id="basketball" value="1">
        <label for="football">足球</label>
        <input type="checkbox" name="hobby[]" id="football" value="2">
        <label for="baseball">棒球</label>
        <input type="checkbox" name="hobby[]" id="baseball" value="3">
    </div>
    <div>
        <input type="button" value="获取短信验证码">
    </div>
    <div>
        <label for="">上传文件</label>
        <input type="file" name="" id="">
    </div>
    <div>
        <input type="submit" value="注册">
        <input type="reset" value="重置">
    </div>
</form>
~~~

label标签会将信息和表单元素绑定，点击信息会将光标移到对应的表单元素

### HTML 5 增加的 input 类型

web 浏览器不支持的输入类型，会被视为输入类型 text

| HTML5 input type 属性值 | 描述 |
| ----------------------- | ---- |
| color                   |      |
| date                    |      |
| datetime                |      |
| datetime-local          |      |
| email                   |      |
| mouth                   |      |
| number                  |      |
| range                   |      |
| search                  |      |
| tel                     |      |
| time                    |      |
| url                     |      |
| week                    |      |

**input number**

限制只能输入数字，还能限制范围

~~~html
<input type="number" name="quantity" min="1" max="5">
~~~

**input date**

您填写输入字段时会弹出日期选择器

~~~html
<input type="number" name="quantity" min="1" max="5">
~~~

**input color**

颜色选择器会出现输入字段中

~~~html
<input type="color" name="favcolor">
~~~

**input range**

输入字段能够显示为滑块控件

~~~html
<input type="range" name="points" min="0" max="10">
~~~

**input month**

允许用户选择月份和年份，日期选择器会出现输入字段中

~~~html
<input type="month" name="bdaymonth">
~~~

**input week**

允许用户选择周和年，日期选择器会出现输入字段中

~~~html
<input type="week" name="week_year">
~~~

**input time**

允许用户选择时间（无时区），日期选择器会出现输入字段中

~~~html
<input type="time" name="week_year">
~~~

**input datetime**

允许用户选择日期和时间（有时区），日期选择器会出现输入字段中

~~~html
<input type="datetime" name="bdaytime">
~~~

**input datetime-local**

允许用户选择日期和时间（无时区），日期选择器会出现输入字段中

~~~html
<input type="month" name="bdaymonth">
~~~

**input email**

输入电子邮件

~~~html
<input type="email" name="email">
~~~

**input search**

用于搜索字段

~~~html
<input type="search" name="search">
~~~

**input tel**

于应该包含电话号码的输入字段，目前只有 Safari 8 支持 tel 类型

~~~html
<input type="tel" name="tel">
~~~

**input url**

用于应该包含 URL 地址的输入字段

~~~html
<input type="url" name="homepage">
~~~



### 下拉表单 select

select 定义下拉菜单，option 定义选项

列表通常会把首个选项显示为被选选项，如果你想默认选中某个选项可以使用selected

`selected="selected"`默认选中

~~~html
<label for="height">请选择身高：</label>
<select name="height" id="height">
    <option>请选择</option>
    <option value="1">170</option>
    <option value="2" selected="selected">180</option>
    <option value="3" >190</option>
</select>
~~~

### 文本域 textarea

textarea 元素允许输入多行文本

~~~html
<textarea name="" id="" cols="30" rows="10"></textarea>
~~~

### 按钮 button

~~~html
<button type="button">发送验证码</button>
~~~

### HTML 5 表单元素

| 元素     | 描述                                                         |
| -------- | ------------------------------------------------------------ |
| datalist | 用户会在他们输入数据时看到预定义选项的下拉列表               |
| keygen   | 表单的密钥生成器，不再推荐使用该特性。虽然一些浏览器仍然支持它 |
| output   | 计算结果输出显示                                             |

~~~html
<form action="action_page.php">
	<input list="browsers">
    <datalist id="browsers">
       <option value="Internet Explorer">
       <option value="Firefox">
       <option value="Chrome">
       <option value="Opera">
       <option value="Safari">
    </datalist> 
</form>
~~~

output

~~~html
<form oninput="x.value=parseInt(a.value)+parseInt(b.value)">0
    <input type="range" id="a" value="50">100
    +<input type="number" id="b" value="50">
    =<output name="x" for="a b"></output>
</form>
~~~



## HTML 输入属性

这些属性一般都是加在表单元素上，对表单元素进行限制

| 属性      | 描述                                   |
| --------- | -------------------------------------- |
| value     | 规定输入字段的初始值                   |
| readonly  | 规定输入字段为只读（不能修改）         |
| disabled  | 输入字段是禁用，禁用字段不能点击和提交 |
| size      | 规定输入字段的尺寸                     |
| maxlength | 规定输入字段允许的最大长度             |

### HTML 5 新的表单属性

 1、HTML 5 新的 form 属性

| 属性         | 描述                             |
| ------------ | -------------------------------- |
| autocomplete | 提示用户之前输出的内容，默认打开 |
| novalidate   | 不验证表单，默认验证             |

**form/input autocomplete 属性** 

form 和 input 都可以使用autocomplete属性，提示用户之前输出的内容，默认打开

~~~html
<form action="demo-form.php" autocomplete="on">
  First name:<input type="text" name="fname"><br>
  Last name: <input type="text" name="lname"><br>
  E-mail: <input type="email" name="email" autocomplete="off"><br>
  <input type="submit">
</form>
~~~

**form novalidate属性**

novalidate 不验证表单，默认验证

~~~html
<form action="action_page.php" novalidate=“novalidate”>
   E-mail: <input type="email" name="user_email" />
   <input type="submit" />
</form> 
~~~

2、HTML 5 新的 input 属性

| 属性         | 描述                                                         |
| ------------ | ------------------------------------------------------------ |
| autofocus    | 自动获得焦点                                                 |
| form         | 规定 input元素所属的一个或多个表单                           |
| formvalidate | 规定不验证改元素，覆盖form的validate                         |
| formaction   | 提交表单时使用该输入控件的文件的 URL，覆盖form表单的action属性 |
| formenctype  | 提交表单时使用该属性设置的enctype值，覆盖form表单的enctype属性 |
| formmethod   | 定义提交的HTTP方法，覆盖form表单的method                     |
| formtarget   | 定义提交表达的打开方式，覆盖form的target                     |
| height/width | 定义input的高度和宽度                                        |
| list         | 和 datalist一起使用，定义了input的下拉预选项                 |
| min 和 max   | min 和 max 属性规定 <input> 元素的最小值和最大值             |
| multiple     | 上传控件设置可以进行批量上传                                 |
| pattern      | 匹配正则表达式                                               |
| placeholder  | 定义一段提示文字                                             |
| required     | 必须输入                                                     |
| step         | 定 input元素的合法数字间隔.如果 step="3"，则合法数字应该是 -3、0、3、6 |



autofocus 

~~~html
<input type="text" name="fname" autofocus="autofocus">
~~~

form

~~~html
<form action="action_page.php" id="form1">
   First name: <input type="text" name="fname"><br>
   <input type="submit" value="Submit">
</form>

Last name: <input type="text" name="lname" form="form1">
~~~

formvalidate、formaction、formenctype、formmethod、formtarget

~~~html
<input type="submit" formaction="demo_admin.asp" value="Submit as admin">
<input type="submit" formenctype="multipart/form-data" value="Submit">
<input type="submit" formmethod="get" value="Submit">
<input type="submit" formnovalidate value="Submit without validation">
<input type="submit" formtarget="_blank" value="Submit to a new window">
~~~

height/width  

~~~html
<input type="image" src="img_submit.gif" alt="Submit" width="48" height="48">
~~~

list

~~~html
<input list="browsers">

<datalist id="browsers">
   <option value="Internet Explorer">
   <option value="Firefox">
   <option value="Chrome">
   <option value="Opera">
   <option value="Safari">
</datalist> 
~~~

min 和 max

```html
<input type="number" name="quantity" min="1" max="5">
```

multiple

```html
Select images: <input type="file" name="img" multiple>
```

pattern

```html
<input type="text" name="country_code" pattern="[A-Za-z]{3}" title="Three letter country code">
```

placeholder

```html
<input type="text" name="fname" placeholder="First name">
```

required

```html
Username: <input type="text" name="usrname" required>
```

step

```html
<input type="number" name="points" step="3">
```



# HTML5

## HTML5 简介

HTML5 是最新的 HTML 标准。

HTML5 是专门为承载丰富的 web 内容而设计的，并且无需额外插件。

HTML5 拥有新的语义、图形以及多媒体元素。

HTML5 提供的新元素和新的 API 简化了 web 应用程序的搭建。

HTML5 是跨平台的，被设计为在不同类型的硬件（PC、平板、手机、电视机等等）之上运行

### HTML 5 的声明

HTML5 的新的文档类型（DOCTYPE）声明非常简单

HTML5 中默认的字符编码是 UTF-8

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>Title of the document</title>
    </head>

    <body>
        Content of the document......
    </body>

</html>
```

### HTML 新的属性语法

HTML5 标准允许4种不同的属性语法。推荐使用双引号

| 类型       | 示例                     |
| ---------- | ------------------------ |
| 空的属性值 | disabled                 |
| 不要引号   | value=Jack               |
| 双引号     | value=“Jack”（推荐使用） |
| 单引号     | value=‘Jack’             |

### HTML5 - 新特性

HTML5 的一些最有趣的新特性：

- 新的语义元素，如header、nav、section、article、footer等等
- 新的表单控件，如数字、日期、日历、滑块
- 强大的图像支持，canvas、svg
- 强大的多媒体支持，video、audio
- 强大的新API，Web存储代替cookie



### HTML5 - 被删元素

以下 HTML 4.01 元素已从 HTML5 中删除：

- `<acronym>`
- `<applet>`
- `<basefont>`
- `<big>`
- `<center>`
- `<dir>`
- `<font>`
- `<frame>`
- `<frameset>`
- `<noframes>`
- `<strike>`
- `<tt>`



## HTML5 兼容

有一些老版本的浏览器不支持HTML5，所有的新版本浏览器都支持HTML5，可以做一些改变尽量使HTML5兼容一些旧版本的浏览器

**把HTML5 元素定义为块级元素**

所有浏览器，不论新旧，都会自动把未识别元素当做行内元素来处理

HTML5 定义了八个新的语义 HTML 元素。所有都是块级元素，所以先把它们定义为块级元素

~~~css
header, section, footer, aside, nav, main, article, figure {
    display: block; 
}
~~~

IE浏览器已经下架，不用做兼容

**HTML5 的骨架代码**

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
<title>HTML5 Skeleton</title>
<meta charset="utf-8">

<!--[if lt IE 9]>
<script src="http://html5shiv.googlecode.com/svn/trunk/html5.js">
</script>
<![endif]-->

<style>
body {font-family: Verdana, sans-serif; font-size:0.8em;}
header,nav, section,article,footer
{border:1px solid grey; margin:5px; padding:8px;}
nav ul {margin:0; padding:0;}
nav ul li {display:inline; margin:5px;}
</style>
</head>

<body>

<header>
  <h1>HTML5 SKeleton</h1>
</header>

<nav>
<ul>
  <li><a href="html5_semantic_elements.asp">HTML5 Semantic</a></li>
  <li><a href="html5_geolocation.asp">HTML5 Geolocation</a></li>
  <li><a href="html5_canvas.asp">HTML5 Graphics</a></li>
</ul>
</nav>

<section>

<h1>Famous Cities</h1>

<article>
<h2>London</h2>
<p>London is the capital city of England. It is the most populous city in the United Kingdom,
with a metropolitan area of over 13 million inhabitants.</p>
</article>

<article>
<h2>Paris</h2>
<p>Paris is the capital and most populous city of France.</p>
</article>

<article>
<h2>Tokyo</h2>
<p>Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
and the most populous metropolitan area in the world.</p>
</article>

</section>

<footer>
<p>© 2014 W3Schools. All rights reserved.</p>
</footer>

</body>
</html>
~~~

## HTML5 元素

HTML5 的新元素，HTML5 提供了新的语义元素来对文档进行布局

| 标签           | 描述                                                 |
| :------------- | :--------------------------------------------------- |
| `<article>`    | 定义文档内的文章。                                   |
| `<aside>`      | 定义页面内容之外的内容。                             |
| `<bdi>`        | 定义与其他文本不同的文本方向。                       |
| `<details>`    | 定义用户可查看或隐藏的额外细节。                     |
| `<dialog>`     | 定义对话框或窗口。                                   |
| `<figcaption>` | 定义 <figure> 元素的标题。                           |
| `<figure>`     | 定义自包含内容，比如图示、图表、照片、代码清单等等。 |
| `<footer>`     | 定义文档或节的页脚。                                 |
| `<header>`     | 定义文档或节的页眉。                                 |
| `<main>`       | 定义文档的主内容。                                   |
| `<mark>`       | 定义重要或强调的内容。                               |
| `<menuitem>`   | 定义用户能够从弹出菜单调用的命令/菜单项目。          |
| `<meter>`      | 定义已知范围（尺度）内的标量测量。                   |
| `<nav>`        | 定义文档内的导航链接。                               |
| `<progress>`   | 定义任务进度。                                       |
| `<rp>`         | 定义在不支持 ruby 注释的浏览器中显示什么。           |
| `<rt>`         | 定义关于字符的解释/发音（用于东亚字体）。            |
| `<ruby>`       | 定义 ruby 注释（用于东亚字体）。                     |
| `<section>`    | 定义文档中的节。                                     |
| `<summary>`    | 定义 <details> 元素的可见标题。                      |
| `<time>`       | 定义日期/时间。                                      |
| `<wbr>`        | 定义可能的折行（line-break）。                       |

新的表单元素

| 标签         | 描述                                   |
| :----------- | :------------------------------------- |
| `<datalist>` | 定义输入控件的预定义选项。             |
| `<keygen>`   | 定义键对生成器字段（用于表单）；已弃用 |
| `<output>`   | 定义计算结果。                         |

新的表单属性

| 新的输入类型（input） | 新的输入属性     |
| --------------------- | ---------------- |
| color                 | autocomplete     |
| date                  | autofocus        |
| datetime              | form             |
| datetime-local        | formaction       |
| email                 | formenctype      |
| month                 | formmethod       |
| number                | formnovalidate   |
| range                 | formtarget       |
| search                | height           |
| tel                   | height 和 width  |
| time                  | list             |
| url                   | min 和 max       |
| week                  | multiple         |
|                       | pattern (regexp) |
|                       | placeholder      |
|                       | required         |
|                       | step             |

HTML 新的属性语法

HTML5 标准允许4种不同的属性语法。推荐使用双引号

| 类型       | 示例                     |
| ---------- | ------------------------ |
| 空的属性值 | disabled                 |
| 不要引号   | value=Jack               |
| 双引号     | value=“Jack”（推荐使用） |
| 单引号     | value=‘Jack’             |

HTML5 图像

| 标签       | 描述                             |
| :--------- | :------------------------------- |
| `<canvas>` | 定义使用 JavaScript 的图像绘制。 |
| `<svg>`    | 定义使用 SVG 的图像绘制。        |

新的媒介元素

| 标签       | 描述                                 |
| :--------- | :----------------------------------- |
| `<audio>`  | 定义声音或音乐内容。                 |
| `<embed>`  | 定义外部应用程序的容器（比如插件）。 |
| `<source>` | 定义` <video> `和` <audio>` 的来源。 |
| `<track>`  | 定义 `<video> `和 `<audio>` 的轨道。 |
| `<video>`  | 定义视频或影片内容。                 |



## HTML5 迁移

### 从 HTML4 迁移至 HTML5

如何把一张已有的 HTML4 页面转换为 HTML5 页面，在不破坏如何原始内容和结构的情况下



**更改 HTML5 声明 和编码**

HTML4

~~~html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">

<meta http-equiv="Content-Type" content="text/html;charset=utf-8">

~~~

HTML5

~~~html
<!DOCTYPE html>

<meta charset="UTF-8">
~~~



为 HTML5 语义元素添加 CSS

用HTML5的语义元素布局





# HTML5  图形

## HTML5 Canvas

### 一、Canvas 简介

canvas 是HTML5 提供的一种新标签

- canvas 是一个矩形区域的画布，可以用JavaScript 在上面绘画。控制其每一个像素
- canvas 标签本身不具备绘图功能，使用JavaScript 在网页上绘制图像
- canvas 拥有多种绘制路径、矩形、圆形、字符以及添加图像的方法



canvas 主要应用

1. 游戏：canvas 在基于 Web 的图像显示方面比 Flash 更加立体、更加精巧，canvas 游戏在流畅度和跨平台方面更好
2. ==可视化数据==：数据图表，比如：百度的 echart
3. ==banner 广告==：canvas 可以代替 Flash 实现动态的广告效果
4. 模拟器、远程计算机控制、图像编辑器（网页实现Photoshop的全部功能）
5. 可嵌入网站的内容
6. ==完整的 canvas 移动化应用==



### 二、使用 Canvas 

#### 1、canvas 标签和属性

不要用 CSS 控制它的宽高，会出现图片拉伸，重新设置 canvas 的宽高属性会让画布擦除所有的内容，可以给canvas 画布设置背景色

canvas 的兼容性处理：如果浏览器不支持 canvas 会把 canvas 标签看成一个普通的标签

~~~html
<canvas id="myCanvas" width="500" height="500">你的浏览器版本过低,请升级浏览器或使用chrome</canvas>
~~~

Canvas 坐标

- canvas 是一个二维网格（x,y）。

- canvas 的左上角坐标为 (0,0)

#### 2、canvas 创建 context 对象

~~~js
// 获取canvas标签
var canvas = document.getElementById("myCanvas");
// canvas设置宽高和样式
canvas.width = 500;
canvas.height = 500;
canvas.style.border = "1px solid #000000";

// 获取canvas的context对象
var cxt = canvas.getContext("2d");
~~~

#### Canvas 路径

在Canvas 上画线

- moveTo(x,y)：定义线条开始坐标
- lineTo(x,y)：定义线条的结束坐标
- strokeStyle = “red”：设置线的样式
- stroke()：把定义的线条描绘出来
- fillStyle = “green”：填充颜色
- fill()：进行填充

~~~js
// 绘制
cxt.moveTo(100,100); // 把画笔移动到(100,100)坐标
cxt.lineTo(200,100); // 画一条直线到坐标(200,100)
cxt.lineTo(100,200); // 从当前位置画一条直线到坐标(100,200)
cxt.closePath(); //闭合路径，或者用lineTo(100,100)回到起点，形成一个三角形

// 设置线的样式
cxt.strokeStyle = "red";
// 设置线宽
cxt.lineWidth = 4;
// 填充颜色
cxt.fillStyle = "#fff000";

cxt.fill(); //进行填充
cxt.stroke(); // 把线描出来 
~~~

在一张图绘制不同的路径，可以开始一条新路径，防止前面的被覆盖掉，为每一个图案都开启一个新路径

- beginPath()：起始一条路径

~~~js
// 绘制
cxt.beginPath();
cxt.moveTo(100,100); // 把画笔移动到(100,100)坐标
cxt.lineTo(200,100); // 画一条直线到坐标(200,100)
cxt.lineWidth = 10;
cxt.strokeStyle = "red";
cxt.stroke();

// 新路径
cxt.beginPath();
cxt.moveTo(100,200);
cxt.lineTo(200,200);
// cxt.lineWidth = 10;
// cxt.strokeStyle = "yellow";
cxt.stroke();
~~~

#### 矩形 rect

快速的绘画矩形

- rect(x, y, w, h)：快速创建矩形，x，y是坐标，w，h是宽高
- strokeRect(x, y, w, h)：绘制矩形，x，y是坐标，w，h是宽高
- fillRect(x, y, w, h)：填充矩形，yx，y是坐标，w，h是宽高
- clearRect(x, y, w, h)：在给定的矩形内清除指定的像素

~~~js
// 快速绘制矩形
cxt.beginPath();
cxt.rect(100,100,50,100);
cxt.stroke();

// 绘制矩形
cxt.strokeRect(200,200,100,100);
// 填充矩形
cxt.fillRect(300,300,50,50);
// 清除矩形
cxt.clearRect(300,300,50,50);
cxt.stroke();
~~~

#### 圆弧 arc

arc 方法创建圆弧（创建圆或部分圆）

- arc(x ,y, r, sAngle, eAngle, [counterclockwise])：
  - x，y（圆心坐标）；r（圆的半径）；
  - sAngle（起始角，单位是弧度，弧的圆形的三点钟位置是 0 度）；
  - eAngle（结束角，单位是弧度）；
  - counterclockwise（可选，false = 顺时针，true = 逆时针，默认是顺时针）



![image-20220914211640023](../../App/Typora/assets/HTML基础_image/image-20220914211640023.png)

角度和弧度的换算：弧度（rad） =  角度/180 * Math.PI

360°的圆：

~~~js
cxt.arc(100,100,50,0,2*Math.PI);
cxt.stroke();
~~~

画扇形图

计算文本位置的x，y轴坐标

~~~
x = x0 + Math.cos(角度/180*Math.PI) * (r + 20);
x = y0 + Math.sin(角度/180*Math.PI) * (r + 20);
~~~

~~~js
var data = [{
    "value": .2,
    "color": "red",
    "title": "篮球",
},{
    "value": .3,
    "color": "blue",
    "title": "足球",
},{
    "value": .4,
    "color": "green",
    "title": "游戏",
},{
    "value": .1,
    "color": "#ccc",
    "title": "LOL",
}];


(function(){
    var tempAngle = -90; // 从-90°开始绘制
    var xr = 300; // x轴圆心
    var yr = 300; // x轴圆心
    var r = 100; // 圆的半径
    for (let i = 0; i < data.length; i++) {
        cxt.beginPath();
        cxt.moveTo(xr, yr);
        var angle = data[i].value * 360; // 扇形度数
        var sAngle = tempAngle / 180 * Math.PI;
        var eAngle = (tempAngle + angle) / 180 * Math.PI;

        cxt.fillStyle = data[i].color;

        // 绘制 文字
        var title = data[i].title;
        var txt = data[i].value * 100 + "%"; // 百分比文本
        var x, y;
        var txtAngle = tempAngle + 1/2 * angle;

        x = xr + Math.cos(txtAngle / 180 * Math.PI) * (r + 20);
        y = yr + Math.sin(txtAngle / 180 * Math.PI) * (r + 20);

        // 文本排列
        if (90 < txtAngle && txtAngle < 270) {
            console.log(txtAngle);
            cxt.textAlign = "right";
        };

        cxt.strokeText(txt, x, y);
        cxt.arc(xr, yr, r, sAngle, eAngle);
        cxt.fill();
        tempAngle += angle;
    }      
})
~~~





#### 绘制文本

属性

- font = “30px, 微软雅黑”：font设置或返回画布上文本内容的当前字体属性，和CSS的font属性相同
- textAlign = “left/right/center/start/end”：设置或返回文本内容的当前对齐方式
- textBaseline = “top/middle/button”：设置或返回在绘制文本时的当前文本基线

方法

- fillText(text, x ,y ,[maxWidth])：画布上绘制填色的文本。文本的默认颜色是黑色
- strokeText(text, x, y, [maxWidth])：在画布上绘制文本（无填充色）
- measureText(text)：返回一个对象，该对象包含以像素计的指定字体宽度

~~~js
cxt.font = "30px Arial";
cxt.textAlign = "center";
cxt.textBaseline = "top";
cxt.fillStyle = "red";
cxt.strokeText("text",300,300);
console.log(cxt.measureText("txt"));
cxt.fillText("Hello World", 400, 300);
~~~



#### 绘制图片

1、用drawImage方法来绘制图片，（能绘制图片就用图片）

- drawImage(img, x, y)：img是图片的dom对象，x，y是坐标，

~~~js
// 第一步，创建图片的dom对象
// var img = document.getElementById("img"); //这样拿到的也是img对象
var img = new Image();
img.src = "images.jpg"; // 只要设置了src属性，当前img对象立即去加载图片

// 图片加载完成，立即执行下面函数
img.onload = function(){
    // 绘制图片
    cxt.drawImage(img, 100, 100);

    // for (let i = 0; i < 5; i++) {
    //     cxt.drawImage(img, 200 + i * 50, 200 + i * 50);
    // }
};
~~~

2、绘制指定宽高的图片

- drawImage(img, x, y, [width], [height])
  - width：指定图片的宽度
  - height：指定图片的高度

同时设置图片的宽和高，会使图片失真拉伸，所以只需要设置其中一个，另一个通过比例计算

原来的宽度（ow）/ 原来的高度（oh） =  绘制图片的宽度 / 绘制图片的高度

~~~js
var ow = img.width;
var oh = img.height;
// 绘制指定宽高的图片
// 指定宽度40，高度就是 40 * oh/ow
cxt.drawImage(img, 200, 200, 40, 40 * oh/ow);
~~~

3、裁剪图片

- drawImage(img, sx, sy, swidth, shtight, x, y, width, height)
  - img：图片的dom对象
  - sx，sy：开始剪切的 x ，y坐标位置
  -  swidth, shtight：被剪切图像的宽度和高度
  - x，y：画布上放置图像的 x ，y坐标位置
  - width，height：要使用的图像的宽度，可选

~~~js
var c=document.getElementById("myCanvas");
var ctx=c.getContext("2d");
var img=document.getElementById("scream");
ctx.drawImage(img,90,130,50,60,10,10,50,60);
~~~

4、绘制序列帧动画

~~~html
        // 绘制序列帧动画
        var img = new Image();
        img.src = "images/role8.png";
        var dirIndex = 0; // 方向
        img.onload = function(){
            
            var frameIndex = 0 // 第几张图片

            setInterval(function(){
                // 清楚之前的图片
                cxt.clearRect(0, 0, canvas.width, canvas.height);
                // canvas重新设置宽高，canvas画布内容会清空
                // canvas.width = canvas.width;
                cxt.drawImage(
                    img,
                    frameIndex * img.width / 8, // 原始图片的 x 坐标
                    dirIndex * img.height / 8 ,     // 原始图片的 y 坐标
                    img.width / 8,              // 截取的宽度
                    img.height / 8,             // 截取的高度
                    200,                        // 图片在画布上的 x 坐标
                    200,                        // 图片在画布上的 y 坐标
                    img.width / 8,
                    img.height / 8
                )

                frameIndex++; // 截取下一张图片
                frameIndex %= 8; // 取余，8张图片循环一次
                
            }, 1000 / 24); // 24帧，
        };
~~~



### Js 对象

就是Javascript对象，Javascript 定义了5种原始变量类型，原始值是一成不变的（它们是硬编码的，因此不能改变）

- string
- number
- boolean
- null
- undefined

JavaScript 对象是被称为属性和方法的命名值的容器，对象也是变量。但是对象能够包含很多值

定义对象有3种方法

1、定义和创建单个对象，使用 `{}`

~~~js
var person = {firstName:"Bill",lastName:"Kobe",age:"18",eyecolor:"blue"}
~~~

空格和折行不重要。对象定义可横跨多行：

~~~js
var person = {
    firstName:"Bill",
    lastName:"Gates",
    age:62,
    eyeColor:"blue"
};
~~~

2、使用 JavaScript 关键词 new

~~~js
var person = new Object();
person.firstName = "Bill";
person.lastName = "Gates";
person.age = 50;
person.eyeColor = "blue";
~~~

3、定义对象构造器，然后创建构造类型的对象



Javascript对象是易变的，它们通过引用来寻址，而非值。

#### Js 对象属性

属性指的是与 JavaScript 对象相关的值，JavaScript 对象是无序属性的集合，属性通常可以被修改、添加和删除，但是某些属性是只读的

访问 Javascript 属性的3种语法

~~~js
var person = {firstName:"Bill",lastName:"Kobe",age:"18",eyecolor:"blue"};
person.firstName;
person["firstName"];
person[firstname];
~~~

JavaScript for...in 循环

用 `for...in`语句遍历对象的属性

~~~js
var person = {firstName:"Bill",lastName:"Kobe",age:"18",eyecolor:"blue"}
for (let x in person) {
    console.log(x);
}
~~~

添加属性

~~~js
var person = {firstName:"Bill",lastName:"Kobe",age:"18",eyecolor:"blue"}
persion.headcolor = "green";
~~~

删除属性

delete 关键词从对象中删除属性：

~~~js
delete person.age
~~~

属性值

所有属性都有名称。此外它们还有值。

原始属性

JavaScript 对象继承了它们的原型的属性。

delete 关键词不会删除被继承的属性，但是如果您删除了某个原型属性，则将影响到所有从原型继承的对象。

#### Js 对象方法

JavaScript 方法是能够在对象上执行的动作。

~~~js
var person = {
  firstName: "Bill",
  lastName : "Gates",
  id       : 648,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
~~~

this 关键词

在函数中使用时，是“拥有”该函数的对象。

请注意 this 并非变量。它是关键词。您无法改变 this 的值。

访问对象方法

~~~js
person.fullName()
~~~

使用 JS 的内建方法

~~~js
var message = "Hello world!";
var x = message.toUpperCase();
~~~

添加新的方法



#### 显示对象

1、显示对象属性

~~~js
person.name + "," + person.age
~~~

2、在循环种显示对象

可以在循环中收集对象的属性：

~~~js
const person = {
  name: "Bill",
  age: 19,
  city: "Seattle"
};
for(let x in person) {
    txt += person[x];
}
console.log(txt);
~~~

您必须在循环中使用 person[x]，person.x 将不起作用（因为 x 是一个变量）

3、使用Object.value()

通过使用 Object.values()，任何 JavaScript 对象都可以被转换为数组：

~~~js
const person = {
  name: "Bill",
  age: 19,
  city: "Seattle"
};

const myArray = Object.values(person);
// myArray["Bill",19,"Seattle"]
~~~

4、使用 JSON.stringify()

任何 JavaScript 对象都可以使用 JavaScript 函数 JSON.stringify() 进行字符串化（转换为字符串）：

~~~js
const person = {
  name: "Bill",
  age: 19,
  city: "Seattle"
};

let myString = JSON.stringify(person);
// myString = {"name":"Bill","age":19,"city":"Seattle"};
~~~

JSON.stringify 将日期转换为字符串

JSON.stringify 不会对函数进行字符串化

#### JS 对象构造器

通过构造器可以创建一种类型的对象

~~~js
function Person(first, last, age, eye) {
    this.firstName = first;
    this.lastName = last;
    this.age = age;
    this.eyeColor = eye;
}
~~~

通过 new 关键词调用构造器函数可以创建相同类型的对象：

~~~js
var Bill = new Person("Bill", "Gates", 62, "blue");
var Steve = new Person("Steve", "Jobs", 56, "green");
~~~

new的原理：创建一个空对象，把this指向空对象，空对象的内部原型指向 构造器 的原型对象

为对象添加属性、方法

~~~js
Bill.nationality = "English";
Bill.name = function () {
    return this.firstName + " " + this.lastName;
};
~~~

只是Bill对象添加了属性和方法



为构造器添加属性和方法

与向已有对象添加新属性不同，您无法为对象构造器添加新属性

如需向构造器添加一个新属性，您必须添加到构造器函数

> new 内部原理
>
> new 构造函数时，如果有返回值（return）就直接把返回值复制，如果没有返回值，返回构造函数的this对象，this 对象指向创建的对象，创建的对象和构造函数都是指向原型对象

#### 原型继承

所有 JavaScript 对象都从原型继承属性和方法。

日期对象继承自 Date.prototype。数组对象继承自 Array.prototype。Person 对象继承自 Person.prototype。

Object.prototype 位于原型继承链的顶端：

日期对象、数组对象和 Person 对象都继承自 Object.prototype。



JavaScript prototype 属性允许您为对象构造器添加新属性：

~~~js
Person.prototype.nationality = "English";
Person.prototype.name = function() {
    return this.firstName + " " + this.lastName;
};
~~~



#### 类的书写方法

1、不传参，不灵活

~~~js
// 在构造函数中，添加属性
function Person() {
    this.name = "Jack";
}

// 尽量在原型对象中添加方法（节省内存），公共属性和常量的值可以放到原型对象
Person.prototype.show = function() {
    console.log(this.name);
}

var person = new Person();
person.show();
~~~

2、参数太多是麻烦

~~~js
// 参数太多时不好
// 在构造函数中，添加属性（传参）
function Person(name, age) {
    this.name = name;
    this.age = age
}

// 尽量在原型对象中添加方法（节省内存），公共属性和常量的值可以放到原型对象
Person.prototype.show = function() {
    console.log(this.name);
}

var person = new Person("Jack", 18);
person.show();
~~~

3、参数是对象，不用按顺序传参

~~~js
// 参数换成对象
// 在构造函数中，添加属性
function Person( option ) {
    this.name = option.name;
    this.age = option.age;
}

// 尽量在原型对象中添加方法（节省内存），公共属性和常量的值可以放到原型对象
Person.prototype.show = function() {
    console.log(this.name);
}

var person = new Person({name:"Jack", age:18});
person.show();
~~~

4、用初始化函数传参（推荐使用）

- 所有的属性初始化放到`_init`

~~~js
// 用构造函数初始化
function Person( option ) {
    this._init( option );
}

Person.prototype = {
    _init: function( option ) {
        this.name = option.name;
        this.age = option.age;
    },
    show: function() {
        console.log(this.name);
    }
}

var person = new Person({name:"Jack", "age":18});
person.show();
~~~



#### 函数的4种调用模式

第一种：函数执行函数

~~~js
// 第一种：函数执行模式
function add(a, b) {
    console.log(this);
    return a + b;
}

add(); // this === window / window.add()
~~~

第二种：对象方法调用模式

~~~js
// 第二种：对象方法调用模式
function Person() {
    this.name = "Jack";
    this.show = function() {
        console.log( this );
    }
}

var person = new Person();
person.show(); // 对象调用自己的方法 this === person
~~~

第三种：构造器的调用模式 

~~~js
// 第三种：构造器的调用模式 
function Person() {
    this.show = function() {
        console.log( this );
    }
}

var person = new Person(); // new的时候，this === person
~~~

第四章：call 和 apply调用模式



### canvas 进阶

#### 设置阴影（性能差）

性能差，很少用，类似CSS3的阴影。一般用个图片代替

- shadowColor：设置或返回用于阴影的颜色
- shadowBlur：设置或返回用于阴影的模糊级别（越大越模糊）
- shadowOffsetX：设置或返回阴影与形状的水平距离
- shadowOffsetY：设置或返回阴影与形状的垂直距离

将 shadowColor 属性与 shadowBlur 属性一起使用，来创建阴影

请通过使用 shadowOffsetX 和 shadowOffsetY 属性来调节阴影效果

~~~js
cxt.fillStyle = "red";
cxt.shadowBlur = 5;
cxt.shadowColor = "black";
cxt.shadowOffsetX = 10; 
cxt.shadowOffsetY = 10; 
cxt.fillRect(100, 100, 50, 50);
~~~

#### 设置渐变（性能差）

createLinearGradient() 方法创建线性的渐变对象（使用该对象作为 strokeStyle 或 fillStyle 属性的值）。渐变可用于填充矩形、圆形、线条、文本等等

- createLinearGradient(x0,y0,x1,y1)
  - x0,y0：渐变的开始坐标
  - x,y：渐变的结束坐标

- addColorStop(stop, color)
  - stop：介于 0.0 与 1.0 之间的值，表示渐变中开始与结束之间的位置
  - color：在 stop 位置显示的颜色

~~~js
// 创建一个从左到右的渐变
var grd = cxt.createLinearGradient(0, 0, 200, 0);
grd.addColorStop(0, "black");
grd.addColorStop(0.3, "#222fff");
grd.addColorStop(0.5, "red");
grd.addColorStop(0.6, "#3334dd");
grd.addColorStop(0.8, "#333333");
grd.addColorStop(1, "green");
cxt.fillStyle = grd;
cxt.fillRect(0, 0, 200, 200);
~~~

设置圆型渐变

- createRadialGradient(x0,y0,r0,x1,y1,r1)：
  - x0,y0,ro：渐变的开始圆的 x，y 坐标和半径
  - x1,y1,r1：渐变的结束圆的 x，y 坐标和半径

~~~js
var rlg = cxt.createRadialGradient(300, 300, 10, 300, 300, 200);
rlg.addColorStop(0, "black");
rlg.addColorStop(0.3, "#222fff");
rlg.addColorStop(0.5, "red");
rlg.addColorStop(0.6, "#3334dd");
rlg.addColorStop(0.8, "#333333");
rlg.addColorStop(1, "green");
cxt.fillStyle = rlg;
cxt.fillRect(100, 100, 500, 500);   
~~~

设置背景图

- createPattern(image,repeat)
  - image：图片的对象
  - repeat：默认重复；repeat-x：水平方向重复；repeat-y：垂直方向重复；no-repeat：不重复

~~~js
var img = new Image();
img.src = "images/image-ui.jpeg";
var pat = cxt.createPattern(img,"repeat");
cxt.rect(0, 0, 900, 900);
cxt.fillStyle = pat;
cxt.fill();
~~~



#### 放大缩小、旋转、透明度，移动画布

- scale(2,2)：对当前绘图进行缩放，坐标和宽高会一起缩放，1=100%，0.5=50%，2=200%，依次类推
- rotate(angle)：旋转当前的绘图，angle是旋转的弧度
- translate(x,y)：x，y是移动后画布（0,0）坐标的位置，一般配合旋转和缩放
- globalAlpha=0.1：透明度，0是完全透明，1是不透明
- save()：保存当前状态
- restore()：还原上一次保存的ctx状态

~~~js
cxt.strokeRect(20, 20, 50, 50);

cxt.save(); // 保存当前状态
cxt.translate(200, 200); // 把画布的(0,0)坐标定义到(200,200)
cxt.rotate(30*Math.PI/180); // 旋转30°
cxt.globalAlpha = .3; // 透明度
cxt.strokeRect(20, 20, 50, 50);
cxt.scale(2,2); // 放大两倍
cxt.fillRect(20, 20, 50, 50);

cxt.restore(); // 还原上一次保存的ctx状态
cxt.strokeRect(50, 50, 50, 50);
~~~



#### 画布保存为base64编码内容

把 canvas 绘制的内容输出成base64内容

- canvas.toDataURL(type, encoderoptions);
  - type：设置输出的类型，如：image/png、image/jpeg等
  - encoderoptions：输出图片的质量，1：无损压缩，image/jpeg

~~~js
<img src="" alt="" id="image-1">

var img1 = document.getElementById("image-1");
img1.src = canvas.toDataURL("image/png",0.5);
~~~

#### 把一块画布在另一块画布上渲染

先在一块隐藏的画布上渲染完成，在另一块画布上展示出来

~~~js
canvasHide = document.getElementById("canvasH");
canvasShow = document.getElementById("canvasS");
cxtH = canvasHide.getContxt("2d");
cxtS = canvasShow.getContxt("2d");
// 在上面的canvas进行绘制，
canvasShow.drawImage(canvasHide,0,0);
~~~

#### 图片像素

- getImageData(x,y,w,h)：返回 ImageData 对象，该对象拷贝了画布指定矩形的像素数据
  - x，y是开始拷贝的坐标，w，h是拷贝的宽高
- putImageData(imgData,x,y)：putImageData() 方法将图像数据（从指定的 ImageData 对象）放回画布上
  - ImageData对象，x，y是放回画布的位置坐标



### 线条样式

lineCap 设置或返回线条的结束端头

~~~js
// butt（默认）、round（向线条的每个末端添加圆形线帽）、square
ctx.lineCap="round";
~~~

lineJoin当两条线条交汇时，创建圆形边角

~~~js
// bevel：创建斜角、 round：创建圆角、miter：默认。创建尖角
ctx.lineJoin="round";
~~~

lineWidth 线的宽度

~~~js
cxt.lineWidth = 4
~~~

meterLimit 最大的斜接长度

~~~js
ctx.miterLimit=10; // 越低线的交接角越是不尖
~~~



#### 贝塞尔曲线

绘制一条二次贝塞尔曲线

~~~js
// 起始点用moveTo定义，20,100是控制点，200,20是结束点
ctx.beginPath();
ctx.moveTo(20,20);
ctx.quadraticCurveTo(20,100,200,20);
ctx.stroke();
~~~

绘制三次贝塞尔曲线

绘制两条切线的弧

~~~js
~~~





### Konva 库

#### Konva 是什么

Konva 是一个 HTML5 Canvas JavaScript 开源框架，支持PC端和移动端，它可以轻松的实现桌面应用和移动应用中的图形交互交互效果

中文文档：http://konvajs-doc.bluehymn.com/docs/overview.html

GitHub：https://github.com/konvajs/konva

#### Konva 原理

Konva 的对象是以一颗树的形式保存的，Konva.Stage 是树的根节点，Stage 子节点是用户创建的图层 （Konva.Layer）。

节点结构图:

~~~
            Stage
                |
         +------+------+
         |             |
       Layer         Layer
         |             |
   +-----+-----+     Shape
   |           |
 Group       Group
   |           |
   +       +---+---+
   |       |       |
Shape   Group    Shape
           |
           +
           |
         Shape
~~~



#### 图形

##### Rect 矩形

~~~js
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>使用 Konva 库</title>
    <script src="https://unpkg.com/konva@4.0.18/konva.min.js"></script>
</head>
<body>
    <div id="container"></div>
</body>
</html>

<script>
    // 创建 stage 
    var stage = new Konva.Stage({
        container: "container",
        width: window.innerWidth,
        height: window.innerHeight
    });
	// 创建 Layer，可以创建很多层，背景层，动画层
    var layer = new Konva.Layer();
	
	// 创建矩形
    var rect1 = new Konva.Rect({
        x: 20,
        y: 20,
        width: 100,
        height: 50,
        fill: 'green',
        stroke: 'red',
        strokeWidth: 4
      });
    // add the shape to the layer
    layer.add(rect1);

    var rect2 = new Konva.Rect({
        x: 150,
        y: 40,
        width: 100,
        height: 50,
        fill: 'red',
        shadowBlur: 10,
        cornerRadius: 10
      });

   	// add the shape to the layer
    layer.add(rect2);
    
    // add the layer to the stage 
    stage.add(layer);
</script>
~~~

>可以去文档查看更多的属性和方法说明



## HTML5 SVG

### SVG 简介

SVG 时一种基于 XML 语法的图像格式，全称时可缩放矢量图（Scalable Vector Graphics）。其他图像格式都是基于像素处理，SVG是对图像的形状描述，本质上是文本文件，放大缩小都不会失真



### 在HTML中使用SVG

1、直接插入HTML页面，可以直接使用svg标签

内嵌SVG最大的优势就是方便交互，不论是JS还是CSS，都可以方便的操作SVG。可以通过JS像操作DOM一样操作SVG元素，添加事件等等，通过CSS也可以很容易的控制SVG的样式。
另外，因为SVG直接包含在HTML文档中，所以无需像img嵌入的方式一样发送HTTP请求，但是同样也有可能导致文件体积变大，并且也无法缓存。
这种方式大多数是用在重交互的场景，比如图表。

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SVG-开始使用</title>
</head>
<body>
    <svg height="500px" width="500px" style="border:1px solid red">
        <rect x="0" y="0" height="100" width="100" style="fill:red; stroke:black; stroke-width:5;fill-opacity:0.1;stroke-opacity:0.9" ></rect>
    </svg>
    
</body>
</html>
~~~

2、SVG 代码可以是一个独立文件，引入到HTML中

图像的渲染和页面是分离的，两者之间无法进行通信，父页面的样式对SVG无法生效，父页面的js脚本也无法操作SVG，所以说只适合单纯作为图片展示用

~~~html
<img src="circle.svg">
~~~

circle.svg

~~~svg
<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
    <rect x="0" y="0" height="100" width="100" style="fill:red; stroke:black; stroke-width:5;fill-opacity:0.1;stroke-opacity:0.9" ></rect>
</svg>
~~~

### svg文件

SVG 文件推荐使用 .svg（全部小写）作为此类文件的扩展名，SVG 代码都放在顶层标签`<svg>`之中

`<svg> height`属性，指定了 SVG 图像在 HTML 元素中所占据的宽度和高度。除了相对单位，也可以采用绝对单位（单位：像素）。如果不指定这两个属性，SVG 图像默认大小是300像素（宽） x 150像素（高）

~~~svg
<svg xmlns="http://www.w3.org/2000/svg" version="1.1" width=1000 height="1000">
    <rect x="0" y="0" height="100" width="100" style="fill:red; stroke:black; stroke-width:5;fill-opacity:0.1;stroke-opacity:0.9" ></rect>
</svg>
~~~



### SVG 形状

#### SVG 矩形（rect）

`<rect>`标签用来创建矩形

~~~html
<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
    <rect x="0" y="0" height="100"  width="100" style="fill:red; stroke:black; stroke-width:5;fill-opacity:0.1;stroke-opacity:0.9" ></rect>
</svg>
~~~

- rect 元素的 width 和 height 属性可定义矩形的高度和宽度
- style 属性用来定义 CSS 属性
- CSS 的 fill 属性定义矩形的填充颜色（rgb 值、颜色名或者十六进制值）
- CSS 的 stroke-width 属性定义矩形边框的宽度
- CSS 的 stroke 属性定义矩形边框的颜色
- rx 和 ry 属性可使矩形产生圆角
- CSS opacity 属性用于定义了元素的透明值 (范围: 0 到 1)



#### SVG 圆形（circle）

`<circle> `标签可用来创建一个圆

~~~html
<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
  <circle cx="100" cy="50" r="40" stroke="black"
  stroke-width="2" fill="red"/>
</svg>
~~~

- cx和cy属性定义圆点的x和y坐标。如果省略cx和cy，圆的中心会被设置为(0, 0)
- r属性定义圆的半径



#### SVG 椭圆（ellipse）

~~~html
<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
  <ellipse cx="300" cy="80" rx="100" ry="50"
  style="fill:yellow;stroke:purple;stroke-width:2"/>
</svg>
~~~



#### SVG 直线（line）

~~~html
<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
  <line x1="0" y1="0" x2="200" y2="200"
  style="stroke:rgb(255,0,0);stroke-width:2"/>
</svg>
~~~



#### SVG 多边形（polygon）

`<polygon> `标签用来创建含有不少于三个边的图形

~~~html
<svg  height="210" width="500">
  <polygon points="200,10 250,190 160,210"
  style="fill:lime;stroke:purple;stroke-width:1"/>
</svg>
~~~



#### SVG 多线段

`<polyline>` 元素是用于创建任何只有直线的形状

~~~html
<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
  <polyline points="20,20 40,25 60,40 80,120 120,140 200,180"
  style="fill:none;stroke:black;stroke-width:3" />
</svg>
~~~



#### SVG 路径

`<path>` 元素用于定义一个路径

开始于位置150 0，到达位置75 200，然后从那里开始到225 200，最后在150 0关闭路径

~~~html
<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
    <path d="M150 0 L75 200 L225 200 Z" />
</svg>
~~~

- M = moveto ：开始路径
- L = lineto：
- H = horizontal lineto
- V = vertical lineto
- C = curveto
- S = smooth curveto
- Q = quadratic Bézier curve
- T = smooth quadratic Bézier curveto
- A = elliptical Arc
- Z = closepath

注意：以上所有命令均允许小写字母。大写表示绝对定位，小写表示相对定位。



#### SVG 文本

`<text>` 元素用于定义文本

~~~html
<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
  <text x="0" y="15" fill="red">I love SVG</text>
</svg>

<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
  <text x="10" y="20" style="fill:red;">Several lines:
    <tspan x="10" y="45">First line</tspan>
    <tspan x="10" y="70">Second line</tspan>
  </text>
</svg>
~~~



#### SVG stroke 属性

stroke属性，可应用于任何种类的线条

- stroke（颜色）
- stroke-width（宽度）
- stroke-linecap（线结点的样式：butt/round/square）
- stroke-dasharray（虚线：stroke-dasharray = 5,5）



### SVG 滤镜

SVG 滤镜用来向形状和文本添加特殊的效果

- feBlend - 与图像相结合的滤镜
- feColorMatrix - 用于彩色滤光片转换
- feComponentTransfer
- feComposite
- feConvolveMatrix
- feDiffuseLighting
- feDisplacementMap
- feFlood
- feGaussianBlur
- feImage
- feMerge
- feMorphology
- feOffset - 过滤阴影
- feSpecularLighting
- feTile
- feTurbulence
- feDistantLight - 用于照明过滤
- fePointLight - 用于照明过滤
- feSpotLight - 用于照明过滤



#### 定义滤镜

SVG滤镜定义在`<defs>`元素，`<filter>`标签用来定义滤镜



模糊滤镜

~~~html
<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
  <defs>
    <!-- id属性定义滤镜唯一名称 -->
    <filter id="f1" x="0" y="0">
        <!-- stdDeviation属性定义模糊量 -->
      <feGaussianBlur in="SourceGraphic" stdDeviation="15" />
    </filter>
  </defs>
  <!-- filter="url(#f1)链接到滤镜 -->  
  <rect width="90" height="90" stroke="green" stroke-width="3"
  fill="yellow" filter="url(#f1)" />
</svg>
~~~



阴影滤镜

~~~html
<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
  <defs>
    <filter id="f1" x="0" y="0" width="200%" height="200%">
      <feOffset result="offOut" in="SourceGraphic" dx="20" dy="20" />
      <feBlend in="SourceGraphic" in2="offOut" mode="normal" />
    </filter>
  </defs>
  <rect width="90" height="90" stroke="green" stroke-width="3"
  fill="yellow" filter="url(#f1)" />
</svg>
~~~



### SVG渐变

SVG 渐变必须在 `<defs>` 标签中进行定义

#### 线性渐变

`<linearGradient>` 可用来定义 SVG 的线性渐变

`<linearGradient> `标签必须嵌套在` <defs>` 的内部。`<defs>` 标签是 definitions 的缩写，它可对诸如渐变之类的特殊元素进行定义。

线性渐变可被定义为水平、垂直或角形的渐变：

- 当 y1 和 y2 相等，而 x1 和 x2 不同时，可创建水平渐变
- 当 x1 和 x2 相等，而 y1 和 y2 不同时，可创建垂直渐变
- 当 x1 和 x2 不同，且 y1 和 y2 不同时，可创建角形渐变

~~~html
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<svg width="100%" height="100%" version="1.1"
xmlns="http://www.w3.org/2000/svg">

<defs>
<linearGradient id="orange_red" x1="0%" y1="0%" x2="100%" y2="0%">
<stop offset="0%" style="stop-color:rgb(255,255,0);
stop-opacity:1"/>
<stop offset="100%" style="stop-color:rgb(255,0,0);
stop-opacity:1"/>
</linearGradient>
</defs>

<ellipse cx="200" cy="190" rx="85" ry="55"
style="fill:url(#orange_red)"/>

</svg>
~~~

- `<linearGradient>` 标签的 id 属性可为渐变定义一个唯一的名称
- fill:url(#orange_red) 属性把 ellipse 元素链接到此渐变
- `<linearGradient>` 标签的 x1、x2、y1、y2 属性可定义渐变的开始和结束位置
- 渐变的颜色范围可由两种或多种颜色组成。每种颜色通过一个 `<stop>` 标签来规定。offset 属性用来定义渐变的开始和结束位置。



#### 放射性渐变

`<radialGradient>` 用来定义放射性渐变。

~~~html
<svg width="100%" height="100%" version="1.1"
xmlns="http://www.w3.org/2000/svg">

<defs>
<radialGradient id="grey_blue" cx="50%" cy="50%" r="50%"
fx="50%" fy="50%">
<stop offset="0%" style="stop-color:rgb(200,200,200);
stop-opacity:0"/>
<stop offset="100%" style="stop-color:rgb(0,0,255);
stop-opacity:1"/>
</radialGradient>
</defs>

<ellipse cx="230" cy="200" rx="110" ry="100"
style="fill:url(#grey_blue)"/>

</svg>
~~~



## Canvas VS SVG

#### SVG

SVG 是一种使用 XML 描述 2D 图形的语言。

SVG 基于 XML，这意味着 SVG DOM 中的每个元素都是可用的。您可以为某个元素附加 JavaScript 事件处理器。

在 SVG 中，每个被绘制的图形均被视为对象。如果 SVG 对象的属性发生变化，那么浏览器能够自动重现图形。



#### Canvas

Canvas 通过 JavaScript 来绘制 2D 图形。

Canvas 是逐像素进行渲染的。

在 canvas 中，一旦图形被绘制完成，它就不会继续得到浏览器的关注。如果其位置发生变化，那么整个场景也需要重新绘制，包括任何或许已被图形覆盖的对象。



#### Canvas 与 SVG 的比较

Canvas

- 依赖分辨率
- 不支持事件处理器
- 弱的文本渲染能力
- 能够以 .png 或 .jpg 格式保存结果图像
- 最适合图像密集型的游戏，其中的许多对象会被频繁重绘

SVG

- 不依赖分辨率
- 支持事件处理器
- 最适合带有大型渲染区域的应用程序（比如谷歌地图）
- 复杂度高会减慢渲染速度（任何过度使用 DOM 的应用都不快）
- 不适合游戏应用



# HTML 媒体



## HTML 多媒体

多媒体来自多种不同的格式。它可以是您听到或看到的任何内容，文字、图片、音乐、音效、录音、电影、动画等等。

在因特网上，您会经常发现嵌入网页中的多媒体元素，现代浏览器已支持多种多媒体格式。

在本教程中，您将了解到不同的多媒体格式，以及如何在您的网页中使用它们。



**浏览器支持**

第一款因特网浏览器只支持文本，而且即使是对文本的支持也仅限于单一字体和单一颜色。随后诞生了支持颜色、字体和文本样式的浏览器，图片支持也被加入。

不同的浏览器以不同的方式处理对音效、动画和视频的支持。某些元素能够以内联的方式处理，而某些则需要额外的插件



**多媒体格式**

多媒体元素（比如视频和音频）存储于媒体文件中。

确定媒体类型的最常用的方法是查看文件扩展名。当浏览器得到文件扩展名 .htm 或 .html 时，它会假定该文件是 HTML 页面。.xml 扩展名指示 XML 文件，而 .css 扩展名指示样式表。图片格式则通过 .gif 或 .jpg 来识别。

多媒体元素元素也拥有带有不同扩展名的文件格式，比如 .swf、.wmv、.mp3 以及 .mp4



### **视频格式**

MP4 格式是一种新的即将普及的因特网视频格式。HTML5 、Flash 播放器以及优酷等视频网站均支持它。

| 格式      | 文件      | 描述                                                         |
| :-------- | :-------- | :----------------------------------------------------------- |
| AVI       | .avi      | AVI (Audio Video Interleave) 格式是由微软开发的。所有运行 Windows 的计算机都支持 AVI 格式。它是因特网上很常见的格式，但非 Windows 计算机并不总是能够播放。 |
| WMV       | .wmv      | Windows Media 格式是由微软开发的。Windows Media 在因特网上很常见，但是如果未安装额外的（免费）组件，就无法播放 Windows Media 电影。一些后期的 Windows Media 电影在所有非 Windows 计算机上都无法播放，因为没有合适的播放器。 |
| MPEG      | .mpg.mpeg | MPEG (Moving Pictures Expert Group) 格式是因特网上最流行的格式。它是跨平台的，得到了所有最流行的浏览器的支持。 |
| QuickTime | .mov      | QuickTime 格式是由苹果公司开发的。QuickTime 是因特网上常见的格式，但是 QuickTime 电影不能在没有安装额外的（免费）组件的 Windows 计算机上播放。 |
| RealVideo | .rm.ram   | RealVideo 格式是由 Real Media 针对因特网开发的。该格式允许低带宽条件下（在线视频、网络电视）的视频流。由于是低带宽优先的，质量常会降低。 |
| Flash     | .swf.flv  | Flash (Shockwave) 格式是由 Macromedia 开发的。Shockwave 格式需要额外的组件来播放。但是该组件会预装到 Firefox 或 IE 之类的浏览器上。 |
| Mpeg-4    | .mp4      | Mpeg-4 (with H.264 video compression) 是一种针对因特网的新格式。事实上，YouTube 推荐使用 MP4。YouTube 接收多种格式，然后全部转换为 .flv 或 .mp4 以供分发。越来越多的视频发布者转到 MP4，将其作为 Flash 播放器和 HTML5 的因特网共享格式。 |

### **声音格式**

音频格式一般分为3大类：未压缩音频格式、有损压缩音频格式和无损压缩音频格式



**未压缩音频格式**

1、PCM

PCM 代表脉冲编码调制，原始模拟音频信号的数字表示，PCM 是 CD 和 DVD 中最常用的音频格式

2、WAV（wav）

WAV（waveform）代表波形音频文件格式。这是 Microsoft 和 IBM 于 1991 年制定的标准，大多数 WAV 文件都包含 PCM 格式的未压缩音频。 WAV 文件只是 PCM 编码的包装器

更适合在 Windows 系统上使用（Max也可以使用）

3、AIFF（.aiff）

AIFF 代表音频交换文件格式。 与 Microsoft 和 IBM 为 Windows 开发 WAV 的方式类似，AIFF 是 Apple 于 1988 年为 Mac 系统开发的一种音频文件格式

与 WAV 文件类似，AIFF 文件可以包含多种音频格式，大多数 AIFF 文件包含 PCM 格式的未压缩音频。 AIFF 文件只是 PCM 编码的包装器。

更适合在 Mac 系统上使用（Window也可以使用）



**有损压缩音频格式**

1、MP3（.mp3）

MP3 代表 MPEG-1 Audio Layer 3，MP3 文件实际上是 MPEG 文件的声音部分。MPEG 格式最初是由运动图像专家组开发的。它于 1993 年发布并迅速流行，最终成为世界上最流行的音乐文件音频格式，MP3 这个术语已经成为数字音乐的代名词

2、AAC

AAC 代表高级音频编码。 它于 1997 年作为 MP3 的继任者而开发，虽然它确实作为一种流行的音频格式流行起来，但它从未真正超过 MP3 成为最受欢迎的格式

AAC 使用的压缩算法比 MP3 更先进和技术性更高，因此当您比较 MP3 和 AAC 格式的相同录音以相同的比特率时，AAC 的音质通常会更好。

尽管 MP3 更像是一种家庭格式，但今天 AAC 仍然被广泛使用。 事实上，它是 YouTube、Android、iOS、iTunes、后来的任天堂便携式电脑和后来的 PlayStation 使用的标准音频压缩方法

3、OGG （.ogg）

OGG 不代表任何东西。 实际上，它甚至不是一种压缩格式。 相反，OGG 是一个多媒体容器，可以保存各种压缩格式，但最常用于保存 Vorbis 文件，因此这些音频文件被称为 Ogg Vorbis 文件

Vorbis 于 2000 年首次发布并越来越受欢迎，原因有两个：它遵循开源软件的原则，并且它的性能明显优于大多数其他有损压缩格式（这意味着它可以在同等音频质量的情况下生成更小的文件） 

MP3 和 AAC 拥有如此强大的立足点，以至于 OGG 很难进入聚光灯下，没有多少设备本身支持它。但随着时间的推移它变得越来越好。 目前，它主要由开源软件的铁杆支持者使用。

4、WMA

WMA 格式 (Windows Media Audio) 代表 Windows 媒体音频。 它于 1999 年首次发布，此后经历了多次演变，同时保持相同的 WMA 名称和扩展名。 它是由 Microsoft 创建的专有格式

与 AAC 和 OGG 不同，WMA 旨在解决 MP3 压缩方法中的一些缺陷。事实证明，WMA 的压缩方法与 AAC 和 OGG 非常相似。 所以是的，就客观压缩质量而言，WMA 实际上是比 MP3 更好的音频文件类型。

但由于 WMA 是专有的，因此支持它的设备和平台并不多。 与 AAC 或 OGG 相比，它也没有提供任何真正的好处，因此当 MP3 不够好时，使用这两者之一而不是 WMA 更实用。



**无损压缩音频格式**

与有损压缩相反的是无损压缩，这是一种减少音频文件大小的方法，而不会丢失源音频文件和压缩音频文件之间的任何数据。

缺点是无损压缩音频文件比有损压缩音频文件大，对于相同的源文件最多大 2 到 5 倍

1、PLAC

FLAC 代表免费无损音频编解码器。 可能有点不妥，但自 2001 年推出以来，它已迅速成为最受欢迎的无损格式之一。

很棒的是，FLAC 可以将原始源文件压缩多达 60%，而不会丢失任何数据。 更好的是，FLAC 是一种开源且免版税的音频文件格式，因此它没有施加任何知识产权限制。

大多数主要程序和设备都支持 FLAC，并且是 MP3 音乐的主要替代品。 有了它，您可以以一半的文件大小获得完整质量的原始未压缩音频。 这就是为什么许多人将 FLAC 视为最佳音频格式的原因。

2、ALAC（苹果）

ALAC 代表 Apple 无损音频编解码器。 它于 2004 年作为专有格式开发和推出，但最终在 2011 年成为开源和免版税的。ALAC 有时被称为 Apple Lossless。

虽然 ALAC 很好，但在压缩方面它的效率略低于 FLAC。 但是，Apple 用户实际上并没有在两者之间做出选择，因为 iTunes 和 iOS 都提供对 ALAC 的原生支持，而根本不支持 FLAC。

3、WMA（Windows）

WMA 代表 Windows 媒体音频。 我们在上面的有损压缩部分中介绍了这一点，但我们在这里提到它是因为有一种称为 WMA Lossless 的无损替代方案，它使用相同的扩展名。 令人困惑，我知道。

与 FLAC 和 ALAC 相比，WMA Lossless 在压缩效率方面是最差的——但差不了多少。 它是一种专有格式，因此对开源软件的粉丝不利，但它在 Windows 和 Mac 系统上都得到了本机支持。

WMA Lossless 的最大问题是硬件支持有限。 如果您想在多个设备和平台上播放无损压缩音频，您应该坚持使用 FLAC。



### HTML5 支持的音频格式

HTML 支持三种音频格式：

1. MP3（有损压缩）
2. OGG（有损压缩，开源）
3. WAV（微软公司、未压缩）



2022主流浏览器支持的音频格式

| 浏览器               | MP3        | Wav       | Ogg       |
| -------------------- | ---------- | --------- | --------- |
| Internet Explorer 9+ | YES        | NO        | NO        |
| Chrome 6+            | YES        | YES       | YES       |
| Firefox 3.6+         | YES        | YES       | YES       |
| Safari 5+            | YES        | YES       | NO        |
| Opera 10+            | YES        | YES       | YES       |
|                      | audio/mpeg | audio/wav | audio/ogg |



## HTML 插件

插件（Plug-in）是扩展浏览器标准功能的计算机程序



`<object>` **元素**

所有浏览器都支持`<object>`元素，它可以定义HTML 文档中的嵌入式对象，如将插件嵌入网页中，也可以嵌入HTML

~~~html
<object width="100%" height="500px" data="snippet.html"></object>
<object data="audi.jpeg"></object>
~~~



`<embed>` **元素**

所有主要浏览器均支持 `<embed>` 元素，`<embed> `元素也可定义了 HTML 文档中的嵌入式对象。


Web 浏览器长期以来一直支持 `<embed>` 元素。但是，它不属于 HTML5 之前的 HTML 规范的一部分，是一个HTML5 标签

~~~html
<embed src="audi.jpeg">
<embed width="100%" height="500px" src="snippet.html">
~~~

请注意，`<embed>` 元素没有结束标记。它无法包含替代文本。

`<embed> `元素也可用于在 HTML 中包含 HTML



## HTML 音频

在 HTML 中播放声音的方法有很多，可以使用 object embed 标签嵌入插件

~~~HTML
<embed  src="syst.mp3" />
<object data="syst.mp3"></object>
~~~

不同浏览器对音频格式的支持不同，无法在所有浏览器中播放（现在所有主流浏览器都支持MP3）



#### 使用 HTML5 audio 元素

audio 是一个HTML 5 元素，定义声音，比如音乐或其他音频流，不支持audio会将它当成普通标签

~~~html
<audio controls="controls">
    <source src="syst.mp3" type="audio/mp3" />
    <source src="syst.ogg" type="audio/ogg" />
    <embed src="syst.mp3" />
    Your browser does not support the audio element.
</audio>
~~~

HTML5 `<audio>` 元素会尝试以 mp3 或 ogg 来播放音频，如果失败，如果失败，代码将回退尝试 `<embed>` 元素（为旧版浏览器做兼容）。都不支持，会显示错误信息

**audio 的属性**

| 属性     | 值                 | 描述                                      |
| -------- | ------------------ | ----------------------------------------- |
| autoplay | autoplay           | 自动播放                                  |
| controls | controls           | 显示播放控件                              |
| loop     | loop               | 循环播放                                  |
| muted    | muted              | 默认静音                                  |
| preload  | auto 、meta 、none | 预加载，如果使用 "autoplay"，则忽略该属性 |
| src      | url                | 要播放的音频的 URL                        |



#### 使用雅虎媒体播放器

点击标签链接，会弹出播放器

~~~html
<a href="syst.mp3">播放</a>
<script type="text/javascript" src="http://mediaplayer.yahoo.com/js"></script>
~~~

使用 a 标签，跟上面类似

~~~html
<a href="syst.mp3">播放</a>
~~~

 

## HTML 视频

在 HTML 中播放声音的方法有很多，可以使用 object embed 标签嵌入插件

~~~html
<embed  src="syst.mp4" />
<object data="syst.mp4"></object>
~~~



#### 使用 HTML5 video 元素

H5支持的媒体格式主要有MP4、OGG、WebM、M3U8，不支持flv

~~~html
<div>
    <video height="500" controls="controls">
        <source src="vedio.mp4" type="video/mp4" />
        <source src="vedio.ogg" type="video/ogg" />
        <source src="vedio.webm" type="video/webm" />
        <embed src="movie.swf" width="320" height="240" />
        Your browser does not support the video tag
    </video>
</div>
~~~



#### 可以链接优酷的地址

如果您希望在网页中播放视频，那么您可以把视频上传到优酷等视频网站，然后在您的网页中插入 HTML 代码即可播放视频

~~~html
<embed src="http://player.youku.com/player.php/sid/XMzI2NTc4NTMy/v.swf" 
width="480" height="400" 
type="application/x-shockwave-flash">
</embed>
~~~



#### 使用 超链接

如果网页包含指向媒体文件的超链接，大多数浏览器会使用“辅助应用程序”来播放文件。

~~~html
<a href="video.mp4">Play a video file</a>
~~~



#### video 的属性

| 属性     | 值                 | 描述                                      |
| -------- | ------------------ | ----------------------------------------- |
| autoplay | autoplay           | 自动播放                                  |
| controls | controls           | 显示播放控件                              |
| loop     | loop               | 循环播放                                  |
| muted    | muted              | 默认静音                                  |
| preload  | auto 、meta 、none | 预加载，如果使用 "autoplay"，则忽略该属性 |
| src      | url                | 要播放的音频的 URL                        |
| poster   | url                | 点击播放按钮前显示的图像                  |
| width    | px                 | 播放器的宽度                              |
| height   | px                 | 播放器的高度                              |



## HTML YouTube 视频

在 HTML 中包含视频的最简单的方法是，使用 YouTube。

YouTobe 的视频有一个唯一ID（网址后面：ih1l6wb7LhU），您可以使用这个 id，并在 HTML 代码中引用您的视频



**在 HTML 中 播放 YouTobe 视频**

1. 将视频上传到 YouTobe，记录ID
2. 用插件元素embed、object

~~~html
<embed width="420" height="345" src="https://www.youtube.com/embed/pi1MQ3SsWwY"></embed>
<object width="420" height="345" data="https://www.youtube.com/embed/pi1MQ3SsWwY"></object>
~~~

属性加载 url 后面

~~~html
<embed width="420" height="345" src="https://www.youtube.com/embed/pi1MQ3SsWwY?autoplay=1&mute=1"></embed>
~~~





