# JavaScript知识点



------



主讲：**MagnumHou**

微信公众号：**前端知识分享喵**

<img src="http://121.89.192.46:8888/ganhuo/weChat.png" alt="微信图片_20200601153857" style="zoom:80%;" />



------



[TOC]

------



# 一、javascript简介

## 1.1 Javascript简史

在WEB日益发展的同时，网页的大小和复杂性不断增加，受制于网速的限制，为完成简单的表单验证而频繁地与服务器交换数据只会加重用户的负担，当时走在技术革新最前沿的<u>**Netscape（网景） 公司**</u>，决定着手开发一种客户端语言，用来处理这种简单的验证。

1995年，就职于**<u>Netscape 公司的布兰登·艾奇（Brendan Eich）</u>**，开始着手为即将于1996年2月发布的Netscape Navigator 2浏览器开发一种名为 **<u>LiveScript</u> 的脚本语言**。为了尽快完成LiveScript 的开发，Netscape 与Sun 公司建立了一个开发联盟。在Netscape Navigator 2 正式发布前夕，Netscape 为了搭上媒体热炒Java 的顺风车，临时把LiveScript 改名为JavaScript。

由于JavaScript1.0获得的关注度越来越高，1996年，微软就在其Internet Explorer 3 中加入了名为**<u>JScript</u>** 的JavaScript 实现，这意味着有了两个不同的JavaScript 版本，导致JavaScript没有一个标准化的语法和特性。

1997 年，以JavaScript 1.1 为蓝本的建议被提交给了**<u>欧洲计算机制造商协会（ECMA</u>**，European Computer Manufacturers Association）。该协会指定39 号技术委员会（TC39，Technical Committee #39）负责“ **<u>标准化一种通用、跨平台、供应商中立的脚本语言的语法和语义</u>**”。TC39 由来自Netscape、Sun、微软、Borland 及其他关注脚本语言发展的公司的程序员组成，他们经过数月的努力完成了ECMA-262标准，定义一种名为**<u>ECMAScript的新脚本语言。</u>**

 

布兰登·艾奇（1961年～），JavaScript的发明人，目前（2005年至2014年）在Mozilla公司担任CTO。2014年4月3日，出任Mozilla的CEO十天就被迫辞职。

2017年5月，Brendan Eich发起的去中心化网页浏览器“Brave”仅30秒就完成了约3千5百万美元的ICO发售。

![image-20201228115608927](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20201228115608927.png)

 

## 1.2 ECMAScript版本发展

1998年6月，ECMAScript 2.0版发布。

1999年12月，ECMAScript 3.0版发布，成为JavaScript的通行标准，得到了广泛支持。

2007年10月，ECMAScript 4.0版草案发布，对3.0版做了大幅升级。草案发布后，由于4.0版的目标过于激进，各方对于是否通过这个标准，发生了严重分歧。以Yahoo、Microsoft、Google为首的大公司，反对JavaScript的大幅升级，主张小幅改动；以JavaScript创造者Brendan Eich为首的Mozilla公司，则坚持当前的草案。

2008年7月，由于各方分歧太大，争论过于激进，ECMA开会决定，中止ECMAScript 4.0的开发，将其中涉及现有功能改善的一小部分，发布为ECMAScript 3.1，而将其他激进的设想扩大范围，放入以后的版本，由于会议的气氛，该版本的项目代号起名为Harmony（和谐）。会后不久，ECMAScript 3.1就改名为ECMAScript 5。

2009年12月，ECMAScript 5.0版正式发布。Harmony项目则一分为二，一些较为可行的设想定名为JavaScript.next继续开发，后来演变成ECMAScript 6；一些不是很成熟的设想，则被视为JavaScript.next.next，在更远的将来再考虑推出。

2011年6月，ECMAscript 5.1版发布，并且成为ISO国际标准（ISO/IEC 16262:2011）。 https://babeljs.io/learn-es2015/

2013年3月，ECMAScript 6草案冻结，不再添加新功能。新的功能设想将被放到ECMAScript 7。

2013年12月，ECMAScript 6草案发布。然后是12个月的讨论期，听取各方反馈。

**<u>2015年6月17日，ECMAScript 6发布正式版本，即ECMAScript 2015。</u>http://www.ecma-international.org/ecma-262/6.0/**

ES 2016（ES7）http://www.ecma-international.org/ecma-262/7.0/

ES 2017（ES8）http://www.ecma-international.org/ecma-262/8.0/

ES 2018（ES9）http://www.ecma-international.org/ecma-262/9.0/

ES 2019（ES10）http://www.ecma-international.org/ecma-262/10.0/



JS的每隔一段时间就会出新的特性，而浏览器只有不断的升级才能满足这些，而且同一个浏览器各版本对新特性的支持情况也不一样。

**浏览器与JS新特性**：https://caniuse.com/

如es6规范新增加的arrow function（箭头函数）的支持如下：

![image-20201228120303208](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20201228120303208.png)

可以看到IE所有版本完全不支持，chrome 45版本才开始支持。

想使用JS的新特性，又想兼容旧浏览器版本，那么就需要一种转换工具：把JS的新特性代码转换为旧浏览器可以支持的JS代码。而Babel就是这么一个工具。

Babel，官方介绍一个JavaScript编译器。说简单点就是把使用ES6及以上的特性的代码转换为对应的ES5代码，以使旧浏览器可以运行。

网址：https://babeljs.io/



## 1.3 应用

数据验证

读写HTML元素、动态的修改样式

与用户进行交互

网页特效

WEB游戏制作

基于Node.js技术进行服务器端编程

Javascript用途很多，我们随时学习随时积累。

 

## 1.4 ECMAScript脚本语言

Javascript，JScript，ActionScript等脚本语言都是基于ECMAScript标准实现的。

在JavaScript，JScript和ActionScript中声明变量，操作数组等语法完全一样，因为它们都是ECMAScript。但是在操作浏览器对象等方面又有各自独特的方法，这些都是各自语言的扩展。

**<u>JavaScript是由ECMAScript核心语法，DOM和BOM三者组成的。</u>**

**ECMAScript核心语法：JS语法格式、常量变量、数据类型、流程语句、函数、内置对象等**

**BOM: Browser Object Model 浏览器对象模型  封装的是操作浏览器相关的API**

**DOM: Document Object Model 文档对象模型  封装的是操作文档相关的API**





# 二、javascript基础

## 2.1 JS语法

- 每一条JS语句必须以分号结束
- 严格区分大小写  例如： a 和 A是两个完全不同的东西
- 忽略所有的换行与空格  它们存在的目的就是为了提高程序的可读性



## 2.2 JS中的注释

html 中的注释： <!-- 注释文本 -->

css 中的注释： /* 注释文本 */

js中的注释：

​	// 单行注释

​	/* 多行注释 */



## 2.3 JS的引入

- 行内方式：借助的是html中的事件属性 如：onmouseover   onmouseout  onclick等
- 嵌入script代码：借助script标签，在script标签内书写 js 代码
- 引入外部的JS代码：借助script标签，引入外部独立的 js 文件

注：script标签可以嵌入到 html 文档的任何位置；

​	    一个html文件中，可以嵌入多个script标签；

​		通过 src 属性引入外部 JS 文件的 script 标签内不能再去书写 JS 代码。

​	   

## 2.4 数据输出的方式

- alert() 警告框   效果：会向页面弹出一个弹框，必须点击确定才能继续执行代码；会有阻塞效果

- console.log()  控制台打印日志

  

# 三、常量

## 3.1 概述

常量：又称字面量，字面的意思就是你看到什么就是什么。在程序执行过程中不会发生改变。

如上面，在控制台输出的 "Hello Javascript!!" 就是一个字面量

常量分为：数值常量、字符串常量、布尔值常量等



## 3.2 数值常量

**数值：整数（10，23）、浮点数（1.34，3.14）**

生活中常见的进制数是十进制数，由 0 - 9之间的数字组成，逢十进一  如：10  20  34  56等等

程序中除了十进制外，可能还会碰到二进制、八进制、十六进制等进制数

计算机底层的运算，使用的是二进制补码的形式进行运算

二进制，由 0 和 1组成，前缀标识为 0b   如：0b1000 0111

八进制，由 0 - 7 之间的数字组成，前缀标识 0 、0o、0O  如： 0o76

十六进制，由 1 - 9，a-f 组成，a-f 代表的是 10 - 15之间的数字，前缀标识 0x  如： 0xa1f6



## 3.3 字符串常量

**双引号或单引号进行包裹的文本**  有点类似于生活中我们说的各种话  如： “Hello”  "您好"  '男'

如果想要添加一些特殊的符号，需要借助转义字符 "\\"，如下：

​		\n    换行

​		\t     制表符

​		\r     回车

​		\\"     "

​		\\'     '

​		\\\      \



## 3.4 布尔值常量

布尔值有且只有两个： true  和  false

​		

# 四、变量

## 4.1 概述

变量：用来存储信息数据的容器。在程序执行的过程中，可以发生改变。

信息数据：可以是上面讲过的常量、也可以是后面要讲的函数、数组、正则等等所有的东西。



## 4.2 变量的声明

**变量使用关键字 var 进行声明**。

语法格式  **var  变量名  = 初始化值**；

解释 将赋值运算符"="右边的初始化值 赋给 左边使用var声明的变量，那么此时这个变量在内存中开辟一个空间，存储初始化值。

举例  var str = "Hello"；   var   num = 10;

```
//第一步：使用var关键字声明一个变量, 变量名为 num
// var num;
// console.log("num:",num);//num: undefined    undefined未被定义的
// //第二步：对声明的变量进行赋值  将字面量 10 赋给变量 num
// num = 10;// = 赋值运算符  运算顺序：从右向左
// console.log("num:",num);//num: 10

//上面两步可以简写为一步
var num = 10;
console.log("num:",num);//num: 10
```



## 4.3 变量的命名规则

- 由数字、字母、下划线以及美元符号($)组成

- 数字不能开头

- 不能是JS中的关键字和保留字

- 见名知意

- 驼峰式命名：首字母小写，多个单词，从第二个单词开始首字母大写  如：getMaxNum 

- 尽可能简化命名的长度 




## 4.4 多个变量的声明方式

- 第一种：每一个都是用 var 声明，分号结束

- 第二种：如果是连续声明多个变量，可以使用使用一个var，变量之间使用逗号隔开，最后分号结束即可

  ```
   //多个变量的声明方式一
   // var a = 1;
   // var b = 2;
   // var c = 3;
  
   //多个变量的声明方式二
   var a = 10,
       b = 20,
       c = 30;
  
  console.log("a:",a,",b:",b,",c:",c);
  ```



## 4.5 变量的提升

我们可以用先使用后面声明的变量，即使变量有赋值，也是 undefined

```
// console.log(a);//报错：Error: a is not defined  在整个程序种，不管是调用前还是调用后，都不存在这个变量的声明，直接调用会报错

//先声明变量 b 并赋值 10
var b = 10;
//再调用
console.log(b);//10

//变量的提升演示
//先调用
console.log(c);//undefined  未被定义的；变量已经被声明，但是没有被赋值
//再声明变量 c 并赋值 20
var c = 20;
console.log(c);//20
```

变量提升的原因：

​	浏览器中的JS引擎，在解析JS代码时，分为两步：预解析阶段 和 运行阶段。

​	预解析阶段：会审查JS中是否有声明语句，如果有，就将其提升到当前作用域内所有JS语句的顶部 

​	运行阶段：进行赋值操作

所以上面，变量的提升演示部分代码，等价于下面的代码

```
var c;
console.log(c);//undefined
c = 20;
console.log(c);//20
```



# 五、变量数据类型

变量的数据类型分为两大类：基本数据类型 和 引用数据类型。

## 5.1 基本数据类型

Number数值类型：整数 10，20  小数 10.23  3.14      Infinity无穷大    NaN(Not a Number)不是一个数字

String字符串类型: 双引号或者单引号包裹的文本 如：var str = "Hello"; 那么变量str的数据类型就是字符串类型

Boolean布尔类型：有且只有两种值 true 和 false

Null空类型：空指针对象 它是一个特殊的对象

Undefined未被定义的：变量被声明，但是没有被赋值

## 5.2 引用数据类型

Object对象类型（所有内置对象都是这个类型，如：数字Array对象、字符串String对象、RegExp对象等）

Function函数类型



# 六、数据类型的检测

通过 typeof 关键字进行检测，检测语法如下：

typeof 变量名

typeof(变量名)

```
//数值类型
var a = 10,
    b = 3.14;
console.log("a:",a,"数据类型是：",typeof a,",b:",b,"数据类型是：",typeof(b));//a: 10 数据类型是： number ,b: 3.14 数据类型是： number

a = Infinity;
b = NaN;
console.log("a:",a,"数据类型是：",typeof a,",b:",b,"数据类型是：",typeof(b));//a: Infinity 数据类型是： number ,b: NaN 数据类型是： number
console.log("10/0=",10/0);//10/0= Infinity
console.log(10 - "hehe");//NaN

//字符串类型
a = "hello";
b = '1000';
console.log("a:",a,"数据类型是：",typeof a,",b:",b,"数据类型是：",typeof(b));//a: hello 数据类型是： string ,b: 1000 数据类型是： string

//布尔类型
a = true;
b = false;
console.log("a:",a,"数据类型是：",typeof a,",b:",b,"数据类型是：",typeof(b));//a: true 数据类型是： boolean ,b: false 数据类型是： boolean

//Null空指针类型
a = null;
//Undefined 未被定义的
b = undefined;
console.log("a:",a,"数据类型是：",typeof a,",b:",b,"数据类型是：",typeof(b));//a: null 数据类型是： object ,b: undefined 数据类型是： undefined
console.log(document.getElementById('box'));//null
var c;
console.log(c);//undefined
```



# 七、数据类型之间的转换

## 7.1 隐式转换

借助的是运算符  +  -  *  /  % 等等

运算符“+”可以是：数学的加运算、有字符串存在的情况下是字符串 拼接运算、正号

```
var a = 10,
    b = "20",
    c = 10.4;
console.log("a+b+c=",a+b+c);//a+b+c=102010.4
console.log("a+c+b=",a+c+b);//a+c+b=20.420
console.log("b+a+c=",b+a+c);//b+a+c=201010.4
console.log(a+c);//20.4
console.log(+b);//20
console.log(a-b);//-10
console.log(10-true);//9
console.log(10-false);//10
console.log(10 - "a");//NaN
console.log(10 - "");//10
console.log(10 - null);//10
console.log(10 - undefined);//NaN
```



## 7.2 显式转换

借助内置的方法或者包装类实现

内置方法：

​	parseInt()   将其他数据类型转为整数类型；数值的取整

​    parseFloat()  将其他数据类型转为浮点数类型；浮点数

​    toString()  将其它数据类型转为字符串类型

包装类：

​	Number()  将其他数据类型转为数值类型

​    String()	将其它数据类型转为字符串类型

​	Boolean()  将其它数据类型转为布尔类型

```
var a = 10,
    b = true,
    c = "hello100",
    d = "100hello";
//toString()  转字符串的方法
console.log(a.toString(),"数据类型：",typeof(a.toString()));//10 数据类型： string
console.log(b.toString(),"数据类型：",typeof(b.toString()));//true 数据类型： string

//parseInt() 转整数
console.log(parseInt(10.23));//10
console.log(parseInt(b));//NaN
console.log(parseInt(c));//NaN
console.log(parseInt(d));//100

//parseFloat() 转浮点数 用法同parseInt()

// Number() 将其它数据类型转换为数值类型
console.log(Number(b));//1
console.log(Number(c));//NaN
console.log(Number(d));//NaN
console.log(Number(false));//0
console.log(Number(''));//0
console.log(Number(null));//0
console.log(Number(undefined));//NaN
console.log(Number("100"));//100

//String() 将其它数据类型转换为字符串型

//Boolean() 将其它数据类型转换为布尔类型  布尔只有两个值 true和false
console.log(Boolean(a));//true
console.log(Boolean(1));//true
console.log(Boolean(c));//true
console.log(Boolean(d));//true

console.log(Boolean(0));//false
console.log(Boolean(''));//false
console.log(Boolean(null));//false
console.log(Boolean(undefined));//false
console.log(Boolean(NaN));//false
```



# 八、prompt

prompt()  信息提示框；提示用户在指定的输入框内输入信息

prompt(msg,ipt)  方法

​		参数  msg 设置文本提示信息，字符串类型

​				  ipt输入框中的内容，字符串类型

​		返回值  返回用户输入的数据，字符串类型

```
//声明一个变量 sex， 来接收用户输入的 性别
var sex = prompt("请输入您的性别：","女");

//声明一个变量 num， 来接收用户输入的 年龄
var num = prompt("请输入您的年龄：","16");

num = parseInt(num);
```



# 九、运算符

## 9.1 算术运算符

算术运算符用来执行数学运算。

生活中常见的算术运算符有：  +     -     *     /     %(取模，取余数)   

```
// 表达式分为运算元和运算符
//JS中算术运算符：+   -    *   /   %    ++    --
// +  除字符串类型外参与的运算，执行数学运算   true隐式转换成数字 1 进行数学运算  false和null隐式转换成 0进行数学运算
console.log(10 + 20);//30
console.log(10 + 4.6);//14.6
console.log(10 + true);//11
console.log(10 + false);//10
console.log(10 + null);//10
console.log(10 + undefined);//NaN

// +  作为正号进行运算
console.log(+10);//10
console.log(+ "10");//10   可以转换数字字符串
console.log(+ "10ab");//NaN
console.log(+ true);//1
console.log(+ false);//0
console.log(+ null);//0
console.log(+ "");// 0 空字符串转为0
console.log(+ undefined);//NaN

// +  字符串参数与的多元运算，属于字符串拼接
console.log(10 + "");// "10"  "string"
console.log(10 + "10");//"1010"
console.log("10" + 10);//"1010"
console.log("10" + true);//"10true"
console.log("10" + false);//"10false"
console.log("10" + null);//"10null"
console.log("10" + undefined);//"10undefined"
console.log("10" + NaN);//"10NaN"

//  -    *   /   %     true隐式转换成数字 1 进行数学运算  false和null隐式转换成 0进行数学运算  undefined参与的都是NaN
console.log(10 - 5);//5
console.log(0.3 - 0.1);//0.19999999999999998
console.log(10 * "10");// 100 number  除了 + 之外的其它数学运算，字符串或者其它非数值类型都会隐式转为数值类型进行运算
console.log(10 * "10abc");// NaN number
console.log(10 - "");// 10
console.log(10 - false);// 10
console.log(10 / true);// 10
console.log(10 / null);// Infinity  无穷大
console.log(10 / undefined);// NaN
console.log(10 % null);// NaN
```

"+" 运算可以作为：加法运算、正号、字符串参与的运算作为字符串拼接



上面这些运算符同样适用于程序执行数学运算，在JS中除了上面几个，还有其它算术运算符： ++(自增)   --(自增)

```
// 前++   前--
var a = 1,
    b = a;
console.log("a:",a,"b:",b);//a: 1 b: 1

--a;// --a ===> a = a - 1
++b;// ++b ===> b = b + 1
console.log("a:",a,"b:",b);//a: 0 b: 2

a = --a;
console.log("a:",a,"b:",b);//a: -1 b: 2

var c = ++b;
console.log("a:",a,"b:",b,"c:",c);//a: -1 b: 3 c:3


// 后++   后--
var i = 1,
    j = i;
console.log("i:",i,"j:",j);//i: 1 j: 1

i--;// i--  ===> i = i - 1
j++;// j++  ===> j = j + 1
console.log("i:",i,"j:",j);//i: 0 j: 2
//总结：根据实践结果，在自身操作前++和后++  前--和后--问题上，没有什么区别

//第三方变量参与时，就不同了，如下观察结果
var s = j++;// 1. 先赋值 2. 再加加
console.log("i:",i,"j:",j,"s:",s);//i: 0 j: 3  s:2

i = i--;//这种方式只有面试的时候脑残面试官才会出这样的问题
console.log("i:",i,"j:",j,"s:",s);//i: 0 j: 3  s:2
//数学中的运算顺序：先乘除后加减
//程序中的运算同样是有顺序的：如上面的算术运算符，优先级  前++、前--、正负号（+ -） >>  *  /  % >>  + - >>  赋值运算符 = >> 后++  后--
```



**练习：**使用 prompt() 方法提示用户输入两个数字，对这两个数字进行加法运算并打印求和结果。

​		   如：用户输入 10 和 20这两个数字，求和后 结果为 30



## 9.2 比较运算符

比较运算符也叫关系运算。

比较运算符比较的结果是一个布尔值。

比较运算符有： >      <       >=       <=      ==(等于)   !=(不等于)     ===(全等于)   !==(全不等于)

```
//纯数值进行比较  按照值得大小
console.log(10 > 20);//false
console.log(3.14 == Math.PI); //false

//数值和其它基本数据类型进行比较  将其它类型转为数值类型进行运算
console.log(10 > "5");//true
console.log(10 > "10ab");//false
console.log(10 < "10ab");//false
console.log(10 == "10ab");//false
console.log(1 == true);//true
console.log(0 == false);//true
console.log(0 == null);//false
console.log(1 === true);//false 数据类型不同
// “==”比较是值是否相同，忽略了数据类型       “===”比较的是值和数据类型是否完全相同

console.log(10 >= 10);//true 等价于  判断10大于10 或者 10等于10吗？

console.log(null === null);//true
console.log(undefined === undefined);//true
console.log(NaN === NaN);//false
console.log(Infinity === Infinity);//true

console.log(null == undefined);//true  ES3中，才新增undefined数据类型，这个数据类型衍生自null  所以在比较值的时候他们是相同的
console.log(null === undefined);//false   数据类型不同  null数据类型为"object"  undefined数据类型为"undefined"

//数字字符串之间的比较  按照ASCII码从左向右逐个进行比较表进行比较  ASCII码表中 0-9 对应的 ASCII值 48-57
console.log("24" > "15");//true
console.log("10" > "5");//false
console.log("234" > "25");//false
```



**练习：**使用prompt()提示用户输入两个数字，利用比较运算符比较其值大小

例如：用户输入 a = 150 和 b = 18， 那么a >= b 比较的结果是 true 



## 9.3 逻辑运算符

用来进行逻辑运算，运算符有： &     &&      |    ||     ! (逻辑非)

①逻辑与&&
将逻辑与比喻成串联电路，判断过程，想象成电流通过的过程。

![image-20201228160908860](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20201228160908860.png)
电流通过：如果a为真，电流能够通过流通到b，结果就是b；如果a为假，电流不能通过，停留在a，结果为a



②逻辑或||
将逻辑或比喻成并联电路，判断过程，想象成电流通过的过程。
![image-20201228160957966](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20201228160957966.png)

电流经过时：如果a为真，电流直接从a完成循环，结果为a；如果a为假，电流从a不能经过，流经到b，我们结果是b。



**真值表**

逻辑与 && 运算：两边都为真才是真，有一个为假则为假。

|   a   |   b   | a && b 结果 |
| :---: | :---: | :---------: |
| true  | true  |    true     |
| true  | false |    false    |
| false | true  |    false    |
| false | false |    false    |

逻辑或 || 运算：有一个为真即为真，两边都为假结果才为假

|   a   |   b   | a \|\| b 结果 |
| :---: | :---: | :-----------: |
| true  | true  |     true      |
| true  | false |     true      |
| false | true  |     true      |
| false | false |     false     |



```
//逻辑运算符：逻辑与（& &&）同时满足才满足  逻辑或(| ||)只要有一个满足即满足  逻辑非(!)
console.log(true);//true
console.log(!true);//false

console.log(10);//10
console.log(!10);//false
console.log(-10);//-10
console.log(!(-10));//false
console.log(0);//0
console.log(!0);//true
//除了0之外的所有数字，进行逻辑非操作，得结果都是 false

console.log("hello");//"hello"
console.log(!"hello");//false
console.log("");// ""
console.log(!"");//true
//非空字符串进行逻辑非操作，所得结果都是false

console.log(null);//null
console.log(!null);//true
console.log(undefined);//undefined
console.log(!undefined);//true
console.log(NaN);//NaN
console.log(!NaN);//true

// &&  和  || 具有短路效果，可以提高程序的执行效率   短路效果解释：
//逻辑与 两边同时满足才满足
//当第一个值是true的情况下，第二值决定最终结果
console.log(true &&  false);//false
console.log(true &&  true);//true
//当第一个值不成立，那么使用 && 的情况下，就不需要在进行后面的判断就能直接得出结果不满足
console.log(false &&  true);//false

//逻辑或 有一个满足即满足
//当第一个值是false的情况下，第二个值决定最终结果
console.log(false || true);//true
console.log(false || false);//false
//当第一个值条件成立，最终结果就是成立的，那么就不需要再去判断后面的结果了，这就是  || 短路效果
console.log(true || false);//true

//上面 ||  和  &&  进行运算，最终结果是 true 或 false
// 如果使用 |  和  &  进行布尔运算  最终结果是  0  或  1
console.log(true | false);//1
console.log(true & false);//0
```



所有的基本数据类型进行逻辑运算时，如何进行运算：

```
// 通过上一个案例逻辑非(!)的操作，我们总结出： 数值0、空字符串""、null、undefined、NaN、false都被当作条件不成立，在进行逻辑非操作时返回true
console.log(10 && 5);//5
console.log(10 && 0);//0

console.log(10 && "hello");//"hello"
console.log("" && "hello");//""

console.log("" || "10");// "10"
console.log("" || null);// null

console.log(undefined && null);// undefined
```



**练习**：

1. false || !false && false || true;

   ```
   	false || !false && false || true
   =   false || true && false || true
   =   false || false || true
   =   false || true
   =   true
   ```

2. 4 && "hello" || !false || !true && null;

   ```
   	4 && "hello" || !false || !true && null;
   =   4 && "hello" || true || false && null
   =   "hello" || true || false
   =   "hello" || false
   =   "hello"
   ```


补充： 逻辑运算符优先级    !  >>  && >> ||



## 9.4 赋值运算符



不同于前面运算符运算顺序从左向右，赋值运算符运算顺序是从右往左的。

如： var  num;         num = 10;    将右边的字面量10赋给左边的变量num

赋值运算符：=     +=    -=     *=      /=    %=

