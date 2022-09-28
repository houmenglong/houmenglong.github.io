# HTML5 知识点



------



主讲：**MagnumHou**

微信公众号：**前端知识分享喵**

<img src="http://121.89.192.46:8888/ganhuo/weChat.png" alt="微信图片_20200601153857" style="zoom:80%;" />



------



[TOC]

------



## 前言

### 1. HTML基础

- 互联网原理
- 当前主流浏览器及其内核介绍
- HTML 是什么，超文本和文本的区别
- 网页和网站
- WEB 三大标准

### 2. 前端开发工具

- 常见的开发工具(WebStorm、VSCode、Hbuilder、Sublime)
- VSCode 下载及安装（规定使用）
- VSCode 常用快捷键介绍

### 3. HTML基本结构

- 网页文件后缀  

  - .html 或 .htm

- HTML 的基本结构

- DOCTYPE 声明

- html 标签  

  - 属性 lang 介绍

- head 标签

- meta 元信息标签

  - 字符编码介绍 
  - SEO 介绍

- body 标签 

  - 属性 bgcolor

- HTML 的注释

  ```
  <!--注释文本-->
  ```



## 一、HTML基本标签 

### 1.1 HTML基本语法

- 标签书写的语法规则
- 属性书写的语法规则

### 1.2 HTML标签分类

- 按闭合特征分类：单标签元素，双标签元素
- 按功能分类：容器级标签，文本级标签
  - 容器级标签可以简单理解为能嵌套其它所有标签的标签。 常见的容器级标签: div h ul ol dl li dt dd 等
  - 文本级标签对应容器级标签，只能嵌套文字/图片/超链接的标签。常见的文本级标签 : p span  b u i s 等

### 1.3 标题与段落标签

- h1 - h6 
- p 
- align属性 

### 1.4 图片标签

img 标签定义 HTML 页面中的图像，它的作用是为被引用的图像创建占位符。有两个必需的属性：src 和 alt。

- src   规定显示图像的 URL

  - 绝对路径：主页上的文件或目录在硬盘上真正的路径 ( URL和物理路径 )

    例如：C:\xyz\test.txt 代表了test.txt文件的盘符绝对路径

    ​			http://www.sun.com/index.htm 也代表了一个URL网络绝对路径

  - 相对路径：相对于某个基准目录的路径。包含Web的相对路径 ( HTML中的相对目录 )

    例如："./" 代表当前目录
    			"../"代表上级目录

- alt    规定图像的替代文本：

- width / height  规定图像的宽度 / 高度

### 1.5 超链接标签

a 标签定义超链接，用于从一个页面链接到另一个页面。它最重要的属性是 href 属性，用于指定超链接的地址

在所有浏览器中，链接的默认外观如下：

- 未被访问的链接带有下划线而且是蓝色的
- 已被访问的链接带有下划线而且是紫色的
- 活动链接带有下划线而且是红色的

链接使用的几种情况

- 链接到本站内的指定页面

- 链接到本站外的指定页面 

- 锚链接(当前页面 | 其它页面) 

  通过给锚点标签设置 id 值，a 标签通过 href 进行锚定



### 1.6 废弃标签与语义标签

- 废弃标签：加粗 / 斜体 / 删除线 / 下划线标签  b / i  / s / u
- 强调标签： strong 加粗 / em 斜体
- 语义标签： del 删除 / ins 下划线

> **注**：i 和 b 是物理元素，em 和 strong 是逻辑元素。物理元素说白了就是告诉浏览器我应该如何显示以什么样的格式显示文字，而这些逻辑元素要告诉浏览器这些文本有着什么样的重要性。 在定义中 em 表示对文本进行强调-----即把文本定义为强调的内容。strong 表示表示更为重要的强调，他在语气上表示为更强烈的语气。这两者都是用于强调内容,但是 strong 的语气上更加的强烈，程度上也更加深刻。

### 1.7 其它标签

- 换行标签
- 水平线标签 属性 size  width  color  align

### 1.8 实体字符

```
&nbsp;  空格
&copy;  版权
&gt;    大于号
&lt;    小于号
&yen;   人民币
&times; 删除
```



## 二、列表

### 2.1 无序列表 ul > li

- type = disc ( 实心圆 ) | circle ( 空心圆 ) | square ( 实心方块 )     指定列表项目符号

### 2.2 有序列表 ol > li

- type = 1 | a | A | i | I     指定列表项目符号
- start = number  指定列表项目符号从第几项开始
- reversed 指定列表项目符号倒叙排列；布尔型属性

### 2.3 自定义列表 dl > dt + dd

