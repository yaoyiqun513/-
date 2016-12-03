[TOC]

# JavaScript权威指南笔记

## JavaScript概述

````html
<html>
  <head>
  <script src="library.js"></script><!-- 引入一个Javascript库 -->
  </head>  
  <body>
    <p>
      This is a paragraph of HTML
    </p>
    <script>
      //在这里编写嵌入到HTML文件中的Javascript代码
    </script>
    <p>
      Here is more HTML.
    </p>
  </body>
</html>
````

定义事件处理程序最简单的方法是，给HTML的以`on`为前缀的属性绑定一个回调函数。当写一些简单的测试程序是，最实用的方法就是给`onclick`处理程序绑定回调。

- 如何在文档中查找元素
- 如何通过表单input元素来获取用户的输入数据
- 如何通过文档元素来设置HTML内容
- 如何将数据存储在浏览器中
- 如何使用脚本发送HTTP请求
- 如何利用`<canvas>`元素绘图
##JavaScript语言核心

JavaScript程序使用`UTF-16`编码的`Unicode`字符集编写的。`ECMAScript5`要求支持`Unicode3`及后续版本。

JavaScript区分大小写，而HTML并不区分大小写。在HTML种，这些标签和属性名可以使用大写也可以是小写，而在JavaScript中则必须是小写。例如在HTML中设置事件处理程序可以是`onclick`或者`onClick`，但是在JavaScript中必须使用`onclick`。

### JavaScript字符

可识别的表示为**空格**的字符：

- 普通空格符(\u0020)

- 水平制表符(\u0009)

- 垂直制表符(\u000B)

- 换页符(\uoooc)

- 不中断空白(\u00A0)

- 字节序标记(\uFEFF)

可识别为表示为**行结束符**的字符：

- 换行符(\u000A)
- 回车符(\u000D)
- 行分隔符(\u2028)
- 段分隔符(\u2029)

### JavaScript保留字

|  break   | delete  |  function  | return | typeof |
| :------: | :-----: | :--------: | :----: | :----: |
|   case   |   do    |     if     | switch |  var   |
|  catch   |  else   |     in     |  this  |  void  |
| continue |  false  | instanceof | throw  |  void  |
| debugger | finally |    new     |  true  |  with  |
| default  |   for   |    null    |  try   |        |

ECMAScript5保留了一下关键字：

`class` `const` `enum` `export` `extends` `import` `super`

### JavaScript预定义的全局变量和函数

|     arguments      |     encodeURI      | Infinity |     Number     |   RegExp    |
| :----------------: | :----------------: | :------: | :------------: | :---------: |
|       Array        | encodeURIComponent | isFinite |     Object     |   String    |
|      Boolean       |       Error        |  isNan   |   parseFloat   | SyntaxError |
|        Date        |        eval        |   JSON   |    parseInt    |  TypeError  |
|     decodeURI      |     EvalError      |   Math   |   RangeError   |  undefined  |
| decodeURIComponent |      Function      |   NaN    | ReferenceError |  URIError   |

### JavaScript函数行为

`构造函数`：用函数来初始化(使用new运算符)一个新建的对象，每个构造函数定义了一类(class)对象——由构造函数初始化的对象组成的集合。

`浮点表示法`:正则表达式为\[digits]\[.digits][(E|e)[(+|-)]digits]

### JavaScript转义字符

| 转义字符       | 含义                            |
| ---------- | ----------------------------- |
| \o         | NUL字符(\u0000)                 |
| \b         | 退格符(\u0008)                   |
| \t         | 水平制表符(\u0009)                 |
| \n         | 换行符(\u000A)                   |
| \v         | 垂直制表符(\u000B)                 |
| \f         | 换页符(\u000C)                   |
| \r         | 回车符(\u000D)                   |
| \"         | 双引号(\u0022)                   |
| \'         | 撇号或单引号(\u0027)                |
| \\         | 反斜线(\u005C)                   |
| \x**XX**   | 由两位十六进制数**XX**制定的Latin-1字符    |
| \u**XXXX** | 由4位十六进制数**XXXX**制定的字Unicode字符 |



<img src='http://g.gravizo.com/g? 
digraph G {
   main -> parse -> execute;
   main -> init;
   main -> cleanup;
   execute -> make_string;
   execute -> printf
   init -> make_string;
   main -> printf;
   execute -> compare;
 }/>