```
//声明一个变量num
var num;
console.log("num:",num);//num:undefined

//赋值运算符：=     +=    -=     *=      /=    %=
//对变量 num 进行赋值操作
num = 10;
console.log("num:",num);//num:10

num += 20;// 等价于  num = num + 20
console.log("num:",num);//num:30

num *= 10;//等价于  num = num * 10
console.log("num:",num);//num:300

num %= 7;//等价于  num = num % 7
console.log("num:",num);//num:6

num /= 3;//等价于  num = num / 3
console.log("num:",num);//num:2
```



## 9.5 运算符的优先级

**运算优先级：** 贴身（前++、前--、正+、负-、逻辑非!） >>> 算术运算符（先乘除后加减）  >>>  比较运算符(先>  >=  <  <= ，再 ==  ！=)>>逻辑运算符（先逻辑与&&，再逻辑或||）>>>  赋值运算符  >>> 后++、后--

**运算顺序：**除赋值运算符运算顺序从右往左，其它都是从左往右



## 9.6 三元运算符

语法：  条件表达式 ? 条件表达式成立执行的语句 : 条件表达式不成立执行的语句

示例：  

```
var a = 100,
	b = 50;
var maxNum = a > b ? a : b;
console.log("a 与 b中的最大值是：", maxNum);//a 与 b中的最大值是： 100
```

练习：提示用户输入两个任意大于0的整数，获取其中的最小值



## 9.7 运算符综合练习

1. var a = 4;
   var sum = 1 * (2 + 3) && a++ || 5 > 6 && 7 < 8 || 9;

   ```
   var a = 4;// a = 4
   var sum = 1 * (2 + 3) && a++ || 5 > 6 && 7 < 8 || 9;
   		= 1 * 5 && a++ || 5 > 6 && 7 < 8 || 9
   		= 5 && a++ || 5 > 6 && 7 < 8 || 9
   		= 5 && a++ || false && true || 9
   		= a++ || false || 9
   		= a++ || 9
   		= a++
   sum = a++; //后++存在的赋值操作，先赋值，再自增
   sum = a = 4;
   a++ <==> a + 1 = 4 + 1 = 5;
   ```

2. var a = 4;
   var  sum = 1 + 2 && 3 * a++ % 5 || 6 < 7 == 8 / !false

   ```
   var a = 4;// a = 5
   var  sum = 1 + 2 && 3 * a++ % 5 || 6 < 7 == 8 / !false
   		 = 1 + 2 && 3 * a++ % 5 || 6 < 7 == 8 / true//3*a++ =>3*a=3*4=12
   		 = 1 + 2 && 2 || 6 < 7 == 8 
   		 = 3 && 2 || 6 < 7 == 8 
   		 = 3 && 2 || true == 8
   		 = 3 && 2 || false
   		 = 2 || false
   		 = 2
   		 
   最后: a++ <==> a = a + 1 = 4 + 1 = 5
   ```

   

3. 当工作年限不满1年，工资小于8000，年终奖为工资的1倍，否则是1.2倍；
   当工作年限不满2年，工资小于10000，年终奖为工资的1.5倍，否则是1.7倍；
   当工作年限为超过2年，工资小于13000，年终奖为工资的2.3倍，否则是3倍；
   用户输入年限，工资，输出年终奖

   ```
   /**
    * 当工作年限不满1年，工资小于8000，年终奖为工资的1倍，否则是1.2倍；
    * 当工作年限不满2年，工资小于10000，年终奖为工资的1.5倍，否则是1.7倍；
    * 当工作年限为超过2年，工资小于13000，年终奖为工资的2.3倍，否则是3倍；
    * 用户输入年限，工资，输出年终奖
    */
   
   //第一步：定义两个变量来接收用户输入工作年限 和 当前薪资
   var jobYear = Number(prompt("请输入您的工作年限","2"));
   // console.log("jobYear:",jobYear,"数据类型：",typeof jobYear);
   var salary = Number(prompt("请输入您当前的薪资","10000"));
   
   //第二步：利用三元运算符，判断各种条件，给出对应的年终奖
   //判断功念年限是否满一年
   // var result = jobYear < 1 ? "工作年限不满1年" : "工作年限满1年";
   // 如果工作年限不满一年，判断工资是否小于8000
   // var result = jobYear < 1 ? (salary < 8000 ? "工资小于8000" : "工资不小于8000") : "工作年限满1年";
   // 当工作年限不满1年，工资小于8000，年终奖为工资的1倍，否则是1.2倍；
   // var result = jobYear < 1 ? (salary < 8000 ? salary * 1 : salary * 1.2) : "工作年限满1年";
   
   // 当工作年限不满2年，工资小于10000，年终奖为工资的1.5倍，否则是1.7倍；
   // var result = jobYear < 1 ? (salary < 8000 ? salary * 1 : salary * 1.2) : (jobYear < 2 ? (salary < 10000 ? salary * 1.5 : salary * 1.7) : "工资年限超过两年");
   
   //当工作年限为超过2年，工资小于13000，年终奖为工资的2.3倍，否则是3倍；
   var result = jobYear < 1 ? (salary < 8000 ? salary * 1 : salary * 1.2) : (jobYear < 2 ? (salary < 10000 ? salary * 1.5 : salary * 1.7) :
       (salary < 13000 ? salary * 2.3 : salary * 3));
   
   console.log("result:",result);
   ```

   



# 十、Math对象		 

这是JS中内置的一个对象，叫做算术对象。

Math 对象用于执行数学任务。

只要是对象，那么就具有特征与行为，体现到程序中就是属性和方法。

Math对象作为JS中的内置对象，给它内置了很多属性和方法。

Math将自己本身当作对象，可以直接调用这些属性和方法。

Math对象调用属性和方法的方式   Math.属性      Math.方法()

## 10.1 Math对象的属性

PI   获取圆周率Π=3.14...

## 10.2 Math对象的方法

random()       获取0-1之间的随机数  左闭右开[0,1)

round(num)   获取参数num的四舍五入的值

pow(x,y)   获取x的y次幂

sqrt(num)  获取参数num的开平方跟

```
//获取圆周率Π=3.14...
console.log(Math.PI);//3.141592653589793   JS中只能获取到小数点后15位

//pow(底数x，指数y)  获取x的y次方
console.log(Math.pow(2,4));//16

//sqrt(num)  获取开平方根
console.log(Math.sqrt(9));//3

//random()  获取 [0,1) 之间的随机数
console.log(Math.random());//每次结果不同

//获取 [0,10) 之间的随机数
console.log(Math.random() * 10);

//获取 [0,10) 之间的随机整数
console.log(parseInt(Math.random() * 10))

//获取 [0,10] 之间的随机整数
//round(num)  获取指定的四舍五入值
console.log(Math.round(Math.random() * 10))
```

**练习：**获取10 - 20之间的随机整数





# 十一、作业

1） 编写程序，提示用户输入圆锥的底面半径和高，然后弹出它的体积，计算圆锥体积的公式是：

体积V=1/3π半径2*高

 

2）用户输入一个三位数，弹出各个数位的和。

比如：

用户输入155，就弹出11

用户输入316，就弹出10

用户输入989，就弹出26

用户输入678，就弹出21



# 附录：ASCII码表

| ASCII值 | 控制字符 | ASCII值 | 控制字符 | ASCII值 | 控制字符 | ASCII值 | 控制字符 |
| :------ | :------- | :-----: | :------- | :------ | :------- | :------ | :------- |
| 0       | NUT      |   32    | (space)  | 64      | @        | 96      | 、       |
| 1       | SOH      |   33    | !        | 65      | A        | 97      | a        |
| 2       | STX      |   34    | "        | 66      | B        | 98      | b        |
| 3       | ETX      |   35    | #        | 67      | C        | 99      | c        |
| 4       | EOT      |   36    | $        | 68      | D        | 100     | d        |
| 5       | ENQ      |   37    | %        | 69      | E        | 101     | e        |
| 6       | ACK      |   38    | &        | 70      | F        | 102     | f        |
| 7       | BEL      |   39    | ,        | 71      | G        | 103     | g        |
| 8       | BS       |   40    | (        | 72      | H        | 104     | h        |
| 9       | HT       |   41    | )        | 73      | I        | 105     | i        |
| 10      | LF       |   42    | *        | 74      | J        | 106     | j        |
| 11      | VT       |   43    | +        | 75      | K        | 107     | k        |
| 12      | FF       |   44    | ,        | 76      | L        | 108     | l        |
| 13      | CR       |   45    | -        | 77      | M        | 109     | m        |
| 14      | SO       |   46    | .        | 78      | N        | 110     | n        |
| 15      | SI       |   47    | /        | 79      | O        | 111     | o        |
| 16      | DLE      |   48    | 0        | 80      | P        | 112     | p        |
| 17      | DCI      |   49    | 1        | 81      | Q        | 113     | q        |
| 18      | DC2      |   50    | 2        | 82      | R        | 114     | r        |
| 19      | DC3      |   51    | 3        | 83      | S        | 115     | s        |
| 20      | DC4      |   52    | 4        | 84      | T        | 116     | t        |
| 21      | NAK      |   53    | 5        | 85      | U        | 117     | u        |
| 22      | SYN      |   54    | 6        | 86      | V        | 118     | v        |
| 23      | TB       |   55    | 7        | 87      | W        | 119     | w        |
| 24      | CAN      |   56    | 8        | 88      | X        | 120     | x        |
| 25      | EM       |   57    | 9        | 89      | Y        | 121     | y        |
| 26      | SUB      |   58    | :        | 90      | Z        | 122     | z        |
| 27      | ESC      |   59    | ;        | 91      | [        | 123     | {        |
| 28      | FS       |   60    | <        | 92      | /        | 124     | \|       |
| 29      | GS       |   61    | =        | 93      | ]        | 125     | }        |
| 30      | RS       |   62    | >        | 94      | ^        | 126     | `        |
| 31      | US       |   63    | ?        | 95      | _        | 127     | DEL      |



# 十二、条件语句

条件if语句，用来指定符合条件后需要执行的语句，不符合条件不执行。

类似于选择器，选择正确的答案，必须符合题干条件。

条件语句有很多种语法格式，如下：

- **只有if关键字的条件语句**

  if(条件表达式){

  ​		当条件表达式成立的情况下才会执行的语句

  }

  案例：判断一个人的年龄是否满18岁，如果满足了，那么你可以进入网站继续观看暴力电影

  ```
  var age = parseInt(prompt("请输入您的年龄","18"));
  if(age >= 18){
      alert("可以观看...")
  }
  ```

  满足条件，执行大括号中的语句体；不满足条件，跳出if语句，继续执行if语句后面的代码。

  

- **存在 else 的if语句**

  if(条件表达式){

  ​	  当条件表达式成立的情况下才会执行的语句

  }else{

  ​		条件表达式不成立执行的语句

  }

  案例：判断一个人的年龄是否满18岁，如果满足了，那么你可以进入网站继续观看暴力电影；如果不满18岁，那么请在家长陪同下进行观看。

  ```
  var age = parseInt(prompt("请输入您的年龄","18"));
  if(age >= 18){
      alert("可以观看...")
  }else{
      alert("警告！！请在家长陪同下进行观看！！")
  }
  ```

  

  通过观察，不难发现，if...else语句 可以和 三元运算进行转换，如上代码，可以用三元表达式优化，如下：

  ```
  age >= 18 ? alert("可以观看...") : alert("警告！！请在家长陪同下进行观看！！");
  ```

  

- **if else存在的多条件判断语句**

  if(条件一){

  ​		条件一满足执行的语句体

  }else if(条件二){

  ​		不满足条件一，满足条件二执行的语句体

  }....else if(条件N){

  ​		不满足N之前的条件，满足条件N执行的语句体

  }else{

  ​		以上所有的条件都不满足执行的语句

  }

  思考？假设公司员工可以根据工龄，领取对应的福利商品：满10年的老员工，发红包2万元，购物卡1000元一张；满5年但是不满10年的老员工，发红包8000元，购物卡1000元一张；满3年但是不满5年的老员工，发红包3000元，购物卡800元一张； 满1年但是不满3年的老员工，购物卡1500元一张；不满一年的员工，购物开300元两张。

  ```
  var jobYear = Number(prompt("请输入您的工作年限","3"));
  if(jobYear >= 10){
      alert("红包2万元，购物卡1000元一张")
  }else if(jobYear >= 5){
      alert("红包8000元，购物卡1000元一张")
  }else if(jobYear >= 3){
      alert("红包3000元，购物卡800元一张")
  }else if(jobYear >= 1){
      alert("购物卡1500元一张")
  }else if(jobYear < 1 && jobYear > 0){
      alert("购物卡300元两张")
  }else{
      alert("输入有误，请重新输入！！！")
  }
  ```

  注意：if语句最终只会执行一个满足条件的大括号中的语句

  

- 省略大括号的情况

  如果if语句的大括号**只有一条**语句，那么我们就可以省略大括号。

  ```
  if(jobYear >= 10)
      alert("红包2万元，购物卡1000元一张")
  else if(jobYear >= 5)
      alert("红包8000元，购物卡1000元一张")
  else if(jobYear >= 3)
      alert("红包3000元，购物卡800元一张")
  else if(jobYear >= 1)
      alert("购物卡1500元一张")
  else if(jobYear < 1 && jobYear > 0)
      alert("购物卡300元两张")
  else
      alert("输入有误，请重新输入！！！")
  ```

  如果有两条执行语句，省略大括号的情况下，直接报错

  ```
  //如果if中有两条语句，进行省略，那么不能达到想要的结果:直接报错：Unexpected token 'else'
  var flag = true;
  if(flag)
      console.log(111);
      console.log(222);
  else
      console.log(333);
      console.log(444);
  ```

  

- **小练习**：

  1. 请用户输入一个数字，判断这个数字是否能被 3 和 7整除
  2. 请输入1-12之间的数字，判断当前月份的季节
  3. if语句嵌套练习：根据用户输入的性别和年龄，判断用户是否满足结婚年龄（男：23  女：20）

  

# 十三、选择语句

switch语句，这是一个选择语句，根据条件去匹配对应的值，匹配成功，执行这条匹配下的语句。

- **语法格式**

​		switch(表达式){

​				case  值1：

​						语句体1；

​						break;

​				case 值2:

​						语句体2；

​						break;

​				......

​				case 值N:

​						语句体N；

​						break;

​				default:

​						以上都不满足执行的语句体；

​						break;

​		}

注：default 语句可以写在 switch 中的任何位置，都是在 case 值都匹配不到的时候执行，习惯上放到最后。

​		default也可以省略，当不满足所有case时，不执行任何操作，直接跳出switch。

​		break是控制语句，打断的意思；这里用来跳出 switch 语句。也就是遇到break 语句就结束了。

需求一：请输入1-7之间的数字，判断今天是星期几

```
var day = parseInt(prompt("请输入1-7之间的整数","5"));

switch (day) {
    case 1:
        alert("今天是星期一");
        break;
    case 2:
        alert("今天是星期二");
        break;
    case 3:
        alert("今天是星期三");
        break;
    case 4:
        alert("今天是星期四");
        break;
    case 5:
        alert("今天是星期五");
        break;
    case 6:
    case 7:
        alert("今天是周末...");
        break;
    default:
        alert("输入有误，请重新输入");
        break;
}
```

需求二：请输入1-12之间的数字，判断当前月份的季节



- **变种**

  switch 中的表达式书写 true, 在 case 后面去写条件表达式。当 case 后面条件表达式成立，即执行对应的语句体，否则继续向下匹配，直到匹配成功，遇到 break 跳出。

  

需求三：根据用户输入的性别和年龄，判断用户是否满足结婚年龄（男：23  女：20）

```
 switch (true) {
    case sex == "男":
        switch (true) {
            case age >= 23:
                alert("符合结婚要求")
                break;
            default:
                alert('男性必须满足23周岁才可以结婚');
                break;
        }
        break;
    case sex == "女":
        switch (true) {
            case age >= 20:
                alert("符合结婚要求")
                break;
            default:
                alert("女性必须满足20周岁才可以结婚");
                break;
        }
        break;
}
```



# 十四、循环语句

生活见到的循环事件有：商场的电梯、传送带、拖拉机传送带、工厂中的机器、驴拉磨。

循环指的其实就是只要符合一定的条件，就会不停的执行某个动作。直到通过外力或者不符合条件后，才会结束循环。

在程序中的循环有三种：while循环、do...while循环、for循环。

## 14.1 while循环

语法格式：

​	while(条件表达式){

​			当条件表达式成立，执行此循环体

​	}



需求：循环输出 100 次 “Hello World!!”

```
//声明一个变量i， 并设置初始值 0
var i = 0;
while(i < 100){
    console.log("Hello World!!");
    //对变量进行操作
    i++;// i = i + 1
}
```



**执行顺序：**

  1. 先定义表达式需要的变量，并赋初始值 var i = 0;

  2. 判断 while 循环中的表达式 i < 100是否成立

  3. 如果表达式成立，那么执行大括号中的循环体语句

     ​		console.log("Hello World!!");

     并从循环体中，改变控制条件的变量的值  i++

  4. 重复执行第2步、第3步，直到 while 循环中的表达式 i < 100不成立，跳出循环为止



**练习：**循环输出1-100之间的所有整数（使用while循环实现）

```
var i = 1;
while(i <= 100){
    console.log("第" + i + "次打印：")
    // console.log("Hello World!");
    i++;
}
console.log('i:',i);//i: 101
```



## 14.2 do...while循环

语法格式

​	do{

​			循环体

​	}while(条件表达式)；

不难发现，do..while 和 while循环最大的区别在于：do...while不管条件是否成立，都会至少执行一次循环。



需求：实现 10 次 “Hello World!” 的控制台输出。

```
var i = 0;
do{
    console.log("Hello World!");
    i++;
}while(i < 10);
```

解析：

1. 当 i = 0 时，打印第 1 次 “Hello World!”  打印完成 i 自增变成 1

   	2. 改变后的 i = 1  去和10做对比   i = 1 < 10 成立，条件成立，继续执行循环体  打印第 2 次 “Hello World!”  打印完成 i 自增变成 2
   			3. 改变后的 i = 2  去和10做对比   i = 2 < 10 成立，条件成立，继续执行循环体  打印第 3 次 “Hello World!”  打印完成 i 自增变成 3
   	 			4. .....
   	    			5. 改变后的 i = 9  去和10做对比   i = 9 < 10 成立，条件成立，继续执行循环体  打印第 10 次 “Hello World!”  打印完成 i 自增变成10
   	       			6. 改变后的 i = 10  去和10做对比   i = 9 == 10 成立，条件不成立，跳出循环



练习：输出 1 - 100 之间，可以同时被 3  和  7 整除的整数（do...while实现）。

```
var i = 1;
do{
    // 通过条件语句判断，循环到的 i 的值是否能被 3  和  7 同时整除
    if(i % 3 == 0 && i % 7 == 0){
        console.log(i,"能被 3  和  7 同时整除");
    }
    i++;
}while(i <= 100);
console.log("i:",i);//i: 101
```



## 14.3 for循环

语法格式：

​	for(初始化变量; 条件表达式; 变量操作){

​			循环体

​	}

执行步骤：

	1. 初始化变量
	2. 判断条件表达式是否成立
	3. 条件表达式成立的情况下，执行循环体
	4. 变量的操作
	5. 继续执行第 2、3、4步，直到第 2 步中的条件表达式不成立为止，跳出循环



```
//需求：在控制台输出 10 次"Hello World"
//while循环向for循环的演变

//初始化变量
// var i = 0;
// //while循环
// while (i < 10){//条件表达式
//     console.log("Hello World!");//大括号包裹的，叫做循环语句
//     //变量操作
//     i++;
// }

//初始化变量
// var i = 0;
// //for循环
// for (;i < 10;){//条件表达式
//     console.log("Hello World!");//大括号包裹的，叫做循环语句
//     //变量操作
//     i++;
// }

//for循环
// for (var i = 0;i < 10;){//(初始化变量; 条件表达式)
//     console.log("Hello World!");//大括号包裹的，叫做循环语句
//     //变量操作
//     i++;
// }


//for循环
for (var i = 0;i < 10; i++){//(初始化变量; 条件表达式; 变量操作)
    console.log("Hello World!");//大括号包裹的，叫做循环语句
}
//到此，上面就是我们最终的for循环
```



练习：请使用 for 循环实现以下需求：

1. 循环输出1-100之间的所有整数

2. 输出 1 - 100 之间，可以同时被 3  和  7 整除的整数

3. 在页面中输出 “九九乘法表”

4. 提示用户输入一个大于0的整数，在控制台输出这个数字所有的约数

5. 输出100~999之间的水仙花数（水仙花数指的时每个数值位上的数值的立方和等于当前数字）

   如 153 = 1³ + 5³ + 3³



## 14.4 穷举思想

**概述：**我们想要得到一组数据，这些数据有特定的场景要求，计算机没有办法帮我们输出这些数据。我们需要人为的去编写一段程序，来实现这个功能：将所有可能符合要求数据，一一的列举出来，然后认为设置限制条件，将符合条件的数据筛选出来，不满足的跳过，继续验证下一个可能符合要求的数据，直到把所有可能的数据都验证一遍。这个方法就叫做穷举法，穷举法也叫全举法。

将可能符合要求的数据，使用for循环进行一一列举（遍历）;

在for循环的内部，使用if条件语句对这些可能符合条件的数据，进行一一验证，筛选出真正的符合条件的数据。

代码演示：提示用户输入一个大于0的整数，在控制台输出这个数字所有的约数

```
var num = Number(prompt("请输入一个大于 0 的整数","10"));

//按照穷举思想，先把所有可能的数据列举出来：一个数的约数，最小是1，最大是它本身
for(var i = 1; i <= num; i++){
    // console.log("i:",i);
    //按照约数的定义规则，判断是否是输出的这个数字的约数，判断条件：遍历的这个数字 i 可以整除 用户输入的数字 num
    if(num % i == 0){//取余的结果为0，即是其约数
        console.log(i,"是",num,"的约数！！");
    }
}
```



## 14.5 for循环嵌套

for循环嵌套，说白了就是 for循环 里面嵌套 for循环

在页面文档中输出数据的方式： document.write("内容");



代码演示：在页面中输出 “九九乘法表”

```
<style>
    table{
        border-collapse:collapse;
    }

    td{
        padding: 4px 8px;
        border: solid 1px;
    }
</style>
<script>
    //向页面输出内容：可以是标签也可以是文本
    // document.write("<h2>Hello World!!</h2>");

    //页面上打印 九九乘法表
    // for (var i = 1; i <= 9; i++) {//外层循环控制行
    //     for (var j = 1; j <= i ; j++) {//内层循环控制列  此时内层循环作为外层循环的循环体存在
    //         document.write(j + "&times;" + i + "=" + (i * j) + "&nbsp;&nbsp;");
    //     }
    //     //上面内层循环执行完毕后，也就相当于这一行的结束，此时在这一行后面加换行符
    //     document.write("<br>")
    // }

    //加表格
    document.write("<table>")
    for (var i = 1; i <= 9; i++) {//外层循环控制行
        document.write("<tr>")
        for (var j = 1; j <= i ; j++) {//内层循环控制列  此时内层循环作为外层循环的循环体存在
            document.write("<td>")
            document.write(j + "&times;" + i + "=" + (i * j));
            document.write("</td>")
        }
        document.write("</tr>")
    }
    document.write("</table>")
</script>
```



## 14.6 综合小练习

输出100~999之间的水仙花数（水仙花数指的时每个数值位上的数值的立方和等于当前数字）

如 153 = 1³ + 5³ + 3³

```
// 穷举思想第一步：--列举出所有可能的值
for (var i = 100; i < 1000; i++) {
    // console.log("i:",i);

    //声明三个变量：接收百位数字的 b  接收十位数字的 s   接收个位数字的 g
    var b = parseInt(i / 100);
    // console.log("b:",b)
    var s = parseInt(i % 100 / 10);
    // console.log("s:",s);
    var g = parseInt(i % 10);
    // console.log("g:",g);

    //穷举思想第二步：通过设置条件，从可能的值中筛选出确定符合条件的值
    if(Math.pow(b,3) + Math.pow(s,3) + Math.pow(g,3) == i){
        console.log(i,"是水仙花数！！")
    }
}
```



## 14.7 累加法

求：1 + 2 + 3 + 4 + 5 + ... + 99 + 100  的和

```
//累加需要将每一次遍历到的数值都加到之前遍历的数字之和上，并保留最新改变后的和
//所以这里，声明一个变量，来保存每一次累加后的和
var sum = 0;
// 获取 1- 100之间所有的数字
for (var i = 1; i <= 100; i++) {
    // console.log("i:",i);
    sum += i;// 等价于 sum = sum + i
}
//循环完成，将累加的结果输出
console.log("sum:",sum);
```



## 14.8 累乘法

求：1 * 2 * 3 * 4 * 5 * ... * 99 * 100 的积

要求大家自己实现，并在作业中提交。





# 十五、控制语句

一般情况下，我们在执行循环时，只要是满足循环条件，那么循环体就会一直执行下去。

这个时候，我们想要在循环时，达到某种条件时，控制循环的执行，那么就用到控制语句。

控制语句有两个：break  和 continue

- break  打断、中断。在JS中，可以应用于 switch 语句、循环语句（常见于 for 循环），用来跳出语句或者说是结束语句的执行

  需求：遍历1-10之间的数字，当数字是6的时候，跳出循环；打印结果：1，2，3，4，5

  ```
  for (var i = 1; i <= 10; i++) {
      if(i == 6){
          break;
      }
      console.log("i:",i);
  }
  console.log("循环执行完毕i:",i);
  ```

  控制台效果：

  

- continue 继续。在JS中，一般应用于循环语句中，用来跳过本次循环继续下一个循环

  需求：遍历1-10之间的数字，当数字是6的时候，跳过本次循环继续下一次循环；打印结果：1，2，3，4，5，7，8，9，10

  ```
  for (var j = 1; j <= 10; j++) {
      if(j == 6){
          continue;//跳过本次循环继续下一次循环
      }
      console.log("j:",j);
  }
  console.log("循环执行完毕j:",j);
  ```

  控制台输出效果：

  

- 多层嵌套循环下，跳出或跳过指定循环

  ```
  outter:for (var i = 1; i <= 5; i++) {
      inner:for (var j = 1; j <= 5 ; j++) {
          if(j == 3){
              // break;//跳出当前循环，当前循环为内层循环
              // continue;//跳过本次循环，继续下一次条件循环
  
              // break outter;//跳出指定标记的那一层循环
              continue outter;
          }
          console.log("i:",i,"j:",j);
      }
  }
  ```

  控制台效果：

  



# 十六、作业

1. 推导循环执行的顺序，用文字进行说明，并推导出可能的结果。

   for(var m = 1,n = 2; m + n < 18; m++){

   ​	n += 3;

   ​	console.log(m);

    }

2. 大家都玩儿过的一个的游戏：

   游戏玩儿法就是，大家轮流报数，如果报到能被7整除的数字，或者尾数是7的数字，都算踩地雷了。就应该罚唱歌。

   请在控制台输出1~60之间的所有“安全数”。

   比如：

   1、2、3、4、5、6、8、9、10、11、12、13、15、16、18、19、20、22、23、24、25、26、29、30……

3. 一个 4 位整数，求将该数反转以后的值。如：1234 反转后 4321

4. 如果某年的年份时4的倍数并且不是100的倍数，或者该年份是400的倍数，那么这一年是闰年。

5. 有一个不多于5位的正整数，求它是几位数，并分别打印出每一位数字。





# 十七、函数的声明与调用

## 17.1 函数概述

函数可以封装一些功能，可以供外部去重复的调用。所以，一般我们把函数叫做具有重复功能的代码块。

假设饭店就是一个函数，饭店的功能就是做各种各样的菜，但是具体做什么菜，需要用户来点，用户可以是我们当中的任何一个人，当我们点好菜付完帐，那么饭店就行驶它做饭的功能，开始为我们做指定的可口饭菜，这个我们点餐的过程，其实就是类似于函数调用的过程。最后，饭店做完菜给我们呈上来，这个菜就类似于函数返回的数据

## 17.2 函数的声明

函数使用关键字 function 来进行声明

在声明的函数内部，我们可以书写一些代码，使这个函数具有某一种特定的功能。在函数内部书写的代码我们习惯上称为函数体。

函数声明的语法格式：

```
function 函数名(形式参数){
	函数体
}
```

```
//思考：求任意两个数的和
// var a = 10,
//     b = 20;
// console.log(a+b);//30
//
// var i = 100,
//     j = 200;
// console.log(i + j);//300

