
[toc]
# 自己写的基础

标签（空格分隔）： HTML

---

这里写你认为是基础的东西


# 1. HTML
- 首先HTML是一种标记语言，由元素组成，用于构建你想要的浏览器页面
- HTML是由元素组成，而元素是由开始标签，内容，结束标签组成

## 1.1 元素有分类：
1.嵌套元素（元素与元素之间存在包含关系）
2.内联元素（通常出现在块级元素之中，并包含文档的一小部分）
3.块元素（页面中以块的形式存在，相对与前面的内容，它会出现在新的一行）
4.空元素（只有一个标签，通常用在此元素在位置插入一些东西）

## 1.2属性：
属性是包含元素的的额外信息，通常不会出现在实际内容中。

- 元素包含的内容有三点：
1：在元素和属性之间有一个空格space
2：属性后面紧跟着一个’=‘
3：有一个属性值用” “引起来

- 布尔属性：
没有值的属性，但是合法

HTML框架

    &lt;!DOCTYPE html>声明文档类型
    &lt;html>包含整个页面，是根元素
     &lt;head>包含了所有你想在HTML页面中而不想在HTML页面中显示的内容
      &lt;meta charset="UTF-8">这个元素设置文档使用utf-8编码
      &lt;title>My first page&lt;/title>页面标题
     &lt;/head>
     &lt;body>页面的所有内容
      &lt;p>This page&lt;/p>
     &lt;/body>
    &lt;/html>
特殊字符的转义

原义字符	等价字符引用
大于号           &gt冒号
小于号           &lt冒号
and符号          &amp冒号
双引号           &quot冒号
单引号           &apos冒号


HTML 注释 
&lt;!--&lt;p>content&lt;/p>-->

##&lt;head&gt;

###元数据&lt;meta元素>
指定字符编码 &lt;meta charset = 'utf-8'&gt;
有name和content两个特性&lt;meta name=‘’ content=‘’&gt;
name：指定meta元素的类型，说明该元素包含了什么类型的信息

 1. name = ”author“ 作者
 2. name = ”description“ 搜索引擎中的关于网站的关键字描述

content：指定了实际的元数据信息

###页面添加图标的方式
在&lt;head&gt;中添加&lt;link rel="" size="" href="">

###为文档设置主语言
&lt;html lang="en-US"&gt;

标签	描述
&lt;base&gt;	定义了页面链接标签的默认链接地址
&lt;link&gt;定义了一个文档和外部资源之间的关系
&lt;script&gt;	定义了客户端的脚本文件
&lt;style&gt;定义了HTML文档的样式文件

##网页内容
&lt;p&gt; 此标签用来对段落进行定义
&lt;h#&gt;此标签用来对标题进行定义，#从小到大表示主次关系

##列表lists
每一份无序清单都从&lt;ul&gt;包裹
用&lt;li&gt;将每个列出的项目分别包裹起来

有序列表则是用&lt;ol&gt;包裹
用&lt;li&gt;将每个列出的项目分别包裹起来

并且列表是可以镶嵌在一起的

描述列表用&lt;dl&gt;包裹
每一项都用&lt;dt&gt;闭合，描述用&lt;dd&gt;闭合
浏览器默认dd和dt之间有缩进

###自定义列表使用&lt;dl>包裹
。每个自定义列表项以 &lt;dt> 开始。每个自定义列表项的定义以 &lt;dd> 开始。

##内容强调用
&lt;em&gt;斜体
&lt;strong&gt;加粗

##超链接
能从我们的文档链接到其他文档或者链接到文档的制定部分

###通过将文本转换成&lt;a>元素内的链接来创建基本链接，给它一个href属性，它将包含你希望链接指向的网址,title属性用来当鼠标悬浮在链接上时，作为提示信息出现，target属性设置为_blank的话，链接会在新的标签页打开.
&lt;a href="https://www.mozilla.org/en-US/" title = ”information“ &gt;the Mozilla homepage &lt;/a&gt;
如果你想让一个图像作为链接的话，你可以将图像放在a标签中间
    
URL统一资源定位器（定义在网络上的位置的一个文本字符串）
要确定URL的话，应该是/path/to/my.html

#文档片段

如果超链接想要链接在文档的那些部分的话，必须在元素内设置id属性
，然后在URL后面用#连接其内容
并且也可以用它自己的文档片段参考链接到同一份文件的不同部分

