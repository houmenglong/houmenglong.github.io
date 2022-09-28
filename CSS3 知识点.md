

# CSS3知识点

------



主讲：**MagnumHou**

微信公众号：**前端知识分享喵**

<img src="http://121.89.192.46:8888/ganhuo/weChat.png" alt="微信图片_20200601153857" style="zoom:80%;" />



------



[TOC]

------

## 前言：CSS 简介 

1. **CSS 概述**

   - CSS ( Cascading  Style Sheet ) 层叠样式表，用来修饰 HTML，使得效果更加多样化
   - CSS 在 HTML4.0 中引入，一般在开发过程中，会使用单独的 CSS 文件进行开发，然后将这个独立 CSS 文件引入到需要的 HTML 文件中

2. **引入 CSS 的好处** 

   - 达到结构与样式的分离，后期维护更加方便；
   - 浏览器兼容性更好；
   - 代码更加简洁，一个CSS文件可以被多个html文件引用；

3. **CSS基础语法**

   - CSS 规则主要由两个部分构成：选择符 和 声明 ( 一条或多条 )
   - 语法  选择符{ 属性 : 属性值 }

   

## 一、CSS 引入方式 

- 行内式 通过 style 属性在标签内嵌入

- 内嵌式 通过 style 标签在 head 标签内嵌入

- 链接式 通过 link 标签在 head 标签内引入外部独立的样式

- 导入式 同内嵌式，不同的是在 style 标签内通过 @import 导入外部独立的样式

  

> CSS 层叠性体现：匹配元素权值相同的前提下，多种引入方式样式冲突时，根据就近原则，离着元素近的引入方式样式覆盖离着元素远的引入样式 



**面试题：链接式与导入式的区别** 

- link是XHTML标签，除了加载CSS外，还可以定义RSS等其他事务；而@import属于CSS范畴，只能加载CSS；
- link引用CSS时，在页面载入时同时加载；而@import需要页面网页完全载入以后加载。
- link是XHTML标签，无兼容问题；而@import是在CSS2.1提出的，低版本的浏览器不支持。
- link支持使用 `JavaScript` 控制DOM去改变样式；而@import不支持。
- @import可以在CSS文件中再次引入其他样式表；而link不支持。 



## 二、CSS 选择器 

### 2.1 基本选择器

- 全局选择器  *
- 标签选择器  `tagname`
- class 选择器  `.classname`
  - 同一个元素可以设置多个类名，空格隔开、
  - 同一个类名可以设置给多个元素

- id 选择器 `#idname`
  - 每个元素的 id 是唯一的

### 2.2 关系选择器 

- 子代选择器  E > F
- 后代选择器  E  F
- 相邻兄弟选择器  E + F
- 通用兄弟选择器  E ~ F
- 并集选择器 E,F,...,N
- 交集选择器 `elment#id.classname1,classname2,...,classnameN`

### 2.3 动态伪类选择器 

- :link  初始状态
- :visited  访问后状态
- :hover  鼠标悬停状态
- :active  激活状态

### 2.4 选择器优先级 

- 权值的计算规则 

  权值代表一个选择器的重要程度，权值越高，选择器的优先级就越高。

![image-20201118151449661](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201118151449661.png)

- 复杂选择器判断优先级 

​		 选中元素，分别判断 id、class、element 选择器的数量

​		 未选中元素，就近原则，距离相同 ，按照  id、class、element 选择器的数量进行判断



> 层叠性体现：优先级高的覆盖优先级低的样式



## 三、文字相关样式

1. 字体类型 font-family

   > 注：可以设置多个字体，使用逗号隔开；如果浏览器不支持第一个字体，则会尝试下一个。

2. 字体大小 font-size: 关键字 | 固定值 | 百分比 ( 基于父元素 ) 

3. 字体粗细 font-weight: 关键字 | 100-900之间的整百数

4. 字体样式 font-style: normal | italic | oblique

   > 注：italic 和 oblique 都是向右倾斜的文字, 但区别在于 italic 是指斜体字，而 oblique 是倾斜的文字，对于没有斜体的字体应该使用 oblique 属性值来实现倾斜的文字效果

6. font 简写属性

   即在一个声明中设置所有字体属性，设置的属性顺序如下：

   ```
   font:"font-style font-weight font-size/line-height font-family"
   ```

   > 注：font-size 和 font-family 的值是必需的； line - height   属性设置行与行之间的空间

7. CSS3 @font-face 规则

   使用 **CSS3**，网页设计师可以使用他/她喜欢的任何字体，在新的 @font-face 规则中，您必须首先定义字体的名称（比如 myFirstFont），然后指向该字体文件。详见：https://www.runoob.com/css3/css3-fonts.html

   **字体定义**

   ```
   @font-face{
       font-family: myFirstFont;
       src: url('Sansation_Light.ttf'),
            url('Sansation_Light.eot'); /* IE9 */
   }
   ```

   **字体使用**

   ```
   div{
   	font-family: myFirstFont;
   }
   ```

   > 注：Internet Explorer 9 只支持 .eot 类型的字体, Firefox, Chrome, Safari, 和 Opera 支持 .ttf 与.otf 两种类型字体。 Internet Explorer 8 及更早IE版本不支持@font-face 规则。



## 四、文本相关样式

1. 文本颜色 color: 颜色名称 | 十六进制 | RGB |  RGBA | HSL | HSLA

2. 文本装饰 text-decoration: underline | overline | line-through | none;

   ```
   /*关键值*/
   text-decoration: none;                     /*没有文本装饰*/
   text-decoration: underline red;            /*红色下划线*/
   text-decoration: underline wavy red;       /*红色波浪形下划线*/
   
   /*全局值*/
   text-decoration: inherit;
   text-decoration: initial;
   text-decoration: unset;
   
   /*虚线dotted 与 波浪线wavy 注意：在Edge/Internet 浏览器中没有效果*/
   text-decoration: underline overline dotted red; /*红色点状上划线和下划线*/
   text-decoration: underline overline wavy blue;  /*蓝色波浪形上划线和下划线*/
   ```

   > 注：text-decoration 属性是以下三种属性的简写
   >
   > - 线条线型 text-decoration-line: none|underline|overline|line-through
   > - 线条颜色 text-decoration-color
   > - 线条种类 text-decoration-style: solid|double|dotted|dashed|wavy(波浪)

3. 文本大小写 text-transform: capitalize (单词首字母大写) | uppercase (字母大写) | lowercase (字母小写) 

4. 段落首行缩进 text-indent: 固定值 | 百分比

5. 文本水平对齐 text-align: left | center | right | justify (分散对齐)

   >  注：属性 text-justify 用域当 text-align 设置为 justify 时指定分散对齐的方式，属性值如下
   >
   > | 值              | 描述                                                   |
   > | :-------------- | :----------------------------------------------------- |
   > | auto            | 浏览器决定齐行算法。                                   |
   > | none            | 禁用齐行。                                             |
   > | inter-word      | 增加/减少单词间的间隔。                                |
   > | inter-ideograph | 用表意文本来排齐内容。                                 |
   > | inter-cluster   | 只对不包含内部单词间隔的内容（比如亚洲语系）进行排齐。 |
   > | distribute      | 类似报纸版面，除了在东亚语系中最后一行是不齐行的。     |
   > | kashida         | 通过拉伸字符来排齐内容。                               |

6. 行高 line-height: 固定(单位)值 | 百分比 (%) | number (倍数)

7. 字，词间距 

   letter-spacing  设置字符间距

   word-spacing  设置单词间距

8. ( 盒子 ) 文本的方向 / 书写方向  direction: ltr (默认) | rtl

9. 元素的垂直对齐方式 vertical-align: 关键字 | 固定值 | 百分比 

   > 注：该属性定义行内元素的基线相对于该元素所在行的基线的垂直对齐。允许指定负长度值和百分比值。这会使元素降低而不是升高。在表单元格中，这个属性会设置单元格框中的单元格内容的对齐方式。

10. 元素内留白处理 white-space 属性值如下

    | 值       | 描述                                                         |
    | :------- | :----------------------------------------------------------- |
    | normal   | 默认。空白会被浏览器忽略。                                   |
    | pre      | 空白会被浏览器保留。其行为方式类似 HTML 中的 pre 标签。      |
    | nowrap   | 文本不会换行，文本会在在同一行上继续，直到遇到 br 标签为止。 |
    | pre-wrap | 保留空白符序列，但是正常地进行换行。                         |
    | pre-line | 合并空白符序列，但是保留换行符。                             |

11.  文本溢出元素处理 text-overflow: clip (修剪) | ellipsis (省略号代替被修剪的文本) | 其它字符串代替修剪文本

    **单行文本溢出 ... 代替处理方案**

    ```
    p {
    	width:300px; /*容器的宽度*/
    	white-space:nowrap; /*强制不换行*/
    	text-overflow:ellipsis; /*省略号代替被修剪的文本*/
    	overflow:hidden;  /*内容溢出容器部分隐藏*/
    }
    ```

    

## 五、列表相关样式

1. 项目符号类型 list-style-type  

   > 属性值不完全统计，详见 https://www.runoob.com/cssref/pr-list-style-type.html 

2. 项目符号位置 list-style-position: inside | outside

   ![image-20201116160005787](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201116160005787.png)

3. 图片类型项目符号 list-style-image:url('图片路径')

4. 列表属性简写 list-style: list-style-type, list-style-position, list-style-image.

   > 注：可以不设置其中的某个值，如 "list-style:circle inside;" ，未被设置的属性会使用其默认值。



## 六、表格相关样式

border-collapse 属性设置表格的边框是否被合并为一个单一的边框，属性值如下

| 值       | 说明                                                         |
| :------- | :----------------------------------------------------------- |
| collapse | 如果可能，边框会合并为一个单一的边框。会忽略 border-spacing 和 empty-cells 属性 |
| separate | 默认值。边框会被分开。不会忽略 border-spacing 和 empty-cells 属性 |



## 七、背景相关样式

1. 背景颜色 background-color: 颜色值 | transparent ( 透明 )

   > 合法颜色值：https://www.runoob.com/cssref/css-colors-legal.html