//假设：还有很多数字，那么我们都要去执行求和操作，那样需要声明好多变量，且功能（求和操作）重复的，这个时候我们就可以借助函数来进行优化
//函数是具有重复功能的代码块
function sum(num1,num2){
    //return 返回的意思  这里用来返回数据
    return num1 + num2;
}

console.log(sum(10,20));
console.log(sum(100,200));
```

函数名的命名规则：同变量命名规则



## 17.3 函数的调用

函数声明后，不会自动执行，需要进行调用

函数调用的语法  函数名()

函数的调用方式

- 直接在 JS 脚本的任何为止进行调用  函数名()
- 事件驱动  <marquee onmouseover='this.stop();'></marquee>



练习：使用函数包装流程语句，也就是将流程语句当作函数体。一个大于0的整数，打印它的所有约数。

分析：一个数它的最小约数是1，最大约数是它本身。如果还有其它约数，肯定在 1 和 它本身之间。

什么是约数？

约数，又称因数。整数a除以整数b(b≠0) 除得的商正好是整数而没有余数，我们就说a能被b整除，或b能整除a。a称为b的倍数，b称为a的约数。

```
//提示用户输入一个大于0的整数
var num = parseInt(prompt("请输入一个大于0的整数","20"));

//不使用函数
// for(var i = 1; i <= num; i++){//使用for循环一一列举可能的值
//     if(num % i === 0){//通过if指定约数条件
//         console.log(i + "是20的约数！！")
//     }
// }
// console.log(i)

//函数封装
getYS(num);
function getYS(n){
    for(var i = 1; i <= n; i++){//使用for循环一一列举可能的值
        if(n % i === 0){//通过if指定约数条件
            console.log(i + "是20的约数！！")
        }
    }
}
// console.log(i);//i is not defined
```

使用函数封装，简单介绍几个好处：

​	避免全局变量的污染；

​	节约内存；

​	提高程序的执行效果；

​	减少重复代码的书写；

​	便于后期维护；

​	可以返回数据进行二次操作；

​	等等....



## 17.4 函数的类型

```
function f(){}
console.log(typeof f);//function
```



# 十八、函数的参数

## 18.1 函数参数概念

参数可以类似的看作我们之前声明的变量，只不过它的位置在函数后面的小括号中，且不需要再使用var进行声明。函数的参数分为两种：形式参数 和 实际参数。

**形式参数：**简称形参。在函数声明的时候，小括号中给定的参数，此时，不能确定参数的数据类型 和 具体的值。类似于前面讲的去饭店服务员给我们的菜单，可以提供给这么多菜，但是具体做什么菜还需要客户指定。

**实际参数：**简称实参。在函数调用的时候，用来替换形参的具体的值（传递的参数），此时确定了数据类型和值。

类似于前面讲的去饭店点菜，根据服务员提供的菜单，点具体的菜名

**传参：**函数调用，有一个传递参数的过程，这个过程我们叫它传参。



需求：求一个大于0的整数，约数的个数

代码演示：

```

```

通过上面的描述和演示，总结出JS的另外一个特点：

​	**JS是一门动态的、弱类型语言。**



## 18.2 函数的重载

重载可以看作是函数参数的应用。

函数的重载：在一个程序中，声明多个同名函数，但是其数据类型以及参数的个数并不相同。

JS中不存在函数重载的概念，我们只能模拟。因为一旦在JS中声明多个同名函数，后面的会覆盖前面的。

```
//求两个数字的和
function sum(a,b){
    return a+b;
}

//求三个数字的和
function sum(a,b,c){
    console.log("a:",a,"b:",b,"c:",c);
    console.log(arguments);
    return a+b+c;
}

//函数调用
console.log(sum(10,20));//NaN  a: 10 b: 20 c: undefined
console.log(sum(10,20,30));//60  a: 10 b: 20 c: 30
console.log(sum(10,20,30,40));//60  a: 10 b: 20 c: 30 直接匹配对应参数的个数，多余的砍掉
// JS中不存在函数重载的概念，我们只能模拟。因为一旦在JS中声明多个同名函数，后面的会覆盖前面的。
/**
 * 总结：
 *      实参的数量少于形参，结果肯定是 NaN
 *      实参的数量多余形参，结果是取匹配形参数量的实参，去执行得到响应的结果，砍掉多余的参数
 */

//但是，我们可以通过 arguments 对象实现重载的模拟
```



## 18.3 arguments对象

arguments对象是JS中一个特殊的对象。它是一个类数组，存储的是函数调用时所有传递的实际参数。

arguments对象中内置了一个 length 属性，用来获取函数调用时实际传递的参数的个数  语法 arguments.length

类数组和数组都具有索引，索引从0开始，依次递增，如上图：arguments对象中，有对应的索引，一一对应于传递的参数。通过 **arguments[索引]**  可以获取执行的对应的参数值：

​		获取第一个参数  arguments[0]

​		获取最后一个参数  arguments[arguments.length - 1]

```
function sum() {
    console.log("arguments:",arguments);
    console.log("函数调用时传递的第一个参数：",arguments[0]);
    console.log("函数调用时传递的参数个数：",arguments.length);
    console.log("函数调用时传递的最后一个参数：",arguments[arguments.length - 1]);
}
```



模拟函数的重载，这个地方做一个求和操作：

```
function sum() {
    //声明一个变量，来存储每次累加的结果
    var result = 0;

    //遍历 arguments 对象的索引
    for (var i = 0; i < arguments.length; i++) {  //此时的 i 对应于 arguments 对象中的索引
        result += arguments[i];
    }

    //将求取的和返回
    return result;
}
```



# 十九、函数的返回值

很多情况下，我们封装函数的目的是为了利用函数的这个功能，得到某些数据，然后对这些数据进行二次操作。

那么，如果想要在函数中返回这些数据，那么需要用到关键字 return。

return 关键字用于在函数中返回数据，并跳出函数。

如果仅仅是为了跳出函数，而不需要返回任何数据，那么直接return即可。



**练习：**判断一个大于0的数字是否是质数。

什么是质数？

​	质数也叫素数，是指在大于1的自然数中，除了1和它本身以外不再有其他因数的自然数。

分析：可以根据约数的个数，当约数的个数是2的时候，那么这个数就是质数。

```
/*
练习：判断一个大于0的数字是否是质数。
什么是质数？
    质数也叫素数，是指在大于1的自然数中，除了1和它本身以外不再有其他因数的自然数。
分析：可以根据约数的个数，当约数的个数是2的时候，那么这个数就是质数。
*/

//封装一个函数，判断一个数字是否是质数
// function isZH(num){
//     var count = 0;
//     for(var i = 1; i <= num; i++){
//         if(num % i === 0){
//             count++;
//         }
//     }
//
//     //判断 count 的数量
//     if(count === 2){
//         return num + "是质数";
//     }else{
//         return num + "不是质数";
//     }
// }


//改造，使函数具有单一独立的功能
//封装一个函数，获取一个数约数的个数
function YSCount(num){
    var count = 0;
    for(var i = 1; i <= num; i++){
        if(num % i === 0){
            count++;
        }
    }
    //返回约数的个数
    return count;
}


//封装一个函数，判断一个数字是否是质数
function isZH(num){
    //判断 count 的数量
    if(YSCount(num) === 2){
        return num + "是质数";
    }else{
        return num + "不是质数";
    }
}

//上面单一功能模块函数，其实就是咱们后面要讲的模块化变成：功能尽量单一、降低耦合性、提高代码的可复用性
```



return作为跳出函数用。

一般会在面试中经常被问道，return、break、continue的区别？

```
 function fn(){
    for (var i = 1; i <= 5; i++) {
        if(i == 3){
            // continue;//跳过本次循环继续下一次循环
            // break;//跳出当前循环
            return;//跳出函数用
        }
        console.log(i);
    }

    console.log("循环外，函数中...")
}
fn();
```



# 二十、函数的作用域

## 20.1 作用域概述

**概述：**当声明函数后，在函数的内部（大括号函数体位置）形成自己一个独立的内部区域，这个内部区域就叫做函数作用域。

函数作用域相对于整个脚本区域来讲，只是一个很小的独立区域，这个很小的区域我们通常叫它局部作用域。而整个脚本区域，我们通常叫它全局作用域。

**全局作用域**：函数外的区域叫做全局作用域；在全局作用域中声明的变量，可以在脚本的任何位置(包裹函数内)都可以对其进行调用，这个变量我们称为**全局变量**。全局变量的生命周期：从文件被执行时创建（当前就是页面被加载），页面关闭后销毁。

**局部作用域**：函数内的区域叫做局部作用域；在局部作用域中声明的变量，只能在函数的内部进行访问调用，那么此时我们称其为**局部变量**。局部变量的生命周期：函数被调用时创建，函数调用完毕销毁。

```
//全局变量：可以在页面的任何位置被调用
var num = 10;
console.log("num:",num);//num: 10
fn();//声明的函数只有被调用，才会执行
function fn(){
    console.log("num:",num);//num: 10
}

//局部变量：只能在当前作用域内被调用
fn2();
function fn2(){
    var n = 100;
    console.log("n:",n);//n: 100
}
// console.log("n:",n);//Error: n is not defined
fn3();
function fn3() {
    console.log("n:",n);//Error: n is not defined
}
```



## 20.2 作用域链问题：

**嵌套函数**中，存在多个**被声明**的同名函数，在调用时，首先查看当前作用域是否有这个变量，有则调用，没有则去它的上一级作用域中查找，如果有则使用，如果没有，继续向上查找，直到找到为止

```
//声明一个全局变量 num
var num = 1;
function fn() {
    //在第一层函数中，声明一个变量 num
    var num = 10;
    //在第一层函数中，声明一个内部函数 fn2
    //创建函数的另外一个方式  将声明的匿名函数赋值给一个变量
    var fn2 = function () {
        var num = 100;
        return num;
    }
    return fn2;
}
```



## 20.3 局部作用域内不使用var声明的变量

如果在函数的内部，不使用var声明，首先这是不标准的写法，一般不建议，且在严格摸下会报错。其次，如果我们不小心这样用了，那么在函数被调用后，这个变量会提升为全局变量。如果函数没有被调用，则不会创建这个变量。

```
function f() {
    num = 10;
    console.log("num:",num);
}
```



这种情况，很容器造成全局变量的污染，不建议使用。

```
var i = 2;
console.log('i:',i);//i: 2
function f1() {
    var i = 20;
    console.log('i:',i);//i: 20
}
f1();
console.log('i:',i);//i: 2

var j = 3;
console.log("j:",j);//j:3
function f2() {
    j = 30;
    console.log("j:",j);//j:30
}
f2();
console.log("j:",j);//j:30
```

上面的 j 本身是想作为一个局部变量来处理，但是由于没有使用 var 声明，造成函数调用时，这个本要作为局部变量定义的变量 变成了 全局变量的赋值操作，这样就造成了全局变量的污染，或称为命名冲突。



## 20.4 同一个变量多次声明

如果在同一个作用域内，一个变量被多次声明，那么声明只会生效一次，以第一次声明为准，后面的声明不再作数，直接作为变量的赋值操作。

```
var num = 1;
console.log("num:",num);//num:1

var num = 10;
console.log("num:",num);//num:10

num = 100;
console.log("num:",num);//num:100
```



# 二十一、函数的提升

在 JS 中，有变量和函数的提升，JS引擎在解析代码时，分成两步：

1. 预解析阶段：将所有变量 和 函数的声明，提升到当前作用域的最顶部
2. 运行阶段：进行变量的赋值操作

在JS中，函数的创建方式有三种：

- 第一种标准的方式  function 函数名(参数列表){函数体}

  ```
  function f() {
      num = 10;
      return "num:"+num;
  }
  ```

- 第二种函数表达式的方式：将一个匿名函数赋值给一个变量  var f = function(参数列表){函数体}

  ```
  var f1 = function(){
      num = 10;
      return "num:"+num;
  }
  ```

- 第三种内置对象的方式 var f = new Function("参数列表"，“函数体”)

  ```
  var f3 = new Function("num = 10; return 'num:'+num");
  
  var f2 = new Function("a","b","return a+b");
  ```




使用标准的方式创建的函数，与其它两种方式在调用时的不同：

1. 如果都是先声明，再去调用，看不出有什么区别：上面已经验证过 f()  f1()  f3() 结果一致

2. 如果时先调用，再去声明的情况，那么结果就不同了，如下代码

   **非标准的方式**，利用的是一个变量来接收一个函数，那么其本质就是变量。前面讲过变量的提升，相当于将变量的声明提升到当前作用域的最顶部，这时还没有赋值，在调用的时候，变量的值是undefined。所以后面两种创建函数的方式，只能先声明再调用。

   **标准的方式：**会将整体作为一个声明部分，再预解析阶段，将其整体提升到当前作用域的最顶部，所以标准的方式创建的函数可以在当前作用域的任何为止被调用。

```
// 第一种标准的方式  function 函数名(参数列表){函数体}
console.log("f():",f());//f(): num:10
function f() {
    num = 10;
    return "num:"+num;
}
console.log("f():",f());//f(): num:10

//第二种函数表达式的方式：将一个匿名函数赋值给一个变量  var f = function(参数列表){函数体}
console.log("f1:",f1);//f1: undefined
// console.log("f1():",f1());//Error: f1 is not a function
var f1 = function(){
    num = 10;
    return "num:"+num;
}
console.log("f1():",f1());//f1(): num:10
```



**小问题**：如果在同一个文件中，存在同名的变量 和 函数，函数优先于变量提升；而前面讲到，在一个文件中，声明多个变量，只有第一个会生效，而函数也可以看作是变量，不管使用var还是使用function都叫做声明。所以函数优先于变量提升后，其它变量的声明都变成了赋值操作。

```
//变量和函数冲突：函数优先于变量提升
console.log("f:",f);
var f = 1;
console.log("f:",f);

function f() {
    console.log("f:",f);
}
f();

//等价于
// function f() {
//     console.log("f:",f);
// }
// console.log("f:",f);
// var f = 1;
// console.log("f:",f);
// f();
```





# 二十二、模块化编程

假设有一个酒店：酒店中有保安负责安保、前台负责接待、服务生负责提供服务、厨师负责做饭、大堂经理负责协调等等。

这时，如果将安保、前台、服务生、厨师、协调等工作全部交给大堂经理一个人去做，这样效率会很慢，酒店几乎没有多久肯定会倒闭。此时，酒店提供所有的功能都在大堂经理一个人身上，肯定是不行。

这时，酒店考虑到经营问题，又招来了保安、前台等等人，负责其自己相应的领域工作，然后大堂经理只需要调配这些人即可。这样效果就会很高了。

那么，代码中也是一样，尽可能的减少代码的耦合性。我们可以利用函数，将功能封装的尽量单一，在不同的场景下，可以被重复的利用，优化了代码又提高了执行的效果。这些，其实就是模块化的思想。

后面随着课程的深入，我们会接触到 seajs、requirejs、nodejs 这些东西，都是用来进行模块化开发的，不同之处在于其将一个js文件作为一个模块，可以避免全局变量的污染。

这里，我们使用函数来体会模块化编程的思想。

人类从古至今，习惯将事情分工，将一些内容做成一些公共模块，模块可以重复反复使用。
模块化编程：将一些基础的公共的部分单独封装到一个函数内，可以多次被调用。

**案例：**输出100以内的质数，模块化编程。
	逆向思维的过程：输出100以内的质数  →  判断是不是质数   →  找约数个数

```
//声明一个函数,来输出指定大于0的整数以内所有的质数
getAllZS(100);
function getAllZS(num) {
    for (var i = 1; i <= num; i++) {//一一列举可能的值
        if(isZS(i)){//判断可能值是不是质数
            console.log(i + "是质数!!");
        }
    }
}

//声明一个函数,判断一个数是不是质数
function isZS(num) {
    //如果约数的个数是 2,也就是只有 1 和 本身两个约数的情况  那么这个数就是质数
    if(getYSCount(num) === 2)
        return true;
    else
        return false;
}

//声明一个函数,获取一个数约数的个数
function getYSCount(num) {
    var count = 0;
    for(var i = 1; i <= num; i++){
        if(num % i === 0){
            count++;
        }
    }
    return count;
}
```

**练习**：找100以内的完美数：（一个数的约数除了它本身外其他约数和还等于这个数）。
	注意：模块化编程，可以让我们的程序更加优化，各个小模块要尽量功能单一，提高重复使用率。

**练习：**赢数是一种特殊的自然数，除去它本身以外所有的约数和大于其本身。请输出100以内所有的赢数

**练习**：如果整数 A 的全部约数（包括1，不包括 A 本身）之和等于 B，且 整数 B 的全部约数（包括1，不包括B 本身）之和等于 A，则称整数 A 和 B是一对亲密数。输出1000以内的亲密数。



# 作业

1. 封装一个函数，实现功能：不借助临时变量，进行两个整数的交换。

   提示：运算符、函数有两个参数

2. 封装一个函数，求3个数中的最大值

   提示：函数有三个参数、要求至少使用两种方式实现

3. 封装一个函数，实现在页面上输出 100 ~ 1000之间所有的质数，并要求每行显示 6 个数字

4. 封装一个函数，实现 12! - 10! 结果

   要求：不能使用递归



# 二十三、数据类型在内存中的位置

数据类型有两大类：基本数据类型 和 引用数据类型

- 基本数据类型：Number数值类型  string字符串类型  Boolean布尔类型  Null空类型 Undefined未被定义的
- 引用数据类型：Object对象类型、Function函数类型

基本数据类型存储在内存的栈中，引用数据类型存储在堆中

内存分区如下：

​	***画图演示***

代码演示：

```
 var a = 10,
    b = 20,
    c = 30,
    fn = function () {};

console.log("a:",a,"b:",b,"c:",c,"fn:",fn);//a: 10 b: 20 c: 30 fn: ƒ () {}

//修改b的值
b = 200;
console.log("a:",a,"b:",b,"c:",c,"fn:",fn);//a: 10 b: 200 c: 30 fn: ƒ () {}

//声明一个变量d来接收基本数据类型的变量c
 var d = c;
 console.log("c:",c,"d:",d);//c: 30 d: 30

 //改变基本数据类型c的值
 c = 300;
 console.log("c:",c,"d:",d);//c: 300 d: 30
//总结：基本数据类型变量在进行赋值时，只是将变量保存的值复制了一份给另外一个变量进行赋值。此时变量值得改变不会互相影响。

//声明一个变量，来接收引用数据类型得变量
var fn2 = fn;
console.log("fn:",fn,"fn2:",fn2);//fn: ƒ () {} fn2: ƒ () {}
console.log(fn === fn2);//true 指向同一个内存地址

//改变其中一个引用数据类型的结构
fn.x = 100;
console.log("fn:",fn,"fn2:",fn2);//fn: ƒ () {} fn2: ƒ () {}
console.log(fn === fn2);//true 指向同一个内存地址
console.log("fn.x:",fn.x,"fn2.x:",fn2.x);//fn.x: 100 fn2.x: 100
//总结：引用数据类型变量在进行赋值时，将引用数据类型的变量保存的地址复制了一份给另外一个变量复制。此时两个变量指向同一个地址，其中一个结构发生改变会影响另外一个
```



# 二十四、递归函数

递归就是在函数的内部调用函数自己本身；

递归函数多用来解决一些 **数字0以上** 的数学问题；

递归函数必须给定一个条件，来退出函数，否则会造成内存堆栈溢出的问题。

如：

​	累加问题 1 + 2 + 3 + ... + 98 + 99 + 100

​	累乘问题 100! = 100 * 99 * 98 * ... * 3 * 2 * 1

​	生兔子的问题 有一对兔子，三个月开始每个月生一对小兔子，这一对小兔子在成长到三个月的时候，每个月也是生一对小兔子，问一年之后，在没有死亡的情况下，总共有多少对兔子？

​	换算成数学，就是一个斐波那契数列  1  1  2  3  5  8  13  21  34  55 89  144...

```
// 斐波那契数列  1  1  2  3  5  8  13  21  34  55 89  144...
console.log(feiBo(1));
console.log(feiBo(2));

console.log(feiBo(11));
console.log(feiBo(12));
// 求斐波那契数列中第 N 项的值
function feiBo(n) {
    if(n === 1 || n === 2){
        return 1;
    }
    return feiBo(n - 1) + feiBo(n - 2);
}

//feiBo(3) =  feiBo(3 - 1) + feiBo(3 - 2) = feiBo(2) + feiBo(1) = 1 + 1 = 2
//feiBo(4) =  feiBo(4 - 1) + feiBo(4 - 2) = feiBo(3) + feiBo(2) =  feiBo(3 - 1) + feiBo(3 - 2) + 1 = 1 + 1 + 1 = 3
//feiBo(5) = ....
```





# 二十五、匿名函数和自执行函数

匿名函数：也叫拉姆达函数，说白了就是没有名字的函数

自执行函数：IIFE，也叫立即执行函数。不需要进行调用，随着程序的执行会自动调用。IIFE有两部分组成，函数体和执行部分。

```
//匿名函数的使用
//1. 声明一个变量，来接收一个匿名函数
var f = function () {

};

//事件驱动  window窗口对象的点击事件
var count = 0;
window.onclick = function () {
    console.log("第" + (++count) +"次点击了窗口...")
};

//IIFE自执行函数
;(function (a,b) {
    console.log(a + b);
})(10,20);

var result = (function (a,b) {
    return a + b;
})(10,20);
console.log("result:",result);
```



# 二十六、闭包函数

什么是闭包？

闭包就是一个函数可以访问另外一个函数内部的变量。

想要理解闭包，需要先了解 作用域链的问题 和 垃圾回收机制的问题（设置到变量的生命周期）。

在JS中，任何一个函数都可以认为是闭包；常见的情况是，函数中可以访问全局变量，嵌套函数可以访问祖先元素中的变量。

```
function f(){
    var i = 1;
    function f2(){
        console.log(i);
    }
    return f2;
}

//f函数中的 变量i 是一个局部变量，局部变量只能在函数的内部被访问到
function f3(){
    console.log(i);
}
```

如果想要在一个函数的外部，访问这个函数内部的变量，那么该怎么操作？

假设，我们将嵌套在内部的函数作为一个联通内外的桥梁，在调用外层函数时，返回这个内部的函数

```
function f() {
    var i = 1;
    return function () {
        return i++;
    }
}

console.log(f);
console.log(f());
console.log(f()());//1
console.log(f()());//1
//也就证明，每一次都是一个全新的环境，得到的值也是一样的  局部变量和函数在外部函数调用完毕后即销毁

//那么，利用对象之间的引用关系，可以保存当时执行的一个环境，进而将局部的变量保存下来
//垃圾回收机制中：对存在引用关系的对象 不会进行回收
var test = f();//此时test就是一个函数
console.log(test)
console.log(test());//1
console.log(test());//2
console.log(test());//3

var test2 = f();//此时又是一个新的闭包函数  当执行f()时，传递给test2的那个桥梁函数会记住当时所执行的上下文环境
console.log(test2);
console.log(test2());//1
console.log(test2());//2
```



闭包的问题：

闭包不宜使用过多，容易造成内存的泄漏问题；

但是，使用闭包可以避免全局变量的污染，很多高级程序中，都会有闭包的应用。后面在高级课，会利用闭包来私有化对象的属性和方法。

闭包目前可以用来解决：

​	循环中，有异步语句存在的情况下，无法正确获取索引的问题。

```
// console.log(1111);
//回调函数：将一个函数作为另外一个函数的参数
//在JS中，有一个内置的延迟器，在指定时间后，去执行相应的操作
// setTimeout(function () {
//     console.log(2222);
// })
// console.log(3333);


//循环中，异步语句，获取索引的问题
// for (var i = 0; i < 10; i++) {
//     console.log("i:",i);
// }

for (var i = 0; i < 10; i++) {
    (function (j) {
        setTimeout(function () {
            console.log("内j:",j);
        })
    })(i);
}
console.log("外i:",i);
```



# 二十七、数组对象

数组对象是JS中的一个内置对象，其内置了很多方法和属性供我们使用。

想要理解数组对象，先要理解什么是数组？

前面讲过变量，变量是用来存储信息的容器，但是一个变量只能存储一条信息。而数组呢，可以看作是存储多条信息的容器，其存储的数据可以是我们学过的任意数据类型。

数组由中括号进行包裹，存储的数据之间使用逗号隔开。如：

```
var arr = [10,"hello",true,null,undefined,Math.random(),function(){},new Object()]
```

数组是一系列数据的集合，所以数据是有长度的，通过 length 属性可以获取数组中元素的个数。

数组具有索引，索引从 0 开始，依次递增，最大的索引值  arr.length - 1。

通过索引可以获取其在数组中对应的值，如：

​	数组中的第一个值  arr[0]

​	数组中的最后一个值 arr[arr.length - 1]

通过指定索引不仅可以获取值，还可以用来对值进行修改操作。

### 27.1 数组对象的创建方式

- 字面量的方式   var arr = [10,20,30,40,50,60]

```
 var arr = [10,20,30,40,50,60];