##电子邮件链接
&lt;a href="mailto:nowhere@mozilla.org"&gt;Send email to nowhere&lt;/a&gt;


#引用
##块引用
###如果一个块级内容被其他地方引用，首先用&lt;blockquote&gt;包裹，在cite属性中使用URL来表示引用的资源
###行内引用则是用&lt;q&gt;包裹
&lt;cite&gt;元素放到引用元素旁边。这就意味着包含引用资源的名称——即引用的书的名字，或人的名字

#缩略语
用&lt;abbr&gt;包裹一个缩略语或者缩写，用title属性来表示意思

&lt;address&gt;包裹一个联系方式

#上标和下标
&lt;sup&gt;上标
&lt;sub&gt;下标
又来表示一些方程式或者数学式
#格式化字符
&lt;b&gt;粗体
&lt;i&gt;斜体
&lt;em&gt;着重字体
&lt;small&gt;小字
&lt;del&gt;删除字
&lt;ins&gt;插入字
#表示计算机代码
&lt;code&gt;: 用于标记计算机通用代码。
&lt;pre&gt;: 对保留的空格（通常是代码块）——如果您在文本中使用缩进或多余的空白，浏览器将忽略它，您将不会在呈现的页面上看到它。但是，如果您将文本包含在&lt;pre&gt;标签中，那么空白将会以与你在文本编辑器中看到的相同的方式渲染出来。
&lt;var&gt;: 用于标记具体变量名。
&lt;kbd&gt;: 用于标记输入电脑的键盘（或其他类型）输入。
&lt;samp&gt;: 用于标记计算机程序的输出

#标记时间
&lt;time datetime = "2018-07-12"&gt;12 July 2018&lt;/time&gt;

##换行元素
 &lt;br&gt;换行
 &lt;hr&gt;插入水平分割线
 
 #图像
 &lt;img src = ”图像的具体地址“&gt; 自闭元素不需要结束标签
 

#网站结构
&lt;main&gt;展现了页面内容的独特性。只可以在每一个页面上使用一次&lt;main&gt;，直接把它放到&lt;body&gt;中。在理想情况下，不应该把它嵌套进其他的元素中。
&lt;section&gt; 闭合一块与自身相关的内容，这块内容能够解释它自身而不是页面上其他的内容（例如一篇单独的博客）。
&lt;section&gt;近似于&lt;acticle&gt;，但是它更多的是伴随着由一个单独功能构成的页面（例如一个小型的地图，或者是一组文章的标题和摘要）。它被认为最好的实际应用是用标题作为每一部分（section）的开头；也要注意的是你可以把不同的&lt;acticle&gt;分到不同的&lt;section&gt;中，或者把不同的&lt;section&gt;分到不同的&lt;acticle&gt;中，这要取决于内容。
&lt;aside&gt; 包含的内容并不与主要内容有直接的联系，但是它可以提供额外的不直接有联系的信息（术语表条目，作者简介，相关链接等等）。
&lt;header&gt;展现了一系列的介绍性内容。如果它是&lt;body&gt; 的子元素,它就定义了网站的全局页眉。但是如果它是&lt;acticle&gt; 或&lt;section&gt; 的子元素，它就定义了这些部分的特定的页眉(不要把这些与titles and headings混淆)。
&lt;&lt;nav&gt;包含了页面主要的导航功能。二级链接等，不会进入导航功能部分。
 &lt;footer&gt;包含了页面的页脚部分。


#HTML中的图片
&lt;img&gt;标签中有以下属性
src（用来表示图片的统一资源定位符）
alt（表示如果图片路径出错将会表示的内容）
title（在图片上加入描述）
width（宽度）
height（高度）
##figure（容器）和figcaption（描述）标签可以用来给图像视频等等添加大得体的语义描述

#HTML视频和音频内容
首先video标签来插入一段视频
&lt;video src="rabbit320.webm" controls>
  &lt;p>Your browser doesn't support HTML5 video. Here is a &lt;a href="rabbit320.webm"&gt;link to the video&lt;/a&gt; instead.&lt;/p&gt;
&lt;/video&gt;

 1. src属性用来指定你视频的位置
 2. controls使用浏览器的回放功能，给用户提供视频回放功能
 3. 标签内的内容会在视频无法播放时出现

