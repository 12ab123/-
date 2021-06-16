web前端

无论是前端工程师还是后端工程师，都是开发软件







## 软件的分类

### c/s架构

​		c表示客户端，s表示服务器

​		客户端：用户通过客户端来操作软件

​		服务器：用来处理软件的业务逻辑

​		当我们在客户端qq中给朋友发个信息，信息会发给服务器，然后服务器发给朋友的客户端

​		特点：

​				c/s架构软件必须安装才能使用

​				c/s架构软件更新时，服务器和客户端都需要更新 

​				c/s架构软件无法跨平台使用，比如windows的qq无法在ios上运行

​				c/s架构软件客户端和服务器之间的通信采用自由的协议，安全性较好







### b/s架构：

​        b表示浏览器，s表示服务器

​		b/s本质上也是c/s，只不过b/s使用浏览器作为软件的客户端

​		b/s实际上就是一个一个的网站，我们可以通过网站来访问软件

​		比如京东，淘宝，12306

​		特点：

​				b/s架构软件不需要安装，可直接使用

​				b/s架构软件无需更新

​				b/s架构软件可以跨平台使用

​				b/s架构软件，客户端和服务器间的通信采用的公共的HTTP协议，安装性较差







### 万维网联盟(W3C)

该联盟试图制作一套标准来解决网络应用在不同平台间的兼容问题

我们所开发的应用都需要遵循W3C的规则



W3C的标准：一个网页主要由三部分组成：**结构**，**表现**，**行为**

结构--------------->HTML：用于描述页面的结构

表现--------------->CSS：用于控制页面中的元素的样式

行为--------------->JavaScript：用于相应用户的操作

一个设计优良的网页，要求结构，表现，行为三者分离













## HTML

HTML：超文本标记语言

标签：元素

属性：属性可以用来设置标签如何处理其中的内容

**html标签**：网页的根标签，网页中的所有内容都应该写在根标签中

**head标签**：head标签是html的子标签，head的内容不会在网页中显示，它是用来对网页进行一些配置管理

**title标签**：网页的标题，他会显示在浏览器的标题栏上，搜索引擎的爬虫软件会根据title来识别网页的主要内容

**body标签**：网页中所有的可见内容都应该写在body中，有且只有一个

**h1标签**：一级标题

**br**：换行

**p**：段落标签

**hr**：下划线

**注释**：<!-- 内容 -->,注释不能嵌套

**font标签**：在开始标签中可以为元素添加属性，属性可以用来设置元素如何显示其中的内容，属性是一个名值对结构  属性名=“属性值”

```html
<html>     <!--主标签开始-->
    <head> <!--子标签-->
     	<title>第一个网页</title>   
    </head>
    <body><!--子标签-->
        <h1>这是我的<font color='red' size='12'>第一个</font>网页</h1>
    </body>
</html>    <!--主标签结束-->
```

```html
<!DOCTYPE html>   <!--文档声明，告诉浏览器网页的版本 -->
<html lang="en">  <!-- lang属性用来指定语言,en为英语，zh为中文 -->
<head>
   <!--
   自结束标签，meta用来设置网页的基本信息
   <meta charset="UTF-8">用来指定网页的编码
   -->
   <meta charset="UTF-8">
   <title>网页标签</title>    
</head>
    
<body>
	<h1>一级标题</h1>    <!--从h1到h6重要性越来越低，h1重要性仅次于title，搜索引擎会根据h1的内容来判断网页的主要内容-->
    <h2>二级标题</h2>    <!--一般情况下，h1只能有一个，且标题标签只会使用到1~3-->
    <h3>三级标题</h3>
    <h4>四级标题</h4>
    <h5>五级标题</h5>
    <h6>六级标题</h6>
    
    <p>我是一个段
                           <!--在HTML中，不管你有多少个换行和空格，都会解析成一个空格-->
        落</p>			  
    <p>我是一个段落</p>
    <p>
        锄禾日端午，<br>     <!--br表示换行-->
        汗滴禾下土。<br>
        谁知盘中餐，<br>
        粒粒皆辛苦。
    </p>
    <hr>                   <!--hr表示下划线-->
</body>    
</html>
```



 



### 编码

计算机底层中所有的数据都是用二进制（1或0）形式保存的

我们可以把计算机的内存想象成一个个格子，每一个格子中可以存放1或0

一个小格，大小是1bit（位）

8bit = 1byte(字节)

1024byte = 1kb（千字节）

1024kb = 1mb

1024mb = 1gb

1024gb = 1tb



我们所创建的文本文件最终也会存储在磁盘中，需要转换为二进制

当我们打开文本文件时，需要将二进制转换为字符

将字符转换为二进制码的过程，称为编码

将二进制转换为字符的过程，称为解码

编码和解码采用的规则称为charset(字符集)

乱码产生的原因就是因为编码和解码所采用的字符集不同

常见的字符集：

​						ASCII

​						ISO8859-1

​						UTF-8





### HTML字符实体

| 显示结果 | 描述              | 实体名称           | 实体编号 |
| -------- | ----------------- | ------------------ | -------- |
|          | 空格              | & nbsp;            | & #160;  |
| <        | 小于号            | & lt;              | & #60;   |
| >        | 大于号            | & gt;              | & #62;   |
| &        | 和                | & amp;             | & #38;   |
| "        | 引号              | & quot;            | & #34;   |
| '        | 撇号              | & apos; (IE不支持) | & #39;   |
| ￠       | 分（cent）        | & cent;            | & #162;  |
| £        | 镑（pound）       | & pound;           | & #163;  |
| ¥        | 元（yen）         | & yen;             | & #165;  |
| €        | 欧元（euro）      | & euro;            | & #8364; |
| §        | 小节              | & sect;            | & #167;  |
| ©        | 版权（copyright） | & copy;            | & #169;  |
| ®        | 注册商标          | & reg;             | & #174;  |
| ™        | 商标              | & trade;           | & #8482; |
| ×        | 乘号              | & times;           | & #215;  |
| ÷        | 除号              | & divide;          | & #247;  |

语法1：&实体的名字(英文的名字);

​            空格：& nbsp;

​			大于：& lt;

语法2：&#UTF-8的十进制编码;

​			空格：& #160;





### 标签



 #### meta

表示网页中的元数据

```html
    <!--application用于告诉搜索引擎网页的内容-->
    <meta name="application" content="这是一个横好的网站...">
    <!--keywords指定网页的关键字，多个关键字用逗号隔开-->
    <meta name="keywords" content="HTML5,JAVA,大数据">
    <!--用来设置请求的重定向,当你打开网页时，它会在3秒后跳转到另一个指定的网页中-->
    <meta http-equiv="refresh" content="3;url=https://www.baidu.com">
```





#### header，main，footer

```html
<!doctype html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>网页标签</title>
</head>

<body>
    <!--header表示网页的头部，主要用于放置logo，导航，搜索框等-->
    <header>
        <h1>我是网页的头部</h1>
    </header>
    <!--main表示网页的主体内容-->
    <main>
        我是网页的主体
    </main>
    <!--footer表示网页的底部，主要放置一些版权信息,友情链接，联系方式....-->
    <footer>
        我是网页的底部
    </footer>
</body>
</html>
```



#### nav，article



```html
<!doctype html>
<html lang="en">

<head>
    <meta charset="utf-8">
    <!--application用于告诉搜索引擎网页的内容-->
    <meta name="application" content="这是一个横好的网站...">
    <!--keywords指定网页的关键字，多个关键字用逗号隔开-->
    <meta name="keywords" content="HTML5,JAVA,大数据">
    <!--用来设置请求的重定向-->
    <title>网页标签</title>
</head>

<body>
    <!--header表示网页的头部，主要用于放置logo，导航，搜索框等-->
    <header>
        我是网页的头部
        <!--表示页面的导航栏-->
        <nav>导航栏</nav>
    </header>
    <!--main表示网页的主体内容-->
    <main>
        我是网页的主体
        <!--article表示一个独立的文章-->
        <article>
           <h1>望明月</h1>
            <article>
               <h2>望明月一</h2>
                <p>
                    窗前明月光，<br>
                    疑是地上霜。<br>
                    举头望明月，<br>
                    低头思故乡。<br>
                </p>
            </article>
            
            <article>
               <h2>望明月二</h2>
                <p>
                    窗前明月光，<br>
                    疑是地上霜。<br>
                    举头望明月，<br>
                    低头思故乡。<br>
                </p>
            </article>
        </article>
    </main>
    <!--footer表示网页的底部，主要放置一些版权信息-->
    <footer>
        我是网页的底部
    </footer>
</body>
<!--以上标签都是h5新增的语义化标签，他们并不能支持所有的浏览器，
    以上的标签都可以被div标签代替
-->
</html>

```





#### aside，section，div

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
    </head>
    
    <body>
        <nav>导航栏</nav>
        <aside>侧边栏</aside>
        <section>一个区块</section>
        <div>一个区块</div>
    </body>
</html>
```







#### em，strong，blockquote，span

```html
<!doctype html>
<html lang="en">
    <head>
    <meta charset="utf-8">
    <title>网页标签</title>
</head>

<body>
    <!--em  表示强调，默认浏览器会以斜体显示em中的字体,表示语音上的强调-->
    <p>今天实在<em>太凉快</em>了！</p>
    <!--strong  强调，默认浏览器会加粗，表示语义上的强调-->
    <p>今天对我来说非常<strong>重要</strong></p>
    <!--向em和strong这种不独占一行的标签，称为行内标签-->
    <p>这是一段<i>文字</i></p>
    <p>这是一段<b>文字</b></p>
    <!--i,b,斜体，加粗用来表示一段文字中的特殊内容-->
    <!--q标签表示短引用-->
    <p>鲁迅说：<q>我家的后院有两棵树</q></p>
    <!--文本都会从常规文本中分离出来，经常会在左、右两边进行缩进（增加外边距），而且有时会使用斜体。也就是说，块引用拥有它们自己的空间。
    -->
    <blockquote>
        厂前明月光，<br>
        疑是地上霜。
    </blockquote>
    <!--没有语义，主要作用就是选中文字-->
    <span>我说的你</span>
</body></html>
```



#### img(导入图片)

图片的格式：

​			jpeg（jpg）

​                        支持的颜色丰富，但不支持透明，适合用来显示照片

​			gif

​						支持的颜色比较少，支持透明，支持动图，适合用来显示颜色单一的图片，比如logo，动图

​			png

​						支持的颜色丰富，支持透明支持动图

​			webp

​						google专门为网页设计的一种网页图片格式

​						支持的颜色丰富，支持复杂透明，并且内存小，但是，兼容性差

​			base64编码图片

​						

效果一致时，用小的，效果不一致时，用好的

```html
<!doctype html>
<html long='en'>

<head>
    <meta charset="utf-8">
    <title>网页标签</title>
</head>

<body>
    <!--图片标签用来向网页引入一个外部图片
        使用img标签来引入外部图片
        属性：
            src 图片的路径
            alt 图片的描述
                这个描述不会在页面显示
                但是有可能是图片无法加载时会显示
                搜索引擎会根据alt属性来判断图片的内容
                如果没有alt属性搜索引擎不会对图片进行收录
            width 图片的宽度
            height 图片的高度
            宽度和高度如果修改一个，另一个会等比例缩放
    -->
    <img src=".\1 (2).gif" alt='小松鼠' height="500">
</body>
    
</html>
```







#### iframe(导入网站)

```html
<!doctype html>
<html lang="en">

<head>
    <meta charset="utf-8">
    <title>网页标题</title>
</head>

<body>
    <!--内联框架iframe，用来引入一个外部网站，iframe的内容不会被搜索引擎抓取-->
    <iframe frameborder="0" title="aaa" src="https://www.baidu.com" height="500" width="500">
    </iframe>
</body>

</html>

```









#### audio(导入音频)

```
音频标签属性
	controls	显示控件
	autoplay	自动播放
	loop		循环播发
	preload		预加载
	muted		静音
```



```HTML
<!doctype html>
<html lang="en">
    <head>
    <meta charset="utf-8">
    <title>网页标题</title>
    </head>

    <body>
        <!--使用audio标签来引入外部的音频
            一般情况下，音频默认选中mp3
            
            默认情况下音频不会在页面中显示
            除非加上controls属性
            controls：
                用来控制是否允许用户控制音频的播放
                加上controls，允许用户控制
                不加controls，拒绝用户控制
            autoplay
                自动播放音频
                但是有些网站不允许
                加上，自动播放
                不加，不会自动播放
        -->
        <audio controls autoplay src="ABBB.mp3"></audio>
        
    </body>

</html>
```





#### source

```html
<!doctype html>
<html lang="en">
   <head>
    <meta charset="utf-8">
    <title>网页标签</title>
   </head>
   
   <body>
     <!--source标签必须和audio标签嵌套使用，否则无法在页面中显示音频，
         sour最大的好处是可以使用输出多个音频，当第一个音频在网页中无法使用，就会使用第二个音频，第二个不行，使用第三个，如果所有的音频都在网页中无法使用，就会显示你输入的指定字体
     -->
      <audio controls autoplay>
       音频格式错误！
       <source src="ABBB.mp3">
       <source src="Charlie%20Puth%20-%20How%20Long.mp3">
      </audio>
   </body>
</html>
```







#### embed

```html
<!doctype html>
<html lang="en">
   <head>
    <meta charset="utf-8">
    <title>网页标签</title>
   </head>
   
   <body>
      <!--embed支持在版本低的网页中显示-->
      <embed src="ABBB.mp3" width="300" height="211">
   </body>
</html>
```

可以嵌套使用

```html
!doctype html>
<html lang="en">
   <head>
    <meta charset="utf-8">
    <title>网页标签</title>
   </head>
   
   <body>
      <audio controls autoplay>
       音频格式错误！
       <source src="ABBB.mp3">
       <source src="Charlie%20Puth%20-%20How%20Long.mp3">
       <embed src="ABBB.mp3" width="200" height="300">
       <!--当source的音频在网页中无法使用时，就会使用embed中的音频-->
      </audio>
   </body>
</html>
```









#### video(导入视频)

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
    </head>
    
    <body>
        <!--<video controls src="12ab.mp4" width="300" height="500"></video>
        -->
        <!--也可以这样使用，导入多个不同格式的视频-->
        <video controls width="300" height="500">
            <source src="12ab.mp4">
            <source src="12ab.webm">
            <embed src="12ab.mp4" width="300" height="500">
        </video>
        
    </body>
</html>
```







#### a标签(超链接)

```html
<!doctype html>
<html lang="en">
   <head>
       <meta charset="utf-8">
       <title>网页标签</title>
   </head>
   
   <body>
       <!--
             a标签(超链接)
                  通过超链接可以从一个网页跳转到另一个网页
                  
                  属性：
                      href
                          指定要跳转目标的路径
                          可以指定一个外部网页的地址
                          也可以跳转到当前页面的其他位置
                             #表示当前页面的顶部
                             #id值 跳转到页面中指定元素的位置
                                 id:
                                    每一个元素都可以有一个属于自己的id
                                    相当于身份证，是独一无二的
                      target
                          表示打开链接的位置
                          _self：在当前窗口打开
                          _blank：在新窗口打开
        -->
        <a href="https://www.baidu.com" target="_blank">去百度</a>
        <br><br>
        <a href="12ab.mp4">去看视频</a>
        <br><br>
        <a href="#p1">去第一段</a>
        <a></a>
        <br><br>
        <a href="#down">去底部</a>
        <p id="p1">早上，阳光明媚的。我已经从甜美的睡梦中醒来，阳光让我更精神了，可妈妈还在睡梦中，她又不舒服。

我知道妈妈很累，我自己先起床了，为了不吵醒妈妈我轻声请步的。终于我到楼下去了！我真不相信，我连脸洗了，牙也刷了。妈妈还没起床，我自言自语的说：“太好了，这样我就可以做一顿丰富的早餐了！”我先把面包烧起来，再到一杯牛奶，然后再拿出沙拉酱，OK！完成了。已经7：10分了，以前妈妈都是6：45起床的，都超了好长时间了，我到楼梯口大叫道：“妈妈，妈妈，妈妈！。。。。。。”我还真准时妈妈干好起床。我先读语文书，等着妈妈下来，妈妈一下楼，我就说：“妈妈快点洗脸，吃早餐吧！”，妈妈看到一桌丰富的早餐兴奋的说：“宝贝，真棒，妈妈的早餐都没有你的好呢！。。。。。。

我知道妈妈想让我开心，但我知道妈妈她最爱我，我爱妈妈，我是妈妈的左右手！</p>
        <p>早上，阳光明媚的。我已经从甜美的睡梦中醒来，阳光让我更精神了，可妈妈还在睡梦中，她又不舒服。

我知道妈妈很累，我自己先起床了，为了不吵醒妈妈我轻声请步的。终于我到楼下去了！我真不相信，我连脸洗了，牙也刷了。妈妈还没起床，我自言自语的说：“太好了，这样我就可以做一顿丰富的早餐了！”我先把面包烧起来，再到一杯牛奶，然后再拿出沙拉酱，OK！完成了。已经7：10分了，以前妈妈都是6：45起床的，都超了好长时间了，我到楼梯口大叫道：“妈妈，妈妈，妈妈！。。。。。。”我还真准时妈妈干好起床。我先读语文书，等着妈妈下来，妈妈一下楼，我就说：“妈妈快点洗脸，吃早餐吧！”，妈妈看到一桌丰富的早餐兴奋的说：“宝贝，真棒，妈妈的早餐都没有你的好呢！。。。。。。

我知道妈妈想让我开心，但我知道妈妈她最爱我，我爱妈妈，我是妈妈的左右手！</p>
        <p>早上，阳光明媚的。我已经从甜美的睡梦中醒来，阳光让我更精神了，可妈妈还在睡梦中，她又不舒服。

我知道妈妈很累，我自己先起床了，为了不吵醒妈妈我轻声请步的。终于我到楼下去了！我真不相信，我连脸洗了，牙也刷了。妈妈还没起床，我自言自语的说：“太好了，这样我就可以做一顿丰富的早餐了！”我先把面包烧起来，再到一杯牛奶，然后再拿出沙拉酱，OK！完成了。已经7：10分了，以前妈妈都是6：45起床的，都超了好长时间了，我到楼梯口大叫道：“妈妈，妈妈，妈妈！。。。。。。”我还真准时妈妈干好起床。我先读语文书，等着妈妈下来，妈妈一下楼，我就说：“妈妈快点洗脸，吃早餐吧！”，妈妈看到一桌丰富的早餐兴奋的说：“宝贝，真棒，妈妈的早餐都没有你的好呢！。。。。。。

我知道妈妈想让我开心，但我知道妈妈她最爱我，我爱妈妈，我是妈妈的左右手！</p>
        <p>早上，阳光明媚的。我已经从甜美的睡梦中醒来，阳光让我更精神了，可妈妈还在睡梦中，她又不舒服。

我知道妈妈很累，我自己先起床了，为了不吵醒妈妈我轻声请步的。终于我到楼下去了！我真不相信，我连脸洗了，牙也刷了。妈妈还没起床，我自言自语的说：“太好了，这样我就可以做一顿丰富的早餐了！”我先把面包烧起来，再到一杯牛奶，然后再拿出沙拉酱，OK！完成了。已经7：10分了，以前妈妈都是6：45起床的，都超了好长时间了，我到楼梯口大叫道：“妈妈，妈妈，妈妈！。。。。。。”我还真准时妈妈干好起床。我先读语文书，等着妈妈下来，妈妈一下楼，我就说：“妈妈快点洗脸，吃早餐吧！”，妈妈看到一桌丰富的早餐兴奋的说：“宝贝，真棒，妈妈的早餐都没有你的好呢！。。。。。。

我知道妈妈想让我开心，但我知道妈妈她最爱我，我爱妈妈，我是妈妈的左右手！</p>
        <a id="down" href="#">去顶部</a>
   </body>
    
</html>s
```













#### 列表

列表主要用来表示多个并列关系的内容

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
    </head>
    
    <body>
       <!--有序列表：

				使用 ol 标签来创建一个有序列表

				使用 li 标签来表示列表中的一个项

           无序列表：

				使用 ul 标签来创建一个无序列表

				使用 li 标签来表示列表中的一个项
       -->
        <ol>
            <li>结构</li>
            <li>表现</li>
            <li>行为</li>
        </ol>
        
        <ul>
            <li>结构</li>
            <li>表现</li>
            <li>行为</li>
        </ul>
        
        <!--嵌套使用-->
        <ul>
            <li>鱼香肉丝
                <ol>
                    <li>鱼</li>
                    <li>肉</li>
                </ol>
            </li>
            <li>宫保鸡丁</li>
        </ul>
        
        
        <!--定义列表，主要用来对内容进行定义
            使用 dl 标签来创建列表
            使用 dt 标签定义项
            使用 dd 标签描述定义项
        -->
        <dl>
            <dt>CSS</dt>
                <dd>负责页面中的表现</dd>
            <dt>HTML</dt>
                <dd>负责页面的结构</dd>
            
        </dl>
        
        
        
        
    </body>
</html>
```

list-style：指定列表中每个li开头的样式













## CSS

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
        
        <style>
            p{
                color: red;
                font-size: 80px;
                background-color: yellow
            }
            
            h1{
                color: blue;
                font-size: 32px;
                background-color: chartreuse
            }
        </style>
        <!--link标签，调用外部资源    -->
        <link rel="stylesheet" href="style.css">
    </head>
    
    <body>
<!--CSS(层叠样式表)
    用来处理网页的表现
    网页中所有外在显示效果都是CSS来控制
    -->
<!--
    第一种方式：可以直接将CSS代码编写到标签的style属性中
              缺点：太过耦合，不方便代码的复用，不方便后期的维护，开发时绝对不要使用这一样式
    第二种方式：将样式写在style标签中(style写在head标签中)
              将样式编写到style标签中，然后通过CSS选择器选中指定的元素并为其设置样式，将html和css分离，使css样式可以复用，方				便后期维护
              缺点：只对当前页面使用，其他页面无法使用
    第三种方式：将页面中的css代码编写到外部的css文件中
              新建一个css文件，在文件中写入代码，在网页中使用link导入，就可以在多个网页中使用
              
           -->

    
    <p style="color: red;font-size: 35px">窗前明月光，疑是地上霜</p>
    <p>举头望明月，低头思故乡。</p>
    <h1>我是一个一级标签</h1>
    </body>
</html>
```



CSS的注释

```css
/*我是单价对比*/
```



CSS的语法

```css
/*
	语法：
		选择器  声明块
		选择器：
			通过选择器可以选中页面中的指定元素
			指定元素：
					p  选中所有p标签(元素)
					div  选中所有div标签
					等等....
		声明块：
			整体是一对大括号
			声明块是由一个个声明构成的
			声明是一个名值对组成，名和值由 : 连接，由 ; 结尾
			声明块中的所有样式将会应用到其前面选择器选中的元素中，改变元素的属性
*/
```







### 选择器

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
        
        <style>
/*元素选择器，根据标签名来选中选择器 */
            h1{
                color: blue;
                font-size: 50px;
            }
            
            p{
                color: red;
                
                
            }
/*id选择器，根据id的值来选中选择器*/
            #p0{
                color: black;
            }
/*并集选择器*/
            #p1,#p2,#p3{
                color: yellow;
                background-color: darkgreen
            }
            
            
/*除了id属性，也可以为元素添加一个class属性，
            clas属性的作用是为元素进行分类，         
            拥有相同class属性的元素属于同一类元素，
            我们可以给一个元素设置多个class属性*/
            .p4{
                color: darkviolet;
            }
            
            .p5{
                background-color: darkgrey
            }
/*通配选择器，使用*号来选择所有属性*/
            *{
                color: floralwhite;
            }
        </style>
    </head>
    
    
    <body>
        <h1>白居易</h1>
        <p id="p0">大漠孤烟直，长河落日圆。</p>
        <p id="p1">大漠孤烟直，长河落日圆。</p>
        <p id="p2">大漠孤烟直，长河落日圆。</p>
        <p id="p3">大漠孤烟直，长河落日圆。</p>
        <p class="p4 p5">大漠孤烟直，长河落日圆。</p>
        <p class="p4">大漠孤烟直，长河落日圆。</p>
        <p class="p4">大漠孤烟直，长河落日圆。</p>
        <p class="p5">大漠孤烟直，长河落日圆。</p>
        <p>大漠孤烟直，长河落日圆。</p>
    </body>
</html>
```

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
        <style>
/*交集选择器：选中符合选择器的指定元素*/
            div.box{
                font-size: 46px;
            }
        </style>
    </head>
    
    <body>
       <div class="box">是大V比打包</div>
        <p class="box">我速度吧</p>
        <div class="box">大V十多度VB以</div>
    </body>
</html>
```











#### 伪类选择器

```html
<!doctype html>
<html lang="en">

<head>
    <meta charset="utf-8">
    <title>网页标签</title>
    
    <style>
        /*将div中的第一个元素变为红色*/
        div p:first-child{
            color: red;
        }
    </style>
</head>

<body>
<!--伪类选择器一般用来表示元素的一些特殊的状态或者特殊的位置
    :first-child
            表示第一个元素

-->
<div>
   
    <P>皇室都是堵</P>
    <P>皇室都是堵</P>
    <P>皇室都是堵</P>
    <P>皇室都是堵</P>
</div>
</body>

</html>

```





![img](https://img-blog.csdn.net/20161226194357051?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvTU9PTkNPTQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)

![img](https://img-blog.csdn.net/20161226194429024?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvTU9PTkNPTQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)







#### 元素选择器

```html
<style>
/*选择元素h1，h2，h3，将指定元素中的字体颜色变为红色，字体变为50*/
    h1,h2,h3{
        color:red;
        font-size:50px;  
    }
</style>
```









#### 类选择器

类class可以有多个重复的

```html
<style>
    h1.box{    /*选择元素为h1，且类为box的元素，将指定元素中的字体颜色变为红色，字体变为50*/
        color:red;
        font-size:50px;
    }
    
    .box{   /*选择类为box的元素，将指定元素中的字体颜色变为红色，字体变为50*/
        color:red;
        font-size:50px;
    }
</style>
```







#### id选择器

id只有一个，是唯一的

```html
<style>
    #ha{       /*获取id为ha的元素，将指定元素中的字体颜色变为红色，字体变为50*/
        color:red;
        font-size:50px;
    }
</style>
```









#### 后代选择器

```html
<style>
    div p{       /*使元素中所有为div的p的元素变为红色,不管p是子元素还是孙元素
        color:red;
        
    }
</style>
```







#### 子选择器

```html
<style>
    div > em{    /*使div中所有子元素为em的元素颜色变为红色
        color:red;
    }
</style>
```















#### 伪类选择器

```html
:first-child    第一个元素
:first-of-type  同类型中第一个元素
:last-child     最后一个元素
:last-of-type   同类型中最后一个元素
:nth-child(n)   第n个元素
:nth-of-type(n) 同类型中第n个元素
:only-child     唯一的子元素
:only-of-type   同类型中唯一的元素
:empty			空元素
:not()          除了
:link           正常的链接(没访问的链接)
:visited        访问过的链接
:hover   		鼠标移入的状态
:active 		鼠标点击的状态

```







#### 属性选择器

```html
<style>
    [title]{       /*选择所有含有title属性的元素*/
        color:red;
    }
</style>
```



```html
<style>
        [title='hello']{  /*选择所有title属性为hello的元素*/
            color: red;
        }
</style>
```



```html
<style>
        [title^='h']{   /*选择所有title属性开头为h的元素*/
            color: red;
        }
    </style>
```



```html
<style>
        [title$='h']{    /*选择所有title属性结尾为h的元素*/
            color: red;
        }
    </style>
```



```html
<style>
        [title*='h']{    /*选择所有title属性含有h的元素*/
            color: red;
        }
    </style>
```



```html
<style>
        [title*='h' i]{    /*选择所有title属性含有h的元素，忽略大小写*/
            color: red;
        }
    </style>
```











### 伪元素

**::before和::after**

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
        
    </head>
    <style>

        #zbc::before{   /*在指定元素前面添加内容  content：添加内容*/
            content:"张三";
            color:red;
        }
        
        .box::after{   /*在指定元素后面添加内容*/
            content: "不必时刻";
            color: yellow;
        }
    </style>
    
    <body>
        <div id="zbc">我爱你</div>
        <div class="box">的女女</div>
    </body>
</html>
```



**frist-letter和first-line**

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
        
    </head>
    <style>
        div::first-letter{  /*选中指定元素内容的第一个字*/
            font-size: 50px;
        }
        
        div::first-line{   /*选中指定元素内容的第一行*/
            color: red;
        }
    </style>
    
    <body>
        <div id="zbc">我爱你</div>
        <div class="box">的女女</div>
    </body>
</html>
```



**selection**

```html
!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
        
    </head>
    <style>
        div::selection{   /*选中元素的所有内容，当我们使用鼠标在页面中选中内容时，会发生指定变化*/
            color: red;
        }
    </style>
    
    <body>
       <div>一九七九年那是一个春天
　　有一位老人在中国的南海边画了一个圈
　　神话般地崛起座座城
　　奇迹般聚起座座金山
　　春雷啊唤醒了长城内外
　　春辉啊暖透了大江两岸
　　啊，中国中国
　　你迈开了气壮山河的新步伐
　　你迈开了气壮山河的新步伐
　　走进万象更新的春天
　　一九九二年又是一个春天
　　有一位老人在中国的南海边写下诗篇
　　天地间荡起滚滚春潮
　　征途上扬起浩浩风帆
　　春风啊吹绿了东方神州
　　春雨啊滋润了华夏故园
　　啊，中国中国
　　你展开了一幅百年的新画卷
　　你展开了一幅百年的新画卷
　　捧出万紫千红的春天
　　啊......</div>
    </body>
</html>
```









### 继承

就好像生活中，子女会继承祖先财产一样

在网页中后代元素也会继承祖先元素上的样式

为祖先元素设置样式，也会应用到其后代元素上 

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
        
        <style>
            p{
                color: red;
            }
        </style>
        
    </head>
    
    
    <body>
      <p>这是也<spen>我我们<em>都不知道的</em>东西</spen></p>
    </body>
</html>
结果：p元素中的字体全部变为红色
```

继承的结果大大的简化了样式的编写

可以只为祖先元素设置样式，即可让后代元素都同时具有该样式

但是有些样式不会被继承，列如：背景色，宽度等







### 优先级

当选择器使用的样式相同时，会发生冲撞，此时，就需要看优先级，优先级高的使用，低的不使用

内联样式   1000

id选择器   100

类和伪类    10

元素             1

通配选择器    0

如果两个选择器的优先级相同，则使用靠下的样式

！important可以在一个样式的最后添加它，这样样式将会获得更高的优先级，优先所有样式，慎用









### 单位

px(像素)

​			—显示器上的图像是由一个一个发光的小点点构成，一个小点就是一个像素

​				在默认的情况下，css像素和物理像素相同

​				在不同的显示器中，像素的大小不同

​				像素点越小，越清晰

​				一些高清屏会将像素放大，使一个css像素等于多个物理像素







百分比

​			—百分比会相对于包含块的指定属性去计算值

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
        
        <style>
            .box{
                width: 300px;
                height: 300px;
                background-color: red;
                
            }
            
            .box1{
                width: 50%;
                height: 50%;
                background-color: rgb(0%,100%,0%);
            }
        </style>
        
    </head>
    
    <body>
        <div class="box">
            <div class="box1">
                
            </div>

        </div>
    </body>
</html>
```





颜色单位

   1. 可以使用颜色名来直接设置颜色

   2. 可以使用RGB值来设置颜色

      ​     RGB值(red   green   blue)

      ​	  RGB值可以通过三种颜色不同的浓度来调配出其他的yanse

      ​	  语法    rgb(红色，绿色，蓝色)

      ​				值的范围0~255

      ```html
      rgb(255,0,0)   红色
      rgb(0,255,0)   绿色
      rgb(0,0,255)   蓝色
      rgb(0%,100%,0%)     绿色
      rgba(0,0,255,.5)    a表示透明度，0.5表示半透明
      ```



​     使用十六进制的rgb的值

   				语法：#红色绿色蓝色

​								需要使用两位十六进制的数字来表示每种颜色的浓度

​								范围00---ff

```html
#00ff00       绿色
#0f0          和上面一样，如果两位十六进制的值一样，可以使用一个表示
```



3. hsl()也可以用来表示颜色

      	h表示色相     0~360

   ​	   s表示饱和度    0%~100%

   ​	    l表示亮度       0%~100%









### 盒子模型

浏览器在渲染页面时，会将页面中的每一个元素想象成一个矩形的盒子

想象成盒子之后，对于页面的布局就变成了如何摆放盒子

每一个盒子从内到外都有以下几个部分组成

​		**内容区(content)**

​				内容区决定了这个盒子能装多少东西(子元素)

​		**内边距(padding)**

​				内容区和边距之间的距离

​		**边框(border)**

​				盒子的边框，决定了盒子的大小

​		**外边距(margin)**

​				盒子距离其他盒子的距离

![img](https://p0.ssl.img.360kuai.com/t018de773727591629a.jpg)



#### 边框



```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
        
        <style>
            .box{
/* 默认情况下，width和height决定了元素的内容区的大小*/
                width: 300px;
                height: 300px;
                background-color: red;
/*边框，是盒子的边框，出了边距就是盒子的外部
                边框相关的三个样式
                    border-color    边框的颜色
                    border-style    边框的样式
                    border-wigth    边框的宽度*/
                border-color: yellow;
                border-width: 20px;
                border-style: solid;
            }
        </style>
        
    </head>
    
    <body>
        <div class="box">


        </div>
    </body>
</html>
```



**border-width**

即使不指定宽度，也会有一个默认值

```html
/*border-width: 30px 30px 40px 50px;  表示上右下左四个方向 */
/*border-width: 30px 20px 10px;       值：上  左右   下*/
/*border-width: 30px 10px;            值：上下   左右*/
/*border-width: 30px;                 值：上左右下*/
```



**border-color**

即使不指定颜色，默认会使用字体的颜色，当我们更改字体颜色时，并且不指定边框颜色时，使用的是字体的颜色

```html
可以指定四个边框的颜色，规则和broder-width一样

```



**border-style**

```html
可以指定四个边框的样式，规则和broder-width一样
solid    实线
dotted   点状虚线
dashed   虚线
double   双线
border-style: double dashed solid ridge;
```





边框的简写属性   border

​	通过该属性可以同时设置四个方向边框的宽度，颜色，样式

​	并且没有顺序要求

```html
border:10px red solid;
border:red solid 20px;
```

但是无法给边框的四个方向单独设置

所有可以使用

​		border-top         上

​		border-right       右

​		border-bottom   下

​		border-left           左

```html
border:20px red solid;
border-left:none;
将上下右设置为宽20像素，颜色为红，样式为实线，左边什么也不设置
```







#### 内边距

边框和内容区之间的距离叫做内边距(padding)

一共有四个方向

​		padding—top

​		padding—right

​		padding—bottom

​		padding—left









#### box—sizing

默认情况下，width和height指定的是盒子内容区的大小

可以通过box—sizing来修改盒子大小的计算方式

​	可选值：

​			content—box   默认值，内容盒子（width和height指定内容区的大小）

​			border—box    width和height指定整个盒子的大小，也就是内容区+内边距+边框的大小

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
        
        <style>
            .box{
                width: 300px;
                height: 100px;
                background-color: red;
                border:yellow 10px solid;
                box-sizing: border-box;
            }
            
        </style>
        
    </head>
    
    <body>
        <div class="box">
        </div>
    </body>
</html>
```















#### 外边距

当前盒子和其他盒子的距离称之为外边距(margin)

外边距不会影响盒子的可见框的大小

但是会影响盒子实际占地的大小，影响盒子的位置



四个方向的外边距：

​		margin-top

​		margin-left

​		margin-bottom

​		margin-right

由于浏览器默认情况下，元素是靠上靠左的，

所以当我们设置上左边距时，会移动元素自身

当我们设置下右边距时，会移动其他元素

外边距可以使用负值，如果是负值，则元素回向相反的方向移动







#### 水平方向

子元素在父元素的位置是父元素的内容区

子元素在父元素中的水平方向的布局，必须满足一下等式

如果七个值的和不等于父元素的宽度，则属于过度约束，浏览器会自动调节右边距的值

在水平方向，有三个值可以设auto

margin-left     margin-right    width

设置auto后，浏览器会自动计算该属性的值

如果将margin-left 或   margin-right的一侧设置为auto，另一侧会为0

如果将margin-left 和  margin-right都设置为auto，另两侧一样宽









#### 垂直方向

宽度是auto时，子元素会占满父元素

高度是auto时，父元素的高度由内容决定

如果不给父元素指定高度，则父元素会自动适应子元素的高度，确保能容纳所有的子元素

如果给父元素指定高度，则指定多少就是多少，此时如果子元素的高度超过父元素的高度，

则会导致子元素溢出，溢出的子元素不会影响布局







#### overflow

```html
<!doctype html>
<html lang="en">
    <head>
    <meta charset="utf-8">
    <title>网页标签</title>
    
    <style>
        .box{
            width: 200px;
            height: 400px;
            background-color: #bfa;
            overflow: auto;
/*            使用overflow来设置溢出内容的处理方式
              可选值：
                    visible  默认值，溢出的内容不会被裁剪，直接显示在父元素外溢出
                    hidden   溢出的内容会被裁剪
                    scroll   生成滚动条
                    auto     根据需要生成滚动条
            */
        }
        
        .box1{
            width: 50%;
            height: 700px;
            background-color: yellow;
            
        }
        
        .box2{
            width: 100px;
            height: 100px;
            background-color: blue;
        }
        </style>
</head>

<body>
    <div class="box">
        <div class="box1">
            
        </div>
         <div class="box2">
            
        </div>
        
    </div>
   
</body></html>
```









#### 外边距的折叠

垂直方向相邻的外边距，会发生外边距折叠现象

兄弟元素间的相邻外边距

   		 如果两个外边距都是正数，会取两个外边距间的最大值

​			如果都是负外边距，则取绝对值较大的

​			如果是一正一负，取两值的和





父子元素间的相邻外边距

​			父子元素的相邻垂直外边距，子元素的外边距会传递给父元素

​			当我们改变子元素的外边距时，父元素的外边距也会发生改变，

​			如果不想让父元素的外边距发生改变，可以将子元素的外边距与父元素的外边距隔开

​			也就是用内边距或者边框将其隔开











#### 文档流

​       文档流是网页中的一个位置，默认情况下页面中的所有元素都在文档流中排列

​		块元素在文档流的特点

​			自上而下进行排列（独占一行）

​			默认宽度和元素一样

​			默认高度被内容撑开



​		行内元素在文档流的特点

​			自左向右水平排列，如果一行中不足以容纳所有的元素则切换到下一行继续自左向右水平排序

​			高度和宽度都被内容撑开









#### 行内元素的盒模型

水平方向相邻的外边距不会重叠，而是相加

内联元素不支持设置高度和宽度

内联元素可以设置内边距和边距，  如果是垂直方向的padding和border，不会影响页面的布局

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>页面标签</title>
        <style>
            .box{
/*                内联元素不支持设置高度和宽度*/
                background-color: yellow;
                height: 100px;
                width: 200px;
/*                内联元素可以设置内边距和边距，
                如果是垂直方向的padding和border，不会影响页面的布局*/
                padding: 20px;
            }
            .box1{
                height: 100px;
                width:100px;
                background-color: red;
            }
        
        </style>
    </head>
    
    
    <body>
        <span class="box">我是一个spen</span>
        <span class="box">我是一个spen</span>
        <span class="box">我是一个spen</span>
        <div class="box1"></div>
    </body>
</html>
```







#### display

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>页面标签</title>
        <style>
            a{
/*                display
                        指定元素所产生框的类型
                        可选值：
                            inline        行内元素
                            block         块元素
                            inline-block  行内块元素
                                既有行内元素的特点，不独占一行
                                又有块元素的特点，可以设置宽高
                			none          元素不在页面中显示
                */
                display: inline-block;
                width: 100px;
                height: 200px;
                background-color: yellow;
            }
            
        
        </style>
    </head>
    
    
    <body>
        <a href="#">我是一个超链接</a>
        <a href="#">我是一个超链接</a>
        <span>wosohsduusd</span>
    </body>
</html>
```



#### visibility

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>页面标签</title>
        <style>
            .box1{
                width: 100px;
                height: 100px;
                background-color: yellow;
/*                visibility
                        可以设置元素的显示的状态
                        可选值：
                            visible  默认值，元素正常显示
                            hidden   不显示元素，但是元素依然占据位置*/
                visibility:hidden;
            }
            
            .box2{
                width: 100px;
                height: 100px;
                background-color: yellow;
            }
            
        </style>
    </head>
         
    <body>
        <div class="box1">
            
        </div>

        <div class="box2">
            
        </div>
    </body>
</html>
```





#### 默认样式

为了确保网页在没有样式的情况下，也可以浏览，所有浏览器都会为网页设置一些默认的样式，这些默认样式对于我们的开发来说没有任何的作用，并且不同的浏览器所设置的默认样式是不同的，所有开发中我们要做的第一件事往往就是去除网页的默认样式

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
        <style>
            /*
            .box{
                width:200px;
                height: 200px;
                background-color: yellow;
                
            }
            body{
                margin:0px;  
            }
            p{
                margin: 0px;
            }
            
            ul{
                margin: 0;
                padding: 0;    这个方法太过麻烦
            }
            */
            
            *{
               margin:0px;
               padding:0px;
            }
        </style>
    </head>
    
    <body>
        <div class="box"></div>
        <p>我是一个单路</p>
        <p>我是一个单路</p>
        <p>我是一个单路</p>
        <ul>
            <li>喝啊</li>
            <li>军不打卡</li>
            <li>道具殴打</li>
        </ul>
    </body>
</html>
```







#### 块和行内

块元素：主要用于页面的布局

行内元素：主要用于在页面中选中文字

一般情况下，我们只会在块元素中放行内元素，不会在内联元素中放块元素

p元素中不能放任何块元素

a元素里什么都能放，除了他自己





​				





#### 复习

1.盒模型相关的几个属性

```
overflow
	设置元素如何处理溢出的内容
	可选值：
		visible  默认值，不处理溢出的内容，在盒子外显示，不会影响布局
		hidden   溢出的内容会被裁剪下来，不会在页面中显示
        scroll   生成滚动条
        auto     根据需要生成滚动条
```



```
display
指定元素所产生框的类型
     可选值：
         inline          行内元素
         block           块元素
         inline-block    行内块元素
                         既有行内元素的特点，不独占一行
                         又有块元素的特点，可以设置宽高
         none            元素不在页面中显示	
         table           元素会作为一个表格显示
         flex 			 元素作为一个弹性容器显示
         inline-flex     元素作为一个行内弹性容器显示
```



```
visibility
	可以设置元素的显示的状态
    可选值：
         visible  默认值，元素正常显示
         hidden   不显示元素，但是元素依然占据位置*/
```





**外边距折叠**

**兄弟元素间的相邻外边距**

   		 **如果两个外边距都是正数，会取两个外边距间的最大值**

​			**如果都是负外边距，则取绝对值较大的**

​			**如果是一正一负，取两值的和**





**父子元素间的相邻外边距**

​			**父子元素的相邻垂直外边距，子元素的外边距会传递给父元素**

​			**当我们改变子元素的外边距时，父元素的外边距也会发生改变，**

​			**如果不想让父元素的外边距发生改变，可以将子元素的外边距与父元素的外边距隔开**

​			**也就是用内边距或者边框将其隔开**

```html
<!doctype html>
<html>
    <head>
       <meta lang="en">
       <title>网页标签</title>
        <style>
            .box1{
                width: 200px;
                height: 200px;
                background-color: yellow;
            }
            .box2{
                width: 100px;
                height: 100px;
                background-color: blue;
                margin-top: 50px;
                margin-left: 40px;
            }
            .box1::before{
                       content: '';   在两个div元素中间加一个内容，并且将样式设置为table
                        display:table;
                    }
        </style>
    </head>
    
    <body>
        <div class="box1">
           
            <div class="box2"></div>
        </div>
        
    </body>
</html>
```



**文档流**

**文档，文档就是网页**

**文档流是网页中的一个基础位置，页面中的所有元素默认都在文档流中排列**

​		**块元素在文档流中的特点：**

​					**在页面中自上而下排列**

​					**默认跨度是父元素的全部**

​					**默认高度被内容撑开**

​		**行内元素在文档流中的特点:**

​					**在页面中自左向右排序，一行占满换到下一行继续自左向右**

​					**默认宽度和高度都是被内容撑开**







#### 三角

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        div{
            width: 0;
            border-width: 10px;
            border-style: solid;
            border-color: transparent;
            border-top-color: red;
        }
    </style>
</head>
<body>
    <div></div>
</body>
</html>
```







#### radius圆角

```html
<!doctype html>
<html>
    <head>
       <meta lang="en">
       <title>网页标签</title>
        <style>
            .box1{
                width: 200px;
                height: 200px;
                background-color: yellow;
/*                指定元素的圆角
                   需要一个长度值，指定圆角的半径*/
/*
                border-top-left-radius: 100px;
                border-top-right-radius: 100px;
                border-bottom-left-radius: 100px;
                border-bottom-right-radius: 100px;
*/
/*                border-radius:20px 30px 50px 100px;
                */
                border-radius: 50%;
            }
            
        </style>
    </head>
    
    <body>
        <div class="box1"></div>
        
    </body>
</html>
```





#### outline轮廓

**轮廓就是不占空间的边框**，**设置边框不会影响元素的布局**

**不会因为内容区的改变而改变**

```html
outline:1px red solid;
和border的操作一样
```





#### box-shadow阴影

**用来设置元素的阴影，和轮廓一样，阴影不会影响页面的布局**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        div{
            width: 200px;
            height: 200px;
            background-color: teal;
            margin: 100px auto;
            box-shadow: 5px 5px 5px 5px black inset;
        /*
            第一个5px，水平偏移，正数是向右，负数是向左
            第二个5px，垂直偏移，正数是向下，负数是向上
            第三个5px，模糊值
            第四个5px，扩大范围，在原有的基础上各个方向扩大5px
            black:阴影的颜色为黑色
            inset：默认向外，添加这个值就是向内
        */
        }
    </style>
</head>
<body>
<div></div>
</body>
</html>
```

```html
box-shadow: 10px 10px 20px #abf,
                 -10px -10px 20px #abf;
多重阴影
```









#### float浮动

**浮动可以使元素向左或向右移动**

**浮动的特点：**

1. **设置浮动之后，元素会向页面的左侧或右侧移动**
   
2. **设置浮动后，元素会完全脱离文档流，不在占据文档流的位置，所有它下边的元素会自动上移**

      3. **浮动元素不会超过没有浮动的元素**

         				4. **浮动元素的默认位置不会超过其上的其他的浮动元素，最多一边齐**

```html
float
	可选值：
		none   默认值，不浮动
		left   向左浮动
		right  向右浮动

```



**元素脱离文档之后的特点：**

	1. **默认高度，被内容撑开**
	2. **默认宽度，被内容撑开**
	3. **块元素不会独占一行**
	4. **行内元素浮动之后，脱离文档流，变得和块元素一样**







#### 制作一个横着的导航栏

```html
<!doctype html>
<html lang="en">
   <head>
       <meta charset="utf-8">
       <title>WANGY</title>
       <style>
           *{
               margin: 0;
               padding: 0;
           }
           ul{
               width: 700px;
               height: 50px;
               
               margin: 50px auto;
               list-style: none;   #将li前的样式去掉
           }
           ul li{
               float: left;        #li脱离文档流，靠向ul的左侧
               margin-right: 10px;
               
               
           }
           ul a{
               color: black;     #设置颜色
               text-decoration: none;     #将文字的下划线去掉
               
           }
           ul a:hover{       #当鼠标移向链接时，连接的样式
               color: red;
           }
           ul .box a{
               color: red;
           }
       </style>
   </head>
    
    <body>
        <ul>
            <li class="box"><a href="#">秒杀</a></li>
            <li class='box'><a href="#">优惠券</a></li>
            <li><a href="#">PLUS会员</a></li>
            <li><a href="#">品牌闪购</a></li>
            <li><a href="#">拍卖</a></li>
            <li><a href="#">品牌闪购</a></li>
            <li><a href="#">品牌闪购</a></li>
            <li><a href="#">品牌闪购</a></li>
            <li><a href="#">品牌闪购</a></li>
            <li><a href="#">品牌闪购</a></li>
        </ul>
    </body>
</html>
```









```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
        <style>
            *{
                margin: 0;
                padding: 0;
            }
            .nav-list{
                /*设置宽高*/
                width: 1210px;
                height: 48px;
                /*设置背景色*/
                background-color: #E8e7e3;
                /*设置位置*/
                margin: 50px auto;
            }
            .nav-list a{
                /*设置字体颜色*/
                color: black;
                /*将链接设置为浮动*/
                float: left;
                /*设置字体大小*/
                font-size: 20px;
                /*去掉下划线*/
                text-decoration: none;
                /*设置行高，使文字居中*/
                line-height: 48px;
                /*设置内边距，内边距中的背景色和内容区的背景色是一样的*/
                padding: 0px 25px;
            }
            .nav-list a:hover{
                /*设置鼠标移入后的样式*/
                background-color: black;
                color: aliceblue;
                
            }
        </style>
    </head>
    
    <body>
        <nav class="nav-list">
            <a href="#">HTML/CSS</a>
            <a href="#">JavaScript</a>
            <a href="#">Server Side</a>
            <a href="#">ASP.NET</a>
            <a href="#">XML</a>
            <a href="#">Web Services</a>
            <a href="#">Web Building</a>
        </nav>
    </body>
</html>
```









#### 浮动和文字

**当我们设置两个块元素，将上一个块设置为浮动，下面的块会上升，但会被设置为浮动的块给盖住**

**若将下面的块设置为浮动，布局不会发生变化**



**文字不会被浮动元素盖住，而是环绕在浮动元素四周，从而我们可以利用浮动来实现文字环绕图片的效果**









#### 浮动的问题 高度塌陷

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
        
        <style>
            .box{
               border: 10px red solid;
/*               float: left;*/
/*               display:inline-block;*/
/*               overflow: auto;*/
            }
            .box1{
                width: 100px;
                height: 100px;
                background-color: aqua;
                float: left;
/*          高度塌陷，块元素的高度默认的情况下是被子元素撑开的
                如果子元素浮动，将会完全脱离文档流，脱离文档流子元素无法撑起父元素的高度
                将会导致父元素的高度丢失，父元素一旦丢失，页面中的其他元素的位置也会发生移动，导致布局混乱
                
                
                BFC(Block Format Context)
                    ——块级格式化环境
                    ——BFC是元素的一个隐藏的属性，一旦元素开了BFC它将会开启一个独立的布局的区域
                        这个布局区域将会具有一些特殊的性质：
                            1.开启了BFC的元素的子元素垂直外边距不会传递给父元素
                            2.开启了BFC的元素不会被浮动的元素所覆盖
                            3.开启了BFC的元素可以包含浮动的子元素
                    
                    ——BFC无法直接开启，需要通过一些属性来开启
                        1.将元素设置为浮动可以开启BFC,但是会丢失宽度，并且会影响页面的布局
                        2.将元素设置为行内元素,会丢失宽度
                        3.可以将元素的overflow设置为非visible的值
*/
            }
            .box3{
                width: 100px;
                height: 100px;
                background-color: oldlace;
            }
        </style>
    </head>
    
    <body>
        <div class="box">
            <div class="box1"></div>
        </div>
        <div class="box3"></div>
    </body>
</html>
```

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
        
        <style>
            .box{
               border: 10px red solid;

            }
            .box1{
                width: 100px;
                height: 100px;
                background-color: aqua;
                float: left;

            }
/*
            .box3{
                clear: both;   方法1
            }
*/
            
/*
            .box:after{
                content: '';
                display: block;    方法2
                clear: both;
            }
*/
            
            .box::before,.box::after{
                content: '';          这个方法完美的解决了折叠和塌陷的问题，副作用最小，除非你需要使用before或after
                display: table;
                clear: both;
            }
            }
        </style>
    </head>
    
    <body>
        <div class="box">
            <div class="box1"></div>
            <div class="box3"></div>
        </div>
        
    </body>
</html>
```









#### clear

```html
<!doctype html>
<html lang="en">
   <head>
       <meta charset="utf-8">
       <title>网页标签</title>
       
       <style>
           .box{
               width: 100px;
               height: 100px;
               background-color:beige;
               float: left;
               
           }
           .box1{
               width: 150px;
               height: 100px;
               background-color:yellow;
                   float: right;
           }
           .box2{
               width: 140px;
               height: 150px;
               background-color:red;
               clear: left;
/*               clear 用来清除浮动元素对当前元素的影响
                    可选值：
                       none   默认值 不清除
                       left   清除左侧浮动元素对当前元素的影响
                       right  清除右侧浮动元素对当前元素的影响
                       both   清除两侧中对当前元素影响最大的那一侧*/
           }
       </style>
   </head>
   
   <body>
       <div class="box"></div>
       <div class="box1"></div>
       <div class="box2"></div>
   </body>
    
</html>
```













#### position 定位

**可以通过定位将元素摆放到页面的任意元素**



 **通过定位我们可以将元素摆放到页面的任意位置**
          **使用position属性来设置元素的定位**
                   **可选值：**
                       **static          默认值  开启定位**
                       **relative      开启相对定位**
                       **absolute    开启绝对定位**
                       **fixed           开启固定定位**

```html
<!doctype html>
<html lang="en">
   <head>
       <meta charset="utf-8">
       <title>网页标签</title>
       
       <style>
           .box1{
               width: 100px;
               height: 100px;
               background-color: #fad;
               
           }
           
           .box2{
               width: 100px;
               height: 100px;
               background-color: #ffa;
/*     
               
               当为元素设置position:relative;则开启元素的相对定位
                   1.开启相对定位，元素不会发生任何变化
                   2.开启相对定位，元素不会脱离文档流
                   3.相对定位的元素，是相对于其在文档流中的位置进行定位的
                   4.相对定位会使元素提升一个层次
                   5.相对定位不会改变元素的性质，块还是块，行内元素还是行内元素
               
               
               当元素定位开启后，可以通过四个方向的偏移量来控制元素的位置：
                   top     元素与其定位位置的顶部距离
                   left    元素与其定位位置的左侧距离
                   right   元素与其定位位置的右侧距离
                   bottom  元素与其定位位置的底部距离*/  
               position: relative;
               top:20px;
               left: 500px;
           }
           
           .box3{
               width: 100px;
               height: 100px;
               background-color: #aff;
               
           }
       </style>
   </head>
    
    <body>
        <div class="box1"></div>
        <div class="box2"></div>
        <div class="box3"></div>
    </body>
</html>
```



```html
<!doctype html>
<html lang="en">
   <head>
       <meta charset="utf-8">
       <title>网页标签</title>
       
       <style>
           .box1{
               width: 100px;
               height: 100px;
               background-color: #fad;
               position: relative;
               
/*            将position设置为absolute则开启元素的绝对定位
                   特点：
                       1.绝对定位会使元素完全脱离文档流
                       2.绝对定位相对于离他最近的开启了定位的祖先元素进行定位，  
             			  如果所有的祖先元素都没有开启定位，
                   		  就相对于html标签进行定位，也就是窗口
                       3.会使元素提升一个层级*/
           }
           .box2{
               width: 100px;
               height: 100px;
               background-color: #ffa;
               position: absolute;
               top:230px;
               
           
           }
           
           .box3{
               width: 130px;
               height: 100px;
               background-color: #aff;
          
           }
       </style>
   </head>
    
    <body>
        <div class="box1"></div>
        <div class="box2"></div>
        <div class="box3"></div>
    </body>
</html>
```

```html
<!doctype html>
<html lang="en">
   <head>
       <meta charset="utf-8">
       <title>网页标签</title>
       <style>
           .box{
               width: 400px;
               height: 400px;
               background-color: yellow;
               position: relative;
               
               
           }
           /*绝对定位元素水平方向布局的等式：
               left + margin-left + boeder-left + padding-left + width + padding-right + border-right + margin-rigth + right==包含块的宽度
           
           此时就有了5个值可以设置auto
              left
              margin-left
              width
              margin-right
              right*/
           .box1{
               width: 100px;
               height: 100px;
               background-color: red;
               position: absolute;
               left: 0;
               right: 0;
               top:0;
               bottom: 0;
               margin: auto;
               
           }
       </style>
   </head>
   
   <body>
       <div class="box"><div class="box1"></div></div>
       
   </body>
    
</html>
```

```html
<!doctype html>
<html lang="en">
   <head>
       <meta charset="utf-8">
       <title>网页标签</title>
       <style>
           body{
               height: 2000px;
           }
           .box{
                width: 600px;
                height: 600px;
                background-color: yellow;
                
               
               
           }
           .box1{
               width: 200px;
               height: 200px;
               background-color: red;
               position: fixed;
/*          将元素的position设置为fixed开启元素的固定定位
               固定定位的特点大部分都和绝对定位一样
               会将元素脱离文档流
               不同的是固定定位总是相对于浏览器的窗口进行定位*/
           }
              
       </style>
   </head>
   
   <body>
       <div class="box"><div class="box1"></div></div>
       
   </body>
    
</html>
```







#### z-index 和 opacity

```html
<!doctype html>
<html lang="en">
   <head>
       <meta charset="utf-8">
       <title>网页标签</title>
       
       <style>
           .box1{
               width: 100px;
               height: 100px;
               background-color: #fad;
               position: relative;
               z-index: 3;
               opacity: 0.5;
               
           }
/*           开启定位的元素都会提升一个层级
                   定位元素层级可以用z-index来设置
                   z-index需要一个整数来做参数，参数越大层级越高
                   如果层级一样，则后面的元素盖住前面的元素
                   父元素的层级再高，也不会盖住子元素
*/
           .box2{
               width: 100px;
               height: 100px;
               background-color: #ffa;
               position: relative;
               left: 50px;
               top:-50px;
               z-index: 2;
               opacity: 0.7;
/*               opacity用来设置元素的不透明度
                   需要一个0 ~ 1 的值
                   rgba()是一个透明的颜色
                   opacity是让元素整个透明*/
           
           }
           
           .box3{
               width: 100px;
               height: 100px;
               background-color: #aff;
               position: relative;
               left: 100px;
               top:-100px;
           }
       </style>
   </head>
    
    <body>
        <div class="box1"></div>
        <div class="box2"></div>
        <div class="box3"></div>
    </body>
</html>
```











### 字体和文本属性font

```html
<!doctype html>
<html lang="en">
   <head>
       <meta charset="utf-8">
        <title>网页标签</title>
        <style>
            .box{
                color: red;     给字体设置颜色
                font-size:      给字体设置大小
                font-family:    设置字体样式，如果设置多个字体，用逗号隔开
                    属性：serif         衬线字体
                         sans-serif    无衬线字体
                         monospace     等宽字体
                         cursive       草书字体
                         fantasy       装饰字体
            }
       </style>
      </head>
      
    <body>
        <div class="box">dvkjdsvksjvs</div>
    </body>
    
</html>
```





**font - face**

如果用户的电脑中没有该字体，可以使用font-face来获取字体

````html
<style>
    @font-face{
        指定字体的名称
        font-family:'text';
        指定获取字体的路径，要求字体必须是本地的
        src:url('路径');
    }
</style>
````







#### 图标字体

```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>网页标签</title>
        <link rel="stylesheet" href="font-awesome-4.7.0/css/font-awesome.min.css">
<!--        使用步骤：
               将css文件和fonts文件放入项目中
               使用link导入-->
        <style>
            .s1{
                color: red;
                font-size: 200px;
            }
        </style>
    </head>
    
    <body>
        <span class="fa fa-low-vision s1"></span>
        
    </body>
</html>
```



进入www.fontawesome.com.cn网页

```html
<!DOCTYPE html>
 <html lang="en">
 <head>
     <meta charset="UTF-8">
     <title>Document</title>
     <link rel="stylesheet" href="font-awesome-4.7.0/css/font-awesome.min.css">
     <style>
         *{
             margin: 0;
             padding: 0;
         }
         ul{
             width: 300px;
             height: 300px;
            margin: 100px auto;
            list-style: none;
         }
         
         ul li:before{
             content: '\f2bd';     将图标字体的编码输入，在编码前加上\
             font-family: 'FontAwesome';      输入图标字体的字体
         }
     </style>
 </head>
 <body>
     <ul>
         <li>nvusfdjsk</li>
         <li>nvusfdjsk</li>
         <li>nvusfdjsk</li>
         <li>nvusfdjsk</li>
     </ul>
     <span class="fa fa-snowflake-o" style="font-size: 50px">nsfdfasfknksd</span>
 </body>
 </html>
```



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <link rel="stylesheet" href="font_2099299_9q71zpbrk3/iconfont.css">
    <style>
        ul{
            list-style: none;
        }
        ul li:before{
            content: '\e6fe';
            font-family: 'iconfont';
        
            font-size: 30px;
/*        1.https://www.iconfont.cn
          2.登录
          3.选择想要的图标
          4.将图标添加到项目中
          5.下载到电脑中，导入项目中
          6.在文件中导入iconfont.css文件*/
            
        }
    </style>
</head>
<body>
<!--    通过实体-->
    <span class="iconfont" style="font-size: 60px">&#xe6fe;</span>
    <span class="iconfont" style="font-size: 60px">&#xe6f0;</span>
    
<!--    通过类-->
    <span class="iconfont icon-namecard-fill
" style="font-size: 60px"></span>

<!--通过伪类-->
<ul>
    <li>ziziziiz</li>
    <li>ziziziiz</li>
    <li>ziziziiz</li>
    <li>ziziziiz</li>
    
</ul>
</body>
</html>
```











#### em

**em也是css中的一个单位**

**1em=1font-size**

**rem也是css中的一个单位**

**1rem=html的font-size**



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        .box{
            font-size: 60px;
            width: 1em;
            height: 1em;
            background-color: red;
        }
        
        .box1{
            width: 1rem;
            height: 1rem;
            background-color: yellow;
        }
    </style>
</head>
<body>
    <div class="box">zzz</div>
    <div class="box1">dnvsdnsd</div>
</body>
</html>
```









#### line-hight

**设置文本框的行高**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
/*        文本在网页中显示时，css会为每一个文本设置一个文本框，以容纳这些文字
          宽度指定，高度由文字撑开*/
        div{
            border: 1px red solid;
            font-size: 50px;
            height: 200px;
/*            通过line-hight来设置行高*/
            
/*            行高可以是一个整数，则行高等于字体的倍数
              line-hight: 2;
            */
            line-height: 200px;
/*            在文本框中，文字并不是贴着行底部排列，而是沿着文本框的基线(base-                 hight)排列的
              文字基本上是居中的，将line-hight设置为何行高一样，文字就会居中*/
        }
    </style>
</head>
<body>
    <div>代表不是打不开</div>
</body>
</html>
```









#### font-weight

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        div{
            font-size: 30px;
/*            字重，字体是否加粗
              可以设置一个100~900之间的值
             font-weight: 900;
                */
             font-weight: bold;
           
        }
    </style>
</head>
<body>
    <div>文字是个好的</div>
</body>
</html>
```









#### font-style

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        div{
            font-size: 30px;
            font-weight: bold;
/*            font-style 设置字体的样式（斜体）
                    normal  正常
                    italic  斜体
            */
            font-style: italic;
        }
    </style>
</head>
<body>
    <div>文字是个好的</div>
</body>
</html>
```







#### font-variant

**字体变形**





#### font

**字体的简写属性**，**可以同时设置所有样式**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        div{
/*            后面必须是字体大小和字体族*/
           font:bold italic 40px '宋体';
        }
    </style>
</head>
<body>
    <div>文字是个好的</div>
</body>
</html>
```









#### text-align

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        div{
            
/*            text-align  用来设置文本的对齐方式
                    left          默认值，靠左对齐
                    right         靠右对齐
                    center        居中对齐
                    justify:      两端对齐;*/
            text-align: center
        }
    </style>
</head>
<body>
    <div>wonnv</div>
</body>
</html>
```





#### vertical-align

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        div{

            font-size: 50px;

        }
        span{
            font-size: 10px;
        /*vertical-align    垂直对齐方式
            baseline     延基线对齐
            top          和父元素的顶部对齐
            bottom:      和父元素的底部对齐
            */
            vertical-align: bottom;
        }
    </style>
</head>
<body>
    <div>我是一个<span>大沙</span></div>
</body>
</html>
```







#### text-indent

**首行缩进**

```html
text-indent:10px;   首行缩进10像素
```









#### white-space

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        p{
            width: 300px;
            background-color: red;
/*            white-space  如何处理空白内容
                normal    默认值，自动换行
                nowrap    不换行
                pre       保留文本格式;*/
            white-space: pre；
        }
    </style>
</head>
<body>
    <P>在这次活动中，我学到了很多，劳动人名的艰辛是我在学校中学不到的，在三十多摄氏度的高温下，仰着头采摘葡萄，是非常辛苦的，这让我更加认识到学习的重要性。
作为一名在校大学生，有着很多丰富的知识值得我去学习和体会，而这次活动，让我真正的从实践中学习到了知识，每次看到努力过后的成果，都是非常开心的，让我真正的认识到，只有努力才有成果，只有知识才能成功。。</P>
</body>
</html>
```







#### text-overflow

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        p{
            width: 300px;
            background-color: red;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
/*       text-overflow: ellipsis;
            将多出的内容以省略号的形式表达*/
        }
    </style>
</head>
<body>
    <P>在这次活动中，我学到了很多，劳动人名的艰辛是我在学校中学不到的，在三十多摄氏度的高温下，仰着头采摘葡萄，是非常辛苦的，这让我更加认识到学习的重要性。
作为一名在校大学生，有着很多丰富的知识值得我去学习和体会，而这次活动，让我真正的从实践中学习到了知识，每次看到努力过后的成果，都是非常开心的，让我真正的认识到，只有努力才有成果，只有知识才能成功。。</P>
</body>
</html>
```















### 背景background





#### background-clip

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        .box{
            width: 300px;
            height: 300px;
            background-color: red;
            border: 10px yellow double;
            padding: 10px;
            background-clip: content-box;
/*            backgrounp-clip  设置背景显示的区域
                可选值：
                        border-box  背景会延伸到边框下
                        padding-box   背景会延伸到内边距下
                        centent-box     背景只设置到内容区中*/
        }
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>
```











#### backgrounp-image

#### backgrounp-repeat

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        .box{
            width: 1000px;
            height: 1000px;
/*        background-image  设置背景图片
            背景颜色可以和背景图片同时设置
            这样背景颜色会作为图片的底色显示
            背景图片默认会在网页中水平垂直双方向重复
            */
            background-image: url(12.jpg);
/*           background-repeat  设置背景图片的重复方式
                   可选值：
                        repeat  默认值，双方向重复
                        repeat-x    水平方向重复
                        repeat-y    垂直方向重复
                        no-repeat   不重复*/
            background-repeat: repeat-x;
            background-color: red;
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>
```







#### background-size

````html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        .box{
         width: 500px;
         height: 500px;
/*            设置背景图片时
                 如果图片小于元素，则图片默认从元素左上角开始平铺
                 如果图片大于元素，则显示图片的左上角，不会全部显示
            */
         background-image: url(1.jpg);
/*         background-size  可以用来设置背景图片的尺寸
            需要两个参数：高度和宽度
                可选值：
                    contain：完整显示图片，可能有的位置没有图片
                    cover：使图片充满整个元素，可能会溢出
                */
        background-size:cover;
        }
         
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>
````









#### background-position

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        .box{
         width: 500px;
         height: 500px;
/*            设置背景图片时
                 如果图片小于元素，则图片默认从元素左上角开始平铺
                 如果图片大于元素，则显示图片的左上角，不会全部显示
            */
         background-image: url(1.jpg);
        background-size:100px;
        background-repeat: no-repeat;
        background-color: antiquewhite;
/*        background-position  用来设置背景图片的位置
              设置方法：
                    1.可以通过位置来设置
                        top   left  right  bottom  center
                    2.通过指定偏移量来设置背景图片的位置
                        第一个值为水平方向
                        第二个值为垂直方向
            background-position: right;
            */
            background-position: 200px 100px;
        }
        
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>
```











#### 雪碧图

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        a{
            display: block;
            width: 500px;
            height: 500px;
            
            background-image: url(2.jpg);
            background-size: cover;
            
        }
        
        a:hover{
            background-image: url(12.png);
            
            
        }
        a:active{
            background-image: url(1.jpg);
        }
    </style>
</head>
<body>
    <a href="#"></a>
</body>
</html>
```



```html
当按钮状态从link切换到hover时或hover切换到active时，第一次会发生闪烁
浏览器在加载页面时需要先加载当前页面，然后再加载页面中引入的外部资源
而外部资源不是立刻加载的，外部资源是需要被使用时才会加载，当我们从link切换到hover时，需要使用外部资源，从而加载
而加载和显示存在一个时间差，当加载时，link下的图片会消失，hover下的图片会显示，但是还有一个时间差，导致出现闪烁

解决问题：
	可以将多个按钮保存到一张图片上，这样我们可以一次性加载所有图片，然后通过偏移量来修改我们显示的图片即可。
	这个技术，我们成为css sprite（css精灵），这个图称为雪碧图

	优点：
		1.将多个图片保存在一张图片中，降低了发送请求的次数，增加了用户的访问速度
		2.将多个图片保存在一张图片中，也会降低图片的总大小，增快记载速度
```





**雪碧图**



![img](C:\Users\86188\Desktop\html3\2)



制作雪碧图的网站















#### background

**背景的简写属性**，**没有顺序要求**





















### 表格table

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
<!--    表格   (table)
            表格用来表示一些格式化的数据
            在网页中，使用table来创建数据
            -->
            <table border="1" align='center' width=300px 
             >
<!--                  在table中，使用tr来表示表格的一行，有几行用几个tr-->
                   <tr>
<!--                   在tr中使用td来表示一行的格数，有几格来几个td-->
                    <td>A1</td>
                    <td>A2</td>
                    <td>A3</td>
                    <td rowspan="2">A4</td>
                </tr>
                
                <tr>
                    <td>B1</td>
                    <td>B2</td>
                    <td>B3</td>
                    
                </tr>
                
                <tr>
<!--                   colspan  横向合并单元格
                       rowspan  纵向合并单元格-->
                    <td>C1</td>
                    <td>C2</td>
                    <td colspan="2">C3</td>
                    
                </tr>
            </table>
</body>
</html>
```





#### thead和tbody和tfoot

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <table width='50%' border="1" align='center'>
        <thead>
<!--           表示表格的头部-->
            <tr>
<!--               表示表格头行的单元格，即加粗居中-->
                <th>学号</th>
                <th>姓名</th>
                <th>性别</th>
                <th>住址</th>
            </tr>
        </thead>
        
        <tbody>
<!--           表示表格的主体-->
            <tr>
                <td>1</td>
                <td>孙悟空</td>
                <td>男</td>
                <td>花果山</td>
            </tr>
        </tbody>
        
        <tfoot>
<!--           表示表格的底部-->
            <tr>
                <td>2</td>
                <td>猪八戒</td>
                <td>男</td>
                <td>高老庄</td>
            </tr>
        </tfoot>
    </table>
</body>
</html>
```







#### border-spacing

设置边框之间的距离







#### border-collapse

合并边框

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        table{
            width: 50%;
            align-content: center;
            margin: 0 auto;
            border: solid 1px ;
/*            border-spacing: 0px;*/
            border-collapse: collapse;

        }
        td{
            border: 1px solid;
        }
      
    </style>
</head>
<body>
    <table>
        <thead>
<!--           表示表格的头部-->
            <tr>
<!--               表示表格头行的单元格，即加粗居中-->
                <td>学号</td>
                <td>姓名</td>
                <td>性别</td>
                <td>住址</td>
            </tr>
        </thead>
        
        <tbody>
<!--           表示表格的主体-->
            <tr>
                <td>1</td>
                <td>孙悟空</td>
                <td>男</td>
                <td>花果山</td>
            </tr>
        </tbody>
        
        <tfoot>
<!--           表示表格的底部-->
            <tr>
                <td>2</td>
                <td>猪八戒</td>
                <td>男</td>
                <td>高老庄</td>
            </tr>
        </tfoot>
    </table>
</body>
</html>
```















### 表单form

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
<!--    表单（form）
            表单用来将信息提交给别人
            网页中的表单用来将信息提交给服务器
            
            使用form标签来创建表单
                cation  是表单提交的目标的地址-->

    <form action="4.html">
<!--        表单中需要添加一个一个的表单项-->
<!--        文本框  input标签   type的值是text，表示一个文本框
              如果希望服务器正常收到表单的数据，必须为表单设置一个name属性
              -->
       <input type="text" name="username">
       <br>
       
<!--       密码框  input标签  type的值是password  表示一个密码框
              如果希望服务器正常收到表单的数据，必须为表单设置一个name属性-->
       <input type="password" name="password">
       
       
<!--       提交按钮   input标签   type的值是submit  表示一个按钮
                通过value属性可以指定按钮的文字内容，默认为提交-->
       <input type="submit" value="注册">
    </form>
</body>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        form{
            width: 300px;
            height: 200px;
            margin: 100px auto;
        }
    </style>
</head>
<body>

    <form action="4.html">
        用户名<input type="text" name="user">
        <br>
        密码

        <input type="password" name="password">
        <br>
<!--        表单中的数据默认情况下会以查询字符串(query string)的形式发送给服务器
            user=赖建东&password=123
            查询字符串就是一个一个的名值对结构，名字就是表单项的name属性值
            值是用户填写的内容，名和值使用=连接，多个名值对之间使用&隔开
-->

<!--        单选按钮，单选按钮是input，type是radio
                单选按钮是通过name属性来分组的，相同name属性的单选按钮只有一个能被选中
                像这种选择框，它不需要用户填写，只是选择即可，这种表单项，必须知道value属性
                最终提交到服务器就是他们的value属性

                可以在单选按钮中添加checked属性来使其变成默认选中状态-->
        性别
        <input type="radio" name="性别" value="男" checked>男
        <input type="radio" name="性别" value="女">女
        <br>

<!--        多选框，多选框也是input，type属性是checkbox-->
        爱好
        <input type="checkbox" name="爱好" value="篮球">篮球
        <input type="checkbox" name="爱好" value="足球">足球
        <input type="checkbox" name="爱好" value="乒乓球">乒乓球
        <br>
<!--        下拉列表
                - 使用select来创建一个下拉列表
                - 在select中使用option来设置选项
                - 在select标签中添加一个multiple属性可以将下拉列表设置为多选下拉列表
                - optgroup  分组   label属性  分组名，无法选中
                - 在option中添加selected属性将当前选项选中为默认选项
-->
        你喜欢的明星
        <select name="喜欢的明星" multiple>
            <option value="李连杰">李连杰</option>
            <option value="成龙">成龙</option>
            <option value="李小龙">李小龙</option>
        </select>
        <br>
        喜欢的动物
        <select name="喜欢的动物">
            <optgroup label="植物">
                <option value="向日葵">向日葵</option>
                <option value="松树">松树</option>
                <option value="夜来香">夜来香</option>
            </optgroup>
            <optgroup label="动物">
                <option value="狗" selected>狗</option>
                <option value="猫">猫</option>
                <option value="鸭子">鸭子</option>
            </optgroup>
        </select>
        <br>
        <input type="submit" value="登录">
<!--     reset  重置按钮  将表单恢复到初始化  -->
        <input type="reset" value="重置">
<!--        button  创建一个按钮，一个单纯的按钮，只能被点-->
        <input type="button" value="按钮">
        <br><br>
<!--        功能和input一样，但是比较灵活-->
        <button type="submit">登录</button>
        <button type="reset">重置</button>
        <button type="button">按钮</button>
    </form>
</body>
</html>
```





````html
属性：
	autofocus	自动获取焦点，当进入页面时，光标在获取焦点的表单中
	requirea	表单项为必填表单项，如果不填，会有提示，并且无法确定
	value		可以用于指定输入框的默认值
	readonly	将属性设置为只读属性
	disabled 	使表单不可用
	autocomplete="off"     自动填写关闭
	autocomplete="on" 	   自动填写开启，默认开启
````













### 过渡transition

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .box1{
            /*过渡：可以使一个属性的值经过一段时间变成另一个值*/
            width: 200px;
            height: 200px;
            background-color: red;
            position: absolute;
            left: 0;
            /*
                过渡相关的属性：
                    transition-property
                        指定过渡的属性， 比如height，width,可以指定多个值，用逗号隔开
                        all     表示所有属性都会进行过渡
                    transition-duration
                         过渡持续的时间
                            单位
                                  s   秒
                                  ms  毫秒
                    transition-delay
                        过渡的延迟
                    transition-timing-function
                        过渡的时间函数
                            ease        起步慢，然后加速，然后减速停止
                            linear      匀速运动
                            ease-in     加速运动
                            ease-out    减速运动
                            ease-in-out 先加速后减速


            */
            /*transition-property: height,width,background-color;*/
            /*transition-duration: 2s,1s,1s;*/
            /*transition-delay: 1s;*/
            transition-property: left;
            transition-duration: 3s;
            transition-timing-function: ease-in;

        }
        .box1:hover{
            /*width: 400px;*/
            /*height: 400px;*/
            /*background-color: yellow;*/
            left: 800px;

        }
    </style>
</head>
<body>
    <div class="box1">

    </div>
</body>
</html>
```



```html
transition-property       指定过渡的属性
transition-duration		  指定过渡的持续时间
transition-delay		  指定过渡的延迟时间
transition-timing-function		指定过渡的时间函数，比如先快后慢
```



使用过渡来制作动画

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .box1{
            height: 100px;
            width: calc(2400px/12);
            background-image: url("dongman.png");
            margin: 100px auto;
            background-position: 2400px 0;
            transition: background-position 2s steps(11,end);
            /*transition-property: background-position;*/
            /*transition-duration: 2s;*/
            /*transition-timing-function: steps(11,end);*/
        }
        .box1:hover{
            background-position: 200px 0;
        }
    </style>
</head>
<body>
    <div class="box1">

    </div>
</body>
</html>
```





#### 时间函数(贝塞尔曲线)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .box{
            height: 200px;
            width: 100%;
            border-bottom: 4px solid black;
            background-color: #baf;
            position: absolute;
        }
        .box1{
            width: 100px;
            height: 100px;
            background-color: yellow;
            position: absolute;
            left: 0;
            bottom: 0;
            border-radius: 50%;
            /*cubic-bezier(p1,p2,p3,p4)
                    可以通过贝塞尔曲线来指定元素的运动方式
                    可以搜索网址(https://cubic-bezier.com/#.24,.59,0,-0.77)来设置运动方式*/
            transition: left 2s cubic-bezier(.24,.59,0,-0.77);
        }

        .box:hover .box1{
            left: 600px;
        }
    </style>
</head>
<body>
    <div class="box">
        <div class="box1">

        </div>
    </div>
</body>
</html>
```























### 动画animation



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .box {
            height: 100px;
            width: 200px;
            background-image: url("dongman.png");
            background-position: 2400px 0;
        /*    需要在执行动画的元素上，设置动画细节*/
        /*    animation-name    指定动画的名字*/
            animation-name: text;

            /*animation-duration    指定动画的执行时间*/
            animation-duration: 1s;

            /*animation-delay   指定动画的延迟时间*/
            animation-delay: 1s;

            /*animation-timing-function    指定动画的时间样式*/
            animation-timing-function: steps(11,end);

            /*animation-iteration-count     指定动画的执行次数
                        infinite    无限执行*/
            animation-iteration-count: infinite;
            
            /*    animation-play-state      动画的播放状态
                    可选值：
                            paused      动画暂停
                            running     动画运行（默认值）*/
            animation-play-state: running;

        /*    animation-direction       动画的运行方向
                    可选值：
                            normal      默认值，动画从0% - 100%
                            reverse     反转执行    100% - 0%
                            alternate   先从0% - 100%,再从100% - 0%   交替
                            alternate-reverse   先从100% - 0%，再从0% - 100%*/
            animation-direction: reverse;
        }
        /*     动画
                    -通过动画可以实现一些更加复杂的交互效果
                    -要实现css动画，必须要设置关键帧
                    @keyframes 用来设置关键帧
                    语法：
                        @keyframes  名字{
                        }

         */
            @keyframes text{
                /*指定动画的开始位置*/
                from{
                    background-position: 2400px 0;
                }
                /*指定动画的结束位置*/
                to{
                    background-position: 200px 0;
            }
        }
    </style>
</head>
<body>
    <div class="box">

    </div>
</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }

        .box{
            height: 500px;
            border-bottom: 2px solid black;
            position: relative;
        }

        .box1{
            width: 100px;
            height: 100px;
            border: 2px solid red;
            position: absolute;
            border-radius: 50%;
            bottom: 0;
            left: 0;
            right: 0;
            margin: 0 auto;
            animation: text 3s infinite;
        }

        @keyframes text {
            0%,100%{
                top:0;
            }

            25%{
                top:396px;
            }

            50%{
                top:300px;
            }

            75%{
                top: 100px;
            }


        }
    </style>
</head>
<body>
    <div class="box">
        <div class="box1">

        </div>
    </div>
</body>
</html>
```













### 变形transform



#### 平移和旋转

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        html{
            /*perspective   视距 ，设置人的眼睛和网页之间的距离*/
            perspective: 800px;
        }
        .box{
            width: 200px;
            height: 200px;
            background-color: #bfa;
            margin: 100px auto;
        /*
            transform
                通过变形可以对元素进行平移，旋转，放大，缩小等操作
                    平移
                        translateX()    沿s轴平移
                        translateY()    沿y轴平移
                        translateZ()    沿z轴平移,如果需要它生效，必须设置perspective

                    旋转
                        rotateX()   沿s轴旋转
                        rotateY()   沿y轴旋转
                        rotateZ()   沿z轴旋转
                            deg     度，单位
        */
            transition:1s;

        }

        .box:hover{
            /*transform:translateZ(-100px);*/
            transform:rotateX(30deg);
        }
    </style>
</head>
<body>
    <div class="box">

    </div>
</body>
</html>
```



```html

                通过变形可以对元素进行平移，旋转，放大，缩小等操作
                    平移
               		    translateX()    沿s轴平移
                        translateY()    沿y轴平移
                        translateZ()    沿z轴平移,如果需要它生效，必须设置perspective

                    旋转
                        rotateX()   沿s轴旋转	也就是沿着指定元素水平中心的线翻转
                        rotateY()   沿y轴旋转	沿着指定元素垂直中心的线翻转
                        rotateZ()   沿z轴旋转	沿着中心点旋转
                            deg     度，单位

transform-origin		指定变形的原点
	transform-origin:50px 50px;		以该元素的宽50px，高50px的位置进行变形
	transform-origin：left top;

perspective   视距 ，设置人的眼睛和网页之间的距离，一般设置为800px ~ 1200px
```





```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        html{
            perspective:800px;
        }
        .box1{
            width: 200px;
            height: 200px;
            /*background-color: #bfa;*/
            margin: 100px auto;
            position: relative;
            transition: all 2s;
            /*设置变形时的效果*/
            transform-style: preserve-3d;
            animation: text 20s linear infinite;
        }
        .box1>div {
            position: absolute;
            width: 200px;
            height: 200px;
            line-height: 200px;
            text-align: center;
            font-size: 100px;
            opacity: 0.5;
            transition: all 2s;

        }
       @keyframes text {
           0%,50%,100%{
               transform: rotateX(-90deg) rotateY(360deg) rotateZ(360deg);
           }
           25%,75%{
               transform: rotateY(180deg) rotateX(180deg) rotateZ(-360deg);
           }
       }
        .box1>div:nth-child(1){
            background-color: yellow;
            transform: rotateY(90deg) translateZ(100px);
        }
        .box1>div:nth-child(2){
            background-color: orange;
            transform: rotateY(-90deg) translateZ(100px);
        }
        .box1>div:nth-child(3){
            background-color:#3eb18b;
            transform: rotateX(-90deg) translateZ(100px);
        }
        .box1>div:nth-child(4){
            background-color:#3ebafb;
            transform: rotateX(-90deg) translateZ(-100px);
        }
        .box1>div:nth-child(5){
            background-color:#3ebaaa;
            transform: translateZ(-100px);
        }
        .box1>div:nth-child(6){
            background-color:#fa54af;
            transform: translateZ(100px);
        }
    </style>
</head>
<body>
    <div class="box1">
        <div>1</div>
        <div>2</div>
        <div>3</div>
        <div>4</div>
        <div>5</div>
        <div>6</div>
    </div>
</body>
</html>
```



​                                              

#### 放大

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        div{
            width: 400px;
            height: 258px;
            border:2px solid black;
            margin: 100px auto;
            overflow: hidden;
        }

        img{
            transition:500ms all;
        }
        img:hover{
            /*
                scaleX()    水平方向缩放
                scaleY()    垂直方向缩放
                scale()     双方向缩放
                scaleZ()    用于3d
            */
            transform: scale(1.3);
        }
    </style>
</head>
<body>
    <div>
        <img src="tx.jpg" alt="">
    </div>
</body>
</html>
```







#### 倾斜

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        div{
            width: 400px;
            height: 258px;
            margin: 100px auto;
        }

        img{
            transition:500ms all;
        }
        img:hover{
            transform: skewX(45deg );	元素左右两边沿x轴倾斜
            transform: skewY(45deg );	元素左右两边沿y轴倾斜
        }
    </style>
</head>
<body>
    <div>
        <img src="tx.jpg">
    </div>
</body>
</html>
```







### 渐变





#### 线性渐变

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .box{
            width: 200px;
            height: 200px;
            margin: 100px auto;
        /*
            渐变背景不是背景颜色，而是图片
                所以我们需要通过background-image或background来设置渐变的效果
                linear-gradient()   线性渐变
                radial-gradient()   径向渐变
        */
            /*background-image: linear-gradient(55deg,red,yellow,blue,black);*/
        /*    线性渐变默认是自上向下进行渐变的
                   可以通过关键字来指定渐变的方向：
                        to top      自下向上渐变
                        to right    自左向右渐变
                        to left     自右向左渐变
                        to bottom   自上向下渐变
                        to left top
                        ......
                    还可以通过度数来设置渐变的方向

               默认情况下，渐变的颜色在元素中是平均分配的，我们可以自定义,
               在颜色后，指定颜色的范围，开始范围，结束范围，但是支持度不高

               颜色后边可以指定一个长度，指的是颜色的开始位置
        */
            /*background-image: linear-gradient(red 10px 110px,yellow);*/
            /*repeating-linear-gradient()   重复渐变*/
            background-image: repeating-linear-gradient(red 25px,yellow 50px);
        }
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>
```







#### 径向渐变

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .box{
            width: 300px;
            height: 300px;
            margin: 100px auto;
            /*
                radial-gradient()   径向渐变
                    也就是从指定元素中心向四周进行渐变
                    渐变的形状会根据元素的形状来自定义
                    也可以自己指定
                            circle      圆形
                            ellipse     椭圆形
                    也可以通过在颜色前设置宽度和高度来指定渐变的形状(直径)

                    可以通过at来指定渐变中心的位置
                            可以设置px，也可以设置center，left等等

                            closest-side    表示渐变效果显示离圆心最近的边上
                            farthest-side   表示渐变效果显示离圆心最远的边上

                            closest-corner   渐变效果显示离圆心最近的角上
                            farthest-corner

                     也可以设置重复
            */
            background-image: radial-gradient(ellipse,red,yellow,blue,seashell);
            background-image: radial-gradient(100px 100px,red,yellow,blue,seashell);
            background-image: radial-gradient(at 10px 10px,red,yellow,blue);
            background-image: radial-gradient(closest-corner at 100px 20px,red,yellow,blue);
            background-image: radial-gradient(red 10%,yellow 30%,blue 70%);
            background-image: repeating-radial-gradient(red 20px,yellow 50px,blue 20px);
        }
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>
```









### 弹性盒

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        ul{
            /*width: 500px;*/
            height: 500px;
            border: 2px red solid;
            list-style: none;
            display: flex;
            /*    设置弹性盒*/
            /*
                弹性容器
                    - 弹性元素就是弹性容器，要使用弹性盒，必须先将元素设置为弹性容器
                            设置弹性容器的两种方式：
                                display:flex;           块级弹性容器
                                display:inline-flex;    行内弹性容器
                弹性元素
                    - 弹性容器中的子元素(只能是子元素)称为弹性元素
            */

            /*
                弹性元素的属性：
                    flex-direction
                        作用：用来设置弹性容器的主轴的方向
                        可选值：
                                row             主轴是横向的(自左向右)
                                row-reverse     主轴是横向的(自右向左)
                                column          主轴是纵向的(自上向下)
                                column-reverse  主轴是纵向的(自下向上)

            */
            flex-direction: row;
            /*
                flex-wrap
                    作用：弹性元素在主轴上是否换行
                    可选值：
                            nowrap          不换行
                            wrap            自动换行
            */
            flex-wrap: wrap;

            /*
                flex-flow
                    作用：它是一个简写属性，可以同时设置 flex-direction 和 flex-wrap
            */
            flex-flow: row wrap;

            /*
                justify-content
                    作用：设置元素在主轴上的对齐方式
                    可选值：
                                flex-start          主轴的起边
                                flex-end            主轴的终边
                                center              主轴的中间
                                space-between       将空白区域分配到元素之间
                                space-around        将空白区域设置到元素的前后
                                space-evenly        将空白区域设置到元素的一侧
                                stretch             拉伸元素使其充满盒子

            */
            justify-content: flex-start;

        /*
            垂轴，辅轴，侧轴的对齐方式
                可选值：
                            flex-start          侧轴的起边
                            flex-end            侧轴的终边
                            center              侧轴的中间

        */
            align-items: flex-start;
        }
        li{
            width: 260px;
            height: 200px;
            flex-shrink: 0;
        }
        li:nth-child(1)
        {
            background-color: #0077aa;
        }
        li:nth-child(2)
        {
            background-color: #5f5750;
        }
        li:nth-child(3)
        {
            background-color: #55a532;
        }
        li:nth-child(4)
        {
            background-color: #3eb18b;
        }
        li:nth-child(5)
        {
            background-color: #3ebaaa;
        }
        li:nth-child(6)
        {
            background-color: yellow;
        }
    </style>
</head>
<body>
<!--
    弹性盒是css3中新增的一种布局方式，通过弹性盒可以使一个盒子自动适应其容器的大小
        通过弹性盒可以创造出非常非常灵活的布局
-->
<ul>
    <li>1</li>
    <li>2</li>
    <li>3</li>
    <li>4</li>
    <li>5</li>
    <li>6</li>
</ul>
</body>
</html>
```



```html
设置弹性容器的两种方式：
                   display:flex;           块级弹性容器
                   display:inline-flex;    行内弹性容器

```







#### flex-direction

```
flex-direction
                        作用：用来设置弹性容器的主轴的方向
                        可选值：
                                row             主轴是横向的(自左向右)
                                row-reverse     主轴是横向的(自右向左)
                                column          主轴是纵向的(自上向下)
                                column-reverse  主轴是纵向的(自下向上)
```





####  flex-wrap

```
 flex-wrap
                    作用：弹性元素在主轴上是否换行
                    可选值：
                            nowrap          不换行
                            wrap            自动换行
```





#### flex-flow

```

 flex-flow
     作用：它是一个简写属性，可以同时设置 flex-direction 和 flex-wrap
            
```





#### justify-content

```
 justify-content
                    作用：设置元素在主轴上的对齐方式
                    可选值：
                                flex-start          主轴的起边
                                flex-end            主轴的终边
                                center              主轴的中间
                                space-between       将空白区域分配到元素之间
                                space-around        将空白区域设置到元素的前后
                                space-evenly        将空白区域设置到元素的一侧
                                stretch             拉伸元素使其充满盒子

```





####  align-items

```
 align-items
 	作用：设置垂轴的对齐方式
 	可选值：
                flex-start          侧轴的起边
                flex-end            侧轴的终边
                center              侧轴的中间
                stretch             拉伸元素使其充满盒子
```





#### align-self

```
align-self
	作用：用于设置弹性元素自身在辅轴上的对齐方式
			用于覆盖元素上的align-items属性
```





#### align-content

```HTML
  align-content
                    作用：用来设置垂轴空白区域的分布
                    可选值：
                                flex-start          元素沿着垂轴的起边对齐
                                flex-end
                                。。。。
```



#### order

```
作用：用于设置弹性元素的排列顺序
```





```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        *{
            padding: 0;
            margin: 0;
        }
        ul{
            width: 600px;
            margin: 0 auto;
            border: 4px solid red;
            display: flex;
            list-style: none;
            flex-flow: row nowrap;
            /*justify-content: stretch;*/

        }
        li{

            width: 200px;
            height: 100px;
            line-height: 100px;
            text-align: center;
            color: #fff;
            font-size: 40px;
            /*flex-grow: 1;*/
        /*
                flex-basis
                    作用：指定弹性元素的标准大小
                            一但元素设置了这个样式，那么元素的width会自动失效
                            默认值是auto
        */

        /*
            flex    简写属性    可以同时设置这三个值：
                flex：flex-grow  flex-shrink  flex-basis
        */
            /*flex:1 0 100px;*/

        }
        li:nth-child(1)
        {
            background-color: #0077aa;
            /*
                当父元素中有空白空间时，需要使用增长系数，来分配每一个元素的增长的大小(按比例)
                flex-grow
                    作用：用来指定元素的增长的系数
            */
            /*flex-grow: 1;*/

        /*
                当元素的总长度超过父元素时，需要使用缩短系数，来分配每一个元素的缩减的大小
                flex-shrink

                每一个元素缩减多少，由元素的flex-basis 和 flex-shrink 共同决定的
                    溢出的大小(200)
                    ----------------------------
                    第一个元素 flex-basis * flex-shrink + 第二个元素 flex-basis * flex-shrink + 。。。。
                                200                                     200
                                            200px / 400px = 0.5
                    所以；
                            第一个元素缩减 = flex-shrink * 0.5 * flex-basis
                            第二个元素缩减 = flex-shrink * 0.5 * flex-basis
        */
        }
        li:nth-child(2)
        {
            background-color: #5f5750;
        }
        li:nth-child(3)
        {
            background-color: #55a532;
        }
        li:nth-child(4)
        {
            background-color: #3eb18b;
        }
        li:nth-child(5)
        {
            background-color: #3ebaaa;
        }
        li:nth-child(6)
        {
            background-color: yellow;
        }

    </style>
</head>
<body>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
        <li>5</li>
        <li>6</li>
    </ul>
</body>
</html>
```









#### flex-basis

```
 flex-basis
                    作用：指定弹性元素的标准大小
                            一但元素设置了这个样式，那么元素的width会自动失效
                            默认值是auto
```







####  flex-grow

```
 flex-grow
                    作用：用来指定元素的增长的系数
                    当父元素中有空白空间时，需要使用增长系数，来分配每一个元素的增长的大小(按比例)
```







####  flex-shrink

```
当元素的总长度超过父元素时，需要使用缩短系数，来分配每一个元素的缩减的大小
                flex-shrink

                每一个元素缩减多少，由元素的flex-basis 和 flex-shrink 共同决定的
                    溢出的大小(200)
                    ----------------------------
                    第一个元素 flex-basis * flex-shrink + 第二个元素 flex-basis * flex-shrink + 。。。。
                                200                                     200
                                            200px / 400px = 0.5
                    所以；
                            第一个元素缩减 = flex-shrink * 0.5 * flex-basis
                            第二个元素缩减 = flex-shrink * 0.5 * flex-basis
```





#### flex 

```
flex    简写属性    可以同时设置这三个值：
                flex：flex-grow  flex-shrink  flex-basis
```





### 视口

```
css像素和物理像素
	在pc端中，一般情况下，1个css像素等于1个物理像素
	但在移动端中，因为移动端的手机屏幕小，但像素多，所以像素要小，所以一个1css像素等于一个物理像素，才可以确保网页可以正常浏览
```





浏览器中用于呈现网页的区域叫视口(viewport)，视口通常不等于屏幕大小

​	手机一般的默认视口都是980，所以移动端默认视口在浏览网页时体验效果非常差

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
<!--    指定视口的大小-->
<!--    <meta name="viewport" content="width=375px">-->
<!--
        输入meta:vp   按tab键
        width=device-width      将视口大小设置为完美视口
        initial-scale=1.0       初始化缩放设置为不缩放
        maximum-scale=1.0       缩放设置为不缩放，表示页面无法放大和缩小
        user-scalable=0         表示没有用户可以设置缩放
-->
    <meta name="viewport" content="width=device-width, initial-scale=1.0,maximum-scale=1.0,user-scalable=0">
    <style>
        *{
            padding: 0;
            margin: 0;
        }
        div{
            width: 100px;
            height: 100px;
            background-color: red;
        }
    </style>
</head>
<body>
    <div></div>
</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        *{
            padding: 0;
            margin: 0;
        }
        html{
            font-size: 3.9999999999vw;
        }
        div{
            /*
                1vw     1vw = 1%的视口宽度
                在移动端可以放心使用
                但是在pc端还是不要使用
                % 参考包含块来计算的
                vw  总是相对于视口计算

                750像素宽的设计图
                使用vw 表示 其中 60像素
                首先用100vw / 750px ，得出1px 等于 0.133333333vw
                如果我们设置一个宽60px的div
                先设置html 的 font-size
                1 rem == 1 html的font-size
                将font-size的大小设置为 5.33333vw，也就是大概40px
            */
            width: 2rem;
            height: 100px;
            background-color: red;
        }
    </style>
</head>
<body>
    <div></div>
</body>
</html>
```











### 在模拟器上查看页面



点击File ---->  setting  ----->   debugger

![image-20201015205410705](C:\Users\86188\AppData\Roaming\Typora\typora-user-images\image-20201015205410705.png)



将localhost换成IP地址

![image-20201015205433515](C:\Users\86188\AppData\Roaming\Typora\typora-user-images\image-20201015205433515.png)



![image-20201015205507639](C:\Users\86188\AppData\Roaming\Typora\typora-user-images\image-20201015205507639.png)



最后在模拟器的浏览器中输入链接







#### 响应式

​				响应式的布局它随着浏览器窗口的改变而改变





#### 媒体查询

```
媒体查询语法：
	@media	查询条件
	{
	
	}
```



```
媒体类型：
	all		适用于所有设备
	print	适用于打印设备
	screen	适用于以屏幕显示的设备
	speech	适用于阅读器
```



```
only
	一般媒体查询都会以only screen开头
	screen 表示仅仅对显示屏应用该样式
	only 主要用于解决兼容性的问题
	 @media only screen {
            body{
                background-color: #bfa;
            }
        }
```



```
媒体功能：
	width，min-width，max-width		视口宽度
	height，min-height，max-height	视口高度
	....
```



```
and		条件必须都成立
or		
not	
```



```
段点

```









## LESS



### windows命名行

**常用命令**

```
dir			显示当前目录下的所有文件和文件夹，如果是文件，文件名前面会显示大小

cd			切换路径

mkdir		创建文件夹

rmkdir		删除文件夹

```



**文件(程序)的搜索流程**

​				当我们在命令行中访问一个文件(或程序)时

​				先在当前文件夹中寻找，再到PATH环境变量中寻找，如果两个都没有，就报错





**环境变量**

PATH环境变量中存储的是一组路径，当我们在当前目录找不到文件时，会依次去到PATH的路径中寻找













### 配置less

```
1.安装nodejs

2.NPM是node的包服务器，通过NPM可以下载js所编写的工具，从而在计算机中使用这些工具
	由于NPM的服务器在国外，所以访问的速度慢，所以我们可以配置镜像
	配置镜像    npm install -g cnpm --registry=https://registry.npm.taobao.org
	使用npm下载工具是在国外下
	使用cnpm下载工具是在国内下
	
3.安装less	
	cnpm install -g less
```









### less的简介

```
less是一门css预处理语言(也就是用less的格式来写样式，然后转换为css)，他扩展了css语言，增加了变量，mixin，函数等特性，使css更容易维护
	转换：打开命令行，使用lessc来转换
			格式：lessc 转换的文件名 转换后的文件名
```







```less
/*
  这是原版css的注释，它里边的内容会被编译到css文件中
*/

//这是less的单行注释，注释的内容不会编译到css文件中

//在webstrom中，每次对less进行编译后，都会自动生成一个xxx.css.map文件
//该文件的作用是，将css文件和less文件进行管理，使我们可以直接对less文件进行调试

```













### less的引入

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
<!--    两种方式
			1.引入css文件，在服务器上编译
			2.引入less文件，在网页中编译
<!--    <link rel="stylesheet" href="css/style.min.css">-->
<!--    在网页中，来对less进行编译-->
    <link rel="stylesheet/less" href="css/style.less">
<!--    引入less.js-->
<!--    使用script标签来引入一个外部的js文件-->
    <script src="css/less.js"></script>
</head>
<body>

</body>
</html>
```





















### less的应用



#### darken

```less
body{
  //darken() 函数，用于加深颜色
  //参数：
  //      第一个参数为指定颜色
  //      第二个参数为加深颜色的百分比
  background-color:darken(yellow,10%);
}
```







#### 加减乘除$

```less
 //使用值时，可以使用加减乘除来计算
  width: 300+500px;
  width: 300*2px;
  width:1600px/40px;
//  $样式名  可以直接引用其他属性的值
  height:$width /2;
```







#### @

```less
//使用 @ 符号来定义变量
@a:10px;        // 全局变量
@className:box2;
// 可以将变量的值作为选择器使用
// 使用格式：
.@{className}{
  width: @a;
  background-image: url("@{className}/img/1.png");
}

.box1{
  @a:40px;     //  局部变量
//  使用变量，依据就近原则
  border-width: @a;

}

@w:400px;
.box3{
    @a:w;
    width:@@a;  //  @@a==@(@a)==@(w)==@w=400px
}


```







#### less中的变量

```
1.作为普通的属性值来使用		@pink
2.作为选择器和属性名来使用			选择器(#@{pink},.@{pink})			属性名(@{pink})
3.作为URL：@url
```







#### 变量的延迟加载

```
先找自身元素，如果自身元素有两个或多个相同的变量，默认找最后一个
如果自身没有，就找父元素，如果有多个，找最后一个
@var:0;
.warp{
  @var:1;
  .box{
    @var:2;
    width: @var;    4
    @var:4;
  }
  width: @var;     1
}
```







#### mixins

```less
// 定义mixins时，如果名字后面加上了括号，则该样式不会被编译到css文件中
//  定义时，如果在()中指定参数，这个参数就相当于变量，但是没有赋值，需要在调用mixins时赋值

.box1(@a,@b){
  width: @a;
  height: @b;
  background-color: red;
}

.box2{
  .box1(20px,200px);
}

//如果在调用时传值，则border的宽度为指定值，如果不传，则为默认值1px
.bord(@a:1px){
  border: @a solid #fa54af;
}

.h1{
  .bord(@a:12px)
}
```





























































## JavaScript



### 简介

```
javascript
	是一门动态的，弱类型，解释性的脚本语言
		动态：只有在执行的时候，才能确定数据类型
		弱类型：变量数据的类型不是确定的，可以随意的进行改变
		解释性：不需要编译，执行的时候，一行一行去解释执行
		脚本：可以嵌在其他的语言当中去执行
```







### 作用

```
js的作用
	可以能干啥
		负责表单验证(仅仅负责表单验证)
		如果没有js，那么我们网页的表单验证需要通过网络传输数据去服务器进行验证，占用带宽资源，并且用户体验极差
	现在能干啥
		1.表单验证
		2.用户交互
		3.游戏
		4.后端开发
```









### 组成部分

```
ECMAscript		负责js的语法部分
DOM				document object model    文档对象模型(操作元素)
BOM				browser object model	 浏览器对象模型(操作浏览器)
```





### 最基础的函数

```
alert('指定输出的内容')			以弹出框的形式输出内容
console.log('指定输出的内容')		以日志的形式在控制台输出内容
document.write('指定输出的内容')	在页面中输出内容
```









### 书写位置

```
1.内嵌式
<script>
    alert('i love you');
    console.log('i love you');
    document.write('i love you');
</script>
优缺点：用的比较多，一般写项目初期都用内嵌，最后变为外嵌

2.外链式
<script src="js/love.js"></script>
优缺点：script标签里面不能写样式

3.行内式
<div onclick="alert('i love you two')"></div>	
优缺点：局限性比较大，只能对事件进行书写js，问题也恒大，做不到结构和行为分离
```









### 变量

```
定义变量
var a;
```











### 数据类型

```
数据类型分为：
	1.基本数据类型
		number		数字
		string		字符串
		boolean		布尔，值为True和false
		undefined	定义的变量没有赋值
		null		定义的变量赋值为null(一般是对对象进行初始化或者删除一个对象的时候用到)
	2.对象数据类型
```



```
变量的约定成俗
	var sum=0;			 初始化，代表以后存储的是一个数字
	var carName='';		 代表以后存储的是一个字符串
	var isClose=true；	代表以后存储的是一个布尔值
	var dog=null；		代表这个dog变量以后存储的是一个狗的对象
```



**typeof**

```
作用：查看变量的类型
```







### 运算符和表达式



```
算术运算符
	+		加
	-		减
	*		乘
	/		除
	%		余
	++		自增
	--		自减
```



```
赋值运算符
	=
	+=
	-=
	*=
	/=
```



```
比较
	>
	<
	==
	>=
	<=
	!=
	===		全等于
	!==		全不等于
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var a=5;
    var b=6;
    var c='5';
    console.log(a == c);
//    如果数字和数字型字符串比较，数字型字符串会隐式转换为数字，进行比较
//    == 判断数值是否一致
    console.log(a === c);
//    === 先判断类型是否一致，再判断数值是否一致
</script>
</body>
</html>
```



```
逻辑运算符
	&&		且
	||		或
	！	    非
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var a=20;
    a=0 && 9;
    //先判断&&之前是否是真，如果是真，那么就取后面的值，如果前面的值是假，就取前面的值
    var b=0 || 1;
    //如果||前面的值是真，就返回前面的值，如果是假，就返回后面的值
    console.log(a);
    console.log(b);
</script>
</body>
</html>
```





```
三目运算符
	?:
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var a = 6;
    var b = a > 0 ? 10 : 100;
    //如果 a 大于 0，就将10赋给b，如果 a 不大于 0，就将100赋给b
    console.log(b);
</script>
</body>
</html>
```









### 数据类型转换



数据类型强制转换

```
Number()		强制将一个其他类型的数据转换为数字类型，转不了就是NaN

String()		强制将一个其他类型的数据转换为字符串类型
	不管给啥都能转换为字符型
	
Boolean()		强制将一个其他类型的数据转换为布尔类型
	转换数字时，除了0，其他都是true
	转换字符串时，除了空字符串，其他都是true
	转换undefined和null都是false
```





数据类型手动转换

```
parseInt()		从字符串中提取整数
parseFloat()	从字符串中提取浮点数
```







### 条件语句

```
for
switch....case
while
if....else if 
do....while
```















### 数组



#### length

```
查看数组的大小
```







#### 增删改查

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="{CHARSET}">
		<title></title>
	</head>
	<body>
		<script type="text/javascript">
			//在数组前面添加数字
//			var arr=[1,2,3,4,5];
//			for(var i=arr.length-1;i>=0;i--){
//				arr[i+1]=arr[i];
//			}
//			arr[0]=6;
//			console.log(arr);


			//在数组后面添加数组
//			var arr=[1,2,3,4,5];
//			arr[arr.length]=6;
//			console.log(arr);


			//在数组中间添加数组
//			var arr=[1,2,3,4,5];
//			for(var i=arr.length-1;i>=parseInt((arr.length-1)/2);i--){
//				arr[i+1]=arr[i];
//			}
//			arr[parseInt((arr.length-1)/2)]=6;
//			console.log(arr);


			//删除数组的第一个数
//			var arr=[1,2,3,4,5];
//			for(var i=1;i<arr.length;i++){
//				arr[i-1]=arr[i];
//			}
//			arr.length--;
//			console.log(arr);


			//删除数组的最后一位数
			var arr=[1,2,3,4,5];
			arr.length--;
			console.log(arr);
		</script>
	</body>
</html>
```













### 函数



#### 定义函数

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    // 函数的定义
    // 1  字面量
    function aaa() {

    }

    // 2  函数表达式定义
    var bbb = function () {

    }
    //函数必须先定义，后调用 
</script>
</body>
</html>
```









#### 作用域

```
概念：
	作用域说的是变量起作用的区域
```

```
局部变量
	在局部作用域当中的变量(函数当中定义的变量)

全局变量
	在全局作用域当中的变量(函数外部定义的变量)
    
局部变量只能在函数内使用，而全局变量在哪都能使用

```

```
在全局中，如果定义变量，不加var，那么必须给这个变量赋值，不然无法定义，赋值就相当于给这个变量加上var，是一个地地道道的全局变量

在局部中，没有定义的变量指(函数的参数没有它，并且在函数内部定义函数时，前面没有加var)，定义变量不加var，首先要看外部是否定义了这个变量，如果外部定义过，就是操作这个变量，也就是重新赋值，即使是在函数外部使用这个变量，变量的值也是函数内部定义好的值，如果没有定义，变量也没有加var，相当于在全局定义了一个变量，也就是全局变量
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
      var a=20;
      function f1(a) {     //如果没有这个参数，a=40就相当于改了全局变量a的值，那么，第二个console.log传出的值是40
          a=40;
          b=20;				//由于外部没有定义b变量，函数的参数里也没有b，那么就相当于定义了一个全局变量b，值为20
          console.log(a,b);  //10 20
      }
      f1(a);
      console.log(a,b);   //20 20
</script>

</body>
</html>
```















#### 作用域链

```
作用域链：
	说的是变量在查找的过程
	
原理：
	变量在查找的过程中，首先从自己的作用域当中去查找，如果没有，就向上一级的作用域中去寻找，一直查到函数最外部的全局作用域中，只要找到，就立即停止往上寻找，将找到的变量输出，如果在函数的内部和函数的外部都没有找到，就报错
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>1</title>
</head>
<body>
<script>
    var num=0;
    function aaa() {
        var num=1;
        function bbb() {
            var num=2;
            function ccc() {
                var num=3;
                function ddd() {
                    var num=4;
                    console.log(num);
                }
                ddd();
            }
            ccc();
        }
        bbb();
    }
    aaa();
</script>
</body>
</html>
```







#### 函数在内存中

```
栈结构：数据先进后出
堆结构：数据随意增删
```

```
第一步
	程序执行开始，首先创建全局环境，然后才是局部环境，并且这些环境都是在栈里进行管理
	创建完全局环境后，会将程序里的所有全局变量收集起来开辟空间，函数也是一个变量
	
第二步
	函数被调用的时候才会创建函数环境，并且收集函数内的所有局部变量，执行开辟空间
	
第三步
	当函数执行完后，也就是函数返回值后，代表函数执行完成，此时，函数的环境会立即从栈中弹出，代表函数被销毁，也就是释放内存
	
第四步
	当整个程序执行完成后，全局环境最后才会弹出栈，也就是销毁了全局环境，释放掉全局环境所占的内存空间
```









#### 预解析

```
预解析也被称为		预解释		声明提升	变量提升
```

```
变量带var和不带var的区别
	预解析只能解析带var的变量，不带var的变量不会被解析

函数的区别
	字面量函数	function f1 () {}		如果是这种写法，函数整体会提升，也就是说函数内部的代码也会提升
	表达式定义函数	var f1=function(){}		只会提升变量f1，函数内部的代码没有提升
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    // console.log(a);
    // var a=12;
    // 等于
    var a;
    console.log(a);
    a=12;

</script>
</body>
</html>
```

```
当执行程序时，首先先创建全局环境，然后收集变量，只有带var的变量会被收集
```

```
预解析的效果
	变量：全局中所有带var的变量，以及使用字面量定义的函数，都会提升到全局的最上方
	函数：函数中所有带var的变量，以及使用字面量定义的函数，都会提升到这个函数的局部环境的最上方
```

```
预解析的优先级：
	先去解析函数，函数如果同名，会被后面的同名函数覆盖
	再去解析变量，如果变量同名，会进行忽略，前面的被忽略
```







#### 匿名函数

```
function(){};	
	这是一个匿名函数，本质上是一个没有名字的函数表达式

调用匿名函数
	(functio(匿名函数的型参){
		匿名函数的代码
	})(传入匿名函数的实参);
	
匿名函数自调用的特点：
	定义的时候就一起调用了，不会发生预解析，只会使用一次
	匿名函数只能执行一次
		作用：
			1.封装代码，不让代码暴露出去
			2.可以防止被外部的命名空间污染
			3.通常用来做一些项目的初始化
```









#### arguments

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var a=10;
    var b=5;
    function add() {
        console.log(arguments);      // 实参伪数组，当我们输入实参，实参会输入给arguments
    }
    add(a,b);
</script>
</body>
</html>
```

```
作用：
	我们可以根据arguments伪数组的长度来实现不同的功能，函数定义当中肯定有一个if else判断
```

```
arguments.callee				输出函数本身
```







#### 回调函数

```
定义：
	如果一个函数被当做参数传给另一个函数，那么这个函数被称为回调函数，虽然概念是这样定义的，但是一个真正的回调函数必须满足一下几个条件
		1.函数使我定义的
		2.我没有调用函数
		3.最终函数执行了
```









#### 函数传参

```
函数传参分为基本数据类型和对象数据类型

传基本数据类型和对象数据类型不一样，基本数据类型传进去后，函数内和函数外操作的值不一样，所以当传递基本数据类型的时候，函数内运算完后需要我们返回，不然值不变

但是如果传的是对象数据类型(数组)，那么函数内部和函数外部操作的是同一个数据，因为我们传入的是一个地址，函数需要通过地址来在堆中找到存放数据的对象，一旦堆中的数据改变，函数内部和外部都会改变，所以运算完后不需要返回，外部一样可以发生变化
```









### 对象

```
概念：在js中，一切皆对象
		对象是无序的名值对的集合(键值对的集合)
```

```
如果存储一个简单的数据(一个数字，一个字符串)		直接var a=10;
如果存储一堆数据，此时我们想到数组，数组就是专门用来存储对个数据用的
如果我们想要执行一段代码，或者让这段代码有功能，此时我们需要函数
如果我想描述一个复杂的事物，比如说一个人，一台电脑(电脑的硬件是什么，软件是什么等等)，需要用到多个属性或者方法才能描述清楚，此时就要用到函数
```







#### 创建方法

```
一般我们说的对象都是object的实例对象

定义对象的方法：
	1.字面量定义
	2.构造函数定义
	3.工厂函数定义
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    // 字面量定义
    var obj = {
        'name': '赵丽颖',
        'age': 18,
        sing: function () {
            console.log('我会唱');
        }

    };
    console.log(obj);

    
    // 构造函数定义
    var obj1 = new Object({name: '张三', age: 33});
    console.log(obj1);

    
    // 工厂函数定义，本质上还是使用构造函数
    function createObject(name,age) {
        var obj=new Object();
        obj.name=name;
        obj.age=age;
        return obj;
    }
    console.log(createObject('李四',33));
</script>
</body>
</html>
```







#### 增

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var obj={};    //相当于new object
    var aaa=12;

    // 增
    obj.name='张三';      // 相当于向实例对象obj添加了一个属性，属性名为name，值为 张三
    obj.age=18;
    obj['color']='yellow';      // 和上面的方式完全一样，注意，中括号内的名必须带引号
    // 如果中括号内不加引号，相当于变量处理，在程序内部寻找变量，将变量的值作为名，赋值的内容作为值，如果找不到，就报错
    obj[aaa]=function () {
        console.log('网');
    };
    console.log(obj);
    obj[aaa]();				// 调用对象中的函数

</script>
</body>
</html>
{name: "张三", age: 18, color: "yellow", 12: ƒ()}
网
```







#### 删

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var obj={};
    var a='category';
    obj.name='小黄';
    obj.age=12;
    obj.category='阿拉斯加';
    delete obj.age;
    console.log(obj);
</script>
</body>
</html>
```







#### 改

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var obj={};
    obj.name='小黄';
    obj.age=12;
    obj.category='阿拉斯加';
    // 改
    // 如果再次调用已经定义过得属性，并对他进行赋值，就是更改值
    obj.age=18;
    console.log(obj);
</script>
</body>
</html>
```







#### 查

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var obj={};
    var a='category';
    obj.name='小黄';
    obj.age=12;
    obj.category='阿拉斯加';
    console.log(obj.name);      // 读取obj对象当中name键的值
    console.log(obj['age']);    
    console.log(obj[a]);
    console.log(obj.aaaaaa)			// 如果对象中没有指定的属性，会输出undefined
</script>
</body>
</html>
```





#### 遍历

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var obj={
        name:'car',
        category:'劳斯莱斯',
        color:'black',
        money:10000000,
        run:function () {
            console.log('跑的很快');
        }
    }
    // 使用for... in遍历对象
    for(var key in obj){
        console.log(key,obj[key]);
        // 只能使用[]来遍历，如果使用obj.key，会将key认为是对象中的属性，但是对象中没有key这个属性
        // 所以会返回undefined，如果将key用中括号括起来，就会认为key是一个变量，就可以遍历对象了
    }
</script>
</body>
</html>
```











#### 构造函数

**this**

```
其实通常情况下任何函数都有this这个关键字
this本质上是一个对象，代表着调用这个函数或者方法的执行者
在函数中，函数也可以叫做window对象的方法，this永远代表window
在对象的属性的方法中，this代表这个对象
在构造函数中，代表的是实例化出来的对象
在事件当中，回调当中的this，代表的是事件对象
```



```html
 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    function P(name,age,color) {
        this.name=name;
        this.age=age;
        this.color=color;
        this.eat=function () {
            console.log('吃饭');
        }
        console.log(this);
    }
    // 构造函数当做普通函数执行，那么this代表的是windows，构造函数的意思就变为给window对象添加属性和方法
    var a=P('赖建东',19,'black');
    console.log(a);
    console.log(this);

    // 加上new，就相当于将函数当做构造函数，this代表的是P
    var b=new P('赖建东',19,'black');
    console.log(b);
</script>
</body>
</html>
```

**new**

```
new关键字实例化对象
	1.开辟内存空间
	2.this指向该内存
	3.执行函数
	4.生成对象实例
```





![image-20201022210031129](C:\Users\86188\AppData\Roaming\Typora\typora-user-images\image-20201022210031129.png)











#### 原型对象和原型链

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
	</head>
	<body>
		<script type="text/javascript">
			function BlueCat(name,age,gender){
				this.name=name;
				this.age=age;
				this.gender=gender;
			}
			Object.prototype.run=function(){
				console.log('跑的哼快');
			}
			var cat1=new BlueCat('tom',5,'male');
			console.log(cat1);
			var cat2=new BlueCat('jerry',8,'male');
			cat1.run();
			cat2.run();
			/*
			 	对象在调用方法（或者属性）的时候，首先会从自己对象的空间当中去找，如果找到就直接用了
			 	如果没有找到，然后去自己的原型对象空间去找（自己构造函数的原型对象），如果找到就用
			 	没有找到，然后去自己的原型对象的原型对象的空间去找（自己的构造函数的构造函数的原型对象中去找），如果找到就用
			 	没有找到，就继续向上去寻找，直到找到object的原型对象中为止，如果object的原型对象中没有，就报错
			 	我们将这个对象找属性的过程叫做原型链
			 	object是所有构造函数的祖宗
			 */
			
		</script>
	</body>
</html>

```

![原型对象示例图](C:\Users\86188\Pictures\Saved Pictures\原型对象示例图.png)

![image-20201105213704010](C:\Users\86188\AppData\Roaming\Typora\typora-user-images\image-20201105213704010.png)



#### apply和call

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
        function BlueCat(name,age,gender){
            this.name=name;
            this.age=age;
            this.gender=gender;
        }
    Object.prototype.run=function(){
        console.log('跑的哼快');
    };
    var cat1=new BlueCat('tom',5,'male');
    var cat2=new BlueCat('jerry',8,'male');

    function add(a,b) {
        return a+b;
    }
    // apply / call 方法可以改变一个函数的执行对象
    // 把add的执行者window改成cat1，让car1有求和的方法
    // apply的用法需要两个参数
    // 第一个参数是执行对象的名字
    // 第二个参数是函数所需要的值，并且值必须以数组的形式输入
    // call和apply的区别是call中第二个参数不需要以数组的形式输入
    var result=add.apply(cat1,[10,20]);
    var result1=add.call(cat2,20,30);
    console.log(result);
    console.log(result1);
    console.log(cat1);

</script>
</body>
</html>
```









#### typeof和instanceof



**typeof**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var a = 10;         //number
    a = 'zzzz';        //string
    a = true;          //boolean
    a = undefined;    //undefined
    a = null;         //object
    a = [1, 2, 3];    //object
    a = function () {
        console.log(111);
    }                 //function
    a = {};          //object
    console.log(typeof a);
    // typeof 在判断基本数据类型当中的数字，字符串，b布尔，undefined及函数时可以派上用场，
    // 但是当我们使用typeof判断数组和对象以及null时，会分别不出来
    
</script>
</body>
</html>
```





**instanceof**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var a = 10;         //number
    a = 'zzzz';        //string
    a = true;          //boolean
    a = undefined;    //undefined
    a = null;
    a = [1, 2, 3];    //Array
    a = function () {
        console.log(111);
    };                 //function
    a = {};          //object
    function Person(name, age) {
        this.name = name;
        this.age = age;
    }

    var per = new Person('zzzsas', 12);
    // instanceof 可以判断是一个数组对象还是一个其他构造函数的实例对象
    console.log(per instanceof Object);   // 判断指定变量是否为Object，返回为布尔值
    console.log(per instanceof Person);    // 判断指定变量是否为指定函数的实例对象
    a = null;
    console.log(a == null);    // == 专门用来判断null，如果相等就是null
</script>
</body>
</html>
```









#### 引用数据类型

```
值类型		就是基本的数据类型
	number
	string
	boolean
	undefined
	null

引用数据类型		就是对象数据类型
	
```



![数据类型导图](C:\Users\86188\Pictures\Saved Pictures\数据类型导图.png)



#### 栈和堆

```
栈	数据类型结构(栈)			先进后出			栈的内存一般比较小，计算机自动分配，存取速度快
堆	数据类型结构(链表)			随意进出		    堆的内存一般比较大，底层是需要程序员自己分配(js做了封装，会自动分配),
													堆里面一般存储的都是一些比较复杂的占空间比较大的数据
队列	数据类型结构(队列)			先进先出			

栈和堆是内存的存数据结构，内存被开辟使用，就一定会被计算机回收(释放内存)
```

```
变量存在栈
对象存在堆
```

![数据存在栈和堆的图解](C:\Users\86188\Pictures\Saved Pictures\数据存在栈和堆的图解.png)





```
栈中的全局环境和变量会随着程序的结束而销毁

堆中的数据不会随着程序的结束而销毁，数据依然在，只是没有任何变量指向他，那么堆中的数据就会变为垃圾对象，垃圾回收机制会在适当的时候将它清理

如果我们在程序中需要删除对象，那么就将这个对象的变量赋值为null，代表这个变量引用改变，这个对象也就成了垃圾对象，其实删除对象就是让堆中的对象数据变成垃圾对象
```









#### 内置对象JSON

```
什么是JSON
	是js中的内置对象，里面封装了对json格式数据的操作方式
	
什么是json
	是一种数据格式，是前后端目前数据交互的主要格式(xml)
	json通常情况下说的是字符串也叫json串
	在前端json串的格式就是对象或者对象的数组，只不过要把这些数据转换为字符串形式
	"[
	{
		"name":'咋整',
		"age":18
	}
	,
	{
		"name":'咋整',
		"age":18
	}
	,
	{
		"name":'咋整',
		"age":18
	}
	]"
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var dataText={
        name:'赵丽颖',
        age:19
    };
    var jjjj=[{name:'赵丽颖',age:19},{name:'孙俪',age:30},{name:'朱茵',age:60}];
    // 将对象json化  字符串化
    // stringify    把前端js当中的对象数组转换为后端json串
     dataText=JSON.stringify(dataText);
     jjjj=JSON.stringify(jjjj);
    console.log(dataText);
    console.log(jjjj);
    // parse    把后端的json串转换为前端的对象数组
    jjjj=JSON.parse(jjjj);
    console.log(jjjj);
</script>
</body>
</html>
```











#### Math工具对象

```
常用的方法：round		floor	ceil	radom    max    min		PI	   pow
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    //round     四舍五入
    //floor     向下取整
    //ceil      向上取整
    console.log(Math.floor(2.9));       // 2
    console.log(Math.ceil(2.1));       // 3
    console.log(Math.round(2.1));       // 2

    // random    取随机数
    console.log(Math.random());    // 返回0 -- 1之间的数，包含0，不包含1

    // max      返回最大数
    // min      返回最小数
    console.log(Math.max(12,45,12,86,21));    // 86
    console.log(Math.min(12,45,12,86,21));    // 12

    // PI       返回数学中的圆周率π
    console.log(Math.PI);

    //pow       计算几次方
    console.log(Math.pow(2,3));     //求2的3次方，为8
    
</script>
</body>
</html>
```



**随机取数**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    function getRadom(min,max) {
        return Math.floor(Math.random()*(max-min+1)+min);
    }
    var max;
    var min;
    max=103;
    min=25;
    var aaa;
    aaa=getRadom(min,max);
    console.log(aaa);
</script>
</body>
</html>
```











#### Date日期对象

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var date = new Date();
    console.log(date.getMonth());       // 月
    console.log(date.getFullYear());    // 年
    console.log(date.getDate());        // 天
    console.log(date.getHours());       // 时
    console.log(date.getMinutes());     // 分
    console.log(date.getSeconds());     // 秒
    console.log(date.toLocaleDateString());     // 获取年月天
    console.log(date.toLocaleTimeString());     // 获取时分秒
    console.log(date.getTime());                // 获取从1970.1.1到现在的毫秒数

</script> 
</body>
</html>
```







#### 包装对象

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var a=10;
    var b=new Number(20);       // 包装对象
    console.log(a.toString());
    // a.toString   a显然是一个对象，才会有方法调用，但是a我们定义的时候是一个基本数据类型，他是没有方法
    // 的，但是js当中基本数据类型操作的时候会有这么一个规定：
    //     当调用数字，字符串，布尔值的方法的时候，会首先把这个值包装成对象(临时的)，然后进行调用
    //      包装对象的方法，调用完之后，临时的包装对象会立即清除
    console.log(b);
</script>
</body>
</html>
```













#### ES5严格模式

```
严格模式
	1.消除javascript语法的一些不合理，不严谨之处，减少一些怪异行为
	2.消除代码运行的一些不安全之处，保证代码运行的安全
	3.提高编译器效率，增加运行速度
	4.为未来的版本做铺垫
```



```
严格模式的用法
	“use strict”	在js的第一行写，针对整个程序      在某个函数的第一行写，只针对这一个函数
	
	1.变量声明必须写var，不写var会报错
	2.禁止this指向window，即使构造函数忘记写new，也不会影响全局，会报错
	3.禁止随意删除对象
	4.对象不能有重复的属性，函数不能有重复的参数
```



```
EX6都是处在严格模式下
```









#### EX6 定义变量 let 和 const



```
let的特点及使用
	1.块级作用域声明变量，变量用let声明后，只能在定义变量的环境中使用，依旧是{}内使用
	2.let定义的变量不会预解析
	3.let变量不能重复定义
```



```
const的特点
	1.和let一样，也是块级作用
	2.变量定义时必须赋值
	3.变量定义后无法修改
	4.不能重复定义
```





#### 属性和属性节点

````
什么是属性?
	对象上保存的变量就是属性
	
	
如何操作属性
	对象.属性名称 = 值
	对象["属性名称"] = 值
	对象.属性名称
	对象["属性名称"]
	
	
什么是属性节点?
	在编写html代码时,在html标签中添加的属性,叫属性节点
	保存在DOM元素中的attributes属性中
	
	
如何操作属性节点
	setAttribute
	getAttribute
	
	
属性节点和属性的区别
	如何对象都有属性
	但是只要DOM对象有属性节点
````







### 数据方法





#### 字符串方法

```
注意：
	字符串无法被更改
	使用方法返回的值是一个新串，和原来的串没关系
```



**charAt**

```
str.charAt(index)  
作用：返回指定下标位置的字符
index 为必须参数，类型为number（0到str.length-1之间，否则该方法返回空串）
另外：str.charAt()即不带参数和str.charAt(NaN)均返回字符串的第一个字符
```





**charCoderAt**

```
str.charCodeAt(index)  
作用：返回指定下标位置的字符的 Unicode 编码
index 为必须参数，类型为number（0到str.length-1之间，否则该方法返回 NaN）
```





**concat**

```
作用：用来连接一个或多个字符串
var a='asddd';
    var b='ahsi1sd';
    var c='dskdushf';
    console.log(a.concat(b,c));
    'asdddahsi1sddskdushf'
```



**indexof**

```
作用：返回指定字符串在字符串中首次出现的位置。匹配不到则返回-1，第二个参数可以指定开始寻找的位置
```



 **lastIndexOf**

```
作用：返回指定字符串值最后出现的位置，在一个字符串中的指定位置从后向前搜索
```



**localeCompare**

```
作用：比较大小
```



**slice**

```
作用： 提取字符串的某个部分，并以新的字符串返回被提取的部分，含头不含尾
```





**split() **

```
 作用：以传入的参数为分割标志，将字符串转换为数组,加上‘’，代表将每个字符进行切割
```



**replace**

```
作用：替换
a.replace('aaa','bbb')			将字符串a中的aaa替换为bbb
```



**toLowerCase**

```
作用：将字符串中的字母全部转换为小写字母
```



**toUpperCase**

```
作用：将字符串中的所有字母转换为大写字母
```



**trim**

```
作用：去除字符串两边的空格
```



**以上的方法时ES5中的方法**

**以下的方法是ES6新增的方法**





**includes**

```
作用：判断指定的字符串是否是字符串中的子元素
```





**startsWith**

```\
作用：判断字符串是否以指定字符串开头
```





**endWith**

```
作用：判断字符串是否以指定字符串结尾
```





**repeat**

```
作用：将指定字符串重复指定次数，次数为正数
```











#### 数组方法

**concat**

```
作用：拼接数组，返回的是一个新的数组，不会更改原来的数组
```

```
    var a=[1,2,3];
    var b=[1,2,3];
    var c=[1,2,3];
    console.log(a.concat(b,c));
    [1, 2, 3, 1, 2, 3, 1, 2, 3]
```





**length**

```
作用：查询指定数组的长度
```





**join**

```
作用：将数组转化为字符串       不会改变原数组
```

```
var a=[1,2,3];
console.log(a.join());
1,2,3
console.log(a.join('*'));       // 以 * 连接数组中的各个元素
1*2*3
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var a=[1,2,3];
    var zz=a.join('*');
    var aaa=zz.split('*');
    var bbb=[];
    for(var i=0;i<aaa.length;i++){
         bbb[i]=Number(aaa[i]);
    }
    console.log(bbb);

</script>
</body>
</html>
```







**reverse**

```
作用：翻转数组       返回经过翻转的原数组，没有参数
```

```
 var a=[1,2,3,4,5,6];
    a.reverse();
   console.log(a);
  [6, 5, 4, 3, 2, 1]
```







**slice**

```
作用：提取指向范围下标的数组元素		含头不含尾		返回新的数组
```

```
 var a=[1,2,3,4,5,6,7,8,9,10];
   console.log(a.slice(2,8));
   [3, 4, 5, 6, 7, 8]
```







**sort**

```
作用：对数组的排序		在原数组上进行排序

		如果什么参数都不传，会按照Unicode码进行从小到大的排序
		
        如果传参数，需要传递一个回调参数
        console.log(arr.sort(function (a,b){
        return a-b;
        }))    
        按照从小到大的方式排序
        console.log(arr.sort(function (a,b){
        return b-a;
        }))    
        按照从大到小的方式排序
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var a = [1, 5, 4, 2, 7, 3, 8, 9, 6];
    console.log(a.sort());       //[1, 2, 3, 4, 5, 6, 7, 8, 9]

    console.log(a.sort(function (a, b) {
        return a - b;              //[1, 2, 3, 4, 5, 6, 7, 8, 9]
    }));

    console.log(a.sort(function (a, b) {
        return b - a;             //[9, 8, 7, 6, 5, 4, 3, 2, 1]
    }));
    var arr = [{id: 3}, {id: 6}, {id: 9}, {id: 1}, {id: 2}];
    console.log(arr.sort(function (a, b) {
        return a.id - b.id;
    }))
    //{id: 1} {id: 2} {id: 3} {id: 6} {id: 9}


</script>
</body>
</html>
```







**push**

```
作用：在原数组的末尾添加元素，返回添加元素后数组的长度
```

```
var a=[1,2,3,4,5,6];
console.log(a.push(1,2,3,4));
10
```







**pop**

```
作用：从原数组的末尾删除一个元素，返回删除元素的值
```

```
var a=[1,2,3,4,5,6];
console.log(a.pop());
6
```





**unshift**

```
作用：在原数组的头部添加元素，然后返回添加元素后数组的长度
```

```
var a=[1,2,3,4,5,6];
    console.log(a.unshift(1,2,3,4));    // 10
    console.log(a);                     // [1, 2, 3, 4, 1, 2, 3, 4, 5, 6]
```





**shift**

```
作用：在原数组的头部删除一个元素，然后返回删除元素的值
```

```
var a=[1,2,3,4,5,6];
    console.log(a.shift());    // 1
    console.log(a);                     // [2, 3, 4, 5, 6]
```





**splice**

```
作用：这个方法是一个万能的方法，可以增，删，改，并且都是在原数组的基础上进行的
```

```
删除
var  a=[1,2,3,4,5,6,7,8,9,10];
    console.log(a.splice(2,3));     // 将删除的元素组成为新的数组返回   [3,4,5]
    console.log(a);                 // 会影响原数组   [1, 2, 6, 7, 8, 9, 10]
```

```
增加
var  a=[1,2,3,4,5,6,7,8,9,10];
    console.log(a.splice(2,0,'zzz'));       // 一个元素也不删除，在元素的前面加入指定字符
    console.log(a);							// [1, 2, "zzz", 7, 8, 9, 10]
```

```
更改
var  a=[1,2,3,4,5,6,7,8,9,10];
    console.log(a.splice(2,1,'zzz'));       // 删除指定元素，然后在加入指定字符
    console.log(a);							// [1, 2, "zzz", 4, 5, 6, 7, 8, 9, 10]
```





**forEach**

```
作用：遍历数组
```

```
 var  a=[1,2,3,4,5,6,7,8,9,10];
    a.forEach(function (item,index) {
        console.log(item,index);
    })
    item	为值
    index	为下标
```



**map**

```
作用：遍历时返回一个新的数组，不会改变原数组
```

```
var  a=[1,2,3,4,5,6,7,8,9,10];
    var b=a.map(function (item,index) {
       return item;      
    });
    console.log(b);     //[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```





**filter**

```
作用：遍历过滤返回一个新的数组,如果条件成立，就返回
```

```
 var  a=[1,2,3,4,5,6,7,8,9,10];
    var b=a.filter(function (item,index) {
       return item>2;
    });
    console.log(b);     //[3, 4, 5, 6, 7, 8, 9, 10]
```



**以下是EX6新增的方法**



**Array.from**

```
作用：将字符串转换为数组，不会改变原数组
```



**of**

```
作用：将输入的参数转化为数组
var a=Array.of(1,2,3,4,5,6);
```





**find**

```
作用：找到指定数组的第一个符合条件的元素的值
```

**findIndex**

```
作用：找到指定数组的第一个符合条件的元素的下标
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    var a=[1,2,3,4,5,6,7,8];
    console.log(a.find(function (a,b) {
        return a>5;       // 6
    }));
    console.log(a.findIndex(function (a,b) {
        return a>5;       // 5
    }))

</script>
</body>
</html>
```



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script>
    /*
        定义数组时，如果用字面量定义，没有什么问题
        如果使用构造函数 new Array 或 Array(普通函数)定义，如果输入一个值，那么这个值就代表数组的长度
        如果是多个值，就是传入多个元素
     */
    var a=[3];
    var b=Array(3);
    var c=new Array(3);
    console.log(a);
    console.log(b);
    console.log(c);
</script>
</body>
</html>
```















### DOM

------

#### 概念

```
DOM		文档对象模型
DOM是一个使程序的脚本有能力动态地访问和更新文档的内容，结构以及样式的平台和语言中立的接口
DOM描述了处理网页内容的方法和接口
```

```
window是浏览器窗口对象，所有的东西都被当做window的子对象
```



**文档对象**

```
文档对象	document	是window下的一个属性	代表整个DOM文档对象(也就是整个页面)
节点		 属性  注释  文本  元素
根元素(root)		html标签
文档数(dom树)	   以HTML为根节点，形成一颗倒立的树状结构，我们成为DOM树
				  这个树上所有的东西都叫节点，节点分多种
				  这些节点如果我们使用DOM方法去获取或者其他的操作去使用的话，就叫DOM对象
```

![image-20201025165633314](C:\Users\86188\AppData\Roaming\Typora\typora-user-images\image-20201025165633314.png)

**文档数**

![image-20201025171242065](C:\Users\86188\AppData\Roaming\Typora\typora-user-images\image-20201025171242065.png)







#### window.onload

```
页面加载完成事件
	一般情况下，我们都是等待页面加载完成之后才去操作dom元素，如果页面没有加载完成就取获dom元素，有可能获取不到
```









#### 获取DOM对象

```
document.getElementById
	这是document下的一个方法，通过id获取到相关元素，封装为DOM对象返回
	必须有id才能获取
```









#### setAttribute 和 getAttribute

````
getAttribute		获取属性
setAttribute		设置属性
removeAttribute		删除属性
````

```
在操作元素属性的时候，语法只能操作元素天生具有的属性，如果是自定义的属性，通过语法是无法操作的
只能通过setAttribute 和 getAttribute 去操作
setAttribute 和 getAttribute是通用的语法，无论元素天生的还是自定义的都可以操作
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<a href="https://www.baidu.com" aa="bb" id="aaa">百度</a>
<input type="button" id="btn">
<script>
    window.onload=function () {
        var btn=document.getElementById('btn');
        var aaa=document.getElementById('aaa');
        btn.onclick=function () {
            // 将id为aaa的元素中的属性aa的值设置为cc
            // 第一个参数传入指定元素的属性
            // 第二个值传入指定元素的属性的值
            aaa.setAttribute('aa','cc');
            // 获取id为aaa的元素中的属性aa的值
            console.log(aaa.getAttribute('aa'));
        }
    }
</script>
</body>
</html>
```









#### getElementsByTagName 和 getElementsByClassName

```
getElementsByTagName
	作用：获取html中元素为指定元素的元素，将他们封装为一个数组
```

```
getElementsByClassName
	作用：获取html中类为指定类的类，将他们封装成一个数组
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <P class="pp">1</P>
    <P class="pp">2</P>
    <P class="pp">3</P>
    <P class="pp">4</P>
    <script>
        window.onload=function () {
            var plist=document.getElementsByTagName('P');
            var plist1=document.getElementsByClassName('pp');
            console.log(plist);
            console.log(plist1);
        }
    </script>
</body>
</html>
```









#### querySelect 和 querySelectAll

```
querySelect 和 querySelectAll也可以获取元素，但是他们和上面不同的是，他们是根据选择器去获取的，也就是说，只要选择器能选择到，他们就可以获取

querySelect	是专门用来获取选择器中单个元素，返回的是单个元素DOM对象
querySelectAll	可以选中多个元素，返回的是数组
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <P class="pp">1</P>
    <P class="pp">2</P>
    <P class="pp">3</P>
    <P class="pp">4</P>
    <script>
        window.onload=function () {
            var plist=document.querySelector("p:nth-child(3)");
            var plist1=document.querySelectorAll('p');
            console.log(plist);
            console.log(plist1);
        }
    </script>
</body>
</html>
```















#### innerHTML 和 innerText 和 textContent

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        p{
            background-color: #fa54af;
        }
    </style>
</head>
<body>
<P class="pp">1</P>
<P class="pp">2</P>
<P class="pp">3</P>
<P class="pp">4</P>
<script>
    window.onload=function () {
        var pList = document.getElementsByTagName('p');
        for (var i = 0; i < pList.length; i++) {
            pList[i].onclick = function () {
                for (var j = 0; j < pList.length; j++) {
                    // pList[j].innerText = '<h1>哈哈</h1>';
                    pList[j].innerHTML='<h1>哈哈</h1>';
                    // pList[j].textContent='<h1>哈哈</h1>';
                }
            }
        }
    }
</script>
</body>
</html>
```

```
他们三个的作用基本一样，都是将指定元素中的文本进行指定改变
```

```
innerHTML 和 innerText之间的区别
	设置内容的时候，如果内容当中包含标签		innerHTML中会生效，也就是说内容中的标签会在页面中生效
										innerText中不会生效，而是将标签以文本的形式输出，不会在页面中生效
	读取内容的时候，如果内容中包含标签		 innerHTML中会把标签也输出
										innerText中不会吧标签输出，只会输出内容
	读取内容的时候，如果内容中没有标签		 他们两一致，都是读取文本中的内容，innerHTML会带空白和换行
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<div id="div">
    i love you
    <span>me too</span>

</div>
<script>
    window.onload=function () {
        var a=document.getElementById('div');
        // console.log(a.innerText);
         console.log(a.innerHTML);
    }
</script>
</body>
</html>
```

````
textContent 和 innerText的区别
	textContent 可以获取隐藏元素的文本，包含换行和空白
	innerText 不能获取，也没有换行和空白
````









#### 排他方法

```
第一步：让所有的都成为一种样式
第二步：让当前发生事件的对象独自成为一种样式
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        p{
            background-color: yellow;
        }
    </style>
</head>
<body>
    <p>1</p>
    <p>2</p>
    <p>3</p>
    <p>4</p>
    <script>
        window.onload=function () {
            var pList=document.querySelectorAll('p');
            for(var i=0;i<pList.length;i++){
                pList[i].onclick=function () {
                    for(var j=0;j<pList.length;j++){
                        pList[j].innerHTML='哈哈';
                    }
                    this.innerHTML='嘻嘻';
                    // pList[i].innerHTML='嘻嘻';
                    // 这种方法是错误的，首先，第一个for循环完成后，为每一个p标签的onclick添加了一个
                    // 方法，添加完成之后，但是没有调用，也就是说我们没有点击，此时i = 4，如果我们点击
                    // 时，pList没有下标为4的元素，点击的元素内容就不会显示为嘻嘻，而使用this就代表这个
                    // 对象
                }
            }
        }
    </script>
</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        p{
            background-color: yellow;
        }
    </style>
</head>
<body>
    <p>1</p>
    <p>2</p>
    <p>3</p>
    <p>4</p>
    <script>
        window.onload=function () {
            var pList=document.querySelectorAll('p');
            for(var i=0;i<pList.length;i++){
                pList[i].a=i;
                pList[i].onclick=function () {
                    for(var j=0;j<pList.length;j++){
                        pList[j].innerHTML='哈哈';
                    }
                    pList[this.a].innerHTML='嘻嘻';
                }
            }
        }
    </script>
</body>
</html> 
```









#### 鼠标事件

```
onmousemove		移动元素
onmouseover / onmouseout		移入和移出
onmounseenter / onmounseleave	移入和移出
onclick / onmousedown / onmouseup 		点击元素
ondbclick		双击元素
```

```
一个元素可以添加多个事件
```













#### 兼容性封装设置读取内容函数

```
浏览器分为两个阵型
	高级浏览器和低级浏览器		IE8为分水岭
	
innerText  		什么浏览器都认识
textCantent		只有高级浏览器认识
```









#### 键盘事件

```
onkeyup		键盘按下执行事件
onkeydown		键盘按下后松开执行事件
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<input type="text" id="in">
<script>
    var inputNode=document.querySelector('input');
    // 键盘事件每一个键都会触发，添加的方式和鼠标事件添加方式一致
    // 但是键盘，我们无法分别到低按下的是哪一个键
    // 所以区分按下的键是什么键就是键盘事件当中的重点
    // 根据事件对象当中的键码去判断是什么键
    // 事件对象本身就存在，但是我们没有调用，在函数的参数中的第一个参数就是事件对象，事件对象包含事件相关的一切信息
    inputNode.onkeydown=function (e) {
        // 指定事件对象等于13，也就是说当输入的键为13(回车)时，执行if中的代码
        if(e.keyCode==13){
            console.log('发生了回车事件');
        }
    }
</script>
</body>
</html>
```



**阻止复制粘贴**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>

</body>
<script>
    window.addEventListener('keydown',function (e) {
        console.log(e.keyCode);
        //获取当前按键的类型
        console.log(e);
    //    如果是CTRL,e中的属性ctrlKey: true
    //    如果是其他按键,e中的属性ctrlKey: false
    //    所以判断组合键的方式为
        if(e.keyCode==67 && e.ctrlKey==true){
            // alert('你按下了ctrl+c');
            e.preventDefault();
        }
    })
     window.oncontextmenu=function (e) {
        e.preventDefault();
    }
</script>
</html>
```





#### 表单事件

```
onfocus		得到焦点
onblur		失去焦点
```

 ```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<input type="text" value="赵丽颖">
<script>
    var inputNode=document.querySelector('input');
    inputNode.onfocus=function () {
        this.value='杨幂';
        this.style.backgroundColor='red';
    };
    inputNode.onblur=function () {
        this.value = '赵丽颖';
        // 获取随机颜色，肯定用rgb设置
        var red = Math.floor(Math.random() * 256);
        var green = Math.floor(Math.random() * 256);
        var blue = Math.floor(Math.random() * 256);
        var c = Math.random();
        this.style.backgroundColor = 'rgb(' + red + ',' + green + ',' + blue +','+c+ ')';
    }

</script>
</body>
</html>
 ```



```
<div tabindex="正数"></div>
		使div可以获取焦点
```













### 节点

```
什么是节点
	文档树所有包含的东西都可以称作节点，最关注的是元素节点
	
节点的分类
	分为12种，重点了解3种	元素，文本，属性
```









#### 子节点和子元素(父节点和父元素)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <div id="box">
<!--        哈哈-->
        <p>我是第一个段落</p>
        <p>我是第二个段落</p>
    </div>

    <script>
        var box=document.getElementById('box');
        // childNodes       获取元素的子元素节点
        console.log(box.childNodes);
        // NodeList(7) [text, comment, text, p, text, p, text]
        for(var i=0;i<box.childNodes.length;i++){
            var a=box.childNodes[i];
            // nodeName     获取节点的名字
            // nodeType     获取节点的类型
            // nodeValue    获取节点的值
            console.log(a.nodeName,a.nodeType,a.nodeValue);
        }

        // documentElement      获取整个html
        var htmlNode=document.documentElement;
        // body     获取body
        var bodyNode=document.body;
        console.log(htmlNode.childNodes);
        // NodeList(3) [head, text, body]       这是系统做的优化，所以head的前面和body的后面没有text
        console.log(bodyNode.childNodes);
        // NodeList(4) [text, div#box, text, script]
    </script>
</body>
</html>
```



```
nodeName     获取节点的名字
	如果是文本节点，返回#text的字符串
	如果是属性节点，返回它的大写字母的名字
	
nodeType     获取节点的类型
	节点的类型是用数字来指定的
	nodeType == 1		元素节点
	nodeType == 2		属性节点
	nodeType == 3		文本节点
	
nodeValue    获取节点的值
	如果是元素节点，返回null
	如果是属性节点，返回属性的值
	如果是文本节点，返回文本的内容
```

```
childNodes		获取指定元素的子节点，包括元素子节点和文本子节点，如果有注释还有注释节点
children		获取指定元素的子元素

parentNode			获取元素的父节点，也就是父元素，所有浏览器都能用	
parentElement		获取元素的父元素，所有浏览器都能用
```



```
firstChild			获取第一个子节点		所有浏览器都能使用
fristElementChild	获取第一个元素节点		高级浏览器认识
lastChild			获取最后一个子节点		都认识
lastElementChild	获取最后一个元素节点		高级认识
previousSibling		获取上一个兄弟节点·		都认识
previousElementSibling		获取上一个兄弟元素节点			高级认识
nextSibling			获取下一个节点		都认识
nextElementSibling	获取下一个元素节点		高级认识
```







#### 创建节点

```
方法1
	documnet.write()	
		只能在页面加载的过程中使用，如果页面加载完成，再使用会将页面中的其他dom干掉，所以基本不用
		
		
方法2
	document.指定元素.innerHTML=
		一样会覆盖掉指定元素的其他子元素及其内容		
	document.指定元素.innerHTML+=
		不会覆盖
		
方法3
	document.createElement()
		创建一个你想要的元素
```

```
a.appendChild(b)
	向元素a的内部导入元素b
```







#### 常用方法

```
insertBefore(新节点，参照节点)							插入节点
replaceChild(新节点，被替换的节点)					  替换节点
removeChild(被删除的节点)								 删除节点
appendChild(被追加的节点)							   	 追加节点
a.remove()											 直接删除指定元素a,ie无法使用
```













### BOM

------



```
DOM的版本为0  1  2  3
	dom0和dom2有自己独立的事件绑定和解绑方法
	dom1和dom4没有
	
	dom0事件所有浏览器都能使用								默认是冒泡事件流
	dom2事件高级浏览器都能使用，   ie9以下不能使用		ie9以下给出了另一种绑定事件
```





#### DOM0事件的绑定和解绑

```
本质上就是让事件函数和事件对象的事件属性断开
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<input type="button" value="点击绑定事件"/>
<input type="button" value="点击解绑事件"/>

<script>
    var btn=document.querySelectorAll('input');
    btn[0].onclick=function () {
        console.log('i love you');
    };
    btn[1].onclick=function () {
        // 本质上就是让对象btn[0]的事件onclick指向的函数发生改变，使其变为null
        btn[0].onclick=null;
    }
</script>
</body>
</html>
```







#### DOM2事件的绑定和解绑

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<input type="button" value="点击绑定事件"/>
<input type="button" value="点击解绑事件"/>

<script>
    var btn=document.querySelectorAll('input');
    // btn[0].addEventListener('click',function () {
    //     console.log('i love you');
    // },false);

    //千万不要在fn后面加上括号，不加括号，就是对象事件调用函数，也即是自调函数，加上括号，就是我们自己调用函数
    // dom2事件如果对同一个对象(元素)添加多个相同的事件，不会覆盖，而是按照顺序依次执行
    // 第一个参数是事件的类型，不加on
    // 第二个参数为事件的自调函数
    // 第三个再议,默认为false
    btn[0].addEventListener('click',fn,false);
    btn[0].addEventListener('click',fn1,false);
    btn[0].addEventListener('click',fn2,false);
    function fn() {
        console.log('i love you');
    }
    function fn1() {
        console.log('i heda you');
    }
    function fn2() {
        console.log('i miss you');
    }
    // dom2事件可以在元素上添加多个相同事件

    // 解绑
    btn[1].addEventListener('click',function () {
        // 解绑的时候一定要和绑定的参数一样
        btn[0].removeEventListener('click',fn,false);
        btn[0].removeEventListener('click',fn1,false);
        btn[0].removeEventListener('click',fn2,false);
    },false);


</script>
</body>
</html>
```





#### ie9事件的绑定和解绑

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<input type="button" value="点击绑定事件" id="btn0"/>
<input type="button" value="点击解绑事件" id="btn1"/>

<script>
	var btn0=document.getElementById('btn0');
	var btn1=document.getElementById('btn1');
	function fn1(){
		console.log('i love you');
	}
	addevent(btn0,'click',fn1,false);
    // 兼容性封装函数
    function addevent(obj,eventType,fn,isBubble){
		if(obj.addEventListener){
			obj.addEventListener(eventType,fn,isBubble);
		}else{
            // 第一个参数为事件的类型，加on
            // 第二个参数为事件的自调函数
			obj.attachEvent('on'+eventType,fn);
		}
	}
	function removeevent(obj,eventType,fn,isBubble){
		if(obj.removeEventListener){
			obj.removeEventListener(eventType,fn,isBubble);
		}else{
			obj.detachEvent('on'+eventType,fn);
		}
	}
	btn1.onclick=function(){
		removeevent(btn0,'click',fn1,false);
	}
</script>
</body>
</html>
```

```
attachEvent			ie10以下使用它来添加多个事件
detachEvent			ie10以下使用它来解绑多个事件

只有在ie浏览器才能使用，其他浏览器无法使用
```











#### 事件流(事件传播)

```
捕获事件流(网景)			最终很少用到

冒泡事件流(ie)			 最终我们用到的时间传播都是冒泡

标准DOM事件流			 这个是我们现用的最标准的事件流，包含三个阶段：由捕获	再到获取元素	最后冒泡
					    	这三个阶段当中的捕获和冒泡可以由我们自己选择，但是通常情况下使用默认(冒泡)
```

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			*{
				padding: 0;
				margin: 0;
			}
			.laoda{
				width: 500px;
				height: 500px;
				background-color: red;
				position: absolute;
				left: 0;
				bottom: 0;
				top:0;
				right: 0;
				margin: auto;
			}
			.laoda .laoer{
				width: 300px;
				height: 300px;
				background-color: green;
				position: absolute;
				left: 0;
				bottom: 0;
				top:0;
				right: 0;
				margin: auto;
			}
			.laoda .laoer .laosan{
				width: 100px;
				height: 100px;
				background-color: yellow;
				position: absolute;
				left: 0;
				bottom: 0;
				top:0;
				right: 0;
				margin: auto;
				text-align: center;
				line-height: 100px;
			}
		</style>
	</head>
	<body>
		<div class="laoda">
			<div class="laoer">
				<div class="laosan">
					我是老三
				</div>
			</div>
		</div>
		
		<script type="text/javascript">
			var laoda=document.querySelector('.laoda');
			var laoer=document.querySelector('.laoda .laoer');
			var laosan=document.querySelector('.laoda .laoer .laosan')
			laoda.addEventListener('click',function(){
				console.log('我是老大');
			},true)
			// true为捕获事件流
			// false为冒泡事件流，默认为false
			laoer.addEventListener('click',function(){
				console.log('我是老二');
			},true)
			laosan.addEventListener('click',function(){
				console.log('我是老三');
                // 阻止冒泡
                event=event||window.event;
				event.stopPropagation();
			},true)
		</script>
	</body>
</html>

```

```
捕获事件流
	从外向内
		点击老大，输出老大
		点击老二，先输出老二外层的老大，再输出老二
		点击老三，先输出最外层的老大，在输出老三外层的老二，最后输出老三
		
冒泡事件流
	从内向外
		点击老大，输出老大
		点击老二，先输出老二，在输出老二外层的老大
		点击老三，先输出老三，在输出老三外层的老二，最后输出最外层的老大
```









#### event的兼容处理

```
event=event||window.event
```





#### 事件冒泡和事件委派

```
事件冒泡的好处就是可以进行事件委派(事件委托，事件代理)


事件委派的用法：
	什么时候用：出现新添加的东西，并且新添加的东西要和老的拥有同样的行为，此时我们就可以使用事件委派
	用法：给爹添加事件，不给元素本身添加，事件发生后通过爹去找真正发生事件的元素进行处理
```

```
事件委托实现步骤：
	1.找到当前节点的父节点或者祖先节点
	2.将事件添加给你找到的父节点或者祖先节点
	3.找到触发对象，进行操作
```





#### onmouse区别

```
 onmouseenter onmouseleave    如果一个父子元素模型，对父元素添加移入和移出，当鼠标移入父元素里面的子元素时，事件没有进行切换，也就是说他们检测不到父元素里的子元素   
 
 onmouseover  onmouseout    事件会进行切换，在进行事件委派的时候，必须用这一对    他们可以检测到父元素的子元素
```







#### window对象是bom的顶级对象

```
location
	调用方法：window.location.href
	作用：1.读：让用户获取当前页面的地址
		 2.写：通过修改地址来重定向到一个新的页面
		 
navigator
	是一个只读对象
	window可以省略
	作用：描述浏览器本身的信息，比如名字，版本，语言等
	
screen
	获取屏幕的信息
	
history
	获取历史记录
```

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
	</head>
	<body>
		<input type="button" value="点我获取网址">
		<script type="text/javascript">
			var btn=document.querySelector('input');
			btn.addEventListener('click',function(){
				// 获取网页的地址
				console.log(window.location.href);
				// 当点击input时，网址跳转到指定网址
				// window.location.href='https://www.baidu.com';
				// console.log(navigator.appName,navigator.appVersion);
				console.log(screen.width);   //屏幕宽度
				console.log(screen.height);  // 屏幕高度
				console.log(screen.availWidth);  // 可用宽度
				console.log(screen.availHeight);  // 可用高度
			})
		</script>
	</body>
</html>

```





#### window.onresize

```
作用：当浏览器窗口发生改变时，执行代码
```

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
	</head>
	<body>
		<script type="text/javascript">
			window.onload=function(){
				window.onresize=function(){
					console.log('浏览器窗口大小改变了');
				}
			}
		</script>
	</body>
</html>

```









#### event对象

```
概念：系统给我们封装的，任何事件都会有一个event对象，就是回调函数的第一个形参

兼容性处理
	event=event||window.event
	
target
	作用：获取发生事件的子元素
	兼容处理
		var target = event.target||event.srcElement
```







#### 获取鼠标位置

```
clientX   clientY	
	拿到鼠标相对于视口的水平位置和垂直位置，以视口的左上角为原点
	
pageX		pageY
	拿到的是鼠标相对于页面的水平位置和垂直位置，以页面的左上角为原点
	
offsetX		offsetY
	拿到的是鼠标相对自身元素的水平位置和垂直位置，相对于自身元素的左上角为原点
```









### 定时器案例

```
定时器的操作是异步的
```





#### 单次定时器

```
单次定时器
	一般用来做延迟效果      定时操作
```

```
setTimeout			延迟定时器
clearTimeout		清除延迟定时器
```

```
同步：指一个进程在执行某个请求的时候，若该请求需要等一段时间才能返回信息，那么这个程序会一直等待下去，知道该请求返回信息才继续执行

异步：程序不会等待，而是继续执行下面的操作，不管其他进程的状态，这样会提高效率
```

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
	</head>
	<body>
		<button>点击清除</button>
		<script type="text/javascript">
			var btn=document.querySelector('button');
			var a=4;
			var b=6;
			var c=a+b;
			// 定位为全局变量
			var timer=null;
			// 延迟定时器，是window下的一个全局方法，有两个参数
			// 第一个参数：回调函数，也就是到时间时干什么
			// 第二个参数：时间，以毫秒为单位
			timer=setTimeout(function(){
				console.log(c);
			},5000);
            
            // 前面有定时器，但是发现后面这句话并没有5秒之后打印，证明定时器是一个异步操作
			// 如果是同步操作，必须等定时器执行完成之后，这句话才会打印
			console.log('i love you');
			
			// 清除延迟定时器
			btn.onclick=function(){
				clearTimeout(timer);
			}
			
			
		</script>
	</body>
</html>

```







#### 多次定时器

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
	</head>
	<body>
		<button type="button">点击清除</button>
		<script type="text/javascript">
			var btn=document.querySelector('button');
			var timer=null;
            // 循环定时器
			timer=setInterval(function(){
				console.log('i love you');
			},3000);
			btn.onclick=function(){
                // 解除循环定时器
				clearInterval(timer);
			}
		</script>
	</body>
</html>

```









#### 元素的大小和位置

```
offset系列 			
	offsetWidth			获取指定元素内容区+padding+border的大小
	offsetHeight
	offsetLeft			获取偏移量，和绝对定位一样，但是是获取
	offsetTop
	
	
	
Client系列
	clientWidth			获取指定元素内容+padding的大小
	clientHeight
	clientTop			获取指定元素上边框的宽度
	clientLeft			获取指定元素左边框的宽度
	
	
	
scroll系列
	scrollWidth			当元素内容区比元素小时，获取的是元素的clientWidth，也就是内容+padding
						当元素内容区比元素大时，获取的是元素的内容的offsetwidth+盒子一侧的内边距(前提是由内边距的情况下加)
	scrollheight
	scrollTop			拿到是盒子内容向上滚动的距离
	scrollLeft			拿的是盒子内容向左滚动的距离
```



```
获取视口的宽高
	document.documentElement.clientwidth
	document.documentElement.clientHeight
```



```
获取元素的宽高，先看看元素是否有边框，如果没有，是由offset和client一样
								如果有，看你的需要，需要边框用offset，不需要用client
```









#### 初始包含块及系统滚动条的控制

```
初始包含块
	 真正意义上来说,绝对定位相对于初始包含块定位,初始包含块的大小就是第一屏视口的大小,也就是打开浏览器时页面的视口大小
```

![初始包含块 (2)](C:\Users\86188\Pictures\Saved Pictures\初始包含块 (2).png)

```
html 和 body这两个元素overflow的scroll属性，控制着系统的滚动条
系统的滚动条有两个，一个是body身上的，一个是document身上的，我们平时看到的滚动条是documnet上的
如果我们想要控制系统滚动条，有以下情况：
	1.单独给body和html设置overflow：scroll，滚动条打开的全部都是document上的
	2.如果给元素同时设置overflow
			body设置为scroll，html设置为hidden
					body身上的滚动条打开，document身上的滚动条关闭
			body设置为hidden，html设置为scroll
					body身上的滚动条关闭，document身上的滚动条打开
	3.给body和html同时设置为overflow：hidden，那么body和document身上的滚动条都关闭
	4.给body和html同时设置为overflow“scroll，那么body和document身上的滚动条都打开
```

```
如何禁用系统的滚动条
	html,body{
	width:100%;         // 这个属性加上只是为了让设置overflow：hidden更有说服力，只有内容超出才会出现滚动条
	height:100%;        // 如果不设置，那么body和html高度由内容撑开，也就是说body当中的内容永远不会溢出
	overflow:hidden;
	}
```







#### 拖拽

```html
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title></title>
	<style>
		*{
			padding: 0;
			margin: 0;
		}
		#box{
			width: 200px;
			height: 200px;
			background-color: red;
			position: absolute;
			top:0;
			left: 0;
		}
	</style>
</head>
<body>
<div id="box">aaaaaa</div>
<script type="text/javascript">
	var box=document.getElementById('box');
	// 鼠标点入指定元素
	box.onmousedown=function(event){
		event=event||window.event;

		// 获取元素的初始位置
		var eleX=box.offsetLeft;
		var eleY=box.offsetTop;

		// 获取鼠标的初始位置
		var satrtX=event.clientX;
		var satrtY=event.clientY;
		
		// 全局捕获
		box.setCapture && box.setCapture();

		document.onmousemove=function(event){
			event=event||window.event;

			// 获取鼠标的移动后位置
			var endX=event.clientX;
			var endY=event.clientY;

			//获取移动的距离差
			var disX=endX-satrtX;
			var disY=endY-satrtY;

			// 获取移动后的元素位置
			var lastX=eleX+disX;
			var lastY=eleY+disY;
            
            if(lastX<0){
                lastX=0;
            }else{
                lastX=
            }

			box.style.left=lastX+'px';
			box.style.top=lastY+'px';
		};

		document.onmouseup=function () {
			document.onmousemove=document.onmouseup=null;
			// 释放全局捕获
			box.releaseCapture && box.releaseCapture();
		};

		// dom0事件取消默认行为
		// return 代表结束，return以下的代码不会执行
		return false;
		// dom2事件取消默认行为
		// event.preventDefault();
	}
</script>
</body>
</html>

```





#### 取消默认行为

```
dom0事件取消默认行为
	return 代表结束，return以下的代码不会执行
	return false;
dom2事件取消默认行为
	event.preventDefault();
```





#### 全局捕获

```
元素发生事件之后，鼠标的所有事件行为全部都被捕获到该元素上，也就是说，即使是在document上移动鼠标，也会被捕获到该元素上
	box.setCapture && box.setCapture();
	
释放全局捕获
	box.releaseCapture && box.releaseCapture();
```







#### getBoundingClientRect

```
获取元素离视口的距离
a.getBoundingClinetRect().top
a.getBoundingClinetRect().left
```











#### 使指定元素居中的方式

```
1.开启定位
2.使用transform中的平移
```









#### 自制滚动条







#### 滚轮事件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        div{
            width: 100px;
            height: 100px;
            background-color: red;
        }
    </style>
</head>
<body>
    <div></div>
</body>
<script>
    // 滚轮事件
    //     onmousewheel
    //     触发条件：当我们滚动鼠标上的滚轮时，触发该条件
    //     由于onmousewheel在火狐上不支持，所以我们需要添加多个事件
    //     DOMMouseScroll


    //     判断滚轮滚动的方向
    //          event.wheelDelta
    //            向上滚       120
    //            向下滚       -120
    //           通常我们只看正负，不看值
    //      wheelDelta在火狐上不支持，所以我们使用detail
    //      detail
    //          向上滚     -3
    //          向下滚     3


    window.onload=function (){
        var box=document.querySelector('div')
        // 给指定元素添加多个事件，如果第一个不能使用，就使用第二个
        box.addEventListener('mousewheel',fn)
        box.addEventListener('DOMMouseScroll',fn)
        var flag=true

        function fn(event) {
            event = event || window.event
            if(event.wheelDelta>0||event.detail>0){
                box.style.height=box.offsetHeight-10+'px'
            }else{
                box.style.height=box.offsetHeight+10+'px'

            }
        }
    }
</script>
</html>
```









### 正则表达式

````
概念：描述字符模式的对象
		用于对字符串模式匹配级检索替换
		
正则就是让我们用来在一个字符串中查找符合正则规则的字符串
````



```
规则：
	计算机可以根据正则表达式，来检查一个字符串是否符合规则
	获取将字符串中符合规则的内容提取出来
```



```
正则表达式是一个对象
```





#### 字面量定义正则

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
	</head>
	<body>
		<script type="text/javascript">
			/*
				使用字面量来创建一个正则表达式
					语法
						var 变量 = /正则表达式/匹配模式
				
				使用字面量的方式创建更加简单
				使用构造函数创建更加灵活
			*/
		   // var reg=new RegExp('a','i');
		   var reg=/a/i;
		   // 检查一个字符串有a或b
		   var a=/a|b/;
		   console.log(a.test('ccb'));
		   /*
			[] 里的内容也是或的关系
			[ab]==a|b
			[a-z]   任意的小写字母
			[A-z]	任意的字母
			
			检查一个字符串是否含有abc adc aec
			var a=/abc|adc|aec/;
			var a=/a[bde]c/;
		   */
		  
		  /*
			[^]    除了
			var a=/[^an]/;
			判断指定字符串是否含有ab,有就返回false，没有返回true
			var a=[^0-9];
		  */
		</script>
	</body>
</html>

```











#### 构造函数定义正则

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
	</head>
	<body>
		<script>
			// 创建正则表达式的对象
			/*
			语法：
				var 变量 = new RegExp("正则表达式","匹配模式");
				使用typeof来检查正则对象，返回object
				在构造函数中可以传递一个匹配模式作为第二个参数
					可以是
						i		忽略大小写
						g		全局匹配模式
			*/
			var reg=new RegExp('a','i');
			console.log(typeof reg);
			
			/*
				正则表达式的方法
					test()
						使用这个方法可以用来检查一个字符串是否符合正则表达式的规则
						如果符合返回true，否则返回false
						
			*/
		   var str='a';
			console.log(reg.test(str));      //true
			console.log(reg.test('abc'));    //true
			console.log(reg.test('db'));     //false
			console.log(reg.test('Abc'));    //false
		</script> 
	</body>
</html>

```







#### 字符串和正则

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
	</head>
	<body>
		<script type="text/javascript">
			/*
				split()
					可以将字符串拆分为数组
					方法中可以传递一个正则表达式作为参数，这样方法将会根据正则表达式去拆分字符串
			*/
		   var str='vvohvod93288w9rdsjdf';
		   var result=str.split(/[A-z]/);
		   console.log(result);
		   
            
            
		   /*
				search()
					可以搜索字符串中是否含有指定内容
					如果搜索到，返回第一次出现的索引，没有搜到返回-1
		   */
		  var str1='hrllo Abc adc da ad ae dsfr abc';
		  result=str1.search(/a[bd]c/i);
		  console.log(result);
		  
            
            
		  
		  /*
			match()
				可以根据正则表达式，从一个字符串中将符合条件的内容提取出来
				默认情况下，match只会找到第一个符合要求的内容，然后停止寻找，我们可以将正则表达式设置为全局匹配模式，这样
						就会匹配所有内容
				可以给一个正则表达式设置多个匹配模式，且顺序无所谓
		  */
		 str='1jsdo1vf837f73dfhi2333544jjjfAAA';
		 result=str.match(/[a-z]/ig);
		 console.log(result);
		 
            
            
	
		/*
			replace()
				可以将指定字符串中的指定内容替换为新的内容
				参数：
					1.被替换的内容，可以接收一个正则表达式作为参数
					2.替换的内容
					默认只会替换第一个
		*/
		result=str.replace(/j/g,'Z');
		console.log(result);
		  
		</script>
	</body>
</html>

```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>

</body>
<script>
    var a='djshsalsdnjdisdfkjdfsgfdnksdjfigfsdfjdsbfsdjfsbdfhbyfsgdfhsdfxjbdsfhjsfnfvadf';
    // 第一个参数为搜索到的指定数字,第二个参数为下标
    var str=a.replace(/d/g,function (val,group) {
        console.log(val,group);
    })
</script>
</html>
```



```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
	</head>
	<body>
		<script type="text/javascript">
			/*
						量词
							- 通过量词可以设置内容出现的次数
							{n}  	 正好出现 n 次
							{m,n}    真好出现 m-n 次
							{m,}     正好出现 m 次以上
							^        以指定字符串开头
							$		 结尾是否是指定字符
					*/
			
			var reg=/a{3}/;       // 判断指定字符串中是否含有字符串aaa
			console.log(reg.test('aaaaa12'));
			var reg=/(ab){3}/;     // 判断指定字符串是否含有ababab
			console.log(reg.test('ababab1212'));
			var reg=/ab{1,3}c/;			// 判断一个字符串是否含有abc，或者abbc ，或者abbbc
			var reg=/^a/;
			console.log(reg.test('accca'));
			var reg=/a$/;
			console.log(reg.test('ccca'));
			
			// 判断手机号
			var reg=/^1[3-9][0-9]{9}$/;
			console.log(reg.test('13011111111'));
			
			// 单词边界   \b
			var reg=/\bchild\b/;
			console.log(reg.test('childaaa'));
			
		</script>
	</body>
</html>

```











````
/[1253]/								字符串是否含有数字1或者2或者5或者3
/(as|djas)/								字符串是否含有字符串as或者字符串djas
\d										一个数字
\d+										多个连着一起的数字,不限长度,但是必须都是数字,不能有其他字符
^										以什么开头
$										以什么结尾

````





















## JS高级



### 变量和常量

```
变量
	作用: 用于储存数据,保存的数据可以改变
	本质: 变量本身也是数据,也需要在内存中占用空间,保存在内存中的栈结构分区中
	
	
常量
	作用: 用于储存数据,保存的数据不可以改变
	本质: 变量本身也是数据,也需要在内存中占用空间,保存在内存中的栈结构分区中
	
	
	常量一般是全部大写
```









### js数据类型

```
js数据类型分为: 基本数据类型和复合数据类型(引用数据类型,对象)

基本数据类型: 
	定义: string  number  boolean  null  undefined
	特征: 基本数据类型数据赋值给某个变量之后值本身就不会再发生变化
	
引用数据类型:
	定义: object  array  function
	特征: 引用数据类型的值可以通过其赋值的变量修改
```







### 内存结构



```
在js中只有堆内存,所谓的栈内存和堆内存其实是堆内存的两块分区
```



```
理解内存
	1. 内存条通电后产生的储存空间(临时的)
	2. 产生和死亡: 内存条 ---> 通电 ---> 产生一定容量的内存 ---> 存储各种数据 ---> 断电 ---> 内存消失(内存中的数据也随之消失)
	3. 内存的空间时临时的,而硬盘的空间时持久的
	4. 一块内存包含两种数据
		* 内存储存的数据
		* 内存地址值数据
	5. 内存分类
		栈结构: 全局变量,局部变量(空间较小)
		堆结构: 对象(空间较大)
```







### 函数基本理解

```
理解:
	1. 函数也是对象
	2. 调用函数的方法
		* test()
		* new test()
		* obj.test()
		* test.call/apply(obj)
	3. this的指向
		* 函数自调用: window
		* 构造函数(new function): 当前构造函数的实例对象
		* 对象.方法(): 对象本身
		* fun.call(指定的对象): 指定的对象
```





### 函数高级

```
new的作用
	第一步: 在堆中开辟一块内存空间
	第二步: this指向内存空间
	第三步: 指向函数
	第四步: 返回结果
```







#### 原型对象和原型链



~~~
原型对象：
	1.每一个函数都有一个prototype属性(与生俱来的,创建函数就有)，该属性指向的是原型对象(显示原型对象：可以操作原型对象的内容)
	2.每个实例对象都有一个__proto__属性，该属性指向的也是原型对象(隐式原型对象：无法操作，只能查看)
	3.构造函数的显示原型对象 == 当前构造函数的实例对象的隐式原型对象
	4.原型对象中的constructor指向的是构造函数，所以说原型对象和构造函数是互相指向的
	5.原型对象的本质：普通的object实例对象(它是一个对象,不是函数,对象中有方法和属性)
~~~



```
当我们将函数当做实例化对象去使用时，它的构造函数他的构造函数
当我们将函数当做普通函数去使用时，它的构造函数就是Function
```



```
原型链
	1. 查找对象的属性的时候先从自身找,自身没有沿着__proto__找原型对象
	2. 如果原型对象身上没有,那么沿着原型对象的__proto__找,直到找到object的原型对象
	3. 如果object的原型对象上也没有,就报错
	4. 原型链: 沿着__proto__查找的这条链称为原型链
```

![原型链](C:\Users\86188\Pictures\Camera Roll\原型链.png)

```
找对象的属性或方法时,会沿着原型链找
找变量时会沿着作用域链找
```



```
设置对象的属性时,不会将它放在原型对象上,属性一般是写在构造函数中
```









### 执行上下文和上下栈



```
变量提升 & 函数提升
	1.js引擎在js代码正式执行之前，会做一些预解析
	2.找关键字：var	function
	3.找到var以后将var后面的变量提前声明，但是不会赋值
	4.找到function以后定义对应的函数，也就是说，函数在预解析的时候已经定义完毕
	5.预解析: 全局预解析  函数预解析
	6.注意:
			全局预解析在定义函数的时候,不管函数函数是否被调用,都会预解析
			函数预解析在定义函数的时候,如果函数内的内部函数没有被调用,就不会预解析
```



```
function aa(){
				
			}
			console.log(aa);     // 打印的是函数整体
			console.log(aa());    // 打印的是函数的值
```





#### 执行上下文

  

```
执行上下文
	理解
		- 执行上下文抽象的概念，代表了代码执行的环境，包含：执行环境，变量对象，this，作用域链
	流程
		- js引擎在js代码执行之前，会先创建一个执行环境
		- 进入该环境以后创建一个变量对象，该对象用于收集当前环境下的：变量，函数，函数的参数，this
			--  找关键字var function
		- 确认this的指向
		- 创建作用域链
```

```
作用域和上下文环境一定要区别分开
	作用域是定义的时候创建的
	上下文环境是调用的时候创建的
```





#### 执行上下文栈

```
在全局代码执行前,JS引擎就会创建一个栈来储存管理所有的执行上下文
在全局执行上下文确定后,将其添加到栈中(压栈)
在函数执行上下文创建后,将其添加到栈中(压栈)
当前函数执行完后,会将其执行环境从栈中弹出(出栈)
当所有的代码执行完后,栈中只有window
```



```
重点:
	执行上下文是动态创建的
	尤其是针对函数,每调用一次函数都会创建一次执行上下文
```











### 作用域和作用域链





~~~~
作用域
	作用域是静态的，只要函数定义好了就一直存在，且不会改变
	上下文环境是动态的，调用函数时创建，调用函数结束后会被释放
~~~~



```
分类
	全局作用域
	函数作用域
	eval作用域
```



```
作用
	隔离变量,不同作用域下同名变量不会有冲突
	规定当前函数之后创建作用域链的上一链条是什么样的
```



```
作用域和执行上下文的区别
	全局作用域之外,每个函数都会创建自己的作用域,作用域在函数定义时就已经确定了,而不是函数调用时
	全局执行上下文环境是在全局作用域确定之后,js代码马上执行之前创建的
	函数执行上下文环境是在调用函数时,函数体代码执行前创建的
	作用域是静态的，只要函数定义好了就一直存在，且不会改变
	上下文环境是动态的，调用函数时创建，调用函数结束后会被释放
```



```
作用域理解
	抽象的理解： 用来决定代码执行的范围，变量所属的范围
	
作用域链理解
	作用域链是一个数组结构
	作用域链是在js代码执行之前创建的
	
```















### 闭包

```
如何产生闭包
	1.函数嵌套
	2.内部函数引用外部函数的局部变量
	3.使用内部函数
```



```
闭包到底是什么
	所谓的闭包是一个引用关系，该引用关系存在于内部函数中，引用的是外部函数的变量的对象
		必须是内部函数引用了外部函数的局部变量
```



````
	function fun(){
            var a=10
            function fun2(){
                console.log(a)
            }
            return fun2
        }
        var fun2=fun()
        fun2()
        

观察上述代码:
	首先,js引擎在js代码执行之前开辟一块运行环境global,然后预解析: fun2=undefined  fun=函数
	预解析时,发现fun是一个函数,在堆中开辟一块内存空间,存放fun代码,栈中变量对象中fun存放的是堆中地址
	从上到下执行,执行到var fun2=fun()时,在栈中压入fun的运行环境,然后预解析: a=undefined  fun2=函数
	预解析时,发现fun2是一个函数,在堆中开辟一块内存空间,存放fun2代码,栈中变量对象中fun2存放的是堆中地址
	从上到下执行,返回fun2,执行fun2函数
	重点: 每一个运行环境(执行上下文环境)都会被引用,如果没有被引用(指向),就会在下一次垃圾回收机制时被回收,当我们执行fun函数时
			会创建fun的执行上下文环境,堆中的fun会指向栈中的fun的执行上下文环境,fun函数执行完后,fun的执行上下文环境就没有被指				向了,然后在下一次垃圾回收机制时就会被消除,但是由于fun2函数执行时用到了fun的变量对象,也就是说堆中的fun2指向了				fun的执行上下文环境,所以说fun的执行上下文环境没有被消除,因此fun2函数可以获取到外部函数fun的变量,当函数fun2执				行完后,就不会指向fun的执行上下文环境了,当垃圾回收机制再来时,fun的执行上下文环境就会被消除
			
			
````



```
闭包的作用
	1.延长外部函数变量对象的生命周期
	2.让函数外部可以操作(读写)到函数内部的数据(变量和函数)
	
	注意：浏览器为了性能后期将外部函数中不被内部函数引用的变量消除了

```



```
闭包的优缺点
	优点：延长了外部函数变量对象的生命周期
	缺点：占内存，如果不及时清除，会造成内存溢出
```



```
缺点的解决方法
	使内部函数为null即可
```





````
一般情况下，在函数fn执行完后，就应该连同它里面的变量一同被销毁，但是在这个例子中，匿名函数作为fn的返回值被赋值给了fn1，这时候相当于fn1=function(){var n = 0 ... }，并且匿名函数内部引用着fn里的变量num，所以变量num无法被销毁，而变量n是每次被调用时新创建的，所以每次fn1执行完后它就把属于自己的变量连同自己一起销毁，于是乎最后就剩下孤零零的num，于是这里就产生了内存消耗的问题s
````









**扩展**

```
作用域的分类
	静态作用域(词法作用域)
	动态作用域
	
特征对比
	1. 词法作用域规定作用域在代码定义的时候就决定了,而不是看调用的时候
	2. 动态作用域是在代码执行的时候决定的
```











### 对象基础

````
什么是对象?
	代表实现中的某个事物,是该事物在编程中的抽象
	多个数据的集合体
	用于保存多个数据的容器
````







### 继承模式



#### 原型链继承

```JavaScript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script>   
    // 原型继承:    子类的原型成为父类的实例对象 
            //问题: 没有constructor
            //解决: 添加constructor
        function Person(name,age){
            this.name=name
            this.age=age
        }
        Person.prototype.showName=function (){
            console.log(this.name)
        }

        var person1=new Person('laijiandong','12')
        person1.showName()

        function Child(name,age){
            this.name=name
            this.age=age
        }
        //原型继承
        Child.prototype=new Person()
        Child.prototype.constructor=Child
        var child1=new Child('zhangsan','13')
        console.log(child1)
        child1.showName()

    </script>
</body>
</html>
```







#### 构造函数继承

```javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script>    
        function Person(name,age){
            this.name=name
            this.age=age
        }
        var person1=new Person('zhangsan','12')

        function Child(name,age,sex){
            //如果直接调用Person函数,this执行window,所以借助call方法使this指向实例对象
            Person.call(this,name,age)
            this.sex=sex
        }

        var child1=new Child('lisi','13','男')
        console.log(child1)
    </script>
</body>
</html>
```









### 线程机制与事件机制



#### 进程和线程

```
进程: 程序的一次执行,它占有一片独有的内存空间
线程: CPU的基本调度单位,是程序执行的一个完整的流程


一个进程中一般至少有一个线程: 主线程
一个进程中可以同时运行多个线程,我们会说程序是多线程运行的
一个进程内的数据可以供其中多个线程直接共享
多个进程之间的数据是不能直接共享的
```







#### 浏览器内核

```
什么是浏览器内核
	支持浏览器运行的最核心的程序
	
	
内核由很多模块组成
	htm,css文档解析模块: 负责页面文本的解析
	dom/css模块: 负责dom/css在内存中的相关处理
	布局和渲染模块: 负责页面的布局和效果的绘制
	定时器模块: 负责定时器的管理
	网络请求模块: 负责服务器请求
	事件响应模块: 负责事件的管理
```







#### js是单线程的

```
js代码的分类
	同步代码
		1. 同步会阻塞代码的执行
		2. 同步没有回调
	异步代码
		1. 异步是非阻塞的
		2. 异步有回调
		
		
先执行同步代码,再执行异步代码
```









#### 事件循环机制

```
事件循环(轮询)机制
	1. JS任务都会在JS的主线程执行
	2. 当开启一个异步任务的时候会交给对应的管理模块取管理
	3. 主线程继续执行后续代码
	4. 管理模块接收的对应的回调,它会在恰当的时机将对应的回调放入callback queue中
	5. 当主线程上的所有同步任务执行完毕后通过"轮询"的方式询问callback queue是否有可执行的回调
    6. 假如没有会反复询问
    7. 假如有可执行的回调将对应的回调钩到主线程执行
```























## ES5_6_7

```
ECMA
他是一种由ECMA组织(前身为欧洲计算机制造商协会)制定和发布的脚本语言规范
而我们学的JavaScript是ECMA的实现,ECMAScript和JavaScript平时表达同一个意思
js包含三个部分:
	1. ECMAScript(核心)
	2. 浏览器端
		* BOM(浏览器对象模型)
		* DOM(文档对象模型)
	3. 服务器
		* Node
		
ES的几个重要版本
	ES5: 09年发布
	ES6(ES2015): 15年发布,也称ECMA2015
	ES7(ES2016): 16年发布,也称ECMA2016(变化不大)
```







### ES5



#### 严格模式

```
 	理解
        除了正常运行模式(混杂模式),ES5添加了第二种运行模式: "严格模式" (strict mode)
        顾名思义,这种模式使得JavaScript在更严格的语法条件下运行

    目的
        消除JavaScript语法的一些不合理,不严谨之处,减少一些怪异行为
        消除代码运行的一些不安全之处,为代码的安全运行保驾护航
        为未来新版本的JavaScript做好铺垫

    使用
        在全局或函数的第一条语句定义为: 'use strict'
        如果浏览器不支持,直接洗为一条简单的语句,没有任何副作用

    语法和行为的改变
        必须用var申明变量(在之前定义变量时不需要写var也可以定义变量)
        禁止自定义的函数中的this执行window
        创建eval作用域
        对象不能有重命名的属性
```











#### Object扩展



**Object.create()**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 
        Object.create()方法
            第一个参数: 指定创建的对象的原型对象
            第二个参数: 可选参数,创建的对象的属性
                 每一个属性的值都必须为一个对象
                    value               值
                    writable            标识当前属性是否可以被修改,默认为false
                    configurable        标识当前属性是否可以被删除,默认为false
                    enumerable          标识当前属性是否可以for...in 枚举,默认为false

     -->
    <script  type="text/javascript">
        var obj={
            name:'kebi',
            showName:function (){
                console.log(this.name)
            }
        }

        var obj2=Object.create(obj,{
            sex:{
                value:'男',
                enumerable:true
            },
            age:{
                value:19,
                enumerable:true
            },
            showAge:{
                value: function (){
                    console.log(this.age)
                },
                enumerable:true
            }
        })

        //for in 枚举对象的时候除了能够枚举自身的属性外,还可以枚举原型的属性
        //所以最好是配合hasOwnProperty使用
        for (var i in obj2){
            //判断i是否是对象obj2自身上的属性(不包括原型对象)
            if(obj2.hasOwnProperty(i)){
                console.log(i)
            }
        }
    </script>
</body>
</html>
```









**Object.defineProperties()**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script>
        var obj={
            name:'kebe',
            age:32
        }

        Object.defineProperties(obj,{
            sex:{
                get:function (){        //获取,get方法的作用: 提供扩展属性的值
                    console.log('get方法被调用')
                    return '男'
                },
                set: function (msg){       //设置,
                    //如果扩展属性一旦被修改set方法就会被调用,并且会自动将修改之后的属性值作为形参传入到函数内部
                    console.log('sex属性被修改,值为',msg)
                }
            }
        })  
        console.log(obj.sex)                //当我们获取扩展属性的值时,get方法就会被调用
        console.log(obj.sex)
        console.log(obj.sex)               
        obj.sex='123'                        //当修改扩展属性值时,会被调用
    </script>
</body>
</html>
```











#### 数组扩展

```
Array.prototype.indexof()			//得到值在数组中的第一个下标
Array.prototype.lastIndexof()			//得到值在数组中的最后一个下标
Array.prototype.forEach(function (tiem,index){})			遍历数组
Array.prototype.map(function (tiem,index){})				遍历数组后返回一个新的数组,返回加工后的值(原数组不会改变)
Array.prototype.filter(function (tiem,index){})				加工过滤数组中的值,返回,原数组不变

```













### ES6





#### let

```
let的作用
    1. 不能重复申明
    2. 会预处理,有变量提升,但是不能提前使用提升的变量
    3. 会创建块级作用域(用于遍历)

    let变量提升:
        全局变量提升:
        会创建一个变量对象(script)用来收集全局作用域下let定义的变量,但是没有赋值
        局部变量提升:
        会将var let定义的变量全部放到当前函数的变量对象中

    同var的变量提升的区别
        let提升的变量在未赋值前不允许被使用
```







#### const

```
定义一个常量
	无法被修改
	其他和let定义的变量一样
```









#### 变量的结构赋值

```
理解: 
	从对象或数组上提取数据,并赋值给变量(多个)

用途:
	多个形参赋值
```

```JavaScript
console.log('----------对象的结构赋值----------')
let obj={name:'laijiandong',age:19,sex:'男'}
let {name,age}=obj          //结构赋值真正实现的是: 按需索取
console.log(name,age)

console.log('----------数组的结构赋值----------')
let arr=[1,2,3,4,5,6]
let [a,b,,,c,d]=arr           //根据index获取value
console.log(a,b,c,d)


console.log('----------结构赋值的应用----------')
function fun({name,age}){
    console.log(name)
    console.log(age)
}
fun(obj)
```









#### 模板字符串

```
作用: 简化字符串的拼接
```



```JavaScript
 let obj={name:'laijiandong',age:13}
 let str='我的名字是'+obj.name+','+'我的年龄为'+obj.age          //字符串拼接
 console.log(str)

let str1=`我的名字是${obj.name},我的年龄为${obj.age}`           //模板字符串拼接
console.log(str1)
```









#### 简化的对象写法

```JavaScript
console.log('---------------对象的基本写法------------------')
let name='赖建东'
let age=18
let obj={
    name:name,
    age:age,
    showName:function (){
        console.log(this.name)
    }
}
console.log(obj)

console.log('---------------对象的简写写法------------------')
let obj1={
    name,       //同名的属性可省略
    age,
    showName1(){            //省略函数的function和:
        console.log(this.name)
    }
}
console.log(obj1)
```









#### 箭头函数

```
箭头函数的特点
	1. 简洁
	2. 箭头函数没有自己的this,箭头函数的this不是调用的时候决定的,而是在定义的时候处在的上下文对象
	3. 扩展理解:
		箭头函数的this看外层是否有函数
		如果有,外层函数的this就是内部箭头函数的this
		如果没有,this就是window
```











#### ...运算符

```JavaScript
        console.log('-------------用途1: rest可变参数-----------------')
        function fun(a,...values){
            //arguments用来收集实参的伪数组
            //伪数组: 有length属性,可以通过下摆哦获取对应的值,但是没有数组的一般方法(push filter map)
            console.log(arguments)

            //它比形参更加灵活,可以传入多个形参,而且values是一个数组
            console.log(values)
        }
        fun(1,2,3)



        console.log('-------------用途1: 扩展运算符-----------------')
        let arr=[1,6]
        let arr2=[2,3,4,5]
        let arr3=[1,...arr2,6]
        console.log(arr3)           //[1,2,3,4,5,6]
        //...运算符去拆包指定数组
        console.log(...arr3)
```













#### 形参默认值

```javascript
        function Point(x=0,y=0){
            this.x=x
            this.y=y
        }   
        
        let ponit1=new Point(100,200)
        console.log(ponit1)

        let ponit2=new Point()
        console.log(ponit2)
```









#### Symbol









#### class

````html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 
        1. 通过class定义类/实现类的继承
        2. 在类中通过constructor定义构造方法
        3. 通过new来创建类的实例
        4. 通过extends来实现类的继承
        5. 通过super调用父类的构造方法
        6. 重写从类中继承的一般方法
     -->
    <script  type="text/javascript">
        console.log('----------定义类-------------')
        class Person{
            //静态资源修饰符,可以给类自身添加属性
            static num=123
            //类的构造方法
            constructor(name,age){
                this.name=name
                this.age=age
            }
            //类的一般方法(放在实例对象的原型对象上)
            showInfo(){
                console.log(this.name,this.age)
            }
        }

        /*
            给类自身添加属性
                方法1: 在类的外面通过基本方法添加属性
                方法2: 在类中给属性前面添加static
        */
        Person.msg='Person自身的属性'
        console.log(Person.msg)

        //使用类
        let person1=new Person('zhangsan',12)
        console.log(person1.showInfo())



        console.log('----------实现类的继承: extends-------------')
        //让子类的原型成为父类的实例
        //正常情况下: 子类的实例 ------> 子类的原型对象 ------> object原型对象
        //继承情况下: 子类的实例 ------> 子类的原型对象 ------> 父类的原型对象 -------> object原型对象
        class Child extends Person{
            constructor(name,age,sex){
                //super做的事情:      1.调用父类的构造方法       2.改变父类构造方法this指向为子类的实例
                super(name,age);        
                this.sex=sex        
            }
            //父类方法重写: 当父类的方法不能满足子类实例的需求时
            showInfo(){
                console.log(this.name,this.age,this.sex)
            }
        }
        let child1=new Child('lisi','14','男')
        console.log(child1)
        child1.showInfo()

    </script>
</body>
</html>
````





#### 扩展

````
字符串扩展
	string.includes(str)			判断指定字符串中是否包含指定片段
	string.startWith(str)			判断指定字符串是否以指定片段开头
	string.endWith(str)				判断指定字符串是否以指定片段结尾
	string.repeat(str)				判断指定片段在指定字符串中的重复次数
````





```
数值扩展
	Number.isNaN(i)					判断i是否是nan
	Number.isInteger(i)				判断是否是整数
	Math.trunc(i)					去除小数部分
```





```
数组扩展
	Array.from(v)					将伪数组转换为真数组
	Array.of(v1,v2,v3)				将一系列值转换为数组
	
```





```
对象扩展
	Object.assign
```

```
合并对象


const target = { a: 1, b: 2 };
const source = { b: 4, c: 5 };

const returnedTarget = Object.assign(target, source);

console.log(target);
// expected output: Object { a: 1, b: 4, c: 5 }

console.log(returnedTarget);
// expected output: Object { a: 1, b: 4, c: 5 }

```





```
set和map数据结构
	set容器: 无序的不可重复的多个value的集合体
	map容器: 无序的key不重复的多个key-value的集合体
	
	使用
		let a=new Set([1,2,3,4,65])
		let a=new map([1,2,3,4,65])
        
    方法
    	add,delete,clear,has,size
```





```
for...of
	1. 遍历数组
	2. 遍历set
	3. 遍历map
	4. 遍历字符串
	5. 遍历伪数组
```

























## JQuery



### 初识jQuery



```
什么是jQuery？
	一个优秀的js函数库
	中大型web项目开发首选
```

```
jQuery的好处
	HTML元素选取(选择器)
	HTML元素操作
	CSS操作
	HTML事件处理
	JS动画效果
	链式调用
	读写合一
	浏览器兼容
	易扩展插件
	ajax封装
    .....
```

```
如何使用jQuery
	引入jQuery库
```







### jquery的两把利器





#### jquery核心函数

```
$ 或 jQuery
	
```

```
jquery对象是一个伪数组对象
```









### jquery常用方法

```
trim()			去除字符串两端的空格
	用法：$.trim(指定字符串)
```



```
 var arr=[12,34,2,5,1]
            // each 相当于原生中的forEach
            $.each(arr,function (index,value){
                console.log(index,value)
            })
```



```
$.each			此时使用的是$，$为工具对象
$(button)		此时是将button的bom对象封装为jquery对象，和$.each不同，一个是工具对象，一个是jquery对象

```



```
$.type()				检查数据类型
$.isArray()				判断是否为数组
$.isFunction()			判断是否为函数
$.parseJSON()			解析json串，转换为对象/数组
```





````
静态方法
	保存在对象上的方法
	
	
实例方法
	保存在原型对象上的方法
````





### jquery中的静态方法

```
1. each
	可以遍历数组和伪数组,由于jquery对象是伪数组,所以不能使用forEach遍历,需要使用each遍历
	
	
2. map
	和each一样,既可以遍历数组,也可以遍历伪数组
	map和each的区别:
		默认情况下,each返回当前遍历的数组,map返回一个空数组
		each不支持在回调函数中对遍历的数组进行处理
		map通过return对遍历的数组进行处理,然后返回一个新的数组
		所以,each用于遍历,map用于加工
		
        
3. trim
	去除字符串左右的空格
	
	
4. isWindow
	判断传入的对象是否是window对象
	
	
5. isArray
	判断传入的对象是否是真数组,伪数组为false
	
	
6. isFunction
	判断传入的对象是否是函数
	
	
7. holdReady
	是否暂停ready事件的执行
		传入false,不暂停ready事件的执行
		传入true,暂停ready事件的执行
```









### jquery选择器

```
 			// 选择id为div1的元素
            $('#div1').css('background','pink')

            // 选择所有div元素
            $('div').css('background','yellow')

            // 选择所有class属性为box的元素
            $('.box').css('background','red')

            // 选择所有div和span元素
            $('div,span').css('background','blue')

            // 选择所有class属性为box的div属性
            $('div.box').css('background','red')

            // 选择ul下所有标签
            $('ul span')

            // 选择第一个div
            $('div:first').css('background','pink')

            // 选择最后一个div
            $('div:last').css('background','pink')

            // 选择所有class属性不为box的div
            $('div:not(.box)').css('background','yellow')

            // 选择第一个和第二个li元素
            // gt:选择下标大于0的所有元素
            // lt:选择下标小于2的所有元素
            // 当我们使用gt将大于0的元素提取后，大于0的元素的下标要减去1，然后再使用lt去提取
            $('li:gt(0):lt(2)').css('background','red')

            // 列出内容为BBBBB的元素
            $('li:contains(BBBBB)').css('background','blue')

            // 选择所有隐藏的li
            $('li:hidden').css('background','red')
```



| 选择器                                                       | 实例                       | 选取                                       |
| ------------------------------------------------------------ | -------------------------- | ------------------------------------------ |
| [*](selector_all.asp.htm)                                    | $("*")                     | 所有元素                                   |
| [#*id*](selector_id.asp.htm)                                 | $("#lastname")             | id="lastname" 的元素                       |
| [.*class*](selector_class.asp.htm)                           | $(".intro")                | 所有 class="intro" 的元素                  |
| [*element*](selector_element.asp.htm)                        | $("p")                     | 所有 <p> 元素                              |
| .*class*.*class*                                             | $(".intro.demo")           | 所有 class="intro" 且 class="demo" 的元素  |
|                                                              |                            |                                            |
| [:first](selector_first.asp.htm)                             | $("p:first")               | 第一个 <p> 元素                            |
| [:last](selector_last.asp.htm)                               | $("p:last")                | 最后一个 <p> 元素                          |
| [:even](selector_even.asp.htm)                               | $("tr:even")               | 所有偶数 <tr> 元素                         |
| [:odd](selector_odd.asp.htm)                                 | $("tr:odd")                | 所有奇数 <tr> 元素                         |
|                                                              |                            |                                            |
| [:eq(*index*)](selector_eq.asp.htm)                          | $("ul li:eq(3)")           | 列表中的第四个元素（index 从 0 开始）      |
| [:gt(*no*)](selector_gt.asp.htm)                             | $("ul li:gt(3)")           | 列出 index 大于 3 的元素                   |
| [:lt(*no*)](selector_lt.asp.htm)                             | $("ul li:lt(3)")           | 列出 index 小于 3 的元素                   |
| :not(*selector*)                                             | $("input:not(:empty)")     | 所有不为空的 input 元素                    |
|                                                              |                            |                                            |
| [:header](selector_header.asp.htm)                           | $(":header")               | 所有标题元素 <h1> - <h6>                   |
| [:animated](selector_animated.asp.htm)                       |                            | 所有动画元素                               |
|                                                              |                            |                                            |
| [:contains(*text*)](selector_contains.asp.htm)               | $(":contains('W3School')") | 包含指定字符串的所有元素                   |
| [:empty](selector_empty.asp.htm)                             | $(":empty")                | 无子（元素）节点的所有元素                 |
| :hidden                                                      | $("p:hidden")              | 所有隐藏的 <p> 元素                        |
| [:visible](selector_visible.asp.htm)                         | $("table:visible")         | 所有可见的表格                             |
|                                                              |                            |                                            |
| s1,s2,s3                                                     | $("th,td,.intro")          | 所有带有匹配选择的元素                     |
|                                                              |                            |                                            |
| [[*attribute*\]](selector_attribute.asp.htm)                 | $("[href]")                | 所有带有 href 属性的元素                   |
| [[*attribute*=*value*\]](selector_attribute_equal_value.asp.htm) | $("[href='#']")            | 所有 href 属性的值等于 "#" 的元素          |
| [[*attribute*!=*value*\]](selector_attribute_notequal_value.asp.htm) | $("[href!='#']")           | 所有 href 属性的值不等于 "#" 的元素        |
| [[*attribute*$=*value*\]](selector_attribute_end_value.asp.htm) | $("[href$='.jpg']")        | 所有 href 属性的值包含以 ".jpg" 结尾的元素 |
|                                                              |                            |                                            |
| [:input](selector_input.asp.htm)                             | $(":input")                | 所有 <input> 元素                          |
| [:text](selector_input_text.asp.htm)                         | $(":text")                 | 所有 type="text" 的 <input> 元素           |
| [:password](selector_input_password.asp.htm)                 | $(":password")             | 所有 type="password" 的 <input> 元素       |
| [:radio](selector_input_radio.asp.htm)                       | $(":radio")                | 所有 type="radio" 的 <input> 元素          |
| [:checkbox](selector_input_checkbox.asp.htm)                 | $(":checkbox")             | 所有 type="checkbox" 的 <input> 元素       |
| [:submit](selector_input_submit.asp.htm)                     | $(":submit")               | 所有 type="submit" 的 <input> 元素         |
| [:reset](selector_input_reset.asp.htm)                       | $(":reset")                | 所有 type="reset" 的 <input> 元素          |
| [:button](selector_input_button.asp.htm)                     | $(":button")               | 所有 type="button" 的 <input> 元素         |
| [:image](selector_input_image.asp.htm)                       | $(":image")                | 所有 type="image" 的 <input> 元素          |
| [:file](selector_input_file.asp.htm)                         | $(":file")                 | 所有 type="file" 的 <input> 元素           |
|                                                              |                            |                                            |
| [:enabled](selector_input_enabled.asp.htm)                   | $(":enabled")              | 所有激活的 input 元素                      |
| [:disabled](selector_input_disabled.asp.htm)                 | $(":disabled")             | 所有禁用的 input 元素                      |
| [:selected](selector_input_selected.asp.htm)                 | $(":selected")             | 所有被选取的 input 元素                    |
| [:checked](selector_input_checked.asp.htm)                   | $(":checked")              | 所有被选中的 input 元素                    |







#### attr

```
  	     // attr
        //    输入一个参数为读
        //    输入两个参数为写
        
        // attr     用来操作标签自定义属性，比如title，class，id，name
        // prop     用来操作元素固有属性  布尔值属性
        $(function (){
            // 读取第一个div的title值
            console.log($('div:first').attr('title'))
            // 给所有div设置一个name属性，值为gege
            $('div').attr('name','gege')
            // 删除所有div的title属性
            $('div').removeAttr('title')
            // 给所有div设置一个class属性，值为box
            $('div').attr('class','box')
            // 给所有div添加一个class属性，值为box1
            $('div').addClass('box1')
            // 移出所有div的class属性，值为box
            $('div').removeClass('box')
            // 查看最后一个li的文本
            console.log($('ul>li:last').html())
            // 设置第一个li的文本为zzzzzz
            $('ul>li:first').html('<h1>zzzzzz</h1>')

            // 全选
            $('button:first').click(function (){
                $(':checkbox').prop('checked',true)
            })
            // 全不选
            $('button:last').click(function (){
                $(':checkbox').prop('checked',false)
            })
```









#### attr

```
传入一个参数,获取
    无论找到多少个元素,都会返回第一个元素指定的属性节点的值
传入两个参数,设置
	无论找到多少个元素,都会设置
	如果设置的元素上指定的属性节点不存在,新增
```





#### removeAttr

```
删除指定属性节点
```





#### prop和removeProp

```
prop
	和arrt方法一致
	
	
removeProp
	和removeProp方法一致
	
	
	
注意:
	prop不仅可以操作属性节点,也可以操作属性
	attr只能操作属性节点
	
	
	
如果操作的属性节点值为布尔值,建议使用prop,否则使用attr
```





#### 类方法

```
addClass('class1 class2 class3')		添加
	
removeClass('class1 class2 class3')		删除

toggleClass('class3')					切换(有就删除,无则添加)
```







#### 文本值

```
html		传入参数设置,不传获取,和innerHTML一样
text		和innerText一样
val			获取和设置文本框的内容
```











#### css

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <script type="text/javascript" src="../jquery-1.10.1.js"></script>
</head>
<body>
    <p style="color: red">aaaaaaaa</p>
    <p style="color: blue">bbbbbbbb</p>

    <script type="text/javascript">
        // 得到第一个p标签的颜色
        console.log($('p:first').css('color'))

        // 设置所有p标签的颜色为pink
        $('p').css('color','pink')

        // 设置第2个字体颜色为(#ff0011)，背景为(blue)，宽(300px)，高(30px)
        $('p:last').css({
            // 传入的是一个对象
            'color':'#ff0011',
            'backgroundColor':'blue',
            'width':'300px',
            'height':'30px'
        })
    </script>
</body>
</html>
```









#### offset和position

```
offset			获取相对于页面左上角的坐标

position		获取相对于父元素左上角的坐标，只对可见元素有效
```



















#### scrollTop

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <script src="../jquery-1.10.1.js"></script>
</head>
<body style="height: 2000px">
    <div id="box" style="border: 1px solid black;width: 100px;height: 150px;overflow: auto">
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text
        this is some text

    </div>

    <button id="btn1">得到scrollTop</button>
    <button id="btn2">设置scrollTop</button>

    <script>
        // 获取指定盒子移动的距离
        $('#btn1').click(function (){
            console.log($('#box').scrollTop())
            // 在Chrome浏览器中，$('body').scrollTop()无法测出值，但是$('html').scrollTop()可以
            // 在ie浏览器中，$('html').scrollTop()无法测出值，但是$('body').scrollTop()可以
            // 兼容写法
            console.log($('body').scrollTop()+$('html').scrollTop())

            // 如果jquery版本新，可以使用document
            console.log($('document').scrollTop())

        })

        //
        $('#btn2').click(function (){
            $('#box').scrollTop(300)

            // 处理兼容
            $('html,body').scrollTop(500)
            //$('body').scrollTop(500)

            // 如果jquery版本新，可以使用document
            $('document').scrollTop(500)
        })
    </script>
</body>
</html>
```









#### 元素的尺寸

```
$('div').width()			获取元素的宽度

$('div').height()			获取元素的高度

$('div').innerHeight()		获取指定元素的内部尺寸(height + padding)

$('div').innerWidth()		获取指定元素的内部尺寸(width + padding)

$('div').outerHeight(true/false)		获取指定元素的内部尺寸(height + padding + border),如果是true，加margin

$('div').outerWidth(true/false)			获取指定元素的内部尺寸(width + padding + border),如果是true，加margin
```













### 筛选

```
$('ul li').first()			获取指定元素的第一个

$('ul li').last()			获取指定元素的最后一个

$('ul li').eq(1)			获取指定元素的第二个

$('ul li').filter('[title=hello]')			获取指定元素title属性为hello的元素

$('ul li').has('span')		获取指定元素中含有sapn标签的li元素
```







```
$('ul').children('span:eq(1)')			获取ul下的第二个span元素(必须是子元素)

$('ul').find('span:eq(1)')				获取ul下的第二个span元素(后代元素)

$('ul').parent()						获取ul的父元素
```













### 文档处理

```
向id为ull的元素内添加一个span(最后，追加)
1.    $('#ull').append('<span>aaaaa</span>')
2.    $('<span>aaaaa</span>').appendTo('#ull')


向id为ull的元素内添加一个span(最前面，第一个)
1.    $('#ull').prepend('<span>aaaaa</span>')
2.    $('<span>aaaaa</span>').】prependTo('#ull')


在id为ull的ul中li的title属性为hello的前面添加一个span
$('#ull>li[title=hello]'.before('<span>aaaaa</span>'))


在id为ull的ul中li的title属性为hello的后面添加一个span
$('#ull>li[title=hello]'.after('<span>aaaaa</span>'))


将id为ull的ul中li的title属性为hello全部替换为span
$('#ull>li[title=hello]').replaceWith('<span>aaaaa</span>')


删除id为ull的ul下的所有元素
$('#ull').remove()			删除节点，不仅将ul下的所有元素删除，连ul也被删除
$('#ull').empty()			掏空节点，删除指定元素的所有子元素



```









#### 取反

```
a=!a
```









### 事件绑定和解绑

```
给.out绑定点击事件
	1.	$('.out').click(funvtion(){
		console.log('我是click绑定的单击回调')
	})
	
	2.	$('.out').on('click',function(){
		console.log('我是click绑定的单击回调')
	})
	


给.inner绑定鼠标移入移出的事件
	1.	$('.inner').on('mouseenter',function(){
			console.log('我是移入')
	}).on('mouseleave',function(){
			console.log('我是移出')
	})
	
	2.	$('.inner').on('mouseover',function(){
			console.log('我是移入')
	}).on('mouseout',function(){
			console.log('我是移出')
	})
	
	
	hover		当传入一个回调函数时，该回调函数执行的都是移入移出事件
				当传入两个回调函数时，第一个回调函数执行移入事件，第二个回调函数执行移出事件
	3.$('.inner').hover(function(){
		console.log('移入')
	},function(){
		console.log('移出')
	})
	
	

点击btn1解除.inner上所有事件
	$('.btn1').click(function(){
		$('.inner').off()
	})
	

点击btn2解除.inner上的mouseover事件和click事件
	$('.btn2').click(function(){
		$('inner').off('mouseover click')
	})
```



```
on可以一次绑定多个事件，必须注意，多个事件执行的回调函数内容必须一样
	$('.btn').on('click mouseover',function(){
			console.log('绑定点击和移入事件')
	})
```



```
mouseenter、mouseleave 和 mouseover、mouseout 的区别

	mouseenter、mouseleave
		当鼠标移入指定元素的子元素时，不会发生事件
		
	mouseover、mouseout
		当鼠标移入指定元素的子元素时，会再次触发事件
```









### 事件委托

```
事件委托
	1.将多个子元素(li)的事件监听委托给父辈元素或祖先元素
	2.监听回调是加在父辈元素上
	3.当操作任何一个子元素(li)时，事件会冒泡给父辈元素(ul)
	4.父辈元素不会直接处理事件，而是根据event，target得到发生事件的子元素(li)，通过这个子元素调用事件回调函数
```



```
绑定事件委托的两种方法
	1.delegate
		第一个参数：指定发生事件的子元素
		第二个参数：事件类型
		第三个参数：回调函数
		
            $('ul').delegate('li','click',function (){
                 $(this).css('backgroundColor','red')
             })
             
             
             
             
	2.on
		第一个参数：事件类型
		第二个参数：指定发生事件的子元素
		第三个参数：回调函数
		
			 $('ul').on('click','li',function (){
        		$(this).css('backgroundColor','red')
   			 })
```



```
解绑事件委托的方法
	undelegate
		$('button:last').click(function (){
        	$('ul').undelegate()
   		 })
   		 
   	注意：undelegate 可以解绑 delegat 和 on 绑定的事件委托
```



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <script src="../jquery-1.10.1.js"></script>
</head>
<body>
<ul>
    <li>11</li>
    <li>22</li>
    <li>33</li>
</ul>
<button>添加新的li</button>
<button>删除ul上的事件委托的监听器</button>

<script>
    var $btn1=$('button:first')

    // 新增li
    $btn1.click(function (){
        $('<li>我会新增的li</li>').appendTo($('ul'))
    })

    // 点击li使li变为红色
    // $('ul').delegate('li','click',function (){
    //     $(this).css('backgroundColor','red')
    // })

    $('button:last').click(function (){
        $('ul').undelegate()
    })

    $('ul').on('click','li',function (){
        $(this).css('backgroundColor','red')
    })

</script>
</body>
</html>
```









### 动画





#### 淡入和淡出

```
fadeOut			淡出
fadeIn			淡入
fadeToggle		淡入淡出切换，当指定元素存在时，点击淡出，再点击淡入


注意：指定元素淡出后不会继续在页面中占据位置
```







#### 展开和收缩

```
slideUp			收缩
slideDown		展开
slideToggle		收缩展开切换

注意：指定元素收缩后不会继续在页面中占据位置
```







#### 显示和隐藏

```
show		显示
hide		隐藏
toggle		显示隐藏切换

注意：指定元素隐藏后不会继续在页面中占据位置
```







#### 自定义动画

```
animate
```



```
停止动画		stop

$('div').stop()				停止当前动画，在当前位置执行下一次动画，不清空队列
$('div').stop(true,true)	立即停止动画，并且元素运动到最终位置，清空队列
$('div').stop(false,true)	结束当前动画，元素运动到当前动画最终位置，不清空队列
$('div').stop(true,fasle)	立即结束动画，元素停留在当前位置，清空队列

	第一个参数：是否清空队列，默认false
	第二个参数：当前动画是否执行完，默认false
```

























## Bootstarp



### 模板

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- 上述3个meta标签*必须*放在最前面，任何其他内容都*必须*跟随其后！ -->
    <title>Bootstrap 101 Template</title>

    <!-- Bootstrap -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@3.3.7/dist/css/bootstrap.min.css" rel="stylesheet">

    <!-- HTML5 shim 和 Respond.js 是为了让 IE8 支持 HTML5 元素和媒体查询（media queries）功能 -->
    <!-- 警告：通过 file:// 协议（就是直接将 html 页面拖拽到浏览器中）访问页面时 Respond.js 不起作用 -->
    <!--[if lt IE 9]>
    <script src="https://cdn.jsdelivr.net/npm/html5shiv@3.7.3/dist/html5shiv.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/respond.js@1.4.2/dest/respond.min.js"></script>
    <![endif]-->
</head>
<body>
<h1>你好，世界！</h1>
<a href="">aaa</a>

<!-- jQuery (Bootstrap 的所有 JavaScript 插件都依赖 jQuery，所以必须放在前边) -->
<script src="https://cdn.jsdelivr.net/npm/jquery@1.12.4/dist/jquery.min.js"></script>
<!-- 加载 Bootstrap 的所有 JavaScript 插件。你也可以根据需要只加载单个插件。 -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@3.3.7/dist/js/bootstrap.min.js"></script>
</body>
</html>
```







### 全局CSS样式





#### 布局容器

`.container` 类用于固定宽度并支持响应式布局的容器。

```
		阈值  					width
	大于等于1200				   1170px
	大于等于992					   970px
	大于等于768						750px
	小于768						auto(屏幕的宽度-padding(左右15px))
```

```
<div class="container">
  ...
</div>
```



`.container-fluid` 类用于 100% 宽度，占据全部视口（viewport）的容器。

```
<div class="container-fluid">
  ...
</div>
```











#### 栅格系统



















#### 自定义快捷键

```
1.打开设置
2.搜索live
3.选择右上角的+
4.选择第一个
5.输入关键字，以及对应的内容，选择生效的文件
6.点击apply
7.点击ok
```

![2020-11-21_214002](C:\Users\86188\Desktop\2020-11-21_214002.png)











#### holder.js    图片占位插件

```
1.引入文件
<script src="https://cdn.bootcss.com/holder/2.9.6/holder.min.js"></script>

2.img标签的src中填写特定的路径，显示图片

```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <script src="https://cdn.bootcss.com/holder/2.9.6/holder.min.js"></script>
</head>
<body>
<div style="width: 300px;height: 300px;margin: 100px auto">
    <img src="holder.js/100px300?text=书籍" alt="">
</div>
</body>
</html>
```

















































## 移动端





### 屏幕相关





#### 屏幕大小

```
屏幕的大小指的是对角线的长度，单位为英寸

注意：
	1.英寸的inch，英尺为foot
	2.1foot=12inch
		1inch=2.54cm
```







#### 屏幕分辨率

```
屏幕分辨率是指屏幕横纵向上的像素点数，一般表示为x*y或者y*x
```









### 像素相关





#### 物理像素/设备像素

```
一个物理像素对应显示设备中一个微小的物理部件(像素点)
```









#### 设备独立像素

```
设备独立像素也是手机屏幕的一个参数，我们可以通过程序来控制设备独立像素

设备独立像素的出现，使得即使在高清屏下，也可以以正常的尺寸显示元素，代码不受到设备的影响
```









#### CSS像素

```
css像素不能直接跟现实中的长度单位换算
css像素主要用于css和js中控制元素的大小和位置
```











#### 位图像素

```
位图图像：是由一个个像素点构成的，放大后会失帧

矢量图：在数学上定位为一个系列由线连接的点，放大后不会失帧


一个位图像素等于一个物理像素，图像才能完美的显示
```







####  像素之间的关系

```
页面不缩放的情况下
	CSS像素==独立 设备像素==逻辑像素==DIP(设备独立像素)==位图像素
	
	
一个标准的显示密度下(普通屏)，一个CSS像素对应着一个设备像素
高清屏幕下，一个CSS像素等于N个物理像素
```



```
iPhone 6 
设备像素	750*1334
设备独立像素	375*667
ppi			326
```







#### 像素比

```
DDR：单一方向上设备物理像素和设备独立像素的比列

window.devicePixelRatio
打印比例
```





````
不加上他<meta name="viewport" content="width=device-width, initial-scale=1.0">,
一个css像素 === 一个物理像素 === 0.5个设备独立像素
加上他<meta name="viewport" content="width=device-width, initial-scale=1.0">,
一个css像素 === 一个设备独立像素 === 2个物理像素
````





### 视口

````
移动端视口和PC端的视口不同
	1.布局视口
	2.视觉视口
	3.理想视口
````





#### 布局视口

```
用来放置网页内容的区域

获取方式
document.documentElement.clientWidth
document.documentElement.clientHeight
```





#### 视觉视口

```
window.innerWidth
window.innerHeight

在不缩放的情况下，视觉视口==布局视口
```





#### 理想视口

```
宽度和屏幕同宽

	1.用户不需要缩放和滚动条就可以看到网页的全部
	2.更加方便
```

```
设置理想视口

	方法1：<meta name="viewport" content="width=device-width">
	方法2：<meta name="viewport" content="initial-scale=1.0">
```







### 缩放

```
PC端时，布局视口和视觉视口发生变化
移动端时，布局视口不变，视觉视口发生变化
```









### 真机测试流程

```
1.关闭防火墙
```

![1](C:\Users\86188\Pictures\真机测试流程\1.png)

```
2.使手机和电脑连接同一个WiFi
3.更改端口
```

![2](C:\Users\86188\Pictures\真机测试流程\2.png)



```
4.cmd中查看电脑的ip
5.将localhost改为ip地址
6.将地址转换为二维码，手机扫码
```













### viewport控制

```
用于移动端布局视口的控制
```

```
width						布局视口宽度
initial-scale				初始化缩放比列
minimum-scale				最小缩放比列
maximum-scale				最大缩放比列
user-scalable				设置是否允许用户缩放
viewport-fit	auto/contain/cover

scale
	设备独立像素/布局视口宽度=scale
	当布局视口的宽度为375时,如果将initial-scale设置为1.0,那么设备独立像素的数目也为375,那么每一个设备独立像素==980/375个物理像素,当我们设置一个100px宽度的元素时,100px == 100*(980/375)个物理像素
```







### 移动端事件

```
touchstart			元素上触摸开始时触发
touchmove			元素上触摸移动时触发
touchend			手指从元素上离开时触发
touchcancel			触摸被打断时触发
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <title>Title</title>
    <style>
        *{
            padding: 0;
            margin: 0;
        }
        #box{
            width: 200px;
            height: 200px;
            background-color: #ccc;
        }
    </style>
</head>
<body>
<div id="box"></div>
<script>
    var box=document.getElementById('box');
    box.addEventListener('touchstart',function () {
        box.style.backgroundColor='red';
    });
    box.addEventListener('touchmove',function () {
        box.style.backgroundColor='yellow';
        box.innerHTML=Math.round(Math.random()*100);
    });
    box.addEventListener('touchend',function () {
        box.style.backgroundColor='#abf';
    });

    // 当触摸被打断时触发的事件(比如来电话时)
    box.addEventListener('touchcancel',function () {
        box.style.backgroundColor='black';
    });

    setTimeout(function () {
        alert('aaaaa')
    },4000)
</script>
</body>
</html>
```







### 点击穿透

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">
    <script src="https://cdn.bootcss.com/holder/2.9.6/holder.min.js"></script>
    <title>Bootstrap 101 Template</title>
    <style>
        *{
            padding: 0;
            margin: 0;
        }
        ul{
            list-style: none;
        }
        .swiper{
            width: 80%;
            height: 100px;
            background-color: #999;
            margin: 0 auto;
        }
        .height-5{
            height: 50px;
        }
        #nav{
            width: 80%;
            height: 50px;
            margin: 0 auto;
            display: flex;
        }
        .item{
            overflow: hidden;
            width: 60px;
            height: 60px;
        }
        .item img{
            border-radius: 50%;
        }
        #zhezhao{
            width: 100%;
            height: 100%;
            position: absolute;
            top: 0;
            left: 0;
            background-color: #000;
            opacity: 0.5;
        }
        .content{
            color: white;
            width: 50%;
            height: 100px;
            margin: 200px auto;
            /*background-color: white;*/
            text-align: center;
            padding-top: 20px;
        }
    </style>
</head>
<body>
<div id="app">


<div class="height-5"></div>
<div class="height-5"></div>
<div class="swiper"></div>
<div class="height-5"></div>
<div id="nav">
    <div class="item"><a href="http://m.atguigu.com"><img data-src="holder.js/50x50" alt=""></a></div>
    <div class="item"><a href="http://m.atguigu.com"><img data-src="holder.js/50x50" alt=""></a></div>
    <div class="item"><a href="http://m.atguigu.com"><img data-src="holder.js/50x50" alt=""></a></div>
    <div class="item"><a href="http://m.atguigu.com"><img data-src="holder.js/50x50" alt=""></a></div>
    <div class="item"><a href="http://m.atguigu.com"><img data-src="holder.js/50x50" alt=""></a></div>

</div>

<div id="zhezhao">
    <div class="content">
        <div class="remind">充值成功</div>
        <button>关闭</button>
    </div>
</div>
</div>
</body>
<script>
    var btn=document.querySelector('button');
    var zhezhao=document.getElementById('zhezhao');
    btn.addEventListener('touchend',function (event) {
        //当我们点击按钮时,按钮下方的a标签的click事件也会触发
        zhezhao.style.display='none';
    //    阻止默认行为
    //    方法1
    //     event.preventDefault();
    });

    //方法2
    // document.documentElement.addEventListener('touchstart',function (e) {
    //     e.preventDefault();
    // },{
    //     // 第三个参数
    //     // 使e.preventDefault()生效,默认为true;
    //     passive:false
    // })

    // 方法3(建议使用)
//    在最外层添加一个包裹器
    var app=document.getElementById('app');
    app.addEventListener('touchstart',function (event) {
        event.preventDefault();
    })
    // 方法4
    // 将a标签去掉,通过js跳转到对应页面中
    
    // 方法5
    setTime(function(){
        zhezhao.style.display='none';
    },400);
</script>
</html>
```







### html中data-uri和data-href的属性有什么作用

```
定义和用法

data-* 属性用于存储页面或应用程序的私有自定义数据。

data-* 属性赋予我们在所有 HTML 元素上嵌入自定义 data 属性的能力。

存储的（自定义）数据能够被页面的 JavaScript 中利用，以创建更好的用户体验
（不进行 Ajax 调用或服务器端数据库查询）。

data-* 属性包括两部分：

属性名不应该包含任何大写字母，并且在前缀 "data-" 之后必须有至少一个字符
属性值可以是任意字符串

简单来说就是存储一些简单信息，然后可以通过js拿到这些信息，
像你说的data-url和data-href估计就是存储的真正的url和href，
可以通过js的element.dataset.url或JQ的data('url')拿到，然后进行相应操作
```

```
查看data属性
a.dataset.src

设置data属性
a.dataset.src=b
```











### 页面跳转的选择

```
方法1:使用a连接
方法2:使用js跳转

效率上,js快
SEO优化上,a标签效果更好
```







### 浏览器默认行为

```
1.滑动留白
2.页面缩放
```

```
阻止默认行为可以使网页在不同的浏览器中都是一样的表现
```

````
阻止默认行为的方法
	给document绑定touchstart事件,并阻止默认行为,不过需要关闭被动模式
	推荐创建一个包裹容器,绑定touchstart事件并阻止默认行为
````



**CSS代码**

```
html,body.#app{
	width:100%;
	height:100%;
	overflow:hidden;
}
```

**html代码**

```
<body>
	<div id="app">
	
	</div>
</body>
```

**js代码**

```
app.addEventListener('touchstart',function(event){
	event.preveDefault();
})
```





```
后遗症
	1.链接失效
	2.form表单无法获取焦点
	3.内容无法选择
```

```javascript
//解决方法
//阻止a标签冒泡,这样a标签就不会冒泡到包裹容器中,让包裹容器阻止
var a=document.querySelectorAll('a');
a.addEventListener('touchstart',function (event) {
        event.stopPropagation();
    })
```

```javascript
//文本和a标签一样
var p=document.querySelectorAll('p');
    p.addEventListener('touchstart',function (event) {
        event.preventDefault();
    })
```

```javascript
// 表单解决
// 方法1
var input=document.querySelectorAll('input[type="text"]');
    input.addEventListener('touchstart',function (event) {
        event.stopPropagation();
    })


// 方法2
var input=document.querySelectorAll('input[type="text"]');
    input.addEventListener('touchstart',function (event) {
        this.focus();
        event.stopPropagation();
    });
    app.addEventListener('touchstart',function (event) {
        input.blur();
    })
```











### 移动端事件属性

```
touch事件对象中有3个非常重要的属性
	1.changedTouches
	2.targetTouches
	3.touches
```





#### 在touchstart事件中

```
changedTouches为当前元素上同时按下的触点对象的数组,也就是当你的手指按在屏幕的数目,必须是同时按下
targetTouches为当前元素上的触点数目,而不是同时按下的触点数目
touches为当前屏幕上的所有触点的数目
```







#### 在touchmove事件中

```
changedtouches为在当前元素上同时滑动的触点对象的数组
targettouches为当前元素上滑动的触点对象
touches为屏幕上滑动的所有触点的数目
```







#### 在touchend事件中

```
changedtouches为同时抬起的触点对象
targettouches为在当前元素上抬起的触点对象的数目
touches为当前屏幕上抬起的触点对象的数目
```

```
获取手指离开元素上的位置只能使用changedTouches
```











### 适配



#### viewport适配

```
设置viewport  width等于设计稿的宽度即可
```

```
console.log(window.devicePixelRatio);
     设备物理像素/设备独立像素
console.log(document.documentElement.clientWidth);
```







#### rem适配

```
方法1
	1.完美视口设置
	2.设计稿总宽375布局
	3.设置font-size=100px尺寸转换为rem
	4.增加js代码进行页面适配
	
写元素的宽度更加简单,不需要计算器
```

```html
<!DOCTYPE html>
<html lang="en" style="font-size: 100px">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <meta name="viewport"
          content="width=device-width,user-scalable=no,initial-scale=1.0,maximum-scale=1.0,minimum-scale=1.0">
    <title>Title</title>
    <style>
        #box {
            width: 1.59rem;
            height: 0.89rem;
            margin-left: 0.21rem;
            margin-top: 2rem;
            background: #886;
        }
    </style>
</head>
<body>
<div id="box"></div>
</body>
<script>
    // // 获取布局视口的宽度
    // var width = document.documentElement.clientWidth;
    //
    // //    计算新的font-size
    // var x = width * 100 / 375;
    //
    // //    设置新的font-size
    // document.documentElement.style.fontSize = x + 'px';
    document.documentElement.style.fontSize = document.documentElement.clientWidth * 100 / 375 + 'px';

    //    当视口发生改变时
    window.onresize = function () {
        document.documentElement.style.fontSize = document.documentElement.clientWidth * 100 / 375 + 'px';

    }
</script>
</html>
```







```
方法2
	1.完美视口设置
	2.设计稿总宽375布局
	3.设置font-size,然后计算页面宽度和font-size的比例
	4.增加js代码进行页面适配
	
配合less使用效果更好
```

```html
<!DOCTYPE html>
<html lang="en" style="font-size: 37.5px">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <meta name="viewport"
          content="width=device-width,user-scalable=no,initial-scale=1.0,maximum-scale=1.0,minimum-scale=1.0">
    <title>Title</title>
    <style>
        #box {
            width: 4.24rem;
            height: 2.373rem;
            margin-left: 0.56rem;
            margin-top: 5.333rem;
            background: #886;
        }
    </style>
</head>
<body>
<div id="box"></div>
</body>
<script>
    document.documentElement.style.fontSize = document.documentElement.clientWidth / 10 + 'px';
    window.onresize=function () {
        document.documentElement.style.fontSize = document.documentElement.clientWidth / 10 + 'px';

    }
</script>
</html>
```





#### rem适配less



**html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <meta name="viewport"
          content="width=device-width,user-scalable=no,initial-scale=1.0,maximum-scale=1.0,minimum-scale=1.0">
    <link rel="stylesheet" href="css/app.css">
    <title>Title</title>
</head>
<body>
<div id="box"></div>
</body>
<script>
    document.documentElement.style.fontSize = document.documentElement.clientWidth / 10 + 'px';
    window.onresize=function () {
        document.documentElement.style.fontSize = document.documentElement.clientWidth / 10 + 'px';
    }
</script>
</html>
```



**less**

```less
*{
     padding: 0;
     margin: 0;
}
ul{
     list-style: none;
}

// 设计稿的宽度/10+rem
@rem:375/10rem;

#box{
  width: 335/@rem ;
  height: 144/@rem;
  margin: 50/@rem auto;
  background-color: #1b6d85;
}
```







``` 
适配的两种思路
	
	1.定值
	375/100 == 414/110.4
    
    2.定比例+less
   
```









### 1px边框问题

```
方法1
	设置伪类
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <meta name="viewport" content="width=device-width,user-scalable=no,initial-scale=1.0,maximum-scale=1.0,minimum-scale=1.0">
    <title>Title</title>
    <style>
        div{
            width: 150px;
            height: 150px;
            /*border-bottom: solid 1px #000;*/
            float: left;margin-right: 10px;
            position: relative;
        }
        #box1{
            border-bottom: solid 1px #000;
        }
        #box::after{
            position: absolute;
            content: '';
            left: 0;
            bottom: -1px;
            width: 100%;
            height: 1px;
            border-bottom: solid 1px #000;

        }
        @media (-webkit-device-pixel-ratio: 2) {
            #box::after{
                transform: scaleY(0.5);
            }
        }
        @media (-webkit-device-pixel-ratio: 3) {
            #box::after{
                transform: scaleY(0.333333);
            }
        }
    </style>
</head>
<body>
    <div id="box1"></div>
    <div id="box"></div>
</body>
</html>
```





```
方法2
	增大页面的宽度,增加内容的大小,边框依然使px
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <meta name="viewport" content="initial-scale=1">
    <title>Title</title>
    <style>
        #box{
            width: 3rem;
            height: 3rem;
            border: 1px solid #ccc;
        }
    </style>
</head>
<body>
<div id="box"></div>
</body>
<script>
    // 设置rem
    var fontsize=50;
    document.documentElement.style.fontSize=fontsize+'px';

    // 判断是高清屏还是超高清频,还是普通屏
    var dpr=window.devicePixelRatio;

    var initialScale=1/dpr;

    var meta=document.querySelector('meta[name=viewport]');

    // 屏幕放大
    meta.content='initial-scale='+initialScale;

    // 内容放大
    var newFontSize=fontsize*dpr;
    document.documentElement.style.fontSize=newFontSize+'px';

    console.log(window.devicePixelRatio);
    console.log(document.documentElement.clientWidth);
</script>
</html>
```







### classLsit

```
classLsit的元素对象的一个属性,用来操作元素的class类
	add		添加类名
	remove	移出类名
	contains	是否包含指定类名
	toggle		类名的有无切换
	
a.classList.add('b')
向元素a添加类b
```

```
menu.addEventListener('touchstart',function () {
        this.classList.toggle('open');
    });
    当我们每次点击menu时,如果menu有这个类,就消除,如果没有,就添加
```







### 水平撑开元素

```
父级元素定位
position:absolute;
while-space:nowarp;
font-size:0;

子元素
display:inline-block;
```









### 自动

```
想到自动,首先用过渡
```





### 获取元素在同辈元素中的索引

```
1.在标签中添加索引标记
<div data-index=1></div>
<div data-index=2></div>
<div data-index=3></div>


2.在遍历元素时,给每个元素添加属性
navItems.forEach(function (item,index) {
        item.index=index;
        item.addEventListener('touchstart',function (e) {
            transformCSS(moveBorder,'translateX',index*42);
        })
    })
```







### 竖向滑屏

```
tween算法

```









### 懒加载

```
是页面的一种加载效果
特点:减少网页加载时间
	减少使用数据
	
```





````
图片接口
	https://picsum.photos/id/10/300/300
	
	10:图片内容
	300	图片宽度
	300 图片高度
````





```
如何使图片不加载
	1.删除图片的src属性
	2.自定义一个src属性
```



```
设置元素的过渡,尽量设置指定的类型,避免js出错
```













### IOS多指事件

```
事件类型
	gesturestart	手指触屏当前元素,屏幕上有两个或两个以上的手指
	gesturechange	手指触屏当前元素,屏幕上有两个或两个以上的手指位置发生移动
	gestureend		手指离开当前元素后,屏幕上还有一个手指
```



```
scale 触点的距离与触点初始距离的比例
rotation 触点的角度差与初始角度差的差
```





### transitionend事件

```
当过渡执行完成后,执行该事件

b.ontransitionend = function () {
            isMove = false;
            console.log(1);
        }
```









### 音频事件

```
音频标签属性
	controls	显示控件
	autoplay	自动播放
	loop		循环播发
	preload		预加载
	muted		静音
```



```
onloadedmetadata		当音频元数据加载完毕后出触发(主要作用:获取音频的总时长)
ontimeupdate			当播放时发生变化时触发
onvolumechange			当声音改变时触发
```



#### 音视频对象属性

**可读可写属性**

```
currentTime			音频已经播放的时长(单位为秒)
volume				控制和获取当前的音量(0~1)
muted				查看和控制静音
playbackRate		播放速率
```



**只读属性**

```
duration		音频总时长(单位为秒)
paused			布尔值.音频是否暂停(true为暂停,false为播放)
ended			布尔值.音频文件播发结束(true表示播发结束,false表示视频播放中,或暂停)
```





#### 音视频对象方法

```
pause		暂停
play		播放
```









### 视频事件

```
	controls	显示控件
	autoplay	自动播放
	loop		循环播发
	poster		预览图片(封面)
	muted		静音
	preload		预加载
		none		不预先加载任何数据
		metadata	只预加载元数据(视频总长度,第一帧画面图形等)
		ayto		预先加载视频
```



```
onplay
	事件,当视频播放的时候
	
onpause	
	当视频暂停触发
```



```
从目前来看,在Chrome浏览器中,currentTime如果是在本地打开运行,currentTime只能获取时长,无法控制时长
但是在ftp或文件中打开,没问题
```



```
http://s8.qhimg.com/share/audio/piano1/f5.mp3
	获取钢琴的键音
```

















## Canvas

````
canvas是html5新增的标签,用来在网页上绘制图像.英文原意画布
````



```
canvas标签默认为300*150的行内块元素,大小的设置应在行内设置,不能在css的style中设置
```







#### 基本使用



**1.创建canvas标签**

```
<canvas></canvas>
```



**2.获取元素对象**

```
var canvas=document.querySelector('canvas');
```



**3.获取渲染上下文**

```
var ctx=canvas.getContext('2d');   //  2d  webgl(3d)  webgl2
```



**4.绘制图形**

矩形绘制方法1:

```
  	//绘制图形
    // 第一个参数为水平方向的起始位置
    // 第二个参数为垂直方向的起始位置
    // 第三个参数为绘制的宽度
    // 第四个参数为绘制的高度
    ctx.fillRect(100,50,200,100);
```



矩形绘制方法2:

```
 	//确定区域
    ctx.rect(200,100,100,300);
    //填充区域
    ctx.fill();
```







1.边框矩形图形绘制

```
	//方法1
    ctx.strokeRect(100,100,200,200);




    //方法2
    ctx.rect(100,100,100,100);
    //边框绘制
    ctx.stroke();
```











#### 线段绘制

```
    //开始绘制
    ctx.beginPath();
    //设置画笔的宽度
    ctx.lineWidth=5;
    //设置画笔的颜色
    ctx.strokeStyle='pink';
    //将画笔移动到起始位置
    ctx.moveTo(100,50);
    //绘制线段      将画笔从当前位置绘制到下一个坐标点
    ctx.lineTo(300,150);
    ctx.lineTo(500,50);
    ctx.lineTo(100,50);
    //描边(绘制路径)
    ctx.stroke();

```





```
设置线段的始末样式lineCap
	butt		线段末端以方形结束(默认值)
	round		线段末端以圆形结束
	square		线段末端以方形结束,但是增加了一个宽度和线段相同,高度是线段厚度一半的矩形区域
```





```
设置线段的转角样式linejoin
	round		圆角
	bevel		斜角
	miter		直角
```



````
	ctx.closePath()		闭合线段
````





#### getComputedStyle

```
getComputedStyle
	获取元素计算后的css样式
	getComputedStyle(a).color
		获取元素a的字体颜色
```





#### 通过js控制canvas的宽高

```
canvas.width=500;
canvas.height=800;
```







#### 圆弧绘制

方法1

```
    //第一个参数为起始水平位置
    //第二个参数为起始垂直位置
    //第三个参数为圆弧半径
    //第四个参数为圆弧起始角度(单位为弧度)
    //第五个参数为圆弧结束角度(单位为弧度)
    //第六个参数为是否为逆时针
    //弧度如何转化为角度     角度/180*π
    //旋转的零度默认在最右侧,顺时针为正角度,逆时针为负角度
    ctx.arc(200, 200, 100, 0, 60 / 180 * Math.PI,true);
```





方法2

```
    //定位第一个点
    ctx.moveTo(200, 100);

    //调用方法
    //作用:先确定三个点,然后用切点来绘制圆弧
    //第一,二个参数为第二个点的位置
    //第三,四个参数为第三个点的位置
    //第五个参数为圆弧的半径
    ctx.arcTo(400, 100, 200, 200, 20);

```









#### 变形

```
canvas变形指的是改变绘制的坐标系

	translate		修改坐标系的位置
	scale			放大或缩小坐标系
	rotate			旋转坐标系
	
	
	save			保存当前的绘制状态
	restore			恢复之前的绘图状态
```





```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        canvas {
            border: 1px solid #000000;
            display: block;
            margin: 100px auto;
        }
    </style>
</head>
<body>
<canvas width="600px" height="600px"></canvas>
</body>
<script>
    var canvas = document.querySelector('canvas');
    var ctx = canvas.getContext('2d');

    //保存当前的绘制状态(   坐标系    画笔状态    颜色      宽度      样式)
    ctx.save();


    //开始绘制
    ctx.beginPath();
    //移动坐标系的位置
    ctx.translate(200, 200);
    //移动坐标系的角度
    ctx.rotate(-67 / 180 * Math.PI);
    //放大或缩小坐标系的大小
    ctx.scale(0.8, 1);
    //移动起始位置
    ctx.moveTo(0, 0);
    //移动画笔绘制到下一个坐标点
    ctx.lineTo(200, 200);
    ctx.stroke();


    
    //还原为上一个状态
    ctx.restore();
    ctx.beginPath();
    ctx.moveTo(0, 0);
    ctx.lineTo(100, 100);
    ctx.stroke();
</script>
</html>
```







#### 擦除

```
	//擦除指定区域
    //第一个参数为起始水平位置
    //第二个参数为起始垂直位置
    //第三个参数为擦除的宽度
    //第四个参数为擦除的高度
    ctx.clearRect(120, 120, 200, 100);
```









#### 图片绘制

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        * {
            padding: 0;
            margin: 0;
        }

        ul {
            list-style: none;
        }

        canvas {
            border: 1px solid #ccc;
        }
    </style>
</head>
<body>
<canvas></canvas>
</body>
<script>
    var canvas = document.querySelector('canvas');
    canvas.width = 600;
    canvas.height = 500;
    var ctx = canvas.getContext('2d');

    //图片操作
    //1.创建图片对象
    //方法1:创建图片对象
    //方法2:使用DOM创建节点
    // var img = new Image;
    var img=document.createElement('img');
    //2.设置src
    img.src = '../img/t1.jpg';
    //3.给图片绑定加载完毕事件
    img.onload = function () {
        //参数1    图片对象
        //参数2    水平起始位置
        //参数3    垂直起始位置
        //参数4    图片宽度
        //参数5    图片高度
        ctx.drawImage(img, 0, 0, 600, img.height * 600 / img.width);            // 画
    }
</script>
</html>
```









#### 渐变



````html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        * {
            padding: 0;
            margin: 0;
        }

        ul {
            list-style: none;
        }

        canvas {
            border: 1px solid #ccc;
            box-sizing: border-box;
        }
    </style>
</head>
<body>
<canvas></canvas>
</body>
<script>
    var canvas = document.querySelector('canvas');
    canvas.width = 600;
    canvas.height = 500;
    var ctx = canvas.getContext('2d');

    //线性渐变
    //参数1       起始水平位置
    //参数2       起始垂直位置
    //参数3       结尾水平位置
    //参数4       结尾垂直位置
    var gradient = ctx.createLinearGradient(0, 0, canvas.width, canvas.height);

    //设置颜色
    //第一个参数     从0开始都是第二个参数指定的颜色
    //第二个参数     颜色
    gradient.addColorStop(0,'red');
    gradient.addColorStop(0.5,'yellow');
    //    从0,2开始都是第二个参数指定的颜色
    gradient.addColorStop(1,'blue');

    //填充颜色
    ctx.fillStyle = gradient;

    ctx.fillRect(0, 0, canvas.width, canvas.height);
</script>
</html>
````





```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        * {
            padding: 0;
            margin: 0;
        }

        ul {
            list-style: none;
        }

        canvas {
            border: 1px solid #ccc;
            box-sizing: border-box;
        }
    </style>
</head>
<body>
<canvas></canvas>
</body>
<script>
    var canvas = document.querySelector('canvas');
    canvas.width = 600;
    canvas.height = 500;
    var ctx = canvas.getContext('2d');

    //径向渐变
    //前三个参数为第一个圆的位置和半径
    //后三个参数为第二个圆的位置和半径
    var gradient = ctx.createRadialGradient(300, 250, 20, 300, 250, 100);

    gradient.addColorStop(0, 'red');
    gradient.addColorStop(0.5, 'yellow');
    gradient.addColorStop(1, 'black');
    //填充颜色
    ctx.fillStyle = gradient;

    ctx.fillRect(0, 0, canvas.width, canvas.height);
</script>
</html>
```







#### 文字

```
    //设置文字样式
    ctx.font = 'bold 30px 宋体';
    
    
    
    
    //填充文字
    //在位置100,100的地方放入文字
    ctx.fillText('i love you', 100, 100);




    //镂空文字
    ctx.strokeText('I LOVE YOU', 100, 200);
```





**文字水平对齐**

```
ctx.textAlign='left';
ctx.textAlign='right';
ctx.textAlign='center';
ctx.textAlign='end';
ctx.textAlign='start';
	都是相对于中心线
```





**垂直对齐**

```
ctx.textBaseline = 'top';					文本基线在顶端
ctx.textBaseline = 'hanging';				文本基线悬挂
ctx.textBaseline = 'middle';				文本基线居中
ctx.textBaseline = 'bottom';				文本基线在底部
ctx.textBaseline = 'alphabetic';			默认
```







#### 阴影

```
    ctx.shadowColor = '#99a';			阴影颜色
    ctx.shadowOffsetX = 10;				阴影水平偏移量
    ctx.shadowOffsetY = 10;				阴影垂直偏移量
    ctx.shadowBlur = 4;					阴影模糊半径
```









#### 图形合成

```
图形合成设置用来控制多个图形的合成规则


	新绘制的图形标示为	  源图形		 source
	以绘制完毕的图形	  目标图形	     destination
```

​	

```
ctx.globalCompositeOperation = 'source-over';


globalCompositeOperation	合成规则的属性


	选项值:
			source-over			默认,在目标图形上显示源图形
			source-atop			源图形在目标图形上的内容显示,不在目标图形上的源图形不显示
			source-in			目标图形和源图形上的交点处显示,其他不显示,就是取交集
			source-out			源图形在目标图形上的部分不显示,并且目标图形也不显示
			
			
			
			destination-over	和上面的一样,只不过是目标图形和源图形处在的位置不同而已,原本是目标图形消失,现在是源图形消失
			destination-atop
			destination-in
			destination-out		
```









#### 像素操作

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        canvas {
            display: block;
            margin: 50px auto;
            border: solid 1px #000;
            background-image: url("../img/t1.jpg");
            background-size: cover;
        }
    </style>
</head>
<body>
<canvas></canvas>

<script>
    var canvas = document.querySelector('canvas');
    var ctx = canvas.getContext('2d');

    canvas.width = 600;
    canvas.height = 500;

    ctx.fillStyle = '#ccc';
    ctx.fillRect(0, 0, 600, 500);

    //获取10 * 10的矩形的像素点的信息
    var pixelData = ctx.getImageData(0, 0, 10, 10);


    function getPixel(imgData, x, y) {
        var index = y * 4 * imgData.width + x * 4;
        var d = [];
        d[0] = imgData.data[index];
        d[1] = imgData.data[index + 1];
        d[2] = imgData.data[index + 2];
        d[3] = imgData.data[index + 3];
        return d;

    }

    function setPixel(imgData, x, y, colors) {
        var index = y * 4 * imgData.width + x * 4;
        imgData.data[index] = colors[0];
        imgData.data[index + 1] = colors[1];
        imgData.data[index + 2] = colors[2];
        imgData.data[index + 3] = colors[3];
    }

    setPixel(pixelData, 5, 5, [255, 112, 0, 255]);

    //设置像素点
    //第一个参数为修改后的像素信息
    //第二,三个参数为偏移量
    ctx.putImageData(pixelData, 0, 0);
</script>
</body>
</html>
```















## 版本控制

```
版本控制工具
	git
	svn
```





### 版本控制器SVN

```
作用:
	1.备份还原,版本回退
	2.协同修改
	3.权限控制
```





```
BUG管理平台			禅道
```



````
集中式 					有一个核心,所有人都可以通过这个核心获取你想要的代码
						   缺点: 一旦核心坏掉,就惨了

分布式						没有核心
````





![SVN操作流程](C:\Users\86188\Pictures\Saved Pictures\SVN操作流程.png)



```
服务器: 配置极高,安装了专业的服务器操作系统(linux),有着极佳的网络环境
```



```
个人PC电脑: 配置相对于满足日常需求,安装的是用户的操作系统
```





#### SVN的安装

```
安装服务端:	VisualSVN-Server
安装客户端:	TortoisesSVN
```









#### SVN服务端创建项目

1.点击 Repositories   ------> Create New Repository

![安装项目第一步](C:\Users\86188\Pictures\SVN\安装项目第一步.png)



![安装项目第二步](C:\Users\86188\Pictures\SVN\安装项目第二步.png)

![安装项目第三步](C:\Users\86188\Pictures\SVN\安装项目第三步.png)

![安装项目第四步](C:\Users\86188\Pictures\SVN\安装项目第四步.png)

![安装项目第五步](C:\Users\86188\Pictures\SVN\安装项目第五步.png)

![安装项目第六步](C:\Users\86188\Pictures\SVN\安装项目第六步.png)

![安装项目第七步](C:\Users\86188\Pictures\SVN\安装项目第七步.png)

![安装项目第八步](C:\Users\86188\Pictures\SVN\安装项目第八步.png)







 https://LAPTOP-N98UJAC9:8443/svn/0719_demo

https://LAPTOP-N98UJAC9:8443/svn/0719_demo/





C:\Users\Public\Documents\VisualSVN Server\Backup\my_backup









#### SVN服务端备份项目



点击 jobs ---------->    Create backup job



![1](C:\Users\86188\Pictures\SVN\SVN服务端项目备份操作流程\1.png)





![2](C:\Users\86188\Pictures\SVN\SVN服务端项目备份操作流程\2.png)



![3](C:\Users\86188\Pictures\SVN\SVN服务端项目备份操作流程\3.png)

![4](C:\Users\86188\Pictures\SVN\SVN服务端项目备份操作流程\4.png)

![5](C:\Users\86188\Pictures\SVN\SVN服务端项目备份操作流程\5.png)



![6](C:\Users\86188\Pictures\SVN\SVN服务端项目备份操作流程\6.png)





#### 地址查看

```
https://LAPTOP-N98UJAC9:8443/svn/0719_demo
https://LAPTOP-N98UJAC9:8443/svn/0719_demo/


LAPTOP-N98UJAC9 为电脑的名字
这个地址只能自己用,别人用不了,要将LAPTOP-N98UJAC9改成你连接的网络的IP地址才可以访问地址,还要关闭防火墙
```





```
局域网:  范围比较小,比如机房的网络,只能一个房间的人可以使用,其他的不能访问到,最小的局域网是手机WiFi

城域网:  一个城市可以使用,其他城市无法访问到

广域网:  范围大,比如百度,所有人都可以访问到

IP地址:  分类    查看自己的IP地址    如何设置自己的IP
```







```
获取MAC地址
	cmd-----> ipconfig/all ------->物理地址
```









#### SVN服务端





```
创建的本地仓库没有标识符,方法
	1.重启电脑
	2.打开资源管理器,重新启动Windows资源管理器(win7叫做explorer.exe)
	如果是win7系统,需要结束explorer.exe,然后打开任务管理器左上角的文件,点击运行新程序,输入explorer.exe,回车即可
```







```
1.检出仓库(checkout) -------- 第一次(本地"啥"也没有)
```







```
2.新增文件,提交
```



```
当我们第一次检出仓库时,会要求输入用户,但是当我们第二次检出时,就不需要,以后检出其他仓库时,也不需要
,这样就是出现一个错误,当其他仓库没有你第一次检出仓库时输入的用户,就会报错
	解决方案:点击TortoiseSVN--->settings--->Saved Data---->将所有clear和clear All按一遍,点击确定,就可以了
```







#### 版本回退



```
版本回退
	右键点击指定回退的文件,点击TortosieSVN----->Update to revision
```

![第一步](C:\Users\86188\Pictures\SVN\SVN客户端\版本回退\第一步.png)





![第二步](C:\Users\86188\Pictures\SVN\SVN客户端\版本回退\第二步.png)



![第三步](C:\Users\86188\Pictures\SVN\SVN客户端\版本回退\第三步.png)

















 https://LAPTOP-N98UJAC9:8443/svn/text













#### 版本冲突

```
原因: 首先,a和b获取了项目text中的文件demo.txt,a和b对文件进行修改,但是a修改的比较快,b修改的比较慢,a将修改后的文件提交给服务端后,b提交就会出错,原因是版本和a提交上去的版本不同,会出现冲突
```

![原因](C:\Users\86188\Pictures\SVN\SVN客户端\版本冲突\原因.png)



```
点击ok,会提示让你更新,点击更新
```



![1](C:\Users\86188\Pictures\SVN\SVN客户端\版本冲突\1.png)



```
然后点击ok,退出提交
```

![2](C:\Users\86188\Pictures\SVN\SVN客户端\版本冲突\2.png)





````
111
222
333
444
<<<<<<< .mine
555
AAA
BBB
CCC||||||| .r1
555=======
555
666
777
888>>>>>>> .r2

````

```
首先,在第一个<前敲一个回车,然后在第一个 | 前敲两个回车,最后一个 = 后敲一个回车
```

```
111
222            这是原本的内容
333
444

<<<<<<< .mine
555
AAA                  这是你的新增的内容
BBB
CCC

||||||| .r1
555=======            这是你们公共的内容

555
666                这是他的内容
777
888>>>>>>> .r2
```



```
将公共的内容剪切到原本的内容后,删除你和他新增的内容中的公共内容,然后将他的内容剪切到原本的内容后,最后将你的内容剪切到原本的内容后即可,还有删除>=|等
```

```
111
222            这是原本的内容
333
444
555
666                这是他的内容
777
888
AAA                  这是你的新增的内容
BBB
CCC


```



```
修改完成后,删除新增的三个文件,提交修改的文件即可
```





``` 
方法2
	修改完成后,直接更新一下,冲突自然暴露出来,不需要先提交,冲突才会出来
	
	
	文件右键点击TortoiseSVN  ----->  Edit conflicts(只有出现冲突才会出现)
	修改即可
```







```
方法3(使用webstrom解决冲突)
	打开webstrom,打开项目,文件右键, Subversion----->Resolve Text Conflict
```

![第一步](C:\Users\86188\Pictures\SVN\SVN客户端\版本冲突\webstrom解决版本冲突\第一步.png)





![第二步](C:\Users\86188\Pictures\SVN\SVN客户端\版本冲突\webstrom解决版本冲突\第二步.png)





```
webstrom中文件颜色的说明
	暗红色: 新增的文件
	亮红色: 冲突的文件
	蓝色:	 修改了,但是没有提交的文件
	绿色:  文件被标识了,代表以后要被提交了
```









#### 配置忽略文件

```
当我们在webstrom中编写文件时,会生成一个文件idea,当我们提交项目时,文件也会被提交,所有我们需要忽略它
```



````
1.点击TortoiseSVN -----> Settings
````



![文件忽略](C:\Users\86188\Pictures\SVN\SVN客户端\文件忽略.png)





```
在最后面输入 .idea即可(指定的文件名)
```







#### 锁

```
当你想让他人无法修改你的文件时,可以给你的文件加一个锁
```



```
1.文件右键点击tortoiseSVN -----> Properties
```

![锁](C:\Users\86188\Pictures\SVN\SVN客户端\锁.png)



```
点击New... ------> Needs-Lock
```

![锁2](C:\Users\86188\Pictures\SVN\SVN客户端\锁2.png)

```
点击加锁即可
```



```
加锁: 可以使你和别人无法修改文件,可以查看,当你修改文件保存时,会让你另存为
		别人也可以解锁,但是,你可以通过TortoiseSVN -----> Show log查看修改记录来确认谁解了你上的锁
		所以说: 上锁是防君子,不防小人的
```





```
多个提交: 选中多个文件,右键TortoiseSVN ---> Add
当我们提交时,他会自动勾选,不需要我们一个个勾选
```







#### webstrom中忽略配置文件

````
点击 Settings ---> Version Control ---> lgnored Files
````

![webstrom文件忽略](C:\Users\86188\Pictures\SVN\SVN客户端\webstrom文件忽略.png)

```
点击忽略文件夹, 找到指定路径,点击Apply ,Ok
```







#### webstrom中提交文件

![webstrom文件提交1](C:\Users\86188\Pictures\SVN\SVN客户端\webstrom文件提交1.png)







#### webstrom中版本回退

```
文件右键点击Subversion ---> Show History
```

![webstrom版本回退](C:\Users\86188\Pictures\SVN\SVN客户端\webstrom版本回退.png)



```
找到指定文件,右键
	Jump to Source			查看
	Get						版本回退
```







```
对比: Subversion -----> Compare with Latest Repository Version
	与上一个版本做对比
```









#### SVN菜单的用法

```
Revert			撤销
```











### 版本控制器git

是目前世界上最先进的分布式版本控制工具(没有之一)





 #### 安装

````
git config --global user.name "laijiandong"					配置名字

git config --global user.email "1369199895@qq.com"			配置邮件
````



```
配置好之后,名字和属性存在电脑用户文件下.gitconfig下
```







![git三区图示](C:\Users\86188\Pictures\git\git三区图示.png)









#### git创建仓库

```
第一步		
	cd 到指定需要创建的仓库的文件夹中,使用命令 git init 初始化这个文件夹,将这个文件夹创建成一个仓库
	成功提示: Initialized empty Git repository in C:/Users/86188/Desktop/demo/.git/
```



````
第二步
	提交文件到暂存区
	git add xxx		添加指定文件到暂存区中
	
	没有任何提示,代表成功
	没有初始化, 会提示 fatal: Not a git repository(or any of the parent directories):.git
	失败会提示: fatal: pathspec 'x.txt' did not match any files
	肯能会出现警告: warning: LF will be replaced by CRLF in xxxxx
    	原因: linux 和 window 的换行符不一致导致的
    	解决方法: git config --global core.autocrlf false
    	
    	
    	git status		查看状态,可以查看到文件是否上传上去了,为绿色
````



```
第三步
	提交文件到版本区
	git commit -m '注释'   
	成功提示: 
	[master (root-commit) e99f0e7] this is one commit
	 1 file changed, 4 insertions(+)
 	create mode 100644 a.txt

git status		如果出现On branch master
						nothing to commit, working tree clean
代表文件以经提交
```



```
git status
		如果为红色				就是文件没有被提交到暂存区
		如果为绿色				就是文件在暂存区中,没有到版本区中
		如果没有指定文件		  就是已经在版本区中
```







````
工作区到暂存区全部存入
	git add *
	git add .
````









#### 差异对比

```
git diff			对比暂存和工作区文件的区别
```

```
diff --git a/a.txt b/a.txt              a代表暂存区的代码				b代表工作区的代码
index 1802a74..cbe236c 100644				代码地址
--- a/a.txt							- 代表暂存区的代码
+++ b/a.txt							+ 代表工作区的代码
@@ -1,3 +1,6 @@						(3~6]
 aaa
 bbb
 ccc
+ddd
+eee
+fff

```





```
git diff --cached				比较版本区和暂存区
```



```
git diff master					比较版本区和工作区
```











#### 日志 + 版本号

```
git log            		显示从最近到最远的所有提交日志
git reflog				显示每次提交的id
```









#### 版本回退 + 版本穿梭 + 版本撤销

```
git reset --hard HEAD^							版本回推(回退一次)
git reset --hard HEAD^^							版本回推(回退两次)
git reset --hard 版本号						  回退到指定版本号的版本
```



```
git reset HEAD									用版本区的文件去替换暂存区的文件
git checkout -- x.txt							用暂存区指定文件去替换工作区的指定文件(危险)
git checkout HEAD x.txt							用版本区的文件替换暂存区和工作区的文件(危险)
git rm --cached x.txt							从暂存区删除文件
```









#### 文件删除

```
git rm x.txt					删除文件(必须在版本区中)
git rm -f xxxx   				删除文件夹(文件夹中必须有文件,不然会被忽视,无法删除)
```









#### 分支

```
1.主分支			 master					 代码经过了开发人员单元测试,以及测试人员详细的一套测试通过后,确定没问题
2.开发分支			 dev       				开发人员所有代码提交到此分支
3.测试分支			 text					测试人员用的(由开发人员进行完单元测试之后的代码会放到此分支)
4.里程碑分支		    tags					一个阶段完成
```

```
1.0.0
第一位: 大版本号
第二位: 小功能添加
第三位: bug
```



```
git checkout -b dev					创建dev分支, 并切换到dev分支(当我们创建分支时,会将主分支的内容复制到创建的分支中,并且									在window上看到的文件内容也是dev分支上的)

git branch							查看当前分支

git checkout master					切换分支

git merge dev						合并分支(首先要站在合并的分支上,然后将dev和当前的分支合并,且dev不受影响)

git branch -d dev					删除dev分支(不能站在要被删除的分支上)

git diff 分支1 分支2				 查看两个分支之间所有的差异(详细差异)

git diff 分支1 分支2 --stat			 显示出两个分支2之间所有差异的文件列表

git diff 分支1 分支2 xxx			 显示指定文件的详细差异
```

```
创建分支时,分支中必须有内容且内容必须要上传到版本区中
```











#### 版本冲突

```

```













#### 本地库和远程库连接

```
首先.我们要使本地库和GitHub远程库连接,需要创建本地库

第二步: git remote add peiqi https://github.com/12ab123/0719_demo.git
		remote			远程
		peiqi			远程库的名字,可以随便起,就是为了告诉本地库,有一个远程库,名字为peiqi
		
		
第三步:git push -u peiqi master
		连接网络,让本地库和远程库连接,传入数据
		peiqi			远程库的名字,依据第一步
		master			分支
```

```
在第三步时,输入命令后,会要求输入用户名和密码,一般情况下,输入一次就会记住,但是有的电脑版本过低,每次提交代码到远程库时,都需要输入用户名和密码,为了解决,输入命令: 	git config --global credential .helper store
	会修改配置文件
```





```
如果关联远程库错了
	git remote remove peiqi				取消关联
```



```
获取远程库的新内容
	git pull peiqi master				获取远程库peiqi的主分支master中的内容 
	
	git fetch peiqi master:aaa			获取远程库peiqi的主分支master中的内容,创建一个新的分支aaa存放从远程库获取的内容
	
	git pull							获取全部
```







#### 克隆

```
git clone 远程仓库路径
```

```
注意:
	克隆只能克隆主分支
	
克隆远程仓库的dev分支
		git checkout -b dev origin/dev
		创建一个dev分支,dev分支的内容为远程仓库中dev分支的内容
```









#### 忽略文件

```
创建一个文件,名为.gitignore
文件中写入忽略的文件名,比如        /.idea
```









#### 搭建博客

```
1.域名
2.服务器
3.域名绑定到服务器上
4.编写一个个人主页
```



https://12ab123.github.io/MYBLOG/.



```
用github创建一个博客,然后明一个域名,与博客绑定,即可
```













## 性能优化



### 浏览器的内核

```
IE ---------> Trident
Safari -------> WebKit
Chrome -------> Webkit的分支引擎(Blink)
Opera---------> Blink
Friefox-------->Gecko
```







```
浏览器的进程
	Browser进程: 浏览器的主进程,负责浏览器界面的显示,创建和销毁
	Renderer进程: 负责页面的渲染
```







### 浏览器渲染引擎

```
一个渲染引擎主要包括:								渲染过程
	1.HTML解析器       	 					 生成DOM树
	2.CSS解析器		  						 生成CSS样式树
	3.JS引擎									  绑定事件,修改DOM和CSS树
	4.布局layout模块							将DOM树和CSS树合成一个渲染树
	5.绘图模块									根据渲染树的信息计算每个节点的几何信息
											   将每个节点绘制到屏幕上
```









### 阻塞



```
浏览器控制台工具
	Network ---> Disable cache				禁用缓存,勾上就是禁用缓存,每次刷新页面都是从网上下载,不会在缓存中找
	
	Network ---> Online						网络状态,可以将网络调为3G,4G,离线等,开可以手动添加
```





```
style样式渲染: 页面加载到style标签时,HTML解析器会让另一个解析器去解析style标签内的内容,自己会继续往下面加载(异步),加载完成之				  后,不会等待style标签内的css样式加载,直接在页面上显示,当style标签中的CSS样式解析完成后,会加载到页面上,页面就会				 闪一下(闪屏)

link样式渲染: 页面加载到link标签时,HTML解析器会让CSS解析器去解析link内的外联CSS样式,而HTML解析器会继续往下面加载,但是加载完			  成之后不会将内容放入页面,而是等待CSS解析器加载完成(同步),才会将CSS样式和DOM结合,放入页面(阻塞)

比较: style加载网页速度更快,但是当style标签内的内容过多,会导致闪屏
	 link加载速度较慢(指的是页面渲染时间慢),但是不会出现闪屏,用户体验好,所以使用link样式渲染
```



```
js样式渲染:
	1.阻塞后续DOM解析
	2.阻塞页面渲染
	3.阻塞后续js的执行
```

```
备注:
	1.js和css永远是互斥的,js执行,css不会执行,css执行,js不会执行
	2.js和css不会阻塞外部资源的加载(图片, 视频, 音频等)
```

```
DOMContentLoaded			DOM树解析完成
onload						DOM树解析完成并且网页所依赖的资源加载完成后
```

```
defer
	紧随DOM解析完成之后执行
	<script defer src="1.js"></script>
```

```
link: 阻塞页面渲染,不阻塞页面解析
js: 阻塞页面渲染,阻塞页面解析
style:不阻塞页面渲染,不阻塞页面解析
```



```
link导入速度慢,我们可以提高外部css加载速度
	1.使用CDN节点进行外部资源加载
	2.对css进行压缩(webpack gulp)
	3.减少http请求数,将多个css文件合并
	4.优化样式表的代码
```













### 图层

```
在渲染DOM时,浏览器所做的工作实际上是:
	1. 获取DOM后分割的多个图层
	2. 对每个图层进行节点计算样式结果		(Recalculate	style---样式重计算)
	3. 为每个节点上生成图形和位置		 (Layout--布局 重排 回流)
	4. 将每个节点绘制填充到图层位图中		(Paint--重绘)
	5. 图层作为纹理上传至GPU
	6. 组合多个图层到页面上生成最终屏幕图像      (Composite  Layers----图层重组)
```



```
图层创建条件
	1. 拥有3D变化的CSS属性
	2. 有video标签
	3. canvas
	4. 动画
	5. CSS加速属性(will-change)
```





````
重绘: 一个元素外观的改变所触发的浏览器行为,重绘是以图层为单位,如果图层中的一个元素需要被重绘,整个图层都要被重绘

重排: 重新排列布局

重绘不一定需要重排,重排大多数情况下需要重绘
````







```
常见触发重排的操作
	1. 增加,删除,移动,修改DOM
	2. 修改CSS样式
	3. 当你resize窗口时(移动端没有)
	4. 修改网页默认字体
	5. 获取某些属性(width,height等等)
	
```





```
优化方案:
	1.元素位置移动变换时尽量使用transform来代替top,left
	
	2.使用opacity代替visibility
		1.使用visibility发生重绘,但不会发生重排
		2.使用opacity即发生重绘,还发生重排(GPU底层设计如此)
		3.opacity和图层一起,既不会发生重绘,也不会发生重排
		
	3.不要使用table布局
	
	4.将多次改变样式属性的操作合并成一个操作
		不要一条一条的修改DOM样式,预先定义好class,然后修改DOM的class
	
	5.将DOM离线后修改
		由于display属性的none不在渲染树中,对于隐藏的元素操作不会引发其他元素的重排
		
	6.利用文档碎片
	
	7.不要把获取某些DOM节点的属性值放在一个循环里当成循环变量
	
	8.动画实现过程中,启用GPU硬件加速(transform:translateZ(0))
	
	9.为动画的元素新建图层,提高动画的z-index
	
	10.编写动画时,尽量使用API
```



```
requestAnimationFrame()
	传入一个函数,在浏览器重绘之前会执行传入的函数,函数内必须再调用一次requestAnimationFrame()
	
	返回值:一个整数id
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        * {
            padding: 0;
            margin: 0;
        }

        ul {
            list-style: none;
        }

        div {
            width: 200px;
            height: 200px;
            background-color: #acf5fa;
        }
    </style>
</head>
<body>
<div></div>
<script>
    var div = document.querySelector('div');
    var index = 0;
    var id = 0;

    function move() {
        index++;
        div.style.transform = 'translateX(' + index + 'px)';
        id = requestAnimationFrame(move)

    }

    id = requestAnimationFrame(move);

    setTimeout(function () {
        cancelAnimationFrame(id);
    }, 2000)
</script>
</body>
</html>
```





### CDN

```
通过缩短地理位置的距离给你一个最快让你响应1的服务器
```











### 函数防抖

```
概念: 延迟要执行的动作,若在延迟的这段时间内,再次触发了,则取消之前开启的动作,重新计时
举例: 电脑无操作1分钟会自动休眠,当第40秒时鼠标被移动一下,重新计时
实现: 定时器
应用: 搜索时,等用户输入完完整的请求,再搜索
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>函数防抖测试</title>
</head>
<body>
<input type="text">
<button>搜索</button>
<script>
    let inputNode=document.querySelector('input');
    let timer;
    inputNode.addEventListener('keyup',function () {
        let value=inputNode.value;
        if(timer){
            clearTimeout(timer);
        }
        timer=setTimeout(function () {
            sendAjax(value);
        },300);
    });

    function sendAjax(data) {
        console.log('发送了一次Ajax请求,内容为' + data );
    }
</script>
</body>
</html>
```









### 函数节流

```
概念: 设定一个特定的时间,让函数在特定的时间内只执行一次,不会频繁执行
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>函数节流</title>
    <style>
        body {
            height: 2000px;
        }
    </style>
</head>
<body>
<script>
    let canLog = true;
    document.body.onscroll = function () {
        if (canLog) {
            console.log(1);
            canLog = false;
            setTimeout(function () {
                canLog = true;
            }, 2000)
        }
    }
</script>
</body>
</html>
```











### 浏览器本地存储

```
Cookie, SessionStorage, LocalStorage这三者都可以用来在浏览器端存储数据,而且都是字符串类型的键值对(json)
```

```
Session: 会话
SessionStorage: 浏览器端用于存储数据的容器,常常被前端人员简称Session
Session会话存储: 服务端一种存储数据的方式,常常被后端人员简称Session
```





**web Storage**

```
SessionStorage 和 LocalStorage都是浏览器本地存储,统称为web Storage,存储内容大小一般支持5~10M
浏览器端通过Window.sessionStorage 和 Window.localStorage 属性来实现本地存储机制
```



```
sessionStorage.setItem('key','value')					存储一个键值对添加到存储中

var data=sessionStorage.getItem('key')					键名为参数,返回对应的值

sessionStorage.removeItem('key')						键名为参数,把对应的键值对从储存中删除

sessionStorage.clear()									删除所有键值对
```





**storage**

```
storage对象发生变化时触发(即创建,删除,更新数据时)
	event中的属性
		key				修改或删除的key值
		newValue		新设置的值
		oldValue		调用改变前的value值
		url				触发该脚本变化的文档的url
		storageArea		当前的storage对象
```



```
数据同步: 同一个网站上不同页面之间的信息传递
```









### 缓存

```
缓存定义: 浏览器在本地磁盘上将用户之前请求的数据储存起来,当访问者再次需要该数据的时候无需再次发送请求,直接从浏览器本地获取数据

缓存的好处:
	1.减少请求的次数
	2.节省宽带,流量
	3.减轻服务器的压力
	4.提高网页加载速度,提高用户体验
```





**缓存分类**

```
强缓存:
	1.不会向服务器发送请求,直接从本地缓存中获取数据
	2.请求资源的状态码为: 200 ok(from memory cache)
	
协商缓存:
	1.向服务器发送请求,服务器会根据请求头的资源判断是否命中协商缓存(也就是判断资源是否过期,如果没有,就是命中,从缓存中拿资源,如果		过期了,就是没有命中,从服务器拿资源)
	2.如果命中,则返回304状态码通知浏览器从缓存中读取资源
	
共同点: 都是从服务器拿资源

不同点: 
	1.强缓存不会向服务器发送请求
	2.协商缓存发送请求给服务器,根据服务器返回的信息判断是否使用缓存
```





**缓存中的header参数**

```
强缓存的header参数
	1.expires		这是http1.0时的规范,它的值是一个绝对时间的GMT格式的时间字符串,如Mon,10,Jum 2015 21:21:21 GMT
					当我们第一次访问这个网页时,服务器会某些资源发送一个expires,当我们下一次访问网页时,如果访问的时间没有超过					 第一次访问网页时给的时间,那么就不会访问服务器,拿数据,而是从缓存中拿数据
		
	2.cache-control: max-age=number
	
	优先级:cache-control > expires
```



```
协商缓存的header参数
	1.Last-Modified/if-Modified-Since
		第一次访问网页时,网页回个某些资源添加一个Last-Modified,它的值是这个资源最后的修改时间
		当我们再次访问网页时,客户端向服务器发送一个if-Modified-Since,值是Last-Modified的值,如果if-Modified-Since的值和		服务器上该资源的最后修改时间一样,就表明该资源没有被修改,就会返回304 Not Modified,资源就从缓存中获取,如果不一样,就返		回资源
		
	2.Etag/if-None-Match
		这两个值是由服务器生成的每个资源独有的唯一标识符,如果资源发送变化,值就会改变
		判断过程和Last-Modified/if-Modified-Since一样
		

	Etag比Last-Modified更加精确,比如某一些文件1s内别修改了多次,Etag可以检查到,而Last-Modified则不行
	当我们修改资源的时间,而没有修改资源的内容,Etag检测的到,而Last-Modified不行
	所以说: Etag比Last-Modified更加精确
```









## JS模块化





### CommonJS

```
双端
```





#### 在node中

```
暴露模块
	方法1: 	module.exports=value
	方法2:	exports.xxxxxx=value
	
	
引入模块
	require(xxx)	
		第三方模块: xxx为模块名
		自定义模块:xxx为模块文件路径
```



```
CommmonJS模块化内置的一个关系: module.exports = exports = {}
	module.exports和exports都指向暴露的对象
```



```js
/*
    第二种暴露方式: exports.xxxx=value
 */

//在CommonJS模块规范中,module.exports 和 exports.xxx 不能混用
//如果出现混用,以module.exports为主
exports.haha = function () {
    console.log('我是module2的函数');
}

module.exports = 'aaa';
```

```
引入自定义模块时,在同一路径下,需要加./
```







#### 在浏览器中

```
前面的操作一样
但是,要下载一个browserify(用于将commonJS的模块化语法,翻译成浏览器认识的语法)

全局安装browserify		npm install browserify -g
-g 		全局安装,安装之后,电脑就不需要安装了,他将browserify安装到c盘的某个文件中
```



```
执行处理命令
	browserify  被翻译的文件路径 -o 翻译后的文件存放位置(文件自动被生成)
	
```



```
最后,在html文件中导入翻译后的文件即可
```







### ES6

```
暴露模块
	1.分别暴露:		export 暴露内容
	2.统一暴露:		export{xxx,yyy}
	3.默认暴露:		export defalut 暴露内容
```



```
引入模块
	1.  import {xxx,yyy} from './module1'
	2.  import module3 from './module3'
```



**babel**

```
将es6转换为es5
```



```
第一步: 全局安装		npm install babel-cli browserify      (如果安装了browserify,可去掉)
第二步: 局部安装		npm install babel-preset-es2015
第三步: 创建.babelrc文件(给babel指定具体任务)
    {
      "presets": ["es2015"]
    }
第四步: 编译
	babel 被编译的文件路径 -d 编译后的文件路径
	browserify  被翻译的文件路径 -o 翻译后的文件存放位置(文件自动被生成)
```











### AMD

```

```







### CMD

























## Node.js

```
基于Chrome V8 引擎的JavaScript运行环境
```





**npm**

```
npm: Node package manager(Node包管理器), 安装了Node就自动安装好了npm

电脑上的一个普通的文件夹,只要包含了package.json,就变成了一个符合npm规范的包
```



**查看自己node的版本命令:  node   -v**

**查看自己npm的版本命令:  npm   -v**







```
异步非阻塞的i/o操作(读写操作)
特别适用于i/o密集型应用(频繁操作i/o)
事件循环机制
单线程
跨平台
```





```
java解决高并发是增加服务器配置
node是使用回调
```







**执行文件:       node  文件名**



 

```
Node中的任何一个模块都被一个外层函数包裹
function (exports, require, module, __filename, __dirname) {}
	exports: 		用于支持CommonJS模块化规范的暴露语法
	require:		用于支持CommonJS模块化规范的引入语法
	module:			用于支持CommonJS模块化规范的暴露语法
	__filename:		当前运行文件的路径
	__dirname:		当前运行文件的文件夹的路径
	
作用: 
	1.用于支持模块化语法
	2.隐藏服务器内部实现
```





```
浏览器端,js由几部分组成
	DOM
	BOM
	ES规范
	
	
Node端,js由几部分组成
	没有DOM,BOM
	几乎包含所有ES规范
	没有window,取而代之的是一个叫global的全局变量
	
	
	
在node中禁止this指向global,而是指向一个空对象
```















### 事件循环模型



```
clearImmediate			清除立即执行函数
clearInterval			清除循环定时器
clearTimeout			清除延迟定时器

setImmediate			设置立即执行函数
setInterval				设置循环定时器
setTimeout				设置延迟定时器

process.nextTick()		用于执行立即执行函数("VIP"-----能在任意阶段优先执行)
```



```
第一个阶段:		timers(定时器阶段-----setTimeout	setInterval)
		1.开始计时
		2.执行定时器的回调
		
第二个阶段:		pending  callbacks (系统阶段)

第三个阶段:		idle  prepare (准备阶段)

第四个阶段:		poll(轮询阶段,核心)
		如果回调队列里有待执行的回调函数
			从回调队列中取出回调函数,同步执行(一个一个,依次执行),直到回调队列为空,或者达到系统的最大限度
		如果回调队列为空
			如果有设置过setImmediate,进入下一个阶段(目的: 为了执行setImmediate所设置的回调)
			如果未设置setImmediate,等待回调函数被插入回调队列,若定时器到点了,也进入下一个阶段(目的: 为了走第五阶段,随后走第			 六阶段,随后走第一个阶段,执行定时器的回调)
		
第五个阶段:		check(专门用于执行setImmediate所设置的回调)

第六个阶段:		close  callbacks  (关闭回调阶段)
```



```
当给定时器不设置时间时,若主线程没有代码,那么定时器和立即执行函数的代码输出顺序就不一定了
如果主线程有代码,且定时器没有设置时间,那么定时器的代码一定比立即执行函数的块
因为当主线程有代码时,定时器是异步的,当执行完主线程的代码,定时器也就到时间执行了,于是在第一个阶段时,就将定时器执行
当主线程没有代码时,执行第一个阶段时,由于过快,定时器正要执行时,就已经到下一个阶段了,于是定时器只有在下一次循环时执行了
```









### 包和包管理器

```
包的组成
	1.包结构: 用于组织包中的各种文件
	2.包描述文件: 描述包的相关信息,以供外部读取分析
```



#### 包结构

```
包实际上就是一个压缩文件,解压之后还原为目录,应该包含以下文件和文件夹
	1. package.json				包描述文件
	2. bin						可执行的二进制文件
	3. lib						js代码
	4. doc						doc文档
	5. test						单元测试
```













### npm

```
常用命令
	搜索:		npm search xxx
			 通过网址: www.npmjs.com
			 
	安装:		npm install xxx --save
			 npm i xxx -S
			 npm i xxx
			 备注:
			 		1.局部安装完的第三方包,放在当前目录中node_modules这个文件夹中
			 		2.安装完毕会自动产生一个packag-lock.json(npm5之后才有),里面存放的是每个下载过的包的下载地址,目的是下
			 		次下载更快
			 		3.安装完一个包,该包的名字会自动写入到package.json中(dependencies(开发依赖))
			 		
			 npm i xxx -D		安装包并将包写入到package.json(devDependencies(生产依赖))
			 
			 npm i xxx -g		全局安装
			 					一般来说,带有指令的包进行全局安装,例如: browserify,babel等
			 					没有带指令的包就无需全局安装
			 					
			 npm root -g		查看全局安装的安装路径
			 
			 npm i xxx@yyy		安装指定版本
			 
			 npm i				安装package.json中所有依赖的包
			 
			 
	移除:		npm remove xxx		删除包和package.json中的依赖申明
	
	
	
	其他命令: 
			npm aduit fix				检测项目依赖中的一些问题,并且尝试修复
			
			npm view xxx versions		查看远程npm仓库中xxx包的所有版本信息
			
			npm view xxx version		查看npm仓库中xxx包的最新版本
			
			npm ls xxx					查看我们安装的包的版本信息
			
```





```
开发依赖和生产依赖
	开发依赖: 只在开发中用到的库(写代码时),叫做开发依赖 ------- 例如: 语法检查,css压缩,格式化代码
	生产依赖: 在生产环境(项目上线)不可缺少,就是生产依赖 ------- 例如: jquery,bootstrap,vue等等
	注意: 某些包即在开发中使用,也在生产中使用: jquery等
```



```
版本
	^3.3.1		锁定大版本,以后安装包时,保证是3.x.x, x代表的是最新的版本
	~3.3.1		锁定小版本,以后安装包是,保证是3.3.x, x代表的是最新的版本
    3.3.1		锁定版本,以后安装包时,保证是3.3.1的版本
```











### cnpm

```
第一种: 直接安装-----查看目录less配置

第二种: 替换npm仓库地址为淘宝镜像地址(推荐)
		命令: npm config set registry https://registry.npm.taobao.org
		查看是否成功: npm config get registry
```













### yarn

```
首先,安装yarn
		npm install yarn -g
```



**注意**

```
由于yarn的全局安装位置和npm不同,所以要配置yarn的全局安装路径到环境变量中,否则全局安装的包不起作用
具体操作如下:
	分别执行yarn global dir
		   yarn global bin
	将上述操作的两个结果配置到环境变量中即可
```





```
命令:
	yarn init				初始化项目
	yarn					下载项目中所有的依赖包
	yarn add xxx@yyy		下载指定包
	yarn global add xxx		全局下载指定包
	yarn global remove xxx	全局删除指定包
	yarn remove	xxx			删除指定包
	yarn info xxx			查看某些包的信息
	yarn config set registry https://registry.npm.taobao.org
```













### Buffer缓存器

```
buffer是一个和数组类似的对象,不同的是buffer是专门保存二进制数据的
```



```
特点:
	1. 效率高,读取和存储的速度快,它是直接对计算机的内存进行操作
	2. buffer的大小一旦确定,无法修改
	3. 每个元素占用内存的大小为1字节
	4. buffer是node中一个非常核心的模块,无需下载,直接使用
```



```
创建buffer对象
	1. new Buffer()
		性能特别差
		首先,在堆中开辟空间,然后清理空间中的内容(因为也许开辟的空间中有一些废弃但是还没有被垃圾回收机制清除的内容)
		
	2. new Buffer()
		性能比new Buffer()好一点
		在堆中找到一个没有被使用的空间进行开辟
		
	3. Buffer.allocUnsafe()
		性能最好
		在堆中开辟空间,不进行清理(输出的内容为十六进制,但是存储的是二进制,输出的时候回自动转换成十六进制)
		
	4. Buffer.from()
		将数据存入buffer实例中
```













### node中的文件操作

```
node中有一个文件系统,对计算机中的文件进行增删改查
node中给我们提供了一个模块,叫做fs模块(文件系统),专门用于操作文件
```





#### 简单文件写入

```
 fs.writeFile(file, data[, options], callback)
        file        要写入的文件路径+文件名+后缀
        
        
        data        要写入的数据
        
        
        options     可选参数(配置对象)
            encoding    设置文件的编码方式(默认为utf-8)
            mode        默认值为:0o666
                            0o111: 文件可被执行
                            0o222: 文件可被写
                            0o444: 文件可被读
            flag        打开文件要执行的操作,默认为w
                        a   追加
                        w   写入


        callback    回调函数
            err         错误对象
```







#### 流式文件写入

```

    fs.createWriteStream(path[, options])
        path            路径
        options         配置对象(可选参数)
            flags           打开文件的操作
            encoding        文件的编码方式
            fd              文件的唯一标识符,linux下文件标识符
            mode            文件的权限
            autoClose       自动关闭(文件),默认值为true
            emitClose       关闭(文件----强制关闭),默认值为false
            start       	读取文件的起始位置    




let fs = require('fs')

//创建一个可写流
let ws = fs.createWriteStream('./demo.txt')

//检测流的状态(只要用到流,就必须检测流的状态)
ws.on('open',function () {
    console.log('可写流打开了');
})
ws.on('close',function () {
    console.log('可写流关闭了');
})


//使用可写流写入数据
ws.write('aasbiufd\n')
ws.write('使得即使吧\n')
ws.write('山顶女惊悚的\n')
ws.write('山顶女惊悚的\n')
//ws.close()   //如果在node8版本中,使用此方法会导致文件丢失

ws.end()        //在node8中,要使用end关闭流

```







#### 简单文件读取

```
    fs.readFile(path[, options], callback)
        path            路径
        options         配置对象
        callback        回调
            err         错误对象(如果出现错误,将错误传入到一个对象中)
            data        读取出来的对象(将读取出来的内容传递到一个对象中),读取出来的内容为buffer类型

```





```
简单文件读取和写入,都是一次性把所有要读取或要写入的内容加到内存中,容易造成内容泄露
```







#### 流式文件读取

```
/*
    fs.createReadStream(path[, options])
        path
        options
            flags
            encoding
            fd
            mode
            autoClose
            emitClose
            start                起始偏移量
            end                 结束偏移量
            highWaterMark       控制每次读取数据的大小,默认值为64*1024
 */


let fs = require('fs');

let rs = fs.createReadStream('./MP4/1.mp4', {highWaterMark:10*1024*1024})

let ws = fs.createWriteStream('../小视频.mp4')

rs.on('open', function () {
    console.log('可读流打开');
})
rs.on('close', function () {
    //当可读流关闭时,也就代表着文件以经读取完成,也就代表着文件写入完成,就可以关闭写入流
    ws.close();
    console.log('可读流关闭');
})
ws.on('open', function () {
    console.log('可写流打开');
})
ws.on('close', function () {
    console.log('可写流关闭');
})

//给可读流绑定一个data事件,就会触发可读流自动读取内容
rs.on('data', function (data) {
    //buffer实例的length属性,是表示buffer实例占用内存空间的大小
    //65536
    // 每次读取64kb的内容
    ws.write(data)

})
```



















## 数据库

```
用来存储,组织和管理数据的仓库
```









### 数据库分类

#### 关系型数据库

```
mysql
oracle
DB2
sql server


```

```
优点:
	1. 易于维护: 都是表结构,格式一致
	2. 使用方便: sql通用
	3. 高级查询: 可以在一个或多个表中进行非常复杂的查询
	
缺点;
	1. 读写性能差
	2. 有固定的表结构,不可随意更改,灵活度差
	3. 硬盘i/o是一个很大的瓶颈
```









#### 非关系型数据库

```
MongoDB
redis
```



```
优点:
	1. 灵活: 存储格式为键值对
	2. 速度快: 可以以内存为载体
	3. 易用: 部署简单
	
缺点:
	1. 不支持sql
	2. 不支持事务
	3. 复杂查询时语句过于繁琐
```



```
对于关系型数据库:
	Excel文件 ------ 数据库
	sheet页签 ------ 表
	列	  头	------ 字段
	一	  行 ------ 一条数据
	
对于非关系型数据库:
	Excel文件 ------ 数据库
	sheet页签 ------ 集合		
	列	  头	------ 字段
	一	  行 ------ 一条文档
```







### 端口号

```
1~65535,不建议使用1~199的端口号,这些都是预留给系统的,一般使用4位的,4位的也不要以1开头
```





```
mongod --port 端口号				指定端口号
mongod --dbpath 路径				指定数据库存放的路径
```















### 基本命令

```
db						查看当前在操作哪一个数据库

show dbs				查看数据库列表

use test				切换到test数据库,如果没有,就创建

db.students.insert()	向当前数据库的students集合中插入一个文档

show collections		查看当前数据库的所有集合
```









### 增删改查

增

```
db.集合名.insert(文档对象)					一个
db.集合名.insertOne(文档对象)				一个
db.集合名.insertMany(文档对象)				多个
```



查

```
db.集合名.find()
db.集合名.findOne()
```



改

```
db.集合名.update(查询对象,改)
```



删

```
db.集合名.remove()
```









### mongoose

```
在node平台中更加简单,高效,安全的使用mongodb
```

```js

//引入模块
let mongoose=require('mongoose')


//连接数据库
//useNewUrlParser: true作用: 当前的url解析器有一点问题,输入它会使用新的url解析器
//useUnifiedTopology: true作用: 使用一个新的拓扑结构
mongoose.connect('mongodb://localhost:27017/demo',{useNewUrlParser: true,useUnifiedTopology: true})

//绑定数据库连接的监听
mongoose.connection.on('open',function (err) {
    if(err){
        console.log('数据库连接失败');
    }else{
        console.log('数据库连接成功');
        //操作数据库
        console.log('操作数据库');
    }
})


```







### mongoose的方法

```
创建
	模型对象.create(文档对象,回调函数)
	

```



```js
//引入模块
let mongoose = require('mongoose')
mongoose.set('useCreateIndex', true)       //使用一个新的索引创建器


//连接数据库
//useNewUrlParser: true作用: 当前的url解析器有一点问题,输入它会使用新的url解析器
//useUnifiedTopology: true作用: 使用一个新的拓扑结构
mongoose.connect('mongodb://localhost:27017/demo', {useNewUrlParser: true, useUnifiedTopology: true})

//绑定数据库连接的监听
mongoose.connection.on('open', function (err) {
    if (err) {
        console.log('数据库连接失败');
    } else {
        console.log('数据库连接成功');
        //操作数据库
        //把数据库想象成一个别墅

        //请来一个保安 -------------- 引入模型对象
        let Schema = mongoose.Schema

        //指定进入你家的规则 -------------- 创建约束对象
        let familyRule = new Schema({
            family_id: {
                type: String,   //限制学号必须为字符串
                require: true,   //限制学号必填
                unique: true     //限制学号唯一,不能重复
            },
            name: {
                type: String,   //限制名字必须为字符串
                require: true,   //限制名字必填
            },
            age: {
                type: Number,   //限制年龄必须为字符串
                require: true,   //限制年龄必填
            },
            sex: {
                type: String,   //限制性别必须为字符串
                require: true,   //限制性别必填
            },
            hobby: [String],       //限制爱好只能是数组,数组的每一项只能是字符串
            info: Schema.Types.Mixed,        //接受所有类型
            data: {
                type: Date,          //类型必须是时间类型
                default: Date.now()      //默认值为当前时间
            },
            enable_flag: {
                type: String,
                default: 'Y'
            }
        })

        //告诉保安你的规则 ------------ 创建模型对象
        let familyModel = mongoose.model('family', familyRule)         //用于生成某个集合所对应的模型对象

        //新增操作 ----C
        // familyModel.create({
        //     family_id:'005',
        //     name:'黄以芳',
        //     age:79,
        //     sex:'女',
        //     hobby:['做饭','聊天','打麻将'],
        //     info:888888
        // },function (err,data) {
        //     if(!err){
        //         console.log(data);
        //     }else{
        //         console.log(err);
        //     }
        // })


        //查询操作 ----R

        //find方法:
        //          1.返回一个数组,就算是一条数据,也包裹一个数组
        //          2.如果查询结果为空,返回一个空数组
        // familyModel.find({name:'赖建东'},function (err,data) {
        //     if(!err){
        //         console.log(data);
        //     }else {
        //         console.log(err);
        //     }
        // })

        //findOne方法:
        //            1.若有结果,返回一个对象
        //            2.若没有结果,返回null
        familyModel.findOne({name: '赖传贵'}, {age: 1, _id: 0}, function (err, data) {
            if (!err) {
                console.log(data);
            } else {
                console.log(err);
            }
        })


        //更新操作 ----U

        //updateOne方法: 匹配一个
        //updateMany方法: 匹配多个
        //update方法: 即将被废除
        // familyModel.update({name:'赖建东'},{age:20},function (err,data) {
        //     if(!err){
        //         console.log(data);
        //     }else {
        //         console.log(err);
        //     }
        // })


        //删除操作 ----D

        //deleteOne
        //deleteMany
        // familyModel.deleteOne({age:20},function (err,data) {
        //     if(!err){
        //         console.log(data);
        //     }else {
        //         console.log(err);
        //     }
        // })
    }
})


```







5ca9e773b49ef916541160d2

5ca9e773b49ef916541160d2









### get和post

```
HTTP设定了8种请求方法,这八种方法没有本质上的区别,只是让请求,更加具有语义化而已
```







```
get
	含义: 从指定资源获取数据
```





```
post
	含义: 向指定资源提交要被处理的数据
```







|                  |            get             |            post            |
| :--------------: | :------------------------: | :------------------------: |
|  后退按钮/刷新   |            无害            |      数据会被重新提交      |
|       书签       |        可收藏为书签        |       不可收藏为书签       |
|       缓存       |          能被缓存          |         不能被缓存         |
|       历史       | 参数能被保留在浏览器历史中 | 参数不能保留在浏览器历史中 |
| 对数据长度的限制 |          2048字符          |           无限制           |
|      安全性      |    较差(密码暴露在地址)    |           较安全           |
| 对数据的类型限制 |          ASCII码           |          没有限制          |
|      可见性      |  数据在URL中,对所有人可见  |    数据不会显示在URL中     |





```
get请求
	1. 参数放在哪? -------- 请求地址里
	2. 以什么方式携带? --------- 查询字符串参数
	3. 参数是什么编码形式? -------- urlencoded
	
	
post请求
	1. 参数放在哪? -------- 请求体里
	2. 以什么方式携带? --------- 请求体参数
	3. 参数是什么编码形式? -------- urlencoded
```









### HTTP

```
协议是指计算机通信网络中两台计算机之间进行通信所必须共同遵守的规定

HTTP就是一种通信规则,这个规则规定了客户端和服务端之间通信的报文格式(请求报文和响应报文)
```



```
报文
	
	请求报文: "废话" + 客户端想带给服务器的东西
				请求头 + 请求体
				
	响应报文: "废话" + 服务端给客户端的东西
				响应头 + 响应体
```



```
http协议是什么?
	超文本传输协议(属于应用层)
	特点: 无状态,现在cookie解决了无状态的问题(早期,现在是cookie配合session使用)
	作用: 规定了服务器和客户端传递信息的规则(统称报文)
	版本:
		http 1.0 (老版本) ------- 不支持长连接
		http 1.1 (主流版本) ----- 优点: 支持长连接 缺点: 同时发送资源的数量过小
		http 2.0 (最新版本) ----- 同时发送资源的数量稍有提升
		
报文的组成
	1.报文首行
	2.报文头
	3.空行(分割)
	4.报文体
	
```





### Fiddler

````
一个http协议调试代理工具,可以抓取网页的所有请求和响应,俗称抓包
````







get请求报文(通过form表单)

```
GET http://localhost:7000/?name=%E8%B5%96%E5%BB%BA%E4%B8%9C&age=1111111 HTTP/1.1
Host: localhost:7000
Connection: keep-alive					告诉服务器浏览器支持长连接
sec-ch-ua: "Google Chrome";v="87", " Not;A Brand";v="99", "Chromium";v="87"
sec-ch-ua-mobile: ?0
Upgrade-Insecure-Requests: 1			告诉服务器可以使用https或http1.1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.141 Safari/537.36
	用户代理: 判断用户的浏览器品牌和版本(现在不好用了)
Accept:text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
	浏览器能够接收资源的类型及优先级,
Sec-Fetch-Site: same-site
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Referer: http://localhost:8080/
	本次请求是从哪发出去的			作用: 1.防盗链	2.广告计费
Accept-Encoding: gzip, deflate, br
	浏览器告诉服务器,浏览器所能接受的压缩文件类型
Accept-Language: zh-CN,zh;q=0.9
	浏览器告诉服务器,浏览器所能接收语言种类,及权重
If-None-Match: W/"c-oyoMYrA945W20EsCUUnFxjSLrVE"


```



报文首行

```
GET http://localhost:7000/?name=%E8%B5%96%E5%BB%BA%E4%B8%9C&age=1111111 HTTP/1.1
请求方式 + 协议名://主机地址:端口号/?urlencoded变形时的参数 + 协议名/协议版本
```









post

```
POST http://localhost:7000/ HTTP/1.1
Host: localhost:7000
Connection: keep-alive
Content-Length: 17		数据的长度
Pragma: no-cache
Cache-Control: no-cache
sec-ch-ua: "Google Chrome";v="87", " Not;A Brand";v="99", "Chromium";v="87"
sec-ch-ua-mobile: ?0
Upgrade-Insecure-Requests: 1
Origin: http://localhost:8080
	精简版的referer
Content-Type: application/x-www-form-urlencoded
	告诉服务器.发送的数据的类型
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.141 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: cross-site
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate, br
Accept-Language: zh-CN,zh;q=0.9

name=kebi&age=123         报文体(类型为urlencoded)
```





```
备注:
	1.form表单的post请求和get请求参数均为urlencoded形式进行编码
	2.get请求将urlencoded编码的参数放入请求地址携带给服务器,所以称之为: 查询字符串参数
	3.post请求将urlencoded编码的参数放入请求体中,所以称之为: 请求体参数
```







### post请求体参数的格式

```
Content-Type				post请求报文有,get请求报文并没有,作用: 告诉服务器客户端传入的报文体的格式类型


1. Content-Type: application/x-www-form-urlencoded
	urlencoded类型的参数
	
2. Content-Type: application/json
	json类型的参数
	
3.Content-Type: multipart/form-data
	用于文件上传请求
```











响应头

```
HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: text/html; charset=utf-8
Content-Length: 2
ETag: W/"2-eoX0dku9ba8cNUXvu/DyeabcC+s"
Date: Mon, 18 Jan 2021 11:52:01 GMT
Connection: keep-alive

ok
```

```
报文首行
HTTP/1.1 200 OK
协议名/版本号   状态码
```

```
报文体
X-Powered-By: Express						服务器所采用的框架
Content-Type: text/html; charset=utf-8		告诉浏览器返回资源的类型及编码格式
Content-Length: 2							返回数据的长度
ETag: W/"2-eoX0dku9ba8cNUXvu/DyeabcC+s"		协商缓存必要字段
Date: Mon, 18 Jan 2021 11:52:01 GMT			响应的日期及时间
Connection: keep-alive						服务器告诉浏览器下次请求时或许会采用长连接
```









| 分类 | 分类描述                                       |
| :--- | :--------------------------------------------- |
| 1**  | 信息，服务器收到请求，需要请求者继续执行操作   |
| 2**  | 成功，操作被成功接收并处理                     |
| 3**  | 重定向，需要进一步的操作以完成请求             |
| 4**  | 客户端错误，请求包含语法错误或无法完成请求     |
| 5**  | 服务器错误，服务器在处理请求的过程中发生了错误 |



常见的状态码

```
200			成功
301			重定向,请求的旧资源被移除了,将会跳转到一个新的网址,将旧网址转换为新网址
302			重定向,请求的旧资源还在,但是临时跳转到一个新资源,
304			请求资源重定向到缓存中(命中协商缓存)
500			服务器出现问题
502			服务器连接失败
```

```
200		OK							请求成功
201		Created						已创建(创建成功)
401		Unauthorized				未授权/请求要求用户的身份认证
404		Not Found					服务器无法根据客户端的请求找到资源
500		Internal Server Error		服务器内部错误,无法完成请求
```





### API的分类

```
1. REST API			(restfull)
	1. 发送请求进行CRUD那个操作都是由请求方式决定
	2. 同一个请求路径可以进行多个操作
	3. 请求方式用到 GET/POST/PUT/DELETE
	
	
2. 非REST API		(restless)
	1. 请求方式不决定请求的操作
	2. 一个请求路径对应一个操作
	3. 一般只有GET/POST
```





```
用户输入url按下回车,一直到用户看到页面,经历了什么?
	一.DNS解析(将域名转换为ip地址,优先走缓存)
		1. 先找浏览器DNS缓存解析域名
		2. 找本机DNS缓存(查看本机缓存命令:ipconfig/displaydns > C:/dns.txt)
		3. 找路由器DNS缓存
		4. 找运营商DNS缓存(80%的DNS查找,到这就结束了)
		5. 递归查询(查询全球根DNS服务器(13台))
		
	二.进行TCP(协议)连接,三次握手(根据上一步请求回来的IP地址,去联系服务器)
		第一次握手: 由浏览器发给服务器,我想和你说话,你能听见吗?
		第二次握手: 由服务器发给浏览器,我能听见
		第三次握手: 由浏览器发给服务器,好,那我开始说话了
		
	三.发送请求(请求报文)
	
	四.得到响应(响应报文)
	
	五.浏览器解析html
		预解析: 将所有外部资源请求发出去
		解析html
		解析css
		合并成render数
		js是否操作DOM或样式
			有: 重绘重排
			没有:null
		最终展示页面
		
	六.断开TCP连接,四次挥手
		第一次挥手: 由浏览器发给服务器,我的东西接受完了,你断开把
		第二次挥手: 由服务器发给浏览器,我会有一些东西没有接收完,你等一会,我接收好了且验证好了告诉你 
        		   如果接收完了,你等一会,我要验证数据的完整性
		第三次挥手: 由服务器发给浏览器,我接收完了(验证完了),你断开把
		第四次挥手: 由浏览器发给服务器,好的,我断开了
		
		
为什么挥手要四次,握手要三次?
	握手之前,还没有传输数据,确保握手就行
	挥手之前,正在进行数据的传输,为了确保数据的完整性,必须多经历一次验证
```









### 路由(route)

````
route		路由 ---------- 盒子下的一个一个小接口
router		路由器 -------- 发射WiFi的小盒子
````





request对象属性和方法

|    属性/方法     |                             描述                             |
| :--------------: | :----------------------------------------------------------: |
|  request.query   |          获取get请求查询字符串参数,拿到的是一个对象          |
|  request.params  |          获取get请求参数路由的参数,拿到的是一个对象          |
|   request.body   | 获取post请求体,拿到的是一个对象(要借助一个中间件body-parser) |
| request.get(xxx) |                获取请求头中指定key对应的value                |





response对象属性和方法

|         属性/方法          |                   描述                   |
| :------------------------: | :--------------------------------------: |
|      response.send()       |             给浏览器一个响应             |
|       response.end()       | 给浏览器做出一个响应(不会自动追加响应头) |
|    response.download()     | 告诉浏览器下载一个文件,可以传递相对路径  |
|    response.sendFile()     |  给浏览器发送一个文件,必须传递绝对路径   |
|    response.redirect()     |        重定向到一个新的地址(URL)         |
| response.set(header,value) |             自定义响应头内容             |
|       response.get()       |       获取响应头指定key对应的value       |
|      res.status(code)      |              设置响应状态码              |



```
多个响应以response.send()为主
```









### 中间件

```
概念: 本身就是一个函数,包含三个参数: request,response,next
```



```
作用:
	1. 执行任何代码
	2. 修改请求和响应对象
	3. 终结请求-响应循环
	4. 调用堆栈中的下一个中间件或路由
	
	
分类:
	1. 应用(全局)级中间件
			定义方式1: app.use(function(request,response,next){})
			定义方式2: 函数创建
			
	2. 第三方中间件(body-parser)
			定义方法: app.use(bodyParser.urlencoded({extended: true}))    
			
	3. 内置中间件
			定义方法: app.use(express.urlencoded({extended: true})) 
			
	4. 路由器中间件
```











### 路由器(router)

````
router是一个完整的中间件和路由系统,也可以看做是一个小型的app对象
````



```
作用: 为了更好的管理路由
```

















## ejs模板

```
模板引擎: 根据指定的模板,批量生产多个类似的东西

分类:
	服务器模板引擎
	浏览器模板引擎
```







### 语法











## cookie

```
一般谁生成: 服务器
交给谁保管: 客户端(浏览器)
什么用: 解决http(无状态)
怎么用: 后端在返回响应的同时"种"下(附属操作),客户端下次请求时自动携带
分类: 会话cookie,持久化cookie
```





```
是什么?
	本质就是一个字符串,里面包含着浏览器和服务器沟通(交互)的信息
	存储的形式: key-value形式
	浏览器会自动携带该网站的cookie,只要是该网站的cookie(也就是说多个cookie),全部都会携带
```



```
分类
	会话cookie: 关闭浏览器后,会话cookie会自动消失,会话cookie储存在浏览器运行的那块内存上
	持久化cookie: 看过期时间,一旦到了过期时间,自动销毁,存储在用户的硬盘上,如果用户清理了浏览器缓存,即使没有到时间,也会销毁
```





```
工作原理:
	当浏览器第一次请求服务器时,服务器可能返回一个或多个cookie给浏览器
	
	浏览器判断cookie种类
		会话cookie: 存储在浏览器运行的内存上
		持久化cookie: 存储到用户的硬盘上
	
	以后请求该网站的时候,自动携带上该网站的所有cookie(用户无法干预)
	
	服务器拿到之前自己"种"下的cookie,分析里面的内容,校验cookie的合法性,更距cookie里保存的内容,进行具体的业务逻辑
```



```
应用:
	解决了无状态的问题(列如: 7天免登陆 一般来说不会单独使用cookie,而是配合后台的session储存使用)
```



````
不同的语言,不同的后端构架cookie的具体语法是不一样的,但是cookie的原理和工作过程是不变的
备注:cookie不一定是由服务器生成,前端一样可以生成cookie,但是前端生成的cookie几乎没有意义
````



```
1、设置cookie（给客户端设置‘cookie’):
	直接使用res.cookie('', '', {})
2、获取cookie（需借助第三方中间件):
	* 安装： npm i cookie-parser
	* 引入：const cookieParser = require('cookie-parser')
	* 使用： app.use(cookieParser)
3、返回给客户端一个cookie:
	* res.cookie('username', 'cookieId', {maxAge: 1000 * 60 * 60})
	备注：
		1.cookie是以：key-value的形式存在的，前两个参数分别为：key、value
		2.maxAge用于配置cookie有效期（单位：毫秒）
		3.如果不传入maxAge配置对象，则为会话cookie，随着浏览器的关闭cookie自动会消失
		4.如果传入maxAge，且maxAge不为0，则cookie为持久化cookie，即使用户关闭浏览器，cookie也不会消失，直到过了有效期

4、接收客户端传递过来的cookie：
	* req.cookie.xxx：获取cookie上xxx属性对应的值。
	* 备注：cookie-parser中间件会自动把客户端发送过来的cookie解析到request对象上
```





## session

```
是什么: 
	标椎的来说,session这个单词指的是会话
		1. 前端通过浏览器去查看cookie的时候,会发现有些cookie的过期时间为session,意味着该cookie为会话cookie
		2. 后端人员常常把[seeion会话存储]简称为: session存储,更简单称为; session
```



```
特点:
	1. 存在于服务端
	2. 存储的是浏览器和服务器之间沟通产生的信息
```





```
默认session的存储在服务器的内存中,每当一个新客户端发来请求,服务端都会开辟出一块内存,工session会话存储使用
```





```
工作流程:
	第一次浏览器请求服务器的时候,服务端都会开辟出一块内存,工session会话存储使用
	
	返回响应的时候,会自动返回一个cookie(有时候会返回多个,为了安全),cookie里包含着会话存储"容器"的编号(将session会话存储的id		放入)
	
	以后请求的时候,会自动携带这个cookie,给服务器
	
	服务器从该cookie中拿到对应的session的id,去服务器中匹配
	
	服务器会根据匹配的信息,绝对下一步逻辑
```





```
备注:
	1.一般来说,cookie一定会配合session使用
	2. 服务端一般会做session持久化,为了防止服务器重启,导致session丢失
```





```
操作session
	express-session				该库的作用是: 用于在express中操作session
```





```
1、下载安装：npm i express-session --save 用于express中操作session
2、下载安装：npm i connect-mongo --save 用于将session写入数据库 （session持久化）
3、引入express-session模块：
	* const session = require("express-session")
4、引入connect-mongo模块
	* const MongoStore = require("connect-mongo")(session)
5、编写全局配置对象：
	app.use(session({
		name: 'useId', // 设置cookie的name，默认值是：connect.sid
		secret: 'userValue',	// 参与加密的字符串（又称签名）
		saveUninitialized: false,	// 是否在存储内容之前创建会话
		reserve: true, // 是否在每次请求时，强制重新保存session，即使他们没有变化
		store: new MongoStore({
			url: 'mongodb://localhost:27017/cookies_container',
			touchAfter: 24 * 3600	// 修改频率（例： // 在24小时内只更新一次）
		}),
		cookie: {
			httpOnly: true,	// 开启后前端无法通过JS操作cookie
			maxAge: 1000 * 30	// 设置cookie的过期时间
		}
	}))；
	6、向session中添加一个xxxx,值为yyy：req.session.xxxx = yyyy
	7、获取session上的xxx属性：const {xxxx} = req.session
```







### session持久化

```
connect-mongo
```













## 加密

```
只要加密的是同一个明文,加密后的密文都一样
密文是不可以逆向转为明文
明文加密后变成密文
```



```
MD5
sha1 
```









## ajax

```
就是异步的js和XML
通过ajax可以在浏览器中向服务器发送异步请求,最大的优势: 无刷新获取数据
```









### XML

```
XML: 可扩展标记语言
XML被设计用来运输和存储数据
XML和HTML类似,不同的是HTML中都是预定义标签,二XML中没有预定义标签,全都是自定义标签,用来表示一些数据
但是现在已被JSON代替
```









```
ajax的特点:
	1. 可以无需刷新页面而与服务器端进行通信
	2. 允许你根据用户事件来更新部分页面内容
	
	
ajax的缺点:
	1. 没有浏览历史,不能回退
	2. 存在跨域问题
	3. SEO不友好
```







```
ajax的五种状态
	0: xhr对象在实例化出来的那一刻,就已经是0状态了,代表着xhr是初始化状态
	1: send方法还没有被调用,即请求没有发出去,此时依然可以修改请求头
	2: send方法被调用了,即: 请求已经发出去了,此时已经不可以修改请求头
	3: 已经回来一部分数据了,如果是比较小的数据,会在此阶段一次性接收完毕
	4: 数据完美的回来了
	
	我们几乎不会在0状态中去做任何事,因为0状态永远进不去onreadystatechange事件,只有0改变才能进
	
	xhr.setRequestHeader();		设置请求头
```





```
form-post: 自动将参数转换为urlencoded形式

ajax-post: 需要加上一个请求头xhr.setRequestHeader('Content-Type','application/x-www-form-urlencoded'),将参数转换为urlencoded形式参数

```









### ajax跨域问题

````
ajax可以发送请求,但是浏览器接收不到
````



```
为什么会有跨域这个问题?
	原因是浏览器为了安全,而采用的同源策略
```





``````
什么是同源策略?
	1. 同源策略是由Netscape提出的一个著名的安全策略,现在所有JavaScript的浏览器都会是由这个策略
	2. web是构建在同源策略上的,浏览器只是针对同源策略的一种实现
	3. 所谓同源,也称为同域,是指: 协议,域名,端口必须要完全相同,即: 协议,域名,端口都相同,才能算是在同一个域里
``````





```
非同源受到哪些限制
	1. cookie不能读取
	2. DOM无法获得
	3. ajax请求不能获取数据
```



```
form跨域 ------ 不拦截
ajax跨域 ------ 拦截

原因: ajax发的请求经过ajax引擎,ajax引擎遵守同源策略
	 form发的请求经过的是浏览器其他模块,不遵守同源策略限制
```





```
get
	1. form ------ 不受同源限制
	2. ajax ------ 受同源限制
	3. 浏览器地址栏 ------ 不受同源限制 
	4. html中引入外部资源的标签		img,link,script    ------ 不受同源限制
```









### Node综合复习



**使用node搭建原生服务器**

````javascript
/*
    不借助任何第三方库,去搭建node原生服务器
 */

//node中内置模块
let http = require('http')

//引入一个内置模块,用于解析key=value&key=value.....这种形式的字符串为js中的对象
//形如: key=value&key=value...编码形式: urlencoded编码形式
//请求地址里携带urlencoded编码形式的参数,叫做: 查询字符串参数
let qs=require('querystring')

//创建服务对象

let server=http.createServer(function (request,response) {
    //request       请求对象(包含着客户端给服务端的东西)
    //response      响应对象(包含着服务端返回给客户端的东西)

    //获取客户端携带过来的urlencoded编码形式的参数
    let params=request.url.split('?')[1];
    let paramsObj=qs.parse(params)
    console.log(paramsObj);
    let{name,age}=paramsObj

    response.setHeader('content-type','text/html;charset=utf-8')

    response.end(`<h1>你好${name},我的年龄是${age}</h1>`)

})


//指定服务器运行的端口号(绑定端口监听)
server.listen(4000,function (err) {
    if(!err){
        console.log('服务器启动成功');
    }else {
        console.log(err);
    }
})
````





**使用express搭建服务器**

```javascript
const express = require('express')


//1.服务员
const app = express()

//禁止服务器返回X-Powered-By
app.disable('x-powered-by')


//2.配置路由 ------ 对请求的url进行分类,服务器根据分类决定交给谁去处理
        //在node.js中,我们所有说路由指的是后端路由
        //路由可以理解为一组组key-value的组合     key:请求方式+ url        value:回调函数
        //根据路由定义的顺序,将定义好的路由放入一个类似于数组的结构中,一次取出,若匹配成功,不继续匹配
app.get('/',function (request,response) {
    /*
        什么样的请求,能交给这个回调函数处理?
            1.必须是get请求
            2.请求的URL必须为"/meishi"
     */
    console.log(request.query);
    response.send('我是主页')
})

app.get('/meishi',function (request,response) {
    response.send('我是美食页面')
})

app.get('/meishi/huoguo',function (request,response) {
    response.send('我是美食--火锅页面')
})

app.post('/',function (request,resoponse) {

})


//监听
app.listen(7000,function (err) {
    if(!err){
        console.log('服务器连接成功');
    }else{
        console.log(err);
    }
})

```





```

//用于暴露静态资源
app.use(experss.static(__dirname + '/public'))
//用于解析post请求的urlencoded参数
app.use(experss.urlencoded({extended: true}))


```





**路由**

```
//路由是express中的一个方法
const {Router} = require('express')


//创建路由器(router实例)
let router = new Router()


//返回路由
module.exports = function () {
    return router
}
```

**服务器**

```
//引入路由
const UIRouter=require('./router/UIRouter')
const loginRegisterRouter=require('./router/loginRegisterRouter')


//调用路由
app.use(UIRouter())
app.use(loginRegisterRouter())
```









**cookie**

```javascript
const express=require('express')

const cookieParser=require('cookie-parser')
const app=express()

app.use(cookieParser())
app.get('/demo',(req,res)=>{
    res.send('我是demo路由给你的反馈,我没有对cookie进行任何的操作')
})

app.get('/demo1',(req,res)=>{

    //express中给客户端种cookie不需要任何的第三方库
    let user={name:'laijiandong',age:12}
    res.cookie('peiqi',JSON.stringify(user))    //给客户端种下一个会话cookie


    res.send('我是demo1路由给你的反馈,我种下了一个会话cookie,去看看吧')
})

app.get('/demo2',(req,res)=>{

    //express中给客户端种cookie不需要任何的第三方库
    let user={name:'laijiandong',age:12}
    res.cookie('peiqi',JSON.stringify(user),{maxAge:1000*30})    //给客户端种下一个持久化cookie


    res.send('我是demo1路由给你的反馈,我种下了一个持久化cookie,去看看吧')
})

app.get('/demo3',(req,res)=>{
    //express读取客户端携带过来的cookie要借助一个中间件,cookie-parser
    console.log(req.cookies);
    let {peiqi}=req.cookies
    console.log(peiqi);
    console.log(JSON.parse(peiqi).name);
    res.send('你去看看服务器吧')
})

app.get('/demo4',function (req,res) {
    //删除cookie
    //方法1
    res.cookie('peiqi','',{maxAge:0})
    //方法2(方法中必须写入对应cookie的名字)
    // res.clearCookie('peiqi')
    res.send('已删除')
})


app.listen(8000,(err)=>{
    if(err){
        console.log(err);
    }else{
        console.log('服务器连接成功');
    }
})
```















## Promise





### error

```
错误的类型:
		Error: 所有错误的父类型
		ReferenceError: 引用的变量不存在
 　　    TypeError: 数据类型不正确的错误
 　　    RangeError: 数据值不在其所允许的范围内
 　　    SyntaxError: 语法错误
```



```
错误处理:
	捕获错误: try.......catch
	抛出错误: throw Error
```



```
错误对象:
	message属性: 错误相关信息
	stack属性: 函数调用栈记录信息
```



````
将错误捕获后进行处理,代码可以继续向后面运行,不会卡顿
````







### Promise理解

````
Promise是JS中进行异步编程的新解决方案


从语法上来说,Promise是一个构造函数
从功能上来说: Promise对象用来封装一个异步操作并可以获取其成功/失败的结果值
````



```
为什么使用promise?
	支持链式调用,可以解决回调地狱
	
```





```js
<script>                              // 成功    失败
var promise1 = new Promise(function (resolve, reject) {      //excutor     执行器函数     同步回调函数
    //开始时promise的状态为pending     未确定的/初始化
    //启动异步操作
    console.log('初始化状态');
    setTimeout(function () {
        //成功了
        resolve('foo')     //promise的状态变为resolved/成功,同时指定成功的value
    }, 1000)
})
console.log('初始化结束');
promise1.then(function (value) {          //异步执行的成功的回调函数
    console.log('成功');
    console.log(value);
})
console.log(promise1);
</script>

```







```
promise的状态改变
	1. pending 变为 resolved
	2. pending 变为 rejected
	
说明: 只有两种,且一个promise对象只能改变一次,无论变为成功还是失败,都会有一个结果数据
	 成功的结果数据一般称为value,失败的结果一般称为reason
```



​                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     



````
resolve(1)          //pending ----- resolved
reject(2)           //pending ----- rejected
throw 3             //pending ----- rejected(抛出异常)
````











### 宏队列和微队列

![宏队列和微队列](C:\Users\86188\Pictures\Camera Roll\宏队列和微队列.png)



```
JS 中用来存储待执行回调函数的队列包含 2 个不同特定的列队
	宏列队：用来保存待执行的宏任务（回调），比如：定时器回调、DOM 事件回调、ajax 回调
	微列队：用来保存待执行的微任务（回调），比如：promise的回调、MutationObserver 的回调

JS 执行时会区别这 2 个队列
	JS 引擎首先必须先执行所有的初始化同步任务代码
	每次准备取出第一个宏任务执行前, 都要将所有的微任务一个一个取出来执行，也就是优先级比宏任务高，且与微任务所处的代码位置无关
```

















## json-server

```
全局下载		npm install -g json-server
```



```
写一个json文件
	
	{
  "posts": [
    { "id": 1, "title": "json-server", "author": "typicode" }
  ],
  "comments": [
    { "id": 1, "body": "some comment", "postId": 1 }
  ],
  "profile": { "name": "typicode" }
}
```





```
运行			json-server --watch db.json
```



```
C:\Users\86188\Desktop\js高级项目文件夹\json-server>json-server --watch db.json

  \{^_^}/ hi!

  Loading db.json
  Done

  Resources						分支,路由
  http://localhost:3000/posts
  http://localhost:3000/comments
  http://localhost:3000/profile

  Home			主页面
  http://localhost:3000

```





```
操作json文件

	get				查
	 	http://localhost:3000/posts				查看所有
	 	http://localhost:3000/posts/1			查看id为1的json数据
	 	
	 
	 post			增
	 	http://localhost:3000/posts				传入的地址
	 	title=aaa       author=bbb				传入的值(id可以不写,会自动加上)
	 	
	 
	 put			改
	 http://localhost:3000/posts/1				更改id为1的json数据
	 	title=aaa       author=bbb				清空所有的值,但是不会清空id,传入指定的内容
	 	
	 
	 delete			删
	 http://localhost:3000/posts/1				删除id为1的json数据
```











## xhr对象

```
使用XMLHttpRequest对象可以与服务器交互,也就是发送ajax请求

前端可以获取到数据,并且无需刷新整个页面

这使得web页面可以只更新页面的局部,而不影响整个页面
```





**区别一般的http请求和ajax请求**

```
1. ajax请求是一种特别的http请求
2. 对服务器端来说,没有任何分别,区别在于浏览器端
3. 浏览器端发请求: 只有XHR或fetch发出的才是ajax请求,其他所有的都是非ajax请求
4. 浏览器端收到响应
	(1). 一般请求: 浏览器一般会直接显示响应体数据,也就是刷新/跳转页面
	(2). ajax请求: 浏览器不会对界面进行任何更新操作,只是调用监视的回调函数并传入响应相关的数据
```





**API**

```
1. XMLHttpRequest()							创建XHR对象的回调函数
2. status									响应状态码值
3. statusText								响应状态文本
4. readyState								请求的状态
5. onreadystatechange						绑定状态改变的监听
6. responseType								指定响应数据类型,比如'json',得到响应后自动解析响应体数据为json格式
7. response									响应体数据
8. timeout									指定请求超时时间,默认为0代表没有限制
9. ontimeout								绑定超时的监听
10. onerror									绑定请求网络错误的监听
11. open()									初始化一个请求
12. send(data)								发送请求
13. abort()									终端请求
14. getResponseHeader(name)					获取指定名称的响应头值
15. getAllResponseHeaders()					获取所有响应头组成的字符串
16. setRequsetHeader(name,value)			设置请求头

```

​				











## axios

```
1. 函数的返回值为promsie类型的对象,成功的结果为response,失败的结果为error
2. 能处理多种类型的请求: get/post/put/delete
3. 函数的参数为一个配置对象
    {
    url:'',				请求的地址
    method:'',			请求类型
    params:{},			det/delete请求的query参数
    data:{},			post/put请求的请求体参数

    }
4. 响应的json数据自动解析为js对象/数组
```







### 对象遍历方法



**方法1**

````
使用keys方法遍历对象


    Object.keys(obj).forEach(key=>{
        console.log(obj);               //遍历后的数组对象
        console.log(key);               //键
        console.log(obj[key]);          //值
    })
    
````





**方法2**

```
使用for....in遍历

for (let key in obj){
        console.log(obj);                   //对象
        console.log(key);                   //键
        console.log(obj[key]);              //值
    }
```







### url上的2种请求参数

```
query参数:
	路由path: /xxx
	请求path: /xxx?username=xxx&password=yyy
	获取参数: req.query.username  /  req.query.password
	
	
params参数:
	路由path: /xxx/:username/:password
	请求path: /xxx/laijiandong/150187aabb
	获取参数: req.params.username  /  req.params.password
```









### 不同请求的作用

```
get				从服务器端读取数据
post			向服务器添加新的数据
put				更该(更新)服务器中的数据
delete			删除服务器数据
```











### 初识axios

```
1. 前端最流行的ajax请求库
2. react/vue官方都推荐使用axios发ajax请求
```



**特点**

```
1. 基于promise的异步ajax请求库
2. 浏览器端/node端都可以使用
3. 支持请求/响应拦截器
4. 支持请求取消
5. 请求/响应数据转换
6. 批量发送多个请求
```













### 源码分析



```
axios的由来:
	首先,使用var axios = createInstance(defaults);来调用函数,参数为配置对象
	
	
	函数被调用
            function createInstance(defaultConfig) {
            	//调用Axios方法实例化一个对象,参数为调用此函数传入的配置对象
              var context = new Axios(defaultConfig);
              	//将第一个参数的内容给instance,this指向context(第一个参数的作用是发送请求)
              var instance = bind(Axios.prototype.request, context);

              // 将Axios原型对象上的方法(post,put,get)属性和实例对象context上的方法复制给instance,
              utils.extend(instance, Axios.prototype, context);

              // 将context上的方法(默认配置和拦截器)复制给instance
              utils.extend(instance, context);

				//返回的instance(此时instance就是一个axios)
              return instance;
            }
            
	
	Axios方法
		function Axios(instanceConfig) {
			//默认的配置对象为传入的参数
          this.defaults = instanceConfig;
          	//拦截器
          this.interceptors = {
            request: new InterceptorManager(),
            response: new InterceptorManager()
          };
        }
```





 

#### 发送请求代码分析

```javascript
Axios.prototype.request = function request(config) {
  //对传入的配置进行一些操作
  if (typeof config === 'string') {
    config = arguments[1] || {};
    config.url = arguments[0];
  } else {
    config = config || {};
  }

	//将默认的配置对象和传入的配置对象做一个合并(如果传入的配置对象中的属性或方法和默认配置对象有重复,则优先使用传入的配置对象)
  config = mergeConfig(this.defaults, config);

  // 对请求方法做一个判断
  if (config.method) {
    config.method = config.method.toLowerCase();
  } else if (this.defaults.method) {
    config.method = this.defaults.method.toLowerCase();
  } else {
    config.method = 'get';
  }

  // 创建拦截中间件,第一个参数用来发送请求,第二个参数用来补位
  var chain = [dispatchRequest, undefined];
  // 创建一个promise对象,状态为成功,值为合并过后的配置对象
  var promise = Promise.resolve(config);

    //遍历实例对象的请求拦截器
  this.interceptors.request.forEach(function unshiftRequestInterceptors(interceptor) {
      //将请求拦截器压入数组的最前面
    chain.unshift(interceptor.fulfilled, interceptor.rejected);
  });

    //遍历实例对象的响应拦截器
  this.interceptors.response.forEach(function pushResponseInterceptors(interceptor) {
      //将响应拦截器压入数组的最后面
    chain.push(interceptor.fulfilled, interceptor.rejected);
  });

    //当chain数组长度不为1时,遍历执行,先执行请求拦截器,再执行请求,最后执行响应拦截器
  while (chain.length) {
      //chain.shift()弹出指定数组中第一个元素,也就是说会执行dispatchRequest,发送请求
    promise = promise.then(chain.shift(), chain.shift());
  }

  return promise;
};
```



dispatchRequest源码分析

```javascript
function dispatchRequest(config) {
	//如果被取消的请求发出去,抛出错误
  throwIfCancellationRequested(config);

  // 确保头信息存在
  config.headers = config.headers || {};

  // 对请求数据进行初始化转换
  config.data = transformData(
    config.data,
    config.headers,
    config.transformRequest
  );

  // 对请求头信息做一个整合
  config.headers = utils.merge(
    config.headers.common || {},
    config.headers[config.method] || {},
    config.headers
  );

    //将配置项中关于方法的配置项全部移除
  utils.forEach(
    ['delete', 'get', 'head', 'post', 'put', 'patch', 'common'],
    function cleanHeaderConfig(method) {
      delete config.headers[method];
    }
  );

    //获取适配器对象(http或xhr)
  var adapter = config.adapter || defaults.adapter;

    //适配器发送请求后返回一个promise类型的数据,然后使用then进行成功或错误的操作
  return adapter(config).then(function onAdapterResolution(response) {
    throwIfCancellationRequested(config);

    // 对响应的结果做一些处理
    response.data = transformData(
      response.data,
      response.headers,
      config.transformResponse
    );

    return response;
  }, function onAdapterRejection(reason) {
    if (!isCancel(reason)) {
      throwIfCancellationRequested(config);

      // Transform response data
      if (reason && reason.response) {
        reason.response.data = transformData(
          reason.response.data,
          reason.response.headers,
          config.transformResponse
        );
      }
    }

    return Promise.reject(reason);
  });
};
```

```
dispatchRequest函数执行完毕意味着发送请求的代码执行完毕,也就意味着axios执行完毕
```

```
axios函数对象上的原型对象上的request函数执行,进入到dispatchRequest函数中,再进入到指定适配器的函数中,
适配器返回结果到dispatchRequest函数中,dispatchRequest函数做一些处理,返回到request函数中,然后就可以
进行成功或失败的回调了
```









#### 拦截器代码分析

```
当我们使用axios方法时,会创建Axios方法的实例对象(实例对象中包含默认配置和拦截器),然后将实例对象中的内容复制到axios函数方法中

		function Axios(instanceConfig) {
			//默认的配置对象为传入的参数
          this.defaults = instanceConfig;
          	//拦截器
          this.interceptors = {
            request: new InterceptorManager(),
            response: new InterceptorManager()
          };
        }

Axios方法中会执行InterceptorManager.js中两个函数
```

**InterceptorManager.js**

````javascript
'use strict';

//拦截器管理器构造函数
var utils = require('./../utils');

function InterceptorManager() {
    //创建一个属性
  this.handlers = [];
}

/**
 * Add a new interceptor to the stack
 *
 * @param {Function} fulfilled The function to handle `then` for a `Promise`
 * @param {Function} rejected The function to handle `reject` for a `Promise`
 *
 * @return {Number} An ID used to remove interceptor later
 */
InterceptorManager.prototype.use = function use(fulfilled, rejected) {
  this.handlers.push({
    fulfilled: fulfilled,
    rejected: rejected
  });
  return this.handlers.length - 1;
};

/**
 * Remove an interceptor from the stack
 *
 * @param {Number} id The ID that was returned by `use`
 */
InterceptorManager.prototype.eject = function eject(id) {
  if (this.handlers[id]) {
    this.handlers[id] = null;
  }
};

/**
 * Iterate over all the registered interceptors
 *
 * This method is particularly useful for skipping over any
 * interceptors that may have become `null` calling `eject`.
 *
 * @param {Function} fn The function to call for each interceptor
 */
InterceptorManager.prototype.forEach = function forEach(fn) {
  utils.forEach(this.handlers, function forEachHandler(h) {
    if (h !== null) {
      fn(h);
    }
  });
};

module.exports = InterceptorManager;

````









#### 取消请求代码分析

```javascript
function CancelToken(executor) {
    //执行器函数必须是一个函数类型,否则报错
  if (typeof executor !== 'function') {
    throw new TypeError('executor must be a function.');
  }

    //申明一个变量
  var resolvePromise;
    
    //实例对象上添加一个promise属性
  this.promise = new Promise(function promiseExecutor(resolve) {
      //将修改promise状态的函数暴露出去
    resolvePromise = resolve;
  });

  var token = this;
    //往传入的函数中添加一个函数类型的参数,也就是说cancel函数 === c
  executor(function cancel(message) {
    if (token.reason) {
      // Cancellation has already been requested
      return;
    }

    token.reason = new Cancel(message);
    resolvePromise(token.reason);
  });
}
```





xhr.js中

```javascript
//判断传入的配置对象中是否有canceToken这个属性
if (config.cancelToken) {
      // Handle cancellation
      config.cancelToken.promise.then(function onCanceled(cancel) {
        if (!request) {
          return;
        }

          //取消请求
        request.abort();
        reject(cancel);
        // Clean up request
        request = null;
      });
    }
```



```
首先,当我们执行了cancel()时,就会执行CancelToken函数中的resolvePromise,随之就会改变promise的状态,改变之后就会调用xhr.js中
的成功的回调,从而取消请求
```









#### 源码分析总结

```
axios和Axios的关系
	从语法上来说; axios不是Axios的实例
	从功能上来说: axios是Axios的实例
	axios是Axios.prototype.request函数bind()返回的函数
	axios作为对象有Axios原型对象上所有的方法,有Axios上所有的属性
```





```
instance和axios的区别
	相同:
		1. 都可以发请求
		2. 都有发特定请求的各种方法
		3. 都有默认配置和拦截器
		
	不同:
		1. 默认配置有可能不一样
		2. instance没有axios上的一些后面添加的方法: create/canceltoken/all等等
```





















## webpack

```
src --- 源代码 ---程序员写的没有经过任何加工的代码
dist---	加工后的代码 --- 经过层层的加工处理的代码



构建: 将程序写的源代码,经过编译,压缩,语法检查,兼容性处理,生成浏览器可以高效,稳定运行的代码


构建工具: 
		1. grunt
		2. gulp
		3. webpack
```













### 了解

```
什么是webpack?
	webpack是一个模块打包器
	在webpack看来,前端的所有资源文件都会作为模块处理
	它将根据模块的依赖关系进行静态分析,生成对应的静态资源
```



```
五个核心概念
	Entry: 入口起点(entry point)指示webpack应该使用哪个模块,来作为构建其内部依赖图的开始
	OutPut: output属性告诉webpack在哪里输出它所创建的bundles,以及如何命名这些文件,默认值为./dist
	loader: 让webpack能够去处理那些非JavaScript文件(webpack本身只能解析JavaScript,json)
	plugins: 插件则可以用于执行范围更广的任务,插件的范围包括,从打包优化和压缩,一直到重新定义环境中的变量等
	mode: 模式,有生产模式(production)和开发模式(development)
```













### 使用

1.初始化项目

```
npm init
```





2.安装webpack

```
首先,要在全局和包内安装webpack和webpack-cli
npm i  webpack@4.29.4 webpack-cli@3.2.3 -g
npm i  webpack@4.29.4 webpack-cli@3.2.3 -D

```



yarn add -D typescript  webpack-dev-server webpack@4.29.4 webpack-cli@3.2.3 html-webpack-plugin clean-webpack-plugin ts-loader cross-env

3. 使用

```
将当前位置下的src下的js下的index.js经过webpack编译生成到dist下

webpack ./src/js/index.js -o ./dist/js/index.js --mode development
		生成的代码没有压缩

webpack ./src/js/index.js -o ./dist/js/index.js --mode development
		生成的代码压缩了
```





结论

```
优点:
    webpack能够编译打包js和json文件
    能将es6的模块化语法转换成浏览器能识别的语法
    能压缩代码
    
缺点:
	不能编译打包css,img,音视频等文件
	不能将js的es6基本语法转换为es5以下语法
	
	
改善: 使用webpack配置文件解决,自定义功能
```









### 配置

```
由于写命令太过麻烦,我们可以写配置文件,从而简化命令
```







1.创建配置文件

```
在项目的根目录下创建一个webpack.config.js的文件
```





2.配置文件

```js
/*
    此文件是webpack的配置文件,用于指定webpack去执行那些任务
 */

const {resolve}=require('path')
//由于webpack是基于node运行的,所以必须使用commonjs来暴露对象(对象内容为webpack的配置)
module.exports={
    entry: './src/js/index.js',      //入口
    output:{
        //也就是说: 第一个属性创建文件夹,第二个属性创建文件
        path: resolve(__dirname+'/dist/js'),       //输出路径(由于必需是绝对路径,所以要这样写)
        filename: "index.js"      //输出的文件名
    },
    mode:'production'           //配置模式(分为生产模式(production)和开发模式(development),生产为压缩编译后的代码,开发则不压缩,就编译)
}


```





3.输入命令

```
在控制台输入webpack即可
```









### loader

```
让webpack能够去处理那些非JavaScript文件(webpack本身只能解析JavaScript,json)
```





#### 解析样式

```
第一步
	安装loader
	yarn add css-loader less-loader style-loader less -D
	
	  style-loader    			   	用于在html文档中创建一个style标签,将样式塞进去(把js中的css转移到html的style标签中)
      css-loader      				 将less编译后的css转换为commonJS的一个模块(将css打包到js中去)
      less-loader@4.0.5      		 编译less为css,但不生成单独的css文件,(编译之后在内存中)
      less							使webpack认识less文件
```





```
使用一个loader

module: {
        rules: [
            {
                test:/\.less$/,                 //匹配所有less文件
                loader: 'less-loader'           //使用less-loader,将less编译为css
            },
        ]
    }
    
    
    
    
使用多个loader
module: {
        rules: [
            {
                test:/\.less$/,                 //匹配所有less文件
                use: [{
                    loader: "style-loader" 
                }, {
                    loader: "css-loader" 
                }, {
                    loader: "less-loader" 
                }],
            },
        ]
    }
    
    
    
    
使用多个loader(简写方式)
module: {
        rules: [
            {
                test:/\.less$/,                 //匹配所有less文件
                use: ['style-loader','css-loader','less-loader'],
            },
        ]
    }
```









#### js语法检查

```
作用: 对js基本语法错误/隐患,进行提前检查
```



```
安装loader	
		npm i eslint-loader eslint -D
```



```
配置
		{
                test: /\.js$/,
                exclude: /node_modules/,            //排除node_modules文件夹中的js
                use:{loader: "eslint-loader"},
                enforce: "pre",                     //提前加载使用

            }
            
            
            
            
在package.json中写入:
"eslintConfig": {
    //解释器配置
    "parserOptions": {
      "ecmaVersion": 6,       //支持es6语法
      "sourceType": "module"      //支持es6模块化
    },
    //设置环境
    "env": {
      "browser": true,        //支持浏览器环境,能够使用window上的全局变量
      "node": true            //支持服务器环境,能够使用node上的global的全局变量
    },
    "globals": {              //申明使用的全局变量,这样即使没有定义也不会报错了
      "$": "readonly"         //$    只读变量
    },
    "rules": {                //eslink检查规则      0  忽略     1  警告     2  错误
      "no-console": 0,        //不检查console
      "eqeqeq": 2,            //用 == 而不用 === 报错
      "no-alert": 2           //不能使用alert
    },
    "extends": "eslint:recommended"       //使用eslint推荐的默认规则,上面定义的规则会覆盖掉原来的指定规则
  }
```









#### js语法转换

```
作用: 将浏览器不能识别的语法转换为能被识别的旧语法,做浏览器兼容处理
```



```
安装loader
		npm install -D babel-loader @babel/core @babel/preset-env
```



```
配置
{
      test: /\.js$/,
      exclude: node_modules,
      use: {
        loader: 'babel-loader',
        options: {
          presets: ['@babel/preset-env']
        }
      }
    }
```













#### js兼容性处理

```
es6中的promise无法通过语法转换转换为es5认识的语法
我们可以在package.json中的 "globals": {
     						 "$": "readonly",
      						"Promise": "readonly"
   						 },
   						 
但是无法在ie浏览器中使用
所以要使用到js兼容性处理
```



**第一种办法----------使用经典的polyfill**

````
安装
	npm install @babel/polyfill
````



```
在index.js中导入
import '@babel/polyfill'            //包含ES6的高级语法的转换
```





```
优点: 解决了babel只能转换部分低级语法的问题,引入polyfill可以转换高级语法

缺点: 将所有高级语法都进行转换,使得编译后的文件大大增大

解决: 按需引入
```









**第二种办法---------借助按需引入core-js按需引入**



````
优势: 编译后的文件不大
````



```
安装
	npm i core-js
```



```
{
                test: /\.js$/,
                exclude: /node_modules/,
                use: {
                    loader: 'babel-loader',
                    options: {
                        presets: [
                            [
                                '@babel/preset-env',
                                {
                                    useBuiltIns: 'usage',       //按需引入需要使用polyfill
                                    corejs: {version: 3},       //解决不能够找到corejs的问题
                                    targets: {                  //指定兼容性处理那些浏览器
                                        "chrome": "58",
                                        "ie": "9"
                                    }
                                }
                            ]
                        ],
                        cacheDirectory: true,                     //开启babel缓存(解析快一些)
                    }
                }
            }
```



```
注意:
	要注释掉index.js中写入的引入import '@babel/polyfill'   
```











#### 注意

```
使用webpack进行js语法转换和样式解析时,webpack的版本要低于5,最好为4,全局和局部的版本要一致
否则语法转换后的代码依然含有箭头函数
less-loader的版本也要为低版本,不然会报错
```









#### 打包样式文件中的图片资源

```
安装
	npm install url-loader -D
	npm install file-loader -D
```

```
区别
	url-loader的功能和file-loader的功能一样,但是,url-loader多了一个功能(识别图片大小)
	
	使用url-loader必须安装file-loader,因为url-loader是对象file-loader的上层封装,使用时需配合file-loader使用
```

```
使用

{
                test: /\.(png|jpe?g|gif)$/i,
                use: [
                    {
                        loader: 'url-loader',
                        options: {
                            limit:8192,                         //小于8kb的图片会自动转换为base64处理
                            outputPath: 'images',               //决定文件本地输出路径
                            publicPath:'../dist/images',        //决定图片的url路径
                            name: '[hash:5].[ext]',             //修改文件名称[hash:5] hash值取前8位  [ext]   文件拓展名
                        }
                    },
                ],
            }
```











#### 打包html文件

```
概述: html文件webpack不能解析,需要借助插件编译解析
```



```
安装
	npm install html-webpack-plugins -D
```



```
使用

    引入
    const HtmlWebpackPlugin = require('html-webpack-plugin')
    
    使用
    plugins: [new HtmlWebpackPlugin({
        template: './src/index.html'            //以当前文件为模板创建新的html(1. 结构和原来一样   2. 会自动引入打包的资源)
    })]
```









#### 打包html中图片资源

```
概述: html中的图片url-loader没法处理,它只能处理js中引入的图片/样式中引入的图片,不能处理html的img标签,需要引入其他html-loader处理
```





```
安装
	npm i html-loader -D
```



```
使用
	{
                test: /\.(html)$/,
                use:{
                    loader: "html-loader"
                }
            },
```









#### 打包其他资源

```
使用file-loader可以打包其他资源
```





**引入图标字体**

```
第一步
	下载图标字体代码
	将iconfont.css引入到src下的css中,并且将后缀改为less
	

第二步
	将iconfont.eot  iconfont.svg  iconfont.woff  iconfont.woff2  iconfont.ttf引入到src下的font文件夹中
	
	
第三步
	在index.js中引入图标字体的less文件			import '../css/iconfont.less'        
	
	
第四步
	使用file-loader处理其他资源
            {
                test: /\.(eot|svg|woff|woff2|ttf|mp3|mp4|avi)$/,        //处理其他资源
                loader: 'file-loader',
                options: {
                    outputPath: 'media',			//将资源放入dist的media文件夹中
                    name: '[hash:5].[ext]'          //取hash值的前5位并且保留后缀
                }
            }
```













#### 自动编译打包运行



```
安装
	npm i webpack-dev-server -D
```





```
配置命令
	在package.json中
	"scripts": {
    "a": "webpack"
  	},
  	 
然后我们可以在命令行中输入 npm run a		即可执行webpack命令

注意: 当名字设为start时,输入命令可以不加run
```





```
第一步
	在package.json中的"scripts"中输入
		"start":"webpack-dev-server"
		
		
第二步
	在webpack.config.js中
	//配置自动化编译
    devServer: {
        open: true,         //自动打开浏览器
        // compress: true,     //启动gzip压缩
        port: 3000          //端口号
    }
    
   
第三步
	修改url-loader的部分配置
	由于构建工具以dist为根目录,所以不用再找dist
	所以将
		publicPath: '../dist/images/', 
	改为
		publicPath: 'images/', 
		
		
```











#### 热模替换功能

```
概述: 热模替换功能(HMR)是webpack提供的最有用的功能之一,它运行在运行时更新所以类型的模块,而无需完全刷新(只更新变化的模块,不变的模块不更新)
```



```
自动刷新		live reload   			webpack-dev-server自带

热模替换(模块热更新)			HMR
```



```
实现
	在devServer中添加属性			hot:true,			开启热模替换
```





```
问题
	开启热模替换后,修改html文件中的内容无法自动刷新,需要手动刷新
	
解决办法
	由于刷新的文件时入口文件,所以,我们可以写入多个文件
	 entry: ['./src/js/index.js','./src/index.html'],      //入口
```





```
结果
	当我们修改样式时,页面会局部刷新
	当我们修改html文件时,页面会全局刷新
	
	html不支持热模替换,样式支持热模替换
```











#### devtool

```
概述: 是一种将压缩文件/编译文件中的代码映射回源文件中的原始位置的技术,让我们调试代码不再困难
```



```
使用
	在webpack.config.js中写入
	
		devtool: "cheap-module-eval-source-map"
```





```
推荐使用
	开发环境: cheap-module-eval-source-map
	生产环境: cheap-module-source-map
```











#### 准备生产环境

```
创建文件夹config(config文件夹在根目录下),将webpack.config.js复制两份
	webpack.dev.js			开发
	webpack.prod.js			生产
```





**修改webpack.prod.js文件**

```
第一步
	由于生产时不需要自动编译,所以要删除webpack.dev.js中的自动化编译部分

//配置自动化编译(生产环境不需要自动化编译,直接编译生成文件即可)
    // devServer: {
    //     open: true,         //自动打开浏览器
    //     // compress: true,     //
    //     port: 3000,          //端口号
    //     hot:true            //开启热模替换
    // },



第二步
	当我们输入webpack时,会报错,原因是没有找到文件,所以需要在package.json中修改"scripts"中的内容
	
	"scripts": {
   		 "start": "webpack-dev-server --config ./config/webpack.dev.js",
   		 "build": "webpack --config ./config/webpack.prod.js"
 	 },
 	 
 	 
第三步
	出口路径
	
	output: {
        //也就是说: 第一个属性创建文件夹,第二个属性创建文件
        path: path.resolve(__dirname + '../dist'),       //输出路径(由于必需是绝对路径,所以要这样写)
        filename: "./js/index.js",      //输出的文件名
        publicPath: "/"                 //所有输出资源在引入时的公共路径
    },
    
    
   
第四步
	修改生产环境
	
	mode: 'production',  
	
	
	
第五步
	修改生产环境错误提示
	
	devtool: "cheap-module-source-map"
```







**serve**

```
serve可以帮助我们快速搭建一个静态资源服务器

npm i serve -g

serve -s dist -p 5000
	s	指定文件夹
	p	指定端口号
```











#### 清除打包文件目录

```
概述: 每次打包生产文件时,都需要手动删除原有的文件,当我们在文件中写入其他内容时,再次打包文件且不清除文件时,我们写入的文件不会被清			除,所以我们需要引入插件帮助我们自动删除上一次的打包文件
```



```
安装插件
	npm i clean-webpack-plugin -D
```



```
引入
	在webpack.prod.js中写入
		const {CleanWebpackPlugin} = require('clean-webpack-plugin')		必须结构赋值


使用
	在插件中写入
        new CleanWebpackPlugin()
```











#### 提取css为单独文件

```
安装
	npm i mini-css-extract-plugin@1.0.0 -D
	
```





```
导入
	const MiniCssExtractPlugin = require('mini-css-extract-plugin')

```





```
更改loader
	将原本解析样式中的loader更改为
	{
                test: /\.less$/,                 //匹配所有less文件
                use: [
                    // 'style-loader',     //用于在html文档中创建一个style标签,将样式塞进去
                    MiniCssExtractPlugin.loader,
                    'css-loader',       //将less编译后的css转换为commonJS的一个模块
                    'less-loader',       //编译less为css,但不生成单独的css文件,(编译之后在内存中)
                ],
            },
```



```
使用
	new MiniCssExtractPlugin({
            filename: "css/[name].css",         //文件创建到css下,文件名为原本的名字,后缀为css
        })
```









#### 添加css兼容

```
安装
	npm i postcss-loader postcss-flexbugs-fixes postcss-preset-env postcss-normalize autoprefixer -D
	
	
注意:
	postcss-loader@3.0.0
	postcss-flexbugs-fixes@4.1.0
	postcss-preset-env@6.7.0
	postcss-normalize@8.0.1
	autoprefixer@9.7.1
```





```
第一步
	更改webpack.prod.js中解析样式loader的配置
	
	{
                test: /\.less$/,                 //匹配所有less文件
                use: [
                    // 'style-loader',     //用于在html文档中创建一个style标签,将样式塞进去
                    MiniCssExtractPlugin.loader,
                    'css-loader',       //将less编译后的css转换为commonJS的一个模块
                    {
                        loader: 'postcss-loader',
                        options: {
                            ident: 'postcss',                //申明使用(postcss-loader需要靠postcss)
                            plugins: () => [
                                require('postcss-flexbugs-fixes'),
                                require('postcss-preset-env')({
                                    autoprefixer: {
                                        flexbox: 'no-2009',         //禁止使用2009年的老语法
                                    },
                                    stage: 3,                       //让更多的浏览器兼容新写法
                                }),
                                require('postcss-normalize')(),
                            ],
                           sourceMap: true,                    //生成css文件时会生成map文件(加与不加无所谓,默认生成)
                        },
                    },
                    'less-loader',       //编译less为css,但不生成单独的css文件,(编译之后在内存中)
                ],
            },
```





```
第二步
	创建一个文件,放在项目的根目录下,名为.browserslistrc
	内容为
	
	
	
# Browsers that we support

last 1 version
> 1%
IE 10 # sorry
```













#### 压缩css

```
安装插件
	npm i optimize-css-assets-webpack-plugin -D
```



```
引入
	const OptimizeCssAssetsPlugin=require('optimize-css-assets-webpack-plugin')
```



```
使用

 new OptimizeCssAssetsPlugin({
            cssProcessorPluginOptions:{
                preset:['default',{discardComments:{removeAll:true}}],
            },
            cssProcessorOptions: {
                map:{
                    inline: false,
                    annotation: true
                }
            }
        })
```











```
{
    removeComments: true,           //移除注释
    collapseWhitespace:true,
    removeRedundantAttributes:true,
    useShortDoctype:true,
    removeEmptyAttributes: true,
    removeStyleLinkTypeAttributes:true,
    keepClosingSlash:true,
    minifyJS:true,
    minifyCSS:true,
    minifyURLs:true
}
```









#### 总结

"devDependencies": {

  "@babel/core": "^7.12.16",

  "@babel/polyfill": "^7.12.1",

  "@babel/preset-env": "^7.12.16",

  "autoprefixer": "^9.7.1",

  "babel-loader": "^8.2.2",

  "clean-webpack-plugin": "^3.0.0",

  "core-js": "^3.8.3",

  "css-loader": "^4.0.0",

  "eslint": "^7.20.0",

  "eslint-loader": "^4.0.2",

  "file-loader": "^6.2.0",

  "html-loader": "^1.1.0",

  "html-webpack-plugin": "^3.2.0",

  "less": "^4.1.1",

  "less-loader": "^4.0.5",

  "mini-css-extract-plugin": "^1.0.0",

  "optimize-css-assets-webpack-plugin": "^5.0.4",

  "postcss-flexbugs-fixes": "^4.1.0",

  "postcss-loader": "^3.0.0",

  "postcss-normalize": "^8.0.1",

  "postcss-preset-env": "^6.7.0",

  "query-string": "^5.1.1",

  "style-loader": "^2.0.0",

  "url-loader": "^4.1.1",

  "webpack": "^4.29.4",

  "webpack-cli": "^3.2.3",

  "webpack-dev-server": "^3.11.2"

 },





|           用法           |                   作用                    |                  使用loader/插件                  |
| :----------------------: | :---------------------------------------: | :-----------------------------------------------: |
|         解析样式         |              将less转换为css              | css-loader    less-loader    style-loader    less |
|        js语法检查        |           检查js语法错误并提出            |              eslint-loader    eslint              |
|        js语法转换        |              将es6转换为es5               | babel-loader    @babel/core    @babel/preset-env  |
|       js兼容性处理       |        将无法被转换的语法进行转换         |            @babel/polyfill     core-js            |
| 打包样式文件中的图片资源 |      将样式文件中的图片资源进行打包       |             file-loader    url-loader             |
|       打包html文件       |            将html文件进行打包             |               html-webpack-plugins                |
|    打包html中图片资源    |          将html图片资源进行打包           |                    html-loader                    |
|       打包其他资源       |       将其他资源(音视频)等进行打包        |                    flie-loader                    |
|     自动编译打包运行     | 输入命令不会打包文件到目录上,而是到内存中 |                webpack-dev-server                 |
|         热模替换         |                                           |                                                   |
|                          |                                           |                                                   |
|                          |                                           |                                                   |
|                          |                                           |                                                   |
|                          |                                           |                                                   |
|                          |                                           |                                                   |
|                          |                                           |                                                   |
|                          |                                           |                                                   |
|                          |                                           |                                                   |
|                          |                                           |                                                   |









## React





### 认识

```
声明式: 不亲自操作DOM,我只是申明一下数据回来去哪里

命令式: 亲自操作DOM
```



````
组件: 页面上一个功能点所有的代码+资源集合

组件化: 将页面上每一个功能都分成一个个组件
````











### 使用



```
相关js库

	1/. react.js		react的核心库
	2/. reac-dom.js		提供操作DOM的react拓展库
	3/. babel.js		解析jsx语法代码转换为纯js语法代码的库
```







#### 虚拟DOM

```
React提供了一些API来创建一种特别的一般js对象

虚拟DOM对象最终都会被React转换为真实的DOM

我们编码时基本只需要操作react的虚拟DOM相关的数据,react会转换为真实DOM变化而更新页面

创建虚拟DOM后,虚拟DOM还在内存中待着,使用react将虚拟DOM放入页面中从而更新页面
```









#### jsx

```
全称: JavaScript XML
```



```
作用: 用于简化创建react虚拟DOM对象
```



```
babel.js的作用
	1. 浏览器不能直接解析jsx代码,需要babel转译为纯js代码才能运行
	2. 只要使用了jsx语法,那么他所在的script标签的属性必须为 type="text/babel",申明需要babel来处理
```



```
jsx中不能写语句,必须写表达式
```





````
js语句和js表达式的区别

表达式: 一个表达式会产生一个值,他可以放在任何需要一个值的地方
	举例
		3+b
		demo("a","b")
		arr.map()
		arr.forEach()
		等....
		
		
语句: 可以理解为是一种行为,循环语句,for,if都是典型的语句
	
````



```
jsx中写入内联样式
	<div style={{color:'red',display:a}}></div>
	
	在jsx中写入内联样式,首先写: style={{}}
	里面的括号写入类似对象格式的样式,样式名为key,值为value
	如果是普通的值,写引号
	如果是js语法,不用写引号
```









### 组件化

```
理解: 用于实现特定(局部)界面功能效果的代码和资源的集合(html/css/js/images)

作用: 复用代码,简化项目编码,提高运行效率
```







#### 自定义组件

```
方法1: 函数组件
方法2: class类组件


函数组件
	function Welcome(props) {
 	 return <h1>Hello, {props.name}</h1>;
	}
	
	
class类组件
    class Welcome extends React.Component {
      render() {
        return <h1>Hello, {this.props.name}</h1>;
      }
    }
```









#### 组件三大属性state

````
理解:
	state是组件实例对象最重要的属性,值是对象(可以包含多个key-value的组合)
	组件被称为"状态机",通过更新组件的state来更新对应的页面显示(重新渲染组件)
	
当我们每次改变组件类中的属性state的值时,都会调用组件类的render方法,刷新标签
````



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .demo{
            cursor:pointer
        }
    </style>
</head>
<body>
    <div id="example1"></div>
    <!-- 引入react核心库 -->
    <script src="js/react.development.js" type="text/javascript"></script>
    <!-- 引入react.dom,用于操作dom -->
    <script src="js/react-dom.development.js" type="text/javascript"></script>
    <!-- 引入babel,用于解析jsx为js -->
    <script src="js/babel.min.js" type="text/javascript"></script>

    <script  type="text/babel">
        //1. 定义组件
        class Weather extends React.Component{
            state={isHot:false,haha:'nice'}
            // constructor(props){
            //     //构造器中的this是组件类的实例对象
            //     super(props)
            //     this.state={isHot:false,haha:'nice'}
            //     this.demo=this.demo.bind(this)      //找到this中的方法demo,使demo的this为this,然后返回给this(一个新函数)
            // }
            //我们自己定义的demo,不是重写父类已经存在的demo
            demo=()=>{
                let {isHot}=this.state
                //demo中的this是undefined
                //在类组件中,所有我们编码人员自己定义的方法中this都是undefined
                // this.state.isHot=!this.state.isHot       组件实例对象的state:  1.不能直接修改  2.不能直接更新
                this.setState({isHot:!isHot})
            }
            render(){
                //render调用的次数: 1+n 初始化页面的时候必须调用一次,随后更新状态时,会触发render再次调用
                let {isHot}=this.state
                //render中的this是组件类的实例对象
                return <h1 className="demo" onClick={this.demo}>今天天气很{isHot?'炎热':'凉爽'}</h1>
            }
        }

        

        //2. 渲染组件标签
        ReactDOM.render(<Weather/>,document.getElementById('example1'))
    </script>
</body>
</html>
```











#### 组件三大属性props

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id="example1"></div>
    <div id="example2"></div>
    <!-- 引入react核心库 -->
    <script src="js/react.development.js" type="text/javascript"></script>
    <!-- 引入react.dom,用于操作dom -->
    <script src="js/react-dom.development.js" type="text/javascript"></script>
    <!-- 引入babel,用于解析jsx为js -->
    <script src="js/babel.min.js" type="text/javascript"></script>
    <!-- 引入prop-types,用于限制传递标签属性的类型和必要性 -->
    <script src="js/prop-types.js" type="text/javascript"></script>

    <script  type="text/babel">
        class Person extends React.Component{
            static propTypes={
            /*
                isRequired: 必须输入内容
            */
            name:PropTypes.string.isRequired,
            age:PropTypes.number,
            sex:PropTypes.string,
        }
            static defaultProps={
            age:18,
            sex:'不男不女'
        }
            render(){
                return (<ul>
                    <li>姓名:{this.props.name}</li>
                    <li>性别:{this.props.sex}</li>
                    <li>年龄:{this.props.age}</li>
                </ul>)
                }
            }

        let person={name:'kebi',age:18,sex:'男'}
        /*
            原本使用...展开对象会报错,但是在babel+react的操作下,可以展开
        */
        ReactDOM.render(<Person {...person}/>,document.getElementById('example1'))
        ReactDOM.render(<Person name='zhaungsanm'/>,document.getElementById('example2'))

    </script>

</body>
</html>
```









#### 组件三大属性refs



**方法1:基本方法**

```javascript
 <script  type="text/babel">
        class Mycomponent extends React.Component{
            clickHandel=()=>{
                alert(this.refs.input1.value)
            }
            blurHandel=(event)=>{
                alert(event.target.value)
            }
            render(){
                return (
                    <div>
                        <input type="text" ref="input1"/>
                        <button onClick={this.clickHandel}>点我提示数据</button>
                        <input type="text" placeholder="失去焦点提示" onBlur={this.blurHandel}/>
                    </div>
                )

            }
        }
        ReactDOM.render(<Mycomponent/>,document.getElementById('example1'))
</script>
```

```
在标签内添加属性ref,值随便写,当运行时,react会将标签内写入属性ref的标签传入到组件类的实例对象的属性refs中,refs是一个对象,标签在属性refs中以键值对形式存在,key为在标签内写入ref的值,value为标签节点
```







**方法2: 回调ref方法**

```javascript
 <script  type="text/babel">
        class Mycomponent extends React.Component{
            clickHandel=()=>{
                alert(this.input.value)
            }
            blurHandel=(event)=>{
                alert(event.target.value)
            }
            render(){
                return (
                    <div>
                        {/*执行下面这段代码: React会将当前节点作为参数传入到回调函数中,给组件类的实例对象添加一个属性,属性的值为传入的节点*/}
                        <input type="text" ref={(input)=>{this.input=input}}/>
                        <button onClick={this.clickHandel}>点我提示数据</button>
                        <input type="text" placeholder="失去焦点提示" onBlur={this.blurHandel}/>
                    </div>
                )

            }
        }
        ReactDOM.render(<Mycomponent/>,document.getElementById('example1'))
    </script>
```







**方法3: React.createRef()方法**

```javascript
<script  type="text/babel">
        class Mycomponent extends React.Component{
            /*
                调用React.createRef()创建一个用于保存ref的容器,且该容器是"专人转用"(只能保存一个ref)

            */
            myRef=React.createRef()

            clickHandel=()=>{
                alert(this.myRef.current.value)
            }
            blurHandel=(event)=>{
                alert(event.target.value)
            }
            render(){
                return (
                    <div>
                        {/*将该ref所在节点保存到this.myRef中*/}
                        <input type="text" ref={this.myRef}/>
                        <button onClick={this.clickHandel}>点我提示数据</button>
                        <input type="text" placeholder="失去焦点提示" onBlur={this.blurHandel}/>
                    </div>
                )

            }
        }
        ReactDOM.render(<Mycomponent/>,document.getElementById('example1'))
    </script>
```















#### 组件化编码流程(重点)

```
第一步: 拆分组件----拆分界面,抽取组件
第二步: 实现静态----使用组件实现静态页面效果
第三步: 实现动态组件
	a. 动态显示初始化数据
		1. 数据类型
		2. 数据名称
		3. 保存在那个组件?
	b. 交互(从绑定事件监听开始)
```









#### 受控组件和非受控组件

````javascript
<script  type="text/babel">
    /*
        每次输入的内容都会放在状态state中,称为受控组件
        反之则为非受控组件
    */
        class Login extends React.Component{
            state={
                password:''
            }
            submitHandel=(event)=>{
                event.preventDefault()
                alert(`准备提交的用户名是:${this.refs.username.value},密码是${this.state.password}`)
            }
            changeHandel=(event)=>{
                // console.log(event.target.value)
                this.setState({password:event.target.value})
            }
            render(){
                return (
                    // 当我们点击button或类型为submit的按钮时,都会触发onSubmit事件
                    <form action="https://www.baidu.com" onSubmit={this.submitHandel}>
                        用户名: <input type="text" ref="username"/>  
                        {/*当内容改变时,会触发onChange事件*/}  
                        密码: <input type="password" onChange={this.changeHandel}/>    
                            <input type="submit"/>
                    </form>
                )
            }
        }
        ReactDOM.render(<Login/>,document.getElementById('app'))
    </script>
````













#### 生命周期函数

````
理解
	1. 组件对象从创建到死亡它会经历特定的生命周期阶段
	2. React组件对象包含一系列的钩子函数(生命周期回调函数),在生命周期特定时刻回调
	3. 我们在定义组件时,可以重写特定的生命周期回调函数,做特定的工作
````



![React生命周期](C:\Users\86188\Pictures\Camera Roll\React生命周期.jpg)

```
componentWillMount			组件将要被挂载
componentDidMount			组件以及被挂载
componentWillUpdate			组件将要被更新
componentDidUpdate			组件以及被更新
componentWillUnmount		组件将要被卸载

shouldComponentUpdate		判断组件是否要需要被更新(返回的是布尔值)

ReactDOM.unmountComponentAtNode()			设置删除指定节点内的组件

componentWillReceiveProps		当props发生变化时执行，初始化render时不执行，在这个回调函数里面，你可以根据属性的变化，通								  过调用this.setState()来更新你的组件状态

this.forceUpdate()				将页面强制渲染一下
```



![生命周期(旧)](C:\Users\86188\Pictures\Camera Roll\生命周期(旧).png)



```
1.初始化
	触发条件: ReactDOM,render(<Mycomponent/>,DOM节点)
		constructor()
		componentWillMount()
		render(): 创建虚拟DOM,添加到页面上,执行n+1次
		componentDidMount(): 启动定时器,发送ajax请求,只执行一次
		
2. 更新
	触发条件: this.setState()
        componentWillUpdate()
        render()
        componentDidUpdate()
	

3. 卸载
	触发条件: ReactDOM.unmountComponentAtNode()
		componentWillUnmount():收尾工作,只执行一次
```





**即将废弃的钩子**

```
componentWillMount()
componentWillReceiveProps()
componentWillUpdate()

以后的版本需要在钩子前面加上UNSAFE_前缀才能使用,也许以后的版本就会废除
```







**生命周期图(新)**

![生命周期图(新)](C:\Users\86188\Pictures\Camera Roll\生命周期图(新).png)

**新增的钩子**

````
getDerivedStateFromProps()				
	作用: 这个钩子用于取代: componentWillMount  componentWillUpdate
	方法: 第一个参数为props,第二个参数为state
    实际作用: 将外部传入的参数设置到状态中
    返回值: 对象(会将对象传入到state中,有则更改,无则增加)
    
    
getSnapshotBeforeUpdate()
	方法: 第一个参数为props,第二个参数为state
	返回值: 为一个值(这个值为componentDidUpdate的第三个参数的值,前两个参数为props和state)
	
````









#### Diff算法

```
React工作流程
	
	初始化显示页面
		创建虚拟DOM树 ----> 真实DOM树 ----> 绘制界面显示
		
	更新界面
		setState()更新状态 ----> 重新创建虚拟DOM数 ----> 新/旧树比较差异 ----> 更新差异对应真实DOM ----> 局部界面重绘
```











#### react中的key

```
 虚拟DOM的key的作用
 	当状态数据发生变化时,react会生成新的虚拟DOM,随后react将之前的旧虚拟DOM与新的虚拟DOM进行Diff比较
 	
 		a. 若旧的虚拟DOM找到新的虚拟DOM(更新后的虚拟DOM)相同的key
 				若虚拟DOM没变(旧的虚拟DOM和新的虚拟DOM一样),就不去刷新页面上的真实DOM
 				若虚拟DOM变了,先更新虚拟DOM,再刷新页面上的真实DOM
 				
		 b. 旧的虚拟DOM没有找到新的虚拟DOM中相同的key
				 创建新的虚拟DOM,随后渲染真实DOM到页面上
```













### react脚手架

```
使用react脚手架,需要使用create-react-app
create-react-app: 用于创建react项目的脚手架库
```







```
安装create-react-ap(只需一次)
	npm i create-react-app -g
	
create-react-app  peiqi			创建react脚手架应用

编译		npm start
```







index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
      		%PUBLIC_URL%/相当于/,相当于public的路径(仅仅适用于react脚手架)
    <link rel="icon" href="%PUBLIC_URL%/favicon.ico" />
      		移动端屏幕适配
    <meta name="viewport" content="width=device-width, initial-scale=1" />
      		更改浏览器地址栏的颜色(手机浏览器,还必须是安卓手机)
    <meta name="theme-color" content="#000000" />
      		爬虫获取的内容
    <meta
      name="description"
      content="Web site created using create-react-app"
    />
      		在苹果手机中,将网站收藏成类似于手机中的应用时,显示的图片为此处指定的图标
    <link rel="apple-touch-icon" href="%PUBLIC_URL%/logo192.png" />
    <!--
      manifest.json provides metadata used when your web app is installed on a
      user's mobile device or desktop. See https://developers.google.com/web/fundamentals/web-app-manifest/
    -->
      		给网页加壳时的配置文件引入
    <link rel="manifest" href="%PUBLIC_URL%/manifest.json" />
    <!--
      Notice the use of %PUBLIC_URL% in the tags above.
      It will be replaced with the URL of the `public` folder during the build.
      Only files inside the `public` folder can be referenced from the HTML.

      Unlike "/favicon.ico" or "favicon.ico", "%PUBLIC_URL%/favicon.ico" will
      work correctly both with client-side routing and a non-root public URL.
      Learn how to configure a non-root public URL by running `npm run build`.
    -->
    <title>React App</title>
  </head>
  <body>
      		当浏览器不支持JavaScript脚本语言时会执行它,输出内容
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
    <!--
      This HTML file is a template.
      If you open it directly in the browser, you will see an empty page.

      You can add webfonts, meta tags, or analytics to this file.
      The build step will place the bundled scripts into the <body> tag.

      To begin the development, run `npm start` or `yarn start`.
      To create a production bundle, use `npm run build` or `yarn build`.
    -->
  </body>
</html>

```





app.js

```javascript
import logo from './logo.svg';		//react脚手架中引入图片的方式
import './App.css';					//react脚手架中引入样式的方式

function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Edit <code>src/App.js</code> and save to reload.
        </p>
        <a
          className="App-link"
          href="https://reactjs.org"
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
    </div>
  );
}

export default App;			//暴露app组件

```







index.js

````javascript
import React from 'react';          					//引入react核心库  
import ReactDOM from 'react-dom';						//引入reactDOM
import './index.css';									//引入样式
import App from './App';								//引入app组件
import reportWebVitals from './reportWebVitals';		

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById('root')
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();

````











#### 小知识

```
往标签内添加事件
	<a onClick={}></a>

如果不写参数
	<a onClick={this.demo}></a>
	
传入参数
	<a onClick={()=>{this.demo(a)}}></a>
```







```
confirm
	window上的一个方法
    会在页面弹出一个提示框,点击确定为true,点击取消为false
    使用:
    	if(window.confirm('你是人吗')){
    	}
```















### react ajax



```
React本身只关注于界面,并不包含发送ajax请求的代码
前端应用需要通过ajax请求与后台进行交互
react应用中需要集成第三方ajax库(或自己封装)
```





**常用的ajax请求库**

````
jquery: 比较重
axios: 轻量级
fetch: 原生函数,但是老版本浏览器不支持使用
````





https://api.github.com/search/repositories?q=r&sort=stars











### react fetch

````
无需引入,是h5特有的,ie8以下无法使用
````



```
xhr,jquery,axios: 看最终结果,不符合关注分离原则
fetch: 1.联系服务器   2. 携带回来服务器给你的数据
```





```
fetch(url)

.then(function(response) {
  return response.json();
})

.then(function(data) {
  console.log(data);
})

.catch(function(e) {
  console.log("Oops, error");
});


分析:
	第一个then: 当你连接服务器成功的时候调用,服务器返回一个成功的promise对象,但是then后的response没有data属性,这是fetch做				的,当你使用response.json()时,fetch会给你一个状态为成功的promise对象,对象的内容为data属性
	
	第二个then: 得到第一个then返回回来的状态为成功的promise对象,内容为data,然后可以进行操作
	
	第一个catch: 当你第一个then和第二个then没有执行时,此时,说明连接服务器失败,就可以调用最后一个catch,处理错误结果
```



```
fetch的问题:
    当你连接服务器时,如果域名写对,路由写错,也算连接到服务器,导致请求不会报错
    当你连接服务器时,如果域名写错,路由写对,就连接不到服务,报错
```















### 消息订阅和发布机制

```
作用: 实现兄弟组件之间通信
```



```
工具库: PubSub-js

安装: npm i pubsub-js
```





```
消息订阅: 就如同订阅一份报纸,每次报刊发布报纸时,我都会有一份

发布机制: 每次发布报纸
```



**使用**

```
消息订阅
    PubSub.subscribe('atguigu',(msg,data)=>{
   		this.setState(data)
    })
    subscribe方法中第一个参数: 订阅消息的名字
    subscribe方法中第二个参数: 回调函数,接收发布时的值
    回调函数中第一个参数: 发布消息的名字,和订阅消息名字一样
    回调函数中第二个参数: 发布的结果
    
    
发布机制
    PubSub.publish('atguigu',{
        users:[],
        isFirst:false,       
        isLoading:true,    
        error:''
    })
    publish方法中第一个参数: 发布消息的名字
    publish方法中第一个参数: 发布的值
    
    
    
什么组件用订阅,什么组价用发布
	需要兄弟组件的值的组件用订阅
	需要给兄弟组件值的组件用发布
	
	
每次publish调用时,subscribe都会调用(前提是他们的名字都一样,也就是第一个参数一样)


缺点: 乱,当你项目过大,组件过多,也许会导致订阅名重复或发布名重复(也就是说没有集中式管理)
```













### 几个重要技术总结



#### 组件间通信

**方法1------通过props传递**

```
1. 共同的数据放在父组件上,特有的数据放在自己组件内部(state)
2. 通过props可以传递一般属性和函数属性(传递函数属性一般是子组件需要使用父组件的state),只能一层一层传递
3. 一般属性---->父组件传递数据给子组件---->子组件读取数据
4. 函数属性---->子组件传递数据给父组件---->子组件调用函数
5. 适应: 最好用父传子,子传父也行,子传子也行(比较麻烦)
```





**方法2------使用消息订阅和发布机制**





**方法3------redux**

```
后面讲
```











### React-router

```
后端路由:
	1. key-value       key=请求方式+请求URL(虚拟地址)			value=回调函数
	2. 用户看到的是什么,由后端决定
	
	
前端路由:
	1. key-value		key=url			value=组件		
	2. 用户看到的是什么由前端决定
```









**react-router-dom**

```
1. react的一个插件库
2. 专门用来实现一个SPA应用
3. 基于react的项目都会用到此库
```





**SPA**

```
1. 单页面web应用
2. 整个应用只有一个完整的页面
3. 点击页面中的链接不会刷新页面,本身也不会向服务器发请求
4. 当点击路由链接时,只会做页面的局部刷新
5. 数据都需要通过ajax请求获取,并在前端异步展现
```







#### API

```
<BrowserRouter> : 路由器,想要在组件内些路由标签,必须在最外层套它

<Route> : 路由,当你输入指定url时,会触发它,执行组件

<Redirect> : 重定向,当全部路由和输入的url不匹配时,触发

<Link> : 路由链接,点击它,会在寻找指定路由(废弃)

<NavLink> : 路由链接,点击它,会在寻找指定路由(最新)

<Switch> : 在Route外层套一个它,当点击路由链接时,如果与路由匹配上,不继续往下匹配

<HashRouter> : 路由器,但是与BrowserRouter不同,他会在url的根路由上添加一个#,#后的都不会向服务器发送请求,为纯前端路由
```









**属性**

```
NavLink中的属性:
	to: 点击该元素时,给url添加路由about
    activeClassName: 点击该元素时,给该元素添加执行类
    replace: 不会产生浏览器历史,默认产生
    
    
Route中的属性:
	exact={true}: 开启精准匹配,默认为模糊匹配(只要path的内容是url中路由的字段,也就是说path="/add" url路由为add123,那么就					匹配上了),精准匹配是完全一样才可以匹配上
```









**路由组件和一般组件的区别**

```
	props多了history
			location
			match
			staticContext
```

```
history:
    action: "REPLACE"
    block: ƒ block(prompt)
    createHref: ƒ createHref(location)
    go: ƒ go(n)
    【goBack: ƒ goBack()】
    【goForward: ƒ goForward()】
    length: 2
    listen: ƒ listen(listener)
    location: {pathname: "/about", search: "", hash: "", state: undefined, key: "013csy"}
    【push: ƒ push(path, state)】
    【replace: ƒ replace(path, state)】
    __proto__: Object
    
location:
    hash: ""
    key: "013csy"
    【pathname: "/about"】   					中括号选中的都是重点
    search: ""
    state: undefined
    __proto__: Object
    
match:
    isExact: true
    【params: {}】
    path: "/about"
    url: "/about"
    __proto__: Object
    
staticContext: undefined		不管,react内部用的
```





```
点击跳转页面
<Button onClick={this.props.history.push('/admin/prod_about/product/add_update')}></Button>

```













### antd

**前讲**

```javascript
import React,{Component} from 'react'
import Button from './components/Button.jsx'

export default class App extends Component{
    render(){
        return (
            <div>
            <h2>App</h2>
            {/* 当我们将一个组件标签设置为不是自结束的标签，标签内的内容会作为key=children，value=内容的props传入到组件中 */}
            <Button>点我</Button>
            </div>
        )
    }
}
```



````javascript
import React,{Component} from 'react'

export default class Button extends Component{


    render(){
        return (
            <button style={{backgroundColor:"gray",color:"orange",width:"100px",height:"40px",outline:"none"}}>{this.props.children}</button>
        )
    }
}
````







#### 实现在react脚手架中按需引入antd样式

```
第一步：
	yarn add react-app-rewired customize-cra
		react-app-rewired的作用：更改create-react-app的配置
		
	
	
第二步：
	修改package文件
  "scripts": {
    "start": "react-app-rewired start",
    "build": "react-app-rewired build",
    "test": "react-app-rewired test",
    "eject": "react-scripts eject"
  },
  
  
第三步：
	在项目根路径下创建js文件config-overrides.js
	内容：
		module.exports=function override(config,env){
   			 return config;
		}
		
		
第四步：
	yarn add  babel-plugin-import
	
	
第五步：
	修改config-overrides.js内容
	内容：
	const {override,fixBabelImports} =require('customize-cra')
		module.exports=override(
    	fixBabelImports('import',{
       		libraryName:'antd',
        	libraryDirectory:'es',
        	style:'css',
    	}),
    );
    
    
第六步：
	删除App.js中的antd.css引入
```









#### 自定义主题

````
第一步
	yarn add less less-loader@5.0.0
	
	
第二步
	修改config-overrides.js内容
	内容：
		const {override,fixBabelImports,addLessLoader} =require('customize-cra')
		module.exports=override(
        fixBabelImports('import',{
            libraryName:'antd',
            libraryDirectory:'es',
            style:true,
        }),
        addLessLoader({
            javascriptEnabled: true,
            modifyVars:{'@primary-color':'#1DA57A'},
        }),
        );
        
        
第三步
	通过修改modifyVars:{'@primary-color':'#1DA57A'},中的#1DA57A来设置主题颜色
````





















### git复习

```
本地有仓库，远程无仓库（项目刚开始）
	1. git add *
	2. git commit -m '提交的信息'
	3. git remote add origin http://github/ad
	4. git push origin 分支名（默认只有一个master分支）
	
	
本地无仓库，远程有仓库（项目在你入职前就已经开始了）
	1. git clone http://github/ad (克隆下来的仓库里面已经包含了git文件夹，不用再设置关联了)
	
	
项目从头开始
	第一种方法
        1. 创建一个远程仓库，随后克隆
        2. 编写代码，本地管理，推送远程
    第二种方法
    	1. 建立一个本地仓库，再建立一个远程仓库，关联
```





## react项目



```
mock.js: 用于实现前端人员在没有服务器，没有数据库的情况下模拟数据
```















### redux

````
redux是一个独立专门用于做状态管理的js库
它可以用在react,angular,vue等项目中,但基本与react配合使用
作用: 集中式管理react应用中多个组件共享的状态
````



```
yarn add redux
```



![redux原理图](C:\Users\86188\Pictures\Camera Roll\redux原理图.jpg)





```
原理:
	首先ReactComponents(react组件)告诉ActionCreators自己要对状态做什么,
	ActionCreators给Store发送一个action,action中包含(type: ReactComponents要对状态做什么 data: 数据)
	Store将原本的状态和action传给Reducers,让Reducers进行处理,随后Reducers将处理后的新状态给Store
	Store再将状态给ReactComponents
```











#### API



**store**

```
作用:
	redux库最核心的管理对象
	它内部维护着:
		state --------- 状态
		reducer ------- 操作状态(store的手下)
```













#### redux的三个核心概念



**action**

```
1. 标识要执行行为的对象
2. 包含2个方面的属性
		type: 标识属性,值为字符串,唯一,必要属性
		xxxx: 数据属性,值为任意类型,可选属性
```







**reducer**

```
1. 根据老的state和action产生新的state的纯函数

```







**store**

```
1. 将state和action和reducer联系在一起的对象
```











#### React-redux将所有组件分为两类

```
yarn add react-redux
```



```
UI组件
	1. 只负责UI的呈现,不带有任何业务逻辑
	2. 通过props接收数据(一般数据和函数)
	3. 不使用redux任何的API
	4. 一般保存在components文件夹下
	
	
容器组件
	1. 负责管理数据和业务逻辑,不负责UI的呈现
	2. 使用Redux的API
	3. 一般保存在containers文件夹下
```







#### redux异步编程

````
yarn add redux-thunk
````













```
yarn add redux-devtools-extension			用于支持redux开发者调试工具的运行
```











### ajax解决跨域

````
解决跨域的方法
	1. jsonp
	2. cors
	3. 配置代理
````



**配置代理**

```
在package.json中添加
	"proxy":"http://localhost:5000"		访问的服务器地址
```



```
jsonp		用于解决跨域的库

	在项目中我们向百度发送请求获取天气,但是百度没有设置core,导致我们发送请求会导致跨域
```







```
401     代表没有权限去访问
```



```
screenfull				页面全屏库


	//切换全屏按钮回调
    fullScreen=()=>{
        screenfull.toggle();
    }
    
    //当全屏切换时会触发
    screenfull.on('change',()=>{
        let isFull=!this.state.isFull
        this.setState({isFull})
    })
```



```
dayjs					专门处理时间的库

	dayjs().format('{YYYY} MM-DDTHH:mm:ss SSS [Z] A')  时间转换
					YYYY: 年
					MM: 月
					DD: 天
					HH: 时
					mm: 分
					ss: 秒
					其他的东西都可以更改或删除
					
					比如:
						data:dayjs().format('YYYY年 MM月DD日 HH:mm:ss')
```





````
天气预报请求地址:
	http://api.map.baidu.com/telematics/v3/weather
	http://api.map.baidu.com/telematics/v3/weather?location=xxx&output=json&ak=3p49MVra6urFRGOT9s8UBWr2
	
	
请求方式:
	get
````

| 参数名称 | 类型   | 是否必选 | 描述          |
| -------- | ------ | -------- | ------------- |
| location | string | Y        | 城市名称      |
| output   | string | Y        | 返回值类型    |
| ak       | string | Y        | 应用的授权key |







````
注意: 当我们在想到如何解决同步操作无法等待异步操作的结果时,首先要想到promise
````









````
当state中的a是一个对象或数组时,不能直接修改
需要先
	let a= [...this.state.a]
	a.b=1
	this.setState({a})
````









```
分页:
	前端分页:
		前端向服务器发送请求,服务器将所有数据返回给前端,前端对数据进行切割,整理,划分页数
		当数据量足够大时会出现页面卡顿或浏览器"假死"
		
	后端分页:
		前端向服务器发送请求,服务器将一部分数据返回给前端,前端发送请求时,需要指明每页显示条数,你要那一页,
		交个服务器进行数据切割
		
```









````
this.setState()
	一个异步操作
	
````







```
wysiwyg				富文本编辑器库(react专用)
```



```
easyUI	zTree				jquery周边库,配合jquery使用			
```











### 数据可视化

```
echarts

D3

highCharts
```









## TypeScript

```
微软发布

ts不能直接在浏览器上运行,需要将ts转换为js,然后运行
```



### 安装

```
npm install -g typescript
```







````
tsc  ./a.ts					将ts文件编译为js文件
````









### 类型注解

```typescript
 /*
 
 类型注解: 是一种轻量级的为函数或者变量添加的约束
        a传入的是一个数组,会报错,但是编译的js不会报错,因为js是弱类型的语言

 */



(()=>{
    function showMsg(str:string){
        return '窗前明月光,' + str
    }
    let a = '实地速度'
    console.log(showMsg(a))
})()
```



















































## VUE

```
渐进式: 不是一下把所有的插件给你,而是你要什么给你什么
```

```
构建: 将源代码经过各种处理编译成浏览器可以高效执行的代码
```



```
特点:
	遵循MVM模式
	编码简洁,体积小,运行效率高,适合移动/PC端开发
	它本身只关注UI,可以轻松引入vue插件或其他第三方库开发项目
```



```
vue扩展插件
	vue-cli							vue脚手架
	vue-resource(axios)				ajax请求
	vue-router						路由
	vuex							状态管理
	vue-lazyload					图片懒加载
	vue-scroller					页面滑动相关
	mint-ui							基于vue的ui组件库(移动端)
	element-ui						基于vue的ui组件库(pc端)
```







### 什么是MVVM？

- 概念介绍

  - MVVM分为三个部分：分别是M（Model，模型层 ），V（View，视图层），VM（ViewModel，V与M连接的桥梁，也可以看作为控制器）
     1、 M：模型层，主要负责业务数据相关；
     2、 V：视图层，顾名思义，负责视图相关，细分下来就是html+css层；
     3、 VM：V与M沟通的桥梁，负责监听M或者V的修改，是实现MVVM双向绑定的要点；
  - MVVM支持双向绑定，意思就是当M层数据进行修改时，VM层会监测到变化，并且通知V层进行相应的修改，反之修改V层则会通知M层数据进行修改，以此也实现了视图与模型层的相互解耦；

  











### VUE对象的选项

````
el
	指定dom标签容器的选择器
	Vue就会管理对应的标签及其子标签
	也可以通过$mount()来处理
	
	
	
	
	
data
	对象或函数类型
	指定初始化状态属性数据的对象
	vm也会自动拥有data中所有属性
	页面中可以直接访问使用
	数据代理: 由vm对象来代理对data中所有属性的操作(读/写)
	data数据监视的特点:
		1. vue会监视data中所有层次的属性
		2. 对象中的属性数据通过添加set方法来实现监视
		3. 数组中的元素也实现了监视: 重写数组一系列更新元素的方法
			1]. 调用原生对应的方法对元素进行处理
			2]. 去更新页面
			
			
			
			
			
methods
	包含多个方法的对象
	供页面中的事件指令来绑定回调
	回调函数默认有event参数,但也可以指定自己的参数
	所有的方法由vue对象来调用,访问data中的属性直接使用this.xxx
	如果想往回调函数中传入参数,也想使用event,在页面绑定回调时传入的参数为(参数1,参数2,$event)
	
	
	
	
computed
	计算data中没有定义,但是在页面上以插值的形式存在的属性
	包含多个计算属性的对象
	根据已有属性进行计算返回一个新的数据,供页面获取显示
	如果同时还需要监视计算属性的变化,需要使用getter/setter
	计算属性有缓存,内部使用对象容器缓存,可以减少计算的次数
	如何给对象定义get/set属性
		对象创建之后指定: Object.defineProperty(obj,age,{get(){},set(){}})
		在创建对象时指定: get name () {return xxx}  /  set name (value) {}



watch
	监视data中定义了的属性
	包含多个属性监视的对象
	分为一般监视和深度监视
	
````





### this



```
mounted() {
    setInterval(function () {			function函数this指向window
    	this.isShow = !this.isShow
    }, 1000);
},


mounted() {
    setInterval(function () {			使用bind将当前函数加工,返回一个this指向为指定this的函数
    	this.isShow = !this.isShow
    }.bind(this), 1000);
},


mounted() {
    setInterval(()=> {					箭头函数的this指向父函数的this
    	this.isShow = !this.isShow
    }, 1000);
},


mounted() {
	const that = this
    setInterval(function () {			在函数外部申明this,函数内部使用
    	that.isShow = !that.isShow
    }, 1000);
},
```



```
bind
	1. 返回了一个新的函数
	2. 新函数内部调用了旧函数(通过call调用)
	3. 在调用旧函数时,旧函数的this指向为bind传入的第一个参数
```







### 生命周期

```
vue生命周期分为三个阶段
	1. 初始化阶段
		beforeCreate()
		created()
		beforeMount()
		mounted()
	2. 更新状态
		beforeUpdate()
		updated()
	3. 销毁vue实例: vm.$destory()
		beforeDestory()
		destoryed()
```





```
常用的生命周期方法
	created()/mounted(): 发送aiax请求,启动定时器等异步任务
	beforeDestory()	   : 做收尾工作,如: 清除定时器
```



```
在beforeCreate()和created()之间实现数据代理/data数据的监视(setter)
	也就是说,在beforeCreate无法得到vue实例的data数据
	但在created可以
```

```
在beforeMount()和mounted()之间实现了可以通过ref读取页面标签对象
	也就是说,在beforeMount中,还是虚拟dom,没有挂载到页面上,无法获取ref
	但是mounted可以,因为挂载到页面上了
```

```
在beforeUpdate()和updated()之间实现的是页面的更新
	也就是说,在beforeUpdate中,页面还没有更新
	但是在updated中,页面更新了
	在beforeUpdate中,数据已经更新,但是页面没有更新
```









### 过滤器

```
过滤器:
    功能: 对要显示的数据进行特点格式化后再显示
    注意: 并没有改变原本的数据,可是产生新的对应的数据

定义过滤器: Vue.filter(filterName,function(value,参数1,参数2){})

使用过滤器: <div>{{value | filter(参数1)}}</div>
```









```
指令 ----------- 操作标签
插值 ----------- 操作文本
```











### 指令

```
常用内置指令
        v-text                      更新元素的textContent
        v-html                      更新元素的innerHTML
        v-if                        如果为true,当前标签才会输出到页面
        v-else                      如果为false,当前标签才会输出到页面
        v-show                      通过控制display样式来控制显示/隐藏
        v-for                       遍历数组/对象
        v-on                        绑定事件监听,简写@
        v-bind                      强制绑定解析表达式,可以省略v-bind(对标签属性强制绑定,可以动态修改标签属性的值)
        v-model                     双向数据绑定(表单)
        ref                         为某个元素注册一个唯一标识,vue对象通过$els属性访问这个元素对象
```



**自定义创建指令**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="../js/vue.js" type="text/javascript"></script>
    <title>Document</title>
</head>
<body>
    <!-- 

     -->

     <div id="app">
         <p v-upper-text="msg"></p>
         <p v-lower-text='msg'></p>
     </div>
    <script  type="text/javascript">
        /*
            注册全局指令
            el: 指令属性所在的标签元素
            binding: 包含指令相关数据的对象
            注意: 要写在实例vm的前面
        */
        Vue.directive('upper-text',function (el,binding) {
            console.log('upper-text',binding)
            el.textContent = binding.value.toUpperCase()
        })

        new Vue({
            el:'#app',
            data: {
                msg : 'I love You'
            },
            //注册局部指令
            directives:{
                'lower-text':function (el,binding) {
                    console.log('upper-text',binding)
                    el.textContent = binding.value.toLowerCase()
                }
            }
        })



    </script>
</body>
</html>
```









### style和class

```
vue中使用style
	1. 对象语法
		<div :style="{color: 'red',font-size: '20px'}"></div>
	2. 数组语法
		<div :style="[redStyle,colorStyle]"></div>
		data(){
			return {
				redStyle:{
					color: 'red',
				},
				colorStyle:{
					font-size: '30px'
				}
			}
		}
		
		
		
		
vue中使用class
	1. 对象写法
		<div :class="{active:true}"></div>
		键为类名,值为布尔值
	2. 数组写法
		<div :class="[active,four,red]"></div>
		<div :class="[true ? active : red]"></div>
		<div v-bind:class="[{ active: isActive }, errorClass]"></div>
```











### 搭建VUE环境



#### 初始化项目

```
1. yarn init

2. 创建入口文件 src/index.js

3. 创建页面文件 index.html
```





#### 使用webpack

```
第一步
	先卸载掉全局安装的webpack和webpack-cli
	
	
第二步
	局部安装webpack和webpack-cli
		npm i  webpack@4.29.4 webpack-cli@3.2.3 -D

第三步
	安装html-webpack-plugin,打包index.html
	
	
第四步
	安装clear-webpack-plugin清除打包文件
	
	
第四步
	安装webpack-dev-server自动编译
	
	
第五步
	安装npm install babel-loader @babel/core @babel/preset-env编译ES6语法
	
	
第六步
	安装  css-loader style-loader编译css文件
	
	
第七步
	安装url-loader,file-loader编译图片资源
	
	
第八步
	搭建vue的环境
	npm i vue
	npm i vue-template-compiler   vue-loader  -D
	const { VueLoaderPlugin } = require('vue-loader')

    module.exports = {
      module: {
        rules: [
          // ... 其它规则
          {
            test: /\.vue$/,
            loader: 'vue-loader'
          }
        ]
      },
      plugins: [
        // 请确保引入这个插件！
        new VueLoaderPlugin()
      ]
    }
    配置loader和plugin
    将编译css的loader写为
    {
        test:/\.css$/,                 //匹配所有less文件
        // vue-style-loader是对style-loader的增强
        use: ['vue-style-loader','css-loader'],
    },
    
    
    
第九步
    引入vue文件时可以省略后缀名,如js一样

        //模块引入解析
        resolve: {
        alias:{
            '@': resolve(__dirname,"src")       //模块路径别名
        },
        extensions: ['js','vue'],            //指定那些后缀的模块可以省略
    }
```







**注意:**

````
babel本身不编译ES6的语法
babel需要基于它的plugin(插件)来实现ES6语法编译
每一个ES6语法都对应一个babel plugin来编译对应的语法
一个babel preset包是包含多个常用的babel plugin的集合包
好处: 便于管理配置

也就是说:babel中有一个包为preset-env,它中包含多个ES6常用语法解析的plugin插件
		
````





```
vscode快速搜索包
	ctrl + k
	ctrl + n
```









```javascript
import Vue from 'vue'
import App from './app.vue'

Vue.config.productionTip = false

//第一种方法
// new Vue({
//     el:'#root',
//     render: function (createElement){           //用来渲染组件标签的回调函数
//         return createElement(App)   //返回<App/>
//     }//调用render函数得到它返回的组件标签对象
// })


//第二种方法
new Vue({
    el:'#root',
    components:{
        App
    },
    template: '<App/>'
})



/*
    render: 没有问题
        内部使用vue-template-complilter提前编译好了模板

    template: 有问题
        不使用vue-template-complilter,就无法编译模板
        解决: 在package.json中写入 'vue$': 'vue/dist/vue.esm.js'
            默认引入的是"main": "dist/vue.runtime.common.js",(不带编译器的版本)
            写入它之后import App from './app.vue'引入的是vue/dist/vue.esm.js(带编译器的版本)

*/
```









````
如果在data中定义属性,如果想要当属性变化时执行,使用监听
如果没有在data中定义,而是在页面中使用插值,需要使用computed
````













### 组件间通信





**组件间通信基本原则**

```
1. 不要在子组件中直接修改父组件的状态数据
2. 数据在哪,更新数据的行为(函数)就应该定义在哪
```







**vue组件间通信方法**

````
1.  props
2.  vue的自定义事件
3.  消息订阅和发布/事件总线
4.  slot
5.  vuex
````









#### props

````
实现父向子,子向父传递

父向子传递
	<MyComponent name="data"></MyComponent>
	父组件向子组件传递一个属性,子组件申明并使用
	
子向父传递
	<MyComponent name="fun"></MyComponent>
	父组件向子组件传递一个函数,子组件申明使用时传递一个属性,函数在父组件调用,此时属性就传递到函数父组件中
````





```
问题:
	a. 如果需要向非子后代传递数据必须多层逐层传递
	b. 兄弟组件之间不能直接props通向,需要借助父组件才可以
```











#### vue的自定义事件

```
作用: 实现子向父通信
```





**事件处理的理解**

```
	
原生的DOM事件
	当我们在页面中触发了指定事件,比如移入元素,移出元素,会触发指定事件(传入的数据为event),浏览器会去分发事件
		注意:
			原生的DOM事件只有浏览器指定的几个事件,事件不能随意创造,也无法传参,回调函数是浏览器执行的
			
			
自定义事件
	我们使用$on绑定事件监听,事件名可以自己起,也可以传入参数
	使用emit触发事件,传入参数
		注意: 触发事件是代码触发,根据你的意愿,在代码中写入触发事件的代码,可以传入参数
```





**API**

```
vm.$on				绑定事件监听
vm.$off				解绑事件监听
vm.emit				分发事件
vm.$once			监听一次,一次后会移出监听器
```



```
子组件
	当执行到此段代码,会分发事件,执行事件回调函数,
	第一个参数: 事件名
	第二个参数: 参数
	this.$emit('addTodo',todo)
```



```
父组件
	//事件回调
     methods: {
         addTodo(todo){
         	this.todos.unshift(todo)
         },
        }
        
	绑定自定义事件监听
	/*
    给header组件绑定自定义事件监听
    要求: 绑定自定义事件监听和分发事件的组件对象得是同一个
    为什么要在app组件内绑定header组件的自定义事件监听: 实现子组件向父组件传递属性
    */
	this.$refs.header.$on('addTodo',this.addTodo)
	
	
	
	beforeDestroy(){
            //解绑自定义事件监听
            this.$refs.header.$off('addTodo')
        }
```







```
vue的组件对象与vue的关系
	组件对象不是Vue的实例对象,它是VueComponent的实例
	组件对象的原型对象时一个vm对象(Vue的实例对象)
	在组件对象中读取this.xxxx,先去自身上找,找不到再去vm对象上找,找不到再到vue的原型对象上找,最后到object的原型对象找
	
	vue的原型对象只有一个,但是组件对象的原型对象是每个组件都有自己的原型对象(vm)
```









#### 全局事件总线

```
借助上面可知,vue的原型对象只有一个,但是每个组件对象的原型对象是不同的vm,而这些不同的vm的原型对象是vue的原型对象
从这可以得知,组件对象依靠原型链可以找到vue的原型对象,也就是说组件对象有一个共同的原型对象(vue的原型对象)

我们可以在vue的原型对象上创建一个vm,在这个vm上依靠vue的自定义事件来实现各个组件之间的通信
```



**操作**

```
在vue的原型对象上创建一个vm,名为$globalEventBus
Vue.prototype.$globalEventBus = new Vue()
```



```
在组件对象中绑定自定义事件
this.$globalEventBus.on(事件名,回调函数)
```



```
在组件对象中分发自定义事件
this.$globalEventBus.emit(事件名,参数)
```



```
在组件对象中解绑自定义事件
this.$globalEventBus.off(事件名)
```



```
注意:
	为什么this中有$globalEventBus?
		依靠原型链,组件对象中没有,会找他们各自的vm,vm没有,会找到vm共同的原型对象上(vue的原型对象),而我们定义了,所以可以找到
		
	为什么在vue的原型对象上创建一个vm?
		因为vm上可以操作自定义事件
```









#### 插槽

```
普通插槽

父组件
<Home>
	<p>默认插槽</p> 
	//命名插槽
    <p name="left">插槽左护法</p>
    <p name="right">插槽右护法</p>
</Home>

子组件
    <slot name="right"></slot>
    <slot name="left"></slot>
    <slot></slot>
```





```
具名插槽

父组件
        <template>
            <p>默认插槽</p>
        </template>
        <template v-slot:left>
            <p>插槽左护法</p>
        </template>
        <template v-slot:right>
            <p>插槽右护法</p>
        </template>
        
        
子组件
    <slot name="right"></slot>
    <slot name="left"></slot>
    <slot></slot>
```





````
后备插槽
<!-- 后备插槽: 在插槽内部写入内容,如果传入组件在使用组件时传入插槽,就使用传入的插槽,没有传入插槽,使用插槽内部的内容 -->
<slot name="left">我是默认的插槽左护法</slot>
````



```
作用域插槽

父组件
<!-- 使用作用域插槽传递过来的props时,需要用与一个变量接住,在插槽名后面写上="变量名"接住,然后即可使用 -->
<template v-slot:right="user">
	<p name="right">插槽右护法{{user.user}}{{user.age}}</p>
</template>


子组件
<!-- 作用域插槽: 如果父组件想使用插槽时同时可以使用子组件的数据,可以在子组件定义插槽时传入一个或多个props -->
<slot name="right" :user='name' :age="age"></slot>
```







### mixins

```
混入:
	export default {
        data () {
            return {
                msg: '混合数据'
            }
        },
        methods: {
            log () {
                console.log('hello',this.msg)
            }
        }
	}
	
	    import mixin from './mixins'
        export default {
            mixins: [mixin],         // 申明使用混入的对象,同时可以使用多个
            // data () {
            //     return {
            //         // msg: 'App组件的数据'
            //     }
            // },

            mounted () {
                // 如果当前组件没有定义属性msg,就会去mixin中去找,如果当前组件定义了msg,就使用当前组件的msg
                // 也就会说:    当前组件的属性 > mixin的属性
                this.log()
                console.log(this.msg)
            }
        }
```





### 动态组件&异步组件

```
1. 动态组件
	1. 使用的时候动态加载,性能优化
	2. <component :is="组件" />
	
	
2. 异步组件
	常规注册组件: components: {组件名: 组件}
	异步注册组件: components: {组件名: (resolve,reject)=>{resolve(组件)}}
```











### keep-alive

```
给组件外套上标签keep-alive,组件切换时不会销毁组件,而是缓存组件,组件内部的数据不会发生变化
```















### vue-ajax



**vue中常用的2个ajax库**

```
vue-resource
axios
```









#### vue-resource

**使用**

```
首先,要在全局申明使用vue-resource
import VueResource from 'vue-resource'
Vue.use(VueResource)		申明使用,所有组件都会有一个属性$http,方法有get(),post等




//使用vue-resource发送请求
// this.$http.get('https://api.github.com/search/repositories?q=j&sort=starts')
// .then(response=>{
//     const result = response.data
//     const {name, html_url} = result.items[0]
//     this.repoName = name
//     this.repoUrl = html_url
// })
// .catch(
//     error=>{
//         alert('请求出错')
//     }
// )
```





#### axios

**使用**

````
//使用axios发送请求
this.$http.get('https://api.github.com/search/repositories',{params:{q:'j',sort:'starts'}})
.then(response=>{
    const result = response.data
    const {name, html_url} = result.items[0]
    this.repoName = name
    this.repoUrl = html_url
})
.catch(
    error=>{
    	alert('请求出错')
    }
)

````









#### 处理跨域

```
在webpack.config.js中的devserver中输入此属性



proxy: {
            //匹配处理以/api开头语的请求
            "/api": {
              target: "http://localhost:5000",          //转发的目标地址
              pathRewrite: {"^/api" : ""},              //在转发请求前去除路径中的/api
              changeOrigin: true                        //支持协议名的跨域
            }
        }
```









#### 解决vue环境无法使用async,await

````
ES6的新语法
	新的语法: let  const 箭头函数
	
	
新的API
	Map  Promise   arr.map()
	
@babel/preset-env它只能编译新的语法,不能处理新的API
````



**解决**

````
npm i @babel/polyfill  -D

@babel/polyfill的依赖包
   "core-js": "^2.6.5"		: 提供es5/es6/es7的新的API的实现
   "regenerator-runtime"	: es8的async/await
   
   
   
使用:
	在入口文件引入使用
		import '@babel/polyfill'
		
	问题: 太大了
	解决: 按需引入
	
	
	
````



















### vue-router

````
实现SPA页面的库
````







#### 基本使用

```javascript
/*
        定义路由器对象
*/

import Vue from 'vue'
import VueRouter from 'vue-router'

import About from '../pages/About.vue'
import Home from '../pages/Home.vue'

//申明使用vue插件
Vue.use(VueRouter)


//向外暴露路由器对象
export default new VueRouter({

    //应用中所有路由
    routes: [
        {
            path: '/about',
            component: About,
        },
        {
            path: '/home',
            component: Home,
        },
        {
            // 自动跳转
            path: '/',
            component: About
        }
    ]
})
```







````
在index.js中引入路由器,并注册路由器

new Vue({
    el:'#root',
    render: h => h(App),
    router:router,          ///注册路由器
})

````





```
<!-- 路由链接 -->
<router-link to="/about" class="list-group-item">About</router-link>
<router-link to="/home" class="list-group-item">Home</router-link>


router-link:
	路由链接,当点击时,跳转到to所指定的路由中, 它最终会被解析成a标签
	
	
	
router-view:
	在此标签中显示当前路由
	<router-view></router-view>
	
	
.router-link-active:
	当前显示的组件所拥有的类名,在这个类名中可以指定当前选中类的样式
```











#### 嵌套路由

```javascript
/*
        定义路由器对象
*/

import Vue from 'vue'
import VueRouter from 'vue-router'

import About from '../pages/About.vue'
import Home from '../pages/Home.vue'
import Messgae from '../pages/Message.vue'
import News from '../pages/News.vue'

//申明使用vue插件
Vue.use(VueRouter)


//向外暴露路由器对象
export default new VueRouter({

    //应用中所有路由
    routes: [
        {
            path: '/about',
            component: About,
        },
        {
            path: '/home',
            component: Home,
            //嵌套路由
            children: [
                {
                    path: 'news',
                    component: News
                },
                {
                    path: '/home/message',          //path左边的/代表项目的根路径,不加/代表当前路径
                    component: Messgae
                },
                // 自动跳转
                {
                    path: '',
                    redirect: '/home/news'  
                }
            ]
        },
        {
            // 自动跳转
            path: '/',
            redirect: About
        },

    ]
})
```





```javascript
在路由组件中引入路由


<template>
  <div>
    <h2>Home</h2>
    <ul class="nav nav-tabs">
      <li>
        <router-link to="/home/news">News</router-link>
      </li>
      <li>
        <router-link to="/home/message">Mesage</router-link>
      </li>
    </ul>
    <!-- 在此显示当前路由组件 -->
    <router-view></router-view>
  </div>
</template>
```











#### 路由组件对象的生命周期

```
路由组件对象在访问对应的路由路径时才会创建对象
    从A组件跳转到B组件对象: 销毁A组件对象,创建B组件对象
    从B组件跳转到A组件对象: 销毁B组件对象,创建A组件对象
	从A组件跳转到A组件对象(只是改变了参数): A组件对象不会销毁重新创建
	
	
问题: 如果是参数改变了,会导致无法刷新页面
解决办法: 监视$route
    watch: {
        '$route'(to,from){          //to就是$route的最新值
            this.show(to.params.mid * 1)
        }
    },
```







````
atguigu-units
````











#### 向路由组件传入参数



```
第一种方法:
	params/query: <router-link to="/home/news/123/abc?zzz=1234"></router-link>
	
	
第二种方法:
	将请求的参数映射为props
	{
        path:'/home/message/detail/:mid',
        component: MessageDetail,
        //props: true             //将params参数映射为props传递给路由组件
        props: (route)=>({          //可以映射params参数和query参数
            mid: route.params.mid, 
            title: route.query.title
        })
	}
	
	
	
第三种方法
	变相props
	<router-view msg="abc"></router-view>
	只要是当前router-view管理的组件,都会有一个属性msg,值为abc
```









#### 命名路由

````
在定义路由时
{
    name:'detail',					//指定路由名
    path:'/home/message/detail/:mid',
    component: MessageDetail,
    //props: true             //将params参数映射为props传递给路由组件
    props: (route)=>({          //可以映射params参数和query参数
        mid: route.params.mid, 
        title: route.query.title
    })
}


可以传入params和query参数
<router-link :to="{name: 'detail',params:{mid:m.id},query:{title:m.title}}">{{m.title}}</router-link>
````









#### 编程式导航

````
push
replace
back
````





**使用方法**

````
            pushShow(messgae){
                // 编程式路由导航
                // this.$router.push(`/home/message/detail/${messgae.id}?title=${messgae.title}`)
                this.$router.push({name: 'detail',params:{mid:messgae.id},query:{title:messgae.title}})
            },
            replaceShow(messgae){
                // 编程式路由导航
                this.$router.replace(`/home/message/detail/${messgae.id}?title=${messgae.title}`)
            },
````











#### keep-alive

````
路由组件对象默认的生命周期: 切换时就会死亡, 切换回来就会重新创建
````



````
            <!-- 
              默认缓存的是所有队员的路由组件对象
                使用include/exclude来指定缓存的组件对象
             -->
            <keep-alive include="home">
              <!-- 显示当前路由组件 -->
              <router-view msg="abc"></router-view>
            </keep-alive>
````













#### history模式

````
hash模式			默认,url: http://localhost:3000/#/about
history模式		url: http://localhost:3000/about
````





**问题**

```
history刷新页面返回的是404?
	原因:
		hash模式: 刷新页面,url地址为 http://localhost:3000/#/about/home
				 请求后台,给后台的url地址为 http://localhost:3000/
				 注意: #/about/home不会交给后台服务器
				 请求后台地址为http://localhost:3000/,后台返回给你的是打包后的index.html
				 index.html文件内容为:
				 <!DOCTYPE html>
                    <html lang="en">
                    <head>
                        <meta charset="UTF-8">
                        <meta http-equiv="X-UA-Compatible" content="IE=edge">
                        <meta name="viewport" content="width=device-width, initial-scale=1.0">
                        <link rel="stylesheet" href="./static/css/base.css">
                        <link rel="stylesheet" href="./static/css/bootstrap.css">
                        <title>VUE Component</title>
                        <style>
                            /* 当前选中的路由的样式 */
                            .router-link-active{
                                color: red !important;
                            }
                        </style>
                    </head>
                    <body>
                        <div id="root">

                        </div>
                    <script type="text/javascript" src="static/js/bundle.js"></script></body>
                    </html>
                  其中bundle.js就会将#/about/home解析为前台路由路径
                  
                  
                  
		history模式: 刷新页面,url地址为: http://localhost:3000/about/home
					请求后台,url地址为: http://localhost:3000/about/home
					此时,请求的路径后台没有,无法处理,返回404
					
					
	解决:
		在某个路由路径下刷新,服务器能返回index页面
	
	方法:
		第一步: 在webpack.config.js的devServer中写入historyApiFallback: true(请求404时返回index页面)                     第二步: 在webpack.config.js的output中写入publicPath: '/',  
				原因: 在请求地址为http://localhost:3000/home/about下刷新,请求的index.html中,引用的文件路径为:
						http://localhost:3000/home/about/a
						http://localhost:3000/home/about/b
						加上publicPath: '/',会将引用的文件在根路径下查找
```







#### $route和$router的区别

```
$router是路由器对象,里边包含路由跳转的方法
$route是路由对象,里面包含当前路由组件下所有的路由信息
```







### mint-ui

```
npm  i mint-ui
```







#### 按需引入

```
npm install babel-plugin-component -D
```



使用

```
在webpack.config.js中的实现js语法转换的option中写入


plugins: [          //配置预设包之外的插件包
                        [
                            "babel-plugin-component",       //插件名
                            {
                              "libraryName": "mint-ui",     //针对mint-ui实现按需引入打包
                              "style": true                 //自动打包组件对应的样式
                            }
                        ]
                    ]
```







````
详细使用查看mint-ui官方文档
````

















### vuex

```
实现多组件状态共享
```





#### state

````
vuex管理的状态对象
它是唯一的
````







#### mutations

```
包含多个直接更新state的方法(回调函数)的对象
谁来触发: action中的commit
```









#### actions

```
包含多个事件回调函数的对象
```







#### getters

```
包含多个计算属性的方法
```











#### 使用

````javascript
/*
    vuex最核心的管理对象store

*/



import Vue from 'vue'
import Vuex from 'vuex'


//申明使用vuex插件
Vue.use(Vuex)


const state = {
    count: 1,           //初始化状态数据
}

//包含n个用于直接更新状态数据方法的对象
//在mutations中的函数只是更改状态中的数据,不做其他事
const mutations = {
    INCREMENT(state){
        state.count++
    },
    DECREMENT(state){
        state.count--
    },
}       

//包含n个用于间接更新状态数据方法的对象
//在actions中的函数可以包含逻辑代码或异步代码
const actions = {
    // increment({commit}){
    //     commit('INCREMENT')
    // },
    // decrement({commit}){
    //     commit('DECREMENT')
    // },
    incrementIfOdd({commit,state}){
        if(state.count%2 === 1)commit('INCREMENT')
    },
    incrementAsync({commit}){
        setTimeout(()=>{commit('INCREMENT')},1000)
    }
}

//包含n个基于state数据的getter的计算属性的方法的对象
const getters = {
    //当state发生改变时,触发
    eventOdd(state){
        return state.count % 2 === 1 ?'奇数' : '偶数'
    }
}


export default new Vuex.Store({
    state,
    mutations,
    actions,
    getters
})
````







```javascript
import '@babel/polyfill'

import Vue from 'vue'
import App from './App.vue'

import store from './store'


Vue.config.productionTip = false


//第一种方法
new Vue({
    el:'#root',
    render: h => h(App),
    store,          //配置store,所有的组件都可以通过$store访问$store对象
})



```







```javascript
<template>
   <div>
     <!-- <p>cilcked {{$store.state.count}} times, count is {{$store.getters.eventOdd}}</p> -->
     <p>cilcked {{count}} times, count is {{eventOdd}}</p>
     <button @click="increment">+</button>
     <button @click="decrement">-</button>
     <button @click="incrementIfOdd">incrent if odd</button>
     <button @click="incrementAsync">increment asycn</button>

   </div>
</template>

<script>
    import {mapState, mapGetters, mapMutations, mapActions} from 'vuex'       //引入方法
    export default {

        //一般写法
        // computed: {
        //   count(){
        //     return this.$store.state.count
        //   },
        //   eventOdd(){
        //     return this.$store.getters.eventOdd
        //   }
        // },

        //简化写法
        computed: {
          ...mapState(['count']),  //mapState是一个函数,返回一个函数{count (){return this.$store.state['count']}}
          ...mapGetters(['eventOdd'])   //eventOdd是一个函数,返回一个函数{eventOdd (){return this.$store.state['eventOdd]}}
        },






        //一般写法
        // methods: {
        //   increment(){
        //     this.$store.commit('INCREMENT')
        //   },
        //   decrement(){
        //     this.$store.commit('DECREMENT')
        //   },
        //   incrementIfOdd(){
        //     this.$store.dispatch('incrementIfOdd')
        //   },
        //   incrementAsync(){
        //     this.$store.dispatch('incrementAsync')
        //   }
        // }


        //简化写法
        methods: {
          ...mapMutations({
            increment: 'INCREMENT',
            decrement: 'DECREMENT'
          }),
          ...mapActions(['incrementIfOdd','incrementAsync'])
        }

        /*
          store: 组件与vuex通信的一个桥梁对象

        
        */
    }
</script>

<style scoped>

</style>
```















#### 解释

```
state:  保存状态的对象
mutations: 直接修改state中状态的对象,对象中有许多函数,这些函数直接并且只能修改state中的状态
actions: 间接修改state中的状态的对象,对象中有很多函数,函数中调用mutations的方法间接修改,可以在函数中做其他事(逻辑判断和异步)
getters: 通过state的状态计算得到的对象,监视state
```





````
组件对象如何获取state中的状态?
	方法1: $store.state.xxx
	方法2: ...mapState(['xxx'])
	
	
	
	
组件对象如何获取getters中的属性
	方法1: $store.getters.xxx
	方法2: ...mapGetters(['xxx'])
	


组件对象如何直接修改状态?
	$store.commit('mutations中的函数名')
	mapMutations()
	
	
	
组件对象如何间接修改状态?
	$store.dispatch('actions中的函数名')
	mapActions()
	


什么情况下直接修改状态?什么情况下间接修改状态?
	当我们只需要修改状态,不需要做其他事情时,我们使用mutations的方法直接修改状态
	当我们在修改状态的同时需要做一些其他的事情,比如: 逻辑判断,发送ajax请求,修改变量,定时器等,需要使用actions的方法间接修改状态
````



![vuex结构图](C:\Users\86188\Pictures\Camera Roll\vuex结构图.png)











### 源码分析



#### 文档碎片

````

        //6. DocumentFragment               文档碎片(在内存中的一个容器,如果使用普通遍历修改li,会一遍一遍修改li并渲染到页面上,效率不高,我们可以直接在容器中修改完,再直接添加到页面上,效率高)

        //创建一个fragment容器
        const fragment = document.createDocumentFragment()
        const div = document.getElementById('app')
        //将div中所有的子节点转移到fragment中

        let child
        //将div中的每一个第一个节点给child,如果赋值成功,执行{}的代码,将child给fragment,由于一个节点只能有一个父节点,所以div中的所有子节点都会到fragment中
        while(child=div.firstChild){
            fragment.appendChild(child)
        }
        //处理fragment中的li
        //children会获取指定节点的子元素,返回一个伪数组,然后使用Array的方法将伪数组转换为真数组,进行遍历
        let lis5 = Array.prototype.slice.call(fragment.children[0].children)
        lis5.forEach((li)=>{
            li.innerHTML = 'laidasnivivd'
        })

        //将处理好的fragment添加到div
        div.appendChild(fragment)
````















#### 数据代理

```
VUE数据代理: data对象的所有属性的操作(读/写)由vm对象来代理操作
好处: 通过vm对象就可以方便的操作data中的数据
实现
		//遍历data中的属性
	    Object.keys(data).forEach(function(key) {
	    	//给每个属性实现数据代理
            Object.defineProperty(me, key, {
                configurable: false,        //不可以重新定义
                enumerable: true,           // 可以枚举
                // 当vm.name读取数据时自动调用
                get: function proxyGetter() {
                    //读取并返回data中对应的属性值
                    return me._data[key];
                },
                //当vm.name = value设置数据时自动调用
                set: function proxySetter(newVal) {
                    //将最新的值保存到data对应的属性上
                    me._data[key] = newVal;
                }
            });
    	});
    	
    	
所有对象有包含get/set方法从而获取/修改数据
```















### vue脚手架

````
npm  i  @vue/cli  -g
````









#### stylus

```
脚手架中使用
	npm i stylus stylus-loader@3.0.2
	
	
	
	
<style lang="stylus">		//申明使用

  #app
    color red 
    h1
      font-size 50px
      
</style>
```



```
stylus语法介绍
	特点:
		1. 简写大括号
		2. 简写分号
		3. 样式嵌套,层级分明
```









#### 移动端适配

````
为什么要适配
	让网页的内容在不同的机型上呈现的效果一致(等比)
	
如何适配
	1. viewport适配
		1. 视觉视口: 所见即所得,屏幕的大小
		2. 布局视口: 网页的宽度
		3. 适配: 视觉视口 === 布局视口
		4. 实现: <meta name="viewport" content="width=device-width, initial-scale=1.0,user-scalable=no">
		
		
	2. rem适配
		根据设置根节点字体的大小设置rem
````



```javascript
        function remRefresh(){
            //1. 获取屏幕的宽度
            let clientWidth = document.documentElement.clientWidth

            //2. 将屏幕的宽度等分, 目的: 降低单位rem值的大小,便于换算,提高精确度
            let rem = clientWidth / 10

            //3. 设置根节点字体的大小
            document.documentElement.style.fontSize = rem + 'px'

            //4. 设置body字体大小, 目的: 由于给根节点设置字体大小,子节点会继承,所有给body设置字体大小,盖住根节点的字体大小
            document.body.style.fontSize = '16px'

        }
        //当页面显示时调用
        window.addEventListener('pageshow',()=>{
            remRefresh()
        })

        let timeoutId
        window.addEventListener('resize',()=>{
            // 防抖
            timeoutId && clearInterval(timeoutId)
            timeoutId = setTimeout(()=>{
                remRefresh()
            },2000)
        })
```





**淘宝适配方案**

```
npm i postcss-px2rem lib-flexible

	lib-flexible  淘宝适配方案
	postcss-px2rem    将项目中的px转换为rem
在项目的index.js文件中引入 import 'lib-flexible/flexible'
```





````
postcss-px2rem的使用:
	在vue.config.js的model.exports中
	css: {
	        loaderOptions: {
	            css: {},
	            postcss: {
	                plugins: [
	                    require('postcss-px2rem')({
	                    	 //lib-flexible 将屏幕分成10份(10rem)，这里设置表示设计图宽度为10*37.5=375px
           					 // 配置成 37.5 是为了兼容 没有适配 rem 布局的第三方 ui 库
	                        remUnit: 75
	                    })
	                ]
	            }
	        }
	    },

````







#### 在vue项目实现适配

````
在项目的index.js文件中引入 import 'lib-flexible/flexible'



	在vue.config.js的model.exports中
	css: {
	        loaderOptions: {
	            css: {},
	            postcss: {
	                plugins: [
	                    require('postcss-px2rem')({
	                    	 //lib-flexible 将屏幕分成10份(10rem)，这里设置表示设计图宽度为10*37.5=375px
           					 // 配置成 37.5 是为了兼容 没有适配 rem 布局的第三方 ui 库
	                        remUnit: 75
	                    })
	                ]
	            }
	        }
	    },
````















#### 路由

```
核心概念
	1. 生成路由器:		const router = new VueRouter()
	2. 安装路由器:		new Vue({router})
	3. 管理路由:		 new VueRouter({routers})   routers = [{path:'路由路径',component:'路由组件'}] 
	4. 请求路由:		 路由链接 <router-link to="路由路径"></router-link>
	5. 显示路由组件		<router-view></router-view>
```











#### vuex

````
核心概念
	store对象
		1. state:  多个组件共享的数据,用于集中管理
		2. mutations:  本质是一个函数, 用于直接修改state的状态数据, 但是只能处理同步数据,不能处理异步数据
		3. actions:  本质是一个函数, 作用: 1. 获取异步数据  2. 调用mutations同时将异步数据交给mutations
		4. getters: 函数, 作用: 同vue的computed一样1,依赖于原数据(state数据)今夕计算得到新的数据
		5. dispatch: 函数,调用action
		
	组件同Vuex交互
		1. mapState, 在computed中使用
			1. 	...mapState(['指定的state数据'])
			2.  ...mapState({key:state=>state.key})
````









#### deep

```
stylus中的deep

修改第三方样式库的样式
使用deep,深度选择器
作用: vue组件中，我们会在style里设置scoped，这个时候在组件里面在写样式是对子组件是没有效果的，如果想让设置的样式对所以子组件都			生效，这个时候得使用 /deep/ 深度选择器。
```









#### vuex刷新丢失

````
原因:
	vuex的数据保存在运行的内存中,刷新页面会重新初始化整个应用,从而重新分配内存
````



```
解决方法:
	1. 当页面刷新的时候重新发请求获取数据,存放到vuex中
	2. 利用页面刷新的事件 + sessionStorage	
		1. 在unload事件调用时将数据保存到sessionStorage
		2. 在组件重新加载后将数据取出保存到sessionStorage中
```









#### 模拟数据

````
mockjs
````









#### 解决滚动条和轮播图

```
        watch: {
            goods () {
                this.$nextTick(()=>{
                    this._initScroll()
                })
            }
        }
```







#### 响应式属性和非响应式属性

````
响应式属性: 组件初始化的时候就有,属性改变时页面中用到该属性的地方也会刷新
非响应式属性: 组件初始化时没有,属性改变页面不会刷新
````









#### vuex可以改变两个组件共同的值

````
当我们将父组件的值传入给子组件时,
子组件通过vuex改变值时,不仅子组件的值会发生变化,父组件的值也会发生变化
如果想让值发生变化时页面中所用的地方也发生变化(不是响应式属性时),使用vue.set来将值转为响应式属性
````



```
需要练习
```



```
验证结果
	当我们的父组件往子组件传入props时,子组件修改通过vuex修改父组件传入的值
	如果父组件传入的是响应式属性,当我们在vuex中修改时,父,子组件都会的值都会修改,页面也会渲染
	如果不是响应式属性,修改时,父子组件不会修改,页面也不会渲染,
	解决办法: 使用vue.set将值进行转换即可
```



**实现**

app.vue

```JavaScript
<template>
    <div>
        <div>{{a.a}}</div>
        <div>{{b.shi}}</div>
        <Hello :a="a" :b="b"/>
    </div>
</template>

<script>
    import {mapState} from 'vuex'
    import Hello from './components/hello'
    export default{

        data () {
            return {
                b : {
                    shi :  '我是不是时怠速'
                }
            }
        },

        mounted () {

        },
        computed: {
            ...mapState({
                a : state => state.a.init
            })
        },
        components: {
            Hello
        }
    }


</script>

<style scoped>
  
</style>
```



hello.vue

```javascript
<template>
    <div>
        {{a.a}}
        {{b.shi}}
        <button @click="btn">点我触发事件</button>
        <button @click="add">jiajiajia</button>
        <button @click="del">触发醉红颜的</button>
    </div>
</template>

<script>
    export default {
        props: {
            a : {
                type: Object,
                required: true
            },
            b : {
                type: Object
            }
        },

        methods: {
            btn () {
                this.$store.commit('changeA',this.a)
            },

            add () {
                this.$store.commit('add',this.a)
            },

            del () {
                this.$store.commit('del',this.b)
            }
        }

    }
</script>

<style>

</style>
```



vuex

```javascript

import Vue from 'vue'


const state = {
    init: {
        a : '我是一个帅哥'
    }
}


const mutations = {
   // 直接对值进行修改即可
    changeA (state,a) {
        Vue.set(a,'a',121212)

        // a = '你真的是一个帅哥吗?????'
    },

    add (state,a) {
        a.a++
    },

    del (state,b) {
        b.shi = 'aaabbabababaaba'
    }
}



const actions = {

}



const getters = {

}


export default {
    state,
    mutations,
    actions,
    getters
}
```











#### 项目打包时的优化操作

```
1. 实现路由懒加载
2. 关闭映射文件的生成
```



````
// 常规引入路由组件的方式
// import Msite from '../pages/Msite/Msite.vue'
// import Order from '../pages/Order/Order.vue'
// import Search from '../pages/Search/Search.vue'
// import Profile from '../pages/Profile/Profile.vue'
// import Login from '../pages/Login/Login.vue'
// import Shop from '../pages/Shop/Shop.vue'


//路由组件懒加载 : ES10     import函数
//  大大加快用户进入页面的速度
const Msite = () => import('../pages/Msite/Msite.vue')
const Order = () => import('../pages/Order/Order.vue')
const Search = () => import('../pages/Search/Search.vue')
const Profile = () => import('../pages/Profile/Profile.vue')
const Login = () => import('../pages/Login/Login.vue')
const Shop = () => import('../pages/Shop/Shop.vue')

````

```
实现组件懒加载之前,打包项目js会生成两个js文件,其中一个js文件中包含所有组件的js代码

实现组件懒加载之后,每懒加载一个组件,都会在打包后生成一个js文件,js文件有当前组件所有的js代码,当我们打开网页时,会加载当前页面的组件的js文件,不会一次加载所有组件共同的js文件

```





#### 正向代理和反向代理

```
正向代理: 代理在前端
反向代理: 代理在后端
```













#### 切换语言

```
yarn add vue-i18n
```



实现

**在src下创建文件为i18n.js**

```javascript
import Vue from 'vue'
import VueI18n from 'vue-i18n'

Vue.use(VueI18n)

function loadLocaleMessages () {
  const locales = require.context('./locales', true, /[A-Za-z0-9-_,\s]+\.json$/i)
  const messages = {}
  locales.keys().forEach(key => {
    const matched = key.match(/([A-Za-z0-9-_]+)\./i)
    if (matched && matched.length > 1) {
      const locale = matched[1]
      messages[locale] = locales(key)
    }
  })
  console.log(messages)
  return messages
}

export default new VueI18n({
  locale: localStorage.getItem('locale_key') || process.env.VUE_APP_I18N_LOCALE || 'en',
  fallbackLocale: process.env.VUE_APP_I18N_FALLBACK_LOCALE || 'en',
  messages: loadLocaleMessages()
})

```



````javascript
import Vue from 'vue'
import 'lib-flexible/flexible'
import {Button} from 'mint-ui'
//import 'mint-ui/lib/style.css'
import App from './App.vue'

import router from './router'
import store from './vuex'
import './veeValidate'

import i18n from './i18n'

//全局引入api文件
import * as API from './api'
Vue.prototype.$API = API          //使用方法: this.$API.请求方法


// 引入mock
import './mock/mockServer'

import GshopHeader from './components/GshopHeader/GshopHeader.vue'
// 全局注册组件
Vue.component('GshopHeader',GshopHeader)
Vue.component(Button.name,Button)

Vue.config.productionTip = false

// new Vue({
//   render: h => h(App),
// }).$mount('#app')

new Vue({
  el: '#app',
  components:{
    App
  },
  template: '<App/>',
  router,
  store,
  i18n
})

````



```
在src创建文件夹locales
文件夹中创建json文件,json文件中包含每一个需要转换的字的变量
在组件中使用{{$t('变量')}}来实现
```



````
1). 搭建项目
	a. 基于vue脚手架3创建的项目
	b. 引入vue-i18n
		vue add i18n
		根据提示依次指定: zh_CN --> zh_CN --> n
2). 实现应用国际化: 支持多语言显示
	a. 创建/修改国际化的message文件
		src/locales/zh_CN.json: 
			{
				"message": "你好, 国际化 !!"
			}
		src/locales/en.json
			{
				"message": "hello i18n !!"
			}
	b. 在组件中读取当前应用指定locale的message
		$t('message')
	c. 读取/设置当前应用的locale
		读取: this.$i18n.locale
		更新: this.$i18n.locale = 'en' // 一旦更新整个应用中所有的message都自动更新为en的版本
	d. 保存/读取当前设置的locale
		保存: localStorage.setItem('locale_key', 'en')
		读取: locale: localStorage.getItem('locale_key')  // src/i18n.js
````











#### vue-scroller

```
yarn add vue-scroller
import VueScroller from 'vue-scroller'
Vue.user(VueScroller)


获取scroller的实例

this.$refs.scroller.
		triggerPullToRefresh()			触发下拉刷新的回调
		finishPullToRefresh()			停止下拉刷新
		finishInfinite()				停止上拉刷新,如果传入true,就会出现没有数据了,传入false,代表还有
```







#### 实现页面左右滑动更新组件

```
nav
	1.更新高亮的nav内容
	        this.nowIndex = this.$route.path === '/one' ? 0 : this.$route.path === '/two' ? 1 : this.$route.path === '/three' ? 2 : this.$route.path === '/four' ? 3 : this.$route.path === '/five' ? 4 : 0;
	判断当前显示的组件是哪一个,然后使他的高亮
	
	2.当滑动页面时,通过swiper发送的下标,执行以下操作
		1. 使其高亮
		2. 路由跳转
		
	3.点击nav时,将下标发给swiper,使swiper滚动,当swiper滚动时,会更新路由链接
```







#### 实现7天免登陆

```
1、第一次登录的时候，前端调后端的登陆接口，发送用户名和密码

2、后端收到请求，验证用户名和密码，验证成功，就给前端返回一个token

3、前端拿到token，将token存储到localStorage和vuex中，并跳转路由页面

4、前端每次跳转路由，就判断 localStroage 中有无 token ，没有就跳转到登录页面，有则跳转到对应路由页面

5、每次调后端接口，都要在请求头中加token

6、后端判断请求头中有无token，有token，就拿到token并验证token，验证成功就返回数据，验证失败（例如：token过期）就返回401，请求头中没有token也返回401

7、如果前端拿到状态码为401，就清除token信息并跳转到登录页面
```







#### 刷新页面数据不丢失

```
将数据保存到localStorage中
```









#### vue重写数组

```
  'push',
  'pop',
  'shift',
  'unshift',
  'splice',
  'sort',
  'reverse'
```

















## 微信小程序



### 数据绑定

```
小程序
	1. data中初始化数据
	2. 修改数据: this.setData()
		注意: 修改数据是同步的
	3. 事件流: 单项
		
		
vue
	1. data中初始化数据
	2. 修改数据: this.key = value
	3. 事件流: 单项 , 但是数据绑定为双向
	
	
react
	1. state中修改数据
	2. 修改数据: this.setState()
		注意: 修改数据是异步的
	3. 事件流: 单项
```







```
如何向事件对象传参
id
data-id
```















































## 回顾





### call,apply,bind

```
call,apply
	调用函数,指定函数中的this为第一个参数的值
bind
	返回一个新的函数,函数内部会调用原来的老的函数,
	新的函数this指向window
	老的函数this指向bind方法第一个参数的值
	注意: 如果obj为null/undefined,this为window
```









````
当在项目中下载webpack后
如果运行webpack,会显示没有该指令,因为在项目中没有配置
此时为  npx webpack 

实时监视项目改动,然后自动编译打包(打包到硬盘中),但是不会自动刷新浏览器
  npx  webpack  --watch
  
 webpack-dev-server
 	实时监视项目改动,自动编译到内存中,会刷新浏览器
````

````
webpack为什么局部下载
	防止多个项目需要使用不同版本的webpack,导致出错
````

```
npx是查找局部的指令
npm是查找全局的指令
如果项目中没有在package.json中配置局部的指令,那么使用npm就会报错,只能使用npx
如果项目中配置了指令,就可以使用npm
```









```
原型对象的老大就是Object
Object后面就是null
```









### 监听手机物理返回键

````
window.addEventListener('popstate',()=>{
            this.$router.push('/login')
          })
````

























## websocket

```
websocket是基于http的一种新的网络协议,它实现了浏览器和服务器全双工通信
	全双工: 客户端可以主动发数据给服务器,服务器可以主动发数据给客户端
	websocket是持久协议
	http是非持久协议
	应用场景: 实时推送信息,聊天,客服咨询等
```







### 基本使用



```
使用
	let socket = new WebSocket(url,options)
```





**websocket事件**

| open    | 连接建立时触发             |
| ------- | -------------------------- |
| message | 客户端接收服务器数据时触发 |
| error   | 通信发生错误时触发         |
| close   | 连接关闭时触发             |





**websocket方法**

| send()  | 使用连接发送数据 |
| ------- | ---------------- |
| close() | 关闭连接         |













### node中使用

```
yarn add nodejs-websocket
```

```javascript
const ws = require('nodejs-websocket')
const PORT = 3000

// 创建一个server

// 每次只有有用户连接,函数就会执行,会给当前连接的用户创建一个connect对象
const  server = ws.createServer(conn => {
    console.log('有用户连接上来了')

    // 每当接收到用户传递来的数据,这个text事件就会触发
    conn.on('text', data => {
        console.log('接收到用户传递来的数据',data)
        // 给用户返回一个数据(可以对数据进行处理)
        conn.send(data)
    })

    conn.on('close', ()=>{
        console.log('断开连接了')
    })

    // 注册error事件(不然当用户断开连接会报错,导致代码停止)
    conn.on('error', ()=>{
        console.log('报错')
    })

})  


server.listen(PORT,() => {
    console.log('websocket服务器启动成功了,监听了端口' + PORT)
})
```













### socket.io

````
注意: 使用socket.io实现websocket协议需要在服务器和客户端都使用socket.io框架
````





#### 在node环境下使用express框架+socket.io框架实现websocket通信

```javascript
const express = require('express');					// 引入express
const app = express();								// 调用express返回对象
const http = require('http');						// 引入node环境下自带的模块http
const server = http.createServer(app);				// 使用http创建一个服务器,服务器内部使用express框架
const { Server } = require("socket.io");			// 引入socket.io中的Server方法
const io = new Server(server);						// 传入服务器实例化并返回一个对象

app.get('/', (req, res) => {
  res.sendFile(__dirname + '/index.html');			// 返回一个html文件(返回给浏览器会自动解析)
});

io.on('connection', (socket) => {
  console.log('a user connected');
});

server.listen(3000, () => {
  console.log('listening on *:3000');
});
```







```
将信息发给所有人
	io.emit(事件名,data)
	
将信息发给除发件人之外的所有人
	io.on('connection', socket => {
		socket.broadcast.emit(事件名,data)
	})
```













## 文件上传

```
URL.createObjectURL() 静态方法会创建一个 DOMString，其中包含一个表示参数中给出的对象的URL。这个 URL 的生命周期和创建它的窗口中的 document 绑定。这个新的URL 对象表示指定的 File 对象或 Blob 对象。

URL.createObjectURL(blob)和FileReader.readAsDataURL(file)很相似，下面是个人的一些理解，如有不正确的地方，欢迎指出：

主要区别
    通过FileReader.readAsDataURL(file)可以获取一段data:base64的字符串

    通过URL.createObjectURL(blob)可以获取当前文件的一个内存URL

执行时机：
    createObjectURL是同步执行（立即的）
    FileReader.readAsDataURL是异步执行（过一段时间）
    
内存使用：
createObjectURL返回一段带hash的url，并且一直存储在内存中，直到document触发了unload事件（例如：document close）或者执行revokeObjectURL来释放。
FileReader.readAsDataURL则返回包含很多字符的base64，并会比blob url消耗更多内存，但是在不用的时候会自动从内存中清除（通过垃圾回收机制）
兼容性方面两个属性都兼容ie10以上的浏览器。

优劣对比：
使用createObjectURL可以节省性能并更快速，只不过需要在不使用的情况下手动释放内存
如果不太在意设备性能问题，并想获取图片的base64，则推荐使用FileReader.readAsDataURL
```











### ArrayBuffer

```

```







```
window.btoa()		编码base64
window.atob()		解码base64
```





```
文件上传
	前端:
		使用<input type="file"/>获取数据,然后使用FormData和ajax将数据上传到服务器
	后端:
		服务器使用multer中间件将数据保存到服务器
```











## vue脚手架的基本配置

```
第一步
	下载less
	yarn add less less-loader@5.0.0  -D
	
	
第二步
	在vue.config.js中关闭eslint语法检查和开启vue解析器
	runtimeCompiler: true,
    lintOnSave: false,
    
    
第三步
	配置路径别名
	chainWebpack: (config)=>{
        //修改文件引入自定义路径
        config.resolve.alias
            .set('@', require('path').join(__dirname,'src'))
    }
```



















## nprogress

```
实现进度条

引入
	import NProgress from 'nprogress'
	import 'nprogress/nprogress.css'
	
	
使用
	NProgress.start()				出现
	NProgress.done()				消失
```













## token实现免登陆思路

```
在前后端完全分离的情况下，Vue项目中实现token验证大致思路如下：

1、第一次登录的时候，前端调后端的登陆接口，发送用户名和密码

2、后端收到请求，验证用户名和密码，验证成功，就给前端返回一个token

3、前端拿到token，将token存储到localStorage和vuex中，并跳转路由页面

4、前端每次跳转路由，就判断 localStroage 中有无 token ，没有就跳转到登录页面，有则跳转到对应路由页面

5、每次调后端接口，都要在请求头中加token

6、后端判断请求头中有无token，有token，就拿到token并验证token，验证成功就返回数据，验证失败（例如：token过期）就返回401，请求头中没有token也返回401

7、如果前端拿到状态码为401，就清除token信息并跳转到登录页面
```















## 自定义封装组件库



```
组件通讯
组件插槽
props校验
```









### 引入iconfont创建图标组件

```
1. 在iconfont官网下载一个项目

2. 将iconfont项目中的iconfont.css, iconfont.tff, iconfont.woff, iconfont.woff2引入到vue项目中

3. 在main.js中引入iconfont.css

4. 更改iconfont.css中的类名
    /* 凡是类名中包含l-icon的字段的类,都会加上一下样式 */
     [class*='l-icon']{
      font-family: "iconfont" !important;
      font-size: 16px;
      font-style: normal;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
    }

    .l-icon-zhuanji-:before {
      content: "\e60b";
    }
    
5. 定义组件,组件中引入图标字体,不需要向以前一样还要引入iconfont,只需要引入图标自身的类名即可,由于类名包含l-icon,所以会引入原本		iconfont类名的样式
	<i class="l-icon-Next"></i>
```











### 组件绑定事件

````
当给组件定义点击事件时,点击组件时,组件没有响应,click不是原生click事件,而是自己定义的click事件
<Button @click="click2">			

此时,需要在组件内部定义click事件(原生的click事件),click事件触发绑定在组件上的click事件(自定义的)
<div @click="handle"></div>

methods: {
	handle (e) {
		this.$emit('click',e)
	}
}

此时,组件就可以使用点击事件
````









### sync

```
作用: 一个语法糖,使子组件改变父组件的属性

默认情况下,子组件修改父组件的属性:
	父组件
	<template>
		<l-aaaa :visible=visible @close="colse"><l-aaaa>
	</template>
	<script>
		data () {
			return {
				visible=false
			} 
		},
		methods: {
			close (value) {
				this.visible = value
			}
		}
	</script>
	
	子组件
	<template>
		<button @click=$emit('close',false)>
	</template>
	
	
	
使用sync
	父组件
	<template>
		<l-aaaa :visible.sync=visible><l-aaaa>
	</template>
	<script>
		data () {
			return {
				visible=false
			} 
		},
	</script>
	
	子组件
	<template>
		<button @click=$emit('update:visible',false)>
	</template>
	
	
sync是一个语法糖,省略了几步,使子组件修改父组件更加简单
	不需要给子组件上绑定自定义事件,只需要传递props时给prop加上.sync,
	子组件修改时只需要$emit('update:prop名',修改的值)

```













## webpack总结



````
webpack是一个静态模块打包工具(开始只能打包json和js)
````





### webpack如何打包

```
以入口文件开始,递归的构建一个依赖图(先查看入口文件有哪些依赖模块,在查看入口文件的依赖模块有哪些依赖模块,依次递归),并生成一个或多个bundle文件

```







### webpack和webpack-cli的区别

````
webpack是做js打包工作的
webpack-cli解析webpack命令,命令内部使用webpack功能
````







### 为什么不全局下载,而是局部下载

````

防止版本不同,导致打包出错
	
	
如果全局下载了webpack,局部也下载了,我们可以使用以下两种办法使用局部webpack
	1. npx webpack			使用局部webpack进行打包
	2. 将webpack命令配置到package.json中的scripts中
	
````







### webpack的组成

```
1. 模式(mode)
	选项
		1. none
		2. development(开发)
		3. production(生产,默认)
		
2. 入口(entry)
	打包的入口文件,可以指定多个
	
3. 出口(output)
	打包后文件
4. loader
	打包webpack不能打包的文件资源,比如图片,html文件,等等
5. 插件(plugin)
	可以用于执行范围更广的任务。插件的范围包括，从打包优化和压缩
```









### babel和eslint

````
babel
	打包js
eslint
	语法检查
````