console.log("arr:",arr);

//通过索引获取值
console.log("数组arr中第一个元素是：",arr[0]);
console.log("数组中元素的个数：",arr.length);
console.log("数组arr中最后一个元素是：",arr[arr.length - 1]);

//通过索引修改值
arr[2] = 300;
console.log("arr:",arr);

//通过索引添加值
arr[6] = 70;
console.log("arr:",arr);
```



- 通过new关键字  var arr = new Array();
  - 如果 new Array(arg) 中的参数 arg 只是一个数值类型的整数，那么代表的是数组的长度
  - 如果上面参数 arg 是其它数据类型，或者是多个参数，那么代表的是数组中的元素

```
var array = new Array();
console.log("array:",array);//array: []  这是一个空数组

array = new Array(10);
console.log("array:",array);//array: (10) [empty × 10]  这是一个长度未10的数组，但是数组中没有值
// 通过索引添加值
array[0] = 100;
array[1] = 200;
array[8] = 900;
array[9] = 1000;
array[14] = 14000;
console.log("array:",array);//array: (10) [100, 200, empty × 6, 900, 1000]

array = new Array("10");
console.log("array:",array);//array: ["10"]

// array = new Array(3.14);
// console.log("array:",array);//RangeError: Invalid array length

array = new Array(10,20);
console.log("array:",array);//array: (2) [10, 20]
```



### 27.2 数组中的属性

length 属性用于获取数组中元素的个数

constructor 获取数组对象的构造函数

```
var arr = [10,20,30,40];
console.log("arr:",arr,"数据类型：",typeof arr);//arr: (4) [10, 20, 30, 40] 数据类型： object

//length 获取数组中元素的个数
console.log("数组中元素的个数：",arr.length);//数组中元素的个数： 4

//construtor 获取指定对象构造函数
console.log("数组的构造函数：",arr.constructor);//数组的构造函数： ƒ Array() { [native code] }

//构造函数和普通函数，最明显的区别就是构造函数的首字母大写
```



### 27.3 数组中的方法

1. 数组转字符串的方法

   toString()   将数组对象转换成字符串对象

   ​		这个方法没有参数

   ​		返回值是一个字符串

   join(seperator?)    将数组对象按照指定的分隔符转换成字符串对象

   ​		参数 seperator 可选参数。指定分隔符号，是一个字符串类型

   ​		返回值是一个字符串

   ```
   var arr = [10,20,30,40,50,60];
   console.log("arr:",arr,"数据类型：",typeof arr);//arr: (6) [10, 20, 30, 40, 50, 60] 数据类型： object
   
   // toString()   将数组对象转换成字符串对象
   var str = arr.toString();
   console.log("str:",str,"数据类型：",typeof str);//str: 10,20,30,40,50,60 数据类型： string
   
   // join(seperator?)    将数组对象按照指定的分隔符转换成字符串对象
   var str2 = arr.join();
   console.log("str2:",str2,"数据类型：",typeof str2);//str2: 10,20,30,40,50,60 数据类型： string
   
   str2 = arr.join("&");
   console.log("str2:",str2,"数据类型：",typeof str2);//str2: 10&20&30&40&50&60 数据类型： string
   ```

   

2. 数组首尾操作方法

   push(args...)  向数组的末尾追加一个或多个元素

   unshift(args...)  向数组的起始位置追加一个或多个元素

   ​	参数 args 要向数组中添加的数据，可以是任意数据类型

   ​	返回值 添加数据后，新的数组长度

   ​	这两个方法，都使原数组结构发生了改变

   

   pop()  删除数组中最后一项

   shift() 删除数组中的第一项

   ​	这两个方法没有参数

   ​	返回值 返回删除的那一项元素

   ```
   var arr = ["苹果","樱桃","猕猴桃","葡萄"];
   console.log("原arr:",arr);//原arr: (4) ["苹果", "樱桃", "猕猴桃", "葡萄"
   
   // push(args...)  向数组的末尾追加一个或多个元素
   var len = arr.push("橙子","桃");
   console.log("结尾添加两项后arr:",arr);//结尾添加一项后arr: (6) ["苹果", "樱桃", "猕猴桃", "葡萄", "橙子", "桃"]
   console.log("结尾添加两项后数组长度：",len);//结尾添加两项后数组长度： 6
   
   // unshift(args...)  向数组的起始位置追加一个或多个元素
   var len2 = arr.unshift("西瓜","柠檬");
   console.log("起始位置追加两项后arr:",arr);//起始位置追加两项后arr: (8) ["西瓜", "柠檬", "苹果", "樱桃", "猕猴桃", "葡萄", "橙子", "桃"]
   console.log("起始位置追加两项后数组长度:",arr.length);//起始位置追加两项后数组长度: 8
   
   // pop()  删除数组中最后一项
   var tipEle = arr.pop();
   console.log("删除最后一项后arr:",arr);//(7) ["西瓜", "柠檬", "苹果", "樱桃", "猕猴桃", "葡萄", "橙子"]
   console.log("删除的元素是：",tipEle);//删除的元素是： 桃
   
   // shift() 删除数组中的第一项
   var headEle = arr.shift();
   console.log("删除第一项后arr:",arr);//删除第一项后arr: (6) ["柠檬", "苹果", "樱桃", "猕猴桃", "葡萄", "橙子"]
   console.log("删除的元素是：",headEle);//删除的元素是： 西瓜
   ```

   

3. 插入、删除、替换的方法

   splice(startIndex,delCount,addEles...)   在指定索引处，删除指定数量的元素，并追加新的元素

   ​	参数  startIndex  插入或删除元素的起始索引

   ​			  delCount   指定索引处开始删除的元素的个数

   ​			  addEles...  在指定索引处插入一个或多个元素

   ​	返回值  返回的是删除的元素组成的数组

   ```
   var arr = [10,20,30,40,50,60];
   console.log("arr:",arr);//arr: (6) [10, 20, 30, 40, 50, 60]
   // splice(startIndex,delCount,addEles...)   在指定索引处，删除指定数量的元素，并追加新的元素
   var delEles = arr.splice();
   console.log("arr:",arr,"delEles:",delEles);//arr: (6) [10, 20, 30, 40, 50, 60] delEles: []
   
   delEles = arr.splice(4);//指定一个起始索引，那么就会删除这个索引后面所有的元素
   console.log("arr:",arr,"delEles:",delEles);//arr: (4) [10, 20, 30, 40] delEles: (2) [50, 60]
   
   delEles = arr.splice(2,1);
   console.log("arr:",arr,"delEles:",delEles);//arr: (3) [10, 20, 40] delEles: [30]
   
   delEles = arr.splice(1,0,300,500,600,800);
   console.log("arr:",arr,"delEles:",delEles);//arr: (7) [10, 300, 500, 600, 800, 20, 40] delEles: []
   ```

   

4. 数组拼接 和 数组片段截取

   concat(args)  拼接一个或多个元素或数组

   ​		参数 args 拼接的元素或数组

   ​		返回值是拼接后的新数组

   slice(startIndex,endIndex)  截取指定索引之间的元素

   ​		参数  startIndex 截取数组的起始索引

   ​				  endIndex 截取数组的结束索引；可以省略，如果省略，截取到数组的末尾

   ​		返回值 截取的元素组成的新数组

   上面两个方法，不会改变原数组

   ```
   var arr = ["苹果","香蕉","橘子","火龙果","猕猴桃"];
   console.log("原数组arr:",arr);//原数组arr: (5) ["苹果", "香蕉", "橘子", "火龙果", "猕猴桃"]
   
   // concat(args)  拼接一个或多个元素或数组
   var newArr = arr.concat("橙子","柚子",["西瓜","桃"]);
   console.log("拼接后arr:",arr);//拼接后arr: (5) ["苹果", "香蕉", "橘子", "火龙果", "猕猴桃"]
   console.log("拼接后返回的数组newArr:",newArr);拼接后返回的数组newArr: (9) ["苹果", "香蕉", "橘子", "火龙果", "猕猴桃", "橙子", "柚子", "西瓜", "桃"]
   
   
   // slice(startIndex,endIndex)  截取指定索引之间的元素
   //指定一个起始索引，一直截取到最后
   var sliceArr = newArr.slice(6);
   console.log("截取后newArr:",newArr);//截取后newArr: (9) ["苹果", "香蕉", "橘子", "火龙果", "猕猴桃", "橙子", "柚子", "西瓜", "桃"]
   console.log("截取的数组：",sliceArr);//截取的数组： (3) ["柚子", "西瓜", "桃"]
   
   //指定两个参数：截取两个索引之间的数组片段  左闭右开
   sliceArr = newArr.slice(3,6);
   console.log("截取的数组：",sliceArr);//截取的数组： (3) ["火龙果", "猕猴桃", "橙子"]
   ```

   

5. 倒叙 和 排序

   reverse()     对数组中的元素进行倒叙排列；没有参数

   sort(callbackfn)  对数组中的元素进行排序

   ​	参数 callbackfn是一个回调函数，通过这个回调函数指定排序的规则

   两个方法改变了原数组

   ```
   var arr = [10,20,30,40,50,60];
   console.log("原数组arr:",arr);//原数组arr: (6) [10, 20, 30, 40, 50, 60]
   
   // reverse() 对数组中的元素进行倒叙排列；没有参数
   arr.reverse();
   console.log("倒叙后arr:",arr);//倒叙后arr: (6) [60, 50, 40, 30, 20, 10]
   
   
   // sort(callbackfn)  对数组中的元素进行排序
   var array = [10,8,34,90,23,123,67,89];
   console.log("原array:",array);//原array: (8) [10, 8, 34, 90, 23, 123, 67, 89]
   //不添加任何参数，默认按照 ASCII码 排序
   array.sort();
   console.log("默认排序后array:",array);//默认排序后array: (8) [10, 123, 23, 34, 67, 8, 89, 90]
   
   //通过 回调函数指定排序的规则
   //指定升序的规则(按照数值大小)
   array.sort(function (a,b) {
       return a - b;
   });
   console.log("指定升序的规则array:",array);//指定升序的规则array: (8) [8, 10, 23, 34, 67, 89, 90, 123]
   
   //指定降序的规则(按照数值大小)
   array.sort(function (a,b) {
       return b - a;
   });
   console.log("指定降序的规则array:",array);//指定降序的规则array: (8) [123, 90, 89, 67, 34, 23, 10, 8]
   ```

   

   ## 27.4 数组的遍历

   使用for循环，一一获取数组中的元素

   ```
   var arr = ["苹果", "香蕉", "橘子", "火龙果", "猕猴桃", "橙子", "柚子", "西瓜", "桃"];
   
   //使用 for 循环对数组进行遍历，也就是一一获取数组中的元素   数组索引从0开始
   for (var i = 0; i < arr.length; i++) {
       console.log("数组中第" + (i + 1) + "个元素是：" + arr[i]);
   }
   ```




# 二十八、字符串对象

前面介绍数据类型时，介绍过字符串是由引号包裹的文本。

字符串除了可能是基本数据类型外，还可能使引用数据类型，所以它比较特殊。其它比较特殊的放在高级课中讲

字符串是一个类数组，既然是类数组，就具有索引和长度，索引从 0开始，长度通过 length 属性获取

类数组可以通过索引去读取对应的值，但是不能添加和修改。

举例："Hello"   '男'



### 28.1 字符串对象的创建方式

- 字面量的方式   var str = "Hello World!"；

- new关键字  var str = new String();

  String()构造函数中可以添加字符串参数 如 var str = new String("Hello World!")

  ```
  //字符串对象的创建方式一: 字面量的方式
  var str = "Hello String";
  console.log("str:",str,"数据类型：",typeof str);//str: Hello String 数据类型： string 这是一个基本数据类型
  
  //通过索引去读取对应的字符
  console.log("字符串中的第一个字符：",str[0]);//字符串中的第一个字符： H
  console.log("字符串中字符的个数：",str.length);//字符串中字符的个数： 12
  console.log("字符串中的最后一个字符：",str[str.length - 1]);//字符串中的最后一个字符： g
  
  //通过索引不可以修改和添加字符
  str[5] = "&";
  console.log("str:",str);//str: Hello String
  
  //字符串对象的创建方式二：new 关键字
  var str2 = new String();
  console.log("str2:",str2,"数据类型：",typeof str2);//str2: String {""} 数据类型： object  这是一个引用数据类型
  
  str2 = new String("Hello new String");
  console.log("str2:",str2);//str2: String {"Hello new String"}
  ```

  

### 28.2 字符串对象的属性

length  获取字符串中字符的个数

constructor  获取字符串对象的构造函数

```
var str = "Hello World!";
// length  获取字符串中字符的个数
console.log("str长度：",str.length);//str长度： 12

// constructor  获取字符串对象的构造函数
console.log("str的构造函数：",str.constructor);//str的构造函数： ƒ String() { [native code] }
```



### 28.3 字符串对象方法

- concat(args...)  方法拼接一个或多个字符或字符串

​		参数 args 字符或字符串

```
//字符串拼接方法一：利用 + 运算符   只要是有字符串存在的 + 运算都是字符串拼接操作
var str = "Hello";
console.log("str:",str);//str: Hello

str += " World";
console.log("+拼接字符串str:",str);//+拼接字符串str: Hello World

//字符串拼接方式二：利用 concat() 方法
var newStr = str.concat("!"," Welcome to code World!")
console.log("concat拼接后原字符串str:",str);//concat拼接后原字符串str: Hello World  原字符串没有发生改变
console.log("concat拼接后返回的新字符串newStr:",newStr);//concat拼接后返回的新字符串newStr: Hello World! Welcome to code World!
```



- split(splitter,limit)  方法用来按照指定的切割符切割字符串

​	   参数 splitter 指定切割符，可以省略

​				limit  切割后，数组保留的长度

​	   返回值是切割后的字符组成的数组

```
//split(splitor)  方法用来按照指定的切割符切割字符串
var str = "Hello World! Welcome to code World!";
console.log("str:",str);//str: Hello World! Welcome to code World!

//不给任何参数:将整个字符串作为数组的元素
var arr = str.split();
console.log("arr:",arr);//arr: ["Hello World! Welcome to code World!"]

//给一个参数，切割符
arr = str.split(" ");
console.log("arr:",arr);//arr: (6) ["Hello", "World!", "Welcome", "to", "code", "World!"]

//给两个参数，限定切割后数组的长度
arr = str.split(" ",2);
console.log("arr:",arr);//arr: (2) ["Hello", "World!"]
```

练习：给一个字符串数据 "name=jack&age=23&sex=female"，然后对其进行切割，最终形成一个类似于对象的格式'{"name":"jack","age":"23","sex":"female"}'。

提示：数组的遍历、字符串的切割、字符串拼接

```
var str = "name=jack&age=23&sex=female";

//利用 split 方法进行第一次切割处理
var arr1 = str.split("&");
// console.log("arr1:",arr1);//arr1: (3) ["name=jack", "age=23", "sex=female"]

//数组遍历 获取里面的字符串元素
var str = "{";
for (var i = 0; i < arr1.length; i++) {
    // console.log(arr1[i]);
    //使用 split 方法进行二次切割
    var arr2 = arr1[i].split("=");
    console.log(arr2);
    str += "\"";
    str +=  arr2[0] + "\"";
    str += ":\"";
    str += arr2[1] + "\"";
    if(i !== arr1.length - 1){
        str += ","
    }
}
str += "}";
console.log("str:",str);
```



- 截取字符串的方法

  slice(startIndex,endIndex)  获取指定索引之间的字符串片段，左闭右开

  subString(startIndex,endIndex) 获取指定索引之间的字符串片段，左闭右开

  subStr(startIndex,howmany)  获取指定索引处开始指定数量的字符串片段

  返回值都是截取的字符串片段

  ```
  var str = "Hello World! Welcome to code World!";
  console.log("str:",str);//str: Hello World! Welcome to code World!
  
  // slice(startIndex,endIndex)  获取指定索引之间的字符串片段，左闭右开
  //没有任何参数  直接相当于复制字符串
  var sliceStr = str.slice();
  console.log("sliceStr:",sliceStr);//sliceStr: Hello World! Welcome to code World!
  
  //指定一个参数  从这个指定的索引开始截取到字符串的最后
  sliceStr = str.slice(13);
  console.log("sliceStr:",sliceStr);//sliceStr: Welcome to code World!
  
  //指定两个参数  获取两个参数之间的字符串片段 [a,b)
  sliceStr = str.slice(13,20);
  console.log("sliceStr:",sliceStr);//sliceStr: Welcome
  
  // substring(startIndex,endIndex) 获取指定索引之间的字符串片段，左闭右开
  //用法 同slice  可以不设置参数、一个参数、两个参数
  subStr = str.substring(13,20);
  console.log(subStr);//Welcome
  
  // substr(startIndex,howmany)  获取指定索引处开始指定数量的字符串片段
  var newStr = str.substr();
  console.log("newStr:",newStr);// newStr: Hello World! Welcome to code World!
  
  newStr = str.substr(13);
  console.log("newStr:",newStr);//newStr: Welcome to code World!
  
  //两个参数：第一个参数是截取的起始索引  第二个参数截取的字符个数
  newStr = str.substr(13,7);
  console.log("newStr:",newStr);//newStr: Welcome
  ```

- 索引相关的方法

  charAt(index)  获取指定索引处的字符 ( [index]也能获取)

  indexOf(searchVale,startIndex?)  从指定索引处开始查找指定字符第一次出现的索引值，如果找不到返回-1

  lastIndexOf(searchVale,startIndex?) 从指定索引处开始查找指定字符最后一次出现的索引值

  ```
  var str = "Hello World! Welcome to code World!";
  // charAt(index)  获取指定索引处的字符 ( [index]也能获取)
  var code = str.charAt(7);
  console.log("code:",code);//code: o
  
  code = str[7];
  console.log("code:",code);//code: o
  //同样 charAt 方式也是只能读取数据 不能修改数据
  
  
  // indexOf(searchVale,startIndex?)  从指定索引处开始查找指定字符第一次出现的索引值，如果找不到返回-1
  //只有一个参数，默认从第一个索引开始查找
  var idx = str.indexOf("o");
  console.log("查找的o在字符串中第一次出现的位置：",idx);//查找的o在字符串中第一次出现的位置： 4
  
  //两个参数：第一个参数为要查找字符或字符片段   第二个参数指定起始查找的索引
  idx = str.indexOf("o",12);
  console.log("从索引12开始查找的o在字符串中第一次出现的位置：",idx);//从索引12开始查找的o在字符串中第一次出现的位置： 17
  
  // lastIndexOf(searchVale,startIndex?) 从指定索引处开始查找指定字符最后一次出现的索引值
  // 用法同 indexOf() 只不过从后往前找，但是索引还是正向从0开始计算
  var lIdx = str.lastIndexOf("o");
  console.log("o在字符串中最后一次出现的索引：",lIdx);//o在字符串中最后一次出现的索引： 30
  ```

  练习：获取指定文件的后缀名 文件为 “D:\爱创32期 JS与JQ\06 JS基础第六天\代码\07 索引相关的方法.html”



- 转换大小写的方法

  toUpperCase()  将字符串中所有的英文字母转为大写

  toLowerCase() 将字符串中所有的英文字母转为小写

  ​	没有参数

  ​	返回值 转换后的新字符串

  ```
  var str = "Hello World! Welcome to code World!";
  console.log("原字符串str:",str);//原字符串str: Hello World! Welcome to code World!
  
  var lowStr = str.toLowerCase();
  console.log("转为小写后lowStr:",lowStr);//转为小写后lowStr: hello world! welcome to code world!
  
  var upStr =str.toUpperCase();
  console.log("转为大写后upStr:",upStr);//转为大写后upStr: HELLO WORLD! WELCOME TO CODE WORLD!
  ```

  练习：有一个字符串 “hello world! welcome to code world!”，将这个字符串中所有的引文单词首字母大写并返回，最终打印效果 “Hello World! Welcome To Code World!”；

  

# 二十九、正则表达式对象

概述：

​		正则表达式(regular expression)描述了一种字符串匹配模式(pattern); 

​		可以用来检查一个串中是否含有某种子串、将匹配的子串替换或者从某个串中取出符合某个条件的子串等。

### 29.1 正则表达式对象的创建方式

- 字面量的方式  var patt = /匹配模式/修饰符;

  ​	/ /  边界的意思       修饰符可以省略

  ```
  //正则表达式操作的式字符串
  var str = "Hello China! 你好，中国！"
  
  //匹配汉字  Unicode码   是一个固定用法，中文只能在正则表达式里这样表示
  var patt = /[\u4e00-\u9fa5]/;
  //test()  匹配指定字符串中是否含有指定规则的字符  返回一个布尔值，匹配成功 返回true 否则返回false
  console.log(patt.test(str));//true
  console.log(patt.test("hehe"));//false
  ```

- 使用new关键字  var patt = new RegExp(/匹配模式/,修饰符);

  ```
  //匹配字符串中是否含有数字
  var reg = new RegExp(/[0-9]/);
  console.log(reg.test("hehe"));//false
  console.log(reg.test("hehe123"));//true
  ```

  

### 29.2 正则表达式中的方法

  test()  检测一个字符串是否匹配某种模式，如果字符串中含有匹配的文本，则返回true，否则返回false

  exec()  检索字符串中的指定值；返回符合指定规则的第一个字符或字符串信息，返回值是一个数组；

```
var patt = /[\u4e00-\u9fa5]/;
// test()  检测一个字符串是否匹配某种模式，如果字符串中含有匹配的文本，则返回true，否则返回false
console.log(patt.test("test方法检测本字符串中是否含有汉字！！"));//true
console.log(patt.test("test method test string has chinese ?"));//false

// exec()  检索字符串中的指定值；返回符合指定规则的第一个字符或字符串信息，返回值是一个数组；
console.log(patt.exec("exec检测本字符串符合规则的第一个字符！！"));//["检", index: 4, input: "exec检测本字符串符合规则的第一个字符！！"]
console.log(patt.exec("exec method get the first chinese char in string"));//null
```



### 29.3 字符串中可以使用正则表达式的方法

split()   按照指定的匹配模式去切割字符串，返回切割后的字符串组成的数组

replace()  按照指定的规则替换字符串中的字符

search()  查找符合指定匹配规则的字符在原字符串中第一次出现的位置

match()  查找符合指定规则的字符或字符串信息，并返回一个数组

```
var str = "你好，Jack! 欢迎来到中国!";

// split()   按照指定的匹配模式去切割字符串，返回切割后的字符串组成的数组
var arr = str.split(' ');
console.log("arr:",arr);//arr: (2) ["你好，Jack!", "欢迎来到中国!"]

var pattArr = str.split(/\s/);// \s 正则表达式中的元字符 代表空格
console.log("pattArr:",pattArr);//pattArr: (2) ["你好，Jack!", "欢迎来到中国!"]

// replace()  按照指定的规则替换字符串中的字符  返回一个新的字符串
//替换 字符串片段 Jack
var rStr = str.replace("Jack","Lucy");
console.log("rStr:",rStr);//rStr: 你好，Lucy! 欢迎来到中国!

var regStr = str.replace(/Jack/,"David");
console.log("regStr",regStr);//regStr 你好，David! 欢迎来到中国!

//替换 ! 为 。
rStr = str.replace("!","。");
console.log("rStr:",rStr);//rStr: 你好，Jack。 欢迎来到中国!  只能替换一个

var regStr = str.replace(/!/g,"。");// 正则表达式中的修饰符  g 执行全局匹配  会将所有匹配到的内容进行替换
console.log("regStr",regStr);//regStr 你好，Jack。 欢迎来到中国。

// search()  查找符合指定匹配规则的字符在原字符串中第一次出现的位置
var idx = str.search("!");
console.log("idx:",idx);//idx: 7

var regIdx = str.search(/[a-z]/);//正则表达式中的匹配模式 [a-z] 匹配的是所有的小写英文字母
console.log("regIdx:",regIdx);//regIdx: 4

```



match() 和 exec() 方法的区别：

```
// 匹配中文的正则表达式
var patt = /[\u4e00-\u9fa5]/;

//声明一个字符串
var str = "你好，Jack! 欢迎来到中国!";

// exec()  正则表达式中的方法。检索字符串中的指定值；返回符合指定规则的第一个字符或字符串信息，返回值是一个数组；
var execArr = patt.exec(str);
console.log("execArr:",execArr);//execArr: ["你", index: 0, input: "你好，Jack! 欢迎来到中国!"]

// match()  字符串方法。查找符合指定规则的字符或字符串信息，并返回一个数组
var matchArr = str.match(patt);
console.log("matchArr:",matchArr);//matchArr: ["你", index: 0, input: "你好，Jack! 欢迎来到中国!"]

//执行全局匹配的正则表达式
var patt2 = /[\u4e00-\u9fa5]/g;

execArr = patt2.exec(str);
console.log("execArr:",execArr);//execArr: ["你", index: 0, input: "你好，Jack! 欢迎来到中国!"]

matchArr = str.match(patt2);
console.log("matchArr:",matchArr);//matchArr: (8) ["你", "好", "欢", "迎", "来", "到", "中", "国"]

//区别：一个是正则表达式中的方法，正则表达式对象才可以调用；一个是字符串中的方法，只能是字符串对象进行调用
//在执行全局匹配时，修饰符 g 对 exec 方法无效
```



### 29.4 修饰符

g   执行全局匹配

i   执行忽略大小写的匹配

m  执行多行匹配

```
// g   执行全局匹配
var pass = "xshls123";
var arr = pass.match(/[s-z]/);
console.log("没有执行全局匹配，返回第一个符合条件元素组成的数组：",arr);
//匹配结果：没有执行全局匹配，返回第一个符合条件元素组成的数组： ["x", index: 0, input: "xshls123"]

arr = pass.match(/[s-z]/g);
console.log("执行全局匹配，返回所有符合条件元素组成的数组：",arr);
//匹配结果：执行全局匹配，返回所有符合条件元素组成的数组： (3) ["x", "s", "s"]