##浏览器格式支持
容器格式分别有MP3,MP4（主要再IE和safari），Webm(主要在火狐和谷歌中支持)
面临格式兼容问题我们可以使用source标签，ex：
&lt;video controls>
  &lt;source src="rabbit320.mp4" type="video/mp4">
  &lt;source src="rabbit320.webm" type="video/webm">
  &lt;p>Your browser doesn't support HTML5 video. Here is a &lt;a href="rabbit320.mp4">link to the video&lt;/a> instead.&lt;/p>
&lt;/video>
上面例子中浏览器将会检查&lt;source>标签，并且会播放第一个格式相兼容的，type属性是可选的，浏览器会首先检查格式，不浪费时间
##video属性
width 和 height
你可以用属性控制视频的尺寸
autoplay
这个属性会使音频和视频内容立即播放
loop
这个属性可以让音频或者视频文件循环播放
muted
这个属性会导致媒体播放时，默认关闭声音。
poster
这个属性指向了一个图像的URL，这个图像会在视频播放前显示。通常用于粗略的预览或者广告。
preload
这个属性被用来缓冲较大的文件，有3个值可选：
"none" ：不缓冲
"auto" ：页面加载后缓存媒体文件
"metadata" ：仅缓冲文件的元数据


#插入音频使用audio 标签
格式与视频相似
&lt;audio controls>
  &lt;source src="viper.mp3" type="audio/mp3">
  &lt;source src="viper.ogg" type="audio/ogg">
  &lt;p>Your browser doesn't support HTML5 audio. Here is a &lt;a href="viper.mp3">link to the audio&lt;/a> instead.&lt;/p>
&lt;/audio>

如果要给视频加字幕，同声翻译，将文字转为音频
则需要使用webvtt格式编写文本文件，以vtt后缀进行保存
subtitle
通过添加翻译字幕，来帮助那些听不懂外国语言的人们理解音频当中的内容。
captions
同步翻译对白，来帮助那些不能听音频的人们理解音频中的内容。
timed descriptions
将文字转换为音频
最后则通过&lt;track>标签链接vtt文件， &lttrack> 标签需放在 &lt;audio> 或 &lt;video> 标签当中，同时需要放在所有 &lt;source> 标签之后。使用 kind 属性来指明是哪一种类型，如 subtitles 、 captions 、 descriptions。然后，使用 srclang 来告诉浏览器你是用什么语言来编写的 subtitles。

例如：&lt;video controls>
    &lt;source> src="example.mp4" type="video/mp4">
    &lt;source> src="example.webm" type="video/webm">
    &lt;track kind="subtitles" src="subtitles_en.vtt" srclang="en">
    
#HTML表格
##表格用&lt;table>来包裹，
&lt;th&gt;用来定义表头
&lt;tr>用来定义表格的行
&lt;td>用来定义表格的列
&lt;caption>	定义表格标题
&lt;colgroup>	定义表格列的组
&lt;col>	定义用于表格列的属性
&lt;thead>	定义表格的页眉
&lt;tbody>	定义表格的主体
&lt;tfoot>	定义表格的页脚

#HTML区块
&lt;div&gt;标签定义了文档的区域
&lt;span>标签用来组合文档中的行内元素

#HTML表单
表单是一个包含表单元素的区域
表单元素允许用户输入内容
表单元素是用&lt;form>标签包裹
##文本域通过&lt;input type="text">标签来设定
&lt;form>
First name: &lt;input type="text" name="firstname">&lt;br>
Last name: &lt;input type="text" name="lastname">
&lt;/form> 

##密码字段通过标签&lt;input type="password"> 来定义:

##单选按钮&lt;input type="radio" name="按钮描述">
##复选框&lt;input type="checkboxes">
##提交按钮&lt;input type="submit" value="按钮描述">

#HTML框架
&lt;iframe>标签规定了一个内联框架
一个内联框架被用于在HTML文档中嵌入另外一个文档
&lt;iframe> src=”“&lt;/iframe>
高度和宽度属性都可以设置（width和height）
frameborder="0"用来移除边框

#HTML颜色
#000000	rgb(0,0,0)
    #000000(黑)
 	#FF0000（红)
 	#00FF00（绿）
 	#0000FF（蓝）
 	#FFFF00（黄）
 	#00FFFF（靛）
 	#FF00FF（紫）
 	#C0C0C0	（灰）
 	#FFFFFF	（白）