```
<dl>
    <dt>列表标题1</dt>
    <dd>列表内容11</dd>
    <dd>列表内容12</dd>
    ...
    <dt>列表标题n</dt>
    <dd>列表内容n1</dd>
    <dd>列表内容n2</dd>
</dl>
```

### 2.4 列表嵌套



## 三、表格 

### 3.1 表格基本结构 

一个 HTML 表格包括 table 元素，一个或多个 tr 、th 以及 td 元素

- table  表格标签

- tr  行标签

- td / th  单元格 / 表头单元格标签

  

### 3.2 表格区域划分 

thead、tfoot 以及 tbody 元素使您有能力对表格中的行进行分组。当您创建某个表格时，您也许希望拥有一个标题行，一些带有数据的行，以及位于底部的一个总计行。这种划分使浏览器有能力支持独立于表格标题和页脚的表格正文滚动。当长的表格被打印时，表格的表头和页脚可被打印在包含表格数据的每张页面上。

它们的出现次序是：thead、tfoot、tbody，这样浏览器就可以在收到所有数据前呈现页脚了。



### 3.3 表格添加标题 

- 通过标题标签 ( h1 - h6 )

- 通过 caption 标签 

  

### 3.4 属性介绍 

- **table 标签属性**
  - border  规定表格单元是否拥有边框
  - width / height   规定表格的宽度 / 高度。HTML5 不支持。
  - cellpadding  规定单元格边沿与其内容之间的空白。HTML5 不支持。
  - cellspacing   规定单元格之间的空白。HTML5 不支持。
  - align  规定表格相对周围元素的对齐方式。 HTML5 不支持。属性值：left  center  right
- **td 标签属性** 
  - width / height   规定单元格的宽度 / 高度。HTML5 不支持。 
  - align  规定单元格内容的水平对齐方式。HTML5 不支持。属性值有left  center  right  justify
  - valign  规定单元格内容的垂直排列方式。HTML5 不支持。属性值有 top  middle  bottom
  - rowspan  设置单元格可横跨的行数。行合并，上下相邻单元格合并。
  - colspan  规定单元格可横跨的列数。列合并，左右相邻单元格合并。



## 四、表单