// i   执行忽略大小写的匹配
var str = "Hello World!";
var arr2 = str.match(/[A-K]/g);
console.log("没有执行忽略大小写的操作arr2:",arr2);//没有执行忽略大小写的操作arr2: ["H"]

var arr2 = str.match(/[A-K]/gi);
console.log("执行忽略大小写的操作arr2:",arr2);//执行忽略大小写的操作arr2: (3) ["H", "e", "d"]


// m  执行多行匹配
var mStr = "Hello\nWorld";  // \n 换行的转义字符
console.log("mStr:",mStr);

//匹配字符串中的单词是否有以 W 开头的单词
var patt = /^W/; // ^ 正则表达式中的量词，代表以 指定模式开头  注意此 ^ 位置紧跟在起始边界后面
var flag = patt.test(mStr);
console.log("没有执行多行匹配的结果：",flag === true ? "存在W开头的单词" : "不存在W开头的单词");
//打印结果 没有执行多行匹配的结果： 不存在W开头的单词

patt = /^W/m;
flag = patt.test(mStr);
console.log("执行多行匹配的结果：",flag === true ? "存在W开头的单词" : "不存在W开头的单词");
//打印结果  执行多行匹配的结果： 存在W开头的单词
```

练习：获取字符串 "Hello Jack!! 欢迎你来到中国！！" 中所有的汉字。



### 29.5 方括号

用于查找某个范围内的字符

| 表达式                                                       | 描述                               |
| :----------------------------------------------------------- | :--------------------------------- |
| [[abc\]](https://www.runoob.com/jsref/jsref-regexp-charset.html) | 查找方括号之间的任何字符。         |
| [[^abc\]](https://www.runoob.com/jsref/jsref-regexp-charset-not.html) | 查找任何不在方括号之间的字符。     |
| [0-9]                                                        | 查找任何从 0 至 9 的数字。         |
| [a-z]                                                        | 查找任何从小写 a 到小写 z 的字符。 |
| [A-Z]                                                        | 查找任何从大写 A 到大写 Z 的字符。 |
| [A-z]                                                        | 查找任何从大写 A 到小写 z 的字符。 |
| [adgk]                                                       | 查找给定集合内的任何字符。         |
| [^adgk]                                                      | 查找给定集合外的任何字符。         |
| (red\|blue\|green)                                           | 查找任何指定的选项。               |

注意：[A-z] 这里有六个特殊的字符存在于 Z  到  a之间，所以严格意义上讲，它并不能真正的匹配所有英文字母，因为还有可能匹配到特殊字符。详见 ASCII 码表。

```
var str = "an123Zs`+=ex|\hg[000]*^44ioS";
var patt = /[A-z]/g;

console.log(str.match(patt));//(15) ["a", "n", "Z", "s", "`", "e", "x", "h", "g", "[", "]", "^", "i", "o", "S"]

//严格上，如果只是匹配所有的大小写英文字母，请使用以下匹配方式
// patt = /[A-Za-z]/g;
patt = /[A-Z]/gi;
console.log(str.match(patt));//(11) ["a", "n", "Z", "s", "e", "x", "h", "g", "i", "o", "S"]

// [abc]查找方括号之间的任何字符。
patt = /[a3Zo85vs]/gi;
console.log(str.match(patt));//(6) ["a", "3", "Z", "s", "o", "S"]

// [^abc]查找任何不在方括号之间的字符。
patt = /[^a3Zo85vs]/gi;
console.log(str.match(patt));//(21) ["n", "1", "2", "`", "+", "=", "e", "x", "|", "h", "g", "[", "0", "0", "0", "]", "*", "^", "4", "4", "i"]    
```



### 29.6 元字符

元字符（Metacharacter）是拥有特殊含义的字符：

| 元字符                                                       | 描述                                        |
| :----------------------------------------------------------- | :------------------------------------------ |
| [.](https://www.runoob.com/jsref/jsref-regexp-dot.html)      | 查找单个字符，除了换行和行结束符。          |
| [\w](https://www.runoob.com/jsref/jsref-regexp-wordchar.html) | 查找单词字符。                              |
| [\W](https://www.runoob.com/jsref/jsref-regexp-wordchar-non.html) | 查找非单词字符。                            |
| [\d](https://www.runoob.com/jsref/jsref-regexp-digit.html)   | 查找数字。                                  |
| [\D](https://www.runoob.com/jsref/jsref-regexp-digit-non.html) | 查找非数字字符。                            |
| [\s](https://www.runoob.com/jsref/jsref-regexp-whitespace.html) | 查找空白字符。                              |
| [\S](https://www.runoob.com/jsref/jsref-regexp-whitespace-non.html) | 查找非空白字符。                            |
| [\b](https://www.runoob.com/jsref/jsref-regexp-begin.html)   | 匹配单词边界。                              |
| [\B](https://www.runoob.com/jsref/jsref-regexp-begin-not.html) | 匹配非单词边界。                            |
| \0                                                           | 查找 NULL 字符。                            |
| [\n](https://www.runoob.com/jsref/jsref-regexp-newline.html) | 查找换行符。                                |
| \f                                                           | 查找换页符。                                |
| \r                                                           | 查找回车符。                                |
| \t                                                           | 查找制表符。                                |
| \v                                                           | 查找垂直制表符。                            |
| [\xxx](https://www.runoob.com/jsref/jsref-regexp-octal.html) | 查找以八进制数 xxx 规定的字符。             |
| [\xdd](https://www.runoob.com/jsref/jsref-regexp-hex.html)   | 查找以十六进制数 dd 规定的字符。            |
| [\uxxxx](https://www.runoob.com/jsref/jsref-regexp-unicode-hex.html) | 查找以十六进制数 xxxx 规定的 Unicode 字符。 |

```
var str = "Hello123";
//指定匹配规则，匹配所有的数字
// var patt = /[0-9]/g;
var patt = /\d/g;
console.log(str.match(patt));//(3) ["1", "2", "3"]

//指定匹配规则，匹配所有的非数字
// patt = /[^0-9]/g;
patt = /\D/g;
console.log(str.match(patt));//(5) ["H", "e", "l", "l", "o"]
```



### 29.7 量词

| 量词                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [n+](https://www.runoob.com/jsref/jsref-regexp-onemore.html) | 匹配任何包含至少一个 n 的字符串。例如，/a+/ 匹配 "candy" 中的 "a"，"caaaaaaandy" 中所有的 "a"。 |
| [n*](https://www.runoob.com/jsref/jsref-regexp-zeromore.html) | 匹配任何包含零个或多个 n 的字符串。例如，/bo*/ 匹配 "A ghost booooed" 中的 "boooo"，"A bird warbled" 中的 "b"，但是不匹配 "A goat grunted"。 |
| [n?](https://www.runoob.com/jsref/jsref-regexp-zeroone.html) | 匹配任何包含零个或一个 n 的字符串。例如，/e?le?/ 匹配 "angel" 中的 "el"，"angle" 中的 "le"。 |
| [n{X}](https://www.runoob.com/jsref/jsref-regexp-nx.html)    | 匹配包含 X 个 n 的序列的字符串。例如，/a{2}/ 不匹配 "candy," 中的 "a"，但是匹配 "caandy," 中的两个 "a"，且匹配 "caaandy." 中的前两个 "a"。 |
| [n{X,}](https://www.runoob.com/jsref/jsref-regexp-nxcomma.html) | X 是一个正整数。前面的模式 n 连续出现至少 X 次时匹配。例如，/a{2,}/ 不匹配 "candy" 中的 "a"，但是匹配 "caandy" 和 "caaaaaaandy." 中所有的 "a"。 |
| [n{X,Y}](https://www.runoob.com/jsref/jsref-regexp-nxy.html) | X 和 Y 为正整数。前面的模式 n 连续出现至少 X 次，至多 Y 次时匹配。例如，/a{1,3}/ 不匹配 "cndy"，匹配 "candy," 中的 "a"，"caandy," 中的两个 "a"，匹配 "caaaaaaandy" 中的前面三个 "a"。注意，当匹配 "caaaaaaandy" 时，即使原始字符串拥有更多的 "a"，匹配项也是 "aaa"。 |
| [n$](https://www.runoob.com/jsref/jsref-regexp-ndollar.html) | 匹配任何结尾为 n 的字符串。                                  |
| [^n](https://www.runoob.com/jsref/jsref-regexp-ncaret.html)  | 匹配任何开头为 n 的字符串。                                  |
| [?=n](https://www.runoob.com/jsref/jsref-regexp-nfollow.html) | 匹配任何其后紧接指定字符串 n 的字符串。                      |
| [?!n](https://www.runoob.com/jsref/jsref-regexp-nfollow-not.html) | 匹配任何其后没有紧接指定字符串 n 的字符串。                  |



需求：匹配网址

​		网址 以 http 或 https 开头  后面是 ://www.  后面是域名由 3-10位的英文或数字  后面 .com 或 .cn 或 ,net

```
<input type="url" id="url" placeholder="请输入合法的网址" value="">
<span id="tip"></span>
<script>
    //通过 id 去获取元素
    var url = document.getElementById('url');
    var tip = document.getElementById("tip");

    // 网址 以 http 或 https 开头  后面是 ://www.  后面是域名由 3-10位的英文或数字  后面 .com 或 .cn 或 .net
    var patt = /^http(s)?:\/\/w{3}\.[A-Za-z0-9]{3,9}\.(com|cn|net)$/;

    //设置表单正在输入的事件
    url.oninput = function () {
        // console.log("对方正在输入...");
        // console.log(this.value,"数据类型：",typeof(this.value));//this 指代指定事件函数的那个元素 也就是 input#url
        //输入的过程中验证是否符合规则
        if(patt.test(this.value)){
            //向页面元素中写入内容
            tip.innerHTML = "网址符合命名规则 √";
            //修改文本的颜色
            tip.style.color = "green";
        }else{
            tip.innerHTML = "网址不符合规则 ×";
            tip.style.color = 'red';
        }
    }
</script>
```



### 29.8 分组

虽然量词的出现，能帮助我们处理一排密紧相连的同类型字符。但这是不够的，我们用中括号表示范围内选择，大括号表示重复次数。如果想获取重复多个字符，我们就要用小括号进行分组了。

```
// 重复出现多个字符
console.log("abcabcabchhh".match(/(abc){3}/g));
```



**分组的反向引用**

反向引用标识是对正则表达式中的匹配组捕获的子字符串进行编号，通过“\编号(在正则表达式中)”，“$编号（在正则表达式外）”进行引用。从1开始计数。有一个分组就对应一个编码。

如果替换参数为一个函数，能对我们截取到的字符串进行进一步操作，更加灵活多变。带函数的方式是我们用的比较多的。

```
//反向引用标识是对正则表达式中的匹配组捕获的子字符串进行编号，通过“\编号(在正则表达式中)”，
// “$编号（在正则表达式外）”进行引用。从1开始计数。有一个分组就对应一个编码。
var patt = /(stu)(tea)\1\2\1/;
console.log(patt.test("stutea"));//false
console.log(patt.test("stuteastutea"));//false
console.log(patt.test("stuteastuteastu"));//true

console.log(RegExp.$1);
console.log(RegExp.$2);
console.log(RegExp.$3);
```



**中文**

匹配中文：[\u4e00-\u9fa5]

是一个固定用法，中文只能在正则表达式里这样表示



练习：匹配密码强度

​		密码规则 如果时纯数字或纯字母，那么提示密码强度低；如果时数字和字母组成的混合密码，密码强度较强；如果除了数字和字母之外，还有一些特殊的字符，那么密码强度高！

​		密码长度 6 - 9 位

练习：匹配手机号

​		手机号规则 以 1 开头，第二位 3 - 9之间的数字，后面9位是 0-9之间所有的数字



# 二十九、Date对象

Date对象可以存储任意一个日期，并且可以精确到毫秒数(1/1000秒);

### 29.1 Date对象的创建 

- var d = new Date(); //Date 对象会自动把当前日期和时间保存为其初始值 
- var d = new Date(milliseconds); //new Date(100000000000); 
- var d = new Date(dateString); //new Date("Oct 11,2015"); 
- var d = new Date(year, month, day, hours, minutes, seconds, milliseconds); //new Date(2016,4,1); 2016年5月1日 0-11代表1-12月

### 29.2 Date对象中的转换方法

- toString() 把Date对象转换为字符串
- toLocaleString() 根据本地时间格式，把Date对象转换为字符串
- toDateString() 把Date对象的日期部分转换为字符串
- toLocaleDateString() 根据本地时间格式，把 Date 对象的日期部分转换为字符串
- toTimeString() 把 Date对象的时间部分转换为字符串
- toLocaleTimeString() 据本地时间格式，把 Date 对象的时间部分转换为字符串
- valueOf() 返回Date对象的原始值;这里的原始值指的是1970年1月1日以来(到指定日期时间)的毫秒数，与getTime()方法获取的值一样 myDate.valueOf();

### 29.3 Date对象中的get/set方法

- get/setTime() 返回/设置时间，单位毫秒数，计算从1970年1月1日零时到日期对象所指的日期的毫秒数 myDate.setTime(2000000000000);
- get/setFullYear() 返回/设置四位数的Date对象年份
- get/setMonth() 返回/设置Date对象月份 (0 ~ 11 代表 1-12月)
- get/setDate() 返回/设置Date对象一个月中的某一天 (1 ~ 31)
- getDay() 从 Date对象返回一周中的某一天 (返回值是0<周日>到6<周六>之间的一个整数)
- get/setHours() 返回/设置Date对象的小时 (0 ~ 23)
- get/setMinutes() 返回/设置Date对象的分钟 (0 ~ 59)
- get/setSeconds() 返回/设置Date对象的秒数 (0 ~ 59)

### 29.4 封装日期格式化函数：

```
/**
 * 获取当前时间并进行格式化输出  "2019年05月01日 星期六 13时:06分:01秒"
 * @function formatdate
 * @returns 当前日期和时间
 */
function formatdate(){
    var weeks = ["星期日","星期一","星期二","星期三","星期四","星期五","星期六"]
    var date = new Date();
    var year = date.getFullYear();
    var month = date.getMonth() + 1 < 10 ? "0" + (date.getMonth() + 1) : date.getMonth() + 1;
    var theDate = date.getDate() < 10 ? "0" + date.getDate() : date.getDate();
    var week = date.getDay();
    var hour = date.getHours() < 10 ? "0" + date.getHours() : date.getHours();
    var min = date.getMinutes() < 10 ? "0" + date.getMinutes() : date.getMinutes();
    var second = date.getSeconds() < 10 ? "0" + date.getSeconds() : date.getSeconds();
    return year + "年" + month + "月" + theDate + "日\t" + weeks[week] + "\t" + hour + "时:" + min + "分:" + second + "秒";
}
```

### 29.5 Date静态方法

Date.now()     获取当前时间





<img src="http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/bom.png" alt="bom" style="zoom:150%;" />



# 三十、BOM 概述

在 JavaScript 语言中有三种对象：内置对象、宿主对象、自定义对象。

宿主对象就是执行 JavaScript 脚本的环境所提供的对象。对于网页编程来说，`js` 是运行在浏览器上的，所以对于网页编程来说，宿主对象就是浏览器对象，而学习浏览器对象，就要学习浏览器对象模型，即BOM。

BOM (Browser Object Model)，浏览器对象模型：

- BOM主要用于管理窗口与窗口之间的通讯，因此其核心对象是window ( 即：窗口对象 )；
- 浏览器对象模型（Browser Object Model）尚无正式标准;但由于现代浏览器已经（几乎）实现了 JavaScript 交互性方面的相同方法和属性，因此常被认为是BOM的方法和属性



# 三十一、Window 对象

### 31.1 概述

- window 对象作为浏览器模型中的顶级对象，指的是当前浏览器窗口，其下有对应的只读属性指向 document、history、location、navigator、screen、`clipboardData` 等对象的引用。

- 所有浏览器都支持 window 对象，所有 JavaScript 全局对象、函数以及变量均自动成为 window 对象的成员 (全局变量是 window 对象的属性，全局函数是window 对象的方法，甚至 Html Dom 的 document 也是 window 对象属性之一。

  如  `window.document.getElementById("myId")` 与`document.getElementById("myId")` 相同。



### 31.2 窗口的打开与关闭

- open(url, target, args)  打开新窗口
  - 参数 url         可选。为打开的网址或路径
  - 参数 target   可选。窗口打开方式
  - 参数args       可选。窗口样式设置。为 key=value 的参数字符串。 窗口设置的样式参数参考如下: 
    - top=像素值，窗口顶部离开屏幕顶部的像素数 
    - left=像素值,窗口左端离开屏幕左端的像素数 
    - width=像素值,窗口的宽度 height=像素值，窗口的高度 
    - menubar=yes|no,设置窗口是否有菜单 
    - toolbar=yes|no,设置窗口是否有工具条 
    - scrollbars=yes|no,设置窗口是否有滚动条 
    - status=yes|no,设置窗口是否有状态栏

- close() 关闭当前窗口



### 31.3 窗口关系及框架

- 通过 window.open() 创建的新窗口的 Window 对象具有 opener 属性，可以通过 opener 打开它的原始窗口，这样两个窗口之间就可以相互引用，彼此之间可以读取对方的属性方法，而窗体也是一样;

- 窗体是由 iframe 创建的，该元素有 contentWindow 属性，它引用自身的 Window 对象，而 Window 对象有 frameElement 属性，若该 Window 对象表示一个窗体，则 frameElement 是对 iframe 元素的引用，如以下元素

  ```
  <iframe id = 'f1'></iframe>
  var elt = document.getElementById('f1');
  var win = elt.contentWindow;
  win.frameElement === elt; //true
  window.frameElement === elt; //false 对于顶级窗口来说永远是false
  ```

- 每个 Window 对象都有一个 frames 属性，包括窗体和子窗体。frames 属性引用了它所包含的窗体和子窗体的 Window 对象，frames 是由这些 Window 对象组成的类数组对象，可通过数字或窗体名来进行索引，如引用第一个子窗体 frames[0]，引用第二个子窗体的第三个子窗体 frames[1].frames[2]，引用兄弟窗体 parent.frames[1];

- 内置对象在不同的窗口、窗体之间是相互独立的，它们有自己的一份独立的构造函数和原型对象的副本，它会在所有窗口窗体内自动预定义；而自定义对象则不同，可以在能够相互通信的窗口、窗体之间共享这个对象的构造函数和它的原型；如窗口中定义了Set类，有子窗体A和B，则：
  在父窗口中 ：

  ```
  var s = new Set(); String.toString = function(){return '内置对象';} （修改String的toString方法）
  s.a === 1; //true
  ```

  在A中 ：

  ```
  var sa = new parent.Set(); parent.Set.prototype.a =1; （给自定义类Set的原型添加属性a，则所有能相互通信的窗口共享a）
  var str = '测试';  str.toString; //测试  （调用的是窗体A自身的String对象的toString方法）
  ```

  在B中 ：           

  ```
  var Set = top.Set(); var sb = new Set(); sb.a === 1;  //true
  ```

- 要引用窗口中的一个窗体，可以使用如下语法：

  ```
  frames[i] //当前窗口的框架
  self.frames[i] //当前窗口的框架
  w.frames[i] //窗口 w 的框架
  ```

- 要引用一个框架的父窗口（或父框架），可以使用下面的语法：

  ```
  parent //当前窗口的父窗口
  self.parent //当前窗口的父窗口
  w.parent //窗口 w 的父窗口
  ```

- 要从顶层窗口含有的任何一个框架中引用它，可以使用如下语法：	

  ```
  top //当前框架的顶层窗口
  self.top //当前框架的顶层窗口
  f.top //框架 f 的顶层窗口
  ```



### 31.4 消息框(弹窗、系统对话框)

- alert() 警告框。常用于确保用户可以得到某些信息；当警告框出现后，用户需要点击确定按钮才能继续进行操作
- confirm() 确认框。用于验证是否接收用户操作,当确认框弹出时，用户可以点击“确认”或者“取消”来确定用户操作，当点击“确认”，确认框返回true,如果点击“取消”，确认框返回false
- prompt() 提示框。常用于提示用户在进入页面前输入某个值;当提示框出现后，用户需要输入某个值，然后点击确认后者取消按钮才能继续操作；若点击确认，那么返回输入的值，若点击 取消，则返回null



### 31.5 获取当前视口大小

innerWidth    获取当前视口的宽度（只读）

innerHeight   获取当前视口的高度（只读）

> 不包含工具栏、菜单栏、系统栏、控制台区域....  包含滚动条

IE8及以下浏览器版本不兼容，那么请使用以下方式获取：

```
document.documentElement.clientWidth || document.body.clientWidth;
dowcument.documentElement.clientHeight || document.body.clientHeight;
```

> IE6及以下只能通过 `document.body` 获取

浏览器兼容性写法

```
var width = window.innerWidth || document.documentElement.clientWidth || document.body.clientWidth;
var height = window.innerHeight || document.documentElement.clientHeight || document.body.clientHeight;
```



### 31.6 计时器

setInterval(callbackfn, time)   间歇调用；每隔指定的时间执行一下重复的操作，多次 调用，除非手动清除

setTimeout(callbackfn, time)  延时调用；指定时间后去执行某个操作，只执行一次，可以在执行之前将其清除掉

clearInterval(timer) 清除指定间歇调用

clearTimeout(timer) 清除指定延时调用



```
var num = document.getElementById("num");
    var count = 0;
    var timer = window.setInterval(function(){
        if(count === 100){
            // 清除计时器
            clearInterval(timer)
        }
        num.innerHTML = count++ + "+";
},80);


window.setTimeout(function(){
    alert("不好意思，我打断一下！！")
},5000)
```

练习：在页面中实现一个数字倒计时10 秒效果，当数字变为 0 时，跳转页面到百度

练习：利用 `setTimeout `模拟间歇调用

练习：利用间歇调用和Date日期对象，模拟一个电子时钟，格式：2021年01月12日  11时36分56秒

练习：实现抽奖效果 

```
<div class="box">
    <div><span id="petName">王芊泽</span></div>
    <div><button id="startBtn">开始抽奖</button><button id="stopBtn" style="display: none;">停止抽奖</button></div>
</div>
<script>
    var petNames = ["王芊泽", "李沁", "刘蓓蓓", "杨美林", "李泽旭", "焦宇", "王培徐"];
    // var petPics = []

    // 获取相关元素
    var petName = $('petName'),
        startBtn = $("startBtn"),
        stopBtn = $("stopBtn");

    // 定义定时器的名称
    var timer = null;

    // 点击开始抽奖
    startBtn.onclick = function () {
        startBtn.style.display = "none";
        stopBtn.style.display = "inline";
        timer = setInterval(function () {
            // 获取随机索引
            var ranIndex = parseInt(Math.random() * petNames.length);
            // 获取随机姓名
            var ranName = petNames[ranIndex];
            // 将随机姓名写入到前台
            petName.innerHTML = ranName;
        }, 100)
    }

    // 点击停止抽奖
    stopBtn.onclick = function(){
        stopBtn.style.display = "none";
        startBtn.style.display = "inline";
        // 清除之前的计时器
        clearInterval(timer);
    }

    // 第二种方案：只写一个按钮，通过修改里面的内容实现不同的功能（请大家自行实现），并在姓名前面添加自己的大头像


    function $(id) {
        return document.getElementById(id);
    }