#HTML脚本
&lt;script>定义了客户端脚本
&lt;noscript>	定义了不支持脚本浏览器输出的文本


#速查列表

HTML 基本文档

&lt;!DOCTYPE html>
&lt;html>
&lt;head>
&lt;title>文档标题&lt;/title>
&lt;/head>
&lt;body> 可见文本... &lt;/body>
&lt;/html>
基本标签（Basic Tags）

&lt;h1>最大的标题&lt;/h1>
 &lt;h2> . . . &lt;/h2>
 &lt;h3> . . . &lt;/h3>
 &lt;h4> . . . &lt;/h4>
 &lt;h5> . . . &lt;/h5>
 &lt;h6>最小的标题&lt;/h6>
 
 &lt;p>这是一个段落。&lt;/p>
 &lt;br> （换行）
 &lt;hr> （水平线）
 &lt;!-- 这是注释 -->
文本格式化（Formatting）

&lt;b>粗体文本&lt;/b>
 &lt;code>计算机代码&lt;/code>
 &lt;em>强调文本&lt;/em>
 &lt;i>斜体文本&lt;/i>
 &lt;kbd>键盘输入&lt;/kbd> 
 &lt;pre>预格式化文本&lt;/pre>
 &lt;small>更小的文本&lt;/small>
 &lt;strong>重要的文本&lt;/strong>
 
 &lt;abbr> （缩写）
 &lt;address> （联系信息）
 &lt;bdo> （文字方向）
 &lt;blockquote> （从另一个源引用的部分）
 &lt;cite> （工作的名称）
 &lt;del> （删除的文本）
 &lt;ins> （插入的文本）
 &lt;sub> （下标文本）
 &lt;sup> （上标文本）
链接（Links）

普通的链接：&lt;a href="链接地址">链接文本&lt;/a>
图像链接： &lt;a href="http://www.example.com/">&lt;img src="URL" alt="替换文本">&lt;/a> 
邮件链接： &lt;a href="mailto:webmaster@example.com">发送e-mail&lt;/a>
书签： &lt;a id="tips">
提示部分&lt;/a> &lt;a href="#tips">跳到提示部分&lt;/a>
图片（Images）

&lt;img src="URL" alt="替换文本" height="42" width="42">
样式/区块（Styles/Sections）

&lt;style type="text/css">
   h1 {color:red;}
   p {color:blue;}
 &lt;/style>
 
 
 &lt;div>文档中的块级元素&lt;/div>
 &lt;span>文档中的内联元素&lt;/span>
无序列表

&lt;ul>
   &lt;li>项目&lt;/li>
   &lt;li>项目&lt;/li>
 &lt;/ul>
有序列表

&lt;ol>
   &lt;li>第一项&lt;/li>
   &lt;li>第二项&lt;/li>
 &lt;/ol>
定义列表

&lt;dl>
   &lt;dt>项目 1&lt;/dt>
     &lt;dd>描述项目 1&lt;/dd>
   &lt;dt>项目 2&lt;/dt>
     &lt;dd>描述项目 2&lt;/dd>
 &lt;/dl>
表格（Tables）

&lt;table border="1">
   &lt;tr>
     &lt;th>表格标题&lt;/th>
     &lt;th>表格标题&lt;/th>
   &lt;/tr>
   &lt;tr>
     &lt;td>表格数据&lt;/td>
     &lt;td>表格数据&lt;/td>
   &lt;/tr>
 &lt;/table>
框架（Iframe）

&lt;iframe src="demo_iframe.htm">&lt;/iframe>
表单（Forms）

&lt;form action="demo_form.php" method="post/get">

&lt;input type="text" name="email" size="40" maxlength="50"> 
&lt;input type="password"> 
&lt;input type="checkbox" checked="checked"> 
&lt;input type="radio" checked="checked"> 
&lt;input type="submit" value="Send"> 
&lt;input type="reset"> 
&lt;input type="hidden"> 

&lt;select> 
&lt;option>苹果&lt;/option> 
&lt;option selected="selected">香蕉&lt;/option> 
&lt;option>樱桃&lt;/option> 
&lt;/select>

&lt;textarea name="comment" rows="60" cols="20">
&lt;/textarea> 
&lt;/form>
实体（Entities）

&lt; 等同于 &lt;
 &gt; 等同于 >
&copy; 等同于 ©







