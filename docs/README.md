![](https://img.goojoe.cc/2022/04/16/odbGRlJa.webp)
> 幽竹晨雪，白兔相望

[Pic by Lunami](https://www.pixiv.net/artworks/70791127)

# **HTML5-CSS3文档**

我又回来写文档了参考[黑马CSS教程](https://www.bilibili.com/video/BV14J4114768)

希望大家都能在自己的手中构建出精美的网页♪（＾∀＾●）

这是我做的网站哦,虽然移动端没有适配233...

https://test.goojoe.cc/nav/

因为bilibili嵌入体验并不好,只有480P,所以直接放链接,大家自己去看吧,视频超链接到了标题

- 无聊可以听首歌哦:`For Life(feat. Marmy)(Coelium Remix)-Rival`

<audio controls="" src="https://test.goojoe.cc/nav/music.mp3">
Your browser does not support the
<code>audio</code> element.
</audio>

# [前言](https://www.bilibili.com/video/BV14J4114768)

## 1.关于学习

先听与看>>再动手练习>>分享交流

![image-20220418103924735](https://img.goojoe.cc/2022/04/18/29WE4gP7.webp)

## 2.关于pink老师

尽心尽力设计每一堂课，
全心全意讲解每一个知识点，
虽然以尽全力，
但总无完美，
只要看我视频的人能喜欢，能有收获，
我亦无遗憾…

# HTML5

## [1.查阅文档](https://www.bilibili.com/video/BV14J4114768?p=60)

- [Google](https://Google.com.hk)

- [W3C-school](https://www.w3school.com.cn/)

- [Mozilla MDN](https://developer.mozilla.org/zh-CN/)

    - 搜索标签即可,例如

        ```
        font-size
        ```


# [CSS3](https://www.bilibili.com/video/BV14J4114768?p=61)

## [1.基础结构](https://www.bilibili.com/video/BV14J4114768?p=63)

选择器:{样式}

```css
<style>
h1 {
    color:red;
}
</style>
```

## [2.CSS基础选择器](https://www.bilibili.com/video/BV14J4114768?p=65)

### [2.1标签选择器(div)](https://www.bilibili.com/video/BV14J4114768?p=65)

选择所有标签

```css
h1 {
    color:red;
}
```

### [2.2类选择器(.class)](https://www.bilibili.com/video/BV14J4114768?p=67)

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
    /*给div加上类属性以选择修改样式*/
    <div class='red'>红色</div>
    ```

多类名:
一个标签指定多个类名

```html
<div class-"red font20">亚瑟</div>
```
1. 在标签class属性中写多类名
2. 多个类名中间必须用空格分开
2. 使用场景
    1. 属性复用
    2. 标签相同样式放到一个类里面
    3. 标签调用公共的类,在调用独有的类
    4. 从而节省CSS代码,统一修改也非常方便
    5. 多类名选择器在后期布局复杂的情况使用比较多

### [2.3ID选择器(#ID)](https://www.bilibili.com/video/BV14J4114768?p=70)

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

### [2.4通配符选择器(*)](https://www.bilibili.com/video/BV14J4114768?p=71)

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

## [3.CSS字体属性](https://www.bilibili.com/video/BV14J4114768?p=72)

CSS Fonts（字体）属性用于定义字体系列、大小、粗细、和文字样式（如斜体）。

### [3.1字体家族 | font-family](https://www.bilibili.com/video/BV14J4114768?p=72)

定义字体样式

```CSS
h2 {
	font-family: '宋体';
}
```

- 各种字体之间半角`,`隔开

- 有空格隔开的单词字体,用`""`包裹

- 尽量使用系统字体

- 最常见的几个字体

    - ```CSS
        body {
        	font-family: 'Microsoft YaHei',tahoma,arial,'Horagino Sans GB';
        }
        ```

### [3.1字体大小 | font-size](https://www.bilibili.com/video/BV14J4114768?p=73)

```css
body {
	font-size: 16px;
}
```

- Google Chrome默认16px
- 不同浏览器默认大小不一致,可能导致显示字号不一致,不要默认大小
- 可以使用body指定整个页面大小

### [3.2字体粗细 | font-weight](https://www.bilibili.com/video/BV14J4114768?p=74)

- [MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font-weight)

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

### [3.3文字样式(斜体,下划线) | font-style](https://www.bilibili.com/video/BV14J4114768?p=75)

[MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font-style)

```css
body {
	font-style: italic;
}
```

### [3.4font复合属性写法](https://www.bilibili.com/video/BV14J4114768?p=76)

```css
body {
	font: font-style font-weight fony-size/line-height font-family;
}
```

例子

```css
body {
	font: italic 700 16px "microsoft yahei"
}

```



### [3.5字体属性总结](https://www.bilibili.com/video/BV14J4114768?p=77)

| 属性        | 表示     | 注意点                                                       |
| ----------- | -------- | ------------------------------------------------------------ |
| font-size   | 字号     | 我们通常用的单位是px(pixel)像素，一定要跟上单位              |
| font-family | 字体     | 实际工作中按照团队约定来写字体                               |
| font-weight | 字体粗细 | 记住加粗是700或者bold不加粗是normal或者400记住数字不要跟单位 |
| font-style  | 字体样式 | 记住倾斜是italic,不倾斜是normal工作中我们最常用normal        |
| font        | 字体连写 | 1.字体连写是有顺序的不能随意换位置 2.其中字号和字体必须同时出现 |



## [4.CSS文本属性](https://www.bilibili.com/video/BV14J4114768?p=78)

CSS Text（文本）属性可定义文本的外观，比如文本的颜色、对齐文本、装饰文本、文本缩进、行间距等。

### [4.1文本颜色 | color](https://www.bilibili.com/video/BV14J4114768?p=78)

[MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/color)

- 关键词颜色

```css
color: pink
```

- 16进制颜色 | 设置颜色透明度可转换RGBA

```css
color: #4183c4
```

- RGB(A)

R:red(红)

G:green(绿)

B:blue(蓝)

A:alpha(透明度)



写法

```
/* <rgb()>值 */
color: rgb(34, 12, 64, 0.6);
color: rgba(34, 12, 64, 0.6);
color: rgb(34 12 64 / 0.6);
color: rgba(34 12 64 / 0.3);
color: rgb(34.0 12 64 / 60%);
color: rgba(34.6 12 64 / 30%);
```

---

- HSL(A)

> 根据其色调、饱和度和亮度分量表示给定颜色。一个可选的 alpha 分量表示颜色的透明度。

H:色调

S:饱和度

L:亮度

A:alpha(透明度)



写法

```
hsla(100, 100%, 50%, 1) /* #5f0 */
hsla(235, 100%, 50%, .5) /* #0015ff with 50% opacity */
hsla(235 100% 50% / 1); /* CSS Colors 4 space-separated values */
```




### 4.2对齐文本 | text-align

[MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/text-align)

```css
div {
    /*本质是让h1
    盒子里面的文字水平居中对齐*/
	text-align: center;
}
```

### 4.3装饰文本(删除线,下划线,上划线) | text-decoration

[MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/text-decoration)

```css
div {
	text-decoration: none;
}
```

### 4.4段落文本缩进 | text-indent

```css
p {
	text-indent: 10px;
}
```

em是一个相对单位,就是当前元素(font-size)1个文字的大小来缩进

### 4.5行高 | text-height

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

### 10.1标准流(普通流)

所谓的标准流：就是标签按照规定好默认方式排列，
1.块级元素会独占一行，从上向下顺序排列。

- 常用元素：div、hr、p、h1wh6、ul、ol、dl、form、table

2.行内元素会按照顺序，从左到右序排列，碰到父元素边缘则自动换行。

- 常用元素：span、a、i、em等

以上都是标准流布局，我们前面学习的就是标准流，**标准流是最基本的布局方式**。

这三种布局方式都是用来摆放盒子的，盒子摆放到恰适位置，布局自然就完成了。

**注意**：实际开发中，一个页面基本都包含了这三种布局方式（后面移动端学习新的布局方式） 

### 10.2为什么需要浮动？

提问：我们用标准流能很方便的实现如下效果吗？

总结：有很多的布局效果，标准流没有办法完成，此时就可以利用浮动院成布局。因为浮动可以改变元素标签默认的排列方式

浮动最典型的应用：可以让多个块级元素一行内排列显示。

网页布局第一准则：**多个块级元素纵向排列找标准流，多个块级元素横向排杨列找浮动。**

### 10.3什么是浮动？
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

### 10.4浮动特性（重难点）

设置了浮动(f1oat)的元素最重要特性：

1.脱离标准普通流的控制（浮）移动到指定位置（动），（俗称**脱标**）

2.浮动的盒子**不再保留原先的位置**

### 10.5浮动元素经常和标准流父级搭配使用

为了约束浮动元素位置我们网页布局一般采取的策略是：

先用标准流的父元素排列上下位置，之后内部子元素采取浮动排列左右位置。符合网页布局第一准侧

![](https://img.goojoe.cc/2022/04/15/iFGHsSK4.webp)

### 10.6为什么需要清除浮动？

由于父级盒子很多情况下，不方便给高度，但是子盒子浮动又不占有位置，最后父级盒子高度为0时，就会影响下面的标准流盒子。

![image-20220415222721048](https://img.goojoe.cc/2022/04/15/2bEWgrtK.webp)

- 由于浮动元素不再占用原文档流的位置，所以它会对后面的元素排版产生影响

### 10.7清除浮动本质

- 清除浮动的本质是清除浮动元素造成的影响
- 如果父盒子本身有高度，则不需要清除浮动

### 10.8清除浮动 | clear:both

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

### 10.9清除浮动方法
1. 额外标签法也称为隔墙法，是W3C推荐的
    1. 额外标签法会在浮动元素末尾添加一个空的标签。例如`<div style="clear:both"></div>`,或渚其他标签
    (如`<br/>`等)。
    优点：通俗易懂，书写方便
    缺点：添加许多无意义的标签，结构化较差

2. **父级添加overflow属性**

    可以给父级添加overflow属性，将其属性值设置为hidden、auto或scroll.
    子不教,父之过,注意是给父元素添加代码

    - 优点：代码简洁
    - 缺点：无法显示溢出的部分

3. **父级添加after伪元素**

    ```css
    .clearfix:after {
      content: "";
      display: block;
      height: 0;
      clear: both;
      visibility: hidden;
    }
    .clearfix {
      /*IE6、7专有*/
      *zoom: 1;
    }
    ```

    - 优点：没有增加标签，结构更简弹
    - 缺点：照顾低版本浏览器
    - 代表网站：百度、淘宝网、网易等

4. **父级添加双伪元素**

    也是给父元素添加

    ```css
    .clearfix:before,
    .clearfix:after {
      content: "";
      display: table;
    }
    
    .clearfix:after {
      clear: both;
    }
    
    .clearfix {
      *zoom: 1;
    }
    ```

    - 优点：代码更简洁
    - 缺点：照顾低版本浏览器
    - 代表网站：小米、腾讯等

### 10.10清除浮动总结

为什么需要清除浮动？

1. 父级没高度。
2. 子盒子浮动了。
3. 影响下面布局了，我们就应该清除浮动了。

| 清除浮动的方式       | 优点               | 缺点                               |
| -------------------- | ------------------ | ---------------------------------- |
| 额外标签法（隔墙法） | 通俗易懂，书写方便 | 添加许多无意义的标签，结构化较差。 |
| 父级overflow:hidden; | 书写简单           | 溢出隐藏                           |
| 父级after伪元素      | 结构语义化正确     | 由于IE6-7不支持：after,兼容性问题  |
| 父级双伪元素         | 结构语义化正确     | 由于1E6-7不支持：after,兼容性问题  |

### PS切图

没啥好说的`CTRL+E`合并图层导出即可

## [11.学成在线案例](https://www.bilibili.com/video/BV14J4114768?p=195)

1.典型的企业级网站

2.目的是为了整体感知企业级网站布局流程复习以前知识

### 11.1准备素材和工具

1. 学成在线PSD源文件。
2. 开发工具:
    1. PS（切图）/cutterman插件
    2. vscode（代码）
    3. chrome（测试）

### 11.2案例准备工作

我们本次采取结构与样式相分离思想：

1. 创建study目录文件夹（用于存放我们这个页面的相关内容）。
2. 用vscode打开这个目录文件夹。
3. study目录内新建images文件夹，用于保存图片。
4. 新建首页文件index.html(以后我们的网站首页统规定为index.html).
5. 新建style.css样式文件。我们本次采用外链样式表。
6. 将样式引入到我们的HTML页面文件中。

```css
<link rel="stylesheet" href="style.css">
```

7. 样式表写入清除内外边距的样式，来检测样式表是否引入成功。

```css
* {
	margin: 0;
	padding: 0;
}
```

### 11.3CSS属性书写顺序（重点）

建议遵循以下顺序：

1. 布局定位属性：display/position./float/clear/visibility/overflow(建议display第一个写，毕竟关系到模式)
2. 自身属性：width/height/margin/padding/border/background
3. 文本属性：color/font/text-decoration/text-align/vertical--align/white-space/break-word
4. 其他属性(CSS3):content./cursor/border-radius/box-shadow/text-shadow/background::linear-gradient.…

### 11.4页面布局整体思路

为了提高网页制作的效率，布局时通常有以下的整体思路：

1.必须确定页面的版心（可视区），我们测量可得知

2.分析页面中的行模块，以及每个行模块中的列模块。其实页面布局第一准则

3.一行中的列模块经常浮动布局，先确定每个列的大小之后确定列的位道页面布局第二准则

4.制作HTML结构。我们还是遵循，先有结构，后有样式的原双则。结构永远最重要

5.所以先理清楚**布局结构**，再写代码尤为重要这需要我们多写多积累

### 11.5确定版心

这个页面的版心是1200像素，每个版心都要水平居中对齐，可以定义版心为公共类：

```css
.w {
	width: 1200px;
	margin: auto;
}
```

### 11.6头部制作 | header

![image-20220420114450068](https://img.goojoe.cc/2022/04/20/9w0V22q8.webp)

- 1号是版心盒子header1200*42的盒子水平居中对齐，上下给一个margin值就可以
- 版心盒子里面包含2号盒子logo
- 版心盒子里面包含3号盒子nav导航栏
- 版心盒子里面包含4号盒子search搜索框
- 版心盒子里面包含5号盒子user个人信息
- 注意：要求里面的4个盒子必须都是浮动

导航栏注意点：
**实际开发中，我们不会直接用链接a而是用li包含链接(li+a)的做法。**

1. li+a语义更清晰，一看这就是有条理的列表型内容。
2. 如果直接用a，搜索引擎容易辨别为有堆砌关键字嫌凝（故意堆砌关键字容易被搜索擎有降权的风险），
    从而影响网站排名

注意：

1. 让导航栏一行显示给ⅱ加浮动，因为ⅱ是块级元素需要一行显示
2. 这个nv导航栏可以不给宽度将来可以继续添加其余文字
3. 因为导航栏里面文字不一样多，所以最好给链接a左右padding撑开盒子，而不是指定宽度

search搜索框：
一个search大盒子里面包含2个表单

![image-20220420122911556](https://img.goojoe.cc/2022/04/20/k0YKhYkv.webp)

## 12.Flex布局

### 12.1传统布局与flex布局

传统布局


- 兼容性好

- 布局繁琐

- 局限性，不能再移动端很好的布局。

flex弹性布局

- 操作方便，布局极为简单，移动端应用很广泛

- PC端浏览器支持情况较差
  
- IE11或更低版本，不支特或仅部分支持
  

建议：

1. 如果是PC端页面布局，我们还是传统布局。
2. 如果是移动端或者不考虑兼容性问题的PC端页面布局，我们还是使用flex弹性布局

### 12.2布局原理

flex是flexible Box的缩写，意为"弹性布局”，用来为盒状模型提供最大的灵活性，任何一个容器都可以
指定为flex布局。

- 当我们为父盒子设为flex布局以后，子元素的float、clear和vertical--align属性将失效
- 伸缩布局=弹性布局=伸缩盖布局=弹性盒布局=lx布局

采用FIex布局的元素，称为Flex容器(f1 ex container),简称"容器"。它的所有子元素自动成为容
器成员，称为Flex项目(flex item),简称"项目"。

## 13.Bootstrap简介
Bootstrap来自Twitter（推特），是目前最受欢迎的前端框架。

Bootstrap是基于HTML、CSS和JAVASCRIPT

的，它简洁灵活，使得Web开发更加快捷。

- 官网：http://getbootstrap.com/

- 中文文档(非官方)：http://www.bootcss.com/

**框架：**顾名思义就是一套架构，它有一套比较完整的网页功能解决方案，而目控制权在框架本身，有预制样式库、组件和插件。使用者要按照框架所规定的某种规范进行开发。

# JavaScript

https://www.bilibili.com/video/BV1Sy4y1C7ha

[资料](https://gitee.com/xiaoqiang001/java-script)

## 1.计算机编程基础

目标(TARGET)

- 能够说出什么是编程语言
- 能够区分编程语言和标记语言的不同
- 能够说出常见的数据存储单位及其换算关系
- 能够说出内存的主要作用以及特点

## 1.编程语言

### 1.1编程

**编程：**就是让计算机为解决桌个问题而使用某种程序设语言编写程序代码，并最终得到结果的过程

**计算机程序：**就是计算机所执行的一系列的**指令集合**，而程序全部都是用我们所掌握的语言来编写的，所以
人们要控制计算机一定要通过计算机语言向计算机发出命令。

从事编程的人员，就是**程序员**。但是一般程序员都比较幽默，为了形容自己的辛苦工作，也成为“码农”，
或者“程序猿”/“程序媛”

**注意：**上面所定义的计算机指的是任何能够执行代码的设备，可能是智能手机、ATM机、黑莓PL、服务器
等等。

### 1.2计算机语言

**计算机语言**指用于**人与计算机之间通讯的语言**，它是人与计算机之间传递信总的**媒介**。

计算机语言的种类非常的多，总的来说可以分成**机器语言，汇编语言**和**高级语言**三大类。

实际上计算机最终所执行的都是**机器语言**，它是由“0”和“1”组成的二进制数，二进制是**计算机语**
**言的基础。**

![image-20220424094828690](https://img.goojoe.cc/2022/04/24/4MkniIn7.webp)

### 1.3编程语言

可以通过类似于人类语言的”语言”来控制计算机，让计算机为我们做事情，这样的语言就叫做编程语言（Programming
Language).

编程语言是用来控制计算机的一系列指令，它有固定的格式和词汇（不同编程语言的格式和词汇不一样），必须遵守。

如今通用的编程语言有两种形式：**汇编语言**和**高级语言**。

- 汇编语言和机器语言实质是相同的，都是直接对硬件操作，只不过指令采用了英文缩写的标识符，容易识别和记忆。
- 高级语言主要是相对于低级语言而言，它并不是特指某一种具体的语言，而是包括了很多编程语言，常用的有C语言、C++
    、Java、C#、Python、PHP、JavaScript、Go语言、Objective-C、Swift等，

![image-20220424094947232](https://img.goojoe.cc/2022/04/24/WYGQqdub.webp)

### 1.4翻译器

高级语言所编制的程序不能直接被计算机识别，必须经过转换才能被执行，为此，我们需要一个翻译器。

翻译器可以将我们所编写的源代码转换为机器语言，这也被称为二进制化。记住1和0。

![image-20220424100143709](https://img.goojoe.cc/2022/04/24/ke7YoXG9.webp)

### 1.5编程语言和标记语言区别

- 编程语言有很强的逻辑和行为能力。在编程语言里你会看到很多if else、for、while等具有逻辑性和行为能力的
    指令，这是主动的。
- 标记语言(HTML)不用于向计算机发出指令，常用于格式化和链接。标记语言的存在是用来被读取的，他是被动的。

### 总结

1. 计算机可以帮助人类解决某些问题
2. 程序员利用编程语言编写程序发出指令控制计算机来实现这些任务
3. 编程语言有机器语言、汇编语言、高级语言

## 2.计算机基础

### 2.1计算机组成

  ![image-20220424100902406](https://img.goojoe.cc/2022/04/24/WNR05pF8.webp)

![image-20220424100913817](https://img.goojoe.cc/2022/04/24/0UxsZxuK.webp)

## 2.2数据存储
1. 计算机内部使用二进制0和1来表示数据
2. 所有数据，包括文件、图片等最终都是以二进制数据(0和1)的形式存放在硬盘中的。
3. 所有程序，包括操作系统，本质都是各种数据，也以二进制数据的形式存放在硬盘中。平时我们所说的安
    装软件，其实就是把程序文件复制到硬盘中。
4. 硬盘、内存都是保存的二进制数据

### 2.3数据存储单位

bit<byte<kb<GB<TB<.....

- 位(bit):1bit可以保存一个0或者1（最小的存储单位）
    G
- 字节(Byte):1B=8b
- 千字节(KB):1KB=1024B
- 兆字节(MB):1MB=1024KB
- 吉字节(GB):1GB=1024MB
- 太字节(TB):1TB=1024GB
- ......

### 2.4程序运行

![image-20220424101509096](https://img.goojoe.cc/2022/04/24/5taAayLe.webp)

1. 打开某个程序时，先从硬盘中把程序的代码加载到内存中
2. CPU执行内存中的代码

**注意：**之所以要内存的一个重要原因，是因为Cpu运行太快了，如果只从硬盘中读数据，会浪费cpu性能，所
 以，才使用存取速度更快的内存来保存运行时的数据。(内存是电，硬盘是机械)

## 2.初识JavaScript

### 2.1JavaScript历史

- 布兰登艾奇(Brendan Eich,1961年~).
- 神奇的大哥在1995年利用10天完成JavaScript设计。
- 网景公司最初命名为LiveScript,后来在与Sun合作之后将其改名为avaScript

### 2.2JavaScript是什么

- JavaScript是世界上最流行的语言之一，是一种运行在客户端的脚本语言(Script是脚本的意思)
- 脚本语言：不需要编译，运行过程中由js解释器(s引擎)逐行来进行解释并执行
- 现在也可以基于Node.js技术进行服务器端编程

![image-20220424102019452](https://img.goojoe.cc/2022/04/24/WKZnAWKp.webp)

## 1.3 JavaScript的作用

- 表单动态校验（密码强度检测）(JS产生最初的目的)

- 网页特效
- 服务端开发(Node.js)
- 桌面程序(Electron)
- App(Cordova)
    R
- 控制硬件-物联网（Ruff)
- 游戏开发(cocos2d-js)

### 1.4HTML/CSS/JS的关系

HTML/CSS标记语言-描述类语言

- HTML决定网页结构和内容（决定看到什么），相当
    于人的身体
- CSS决定网页呈现给用户的模样（决定好不好看），
    相当于给人穿衣服、化妆

JS脚本语言-编程类语言

- 实现业务逻辑和页面控制（决定功能），相当
    于人的各种动作