</script>
```



# 三十二、Navigator对象

Navigator对象属性如下：

| 属性                                                         | 说明                                        |
| :----------------------------------------------------------- | :------------------------------------------ |
| [appCodeName](https://www.runoob.com/jsref/prop-nav-appcodename.html) | 返回浏览器的代码名                          |
| [appName](https://www.runoob.com/jsref/prop-nav-appname.html) | 返回浏览器的名称                            |
| [appVersion](https://www.runoob.com/jsref/prop-nav-appversion.html) | 返回浏览器的平台和版本信息                  |
| [platform](https://www.runoob.com/jsref/prop-nav-platform.html) | 返回运行浏览器的操作系统平台                |
| [userAgent](https://www.runoob.com/jsref/prop-nav-useragent.html) | 返回由客户机发送服务器的user-agent 头部的值 |



# 三十三、Screen对象 

Screen对象属性如下：

| 属性                                                         | 说明                                                       |
| :----------------------------------------------------------- | :--------------------------------------------------------- |
| [availHeight](https://www.runoob.com/jsref/prop-screen-availheight.html) | 返回屏幕的高度（不包括Windows任务栏）                      |
| [availWidth](https://www.runoob.com/jsref/prop-screen-availwidth.html) | 返回屏幕的宽度（不包括Windows任务栏）                      |
| [colorDepth](https://www.runoob.com/jsref/prop-screen-colordepth.html) | 返回目标设备或缓冲器上的调色板的比特深度                   |
| [height](https://www.runoob.com/jsref/prop-screen-height.html) | 返回屏幕的总高度                                           |
| [pixelDepth](https://www.runoob.com/jsref/prop-screen-pixeldepth.html) | 返回屏幕的颜色分辨率（每象素的位数） 不支持IE8及以下浏览器 |
| [width](https://www.runoob.com/jsref/prop-screen-width.html) | 返回屏幕的总宽度                                           |



# 三十四、History对象

History对象属性如下：

| 属性                                                        | 说明                   |
| :---------------------------------------------------------- | :--------------------- |
| [length](https://www.runoob.com/jsref/prop-his-length.html) | 返回历史列表中的网址数 |

History对象方法如下：

| 方法                                                         | 说明                                                        |
| :----------------------------------------------------------- | :---------------------------------------------------------- |
| [back()](https://www.runoob.com/jsref/met-his-back.html)     | 加载 history 列表中的前一个 URL，相当于浏览器上面的回退箭头 |
| [forward()](https://www.runoob.com/jsref/met-his-forward.html) | 加载 history 列表中的下一个 URL，相当于浏览器上面的前进箭头 |
| [go()](https://www.runoob.com/jsref/met-his-go.html)         | 加载 history 列表中的某个具体页面                           |



# 三十五、Location对象 

Location对象属性如下：

| 属性                                                         | 描述                                        |
| :----------------------------------------------------------- | :------------------------------------------ |
| [hash](https://www.runoob.com/jsref/prop-loc-hash.html)      | 返回一个URL的锚部分                         |
| [host](https://www.runoob.com/jsref/prop-loc-host.html)      | 返回一个URL的主机名和端口                   |
| [hostname](https://www.runoob.com/jsref/prop-loc-hostname.html) | 返回URL的主机名                             |
| [href](https://www.runoob.com/jsref/prop-loc-href.html)      | 返回完整的URL                               |
| [pathname](https://www.runoob.com/jsref/prop-loc-pathname.html) | 返回的URL路径名。                           |
| [port](https://www.runoob.com/jsref/prop-loc-port.html)      | 返回一个URL服务器使用的端口号               |
| [protocol](https://www.runoob.com/jsref/prop-loc-protocol.html) | 返回一个URL协议（如：http https ftp等协议） |
| [search](https://www.runoob.com/jsref/prop-loc-search.html)  | 返回一个URL的查询部分                       |

Location对象方法如下：

| 方法                                                         | 说明                                         |
| :----------------------------------------------------------- | :------------------------------------------- |
| [assign()](https://www.runoob.com/jsref/met-loc-assign.html) | 载入一个新的文档                             |
| [reload()](https://www.runoob.com/jsref/met-loc-reload.html) | 重新载入当前文档，相当于浏览器上面的刷新按钮 |
| [replace()](https://www.runoob.com/jsref/met-loc-replace.html) | 用新的文档替换当前文档                       |

附地址栏解析：

![image-20210112161122731](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20210112161122731.png)



# 三十六、DOM概述

### 36.1 什么是DOM

- DOM(Document Object Model)文档对象模型，用来表示和操作html或xml文档内容的基础API;
- 当网页被加载时，浏览器会创建页面的文档对象模型DOM，而DOM模型被构造为对象的树（Dom Html Tree）;
- DOM包含了所有的html标签元素、文本字符串、甚至是html注释；
- 利用DOM中的属性和方法，使程序有能力动态的访问和更新文档中的内容、结构以及样式，这样就使得页面的交互性大大增强；

### 36.2 DOM应用

- 通过DOM操作能够改变页面中所有HTML元素；
- 通过DOM操作能够改变页面中所有HTML属性；
- 通过DOM操作能够改变页面中所有CSS样式；
- 通过DOM操作能够对页面中所有事件做出反应；

### 36.3 DOM树 

DOM把层次中的每一个对象都称之为节点，这个层次结构可以看作树形结构，就如同我们的目录，一个根目录下有子目录，子目录下面还有子目录。DOM树形图如下；

![image-20210220113047306](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20210220113047306.png)

### 36.4 DOM节点类型与相关属性

DOM树中所有的对象都是节点，如：文档节点、元素节点、属性节点、文本节点、注释节点等；

节点相关的属性如下：

- nodeName   获取节点的名称，只读
- nodeValue  获取节点内容（适用于文本节点和注释节点）
- nodeType   获取节点类型，只读

一个HTML或XML文档的文件，元素，属性等有不同的节点类型。有12种不同的节点类型，不同的节点类型也可以有不同的子节点类型如下：

| 节点类型 | 描述                  | 子节点                     |                                                              |
| :------- | :-------------------- | :------------------------- | ------------------------------------------------------------ |
| 1        | Element               | 一个元素                   | Element, Text, Comment, ProcessingInstruction, CDATASection, Entity参考手册 |
| 2        | Attr                  | 一个属性                   | Text, Entity参考手册                                         |
| 3        | Text                  | 一个元素的文本内容 或属性  | None                                                         |
| 4        | CDATASection          | 一个文档的CDATA部分        | None                                                         |
| 5        | Entity参考手册        | 实体引用                   | Element, ProcessingInstruction, Comment, Text, CDATASection, Entity参考手册 |
| 6        | Entity                | 一个实体                   | Element, ProcessingInstruction, Comment, Text, CDATASection, Entity参考手册 |
| 7        | ProcessingInstruction | 一个处理指令               | None                                                         |
| 8        | Comment               | 一个注释                   | None                                                         |
| 9        | Document              | 整个文档（DOM树的根节点）  | Element, ProcessingInstruction, Comment, DocumentType        |
| 10       | DocumentType          | 为文档实体提供接口         | None                                                         |
| 11       | DocumentFragment      | 表示邻接节点和它们的子树。 | Element, ProcessingInstruction, Comment, Text, CDATASection, Entity参考手册 |
| 12       | Notation              | 代表一个符号在DTD中的声明  | None                                                         |

通过属性nodeType可以判断节点类型，那么根据节点类型DOM树可以分为以下两种：

- 第一种就是上面讲过的，包含了所有标签、属性、文本、注释等全部类型的DOM树，可以称为节点（node）树；
- 第二种就是只包含标签这一种类型，可以称为元素（element）树。元素树状图更加简洁，查找和操作起来也更加快捷。所以，一般除非必要情况，都使用元素树来操作。

### 36.5  DOM节点层级关系

所谓DOM树中的节点关系，和我们人类直系关系相似，无非就是父子关系、兄弟关系、祖孙关系；对应节点如下：

- 父节点（parent node）     父节点可以拥有任意数量的子节点
- 子节点（child node）      子节点只能拥有一个父节点
- 兄弟节点（sibling node）  拥有相同父节点的同级节点
- 根节点(root node)         一个html文档一般只有一个根节点，根节点没有父节点，是最上层的节点
- 祖先节点   包含子节点的节点都可以叫做祖先节点，包括父节点
- 后代节点   一个节点内包好的所有节点，叫做后代节点，包括子节点

### 36.6 节点的层级访问

- parentNode  获取当前节点的父节点
- childNodes  获取当前元素节点的所有子节点
- firstChild  获取当前元素节点的第一个子节点
- lastChild   获取当前元素节点的最后一个子节点
- previousSibling 获取当前节点的前一个同级节点
- nextSibling     获取当前节点的后一个同级节点

### 36.7 元素的层级访问（Element元素节点之间的访问）

- firstElementChild、lastElementChild  类似firstChild和lastChild,返回类型只有Element类型，忽略文本、注释、空白节点(IE8及以下返回undefined)
- nextElementSibling、previousElementSibling  类似nextSibling和previousSibling,返回类型只有Element类型，忽略文本、注释、空白节点(IE8及以下返回undefined)
- children  得到当前元素所有子元素的集合
- childElementCount  子元素的数量
- Element同样可以访问parentNode属性，只不过返回的结果都是Elment类型 

### 36.8 document对象属性介绍

- document.documentElement       获取文档的根节点
- document.body      获取文档的主体对象
- document.cookie    设置和获取cookie（后面本地存储讲）       
- document.readyState     获取当前文档的载入状态



# 三十七、DOM基础操作

### 37.1 获取元素的六种方式

- getElementById()     通过id名获取元素
- getElementsByTagName()       通过标签名获取元素
- getElementsByClassName()    通过类名获取元素
- getElementsByName()     通过name的值来获取元素，一般用在表单中(含有name属性的标签)
- querySelector()	 通过css选择器获取符合条件的第一个元素
- querySelectorAll()	通过css选择器获取符合条件的所有元素

### 37.2 向页面输出内容的方式

- document.write()
- element.innerHTML
- element.innerText

### 37.3 操作html属性的属性和方法

- 通过对象属性设置和获取元素属性，格式  element.att  || element[att]      如：img.src    li.type   div.className   div.id   p.style 等
- 通过get/set方法设置和获取属性（所有html属性）
  - element.getAttribute(name) 	     通过元素节点的属性名称获取属性的值 
  - element.setAttribute(name,value)   设置元素中的属性值
  - element.removeAttribute(name)  删除指定属性

### 37.4 获取和设置css样式

- **内部样式**

  - 利用上面设置html属性的方式添加样式

    ```
    p.style.color = "red";
    p.style = "color:red;text-indent:2em;";
    p.setAttribute("style","color:red;text-indent:2em;")
    ```

  - 利用cssText添加多个样式

    ```
    p.style.cssText = "color:red;text-indent:2em;";
    ```

  - 清除内部样式

    ```
    element.style.cssText = "";
    element.removeAttribute("style","");
    element.style="";
    ```

- **外部样式（考虑兼容性）**

  高级浏览器使用 window.getComputed(element, null)

  IE低版本浏览器使用 element.currentStyle

  ```
  // 浏览器兼容性写法
  function getOutStyle(ele,attr) {
      if (window.getComputedStyle) { //兼容高版本
          return window.getComputedStyle(ele)[attr];
      } else { //兼容 IE8以下
          return ele.currentStyle[attr];
      }
  }
  ```



## 三十八、DOM高级操作

### 38.1 节点创建

- createElement()     创建一个元素节点

- createTextNode()   创建文本节点

- createAttribute()     创建属性节点，属性节点通过 nodeValue 或者 value 进行赋值

  > 属性节点通过借助  setAttributeNode(attr) 方法进行设置

- createComment()   创建注释节点

### 38.2 节点操作

- appendChild()    向指定元素中追加一个子元素节点

- insertBefore(newNode, oldNode)   向父元素内部指定元素的前面插入一个新的子元素节点

- replaceChild(newNode, oldNode)   使用新的节点替换父元素内部的原有子节点

- cloneNode(deep?)   克隆指定节点，参数deep默认false，仅克隆当前节点。设置true，克隆当前及后代所有节点

- removeChild()    从父元素中删除指定子元素节点

- remove(index?)    移除指定(索引)节点

  ```
  例： 删除下拉列表中选中的菜单项
  ================================== html代码 ================================
  <select id="mySelect">
  function removeOption(){
      <option>苹果</option>
      <option>香蕉</option>
      <option>葡萄</option>
      <option>西瓜</option>
      <option>橙子</option>
  </select>
  <input type="button" onclick="removeOption()" value="移除选中的菜单项"/>
  ================================== js代码 ================================
  function removeOption(){
      var myEle = document.getElementById("mySelect");
      myEle.remove(myEle.selectedIndex);
  }
  小贴士：selectedIndex 属性可设置或返回下拉列表中被选选项的索引号；若允许多重选择，则仅会返回第一个被选选项的索引号	
  ```

  > element.removeAttributeNode(attributename)  删除指定属性节点并返回移除后的节点

- hasChildNodes()  用来检查当前元素是否含有子节点





## 三十九、DOM操作案例

### 39.1 选项卡切换

![image-20210220133237571](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20210220133237571.png)

**HTML代码**：

```
<div class="wrap">
    <!-- 导航条 -->
    <ul class="nav">
        <li>国际新闻</li>
        <li class="active">国内新闻</li>
        <li>世界杯</li>
    </ul>

    <!-- 导航条对应的内容部分 -->
    <div class="contents">
        <ul class="hid">
            <li>拜登与狗玩耍摔倒后去医院检查，特朗普发推：早日康复</li>
            <li>特朗普“大选日”后首次接受电视台采访：选举被操纵了</li>
            <li>美媒：特朗普已开始2024年大选竞选 或在拜登就职</li>
            <li>特朗普要给拜登“上眼药”了</li>
        </ul>

        <ul>
            <li>【话洛阳】厉害了！洛阳这个县的案例入选第二届全</li>
            <li>国合·耶鲁企业家走进长沙市恒定中学 为教育情怀</li>
            <li>大型沉浸式体验剧《十八梯龙门阵》11月28日正式上</li>
        </ul>

        <ul class="hid">
            <li>世界杯</li>
        </ul>
    </div>
</div>
```

**CSS代码**：

```
* {
    margin: 0;
    padding: 0;
}

ul {
    list-style: none;
}

.hid {
    display: none;
}

.wrap {
    width: 300px;
    margin: 100px auto;
}

.nav {
    overflow: hidden;
}

.nav>li {
    float: left;
    width: 80px;
    margin-bottom: -2px;
    padding: 6px 0;
    text-align: center;
    border: 1px solid gray;
    border-bottom: none;
    cursor: pointer;
}

.nav>li:nth-of-type(1) {
    margin-left: 8px;
}

.nav>li:nth-of-type(2) {
    margin: 0 20px;
}

.nav>li.active {
    margin-bottom: 0px;
    border-top-width: 2px;
    border-bottom: solid 2px white;
}

.contents {
    margin-top: -2px;
    padding: 10px 6px;
    line-height: 2;
    border: 1px solid #000;
    border-top-width: 2px;
}

.contents li {
    white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;
}
```

**JS代码**：

```
var navs = document.querySelectorAll(".nav>li");
var contentItems = document.querySelectorAll(".contents>ul");

for(var i = 0; i < navs.length; i++){
    console.log(i,navs[i])
    navs[i].index = i;
    navs[i].onclick = function(){
        // console.log(this.innerHTML)
        for(var j = 0; j < navs.length; j++){
            // navs[j].setAttribute('class',"")
            navs[j].removeAttribute('class')
            contentItems[j].setAttribute('class',"hid")
        }

        this.setAttribute("class","active");
        console.log(i,this.index)
        contentItems[this.index].removeAttribute('class');
    }
}
console.log(i)
```



### 39.2 评论系统

![image-20210220133849258](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20210220133849258.png)

**HTML代码**：

```
<pre>
1. 点击发送按钮，获取输入框中的值，将其提交到评论区
2. 点击每一天评论内容右侧的 X，可以删除当前行内容
3. 添加和删除的过程中，消息数量动态改变
4. 添加和删除过程中，实现评论信息的隔行变色效果
</pre>
<div class="container">
    <h2>消息数量：<span id="num">1</span></h2>
    <ul class="articals">
        <li>您好！世界！<span class="removebtn">&times;</span></li>
    </ul>
    <textarea name="" id="ipt" placeholder="请输入您的评论..."></textarea>
    <button id="sendbtn">发送</button>
</div>
```

**CSS代码**：

```
*{margin: 0;padding: 0;}
ul,ol{list-style: none;}
.container{
    width: 1000px;
    padding: 15px;
    background-color: #E7E7E7;

    position: fixed;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
}

.articals{
    margin: 10px 0 40px;
    padding: 4px;
    border: 1px solid pink;
}

.articals li{
    padding: 4px;
}

.articals li:nth-child(odd){
    background-color: yellowgreen;
}

.removebtn{
    float: right;
    cursor: pointer;
}

#ipt{
    width: 100%;
    height: 80px;
}

#sendbtn{
    padding: 2px 8px;
    cursor: pointer;
}
```

**JS代码**：

```
// 获取相关元素
var ipt = $("#ipt"),
    sendBtn = $("#sendbtn"),
    articals = $(".articals"),
    num = $("#num");

// 监听发送按钮的点击事件
sendBtn.onclick = function(){
    // 获取输入框中的值，并提交到评论区
    var iptVal = ipt.value.trim();
    // 判断
    if(!iptVal)  return;
    // 创建元素写入内容
    var item = document.createElement('li');
    item.innerHTML = iptVal + '<span class="removebtn">&times;</span>';
    articals.appendChild(item);
    // 消息数量递增
    num.innerHTML++;
    // 清空输入框
    ipt.value = ""
    // 调用高亮
    // highLight()
    // 删除操作
    removeItem()
}

// 删除操作
removeItem()
function removeItem(){
    var removebtns = document.getElementsByClassName('removebtn');
    for(var i = 0; i < removebtns.length; i++){
        removebtns[i].onclick = function(){
            this.parentNode.remove()
            //消息数量递减
            num.innerHTML--;
        }
    }
}

// 高亮显示
// highLight()
// function highLight(){
//     var items = document.querySelectorAll(".articals>li");
//     // console.dir(items)
//     for(var i = 0; i < items.length; i++){
//         // console.log(items[i])
//         if(i % 2 == 0){
//             items[i].style.backgroundColor = "greenyellow"
//         }
//     }
// }

// 封装通过选择器获取元素的方法
function $(selector){
    // querySelectorAll() 匹配所有符合条件的元素
    // querySelector()  获取的是符合条件的第一个元素
    return document.querySelector(selector);
}
```



### 39.3 微博评论

![image-20210220134019824](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20210220134019824.png)

**HTML代码**：

```
<div class="container">
    <fieldset>
        <legend>发表评论</legend>
        <input type="text" placeholder="输入账号" id="account" class="my-block">
        <textarea name="" id="artical" placeholder="请输入评论内容" class="my-block artical"></textarea>
        <button id="commitbtn" class="btn">提交</button>
    </fieldset>
    <div class="contents">
        <div class="title">
            <span>评论</span>
            <button id="clearInfo" class="btn">清空信息</button>
        </div>
        <ul class="articals">
            <!-- <li>
                <h3>Jack</h3>
                <p>的萨拉分解机啊撒旦发生了的发射点发射点上的飞机哈士大夫</p>
                <time>2021/1/15 14:33:45</time>
                <button class="btn" style="float: right;">删除</button>
            </li> -->
        </ul>
    </div>
</div>
```

**CSS代码**：

```
* {
    margin: 0;
    padding: 0;
}

li {
    list-style: none;
}

.container {
    width: 1200px;
    margin: 20px auto;
}

fieldset {
    padding: 16px;
}

.my-block {
    display: block;
    width: 100%;
    margin: 20px 0;
    outline: none;
}

.artical {
    height: 80px;
}

.btn {
    width: 84px;
    height: 30px;
    line-height: 30px;
    color: white;
    outline: none;
    border: none;
    border-radius: 20px;
    background-color: rgb(14, 13, 13);
    cursor: pointer;
    align-self: center;
}

.title {
    display: flex;
    justify-content: space-between;
    height: 40px;
    background-color: gray;
}

.title span {
    display: block;
    margin-left: 10px;
    padding: 4px 10px;
    align-self: flex-end;
    background-color: white;
}

.articals {
    margin-top: 10px;
    padding: 10px;
    line-height: 1.6;
    border: 1px solid #000;
}

.articals li {
    padding: 6px;
    border-bottom: dotted 1px gray;
}
```

**JS代码**：

```
// 获取相关元素、
var commitbtn = document.getElementById('commitbtn');
var account = document.getElementById('account');
var artical = document.getElementById('artical');
var clearInfo = document.getElementById('clearInfo');
var articals = document.querySelector('.articals')

// 设置提交按钮的点击事件
commitbtn.onclick = function () {
    // 获取输入框中的内容
    var accountVal = account.value.trim();
    var articalVal = artical.value.trim();

    if (!accountVal && !articalVal) {
        alert("账号和内容不能为空")
    } else {
        var li = document.createElement('li');
        li.innerHTML = `<h3>${accountVal}</h3>
                <p>${articalVal}</p>
                <time>${formatdate()}</time>
                <button class="btn delItem" style="float: right;">删除</button>`;
        articals.appendChild(li);

        // 清空输入框
        clear();

        // 删除单个函数
        removeItem()
    }
}

// 清除全部信息
clearInfo.onclick = function(){
    if(!articals.hasChildNodes)  return;
    articals.innerHTML = "";
}

// 删除一条数据函数
function removeItem() {
    var delBtns = document.querySelectorAll(".delItem");
    // console.log(delBtns)
    for(var i = 0; i < delBtns.length; i++){
        delBtns[i].onclick = function(){
            this.parentNode.remove()
        }
    }
}

// 清空输入框的方法
function clear() {
    account.value = artical.value = ""
}

// 获取当前时间并进行格式化输出  "2019年05月01日 星期六 13时:06分:01秒"
function formatdate() {
    var date = new Date();
    var year = date.getFullYear();
    var month = date.getMonth() + 1 < 10 ? "0" + (date.getMonth() + 1) : date.getMonth() + 1;
    var theDate = date.getDate() < 10 ? "0" + date.getDate() : date.getDate();
    var hour = date.getHours() < 10 ? "0" + date.getHours() : date.getHours();
    var min = date.getMinutes() < 10 ? "0" + date.getMinutes() : date.getMinutes();
    var second = date.getSeconds() < 10 ? "0" + date.getSeconds() : date.getSeconds();
    return year + "/" + month + "/" + theDate + "/\t" + hour + ":" + min + ":" +
        second;
}
```



### 39.4 购物车

![image-20210220134257711](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20210220134257711.png)

**HTML代码**：

```
<table id="shopping">
    <thead>
        <th width="60"><input type="checkbox" name="" id="checkAll" class="checkAll" value="" /> 全选</th>
        <th width="300">商品</th>
        <th width="80px">单价</th>
        <th width="120px">数量</th>
        <th width="180px">小计</th>
        <th width="60px">操作</th>
    </thead>
    <tbody>
        <!--<tr>
            <td><input type="checkbox" name="" id="" class="checkItem" value="" /></td>
            <td>
                <img src="img/1.jpg" class="shopping-show"/>
                <span class="shopping-des">Casio/卡西欧 EX-TR350</span>
            </td>
            <td class="shopping-price" width="80px">6999.99</td>
            <td class="shopping-count" width="120px">
                <div>
                    <span class="shopping-reduce">-</span>
                    <input type="text" name="" id="" class="shopping-input" value="1" />
                    <span class="shopping-add">+</span>
                </div>
            </td>
            <td class="shopping-subtotal" width="180px">6999.99</td>
            <td class="shopping-remove" width="60px">删除</td>
        </tr>-->
    </tbody>
</table>
<div id="shopping-foot">
    <span class="removeSlt shopping-remove">删除选中商品</span>
    <span>已选中<strong class="sltCount"> 0 </strong>件商品</span>
    <span>合计:￥<strong class="totalPrices"> 0 </strong>元</span>
    <span class="account-colse" style="margin-left: 400px;cursor:pointer;background: #E2E4E6;padding: 8px;">结算</span>
</div>
```

**CSS代码**：

```
* {
	margin: 0;
	padding: 0;
}



table#shopping {
	/*width: 800px;*/
	margin: 60px 100px 30px;
	text-align: center;
	border: solid 1px;
	border-collapse: collapse;
}

table thead{
	background: #FFA500;
}

table#shopping th,
table#shopping td {
	padding: 6px;
	border: solid 1px;
}

table#shopping img {
	width: 80px;
	height: 60px;
	vertical-align: middle;
}

.shopping-des {
	display: inline-block;
	width: 200px;
}

.shopping-count div {
	display: flex;
	justify-content: center;
}

.shopping-count span,
.shopping-count input {
	display: block;
	width: 30px;
	height: 26px;
	margin-left: -1px;
	/*padding: 2px;*/
	border: solid 1px;
	background: #E7E7E7;
}

.shopping-count input {
	width: 50px;
	background: white;
	text-align: center;
}

.shopping-count span {
	cursor: pointer;
}

.shopping-remove:hover {
	color: red;
	cursor: pointer;
	text-decoration: underline;
}

/*隔行变色*/
.oddbg {
	background: pink;
}

.evenbg {
	background: #E7E7E7;
}

.hoverbg {
	background: #EEE8AA;
}

#shopping-foot{
	margin:0 100px;
}

#shopping-foot span{
	margin-left: 20px;
}
```

**JS代码**：

```
//获取元素
var table = document.querySelector('table')
var tbody = table.querySelector('tbody')
var shoppingFoot = document.getElementById('shopping-foot');
var sltCount = document.querySelector('.sltCount')
var totalPrices = document.querySelector('.totalPrices')
var arr;
var flagArr = [];

//加载数据渲染到页面
loadData();
function loadData(){
	//JSON数据
	var shoppingData = '[{"imgUrl":"img/1.jpg","des":"Casio/卡西欧 EX-TR350","price":"6999","countNum":"1"},' + 
						'{"imgUrl":"img/2.jpg","des":"Canon/佳能 PowerShot SX50 HS","price":"3999","countNum":"1"},' + 
						'{"imgUrl":"img/3.jpg","des":"Sony/索尼 DSC-WX300","price":"1699","countNum":"1"},' + 
	 					'{"imgUrl":"img/4.jpg","des":"Fujifilm/富士 instax mini 25","price":"599","countNum":"1"}]';
 					
	//将JSON数据转换成对象
	arr = JSON.parse(shoppingData);
	
	//渲染页面
	showPage();
}

//渲染页面
function showPage(){
	tbody.innerHTML = "";
	
	var str = "";
	for (var i = 0; i < arr.length; i++) {
		str += '<tr><td><input type="checkbox" name="" id="" class="checkItem" value="" index="'+i+'"/></td><td><img src="' + 
				arr[i].imgUrl + '" class="shopping-show"/><span class="shopping-des">'+ arr[i].des +
				'</span></td><td class="shopping-price" width="80px">'+ arr[i].price +
				'</td><td class="shopping-count" width="120px"><div><span class="shopping-reduce" index="'+i+'">-</span>' + 
				'<input type="text" name="" id="" class="shopping-input" index="'+i+'" value="'+arr[i].countNum +'"/><span class="shopping-add" index="'+i+'">+</span>' + 
				'</div></td><td class="shopping-subtotal" width="180px">' + (arr[i].price * arr[i].countNum).toFixed(2) + 
				'</td><td class="shopping-remove" width="60px" index="'+ i+'">删除</td></tr>'	;
	}
	
	tbody.innerHTML = str;
	
	var checks = tbody.getElementsByClassName('checkItem');
	for (var i = 0; i < arr.length; i++) {
		if(arr[i].flag){
			checks[i].checked = "checked";
		}
	}
	
	//以msg方式存储到localStorage中
	localStorage.msg = JSON.stringify(arr);
	
	//隔行变色
	chBg();
}

//利用事件委托操作删除、增减的操作
table.onclick = function(e){
	var ev = e || event;
	var t = ev.target ||ev.srcElement;
	var cls = t.className;
	switch (cls){
		case "shopping-reduce":
			console.log('商品数量减一')
			/*console.log(t.getAttribute("index"))
			console.log(arr[t.getAttribute("index")].countNum)*/
			var num = arr[t.getAttribute("index")].countNum;
			if(--num < 1){
				t.innerHTML = ""
				return;
			}
			arr[t.getAttribute("index")].countNum = num;
			
			//渲染页面
			showPage()
			totalPrice()
			break;
		case "shopping-add":
			console.log('商品数量加一')
			t.previousElementSibling.previousElementSibling.innerHTML = "-"
			arr[t.getAttribute("index")].countNum++;
			//渲染页面
			showPage()
			totalPrice()
			break;
		case "shopping-remove":
			console.log('移除当前商品')
			console.log(t.getAttribute('index'))
			arr.splice(t.getAttribute('index'),1);
			showPage();
			totalPrice()
			break;
		default:
			break;
	}
}