2. 背景图片 background-image 属性值如下

   | 值                                                           | 说明                                      |
   | :----------------------------------------------------------- | :---------------------------------------- |
   | url(*'URL'*)                                                 | 图像的URL                                 |
   | none                                                         | 无图像背景会显示。这是默认                |
   | [linear-gradient()](https://www.runoob.com/cssref/func-linear-gradient.html) | 创建一个线性渐变的 "图像"(从上到下)       |
   | [radial-gradient()](https://www.runoob.com/cssref/func-radial-gradient.html) | 用径向渐变创建 "图像"。 (center to edges) |

   > 注：1. 元素的背景是元素的总大小，包括填充和边界（但不包括边距）
   >
   > ​	    2. 多张背景图片，请使用逗号隔开

3. 背景图片平铺方式 background-repeat: repeat (默认) | repeat-x | repeat-y | no-repeat

4. 背景图片起始位置设置 background-position: 关键字 () | 百分比 <*x% y%*> | 固定 (单位) 值 <*xpos ypos*>

   > 注：1. 关键字有left top、left、left bottom、right top、right 、right bottom、top、center、bottom
   >
   > ​		2. 百分比 和 固定值 中第一个值是水平位置值，第二个值是垂直位置值

5. 背景图片大小 background-size: 固定值(单位)  | 百分比 (相对于背景定位区域) | cover | contain

   > 注：1. 固定值 和 百分比，第一个值为宽度，第二个值为高度。如果只有一个值，第二个值为 **auto**(自动)
   >
   > ​		2. cover 保持图像纵横比并将图像缩放成将完全覆盖背景定位区域的最小大小 
   >
   > ​		3. contain 保持图像的纵横比并将图像缩放成将适合背景定位区域的最大大小

6. 背景图片是否随对象内容滚动  background-attachment 属性值如下

   | 值     | 描述                                       |
   | :----- | :----------------------------------------- |
   | scroll | 背景图片随着页面的滚动而滚动，这是默认的。 |
   | fixed  | 背景图片不会随着页面的滚动而滚动。         |
   | local  | 背景图片会随着元素内容的滚动而滚动。       |

7. 背景（颜色、图片）裁剪显示区域  background-clip: border-box|padding-box|content-box

8. 背景原点 background-origin:  padding-box|border-box|content-box

9. 背景简写 background:bg-color bg-image position/bg-size bg-repeat bg-origin bg-clip bg-attachment

10. 雪碧图介绍与应用

    - **什么是雪碧图？**

      雪碧图也叫CSS精灵， 是一种CSS图像合成技术，就是将许多小图标合并在一张背景透明的图片上，使用background-position和background-size来控制图片显示的区域

    - **为什么要使用雪碧图？**

      网站开发90%会用到小图标， 多小图标调用显示是前端开发常见的问题，如果每个小图标都单独调用一张图片， 即意味着每个小图标的显示都产生一个HTTP请求；每个请求都需要一定的性能开销，主要在请求、以及响应阶段。为了减少http请求数量，加速网页内容显示，很多网站的导航栏图标、登录框图片等，使用的并不是<image>标签，而是CSS Sprite雪碧图。

    - **使用雪碧图的优缺点**

      优点：

      - 通过将多张图片合并成一张，可以有效减少 HTTP 请求，提高页面加载的性能
      - 将多张图片合并到一张图片中，可以减小图片的总大小
      - 整理起来更为方便，同一个按钮不同状态的图片也不需要一个个切割出来并个别命名
      - 只需要修改一张或少张图片的颜色或样式来改变整个网页的风格
      - 只需对一张集合的图片命名，不需要对每一个小图片进行命名，从而提高了网页制作效率

      缺点：

      - 合成起来麻烦
      - 适应性差
      - 可维护性差
      - 小图标在高清屏幕上可能会失真，另外频繁使用定位会占用比较多的CPU

    - **应用场景**

      - 静态图片，不随用户信息的变化而变化
      - 小图片，图片容量比较小
      - 加载数量比较大

    - PS or  PW 工具的基本使用（能够自己进行切图处理）

      ![image-20201116165626986](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201116165626986.png)<img src="http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201116165740790.png" alt="image-20201116165740790" style="zoom:90%;" />

      

    - **练习**

      ![image-20201116165403580](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201116165403580.png)



## 八、盒模型概念与组成

### 8.1 生活举例

比方买电脑快递过来的整个盒子就可以看做是盒模型，体现在html中就是一个外层标签。

想要盛放东西，那么盒子必须有一定的大小，体现到 css 中通过**width、height**属性设置。

这个时候将买的电脑放到盒子中，这台电脑就是盒子中所要存放的**内容content**。

为了防止在运输过程中，电脑屏幕被挤压，需要在盒子内部与电脑之间加一些填充物（泡沫），体现到CSS中就是**padding叫做内填充**，给外层盒子的填充，加完填充物，需要使用更大的盒子来装电脑。

这个时候根据物品的重要性是否怕压等，选择合适质地的纸盒子，提现到CSS中就是纸**盒子边框**的线型、厚度、颜色 **border**。

电脑打包完毕，开始给快递公司运输。但是店家会把所有人的电脑订单一块给快递公司，这个就会有很多天电脑的包装，快递员收的时候，可能对这些贵重物品，做一个简单的处理，让这些盒子之间，设置一定的间隔或填充物来防止**盒子之间**的挤压。这些盒子外边缘与外边缘之间的间隔或距离体现到CSS中就是 **margin**。

### 8.2 概念

**CSS（Cascading Style Sheet）可译为“层叠样式表 ”或“级联样式表”**，它定义如何显示HTML 元素，用于控制Web页面的外观。通过使用CSS实现页面的内容与表现形式分离，极大提高了工作效率。CSS 假定所有的HTML 文档元素都生成了一个描述该元素在HTML文档布局中所占空间的矩形元素框，可以形象地将其看作是一个盒子

CSS 围绕这些盒子产生了一种“盒子模型”概念，通过定义一系列与盒子相关的属性，可以极大地丰富和促进各个盒子乃至整个HTML文档的表现效果和布局结构。对于是盒子的元素，如果没有特殊设置，其默认总是占独立的一行，宽度为浏览器窗口的宽度，在其前后的元素不管是不是盒子，都只能排列在它的上面或者下面，即上下累加着进行排列。

**HTML文档中的每个盒子都可以看成是由从内到外的四个部分构成，即内容区（content）、填充(padding)、边框(border)和空白边(margin)**。 CSS 为四个部分定义了一系列相关属性，通过对这些属性的设置可以丰富盒子的表现效果。



## 九、盒模型组成分析

盒子模型包含四个部分：内容content、内填充padding 、边框border、外边距margin

### 9.1 **内容区（content）**

**内容区是盒子模型的中心**，它呈现了盒子的主要信息内容，这些内容可以是文本、图片等多种类型。内容区有三个属性，width、height 和 overflow。

- 属性 width和height 指定盒子内容区的高度和宽度

- 属性 overflow 指定内容溢出盒子后得处理方式，属性值如下：

  - hidden，溢出部分将不可见；

  - visible，溢出的内容信息可见，只是被呈现在盒子的外部

  - scroll，滚动条将被自动添加到盒子中，用户可以通过拉动滚动条显示内容信息；

  - auto，将由浏览器决定如何处理溢出部分

    > 当内容信息太多，超出内容区所占范围时，可以使用overflow 溢出属性来指定处理方法

**注意：盒模型是所有页面布局的基础，可以说是重中之重的内容。就类似于盖房子的地基，地基打不好，一切都白搭。**

### 9.2 内填充（padding）

**填充是内容区和边框之间的空间**。

- **按照填充方向划分**

  - padding -top
  - padding -bottom
  - padding -left
  - padding-right 

- **按照值的多少划分**

  综合了以上四种方向的快捷填充属性padding

  - 单值法
  - 二值法
  - 三值法
  - 四值法

> 注：使用这五种属性可以指定内容区信息内容与各方向边框间的距离。设置盒子背景色属性时，可使背景色延伸到填充区域。

### 9.3 **边框（border）**

边框是环绕内容区和填充的边界。

- **按照属性不同分类**

  - border-style  边框样式

    1. 此属性是边框最重要的属性，如果没有指定边框样式，其他的边框属性都会被忽略，边框将不存在

    2. CSS规定了 dotted、dashed、solid等九种边框样式，如下

       ![image-20201117133817287](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201117133817287.png)

  - border-width 边框厚度

    1. 属性值可以是长度计量值，也可以是CSS规定的thin、medium 和thick

  - border-color  边框颜色

- **按照方向进行分类**，如下：

  border-top-style: solid

  border-left-color: red

  border-bottom-width:10px;

- **按照值的多少进行分类**

  `border-style:top right bottom left`

  `border-width:top right bottom left`

  `border-color:top right bottom left`

  ```
  /*同时设置四个方向的样式*/
  /*设置的边框样式*/
  /*一个值代表四个边框都是一样的*/
  /*border-style:solid;*/
  /*设置两个值  第一个上下单实线 第二个左右双实线*/
  /*border-style: solid double ;*/
  /*设置三个值 第一个是上单实线 第二个左右双实线  第三个下虚线*/
  /*border-style:solid double dashed;*/
  /*四个值 分别是对应上右下左的设置*/
  border-style:solid double dashed dotted;
  
  /*设置边框的厚度 和上面一样 一个值 两个值 三个值 四个值*/
  /*border-width: 4px;*/
  /*border-width: 4px 10px;*/
  /*border-width: 4px 10px 1px;*/
  border-width: 4px 10px 8px 20px;
  
  /*设置颜色 和上面一样*/
  /*border-color: red;*/
  /*border-color: red blue;*/
  /*border-color:red blue green;*/
  border-color:red blue green orange;
  ```

**综合了以上四种方向的简写属性  `border:style width color;`** 设置四个边相同的样式

> **注：设置盒子背景色属性时，在IE中背景不会延伸到边框区域，但在FF等标准浏览器中，背景颜色可以延伸到边框区域，特别是单边框设置为点线或虚线时能看到效果**



**边框案例**：三角形制作

**等腰三角形制作：**

![image-20201117135213515](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201117135213515.png)

```
/*设置元素为行内块元素：能设置宽高 且能与其它行内级元素在同一行内排列*/
display: inline-block;

/*border: solid 100px red;
border-left-color: white;
border-bottom-color:white;
border-right-color:white;*/
	
/*简化*/
/*border: solid 100px white;
border-top-color: red;*/
	
/*当祖先有背景的情况下，白色很突兀，这个时候请使用 透明色替换白色*/
border:solid 100px transparent;
/*箭头朝下  上面边框设置颜色*/
/*border-top-color: red;*/
/*箭头朝上  下面边框设置颜色*/
/*border-bottom-color: green;*/
/*箭头朝左  右边*/
/*border-right-color: orange;*/
/*箭头朝右  左边*/
border-left-color: purple;
```

**直角三角形制作：根据直角的位置，保留两个方向的边框，如左上角** **保留左边和上边的边框**

![image-20201117135248358](D:/J-11/couser_note/html-css-js-courseware/00-07 HTML5+CSS3/02_盒子模型相关/盒子模型相关笔记.assets/image-20201117135248358.png)

```
display: inline-block;
margin-left: 200px;
	
border: solid 50px transparent;
/*直角在左上角*/
border-left-color: red;
border-top-color: red;
```



### 9.4 外边距（margin）

外边距位于盒子的最外围，是添加在边框外周围的空间。外边距使盒子之间不会紧凑地连接在一起，是CSS 布局的一个重要手段。

![image-20201117140934164](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201117140934164.png)

- **按照填充方向划分**

  - margin-top
  - margin-bottom
  - margin- left
  - margin-right

- **按照值的多少划分**

  综合了以上四种方向的外边距属性 margin，使用类似于内填充 padding

  - 单值法
  - 二值法
  - 三值法
  - 四值法

> 注：CSS 容许给外边距属性指定负数值，当指定负外边距值时，整个盒子将向指定负值方向的相反方向移动，以此可以产生盒子的重叠效果。采用指定外边距正负值的方法可以移动网页中的元素，这是CSS 布局技术中的一个重要方法。



### 9.5 外边距合并问题

**外边距合并指的是，当两个垂直外边距相遇时，它们将形成一个外边距。合并后的外边距的高度等于两个发生合并的外边距的高度中的较大者。**

当一个元素出现在另一个元素上面时，第一个元素的下外边距与第二个元素的上外边距会发生合并。请看下图：

![image-20201117145822621](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201117145822621.png)

当一个元素包含在另一个元素中时（假设没有内边距或边框把外边距分隔开），它们的上和/或下外边距也会发生合并。请看下图：

![image-20201117145847865](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201117145847865.png)

尽管看上去有些奇怪，但是外边距甚至可以与自身发生合并。

假设有一个空元素，它有外边距，但是没有边框或填充。在这种情况下，上外边距与下外边距就碰到了一起，它们会发生合并：

![image-20201117150023969](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201117150023969.png)

如果这个外边距遇到另一个元素的外边距，它还会发生合并：

![image-20201117150044446](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201117150044446.png)

这就是一系列的段落元素占用空间非常小的原因，因为它们的所有外边距都合并到一起，形成了一个小的外边距。

外边距合并初看上去可能有点奇怪，但是实际上，它是有意义的。以由几个段落组成的典型文本页面为例。第一个段落上面的空间等于段落的上外边距。如果没有外边距合并，后续所有段落之间的外边距都将是相邻上外边距和下外边距的和。这意味着段落之间的空间是页面顶部的两倍。如果发生外边距合并，段落之间的上外边距和下外边距就合并在一起，这样各处的距离就一致了。

![image-20201117150120723](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201117150120723.png)

> **注释：**只有普通文档流中块框的垂直外边距才会发生外边距合并。行内框、浮动框或绝对定位之间的外边距不会合并。



### 9.6 总结

元素总宽度计算公式：总元素的宽度=宽度+左填充+右填充+左边框+右边框+左边距+右边距

元素总高度最终计算公式：总元素的高度=高度+顶部填充+底部填充+上边框+下边框+上边距+下边距

> **需要注意的是：当给元素设置的 margin 或 padding 值为百分比时，不管哪个方向，永远定义的是基于父对元素宽度的百分比的外边距 或 内填充**



### 9.7 CSS继承性体现：

继承性：某些祖先元素的样式子类可以继承

文本相关和排版相关的样式可以继承，如：color 、font-系列、text-系列等等

盒子相关属性和背景相关属性不可以继承，如：width、height、margin、padding、border、background-color等



## 十、盒模型分类

CSS3 `box-sizing` 属性允许你以某种方式定义某些元素，以适应指定区域，属性值如下：

- content-box 指定盒模型为 W3C 标准模型

  ```
  W3C标准盒模型（conten-box值）【width/height被改变，扩展】
  width = content + border + padding;
  ```

- border-box 指定盒模型为 IE模型（怪异模式）

  ```
  IE怪异盒模型（border-box值）【content被改变，压缩】
  content = width - border - padding;
  ```

  > 注：上面width 为在CSS中设置的元素的width;



## 十一、元素框类型  

**display 属性规定元素应该生成的框的类型**，选取部分属性值如下

| 值           | 描述                                                         |
| :----------- | :----------------------------------------------------------- |
| none         | 此元素不会被显示。                                           |
| block        | 此元素将显示为块级元素，此元素前后会带有换行符。             |
| inline       | 默认。此元素会被显示为内联元素，元素前后没有换行符。         |
| inline-block | 行内块元素。（CSS2.1 新增的值）                              |
| table        | 此元素会作为块级表格来显示（类似 table），表格前后带有换行符。 |
| table-row    | 此元素会作为一个表格行显示（类似 tr）。                      |
| table-cell   | 此元素会作为一个表格单元格显示（类似 td 和 th）              |

> 注：行内元素 margin 和 padding 设置上下方向值无效



**盒子在标准流定位原则（元素排列方式）** 

按照我们书写的 html 结构顺序，依次按照元素默认的类型在浏览器进行渲染：块状元素独占一行，非块状元素从左到右依次排列。



## 十二、visibility 与 opacity

visibility 属性指定一个元素是否是可见的

```
visibility:visible(默认，元素可见) | hidden(元素不可见)
```

opacity 属性指定不透明度。从0.0（完全透明）到1.0（完全不透明）



**面试题： 如何设置元素不可见**

```
/**/
display: none

/**/
visibility: hidden;

/**/
opacity:0

/**/
height: 0; 
overflow: hidden;

/**/
transform: scale(0); 

/**/
position: absolute;
left: -9999px;
```





## 前言

### **布局方式的介绍**

布局模型是基于盒模型基础上进行的拓展，关于布局有流式布局（标准的布局），浮动布局、定位布局、flex布局等。

#### 标准流（流动模型）

描述：元素按照自己默认的元素类型在页面中进行排列的方式叫做标准流布局。

**按照元素的框类型分类：**

- **块块元素block**

  前后具有换行符，默认独占一行。

  可以设置宽高，设置宽高后容器范围为设置的宽高的范围，但换行符一直存在。

  设置上下外边距存在合并问题。

  非块状元素设置为块状元素 display:block;

  目前学过的块状元素 h1-h6 p  div 等

- **行内元素inline**

  在同一行内与其它行内级元素从左到右依次排列。默认包裹内容。

  行内元素不能设置宽高。

  设置左右外边距生效，上下外边距不生效；

  设置左右内填充生效，上下内填充不生效（不占位，不会撑大盒子，但是背景色又呈现）;

  非行内元素设置为行内元素 display:inline;

  目前学过的行内元素 span a strong em ins del 等

- **行内块元素 inline-block**

  在同一行内与其它行内级元素从左到右依次排列。默认包裹内容。

  可以设置宽高，设置宽高后容器范围为设置的宽高的范围。

  所有的外边距和内填充都是生效的。

  非行内块元素设置为行内块元素 display:inline-block; 

  常见的行内块元素 input textarea select img等

  

**总结：**标准流中，块级元素block在页面中从上往下依次排列，行内级元素（inline、inline-block）在同一行内从左到右依次排列，超出父容器后自动换行。如果文本内容没有使用元素进行包裹，那么被识别为匿名行内元素。

 

**案例：**导航栏制作

![image-20201119114619154](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201119114619154.png)





## 十三、浮动布局

### 13.1 浮动的概念 

- 浮动模型：用来改变块元素(block element)对象的默认显示方式。block对象设置了float属性之后，它将本来占据一行的元素，可以并列排在一行里。

- 设置浮动属性， 可以向左侧或右侧，浮动的框就因此向左或向右移动，直到它的外边缘碰到包含框(浮动元素的包含块是其最近的块级祖先元素)或另一个浮动框的边框为止。

- **通过属性 float 设置元素的浮动，对应的属性值**

  - **left  (左浮动 )**  
  - **right ( 右浮动 )**
  - **none ( 默认，不浮动 )**  

- 浮动设计的初衷，仅仅是为了在排版中，实现文字环绕图片效果

  ```
  <div style="background-color: #f5f5f5;">
  	<img src="img/3.jpg">
  	<p> ....</p>
  </div>
  ```

  以上代码使用样式对img设置左浮动，p不设置浮动，适量增加p中的内容，缩放视口查看效果； 脱离了文档流（是相对于普通文档流来说的），该元素就不在占空间，因此在计算高度时这个元素就不考虑，上面本身div没有设置高度，它的高度由元素里的内容 与元素里的内容高度共同决定（把父元素撑开），当元素设置浮动后，它就脱离文档流，在标准流中，就只有元素一个，元素就自然排在上面去了，此时 父元素div的高度就是由元素里的内容的高度决定。（也就是经常说的，父元素会塌陷问题，道理就在这）脱离文档流只是在视觉上这个元素还是占据空间的，图片元素 不会覆盖其他元素内容（这里内容俩字很重要，也充分说明了在使用float脱离文档流时，其他盒子会无视这个元素，但其他盒子内的文本内容依然会为这个元素让出位置， 环绕在周围），或不被其他元素内容覆盖，如以下操作：在以上代码基础上，div外新增一个p元素，添加文本内容，然后将div内部img和p元素设置左浮动，查看效果

### 13.2 浮动的特性 

- 浮动模型改变了元素的默认排列方式，可以使元素紧密排列（按照设置浮动的方向依次贴边显示）
- 浮动后的元素都具有了块级元素的特点
- 设置浮动后的元素，不存在上下外边距合并的问题
- 浮动的元素脱离了标准的文档流，不在文档流中占位置，且会形成压盖效果，前面设置浮动的元素压盖后面标准流中的元素
- 子元素设置浮动，父元素在没有设置高度的情况下，会呈现塌陷的效果

### 13.3 清除浮动 

- **为什么要清除浮动** 

  当父元素不设置高度或者设置的高度小于子元素；而子元素又设置了浮动，那么会造成父元素塌陷。如下，子元素全部设置浮动后，父元素塌陷效果：

  ![img](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/clip_image002.jpg)

- **清除浮动的属性 clear**，属性值

  - left  清除左浮动
  - right  清除右浮动
  - both  清除左右浮动，常用

- **清除浮动的方式**（至少需要讲以下四种）

  - 父元素设置合理的高度

    这种方式可以解决视觉上父元素塌陷问题，但元素还是浮动的效果；

    且在页面布局中，更多的容器其实是被内容撑起来的，在一开始布局的时候，父元素的高度其实是不太好确定的，所以除非是明确尺寸的布局，否则不建议使用这种方式

  - 父元素设置`overflow:hidden|scroll |auto`属性

    描述：通过给父元素设置overflow:hidden | scroll | auto

    问题：如果子元素及内容不超出父元素，用起来很方便。但是如果有定位存在需要将子元素定位到父元素外的某个位置，那么溢出的部分就看不到了。根据实际情况使用。

  - 利用空元素（内墙或外墙）

    描述：这种方式是在父元素内部的最后，添加一对空标签，然后给这个空标签设置清除浮动clear:both

    问题：当页面应用浮动过多的时候，会增加html空标签的数量，一方面影响加载速度，另一方面也不美观

  - after 伪类清浮动（推荐）

    这种方法是推荐使用的，bootsrtap也在使用，应该掌握，不然太low了，他的原理就是通过伪元素选择器，在div后面添加了一个clear:both的属性，跟第三种方法是一样的道理。

    如下：给父元素添加一个伪元素

    ```
    .clearfix::after{
        display: block;
        height: 0;
        content: '';
        clear: both;
        visibility: hidden;
    }
    
    .clearfix{
    	//兼容低版本IE
    	zoom:1;
    }
    ```

  - 了解其它清除浮动的方式

    - 给父元素设置浮动，会造成新的问题

    - 给父元素设置 `display:table;`

      将div属性变成表格，会产生新的未知问题

    - 使用双伪元素清除浮动

      ```
      .clearfix:after,.clearfix:before{
      	content:'';
      	display:block;
      	clear:both;
      }
      .clearfix{
      	//兼容低版本IE
      	zoom:1;
      }
      ```

      

  ### 13.4 练习

  1. 色块布局

     ![image-20201119142253295](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201119142253295.png)

  2. 导航栏一

     ![image-20201119142410595](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201119142410595.png)

  3. 导航栏二

     ![image-20201119142428927](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201119142428927.png)





## 十四、定位

### 14.1 定位的概念

日常生活中，去到某个陌生的城市，我们通常打开手机地图，定位自己当前位置和要去的位置，查找所对应的路线。

在CSS中的定位，道理其实差不多。就是给当前元素进行位置的处理。

W3CSchool规定定位的基本思想：它允许你定义元素框相对于其正常位置应该出现的位置，或者相对于父元素、另一个元素甚至浏览器窗口本身的位置。

参考文档：https://www.w3school.com.cn/css/css_positioning.asp

### 14.2 定位的种类 

- 静态定位static
  - HTML 元素的默认值，即没有定位，遵循正常的文档流对象。
  - 静态定位的元素不会受到 top, bottom, left, right影响。
- 相对定位relative
  - 元素框偏移某个距离。元素仍保持其未定位前的形状，它原本所占的空间仍保留。
  - 相对定位元素经常被用来作为绝对定位元素的容器块。
- 绝对定位absolute
  - 绝对定位的元素的位置相对于最近的已定位父元素，如果元素没有已定位的父元素，那么它的位置相对于 html
  - absolute 定位使元素的位置与文档流无关，因此不占据空间。
  - absolute 定位的元素和其他元素重叠。
- 固定定位fixed
  - 元素的位置相对于浏览器窗口是固定位置。即使窗口是滚动的它也不会移动：
- 粘性定位
  - sticky 英文字面意思是粘，粘贴，所以可以把它称之为粘性定位。
  - **position: sticky;** 基于用户的滚动位置来定位。
  - 粘性定位的元素是依赖于用户的滚动，在 **position:relative** 与 **position:fixed** 定位之间切换。它的行为就像 **position:relative;** 而当页面滚动超出目标区域时，它的表现就像 **position:fixed;**它会固定在目标位置。
  - 元素定位表现为在跨越特定阈值前为相对定位，之后为固定定位。
  - 这个特定阈值指的是 top, right, bottom 或 left 之一，换言之，指定 top, right, bottom 或 left 四个阈值其中之一，才可使粘性定位生效。否则其行为与相对定位相同。

### 14.3 位置相关属性

​	top | right | bottom | left 

### 14.4 z-index 属性 

元素的定位与文档流无关，所以它们可以覆盖页面上的其它元素

z-index属性指定了一个元素的堆叠顺序（哪个元素应该放在前面，或后面），属性值为 number 数字

一个元素可以有正数或负数的堆叠顺序，一般设置大于0的数字

具有更高堆叠顺序的元素总是在较低的堆叠顺序元素的前面。

如果两个定位元素重叠，没有指定z - index，最后定位在HTML代码中的元素将被显示在最前面。

### 14.5 压盖顺序：

通过z-index设置，属性值大于0的数字

1）第一种情况：设置了定位压盖没有设置定位的元素

2）第二种情况：设置了非静态定位的同级元素之间默认后面压盖前面；如果设置z-index，值越大，越靠上

3）第三种情况，嵌套的元素，父元素的z-index决定压盖的顺序



## 拓展：BFC概念

官方文档：https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS/Block_formatting_context

### 1. Box、Formatting Context的概念

- **Box**

  Box 是 CSS 布局的对象和基本单位， 直观点来说，就是一个页面是由很多个 Box 组成的。元素的类型和 display 属性，决定了这个 Box 的类型。 不同类型的 Box， 会参与不同的 Formatting Context（一个决定如何渲染文档的容器），因此Box内的元素会以不同的方式渲染。让我们看看有哪些盒子：

  - block-level box:display 属性为 block, list-item, table 的元素，会生成 block-level box。并且参与 block fomatting context；
  - inline-level box:display 属性为 inline, inline-block, inline-table 的元素，会生成 inline-level box。并且参与 inline formatting context；
  - run-in box: css3 中才有， 这儿先不讲了。

- **Formatting context**

  Formatting context 是 W3C CSS2.1 规范中的一个概念。它是页面中的一块渲染区域，并且有一套渲染规则，它决定了其子元素将如何定位，以及和其他元素的关系和相互作用。最常见的 Formatting context 有 Block fomatting context (简称BFC)和 Inline formatting context (简称IFC)。

  CSS2.1 中只有 `BFC `和 `IFC`, [CSS3](http://www.cnblogs.com/lhb25/category/146075.html) 中还增加了 `GFC `和 `FFC。`



### 2. 什么是 BFC ?

**BFC(Block formatting context)直译为"块级格式化上下文"。它是一个独立的渲染区域，只有Block-level box参与， 它规定了内部的Block-level Box如何布局，并且与这个区域外部毫不相干。**



### 3. BFC布局规则

- 内部的Box会在垂直方向，一个接一个地放置。
- Box垂直方向的距离由margin决定。属于同一个BFC的两个相邻Box的margin会发生重叠
- 每个元素的margin box的左边， 与包含块border box的左边相接触(对于从左往右的格式化，否则相反)。即使存在浮动也是如此。
- BFC的区域不会与float box重叠。
- BFC就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素。反之也如此。
- 计算BFC的高度时，浮动元素也参与计算



### 4. 哪些元素会生成BFC ?

- 根元素html

- float属性不为none

- position为absolute或fixed

- display为inline-block, table-cell, table-caption, flex, inline-flex

- overflow不为visible

  参考文档：https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS/Block_formatting_context



### 5. BFC作用及原理

- **自适应两栏布局**

  ```
  <style>
      body {
          width: 300px;
          position: relative;
      }
   
      .aside {
          width: 100px;
          height: 150px;
          float: left;
          background: #f66;
      }
   
      .main {
          height: 200px;
          background: #fcc;
      }
  </style>
  <body>
      <div class="aside"></div>
      <div class="main"></div>
  </body>
  ```

  效果

  ![image-20201119144034636](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201119144034636.png)

  **根据`BFC`布局规则第3条：**

  > **每个元素的margin box的左边， 与包含块border box的左边相接触(对于从左往右的格式化，否则相反)。即使存在浮动也是如此。**

  **因此，虽然存在浮动的元素aslide，但main的左边依然会与包含块的左边相接触。**

  **根据`BFC`布局规则第四条：**

  > **`BFC`的区域不会与`float box`重叠。**

  **我们可以通过通过触发main生成`BFC`， 来实现自适应两栏布局。**

  ```
  .main {
      overflow: hidden;
  }
  ```

  **当触发main生成`BFC`后，这个新的`BFC`不会与浮动的aside重叠。因此会根据包含块的宽度，和aside的宽度，自动变窄。效果如下：**

  ![image-20201119144224710](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201119144224710.png)

  

- **清除内部浮动**

  ```
  <style>
      .par {
          border: 5px solid #fcc;
          width: 300px;
      }
   
      .child {
          border: 5px solid #f66;
          width:100px;
          height: 100px;
          float: left;
      }
  </style>
  <body>
      <div class="par">
          <div class="child"></div>
          <div class="child"></div>
      </div>
  </body>
  ```

  页面效果：

  ![image-20201119144318047](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201119144318047.png)

  **根据`BFC`布局规则第六条：**

  > **计算`BFC`的高度时，浮动元素也参与计算**

  **为达到清除内部浮动，我们可以触发par生成`BFC`，那么par在计算高度时，par内部的浮动元素child也会参与计算。**

  **代码：**

  ```
  .par {
      overflow: hidden;
  }
  ```

  页面效果：

  ![image-20201119144402603](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201119144402603.png)

  

- **防止垂直 margin 重叠**

  ```
  <style>
      p {
          color: #f55;
          background: #fcc;
          width: 200px;
          line-height: 100px;
          text-align:center;
          margin: 100px;
      }
  </style>
  <body>
      <p>Haha</p>
      <p>Hehe</p>
  </body>
  ```

  页面效果：

  ![image-20201119144447830](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201119144447830.png)

  **两个p之间的距离为100px，发送了margin重叠。**
  **根据BFC布局规则第二条：**

  > **`Box`垂直方向的距离由margin决定。属于同一个`BFC`的两个相邻`Box`的margin会发生重叠**

  **我们可以在p外面包裹一层容器，并触发该容器生成一个`BFC`。那么两个P便不属于同一个`BFC`，就不会发生margin重叠了。**
  **代码：**

  ```
  <style>
      .wrap {
          overflow: hidden;
      }
      p {
          color: #f55;
          background: #fcc;
          width: 200px;
          line-height: 100px;
          text-align:center;
          margin: 100px;
      }
  </style>
  <body>
      <p>Haha</p>
      <div class="wrap">
          <p>Hehe</p>
      </div>
  </body>
  ```

  页面效果：

  ![image-20201119144527487](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201119144527487.png)



### 6. 总结

**其实以上的几个例子都体现了`BFC`布局规则第五条：**

> **`BFC`就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素。反之也如此。**

**因为`BFC`内部的元素和外部的元素绝对不会互相影响，因此， 当`BFC`外部存在浮动时，它不应该影响`BFC`内部Box的布局，`BFC`会通过变窄，而不与浮动有重叠。同样的，当`BFC`内部有浮动时，为了不影响外部元素的布局，`BFC`计算高度时会包括浮动的高度。避免margin重叠也是这样的一个道理。**





## 十五、CSS3

### 15.1 CSS3 简介

CSS3是CSS的第三个版本，也是目前最新的版本。添加一些新的特性，如：

- 新增选择器：属性选择器、结构性伪类选择器、伪元素等等
- 新增属性：border-radius  backgound-size  box-sizing等等...
- 新增渐变色：之前都是使用图片进行平铺操作，使用渐变色可以减少服务器压力和带宽，加快页面渲染
- 新增变形：平移 缩放 旋转  倾斜等  2d变形和3d变形
- 新增过渡：从一种效果过渡到另外一种效果
- 新增动画：
- 新增媒介查询
- 新增flex布局 

### 15.2 CSS3 新增属性介绍

#### 15.2.1 新增盒子阴影、文字阴影

- **盒子阴影**

  ```
  box-shadow: h-shadow v-shadow blur spread color inset;
       h-shadow	必需。水平阴影的位置。允许负值。	
       v-shadow	必需。垂直阴影的位置。允许负值。	
       blur		可选。模糊距离。
       spread		可选。阴影的尺寸。
       color		可选。阴影的颜色。请参阅 CSS 颜色值。	
       inset		可选。将外部阴影 (outset) 改为内部阴影。
  ```

  > 注：box-shadow 向框添加一个或多个阴影。该属性是由逗号分隔的阴影列表，每个阴影由 2-4 个长度值

  ![image-20201119163659387](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201119163659387.png)

  

- **文字阴影**

  ```
  text-shadow: h-shadow v-shadow blur color;
  	 h-shadow	必需。水平阴影的位置。允许负值。
       v-shadow	必需。垂直阴影的位置。允许负值。	
  	 blur		可选。模糊的距离。	
  	 color		可选。阴影的颜色。
  ```

  > 注：text-shadow 属性向文本添加一个或多个阴影。该属性是逗号分隔的阴影列表，每个阴影有两个或三个长度值和一个可选的颜色值进行规定。省略的长度是 0

![image-20201119164034403](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201119164034403.png)



#### 15.2.2 新增圆角边框  

border-radius : 固定值 | 百分比（相对父元素）

- 按照值的多少进行分类
  - 单值法 border-radius:10px;  左上角、右上角、右下角、左下角圆角都设置为10像素
  - 二值法 border-radius:10px 20px; 左上角、右下角为10px，右上角、左下角为20px
  - 三值法 border-radius:10px 20px 30px; 左上角10px,右上角、左下角为20px,右下角30px
  - 四值法 border-radius:10px 20px 30px 40px; 从左上角开始顺时针分别设置10px、20px、30px、40px

- 按照四个边角进行分类
  - border-top-left  设置左上角
  - border-top-right  设置右上角
  - border-bottom-right 设置右下角
  - border-bottom-left 设置左下角



**圆形：**首先元素必须是正方形，然后设置圆角边框像素值为元素（标准盒）宽或高的一半，但真正好用的是使用百分比50%（不受padding、border影响）

**其它图形：**

![img](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/clip_image002-1605769490470.jpg)



**HTML结构：**

```
<div class="box"></div>
<div class="box2"></div>
<div class="box3"></div>
<div class="box4"></div>
<div class="box5"></div>
<div class="box6"></div>
```

**CSS样式：**

```
div{
    display: inline-block;
    height: 100px;
    width: 100px;

    margin: 20px;
    padding: 20px;
}
.box{ 
    /* 填充 背景 */
    background-color: red;
    /* 设置圆角边框 */
    border-radius: 50%;
}
.box2{
    /* 描边 边框 */
    border: solid 10px purple;
    /* 标准盒  边框盒内填充会撑大盒子 */
    /* 设置圆角边框 */
    border-radius: 50%;
}
.box3{
    background-color: yellow;
    border-radius: 30px;
}
.box4{
    width: 500px;
    /* 设置短边和宽度一致  或者是大于短边 */
    border-radius: 100px;
    background-color: pink;
}
.box5{
    width: 500px;
    border-radius: 100px 250px;
    background-color: orange;
}
.box6{
    width: 100px;
    border-radius:140px 160px 149px 0px;
    background-color: orange;
}
```

 

#### 2.2.3 新增线性渐变和径向渐变

CSS3 渐变（gradients）可以让你在两个或多个指定的颜色之间显示平稳的过渡；在以前，你必须使用图像来实现这些效果。

通过使用 CSS3 渐变（gradients），你可以减少下载的事件和宽带的使用。

渐变效果的元素在放大时看起来效果更好，因为渐变（gradient）是由浏览器生成的。

**CSS3 定义了两种类型的渐变（gradients）：**

- 线性渐变(Linear Gradients）

  想要创建一个线性渐变，你必须至少定义两种颜色结点(即你想要呈现平稳过渡的颜色)。同时，你也可以设置一个起点和一个方向(或一个角度)

  ```
  //浏览器兼容 写法
  background-image: -webkit-linear-gradient(direction, color-stop1, color-stop2, ...);
  background-image: -moz-linear-gradient(direction, color-stop1, color-stop2, ...);
  background-image: -o-linear-gradient(direction, color-stop1, color-stop2, ...);
  /*direction的值的写法为 top、right、bottom、left、left top、right bottom等等,为起始方向*/
  
  //标准写法
  background-image: linear-gradient(direction, color-stop1, color-stop2, ...);
  /*direction的值的写法为 to top、to right、to left、to bottom right等等，为结束方向*/
  ```

  ![image-20201119163457835](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201119163457835.png)

- 径向渐变（Radial Gradients）

  为了创建一个径向渐变，你也必须至少定义两种颜色结点。颜色结点即你想要呈现平稳过渡的颜色。同时，你也可以指定渐变的中心、形状（圆形或椭圆形）、大小。默认情况下，渐变的中心是 center（表示在中心点），渐变的形状是 ellipse（表示椭圆形），渐变的大小是 farthest-corner（表示到最远的角落）。

  ```
  语法：background: radial-gradient(center, shape size, start-color, ..., last-color);
  举例：
  	background: radial-gradient(red, green, blue);   颜色结点均匀分布（默认情况下）  
  	background: radial-gradient(red 5%, green 15%, blue 60%);  颜色结点不均匀分布            
  	background: radial-gradient(red, yellow, green);  默认椭圆 Ellipse 
  	background: radial-gradient(circle, red, yellow, green);  设置圆形 Circle 
      
      background: radial-gradient(circle at top, red, yellow, green);  设置从顶部开始渐变
  ```

  **定义渐变的位置。可能值**：

  - center（默认）：设置中间为径向渐变圆心的纵坐标值。
  - top：设置顶部为径向渐变圆心的纵坐标值。
  - bottom：设置底部为径向渐变圆心的纵坐标值。

![image-20201119163513481](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201119163513481.png)



#### 15.2.4 新增多列

- column-count   指定需要分割的列数
- column-gap   指定列与列之间的空隙
- column-rule-style   列与列之间的边框样式
- column-rule-width   两列的边框厚度
- column-rule-color   两列的边框颜色
- column-rule    是以上多种列样式的符合简写属性
- column-span   元素跨列合并
- column-width   列宽度

![image-20201119164127405](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201119164127405.png)



#### 15.2.5 CSS3属性需要做浏览器兼容，浏览器前缀如下

- -webkit-  谷歌Chrome或者苹果Safari
- -ms-         微软IE
- -moz-       火狐Firefox
- -o-            欧朋Opera



### 15.3 CSS3 新增选择器 

- 属性选择器

  ```
  E[att]			匹配含有att属性的E元素
  E[att=value]	匹配属性att值为value的E元素
  
  E[att~=value]	匹配属性att值包含value的E元素
  E[att|=value]	匹配属性att值以value开头的E元素，开头的只能是独立的单词  或者  val-  开头才可以
  
  /* 以下是CSS3中新增 */
  E[att^=value]	匹配属性att值以value开头的E元素
  E[att$=value]	匹配属性att值以value结尾的E元素
  E[att *= value] 匹配属性att的值包含value的元素
  ```

- 儿子序选择器

  ```
  E:fisrt-child		作为父元素的第一个子元素的元素E。与E:nth-child(1)等同
  E:last-child	    作为父元素的最后一个子元素的元素E。与E:nth-last-child(1)等同
  E F:nth-child(n)	选择父元素E的第n个子元素F。其中n可以是整数（1，2，3）、关键字（even，odd）、可以是公式（2n+1）,而且n值起始值为1，而不是0.
  E F:nth-last-child(n)	选择父元素E的倒数第n个子元素F，其中：nth-last-child(1)始终匹配最后一个元素，与last-child等同
  ```

  > 注意：儿子序选择器受其它元素排名的影响，是所有同级元素的一个大排名

- 儿子类型序选择器

  ```
  E:first-of-type  匹配符合条件的第一个元素
  E:last-of-type   匹配符合条件的最后一个元素
  E:nth-of-type(n)  匹配符合条件的第n个元素，n的值同上
  E:nth-last-of-type(n) 匹配符合条件的倒数第n个元素，n的值同上
  ```

  > 注意：儿子类型不受其它元素的影响，匹配的是同种类型的符合条件的元素

- 表单相关的 UI 状态伪类选择器

  ```
  E:checked	选中状态伪类选择器	匹配选中的复选按钮或者单选按钮表单元素
  E:enabled	启用状态伪类选择器	匹配所有启用的表单元素
  E:disabled	不可用状态伪类选择器	匹配所有禁用的表单元素(配合disabled使用)
  ```

- 否定伪类选择器

  ```
  E:not(F) 匹配所有除元素F外的E元素
  
  //例子:匹配所有除p标签外的所有标签
  h1:not(p) {
      color: #ff0000;
  }
  ```

- 伪元素选择器

  ```
  :first-line   // 为某个元素的第一行文字使用样式
  :first-letter // 为某个元素中的文字的首字母或第一个字使用样式
  :before // 在某个元素之前插入一些内容 需要配合content属性进行使用
  :after  // 在某个元素之后插入一些内容 需要配合content属性进行使用
  ```

  



![Video_2020-11-20_093900](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/Video_2020-11-20_093900.gif)

## 十六、变形 transform

transform 属性应用于元素的2D或3D转换。这个属性允许你将元素旋转，缩放，移动，倾斜等。

变形都是相对于自己本身原来的位置进行转换，原来的位置还占位，只是视觉上的变化。这点来看和相对定位有点类似。

![image-20201120094221579](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201120094221579.png)

#### 16.1 2D 变形 

2d中的坐标系：x 表示正方向向右 y表示正方向向下

- **translate(x,y) 偏移**，值函数，两个参数分别为 x 方向和 y 方向偏移；如果只有一个值，就是代表向 x偏移

  `translateX (x)`   X 方向偏移
  `translateY (y)`   Y 方向偏移

  ```
  /* 向下偏移100px */
  /* transform: translateY(100px); */
  /*  向右偏移200px*/
  /* transform: translateX(200px); */
  /* 同时设置向下偏移100px向右偏移200px */
  /* transform: translate(200px,100px) */
  
  transform: translate(100px);
  ```

- **scale(x,y) 缩放**，两个参数分别为x方向和y方向缩放值；如果只有一个值，代表元素两个方向的缩放值

  `scaleX(x)`  X 方向缩放

  `scaleY(y)`  Y 方向缩放

  ```
  /* x方向缩小一半 */
  /* transform: scaleX(0.5); */
  /* y方向变大一半 */
  /* transform: scaleY(2); */
  
  /* 设置x、y方向的缩放值 */
  /* transform: scale(0.9,0.5); */
  
  transform: scale(0.5);
  ```

- **skew(x deg,  y deg); 倾斜**，定义沿着 X 和 Y 轴的 2D 倾斜转换

  `skewX()`

  `skewY()` 

  ```
  /* x方向倾斜30deg */
  /* transform: skewX(30deg); */
  
  /* y方向倾斜30deg */
  /* transform: skewY(60deg); */
  
  transform: skewX(30deg);
  ```

- **rotate(z deg) 旋转**  定义 2D 旋转，在参数中规定角度

  `rotateX() x轴旋转`

  `rotateY() y轴旋转`

  `rotateZ() z旋转，平面旋转`

  ```
  /* x轴旋转30deg */
  /* transform: rotateX(30deg); */
  /* y轴旋转30deg */
  /* transform: rotateY(60deg); */
  
  transform: rotateZ(60deg)
  ```

#### 16.2 改变变形中心点 

transform-origin 属性允许您更改转换元素的位置

```
transform-origin: x-axis y-axis z-axis;
```

- x-axis 定义视图被置于 X 轴的何处。可能的值：left center right  固定值  百分比
- y-axis 定义视图被置于 Y 轴的何处。可能的值：top center bottom  固定值  百分比
- z-axis 定义视图被置于 Z 轴的何处。可能的值：固定值

![image-20201120095810374](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201120095810374.png)

> 注：2D转换元素可以改变元素的X和Y轴。 3D转换元素，还可以更改元素的Z轴。



#### 16.3 改变变形类型

transform--style 属性指定嵌套元素是怎样在三维空间中呈现，2D 变形 和 3D 变形，属性值如下

- flat  表示所有子元素在2D平面呈现
- preserve-3d  表示所有子元素在3D空间中呈现

![image-20201120101333110](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201120101333110.png)

#### 16.4 3D 变形相关属性和属性值

3d中的坐标系：x 表示正方向向右 y表示正方向向下 z表示垂直于屏幕

- `perspective` 景深，表示距离屏幕多少像素
- `translate3d(x,y,z)` 
- `translateZ(z)`  属性表示元素沿着自身Z轴移动了多少像素
- `scaleZ(z deg)`
- 

注意：3d 变形需要配合景深使用，给父元素添加 perspective 属性

```
父元素{
	prespective: 101px; // 表示父元素距离屏幕101px的距离，类似于看戏时确定舞台的距离
}
子元素{
	transform: translateZ(100px); // 表示子元素从距离屏幕101px的位置，移动到了距离屏幕1px的位置
}
```



#### 16.5 背面不可见

`backface-visibility : visible(默认，背面可见) | hidden(背面不可见);` 



## 十七、过渡 transition

![111](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/111-1605841347784.gif)

过渡是从一种效果到另外一种效果的演变，需要触发条件，如：鼠标滑过  获取焦点 点击事件等等

两个必要的条件：

​    过渡属性 transition-property

​    过渡的时间 transition-duration

除了以上两个属性：

​    过渡的作用曲线 transition-timing-function

​    过渡的延迟时间 transition-delay



## 十八、动画 animation

![444](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/444.gif)

动画也是从一种效果过渡到另外一种，这个不需要任何触发条件，自动播放；

**两个必要条件**：

​    animation-name	动画的名称

​	animation-duration  动画的过渡时间



**其他属性**：

  animation-delay  动画延迟播放的时间

  animation-timing-function 动画的播放速率，属性值同transition-timing-function

  animation-iteration-count 设置动画的播放次数；可以给数字，如果设置为**infinity** 代表无限次播放

  animation-direction 设置动画播放的方向，属性值如下：

​		normal 正向播放

​		reverse 反向播放

​		alternate 奇数次正向播放，偶数次反向播放

​		alternate-reverse 偶数次正向播放，奇数次反向播放

animation-fill-mode 属性规定当动画不播放时（当动画完成时，或当动画有一个延迟未开始播放时），要应用到元素的样式 属性值 forwards 保留动画最后一帧效果



**动画集规则**：

```
@keyframes name{ 
	from{}  
	to{}
}
```

注意：由于form...to 过渡效果太少，一般我们会利用百分比 0% ， 10%，...,90%,100%呈现更加细腻的动画过程

```
@keyframes name{
    0%{}
    10%{}
    ...
    90%{}
    100%{}
}

```



**动画简写属性** 

```
animation:name duration delay timing-function iteration-count direction;
```



**控制动画的播放状态**

```
animation-play-state: running (默认运动) | paused (停止) ; 
```

如：设置鼠标滑过容器停止动画的播放





## 十九、弹性盒子

![image-20201120114649014](http://121.89.192.46:8888/ganhuo/note/image-20201120114649014.png)

### 19.1 概述

- 弹性盒子是 CSS3 的一种新的布局模式。
- CSS3 弹性盒（ Flexible Box 或flexbox），是一种当页面需要适应不同的屏幕大小以及设备类型时确保元素拥有恰当的行为的布局方式。
- 引入弹性盒布局模型的目的是提供一种更加有效的方式来对一个容器中的子元素进行排列、对齐和分配空白空间。
- 弹性盒子由弹性容器(Flex container)和弹性子元素(Flex item)组成。



### 19.2 弹性盒组成 

- 弹性盒容器：通过设置 display 属性的值为 flex 或 inline-flex 将其定义为弹性容器。
  - 弹性容器内包含了一个或多个弹性子元素。
  - 弹性容器外及弹性子元素内是正常渲染的(即盒子内外其它元素属性效果)。弹性盒子只定义了弹性子元素如何在弹性容器内布局。
  - 弹性子元素通常在弹性盒子内一行显示。默认情况每个容器只有一行。但是可以通过设置 `direction` 属性值为 `rtl` , 使弹性子元素的排列方式发生改变，页面布局也跟着改变(改变子元素的排列方式);

- 弹性子元素:盒子里面的元素



### 19.3 弹性盒容器六大属性介绍 

- `flex-direction` 指定了弹性子元素在父容器中的位置，属性值如下

  - row：横向从左到右排列（左对齐），默认的排列方式。
  - row-reverse：反转横向排列（右对齐，从后往前排，最后一项排在最前面。
  - column：纵向排列。
  - column-reverse：反转纵向排列，从后往前排，最后一项排在最上面。

- `flex-wrap:wrap` 设置盒子内部元素的换行方式，在页面缩放时，水平方向溢出部分可以进行换行

- `flex-flow` 复合属性，用于同时设置子元素的位置和换行方式

  > 注意：如果元素不是弹性盒对象的元素，则 flex-flow 属性不起作用。

- `justify-content` 应用在弹性容器上，把弹性项沿着弹性容器的主轴线（main axis）对齐，属性值如下

  - flex-start：弹性项目向行头紧挨着填充。这个是默认值。	
  - flex-end：弹性项目向行尾紧挨着填充。
  - center：弹性项目居中紧挨着填充。
  - space-between：弹性项目平均分布在该行上。
  - space-around：弹性项目平均分布在该行上，两边留有一半的间隔空间。

- `align-items` 设置或检索弹性盒子元素在侧轴（纵轴）方向上的对齐方式，属性值如下

  - flex-start：弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴起始边界。
  - flex-end：弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴结束边界。
  - center：弹性盒子元素在该行的侧轴（纵轴）上居中放置。（如果该行的尺寸小于弹性盒子元素的尺寸，则会向两个方向溢出相同的长度）。

- align-content:类似于justify-content，子元素根据设置的属性值在Y方向进行不同的排列方式，属性值如下

  - stretch - 默认。各行将会伸展以占用剩余的空间。
  - flex-start - 各行向弹性盒容器的起始位置堆叠。
  - flex-end - 各行向弹性盒容器的结束位置堆叠。
  - center -各行向弹性盒容器的中间位置堆叠。
  - space-between -各行在弹性盒容器中平均分布。
  - space-around - 各行在弹性盒容器中平均分布，两端保留子元素与子元素之间间距大小的一半



### 19.4 弹性项六大属性介绍 

- order 排序。属性值为整数，用整数值来定义排列顺序，数值小的排在前面。可以为负值
- align-self:用于设置弹性元素自身在侧轴（纵轴）方向上的对齐方式
  - auto：如果'align-self'的值为 auto，则其计算值为元素的父元素的 align-items 值，如果其没有父元素，则计算值为 stretch。
  - flex-start：弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴起始边界。
  - flex-end：弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴结束边界。
  - center：弹性盒子元素在该行的侧轴（纵轴）上居中放置。（如果该行的尺寸小于弹性盒子元素的尺寸，则会向两个方向溢出相同的长度）。
  - baseline：如弹性盒子元素的行内轴与侧轴为同一条，则该值与'flex-start'等效。其它情况下，该值将参与基线对齐。
  - stretch：如果指定侧轴大小的属性值为'auto'，则其值会使项目的边距盒的尺寸尽可能接近所在行的尺寸，但同时会遵照'min/max-width/height'属性的限制。
- flex-grow 属性用于设置或检索弹性盒的扩展比率，属性值为数字即可，默认值是 0
- flex-shrink 属性指定了 flex 元素的收缩规则。flex 元素仅在默认宽度之和大于容器的时候才会发生收缩，其收缩的大小是依据 flex-shrink 的值。
- flex-basis 属性用于设置或检索弹性盒伸缩基准值 属性值一个长度单位或者一个百分比，规定灵活项目的初始长度
- flex:指定弹性子元素如何分配空间，即所占比重，一般设置为数值即可；可以作为flex-grow、flex-shrink、flex-basis元素的简写方式：



**设置元素垂直居中**：

- 块元素垂直居中问题采用 flex 解决
- 行内元素垂直居中问题解决如下
  - 单行 该元素 `css` 属性 line-height 的值与该元素的父级元素 `css` 属性 height 一致即可
  - 多行 设置该元素 `css` 属性：**display: table-cell; vertical-align: middle;**，还需设置该元素的父级元素 `css` 属性：**display: table;**



## 二十、固比固布局

**三栏布局 左右固定 中间自适应**

- 使用浮动实现：左 float + 右 float + 中 设为 BFC（`overflow:hidden`）

  HTML结构：

  ```
  <div class="left">左</div>
  <div class="right">右</div>
  <div class="main">content area</div>
  ```

  CSS样式：

  ```
  .container {
      height:100%;
  
      .left {
          float: left;
          height: 100%;
          width:100px;
          background-color:lightblue;
      }
      .right {
          float: right;
          height: 100%;
          width:100px;
          background-color:lightgreen;
      }
      .main {
          height:100%;
          overflow:hidden;
          background-color:lightpink;
      }
  }
  ```

  

- 使用定位实现  左`absolute` + 右 `absolut` + 中 `margin`

  上面 HTML 结构 left right 和 main，顺序可以随意调换

  CSS代码：

  ```
  .container {
      height:100%;
      position:relative;
  
      .left {
          position:absolute;
          left:0;
          top:0;
          height: 100%;
          width:100px;
          background-color:lightblue;
      }
      .right {
          position:absolute;
          right:0;
          top:0;
          height: 100%;
          width:100px;
          background-color:lightgreen;
      }
      .main {
          height:100%;
          margin:0 100px;
          background-color:lightpink;
      }
  }
  ```

  

- 使用弹性盒子实现

  HTML代码:

  ```
  <div class="wrap">
      <aside class="left">左边栏</aside>
      <div class="center">中间栏</div>
      <aside class="right">右边栏</aside>
  </div>
  ```

  CSS代码：

  ```
  .wrap{
      /*设置父元素为弹性盒*/
      display: flex;
      height: 400px;
      background-color: lightgray;
  }
  
  .left{
      width: 260px;
      height: 100%;
      background-color: red;
  }
  
  .center{
      width: 320px;
      height: 120%;
      /*设置弹性子元素的属性,对剩余空白空间的分配比重*/
      flex: 1;
      background-color: #00b1e8;
  }
  
  .right{
      width: 320px;
      height: 100%;
      background-color: yellow;
  }
  ```

  

## 二十一、双飞翼 和 圣杯布局

在面试时，你会经常遇到那么一个考题?有left、right、container三个盒子，要求left与right盒子宽度固定，分别固定于浏览器两侧，container位于中间，
宽度随浏览器窗口自适应；说白了，就是要你进行两边定宽，中间自适应的三栏布局，并且中间栏要放在文档流前面以优先渲染。而圣杯布局与双飞翼布局就是用
来解决这个问题最常见的布局方法。

圣杯布局的出现是来自于a list part上的一篇文章In Search of the Holy Grail。比起双飞翼布局，它的起源不是源于对页面的形象表达。在西方，圣杯是
表达“渴求之物”的意思。而双飞翼布局则是源于淘宝的UED，可以说是灵感来自于页面渲染

圣杯布局和双飞翼布局基本上是一致的，都是两边固定宽度，中间自适应的三栏布局，其中，中间栏放到文档流前面，保证先行渲染。解决方案大体相同，都是三
栏全部float:left浮动，区别在于解决中间栏div的内容不被遮挡上，圣杯布局是中间栏在添加相对定位，并配合left和right属性，效果上表现为三栏是单独分
开的（如果可以看到空隙的话），而双飞翼布局是在中间栏的div中嵌套一个div，内容写在嵌套的div里，然后对嵌套的div设置margin-left和margin-right，
效果上表现为左右两栏在中间栏的上面，中间栏还是100%宽度，只不过中间栏的内容通过margin的值显示在中间。

简单说起来就是:双飞翼布局比圣杯布局多创建了一个div，但不用相对布局了。

双飞翼布局的好处：

- 主要的内容先加载的优化
- 兼容目前所有的主流浏览器，包括IE6在内
- 实现不同的布局方式，可以通过调整相关CSS属性即可实现

参考资料：

- 圣杯布局的来历是2006年发在a list part上的这篇文章：http://alistapart.com/article/holygrail
- 双飞翼布局介绍-始于淘宝UED：http://www.imooc.com/wenda/detail/254035
- 还有这里的一篇两者的比较：http://www.cnblogs.com/imwtr/p/4441741.html
- 双飞翼布局实战：http://www.jikexueyuan.com/course/981.html





## 前言

### 1. 布局介绍

布局:layout 对事物的全面规划和安排

页面布局：对页面的文字、图形或表格进行格式设置。包括字体、字号、颜色纸张大小和方向以及[页边距](https://baike.baidu.com/item/页边距)等。

网页布局：利用html搭建结构与内容，使用CSS添加装饰

网页布局有很多种方式，一般分为以下几个部分：头部区域、菜单导航区域、内容区域、底部区域。

![img](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/clip_image002.jpg)

**注：**所有的页面布局都是基于盒子模型基础之上进行布置。

### 2. 目前常用的网页布局

1. **固定布局(最基本的布局)**

2. **流式布局（百分比布局）**

   流式布局也叫百分比布局。把元素的宽,高,margin,padding不再用固定数值,改用百分比,这样元素的高,margin,padding会根据页面的尺寸随时调整，以达到适应当前页面的目的。

   需要注意的是：

   * 百分比是基于元素父级的大小计算得来的；
   * 元素的水平或者竖直间距都是相对于父级的宽度计算的.(margin&padding)
   * 边框不能用百分比设置

   优缺点：

   ​	以百分比为主要形式，让屏幕自适应，这种布局方式定义灵活，能够根据屏幕的情况变化，但是这种方式设计的效果不太容易控制，一般移动端结合 rem 的比较多，pc端用的不是非常多。

3. **弹性布局（伸缩布局）**

   CSS3引入了一种新的布局模式——Flexbox布局，即伸缩布局盒模型（FlexibleBox），用来提供一个更加有效的方式制定、调整和分布一个容器里项目布局，即使它们的大小是未知或者动态的，这里简称为Flex。

   Flexbox布局常用于设计比较复杂的页面，可以轻松的实现屏幕和浏览器窗口大小发生变化时保持元素的相对位置和大小不变，同时减少了依赖于浮动布局实
   现元素位置的定义以及重置元素的大小

   Flexbox布局在定义伸缩项目大小时伸缩容器会预留一些可用空间，让你可以调节伸缩项目的相对大小和位置。例如，你可以确保伸缩容器中的多余空间平均
   分配多个伸缩项目，当然，如果你的伸缩容器没有足够大的空间放置伸缩项目时，浏览器会根据一定的比例减少伸缩项目的大小，使其不溢出伸缩容器。综合
   而言，Flexbox布局功能主要具有以下几点：

   - 第一，屏幕和浏览器窗口大小发生改变也可以灵活调整布局；
   - 第二，可以指定伸缩项目沿着主轴或侧轴按比例分配额外空间（伸缩容器额外空间），从而调整伸缩项目的大小；
   - 第三，可以指定伸缩项目沿着主轴或侧轴将伸缩容器额外空间，分配到伸缩项目之前、之后或之间；
   - 第四，可以指定如何将垂直于元素布局轴的额外空间分布到该元素的周围；
   - 第五，可以控制元素在页面上的布局方向；
   - 第六，可以按照不同于文档对象模型（DOM）所指定排序方式对屏幕上的元素重新排序。也就是说可以在浏览器渲染中不按照文档流先后顺序重排伸缩项目顺序。

   Flexbox规范版本众多，浏览器对此语法支持度也各有不同

4. **浮动布局**

   此布局上述都有演示浮动布局，此处就不做代码演示，浮动布局关键词，float，可以设置left或者right，他使元素脱离文档流进而达到布局的目的，也是目前
   一个比较主流的布局方式，但是使用浮动的结束以后，别忘记清除浮动

5. **定位布局**

   定位布局也是目前比较常用的一种布局方式，关键词：

   - position: fixed; 固定布局，将元素固定在一个位置，不随页面移动而移动
   - position: relative; 相对定位，相对于元素自身定位，不脱离文档流，相当于定义一个参照物，一般和绝对定位结合使用
   - position: absolute;绝对定位，脱离文档流，一般和相对定位结合使用，如果不定义相对定义，将会相对于整个浏览器定位，所以定位布局，一般情况下都是相对定位和绝对定位结合着来，相当定位相当于划定一个势力范围，制定一个封闭的容器块，然后绝对定位就行对于相对定位来定位，从而达到有效的布局。

6. **响应式布局**

   使用@media媒体查询给不同尺寸和介质的设备切换不同的样式。优秀的响应范围设计可以给适配范围内的设备做好的体验

7. **rem布局(移动端)**

   CSS3新出现的rem布局。原理是，先按定高宽设计出来页面，然后转换为rem单位，配合js查询屏幕大小来改变html的font-size，最终做出所谓的完美自适应。



## 二十二、响应式布局

#### 22.1 响应式布局概述 

- **历史由来：**

  响应式布局是 Ethan Marcotte 在2010年5月份提出的一个概念，简而言之，就是一个网站能够兼容多个终端，而不是为每个终端做一个特定的版本。这个概念是为解决移动互联网浏览而诞生的。

- **概念**

  响应式布局可以为不同终端的用户提供更加舒适的界面和更好的用户体验，而且随着目前大屏幕移动设备的普及，用“大势所趋”来形容也不为过。随着越来越多的设计师采用这个技术，我们不仅看到很多的创新，还看到了一些成形的模式。

- **优势与不足：**

  响应式布局解决了不同设备之间的差异化展示，让一个网站可以兼容不同分辨率的设备，给用户更好的视觉使用体验。但是同时也存在一些不足，如：兼容性代码多，工作量大，加载速度受影响

- **响应式网页设计的实现思路及优缺点**

  - Css3-Media Quary  最简单的方式(手持设备一般都支持，传统PC端老版本浏览器不一定支持)
  - 不支持Css3的浏览器使用js实现    成本高，不推荐使用
  - 使用第三方的开源框架(例如：BootStrap(推特)、UIKit)  可以很好的支持浏览器响应式布局的设计

- **响应式设计的原则**

  - 移动优先：在设计初期就要考虑页面如何让在多终端展示。做响应式网站的时候，一定要在页面头部加入如下的声明

    ```
    <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0,user-scalable=no">
    ```

    width=device-width 样式中定义的宽度等于设备中定义的宽度

    initial-scale=1.0 缩放比例1

    minimum-scale=1.0 最大缩小比例1

    maximum-scale=1.0 最大放大比例1

    > **注**：在 HTML 中，meta 标签没有结束标签，meta标签定义了与文档相关联的名称或值。可提供有关页面的元信息。

  - 渐进增强：充分发挥硬件设备的硬件功能(例如最新的浏览器支持Css3动画可以增加用户的体验)



#### 22.2 媒介查询 Media Quary

- **媒介查询的概念**

  1. 媒体查询可以让我们根据设备显示器的特性（如视口宽度、屏幕比例、设备方向：横向或纵向）为其设定CSS样式，媒体查询由媒体类型和一个或多个检测媒体特性的条件表达式组成。
  2. 媒体查询中可用于检测的媒体特性有 width、height 和 color ( 等 )。使用媒体查询，可以在不改变页面内容的情况下，为特定的一些输出设备定制
     显示效果。

- **媒介查询的意义**

  如果没有CSS3的媒体查询模块，就不能针对设备特性（如视口宽度）设置特定的CSS样式

- **媒介查询的实现**

  - 媒体查询写在CSS样式代码的最后，CSS是层叠样式表，在同一特殊性下，靠后的的样式会重叠前面的样式

  - 首先需要在html文档中添加以下代码，用来兼容移动设备的显示效果		

    ```
    <meta name="viewport content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no"/>
    ```

    width=device-width:宽度等于当前设备的宽度

    initial-scale=1：初始的缩放比例（默认为1）

    maximum-scale=1：允许用户缩放到得最大比例（默认为1）

    user-scalable=no：用户不能手动缩放	

  - 在CSS文件中写CSS响应式媒体查询,有以下几种写法

    - 使用link引入css文件

      ```
      <link type="text/css" rel="stylesheet" href="" media="only screen and (max-width:480px)"/>
      ```

    - 在链接式的 css 文件中限定屏幕尺寸

      ```
      <link type="text/css" rel="stylesheet" href=""/>
      ```

      css 文件代码：

      ```
      @media only screen and (max-width:480px){
          样式:样式值;
      }
      @media only screen and (min-width:900px){
          样式:样式值;
      }
      ```

    - 嵌入式css文件中限定屏幕尺寸

      ```
      <style type=text/css>
          @media only screen and (max-width:480px){
              样式:样式值;
          }
          @media only screen and (min-width:900px){
              样式:样式值;
          }
      </style>
      ```

    - 导入式

      ```
      <style type="text/css" media="screen and (min-width:600px) and (max-width:900px)">  
          @import url("css/style.css");  
      </style>  
      ```

  

- **常见属性介绍**

  - device-width，device-height  屏幕宽高(设备物理宽高)
  - width，height  渲染窗口(可视区域如浏览器窗口)宽高
  - viewport  视口
  - content  内容
  - initial-scale  初始-比例
  - minimum-scale  最小-比例
  - maximum-scale  最大-比例
  - media  媒体
  - query  查询
  - orientation   设备方向(横屏、竖屏)
  - resolution	 设备分辨率(分辨率由dpi决定)

  

## 二十三、Bootstrap

官网：https://www.bootcss.com/

![image-20201120170204615](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201120170204615.png)

### 23.1 概述

bootstrap 是世界上最受欢迎的前端框架，用于构建响应式、移动设备优先的网站。

bootstrap分为“全局css样式”、“组件”、“javascript插件”这么几个主要的部分。

​     设置全局 css 样式：基本的 html 元素均可以通过 class 设置样式并得到增强效果；还有先进的栅格系统。

​     组件：无数可复用的组件，包括字体图标、下拉菜单、导航、警告框、弹出框等更多功能。

​     javascript插件：jquery 插件为 bootstrap 的组件赋予了“生命”。可以简单地一次性引入所有插件，或者逐个引入到你的 页面中。



### 23.2 Bootstrap 引入方式介绍 

npm 需要安装环境node.js

cdn 在线方式，需要联网

离线的方式 下载引入自己的网站中



### 23.3 移动设备优先

**Bootstrap 是移动设备优先的**。为了确保适当的绘制和触屏缩放，需要在 `<head>` 之中**添加 viewport 元数据标签**。

```
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">
```



### 23.4 全局 CSS 样式介绍

1. **容器**

   类名 .container 根据不同视口给出不同的方案，但是都是页面居中的效果

   类名 .container-fluid 宽度百分百

   ```
   <div class="container border2">
     <!-- content here -->
     <h1>这是bootstrap</h1>
     <h2>这是bootstrap</h2>
     <h3>这是bootstrap</h3>
     <h4>这是bootstrap</h4>
     <h5>这是bootstrap</h5>
     <h6>这是bootstrap</h6>
   </div>
   ```

   > 注：标题标签单位rem 改变了w3c 标准样式

   

2. **媒体查询**

   在栅格系统中，我们在 Less 文件中使用以下媒体查询（media query）来创建关键的分界点阈值。

   ```
   /* 超小屏幕（手机，小于 768px） */
   /* 没有任何媒体查询相关的代码，因为这在 Bootstrap 中是默认的（还记得 Bootstrap 是移动设备优先的吗？） */
   
   /* 小屏幕（平板，大于等于 768px） */
   @media (min-width: @screen-sm-min) { ... }
   
   /* 中等屏幕（桌面显示器，大于等于 992px） */
   @media (min-width: @screen-md-min) { ... }
   
   /* 大屏幕（大桌面显示器，大于等于 1200px） */
   @media (min-width: @screen-lg-min) { ... }
   ```

   我们偶尔也会在媒体查询代码中包含 `max-width` 从而将 CSS 的影响限制在更小范围的屏幕大小之内

   ```
   @media (max-width: @screen-xs-max) { ... }
   @media (min-width: @screen-sm-min) and (max-width: @screen-sm-max) { ... }
   @media (min-width: @screen-md-min) and (max-width: @screen-md-max) { ... }
   @media (min-width: @screen-lg-min) { ... }
   ```

   

3. **栅格参数**

   通过下表可以详细查看 Bootstrap 的栅格系统是如何在多种屏幕设备上工作的。

   | 超小屏幕 手机 (<768px) | 小屏幕 平板 (≥768px)       | 中等屏幕 桌面显示器 (≥992px)                        | 大屏幕 大桌面显示器 (≥1200px) |            |
   | :--------------------- | :------------------------- | :-------------------------------------------------- | :---------------------------- | ---------- |
   | 栅格系统行为           | 总是水平排列               | 开始是堆叠在一起的，当大于这些阈值时将变为水平排列C |                               |            |
   | `.container` 最大宽度  | None （自动）              | 750px                                               | 970px                         | 1170px     |
   | 类前缀                 | `.col-xs-`                 | `.col-sm-`                                          | `.col-md-`                    | `.col-lg-` |
   | 列（column）数         | 12                         |                                                     |                               |            |
   | 最大列（column）宽     | 自动                       | ~62px                                               | ~81px                         | ~97px      |
   | 槽（gutter）宽         | 30px （每列左右均有 15px） |                                                     |                               |            |
   | 可嵌套                 | 是                         |                                                     |                               |            |
   | 偏移（Offsets）        | 是                         |                                                     |                               |            |
   | 列排序                 | 是                         |                                                     |                               |            |

   

4. **网格布局**

   栅格系统用于通过一系列的行（row）与列（column）的组合来创建页面布局，你的内容就可以放入这些创建好的布局中

   **类名row** 行必须包含在 `.container` （固定宽度）或 `.container-fluid` （100% 宽度）中，以便为其赋予合适的排列（aligment）和内补（padding）

   **类名** **col-** **列、栏**  通过“行（row）”在水平方向创建一组“列（column）” ，内容应当放置于“列（column）”内，并且，只有“列（column）”可以作为行（row）”的直接子元素

   一行一共有12栏，如果一行多余12栏，会自动换行

   **响应式**：

   - .col-
   - .col-sm-
   - .col-md-
   - .col-lg-
   - .col-xl-

   ![image-20201120172149735](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201120172149735.png)

   偏移值：

   - offset- 

   

5. **表格**

   默认样式  .table
   可选样式
   	.table-striped  为表格提供了斑马线的样式
   	.table-bordered  为表格增加边框(border)
   	.table-hover 为表格中的每一行赋予鼠标悬停样式。鼠标划过后会添加一个背景色。
   	.table-condensed 每个单元格的内补(padding)减半，可使表格更紧凑。

   

6. **表单**

   

7. **按钮**

   ![image-20201120172640123](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201120172640123.png)

   

8. **卡片 面包屑**

   ![image-20201120172711953](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201120172711953.png)

   ```
   <div class="container">
       <div class="row">
           <div class="col-4">
               <div class="card" style="width: 18rem;">
                 <img class="card-img-top" src="images/1.jpg" alt="Card image cap">
                 <div class="card-body">
                   <h5 class="card-title">Card title</h5>
                   <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                   <a href="#" class="btn btn-primary">Go somewhere</a>
                 </div>
               </div>
           </div>
           <div class="col-4">
               <div class="card" style="width: 18rem;">
                 <img class="card-img-top" src="images/1.jpg" alt="Card image cap">
                 <div class="card-body">
                   <h5 class="card-title">Card title</h5>
                   <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                   <a href="#" class="btn btn-primary">Go somewhere</a>
                 </div>
               </div>
           </div>
           <div class="col-4">
               <div class="card" style="width: 18rem;">
                 <img class="card-img-top" src="images/1.jpg" alt="Card image cap">
                 <div class="card-body">
                   <h5 class="card-title">Card title</h5>
                   <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                   <a href="#" class="btn btn-primary">Go somewhere</a>
                 </div>
               </div>
           </div>
       </div>
   </div>
   ```

   ![image-20201120172827228](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201120172827228.png)

### 23.4 组件介绍 



### 23.5 JavaScript插件

**轮播图**

![image-20201120172946601](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201120172946601.png)

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<link rel="stylesheet" type="text/css" href="bootstrap-4.0.0-dist/css/bootstrap.css"/>
		<script src="https://cdn.bootcss.com/jquery/3.2.1/jquery.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
		<script src="https://cdn.bootcss.com/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
		<script src="https://cdn.bootcss.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
	</head>
	<body>
		<div class="container">
			<div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
			  <ol class="carousel-indicators">
			    <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
			    <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
			    <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
			  </ol>
			  <div class="carousel-inner">
			    <div class="carousel-item active">
			      <img class="d-block w-100" src="images/1.jpg" alt="First slide">
			    </div>
			    <div class="carousel-item">
			      <img class="d-block w-100" src="images/2.jpg" alt="Second slide">
			    </div>
			    <div class="carousel-item">
			      <img class="d-block w-100" src="images/3.jpg" alt="Third slide">
			    </div>
			  </div>
			  <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
			    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
			    <span class="sr-only">Previous</span>
			  </a>
			  <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
			    <span class="carousel-control-next-icon" aria-hidden="true"></span>
			    <span class="sr-only">Next</span>
			  </a>
			</div>
		</div>
	</body>
</html>
```



## 二十四、移动端布局

### 前奏：视口介绍

**分辨率**：就是屏幕像素的数量，比如1600*900，指的是横向有1600的像素点，纵向有900个像素点。所谓的像素点是物理元件最小的发光单位。

手机的分辨率是多少呢？非常的大：目前主流的分辨率 1920×1080

如果手机真的用自己的真实分辨率，来呈递网页，就是这种情况了：非常像在3000米的高空，俯瞰整个页面。字非常小，h1巨小。

有的同学说，这样挺好，正好可以把整个网页一目了然的看全。乔布斯也这么想。乔布斯说，手机可以呈递电脑网页，但是网页制作者还来不及制作，所以此时我

们如果设置手机的一个宽度为980px，而实际上的网页的版心，绝大多是都是，岂不是手机刚好卡住了整个版心么？乔布斯在iPhone1就命令工程师，把自己的手机的浏览器，认为自己是980px宽，而不是像素宽度，这个宽度就是**视口**。

我们做个实验，用这个**JS语句**测试浏览器的宽度：

```
var h1=document.getElementsByTagName("h1")[0];

h1.innerHTML =document.documentElement.clientWidth;
```

显示980！而iphone的横向的像素数量不是980！

我们发现班级里面所有同学的所有设备，这个测试的结果都是980。

这个数字就是**视口宽度**，viewport。980是所有设备的初始视口宽度。浏览器会以980这个宽度来渲染页面。

也就是说，我们做前端开发的，完全没有必要关心手机的分辨率！

但是980对于手机页面来说，也大。所以乔帮主又做了一个精妙的设计，就是能够让页面的开发者，自定义设置移动设备的视口宽度。

可以用这样的**meta标签**，来设置视口的宽度：

```
<meta name="viewport" content="width=300px" />
```

一旦设置了，浏览器此时就会认为自己的宽度是300px。此时就会按照300px的宽度来渲染页面。这东西太好用了，我们居然可以命令视口认为自己有多宽。

我们发现：不同的视口大小，呈递相同的页面，给人的感觉，是不一样的，尤其是看文字，h1的默认字号32px。如果你的视口是980px，此时看文字非常小。此时如果视口是320左右，此时刚刚好：

此时就有一个换算关系，什么关系呢？

如果让一个300px的盒子，在电脑上看，和在手机上看的物理长度一样！就是我们用尺子量，是一样宽的。

![image-20201216085837130](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201216085837130.png)

此时就有一个**ppi**的事儿。ppi就是pixel per inch。每英尺多少个像素点。比如iphone的ppi是534像素/英尺。

手机ppi >> 电脑ppi。

电脑的分辨率 / 电脑的ppi = 手机的分辨率（视口宽度） / 手机的ppi

A品牌手机的分辨率（或者视口宽度） / 手机ppi = B品牌手机的分辨率（视口宽度） / 手机ppi 

所以任何手机如果想要有显示和计算机一样的宽度，就要根据自己的分辨率、ppi的不同，而设置不同的视口。

如果我们加上：

```
<meta name="viewport" content="width=device-width" />
```

此时每个手机的视口宽度，都是“视口约束宽度”。每个手机的视口约束宽度不一样，这是为了给人看上去的物理感觉是一样的：

各个设备约束视口之后的视口宽度（300-400）

你会发现这个宽度都不一样，但是此时人看上去的感觉是一样的。字号是一样大的。

**做手机页面的时候，一定要加上**

```
<meta name="viewport" content="width=device-width" />
```

此时如果你写一个p的字号为font-size:14px;不用担心用户能不能看清！用户一定能看的真真的！此时厂商已经计算好了一个所谓视口约束宽度。14px和14px的感觉完全一样！

一般来说，手机视口约束之后都是320~420之间。而分辨率基本上都是1000~1200，也就是说，约束视口之后所谓的1px，实际上手机用了2点多个像素来渲染。手机中的图片，必须使用放大两倍的图片缩小使用，这样能精细。

```
<meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0,user-scalable=no" id="viewport" />不用背诵
```

width=device-width    约束视口

initial-scale=1.0  初始视口倍数是1倍

minimum-scale=1.0  最小允许视口宽度是1倍

maximum-scale=1.0 最大允许视口宽度是1倍



### 24.1 px、em、rem、vm 等单位的介绍 

- **背景介绍**

  传统的项目开发中，我们只会用到px、%、em这几个单位，它可以适用于大部分的项目开发，并且拥有比较良好的兼容性。但是你知道吗？从css3开始，浏览器对逻辑单位的支持又提升到了另外一个境界，增加了rem、vh、vw、vm等一些新的长度单位，我们可以利用这些新的单位开发出比较良好的响应式页面，随之覆盖多种不同分辨率的终端，包括移动设备等。现在让我们来看下这些长度单位有什么区别。

- **单位剖析**

  - px 像素单位，英文 pixel 的缩写。px就是一张图片最小的一个点，一张位图就是千千万万的这样的点构成的，比如常常听到的电脑像素是1024x768的，表示的是水平方向是1024个像素点，垂直方向是768个像素点。

  - em 字符单位，参考物是父元素的font-size，具有继承的特点。如果自身定义了font-size按自身来计算（浏览器默认字体是16px），整个页面内 1em 不是一个固定的值。

  - rem CSS3新单位，相对于根元素html（网页）的font-size，不会像em那样，依赖于父元素的字体大小，而造成混乱。

  - %   百分比，一般宽泛的讲是相对于父元素，但是并不是十分准确。

    - 对于普通定位元素就是我们理解的父元素
    - 对于position: absolute;的元素是相对于已定位的父元素
    - 对于position: fixed;的元素是相对于ViewPort（可视窗口）

  - vw  css3新单位，viewpoint width 的缩写，视窗宽度，1vw 等于视窗宽度的1%

    vh  css3新单位，相对于视口的宽度或高度中较小的那个。其中最小的那个被均分为100单位的 vm

    ```
    浏览器宽度1200px, 1vw = 1200px/100 = 12px
    浏览器高度900px, 1vh = 900px/100 = 9px
    ```

    - vh / vw 是不包含页面滚动条的视窗宽度(innerwidth)，% 包含了滚动条的宽度在里面 (outerwidth)
    - 一般的情况下%就可以满足大部分自适应设计的需求，可以用height：100vh做一个高度占满屏幕的自适应，没有滚动条
    - 用vw / vh设定的大小只和视窗大小有关，所以用来开发多种屏幕设备的应用用这个单位还是挺合适的



### 24.2 移动端适配规则介绍

1. 按照设计稿与设备宽度的比例,动态计算并设置html根标签的`font-size`大小;
2. CSS中,设计稿元素的宽、高、相对位置等取值,按照同等比例换算为`rem`为单位的值;

| 技术方案1 |    技术方案2     |
| :-------: | :--------------: |
| 媒体查询  |   flexible.js    |
|    rem    |       rem        |
|   less    | vscode插件cssrem |

```
移动端屏幕宽除以设计图宽得到比例，比如屏幕宽等于750px，设计图宽等于1000px，750除以1000得到0.75px，等于说是设计图的1px，在浏览器上展示的大小为0.75px，这里我们要继承这个比例大小，采用rem的方法，继承html的font-size大小的方法去实现，设置html的font-size等于 0.75px（屏幕的0.75px相当于设计图的1px）,rem会继承html的font-size大小，所以我们在页面里面使用的1rem就等于设计图的1px，后面可以忽略（为了方便我们可以把得到的设计图和屏幕宽的比例乘以100，等于75，现在1rem等于设计图的100px,0.01rem等于设计图的1px。
公式 屏幕宽度 / 设计图宽度 * 100 = html font-size（0.01rem 等于设计图的 1px）
```

> 兼容性：Ios6以上和android2.1以上，基本覆盖所有流行的手机系统



### 24.3 简洁高效的 rem 配方案 flexible.js

- **适配原理**

  手机淘宝团队出的简洁高效移动端适配库
  它的原理是把当前设备划分为10等份,但是不同设备下,比例还是一致的
  我们要做的,就是确定好我们当前设备的html文字大小就可以了
  比如当前设计稿是750px,那么我们只需要把html文字大小设置为 **75px** (750px/ 10) 就可以了
  里面页面元素rem值:页面元素的px值/ 75
  剩余的,让flexible.js来去算

- **页面元素取值公式**

  ① 页面元素的rem值 = 页面元素值(px) / (屏幕宽度/划分的份数))
  ② 屏幕宽度 / 划分的份数就是html的 font-size的大小
  ③ 页面元素的 rem 值 = 页面元素值(px) / html font-size字体大小

- **使用步骤**

  1. **下载 flexible.js**

     github下载地址: [https://github.com/amfe/lib-flexible](https://links.jianshu.com/go?to=https%3A%2F%2Fgithub.com%2Famfe%2Flib-flexible)

  2. **`index.js`中原理是把当前设备划分为10等份**

     ```
     // set 1rem = viewWidth / 10
     function setRemUnit () {
         var rem = docEl.clientWidth / 10
         docEl.style.fontSize = rem + 'px'
     }
     ```

  3. **设置 meta 标签**

     ```
     <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0, user-scalable=no">
     ```

  4. ##### 引入flexible.js

     ```
     <script src='js/flexible.js'></script>
     ```

  5. ##### 初始化style

     ```
     <style>
       /* 如果屏幕超过了750px，那么我们就就按照750px设计稿来走，不会让页面超过750px ,使用媒体查询来设置*/
       @media screen and (min-width: 750px) {
         html {
           font-size: 75px !important;
         }
       }
       
       body {
         min-width: 320px;
         max-width: 750px;
        /* flexible.js把设计稿750px进行10等分，所以html文字大小设置为75px(750px/ 10)，页面元素rem值:页面元素的px值/ 75(750px/75)*/
         width: 10rem;
         margin: 0 auto;
       }
     </style>
     ```

     这样就完成了，然后就可以根据750的设计稿进行在移动端开发了
     同样要是640的设计稿，则要设置html根字体cssroot为64

     

  6. **辅助工具**

     **VSCode px转 rem插件 cssrem**

     **配置：**

     ![image-20201120164612846](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201120164612846.png)

     

     **应用：**

     ![image-20201120164734930](http://121.89.192.46:8888/ganhuo/note/CSS样式属性笔记.assets/image-20201120164734930.png)

     

     **注意点：**

     - 作用：编写代码时自动根据写的px单位计算出等于多少rem
     - 注意：cssrem默认的html字体大小cssroot为16px ，因此要修改为此时的75px；
     - 修改方法: 在vscode设置中查找cssroot，设置为75，设置完成后重新启动vscode就可以了，见上面的 **配置图**

     

  7. **flexsible.js 源代码**

     ```
     (function flexible (window, document) {
       var docEl = document.documentElement
       var dpr = window.devicePixelRatio || 1
     
       // adjust body font size
       function setBodyFontSize () {
         if (document.body) {
           document.body.style.fontSize = (12 * dpr) + 'px'
         }
         else {
           document.addEventListener('DOMContentLoaded', setBodyFontSize)
         }
       }
       setBodyFontSize();
     
       // set 1rem = viewWidth / 10
       function setRemUnit () {
         var rem = docEl.clientWidth / 10
         docEl.style.fontSize = rem + 'px'
       }
     
       setRemUnit()
     
       // reset rem unit on page resize
       window.addEventListener('resize', setRemUnit)
       window.addEventListener('pageshow', function (e) {
         if (e.persisted) {
           setRemUnit()
         }
       })
     
       // detect 0.5px supports
       if (dpr >= 2) {
         var fakeBody = document.createElement('body')
         var testElement = document.createElement('div')
         testElement.style.border = '.5px solid transparent'
         fakeBody.appendChild(testElement)
         docEl.appendChild(fakeBody)
         if (testElement.offsetHeight === 1) {
           docEl.classList.add('hairlines')
         }
         docEl.removeChild(fakeBody)
       }
     }(window, document))
     ```

     

## 拓展知识：max-device-width 和 max-width 的区别

1. max-device-width是设备的宽度，例如，真实的设备屏幕宽度。

2. max-width是目标显示区域的宽度，例如，浏览器宽度。

3. 如果使用max-device-width，那么在PC浏览器上浏览网页时，缩小或放大浏览器时是不执行CSS的，因为“PC设备”没有变化。但如果使用max-width，缩小或放大浏览器时是执行CSS的，因为“显示区域”即浏览器大小发生了变化。

4. 如果使用max-device-width，那么当手机由竖变横时，CSS是不执行的，因为“手机宽度”并没有变化。如果使用max-width，那么当手机由竖变横时，CSS是执行的，因为“显示区域”发生了变化。

5. 通常，面向“ 移动设备”用户使用max-device-width；面向“ PC设备”用户使用 max-width。

   ```
   /*==== 移动设备 ==== */
   @media screen and (max-device-width: 480px){
       /* CSS 代码 */
   }
   
   /*==== PC ==== */
   @media screen and (max-width: 1024px){
       /* CSS 代码 */
   }
   ```

   