![image-20201118142937124](http://121.89.192.46:8888/ganhuo/note/HTML基础表格表单.assets/image-20201118142937124.png)

### 4.1 表单简介和使用场景 

HTML 表单用于接收不同类型的用户输入，用户提交表单时向服务器传输数据，从而实现用户与Web服务器的交互。

### 4.2 表单标签及属性 

- form 标签

  form 标签用于创建供用户输入的 HTML 表单

- form 属性

  - action   规定表单提交的地址
  - method  规定用于发送表单数据的 HTTP 方法：GET 或 POST 提交 
  - target  规定在何处打开 action URL

- GET 和 POST 区别

  - 传递数据方式不同
  - 处理效率不同
  - 安全性不同

  > 详见：
  >
  > https://zhidao.baidu.com/question/1498597843748014619.html

### 4.3 表单控件 

- **input 规定了用户可以在其中输入数据的输入字段**，属性 type 的值如下：

  - text  文本输入框

  - password  密码输入框

  - radio  单选框

  - checkbox  复选框

    checked 属性规定在页面加载时应该被预先选定的但选项或复选项

    单选项或复选项通过 name 属性指定归属题干

  - file  文件域

    accept 属性规定了可通过文件上传提交的服务器接受的文件类型，多个类型使用逗号分隔

    | 值          | 描述                                                         |
    | :---------- | :----------------------------------------------------------- |
    | audio/*     | 接受所有的声音文件。                                         |
    | video/*     | 接受所有的视频文件。                                         |
    | image/*     | 接受所有的图像文件。                                         |
    | *MIME_type* | 一个有效的 MIME 类型，不带参数。请参阅 [IANA MIME 类型](http://www.iana.org/assignments/media-types/)，获得标准 MIME 类型的完整列表。 |

  - image  图像域

    src  属性规定显示为提交按钮的图像的 URL

    alt  定义图像输入的替代文本

    height / width   定义图像的高度 / 宽度

  - hidden   隐藏

  - button  普通按钮

  - submit  提交按钮

  - reset  重置按钮

- **textarea  定义一个多行的文本输入控件**

  > 通过 cols 和 rows 属性来规定 textarea 的尺寸大小，不过更推荐使用 CSS 的 height 和 width 属性。

- **select  用来创建下拉列表控件**

  > 嵌套标签 option 定义列表中的可用选项，属性 selected 规定当前选项表现为选中状态。

### 4.4 相关属性

name  规定元素的名称

value  指定元素的值

autofocus   规定当页面加载时元素应该自动获得焦点

placeholder 属性规定可描述输入字段预期值的简短的提示信息 

readonly 属性规定输入字段是只读的

disabled 属性规定应该禁用的 元素

required 属性规定必需在提交表单之前填写输入字段

maxlength 属性规定元素中允许的最大字符数

size 属性规定以字符数计的元素的可见宽度。

multiple  属性规定允许用户输入到元素的多个值



### 4.5 label 标签

- label 标签介绍

  label 标签为 input 元素定义标注（标记）。

  label 元素不会向用户呈现任何特殊效果。不过，它为鼠标用户改进了可用性。如果您在 label 元素内点击文本，就会触发此控件。就是说，当用户选择该标签时，浏览器就会自动将焦点转到和标签相关的表单控件上。

- label 标签与控件关联方式
  - 通过 for 属性的值设置为相关表单元素的 id 属性的值
  - 直接包裹表单元素



## 五、HTML5

### 5.1 HTML5 简介 

- html5 是HTML第五个版本，其中某些特性，低版本浏览器是不支持的。

- html5 不再区分三个小标准。

- html5 的设计目的是为了在移动设备上支持多媒体。

- html5 新增一些有趣的特性

  HTML5 是 HTML 标准的最新演进版本。 这个术语代表了两个不同的概念：

  1. 它是一个新的 HTML 语言版本包含了新的元素，属性和行为

  2. 同时包含了一系列可以被用来让 Web 站点和应用更加多样化，功能更强大的技术

     - 用于绘画的 canvas 元素

     - 用于媒介回放的 video 和 audio 元素，使 video 和 audio 成为了在所有 Web 中的一等公民

     - 对本地离线存储的更好的支持，能够让网页在客户端本地存储数据以及更高效地离线运行

     - 新增了一些语义化标签，如 footer、header、section

       > 语义：能够让你更恰当地描述你的内容是什么

     - 新的表单控件，比如date、time、email、url、search等等

     - 新的表单属性，比如placeholder requared等等

     - 新增布尔值属性(简写)，如：reversed autofocus multiple属性值可以省略

     - 连通性：能够让你和服务器之间通过创新的新技术方法进行通信

     - 性能 & 集成：提供了非常显著的性能优化和更有效的计算机硬件使用

     - 设备访问 Device Access：能够处理各种输入和输出设备

     - 样式设计: 让作者们来创作更加复杂的主题

  > 注：HTML5的改变，涵盖了CSS3和JS的一些新特性，这些东西统称HTML5技术。

  

- html5 语法规则（更加人性化）

  - 骨架更加精简

    ```
    <!DOCTYPE html>
    <html lang="zh-CH">
    <html>
    	<head>
    		<meta charset="utf-8">
    		<title>文档标题</title>
    	</head>
    		 
    	<body>
    		文档内容......
    	</body>
    </html>
    ```

  - 大小写都可以

  - 布尔型属性 checked reversed

  - 属性值省略引号 align=center

  - 可以进行省略的标签

    ```
    不允许写结束符的标签(即单标签)：hr img input link meta 等等
    可以省略结束符的标签：li dt dd p thead tbody tr td th 等等
    可以完全省略的标签：html head body tbody等等
    ```



### 5.2 HTML5 新增语义化标签 

- **新增结构化语义(语义就是有意义)标签(结构标签（块状元素）—-可以理解为有意义的div)：主要负责web上下文结构的定义，确保html文档的完整性**

  - header  定义一个页面或者一个区域的头部

  - section  定义文档中的节（section、区段）

  - footer    定义一个页面或者一个区域的底部

  - nav        定义导航链接部分

  - article   定义页面独立的内容区域，可能的 article 实例：

    论坛帖子
    报纸文章
    博客条目
    用户评论

  <img src="http://121.89.192.46:8888/ganhuo/note/HTML基础表格表单.assets/image-20201119171557770.png" alt="image-20201119171557770" style="zoom:150%;" />

  

- **非结构化语义标签：主要完成web页面区域的划分，确保内容的有效分隔**

  - aside       定义页面的侧边栏内容
  - hgroup   用于划分标题标签分组
  - figure      用于设置独立的流内容（图片、表单、表格等等）
  - figcaption   给figure添加标题

  

- **行内语义性标签：主要完成web页面具体内容的引用和表述，是丰富内容展示的基础**

  - progress     用于表示进度条，可以用来显示下载的进度，属性有max(定义需要完成的值)和value(定义进程的当前值)

    <progress max="100" value="30">调整</progress>

    ```
    <progress max="100" value="30">调整</progress>
    ```

  - time 修饰时间

  - mark 高亮显示

  - audio   定义音频，比如音乐或其他音频流

  - vidoe   定义视频，比如电影片段或其他视频流(考虑浏览器兼容性)

    > 注：当前video元素支持三种视频格式：
    >
    > ```
    > MP4 = 带有 H.264 视频编码和 AAC 音频编码的 MPEG 4 文件(.mp4) -->  type = video/mp4
    > WebM = 带有 VP8 视频编码和 Vorbis 音频编码的 WebM 文件(.mkv) --> type = video/webm
    > Ogg = 带有 Theora 视频编码和 Vorbis 音频编码的 Ogg 文件(.ogg) --> type = video/ogg
    > ```



### 5.3 新增 input 控件属性 type 值 

- date 年月日
- month 年月
- week 年周
- time 时间
- datetime-local 年月日时分

 

- search 搜索栏
- number 数字
- color 颜色
- range 进度条

 

- tel 电话号码

- email 电子邮箱

  输入内容后，在提交时会有一个简单的验证

  <img src="http://121.89.192.46:8888/ganhuo/note/HTML基础表格表单.assets/image-20201119174204336.png" alt="image-20201119174204336" style="zoom:150%;" />

- url 网址链接

  输入内容后，在提交时会有一个简单的验证 前缀 http:// 或 https://

<img src="http://121.89.192.46:8888/ganhuo/note/HTML基础表格表单.assets/image-20201119174246313.png" alt="image-20201119174246313" style="zoom:150%;" />



### 5.4 新增表单属性 

placeholder  文本提示信息

autofocus 自动获取焦点

多个autofocus第一个生效

multiple 设置多选；file文件域 select标签

required 必填项；不填不能提交

![img](http://121.89.192.46:8888/ganhuo/note/HTML基础表格表单.assets/clip_image001-1605778877629.png)

readonly 只读

disabled 禁用

 

height、width  图像域image设置宽高

max、min 设置最大最小值 number数字、日期、range滚动条可以设置

step 步长 nuber数字



### 5.5 新增表单元素 

datalist	标签规定了 input 元素可能的选项列表

**任何的文本框都可以用 list 属性和一个 datalist 标签通过 id 产生绑定，表示智能感应**

**代码**：

```
<input list="browsers">
<datalist id="browsers">
  <option value="Internet Explorer">
  <option value="Firefox">
  <option value="Chrome">
  <option value="Opera">
  <option value="Safari">
</datalist>
```

**效果**：

<img src="http://121.89.192.46:8888/ganhuo/note/HTML基础表格表单.assets/image-20201119173837341.png" alt="image-20201119173837341" style="zoom:150%;" />

> 注：datalist 标签被用来在为 input 元素提供"自动完成"的特性。用户能看到一个下拉列表，里边的选项是预先定义好的，将作为用户的输入数据。请使用 input 元素的 list 属性来绑定 datalist 元素



### 5.6 新增音频和视频 

- video 标签的详解

  video 元素支持三种视频格式：MP4、WebM、Ogg

- audio 标签的详解

  audio 元素支持的3种文件格式：MP3、Wav、Ogg

相关属性 

| 属性                                                         | 值                 | 描述                                                        |
| :----------------------------------------------------------- | :----------------- | :---------------------------------------------------------- |
| [autoplay](https://www.runoob.com/tags/att-audio-autoplay.html) | autoplay           | 如果出现该属性，则音频在就绪后马上播放。                    |
| [controls](https://www.runoob.com/tags/att-audio-controls.html) | controls           | 如果出现该属性，则向用户显示音频控件（比如播放/暂停按钮）。 |
| [loop](https://www.runoob.com/tags/att-audio-loop.html)      | loop               | 如果出现该属性，则每当音频结束时重新开始播放。              |
| [muted](https://www.runoob.com/tags/att-audio-muted.html)    | muted              | 如果出现该属性，则音频输出为静音。                          |
| [preload](https://www.runoob.com/tags/att-audio-preload.html) | auto metadata none | 规定当网页加载时，音频是否默认被加载以及如何被加载。        |
| [src](https://www.runoob.com/tags/att-audio-src.html)        | *URL*              | 规定音频文件的 URL                                          |





### 5.7 补充

- details 标签用于描述文档或文档某个部分的细节
  - open 布尔型属性，规定 details 是否可见，内容默认对用户是不可见的
- summary 标签为元素定义一个可见的标题。 当用户点击标题时会显示出详细信息。

**代码**：

```
<datails>
	<summary>国家全称</summary>
	<p>中华人民共和国</p>
	<p>美利坚合众国</p>
	<p>大不列颠及北爱尔兰联合王国</p>
	<p>俄罗斯联邦政府</p>
</datails>
```

**页面效果**：

<img src="http://121.89.192.46:8888/ganhuo/note/HTML基础表格表单.assets/image-20201119171841188.png" alt="image-20201119171841188" style="zoom:150%;" />