//利用事件委托操作全选、单选、数量的改变
var n = 0;
table.onchange = function(e){
	var ev = e || event;
	var t = ev.target ||ev.srcElement;
	var cls = t.className;
	var checkItems = this.getElementsByClassName('checkItem');
	switch (cls){
		case "checkAll":
			console.log("全选操作")
			for (var i = 0; i < checkItems.length; i++) {
				checkItems[i].checked = t.checked;
				if(checkItems[i].checked){
					n++;
				}else{
					n--;
				}
			}
			console.log(n)
			totalPrice()
			break;
		case "checkItem":
			console.log("单选操作")
			var checkAll = this.getElementsByClassName('checkAll')[0];
			if(t.checked){
				n++;
				console.log(n)
			}else{
				n--;
				checkAll.checked = t.checked;
				console.log(n)
			}
			if(n === checkItems.length){
				checkAll.checked = t.checked;
			}
			totalPrice()
			break;
		case "shopping-input":
			console.log("商品数量发生改变")
			//console.log(t.value);//string类型
			//console.log(parseInt(t.value));//number
			var count = parseInt(t.value);
			if(count < 1 || isNaN(count)){
				count = 1;
			}
			arr[t.getAttribute("index")].countNum = count++;
			showPage();
			totalPrice()
			break;
		default:
			break;
	}
}

//利用事件委托操作商品删除、结算
shoppingFoot.onclick = function(e){
	var ev = e || event;
	var t = ev.target ||ev.srcElement;
	var cls = t.className;
	switch (cls){
		case "removeSlt shopping-remove":
			console.log('删除选中商品')
			rmSlt();
			break;
		case "account-colse":
			console.log('商品结算')
			break;
		default:
			break;
	}
}



//移除选中的函数
function rmSlt(){
	var checkItems = document.getElementsByClassName("checkItem");
	//console.log(checkItems)
	
	var newArr = [];
	for (var i = 0; i < checkItems.length; i++) {
		/*if(checkItems[i].checked){
			arr.splice(i,1);
			checkItems[i].parentNode.remove();
			i--;
		}*/
		
		if(!checkItems[i].checked){
			newArr.push(arr[i])
			//console.log(arr[i])
		}
	}

	arr = newArr;
	totalPrice()
	showPage();
}


//选中商品的数量及商品总价
function totalPrice(){
	var checkItems = document.getElementsByClassName("checkItem");
	var count = 0;
	var tprice = 0;
	for (var i = 0; i < checkItems.length; i++) {
		if(checkItems[i].checked){
			count += Number(arr[i].countNum);
			tprice += Number(arr[i].countNum) * Number(arr[i].price);
			
			arr[i].flag = true;
		}else{
			arr[i].flag = false;
		}
	}
	/*console.log(count)
	console.log(tprice)*/
	
	sltCount.innerHTML = count;
	totalPrices.innerHTML = tprice.toFixed(2);
}


//隔行变色
function chBg(){
	var trs = tbody.rows;
	for (var i = 0; i < trs.length; i++) {
		if(i % 2 === 0){
			trs[i].className = "evenbg"
		}else{
			trs[i].className = "oddbg"
		}
		
		trs[i].onmouseover = function(){
			this.oldClass = this.className;
			this.className = "hoverbg"
		}
		
		trs[i].onmouseout = function(){
			this.className = this.oldClass;
		}
	}
}
```



# 拓展：

xml、json都是用来存储数据，但是xml结构看起来清晰，而json字符串结构不容易查看；但是xml不够简洁，对于计算机来说，json字符串保存数据更经济。



# 四十、事件 和 元素相关属性

事件是用户或者浏览器自身执行的某种动作，如：click、load和mouseover等，都是事件的名字；



### 40.1 窗口或元素相关事件：

| 事件     | 描述                           |
| -------- | ------------------------------ |
| onload   | 页面或图像加载完成后触发的事件 |
| onresize | 窗口发生改变时触发的事件       |
| onscroll | 窗口滚动条滚动时触发的事件     |

### 40.2 元素相关属性

| 属性                   | 描述                                                   |
| ---------------------- | ------------------------------------------------------ |
| *element*.clientHeight | 在页面上返回内容的可视高度（不包括边框，边距或滚动条） |
| *element*.clientWidth  | 在页面上返回内容的可视宽度（不包括边框，边距或滚动条） |
| *element*.offsetHeight | 返回任何一个元素的高度包括边框和填充，但不是边距       |
| *element*.offsetWidth  | 返回元素的宽度，包括边框和填充，但不是边距             |
| element.scrollTop      | 页面或元素顶部被卷去的距离                             |
| element.scrollLeft     | 页面或元素左边被卷去的距离                             |
| *element*.offsetLeft   | 返回当前元素的相对水平偏移位置的偏移容器               |
| *element*.offsetTop    | 返回当前元素的相对垂直偏移位置的偏移容器               |
| *element*.offsetParent | 返回元素的偏移容器                                     |

### 40.3 相关案例及代码：

#### 40.3.1 页面滚动指定距离后，开始计数

![image-20210120144457953](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20210120144457953.png)

![image-20210120144511755](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20210120144511755.png)

HTML代码：

```
<body style="height: 1000px;width: 3000px;">
    <div id="box">
        <p>爱神的箭房间阿里山的和法律上的就会发生阿斯兰的空间会发生拉到恢复了撒旦发生</p>
        <p>爱神的箭房间阿里山的和法律上的就会发生阿斯兰的空间会发生拉到恢复了撒旦发生</p>
        <p>爱神的箭房间阿里山的和法律上的就会发生阿斯兰的空间会发生拉到恢复了撒旦发生</p>
        <p>爱神的箭房间阿里山的和法律上的就会发生阿斯兰的空间会发生拉到恢复了撒旦发生</p>
        <p>爱神的箭房间阿里山的和法律上的就 <strong id="count" style="font-size: 30px;color: yellow;">0</strong>+会发生阿斯兰的空间会发生拉到恢复了撒旦发生
        </p>
        <p>爱神的箭房间阿里山的和法律上的就会发生阿斯兰的空间会发生拉到恢复了撒旦发生</p>
    </div>
</body>
```

CSS代码：

```
p {
    height: 100px;
    margin-top: 30px;
    background-color: orange;
}
```

JS代码（嵌入到head标签中）：

```
//var box = document.getElementById("box");
//console.log(box)

// 文档就绪或图片加载完成执行的事件
window.onload = function () {
    var box = document.getElementById("box");
    console.log(box)
    var count = document.getElementById('count');
}

// console.log(box)

// 滚动条滚动事件
var timer = null,
    timer2 = null;
// 定义锁
var flag = true;
window.onscroll = function () {
    // console.log(box)
    // 获取滚动的距离，被顶部或者左边卷去的距离
    // element.scrollTop	返回当前视图中的实际元素的顶部边缘和顶部边缘之间的距离
    // element.scrollLeft	返回当前视图中的实际元素的左边缘和左边缘之间的距离
    // console.log("被浏览器顶部卷去的距离：", document.documentElement.scrollTop)
    // console.log("被浏览器左边卷去的距离：",document.documentElement.scrollLeft)
    // var sTop = document.documentElement.scrollTop;
    // console.log(sTop)

    var sTop = document.documentElement.scrollTop;
    console.log(sTop)

    // 函数节流：解决一些高频触发事件
    clearTimeout(timer);
    timer = setTimeout(function () {
        if (sTop > 120) {
            if (flag) {
                timer2 = setInterval(function () {
                    count.innerHTML = Number(count.innerHTML) + 10;
                    if (count.innerHTML >= 100) {
                        clearInterval(timer2);
                        flag = false;
                        return;
                    }
                }, 20);
            }
        }
    }, 200);

    if (sTop <= 100) {
        flag = true;
        count.innerHTML = 0;
    }
}


window.onresize = function () {
    console.log("窗口宽度为：", window.innerWidth, "高度为：", window.innerHeight);
}
```



#### 40.3.2 指定元素内的滚动条事件

![image-20210120144416766](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20210120144416766.png)

HTML代码：

```
<div id="box">
    <p>
        撒旦洛夫将军哈四大皆空六氟化硫吉萨大和了解撒大化肥距离喀什地方老师的话法拉盛地
        撒旦洛夫将军哈四大皆空六氟化硫吉萨大和了解撒大化肥距离喀什地方老师的话法拉盛地
        撒旦洛夫将军哈四大皆空六氟化硫吉萨大和了解撒大化肥距离喀什地方老师的话法拉盛地
        撒旦洛夫将军哈四大皆空六氟化硫吉萨大和了解撒大化肥距离喀什地方老师的话法拉盛地
        撒旦洛夫将军哈四大皆空六氟化硫吉萨大和了解撒大化肥距离喀什地方老师的话法拉盛地
        撒旦洛夫将军哈四大皆空六氟化硫吉萨大和了解撒大化肥距离喀什地方老师的话法拉盛地
        撒旦洛夫将军哈四大皆空六氟化硫吉萨大和了解撒大化肥距离喀什地方老师的话法拉盛地
        撒旦洛夫将军哈四大皆空六氟化硫吉萨大和了解撒大化肥距离喀什地方老师的话法拉盛地
        撒旦洛夫将军哈四大皆空六氟化硫吉萨大和了解撒大化肥距离喀什地方老师的话法拉盛地
        撒旦洛夫将军哈四大皆空六氟化硫吉萨大和了解撒大化肥距离喀什地方老师的话法拉盛地
    </p>
</div>
<div class="scroll_info"></div>
```

CSS代码：

```
#box {
    width: 400px;
    height: 200px;
    border: 1px solid #000;
    overflow: scroll;

    /* display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 3; 
    overflow: hidden;*/
}

p{
    width: 600px;
    margin: 0;
}
```

JS代码：

```
var box = document.getElementById("box");
var scrollInfo = document.querySelector(".scroll_info");
box.onscroll = function(){
    // console.log(this.scrollTop)
    scrollInfo.innerHTML = "水平滚动条卷去的距离："+this.scrollLeft+
    						"px，垂直滚动条卷去的距离："+this.scrollTop+"px";
}
```



#### 40.3.3 小球在页面范围内的旋转移动

![f2yjo-cwmns](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/f2yjo-cwmns.gif)

HTML代码：

```
<div id="ball">球</div>
```

CSS代码：

```
#ball {
    width: 100px;
    height: 100px;
    color: white;
    /* font-size: 60px;
    font-family: "楷体";
    line-height: 100px; */
    font: bold 60px/100px "楷体";
    text-align: center;
    background-color: red;
    border-radius: 50%;

    transform: rotate(0);

    position: fixed;
    top: 0;
    left: 0;
}
```

JS代码：

```
var ball = document.getElementById("ball");

// 获取当前窗口有效区域
var aw = window.innerWidth - parseInt(getOutStyle(ball, "width"));
var ah = window.innerHeight - parseInt(getOutStyle(ball, "width"));

var count = 0;
var step = 10;
var direction = "right";
setInterval(function () {
    if (direction == "right") { //向左
        count += 10;
    } else if (direction == "left") {
        count -= 10;
    }

    var ox = parseInt(getOutStyle(ball, "left")) + step;
    if (ox >= aw) {
        ox = aw;
        step *= -1; //step = step * -1   ||  step = -step
        count = 0;
        direction = "left"
    } else if (ox <= 0) {
        ox = 0;
        step = -step;
        count = 0;
        direction = "right"
    }

    ball.style.left = ox + "px";
    ball.style.transform = "rotate(" + count + "deg)";
    console.log(count)
    // console.log(parseInt(getOutStyle(ball,"left")))
}, 100)

function getOutStyle(element, attr) {
    if (window.getComputedStyle) {
        return window.getComputedStyle(element, null)[attr];
    } else {
        return element.currentStyle[attr];
    }
}


// 窗口改变事件
window.onresize = function () {
    aw = window.innerWidth - parseInt(getOutStyle(ball, "width"));
    ah = window.innerHeight - parseInt(getOutStyle(ball, "width"));
}
```



#### 40.3.4 图片就绪事件

![image-20210120144830339](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20210120144830339.png)

HTML代码：

```
<div id="box"></div>
<canvas id="myCanvas" width="500" height="400">HTML5标签</canvas>
```

CSS代码：

```
#box{
    width: 500px;
    height: 400px;
    border: 1px solid #000;
}

#myCanvas{
    background-color: orange;
}
```

JS代码：

```
var box = document.getElementById('box');   
var img = document.createElement('img');
img.src = "./images/1.jpg"
box.style.background = "url(./images/1.jpg)";
document.body.appendChild(img);

console.log(img);//打印标签和图片路径而已  图片请求是耗时操作

var date = new Date();

// 获取画板
var myCanvas = document.getElementById("myCanvas");
// 获取画笔（上下文对象）
var ctx = myCanvas.getContext('2d');
// canvas绘制图片的方式
// ctx.drawImage(img,0,0)
// console.log(new Date() - date)
// 图片请求完成（就绪）事件、
img.onload = function(){
    console.log(new Date() - date);//观察时间差，不难发现，图片请求是耗时操作
    ctx.drawImage(img,0,0)
}
```



#### 40.3.5 利用元素属性进行小球页面范围内滚动的优化

![f2yjo-cwmns](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/f2yjo-cwmns-1611130087405.gif)

HTML代码：

```
<div id="ball">球</div>
```

CSS代码：

```
#ball {
    width: 100px;
    height: 100px;
    color: white;
    font: bold 60px/100px "楷体";
    text-align: center;
    background-color: red;
    border-radius: 50%;

    transform: rotate(0);

    position: fixed;
    top: 0;
    left: 0;
}
```

JS代码：

```
// 获取元素
var ball = document.getElementById("ball");

// 获取小球可移动最大范围
var maxX = document.documentElement.clientWidth - ball.offsetWidth;

// 定义步长值
var step = 10;

// 定义旋转角度
var degree = 0;

// 监听运动方向
var direc = 0;

// 利用间歇调用实现小球每隔一段时间的位置移动
var timer = setInterval(function () {
    // 移动之后的最新位置
    var ml = ball.offsetLeft + step;

    // 判断移动后是否超出边界
    if (ml >= maxX) {
        ml = maxX;
        step = -step;
        direc++;
        degree = 0
    } else if (ml <= 0) {
        ml = 0;
        step *= -1;
        direc++;
        degree = 0
    }

    // 每次旋转10度
    if (direc % 2 == 0) {
        degree += 10;
    }else{
        degree -= 10;
    }

    // 小球旋转
    ball.style.transform = "rotate(" + degree + "deg)";

    // 通过 style.left 设置小球最新的位置
    ball.style.left = ml + "px";
}, 100)


// 监听窗口改变事件
window.onresize = function () {
    maxX = document.documentElement.clientWidth - ball.offsetWidth;
}
```



### 40.4 鼠标事件

| 事件          | 描述                               |
| ------------- | ---------------------------------- |
| onclick       | 鼠标单击触发的事件                 |
| ondblclick    | 鼠标双击触发的事件                 |
| oncontextmenu | 鼠标右键触发的事件                 |
| onmouseover   | 鼠标滑过触发的事件                 |
| onmoseout     | 鼠标离开触发的事件                 |
| onmouseenter  | 鼠标指针移动到当前元素上触发的事件 |
| onmouseleave  | 鼠标指针移出当前元素触发的事件     |
| onmousedown   | 鼠标被按下触发的事件               |
| onmouseup     | 鼠标被松开触发的事件               |
| onmousemove   | 鼠标移动事件                       |

> **注**：
>
> 1. onmouseenter 和 onmouseleave 不支持事件冒泡；而onmouseout 和 onmouseover支持事件冒泡
> 2. mouseenter 事件只有在鼠标指针进入被选元素时被触发，mouseover事件在鼠标指针进入任意子元素时也会被触发；
> 3. mouseleave 事件只有在鼠标指针离开被选元素时被触发，mouseout事件在鼠标指针离开任意子元素时也会被触发
> 4. onclick、onmousedown、onmouseup执行的顺序   onmousedown --> onmouseup --> onclick 



### 40.5 鼠标相关案例：

#### 40.5.1 点击按钮，页面范围内随机产出色块

![image-20210120145052768](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20210120145052768.png)

HTML代码：

```
<button id="btn">点一下随机出一个</button>
```

JS代码：

```
document.getElementById('btn').onclick = function () {
    var colorBox = document.createElement("div");
    var eleWidth = getRanNum(100, 200);
    var eleHeight = getRanNum(200, 300);
    var maxX = document.documentElement.clientWidth - eleWidth;
    var maxY = document.documentElement.clientHeight - eleHeight;
    console.log("colorBox:",colorBox,"eleWidth:",eleWidth,"eleHeight:",eleHeight,"maxX:",maxX,"maxY:",maxY)
    colorBox.style.cssText = `width:${eleWidth}px;height:${eleHeight}px;background-color:${getRanColor()};
                            position:fixed;left:${getRanNum(0,maxX)}px;top:${getRanNum(0,maxY)}px`;
    document.body.appendChild(colorBox)
}


// 获取两个数字之间的随机数
function getRanNum(a, b) {
    if (a > b) {
        return Math.round(Math.random() * (a - b)) + b;
    } else {
        return Math.round(Math.random() * (b - a)) + a;
    }
}

// 获取随机颜色  十六进制 0-9a-f    RGB 0-255     英文字母
function getRanColor() {
    var r = Math.round(Math.random() * 255);
    var g = Math.round(Math.random() * 255);
    var b = Math.round(Math.random() * 255);
    return "rgb(" + r + "," + g + "," + b + ")";
}
```



#### 40.5.2 在点击位置生成随机大小色块

![image-20210120145208304](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20210120145208304.png)

JS代码：

```
document.onclick = function (e) {
    console.log(e)
    // 事件对象的兼容性写法
    var ev = e || event;
    var colorBox = document.createElement("div");
    var eleWidth = getRanNum(100, 200);
    var eleHeight = getRanNum(200, 300);
    var maxX = document.documentElement.clientWidth - eleWidth;
    var maxY = document.documentElement.clientHeight - eleHeight;
    // 获取鼠标点击的位置
    var ml = ev.clientX - eleWidth/2;
    var mt = ev.clientY - eleHeight/2;
    console.log("colorBox:",colorBox,"eleWidth:",eleWidth,"eleHeight:",eleHeight,"maxX:",maxX,"maxY:",maxY)
    colorBox.style.cssText = `width:${eleWidth}px;height:${eleHeight}px;background-color:${getRanColor()};
                            position:fixed;left:${ml}px;top:${mt}px`;
    document.body.appendChild(colorBox)
}


// 获取两个数字之间的随机数
function getRanNum(a, b) {
    if (a > b) {
        return Math.round(Math.random() * (a - b)) + b;
    } else {
        return Math.round(Math.random() * (b - a)) + a;
    }
}

// 获取随机颜色  十六进制 0-9a-f    RGB 0-255     英文字母
function getRanColor() {
    var r = Math.round(Math.random() * 255);
    var g = Math.round(Math.random() * 255);
    var b = Math.round(Math.random() * 255);
    return "rgb(" + r + "," + g + "," + b + ")";
}
```



### 40.6 键盘事件

| 事件       | 描述                                           |
| ---------- | ---------------------------------------------- |
| onkeydown  | 键盘按键被按下触发的事件                       |
| onkeyup    | 键盘按键被松开触发的事件                       |
| onkeypress | 键盘按键（数字和字母）被按下并松开时触发的事件 |

> **注**：
>
> 1. 三个键盘事件触发的顺序  onkeydown --> onkeypress --> onkeyup
> 2. keypress 主要用来接收字母、数字等ANSI字符，箭头键和功能键不能被触发，如：Alt、Ctrl、Shift、Esc 等功能键
> 3. keydown和keyup事件可以处理任何不被keypress识别的击键。诸如：功能键（F1-F12），编辑键、定位键以及任何这些键和键盘换档键的组合键



### 40.7 键盘事件案例：仿下拉列表

![xv4f7-wm578](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/xv4f7-wm578.gif)

HTML代码：

```
<div id="con">
    <span id="tit">请选择户籍所在地</span>
    <ul id="sltAll">
        <li>厦门</li>
        <li>重庆</li>
        <li>成都</li>
        <li>深圳</li>
        <li>沧州</li>
    </ul>
</div>
```

CSS代码：

```
*{margin: 0;padding: 0;}

#con{
    box-sizing: border-box;
    width: 180px;
    height: 26px;
    margin: 100px auto;

    position: relative;
}

#tit{
    display: block;
    padding: 0 5px;
    color: gray;
    line-height: 26px;
    border: solid 1px black;

    cursor: pointer;
}

#con::after{
    content: "";
    border: solid 8px transparent;
    border-top-color: skyblue;
    border-bottom: none;

    position: absolute;
    right: 10px;
    top: 13px;
    transform: translateY(-50%);
}


#sltAll{
    box-sizing: border-box;
    width: 100%;
    line-height: 2;
    list-style: none;
    border: solid 1px;

    position: absolute;
    top: 27px;
    left: 0px;

    display: none;
}

#sltAll li{
    padding: 0 5px;
    cursor: pointer;
}

#sltAll li:hover{
    background-color: #e3e3e3;
}
```

JS代码：

```
// 获取相关元素
var tit = document.getElementById("tit");
var sltAll = document.getElementById("sltAll");
var citys = sltAll.getElementsByTagName("li");

// 设置初始索引
var cutIndex = -1;

// 设置点击事件
tit.onclick = function(e){
    // 获取事件对象的兼容
    var ev = e || event;

    // 阻止事件冒泡
    ev.stopPropagation();

    sltAll.style.display = "block";

    // 设置键盘事件 判断是 ↑ keyCode 38 === key ArrowUp  ↓ - keyCode 40 === key ArrowDown
    // 回车  keyCode 13 === key Enter
    document.onkeydown = function(){
        // 阻止默认事件
        event.preventDefault();

        // console.log(event.keyCode, "===" ,event.key);
        // 获取keyCode码 或者 key的值
        var codeVal = event.keyCode;

        for(var i = 0; i < citys.length; i++){
            citys[i].removeAttribute("style");
        }

        // 根据按下的 ↑ ↓ 回车 完成指定的功能
        switch(codeVal){
            case 38:
                // 匹配上箭头 ↑
                cutIndex--;

                if(cutIndex < 0){
                    cutIndex = citys.length - 1;
                }

                citys[cutIndex].style.backgroundColor = "#E3E3E3";

                break;
            case 40:
                // 匹配下箭头 ↓
                cutIndex++;

                if(cutIndex >= citys.length){
                    cutIndex = 0;
                }

                citys[cutIndex].style.backgroundColor = "#E3E3E3";

                break;
            case 13:
                // 匹配回车键
                // console.log(citys[cutIndex].innerHTML);

                tit.innerHTML = citys[cutIndex].innerHTML;
                sltAll.style.display = "none";

                break;
            default:
                console.log("请按上下箭头和回车键....")
                break;
        }
    }

    // 设置每一个li点击事件
    for(var i = 0; i < citys.length; i++){
        citys[i].onclick = function(){
            // console.log(this.innerHTML);
            tit.innerHTML = this.innerHTML;
        }
    }

    // console.log("1111")
}

// 点击文档的任何位置 隐藏城市列表
document.onclick = function(){
    sltAll.style.display = "none";

    // console.log("22222")
}
```



### 40.8 表单事件

| 事件     | 描述                           |
| -------- | ------------------------------ |
| onfocus  | 获取表单控件的焦点             |
| onblur   | 失去表单控件的焦点             |
| oninput  | 获取用户在控件中正在输入的事件 |
| onchange | 获取表单发生改变的事件         |
| onselect | 表单中内容被选中的事件         |
| onsubmit | 表单提交事件                   |
| onreset  | 表单信息重置事件               |

> 注：onsubmit、onreset 事件由 form 元素驱动



### 40.9 表单事件案例

#### 40.9.1 二级联动

![hxkjd-nknpn](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/hxkjd-nknpn.gif)

HTML代码：

```
<select name="" id="city">
    <option value="">请选择城市</option>
    <option value="">厦门</option>
    <option value="">重庆</option>
</select>
<select name="" id="region">
    <option value="">请选择行政区域</option>
</select>
```

JS代码：

```
var citys = document.getElementById('city')
var region = document.getElementById('region')
var regions = [["请选择行政区域"],["湖里区","思明区","集美区"],['江北区',"渝中区","渝北区"]]

