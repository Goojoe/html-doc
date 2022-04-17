# **html的文档**

我又回来写文档了参考[黑马CSS教程](https://www.bilibili.com/video/BV14J4114768)

# HTML5

## 1.查阅文档

- [Google](https://Google.com.hk)

- [W3C-school](https://www.w3school.com.cn/)
- [Mozilla MDN](https://developer.mozilla.org/zh-CN/)

# CSS3

## 1.基础结构

选择器:{样式}

```css
h1 {colror:red;}
```

## 2.CSS基础选择器

### 2.1标签选择器(div)

选择所有标签

### 2.2类选择器(.class)

- 单独选择一个,或者某几个标签

- ```css
    .类名 {
    	属性值1:属性值
    }
    .green {
                /* 盒子 */
                width: 100px;
                height: 100px;
                /* 背景颜色 */
                background-color: green;
            }
    <div class='red'>红色</div>
    ```

多类名:

    一个标签指定多个类名
    
    ```css
    <div class-"red font20">亚瑟</div>
    ```
    
    1. 在标签class属性中写多类名
    2. 多个类名中间必须用空格分开
    3. 使用场景
        1. 属性复用
        2. 标签相同样式放到一个类里面
        3. 标签调用公共的类,在调用独有的类
        4. 从而节省CSS代码,统一修改也非常方便
        5. 多类名选择器在后期布局复杂的情况使用比较多

### 2.3ID选择器(#ID)

- ID选择器可以为标有特定ID的HTML元素指定特定的样式

- ```CSS
    #ID名 {
    	属性1:属性值;
    }
    #nav {
        color:red;
    }
    ```

- ID选择器的口诀:样式#定义,结构id调用,只能调用一次,别人切勿使用

#### 2.3.1类选择器和ID选择器的区别

1. 类选择器(class)好比人名,一个人可以有多个名字,一个名字多个人使用
2. ID选择器(#ID):好比身份证号码,唯一的
3. ID选择器和类选择器最大的区别在于使用次数
4. 类选择器修改样式使用最多,ID选择器一般用于界面唯一性元素上,经常和JS搭配使用

### 2.4通配符选择器(*)

选取所有的元素

```CSS
* {
   属性1:属性值
}
```

 特殊情况使用

```css
/*清除元素标签的内外边距*/
* {
	margin: 0;
	padding: 0;
}
```

## 3.CSS字体属性

定义字体样式

```CSS
h2 {
	font-family: '宋体';
}
```

- 各种字体之间半角,隔开

- 有空格隔开的单词字体,用""隔开

- 尽量使用系统字体

- 最常见的几个字体

    - ```CSS
        body {
        	font-family: 'Microsoft YaHei',tahoma,arial,'Horagino Sans GB';
        }
        ```

### 3.1字体大小 | font-size

```css
body {
	font-size: 20px;
}
```

- Google Chrome默认16px
- 不同浏览器默认大小不一致,可能导致显示字号不一致,不要默认大小
- body指定整个页面大小

### 3.2字体粗细 | font-weight

[MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font-weight)

```css
body {
	font-weight: 500;
}
```

| 属性值      | 描述                                 |
| ----------- | ------------------------------------ |
| normal(400) | 默认值                               |
| bold(700)   | 加粗                                 |
| 100-900     | 400=normal,700=bold,数字后面没有单位 |

### 3.3文字样式(斜体,下划线) | font-style

[MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font-style)

```css
body {
	font-style: italic;
}
```

### 3.4字体连写-复合属性

```css
body {
	font: font-style font-weight fony-size/line-height font-family;
}
```

## 4.CSS文本属性

### 4.1文本颜色

[MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/color)

```css
/* 关键词 */
color: currentcolor;

/* <named-color>值 */
color: red;
color: orange;
color: tan;
color: rebeccapurple;

/* <hex-color>值 */
color: #090;
color: #009900;
color: #090a;
color: #009900aa;

/* <rgb()>值 */
color: rgb(34, 12, 64, 0.6);
color: rgba(34, 12, 64, 0.6);
color: rgb(34 12 64 / 0.6);
color: rgba(34 12 64 / 0.3);
color: rgb(34.0 12 64 / 60%);
color: rgba(34.6 12 64 / 30%);

/* <hsl()>值 */
color: hsl(30, 100%, 50%, 0.6);
color: hsla(30, 100%, 50%, 0.6);
color: hsl(30 100% 50% / 0.6);
color: hsla(30 100% 50% / 0.6);
color: hsl(30.0 100% 50% / 60%);
color: hsla(30.2 100% 50% / 60%);

/* 全局值 */
color: inherit;
color: initial;
color: unset;
```

### 4.2对齐文本

[MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/text-align)

```css
div {
    /*本质是让h1
    盒子里面的文字水平居中对齐*/
	text-align: center;
}
```

### 4.3装饰文本(删除线,下划线,上划线)

[MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/text-decoration)

```css
div {
	text-decoration: none;
}
```

### 4.4段落文本缩进

```css
p {
	text-indent: 10px;
}
```

em是一个相对单位,就是当前元素(font-size)1个文字的大小来缩进

### 4.5行高

```css
p {
	text-height: 26px;
}
```

文字上下的间距距离

![image-20220412122029319](https://img.goojoe.cc/2022/04/12/lL5znpgG.webp)

 ## 5.CSS引入

### 5.1外部引入

```
<link rel="stylesheet" href="路径">
```

## 6.Emmet语法

### 6.1HTML

1. 生成标签:div>TAB
2. 多个相同标签div*3
3. 父级标签ul>li
4. 兄弟标签div+p 同级标签
5. 类名 .demo #two p.one
6. 顺序 $ .demo$*5
7. 标签默认显示字: div{123}

### 6.2CSS

w100

h100

ti2em

## 7.CSS复合选择器

### 7.1后代选择器 | ol li a

后代选择器可以选择父元素里的子元素,外层标签在前面,内层标签在里面,中间空格分割

```css
ol li a {
	color: red;
}
```



### 7.2子选择器 | .nav>a

选择最近一级的子元素

```css
 .nav>a {
            color: pink;
        }	
```

 ### 7.3并集选择器 | div,p

可以选择多组标签,同时为他们定义相同的样式

```css
div,
p {
	color: pink;
}
```

### 7.4伪类选择器(a:鼠标激活)

#### 7.4.1链接伪类

| a:link    | 选择所有未被访问的链接     |
| --------- | -------------------------- |
| a:visited | 选择所有已经被访问的链接   |
| a:hover   | 选择鼠标指针位于其上的链接 |
| a:active  | 选择活动链接(拖动)         |

LVHA声明 LOVE HATE

#### 7.4.2Focus伪类选择器

Focus伪类选择器用于选择获得焦点的表单元素

焦点就是鼠标

```css
 input:focus {
            background-color: pink;
            color: red;
        }
```

 ## 8.CSS元素显示模式

块元素



<h1>~<h6>



## 9.CSS盒子模型

### 9.1盒子模型

页面布局要学习三大核心:盒子模型,浮动,定位,学习好盒子模型可以非常好的帮助我们布局页面

### 9.2网页布局过程：
1.先准备好相关的网页元素，网页元素基本都是盒子box.
2.利用CSS设置好盒子样式，然后摆放到相应位置。

### 9.3盒子模型(Box Model)组成

所谓盒子模型：就是把HTML页面中的布局元素看作是一个矩形的盒子，也就是一个盛装内容的容器。
CSS盒子模型本质上是一个盒子，封装周围的HTML元素，它包括：边框、外边距、内边距、和实际内容

![image-20220413175745394](https://img.goojoe.cc/2022/04/13/va7pm87k.webp)

![image-20220413175930172](https://img.goojoe.cc/2022/04/13/SbIKUegn.webp)

### 9.4边框(border)

borderi可以设置元素的边框。边框有三部分组成：边框宽度（粗细）边框样式边框颜色

语法：

| border       |                     |
| ------------ | ------------------- |
| border-width | 定义边框粗细,单位px |
| border-style | 边框的样式          |
| border-color | 边框颜色            |

CSS边框属性允许你指定一个元素边框的样式和颜色，
边框简写：

```css
border:1px solid red; /*没有顺序*/
```

#### 表格的细线边框

**border-collapse**属性控制浏览器绘制表格边框的方式。它控制相邻单元格的边框。
语法：

```css
border-collapse:collapse;
```

- collapse单词是合并的意思
- border-collapse:collapse;表示相邻边框合并在一起

#### 边框会影响盒子实际大小

边框会额外增加盒子的实际大小。因此我们有两种方案解决：

1. 测量盒子大小的时候，不量边框
2. 如果测量的时候包含了边框，则需要width/height减去边框宽度

### 9.5内边距(padding)
padding属性用于设置内边距，即边框与内容之间的距离。

padding属性（简写属性）可以有一到四个值:

上>>右>>下>>左 顺时针

> 当我们给盒子指定padding值之后，发生了2件事情：
> 1.内容和边框有了距离，添加了内边距。
> 2.padding影响了盒子实际大小。

### 9.6外边距(margin)

margin属性用于设置外边距，即控制盒子和盒子之间的距离。

#### 清除内外边距

网页元素很多都带有默认的内外边距，而且不同浏览器默认的也不致。因此我们在布局前，首先要清除下网
页元素的内外边距。

```css
* {
padding:0;/*清除内边距*/
margin:0;/*清除外边距*/
}
```



### 9.7PS基本操作



### 9.8列表去掉圆点 | list-style

```css
li{
list-style:none;
}

```



### 9.9CSS圆角边框 | border-radius

在CSS3中，新增了圆角边框样式，这样我们的盒子就可以变圆角了。
border-radius属性用于设置元素的外边框圆角。
语法：

```css
border-radius: 10px;
```

### 9.10盒子阴影 | box-shadow

CSS3中新增了盒子阴影，我们可以使用box-shadow属性为盒子添加阴影
语法：

```css
box-shadow:h-shadow v-shadow blur spread color inset;
```

| 值       | 描述                                   |
| -------- | -------------------------------------- |
| h-shadow | 必需。水平阴影的位置。允许负值。       |
| v-shadow | 必需。垂直阴影的位置。允许负值，       |
| blur     | 可选。模糊距离。                       |
| spread   | 可选。阴影的尺寸。                     |
| color    | 可选。阴影的颜色。请参阅CSS颜色值。    |
| inset    | 可选。将外部阴影(outset)改为内部阴影。 |

## 10.CSS浮动(float布局)

1.1传统网页布局的三种方式
网页布局的本质一用CSS来摆放盒子。把盒子摆放到相应位置
CSS提供了三种传统布局方式简单说就是盒子如何进行排列序：

- 普通流(标准流)
- 浮动
- 定位

#### 10.1标准流(普通流)

所谓的标准流：就是标签按照规定好默认方式排列，
1.块级元素会独占一行，从上向下顺序排列。

- 常用元素：div、hr、p、h1wh6、ul、ol、dl、form、table

2.行内元素会按照顺序，从左到右序排列，碰到父元素边缘则自动换行。

- 常用元素：span、a、i、em等

以上都是标准流布局，我们前面学习的就是标准流，**标准流是最基本的布局方式**。

这三种布局方式都是用来摆放盒子的，盒子摆放到恰适位置，布局自然就完成了。

**注意**：实际开发中，一个页面基本都包含了这三种布局方式（后面移动端学习新的布局方式） 

#### 10.2为什么需要浮动？

提问：我们用标准流能很方便的实现如下效果吗？

总结：有很多的布局效果，标准流没有办法完成，此时就可以利用浮动院成布局。因为浮动可以改变元素标签默认的排列方式

浮动最典型的应用：可以让多个块级元素一行内排列显示。

网页布局第一准则：**多个块级元素纵向排列找标准流，多个块级元素横向排杨列找浮动。**

#### 10.3什么是浮动？
**float**属性用于创建浮动框，将其移动到一边，直到佐边缘或右边缘触及包含块或另一个浮动框的边缘。

语法

```
选择器 {
float:属性值
}
```

| 属性值 | 描述               |
| ------ | ------------------ |
| none   | 元素不浮动(默认值) |
| left   | 左浮动             |
| right  | 右浮动             |

#### 10.4浮动特性（重难点）

设置了浮动(f1oat)的元素最重要特性：

1.脱离标准普通流的控制（浮）移动到指定位置（动），（俗称**脱标**）

2.浮动的盒子**不再保留原先的位置**

#### 10.5浮动元素经常和标准流父级搭配使用

为了约束浮动元素位置我们网页布局一般采取的策略是：

先用标准流的父元素排列上下位置，之后内部子元素采取浮动排列左右位置。符合网页布局第一准侧

![](https://img.goojoe.cc/2022/04/15/iFGHsSK4.webp)

#### 10.6为什么需要清除浮动？

由于父级盒子很多情况下，不方便给高度，但是子盒子浮动又不占有位置，最后父级盒子高度为0时，就会影响下面的标准流盒子。

![image-20220415222721048](https://img.goojoe.cc/2022/04/15/2bEWgrtK.webp)

- 由于浮动元素不再占用原文档流的位置，所以它会对后面的元素排版产生影响

#### 10.7清除浮动本质

- 清除浮动的本质是清除浮动元素造成的影响
- 如果父盒子本身有高度，则不需要清除浮动

#### 10.8清除浮动 | clear:both

```css
选择器{clear:属性值；}
```



| 属性值 | 描述                                       |
| ------ | ------------------------------------------ |
| left   | 不允许左侧有浮动元素（清除左侧浮动的影响） |
| right  | 不允许右侧有浮动元素（清除右侧浮动的影响） |
| both   | 同时清除左右两侧浮动的影响                 |


我们实际工作中，几乎只用clear:both;

清除浮动的策略是：闭合浮动

#### 10.9清除浮动方法
1. 额外标签法也称为隔墙法，是W3C推荐的
    1. 额外标签法会在浮动元素末尾添加一个空的标签。例如`<div style="clear:both"></div>`,或渚其他标签
    (如`<br/>`等)。
    优点：通俗易懂，书写方便
    缺点：添加许多无意义的标签，结构化较差

2. **父级添加overflow属性**
3. **父级添加after伪元素**
4. **父级添加双伪元素**

## 11.Flex布局

### 11.1传统布局与flex布局

传统布局


- 兼容性好

- 布局繁琐

- 局限性，不能再移动端很好的布局。

flex弹性布局

- 操作方便，布局极为简单，移动端应用很广泛

- PC端浏览器支持情况较差
  
- E11或更低版本，不支特或仅部分支持
  

建议：

1. 如果是PC端页面布局，我们还是传统布局。
2. 如果是移动端或者不考虑兼容性问题的PC端页面布局，我们还是使用flex弹性布局

### 11.2布局原理

flex是flexible Box的缩写，意为"弹性布局”，用来为盒状模型提供最大的灵活性，任何一个容器都可以
指定为flex布局。

- 当我们为父盒子设为flex布局以后，子元素的float、clear和vertical--align属性将失效
- 伸缩布局=弹性布局=伸缩盖布局=弹性盒布局=lx布局

采用FIex布局的元素，称为Flex容器(f1 ex container),简称"容器"。它的所有子元素自动成为容
器成员，称为Flex项目(flex item),简称"项目"。

## 12.Bootstrap简介
Bootstrap来自Twitter（推特），是目前最受欢p的前端框架。Bootstrap是基于HTML、CSS和JAVASCRIPT
的，它简洁灵活，使得Web开发更加快捷。
●中文官网：http://www.bootcss..com/
●官网：http://getbootstrap.com/
●推荐使用：http://bootstrap.css88.com/
**框架：**顾名思义就是一套架构，它有一套比较完整的网页功能解决方案，而目控制权在框架本身，有预制样式库、组
件和插件。使用者要按照框架所规定的某种规范进行开发。
