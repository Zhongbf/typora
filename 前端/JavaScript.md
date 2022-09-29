# JavaScript 代码约定

### 命名约定

所有的代码使用相同的命名约定

- 变量和函数名以驼峰大小写来写
- 全局变量使用大写
- 常量（比如 PI）使用大写

变量和函数使用小驼峰写法，所有名称以字母开头

~~~js
firstName = "Bill";
price = 19.90;
~~~



### 运算符周围的空格

请始终在运算符（ = + - * / ）周围以及逗号之后添加空格

~~~js
var x = y + z;
var values = ["Volvo", "Saab",  "Fiat"];
~~~



### 代码缩进

请始终使用对代码块缩进使用 4 个空格

~~~js
function toCelsius(fahrenheit) {
    return (5 / 9) * (fahrenheit - 32);
}
~~~



### 语句规则

简单语句的通用规则：请始终以分号结束单条语句

~~~js
var values = ["Volvo", "Saab",  "Fiat"];

var person = {
    firstName: "Bill",
     lastName: "Gates",
    age: 50,
    eyeColor:  "blue"
};
~~~

### 复杂语句：

- 请在第一行的结尾处写开括号
- 请在开括号前使用一个空格
- 请在新行上写闭括号，不带前导空格
- 请不要以分号来结束复杂语句

~~~js
// 函数
function toCelsius(fahrenheit) {
    return (5 / 9) * (fahrenheit - 32);
}
// 循环
for (i = 0; i < 5; i++) {
    x += i;
}
// 条件
if (time < 20) {
    greeting = "Good day";
} else {
     greeting = "Good evening";
}
~~~

### 对象规则

针对对象定义的通用规则：

- 把开括号与对象名放在同一行
- 在每个属性与其值之间使用冒号加一个空格
- 不要在最后一个属性值对后面写逗号
- 请在新行上写闭括号，不带前导空格
- 请始终以分号结束对象定义

~~~js
var person = {
    firstName: "Bill",
    lastName: "Gates",
    age: 19,
    eyeColor:  "blue"
};
// 可以对短对象在一行中进行压缩，只在属性之间使用空格
var person = {firstName:"Bill", lastName:"Gates", age:50, eyeColor:"blue"};
~~~

### 行长度小于 80

为了提高可读性，请避免每行的长度超过 80 个字符

### 在 HTML 中加载 JavaScript

使用简单的语法来加载外部脚本（type 属性不是必需的）

~~~js
<script src="myscript.js"></script>
~~~

### 访问 HTML 元素

使用“不整洁的” HTML 样式的后果，也许是导致 JavaScript 错误

这两条 JavaScript 语句会产生不同的结果（HTML 不区分大小写，最好不要这样做）

~~~js
var obj = getElementById("Demo")
var obj = getElementById("demo") 
~~~

### 文件扩展名

HTML 文件应该使用 .html 扩展名（而非 .htm）。

CSS 文件应该使用 .css 扩展名。

JavaScript 文件应该使用 .js 扩展名。

### 使用小写文件名

大多数 web 服务器（Apache、Unix）对文件名的大小写敏感：

london.jpg 无法视作 London.jpg 进行访问。

其他 web 服务器（微软的 IIS）对大小写不敏感：

london.jpg 能够以 London.jpg 或 london.jpg 来访问。

如果您混合使用大小写，则必须严格保持连续和一致。

如果您将站点从大小写不敏感的服务器转移至对大小写敏感的服务器，即使这种小错误也可能破坏您的网站。

为了避免这些问题，请始终使用小写文件名（如果可能）。

### 性能

计算机不会使用代码约定。大部分规则对程序的执行影响很小。

缩进和额外的空格对小段脚本并不重要。

对于开发中的脚本，应该优先考虑可读性。应该缩小更大型的生产脚本。