citys.onchange = function(){
    console.log(citys.selectedIndex)
    console.log(regions[citys.selectedIndex])

    var regionArr = regions[citys.selectedIndex];
    region.innerHTML = ""
    var option = document.createElement('option')
    option.innerHTML = "请选择行政区域"
    region.appendChild(option)

    for (var i = 0; i < regionArr.length; i++) {
        var option = document.createElement('option')
        option.innerHTML = regionArr[i]
        region.appendChild(option)
    }
}
```



#### 40.9.2 三级联动

![23ggu-ssgy6](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/23ggu-ssgy6.gif)



#### 40.9.3 输入剩余可输入字数（检测中英文输入法）

* 拓展：实现中文输入法下，仅在选词后触发 input 事件

* 描述：在使用 oninput 监控输入框内容变化时，我们期望仅在 value 值变化时，才触发 oninput 事件，而在中文输入下，未选词时的按键也会触发 oninput 事件。

* 两个事件：

  * compositionstart 事件
  * compositionend 事件

  > MDN事件描述与案例：https://developer.mozilla.org/zh-CN/docs/Web/Events/compositionstart

* 实现方式：使用一个变量表示拼写状态，在 oninput 事件中判断是否在拼写状态，当拼写状态结束，继续执行下一步操作。

* 代码实现：

  HTML代码：

  ```
  <h2>单项数据绑定：通过修改JS中的数据，页面呈现最新修改的数据信息。这是一种映射关系，把JS数据的变化映射到DOM结构上</h2>
  <div id="box">数据单项绑定呈现位置</div>
  <input type="text" id="ipt">
  ```

  JS代码：

  ```
  // 获取元素
  var box = document.getElementById("box");
  var ipt = document.getElementById("ipt");
  
  // 设置元素的内部文本
  box.innerHTML = obj.des;
  Object.defineProperty(obj,'des',{
      //赋值器
      set:function(value){
          // 当设置或修改新的值时，将最新的值输出到页面
          box.innerHTML = value;
          // 备用属性赋值
          this.oDes = value;
      },
      // 取值器
      get:function(){
          return this.oDes;
      }
  });
      
  // 定义是否开启输入法的开关 默认关闭
  var flag = false;
  //oninput在oncompositionend之前执行，需加定时器
  ipt.oninput = function(){
      this.addEventListener('compositionstart',function(){//中文开始书写
          flag = true;//检测到中文输入法开启，设为true
      })
      this.addEventListener('compositionend',function(){//中文书写完毕，选取文字完毕
          flag = false;//输入完毕，设置false
      })
      setTimeout(function() {
          if(!flag) {//保证输入法没有开启也能正常获取数据
              if(ipt.value === ""){
                  box.innerHTML = "把Model的变化映射到DOM结构上";
              }else{
                  obj.des = ipt.value;
              }
          }
      },0);
  }
  ```

  页面效果：

  ![单项数据绑定](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/单项数据绑定-1611301457311.gif)



# 四十一、事件对象

事件对象是用来记录事件发生时相关信息的对象。如: 鼠标事件发生后，获取鼠标的横坐标 event.clientX ( clientX用来获取鼠标距离浏览器左边的距离 ) 。

事件对象只有在事件被触发时才会产生，并且只能在事件处理函数内部访问；当事件处理函数运行结束后，事件对象就被销毁。



对于不同的浏览器，事件对象获取的方式不同：

- IE8及以下浏览器版本中，只能直接从全局中获取事件对象 window.event

- 火狐（Firefox，简称FF）低版本浏览器中，只能通过事件传递的方式，在事件函数中传递事件对象
- 所有高版本浏览器两者都兼容

获取事件对象的兼容性写法：

```
element["on" + 事件类型] = function(e){
	var ev = e || window.event;
}
```



事件对象通用属性：

| 属性 | 描述           |
| :--- | :------------- |
| type | 返回事件的类型 |



鼠标事件对象相关属性：

| 属性                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [clientX](https://www.runoob.com/jsref/event-clientx.html)   | 返回当事件被触发时，鼠标指针的水平坐标。                     |
| [clientY](https://www.runoob.com/jsref/event-clienty.html)   | 返回当事件被触发时，鼠标指针的垂直坐标                       |
| [screenX](https://www.runoob.com/jsref/event-screenx.html)   | 返回当某个事件被触发时，鼠标指针的水平坐标。                 |
| [screenY](https://www.runoob.com/jsref/event-screeny.html)   | 返回当某个事件被触发时，鼠标指针的垂直坐标。                 |
| [pageX](https://developer.mozilla.org/zh-cn/docs/web/api/mouseevent/pagex) | 鼠标相对于浏览器（这里说的是浏览器的有效区域）左上角x轴的坐标；  随滚动条滚动而改变 |
| [pageY](https://developer.mozilla.org/zh-cn/docs/web/api/mouseevent/pagey) | 鼠标相对于浏览器（这里说的是浏览器的有效区域）左上角y轴的坐标；  随滚动条滚动而改变 |
| [offsetX](https://developer.mozilla.org/zh-CN/docs/Web/API/MouseEvent/offsetX) | 鼠标相对于事件源左上角X轴的坐标                              |
| [offsetY](https://developer.mozilla.org/zh-CN/docs/Web/API/MouseEvent/offsetY) | 鼠标相对于事件源左上角Y轴的坐标                              |



键盘事件对象相关属性：

| 属性                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [key](https://www.runoob.com/jsref/event-key-key.html)       | 在按下按键时返回按键的标识符                                 |
| [keyCode](https://www.runoob.com/jsref/event-key-keycode.html) | 返回onkeypress事件触发的键的值的字符代码，或者 onkeydown 或 onkeyup 事件的键的代码 |
| [which](https://www.runoob.com/jsref/event-key-which.html)   | 返回onkeypress事件触发的键的值的字符代码，或者 onkeydown 或 onkeyup 事件的键的代码 |

> 注：`onkeypress` 事件触发的键的值的字符代码(表示ASCII字符的数字)，或者 `onkeydown` 或 `onkeyup` 事件的键的代码(表示键盘上真实键的数字)。



# 四十二、事件处理程序

事件处理程序指的是当HTML中发生某些事件时所调用的方法。

事件处理程序分为以下几种：

1. **HTML事件处理程序**

   直接在html元素中使用"on"+事件类型实现，如：onclick ，使得html元素具有能够执行js 代码的特性

   这种事件处理程序有两个缺点：

   - 存在一个时差的问题，如果将 script 程序写在页面的最底部，而用户又在 html 元素一出现就触发相应的事件，这个时候事件处理程序有可能尚不具备执行条件（即：script 程序未加载，dom 从上往下依次解析html 文件）
   - html 代码与 JS 代码紧密耦合，这样在维护或修改时需要修改两个地方。所以建议摒弃 html 事件处理程序，进而使用 JS 指定事件处理程序

2. **DOM0级事件处理程序**

   通过 JS 指定事件处理程序的传统方式，就是将一个函数赋值给一个事件处理程序属性。这种操作简单且具有跨浏览器的优势。

   - 使用DOM0级方法指定的事件处理程序被认为是元素的方法；因此这时候的事件处理程序是在元素的作用域中运行；即：程序中的this引用的是当前元素
   - 这种方式添加的事件处理程序会在事件流的冒泡阶段被处理

   > 添加方式：element['on' + 事件类型] = function(){}
   >
   > 移除方式：element['on' + 事件类型] = null

3. **DOM2级事件处理程序**

   > 添加方式：element.addEventListener(type,handler,boolean) 
   >
   > 移除方式： element.removeEventListener(type,handler,boolean)  
   >
   > 注意：移除时三个对应参数事件类型、事件函数、事件冒泡或捕获阶段要一一对应，匿名函数没有办法被移除。

   IE8及以下浏览器报错： 对象不支持 “`addEventListener`” 属性或方法；

   可以给同一个元素定义多个同种类型的事件函数；

   第三个参数默认是false，事件冒泡流阶段。多个同种类型的事件，按照渲染顺序，依次执行。

4. **IE事件处理程序**

   > 添加方式：element.attachEvent(‘on’+事件类型,事件函数)
   >
   > 移除方式：element.detachEvent(‘on’+事件类型,事件函数)
   >
   > 只能在IE10及以下浏览器版本中使用，其它浏览器报错：btn.attachEvent is not a function
   >
   > 也可以添加多个同种类型的事件，执行顺序按照渲染顺序逆向执行。

   与DOM0级方法的区别在于事件处理程序的作用域不同:DOM0级是在其所属元素的作用域内运行，而IE事件处理程序是在全局作用域运行，因此this等于window。

   与DOM2级方法一样，可以为同一个按钮添加两个不同事件处理程序，但是IE事件处理程序的执行顺序是以相反的顺序触发，即先触发的是后面添加的事件。

   使用detachEvent()来移除通过attachEvent()方法添加的事件，与DOM2级方法一样，匿名函数无法被移除

   

**添加事件的事件处理程序兼容性代码：**

```
function addEvent(elem, type, fn) {
    if (elem.addEventListener) { //支持DOM2
        elem.addEventListener(type, fn);
    } else if (elem.attachEvent) { //IE8及以下
        elem.attachEvent('on' + type, fn)
    } else {
        elem['on' + type] = fn
    }
}
```

**移除事件的事件处理程序兼容性代码**：

```
function removeEvent(elem, type, fn) {
    if (elem.removeEventListener) {
        elem.removeEventListener(type, fn)
    } else if (elem.detachEvent) {
        elem.detachEvent("on" + type, fn)
    } else {
        elem["on" + type] = null
    }
}
```

**添加和移除事件处理程序的兼容性代码：**

```
var oEvent = {
        /**
         * 添加事件的函数
         * @elem 添加事件的元素
         * @type 事件类型
         * @fn  事件执行函数
         * */
        addEvent: function (elem, type, fn) {
            if (elem.addEventListener) {
                elem.addEventListener(type, fn);
            } else if (elem.attachEvent) {
                elem.attachEvent('on' + type, fn)
            } else {
                elem["on" + type] = fn;
            }
        },
        /**
         * 添加事件的函数
         * @elem 添加事件的元素
         * @type 事件类型
         * @fn  事件执行函数
         * */
        removeEvent: function (elem, type, fn) {
            if (elem.removeEventListener) {
                elem.removeEventListener(type, fn)
            } else if (elem.detachEvent) {
                elem.detachEvent("on" + type, fn)
            } else {
                elem["on" + type] = null
            }
        },
        /**
         * 定义一个函数，元素只能执行一次事件；如：点击事件，第一次点击有效，第二次点击无效
         * */
        once: function () {

        }
}
```





# 四十三、事件流

事件流用来描述从页面中接收事件的顺序。

事件流分为两种：事件冒泡流和事件捕获流。这两种事件流的概念几乎完全相反。

事件流出现的前提：嵌套元素中定义了同种类型的事件。

事件捕获流只能通过 DOM2 级事件处理程序实现



### 43.1 事件冒泡流

IE事件流叫做事件冒泡，即事件最开始由最具体的元素(文档中嵌套层次最深的那个节点)接收，然后逐级向上传播至最不具体的那个节点(文档);也就是说一个标签元素处理完事件之后，它的父元素、父元素的父元素也都会处理事件(从内到外)。



### 43.2 事件捕获流

Netscape(网景)的事件流叫做事件捕获，不太具体的节点(最外层标签)应该更早接收到事件，而最具体的节点(最内层标签)最后接收到事件(事件执行的顺序是从外到内)；由于老版本浏览器不支持，因此很少有人使用事件捕获。建议大家放心地使用事件冒泡，在有特殊需要时再使用事件捕获。

DOM2级事件处理程序添加事件   element.addEventListener(type, callbackfn, boolean)，第三个参数boolean是一个布尔值，默认是false，表示绑定到冒泡阶段，如果是true则表示绑定到捕获阶段。



### 43.3 阻止事件冒泡或事件捕获的兼容代码

```
if(ev.stopPropagation){//DOM推荐标准
    ev.stopPropagation()
}else{//兼容IE678
    ev.cancelBubble = true;
}
```

> IE8及以下浏览器：对象不支持“stopPropagation”属性或方法



### 43.4 阻止元素默认行为的兼容性代码：

> 只有有默认行为的对象，才有阻止的必要性。如：页面鼠标右键事件、a标签href链接、img标签中的src请求等等....

```
// 兼容性写法
if (event.preventDefault) {//dom标准写法
    event.preventDefault()
} else {//兼容IE678
    event.returnValue = false;
}

// 利用return false也能阻止默认行为,没有兼容问题(只限传统注册方式DOM0级事件处理程序)
```

> 对象不支持 “preventDefault” 属性或方法



### 43.5 事件代理

事件代理也叫事件委托。利用事件冒泡机制，给父元素指定一个事件处理程序，就可以管理父元素及其后代元素某一类型的所有事件；如:子元素要触发的事件交由父元素代为触发执行。

1. **为什么要用事件委托?**

   一般来说，dom需要有事件处理程序，我们都会直接给它设事件处理程序就好了，那如果是很多的dom需要添加事件处理呢？比如我们有100个li，每个li都有相同的click点击事件，可能我们会用for循环的方法，来遍历所有的li，然后给它们添加事件，那这么做会存在什么影响呢？

   - 操作DOM次数过多，造成浏览器的重排和重绘就越多；
     在JavaScript中，添加到页面上的事件处理程序数量将直接关系到页面的整体运行性能，因为需要不断的与dom节点进行交互，访问dom的次数越多，引起浏览器重绘与重排的次数也就越多，就会延长整个页面的交互就绪时间，这就是为什么性能优化的主要思想之一就是减少DOM操作的原因；如果要用事件委托，就会将所有的操作放到js程序里面，与dom的操作就只需要交互一次，这样就能大大的减少与dom的交互次数，提高性能；

   - 每个事件都是一个对象，事件处理程序越多，占用的内存越多，影响前端性能；每个函数都是一个对象，是对象就会占用内存，对象越多，内存占用率就越大，自然性能就越差了（内存不够用，是硬伤，哈哈）比如上面的100个li，就要占用100个内存空间，如果是1000个，10000个呢，那只能说呵呵了，如果用事件委托，那么我们就可以只对它的父级（如果只有一个父级）这一个对象进行操作，这样我们就需要一个内存空间就够了，是不是省了很多，自然性能就会更好。

     

2. **事件委托（事件代理）原理**

   对“事件处理程序过多”问题的解决方案就是事件委托，事件委托利用事件冒泡（从最深的节点开始，然后逐步向上传播事件）只在他们的父素上指定一个事件处理程序，就可以管理某一类型的的所有事件。这就是事件委托，委托它们父级代为执行事件。

   

3. **事件委托的实现:查找事件源**，IE和DOM事件处理程序获取方式如下：

   - DOM中的事件对象：事件对象.target 		获取事件目标（事件源）

   - IE中的事件对象：  事件对象.srcElement   获取事件目标（事件源）

   - 获取事件目标兼容性写法：

     ```
     element["on"+事件类型] = function(e){
         var ev = e || event;
         //获取目标对象
         //支持DOM事件的浏览器使用target来获取事件目标
         //IE8及以前版本浏览器通过srcElement来获取事件目标
         var target = ev.target || ev.srcElement; 
     }
     ```

     

4. **事件委托的使用场景**

   - 为DOM中的很多元素绑定相同事件；

   - 为DOM中尚不存在的元素绑定事件。

     

5. **事件委托的优点**

   - 适合事件委托的事件有：click，mousedown，mouseup，keydown，keyup，keypress
   - 减少DOM操作:减少浏览器的重绘（repaint）和重排（reflow），从而提高性能；
   - 减少内存空间的占用率，因为每一个函数都是一个对象，对象越多，内存占有率就越大，自然性能就越差，使用事件委托，只需要在其父元素中定义一个事件就可以。



# 四十四、鼠标滚轮事件

代码：

```
// 鼠标滚轮事件   
// onmousewheel  谷歌和IE8以上支持的鼠标滚轮事件；火狐浏览器不支持onmousewheel形式，无响应
// window.onmousewheel = function(e){
//     var ev = e || event;
//     console.log(ev);//WheelEvent {isTrusted: true, deltaX: -0, deltaY: 100, deltaZ: 0, deltaMode: 0, …}
//     console.log(ev.type);//mousewheel
// }

// DOMMouseScroll  只能使用DOM2级事件处理程序；火狐浏览器可以正常使用；谷歌和IE8以上不支持，无响应
// window.addEventListener("DOMMouseScroll",function(e){
//     console.log(e)
// })

// 鼠标滚轮事件的兼容性代码
window.onmousewheel = wheelHandler;
window.addEventListener('DOMMouseScroll', wheelHandler);
function wheelHandler(e) { //事件对象传参是DOM标准推荐的方式
    console.log(e)
}
```

> 注：鼠标滚轮事件的属性
>
> 1. 谷歌浏览器：属性 deltaY 垂直方向滚动的距离，滚轮向下滚动，每次滚动的距离是 100px，向上滚动，每次滚动的距离是 -100px。它是固定的值。
> 2. 谷歌浏览器、IE8以上浏览器，属性 wheelDelta 固定值 120，向下是负值 -120，向上是正值 +120
> 3. 火狐浏览器：属性 detail 固定值 3，向上是负值 -3 ，向下是正值 +3



**案例**：页面中的一张图片，鼠标滚轮向下滚动时图片缩小，向上滚动时图片放大

```
<img src="./4.jpg" alt="" id="img">
<script>
    var img = document.getElementById("img");

    img.onmousewheel = wheelHanlder;
    img.addEventListener('DOMMouseScroll',wheelHanlder)
    function wheelHanlder(e){
        e.//阻止默认事件
        //preventDefault()[dom标准写法(ie678不兼容)]
        //ie678用returnValue
        //或者利用return false也能阻止默认行为,没有兼容问题(只限传统注册方式)
        preventDefault()

        // console.log(e)
        if(e.wheelDelta){//Chrome 和 IE8↑
            e.wheelDelta > 0 ? img.width++ : img.width--;
        }else if(e.detail){
            e.detail < 0 ? img.width++ : img.width--;
        }
    }
</script>
```



# 四十五、DOM操作相关案例

1. 放大镜（商品细节展示）

   ![image-20210219171540244](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20210219171540244.png)

   HTML代码：

   ```
   <div id="demo">
       <div id="small-box">
           <div id="mark"></div>
           <div id="float-box"></div>
           <img src="macbook-small.jpg"/>
       </div>
       <div id="big-box">
           <img src="macbook-big.jpg"/>
       </div>
   </div>
   ```

   CSS代码：

   ```
   * {
       margin: 0;
       padding: 0
   }
   
   #demo {
       display: block;
       width: 400px;
       height: 255px;
       margin: 50px;
       position: relative;
       border: 1px solid #ccc;
   }
   
   #small-box {
       position: relative;
       z-index: 1;
   }
   
   #float-box {
       display: none;
       width: 160px;
       height: 120px;
       position: absolute;
       background: #ffffcc;
       border: 1px solid #ccc;
       filter: alpha(opacity=50);
       opacity: 0.5;
   }
   
   #mark {
       position: absolute;
       display: block;
       width: 400px;
       height: 255px;
       background-color: #fff;
       filter: alpha(opacity=0);
       opacity: 0;
       z-index: 10;
   }
   
   #big-box {
       display: none;
       position: absolute;
       top: 0;
       left: 460px;
       width: 400px;
       height: 300px;
       overflow: hidden;
       border: 1px solid #ccc;
       z-index: 1;;
   }
   
   #big-box img {
       position: absolute;
       z-index: 5
   }
   ```

   JS代码：

   ```
   //页面加载完毕后执行
   window.onload = function () {
       var objDemo = document.getElementById("demo");
       var objSmallBox = document.getElementById("small-box");
       var objMark = document.getElementById("mark");
       var objFloatBox = document.getElementById("float-box");
       var objBigBox = document.getElementById("big-box");
       var objBigBoxImage = objBigBox.getElementsByTagName("img")[0];
   
       objMark.onmouseover = function () {
           objFloatBox.style.display = "block"
           objBigBox.style.display = "block"
       }
   
       objMark.onmouseout = function () {
           objFloatBox.style.display = "none"
           objBigBox.style.display = "none"
       }
   
       objMark.onmousemove = function (ev) {
           var _event = ev || window.event;  //兼容多个浏览器的event参数模式
           var left = _event.clientX - objDemo.offsetLeft - objSmallBox.offsetLeft - objFloatBox.offsetWidth / 2;
           var top = _event.clientY - objDemo.offsetTop - objSmallBox.offsetTop - objFloatBox.offsetHeight / 2;
   
           if (left < 0) {
               left = 0;
           } else if (left > (objMark.offsetWidth - objFloatBox.offsetWidth)) {
               left = objMark.offsetWidth - objFloatBox.offsetWidth;
           }
   
           if (top < 0) {
               top = 0;
           } else if (top > (objMark.offsetHeight - objFloatBox.offsetHeight)) {
               top = objMark.offsetHeight - objFloatBox.offsetHeight;
   
           }
   
           objFloatBox.style.left = left + "px";   //oSmall.offsetLeft的值是相对什么而言
           objFloatBox.style.top = top + "px";
   
           var percentX = left / (objMark.offsetWidth - objFloatBox.offsetWidth);
           var percentY = top / (objMark.offsetHeight - objFloatBox.offsetHeight);
   
           objBigBoxImage.style.left = -percentX * (objBigBoxImage.offsetWidth - objBigBox.offsetWidth) + "px";
           objBigBoxImage.style.top = -percentY * (objBigBoxImage.offsetHeight - objBigBox.offsetHeight) + "px";
       }
   }
   ```

   

2. 轮播图

   - 滚动轮播图
   - 呼吸轮播图
   - 点击按钮切换图片
   - 鼠标滚动切换图片

   普通轮播图示例代码：

   ![image-20210219172105223](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20210219172105223.png)

   HTML代码：

   ```
   <div id="wrap">
       <a href="" id="link">
           <img src="img/248967.jpg" id="pic"/>
       </a>
       <div id="control">
           <span id="left"><</span>
           <span id="right">></span>
       </div>
       <ul id="btns">
           <li>1</li>
           <li>2</li>
           <li>3</li>
           <li>4</li>
           <li>5</li>
           <li>6</li>
       </ul>
   </div>
   ```

   CSS代码：

   ```
   *{
   	margin: 0;
   	padding: 0;
   }
   
   img{
   	width: 1000px;
   }
   
   /*设置整体的相对位置*/
   #wrap{
   	width: 1000px;
   	height: 562px;
   	border: solid 1px red;
   	margin:0 auto;
   	position: relative;	
   	/*溢出隐藏*/
   	overflow: hidden;
   }
   
   #control span{
   	width: 40px;
   	height: 60px;
   	display: inline-block;	
   	/*设置背景色并给其相应的透明度*/
   	background: rgba(0,0,0,0.3);
   	color: white;
   	font-size: 40px;
   	text-align: center;
   	position: absolute;
   	top: 50%;
   	/*cursor属性可规定当指向某元素之上时被显示的指针类型*/
   	cursor: pointer;/*设置指针类型为pointer 光标呈现为指示某个链接的指针（一只手） */	
   	margin-top: -40px;
   	/*设置元素不显示*/
   	display: none;
   }
   
   #left{
   	left: 50px;
   }
   
   #right{
   	right: 50px;
   }
   
   #btns{
   	position: absolute;
   	right: 30px;
   	bottom: 10px;
   }
   
   #btns li{
   	list-style: none;
   	float: left;
   	padding:5px 10px;
   	margin: 5px;
   	
   	background: white;
   	border-radius: 20px;
   }
   ```

   JS代码：

   ```
   //通过Id获取到每一个对应的标签信息
   var wrap = document.getElementById("wrap");
   var link = document.getElementById("link");
   var pic = document.getElementById("pic");
   var control = document.getElementById("control");
   var left = document.getElementById("left");
   var right = document.getElementById("right");
   
   //通过类似jquery选择器方法筛选出符合要求的集合 (查询并筛选除所有符合条件的标签)
   var lis = document.querySelectorAll("#btns li");/*H5新添加方法，参数为合法的除伪类选择器以外的其他类型选择器；返回所有符合条件的元素*/
   
   //声明一个原始数组类盛放所有需要轮播的图片
   var srcArr = ["img/248967.jpg","img/1378821834056778.jpg",'img/243654.jpg','img/243660.jpg','img/245210.jpg','img/245672.jpg'];
   //声明一个数组，存放对应原始图片数组
   var linkArr = ["img/248967.jpg","img/1378821834056778.jpg",'img/243654.jpg','img/243660.jpg','img/245210.jpg','img/245672.jpg'];
   //设置第一个图片对应的列表数字背景为红色
   lis[0].style.backgroundColor = 'red';
   
   //设置自动轮播
   //声明一个定时器
   var timer = setInterval(move,1000);
   
   //声明一个全局变量
   var i = 0;
   
   //移动的操作
   function move(){
   	i++;
   	//判断如果i的值大于数组长度，置为初始值
   	if(i > srcArr.length - 1){
   		i = 0;
   	}
   	
   	//调用图片轮播的方法
   	change(i);
   }
   
   //手动轮播
   //当鼠标划过">"、"<"导航箭头时时候执行的操作
   wrap.onmousemove = function(){
   	left.style.display = "block";
   	right.style.display = "block";
   	
   	//取消setInterval()方法设置的定时器
   	clearInterval(timer);
   }
   
   //当鼠标离开">"、"<"导航箭头时时候执行的操作
   wrap.onmouseout = function(){
   	left.style.display = "none";
   	right.style.display = "none";
   	
   	//设置定时器，离开后继续自动滚动
   	timer = setInterval(move,3000);
   }
   
   //右击按钮
   right.onclick = move;
   
   //左击按钮
   left.onclick = function(){
   	i--;
   	//左变切换到0，将i值设置为最大数量
   	if(i < 0){
   		i = srcArr.length - 1;
   	}
   	//调用图片轮播的方法
   	change(i);
   }
   
   
   //图片轮播的函数装
   function change(no){
   	pic.src = srcArr[no];
   	link.href = linkArr[no];
   	//脚步背景颜色变化
   	for(var j = 0; j < lis.length; j++){
   		lis[j].style.backgroundColor = "";
   	}
   	lis[no].style.backgroundColor = "red";
   }
   
   
   //小点轮播；给每个小点添加滑过事件
   for(var i = 0; i < lis.length; i++){
   	lis[i].index = i;//设置循环i对应的数值赋值给对应的数组的角标（从0开始的角标）
   	lis[i].onmouseover = function(){
   		change(this.index);
   	}
   }
   ```

   

3. 手风琴效果

   ![image-20210219172713397](http://121.89.192.46:8888/ganhuo/note/JavaScript.assets/image-20210219172713397.png)

   HTML代码：

   ```
   <div class="wrap">
       <img src="img/手风琴图片/t75t3yp838qnmrx7.png"/>
       <img src="img/手风琴图片/t75yr7hztrwkb5hj.png"/>
       <img src="img/手风琴图片/t75tftabcgpduzs4.png"/>
       <img src="img/手风琴图片/t7fmhk7z7ph2er3u.png"/>
       <img src="img/手风琴图片/t7j23wu7yb4bv4ttk.png"/>
       <img src="img/手风琴图片/t7vmwk4bmz3er833.png"/>
   </div>
   ```

   CSS代码：

   ```
   .wrap{
       width: 1000px;
       height: 300px;
       margin: 100px auto;
       border: dotted 4px orange;
       overflow: hidden;
       position: relative;
   }
   
   .wrap img{
       width: 750px;
       position: absolute;
   }
   ```

   JS代码：

   ```
   var imgs = document.querySelectorAll('.wrap img');
   for (var i = 0; i < imgs.length; i++) {
       if(i === 0){
           imgs[i].style.left = 0;
       }else{
           imgs[i].style.left = (i * 50 + 700) + "px"
       }
   
       imgs[i].index = i;
       imgs[i].onmouseover = function(){
           for (var j = 0; j < imgs.length; j++) {
               if(j <= this.index){
                   imgs[j].style.left = (j * 50) + "px"
               }else{
                   imgs[j].style.left = (j * 50 +700) + "px";
               }
           }
       }
   }
   ```

   

# 补充一：classList 属性

`classList` 属性返回元素的类名，作为 `DOMTokenList` 对象。该属性用于在元素中添加，移除及切换 CSS 类。

> 注：`classList` 属性是只读的，但你可以使用 add() 和 remove() 方法修改它

相关方法：

- add(class1, class2, ...)	在元素中添加一个或多个类名。如果指定的类名已存在，则不会添加

- remove(class1, class2, ...)	移除元素中一个或多个类名。如果移除不存在的类名，不会报错。

- contains(class)	返回布尔值，判断指定的类名是否存在。

- item(index)	返回元素中索引值对应的类名。索引值从 0 开始。如果索引值在区间范围外则返回 null

- toggle(class, true|false)	在元素中切换类名

  > 第一个参数为要在元素中移除的类名，并返回 false。 如果该类名不存在则会在元素中添加类名，并返回 true。 
  >
  > 第二个是可选参数，是个布尔值用于设置元素是否强制添加或移除类，不管该类名是否存在（部分低版本浏览器不支持）

