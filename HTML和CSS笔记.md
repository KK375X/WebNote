# 第一章：HTML基础知识

## 第一节：基础知识

### 1、HTML基本框架

```html
<html>
	<head>		
    	<title>测试</title>	//‘测试’出现在网页地址栏处
    </head>
    <body>		//网页的文本编辑处
        文本编辑区
        <!-- HTML的注释 -->
    </body>
</html>
```

### 2、属性

```html
<html>
	<head>		
    	<title>测试</title>	
    </head>
    <body>		
    <!-- 
		属性：在标签中设置属性，属性是一个键值对（x=y）
		属性的作用是设置内容如何显示
		font标签是标记字体颜色，color为属性名，#dc143c为属性值;size为属性名，3为属性值。
	--> 
        <h1>
            <h1>这是我的<font color="red" size="3">第一个</font>网页！</h1>
        </h1>
    </body>
</html>
```

### 3、进制

```html
<!--
文档声明：DOCTYPE
	- 文档声明用来告诉浏览器当前的版本
	- HTML5的文档声明：<!DOCTYPE HTML>
-->
<!--
进制：
	- 十进制：满十进一
	- 二进制：满二进一
	- 八进制：满八进一
		- 计数：0 1 2 3 4 5 6 7 10 11 12 13 ... 17 20 21 ...
		- 单位数字：8个（0 ~ 7）
	- 十六进制：满十六进一
		- 计数：0 1 2 3 4 ... 8 9 A B C D E F 10 11 12 13 ... 19 1A 1B 1C ... 1F 20 ...
		- 单位数字：十六个（0 ~ F）
-->
```

## 第二节：字符编码，基本框架和文档的使用

### 1、字符编码

- 所有的数据都是以二进制存储在计算机中的，当我们需要查看数据时，计算机会将编码转换成文字形式。
- 编码：将字符转换成二进制码的过程。
- 解码：将二进制码转换成字符的过程。
- 字符集（charset）：编码和解码所采用的规则
- 乱码问题：编码和解码所采取的字符集不同，就会出现乱码问题。
- 常见的字符集：ASCII 、ISO88591 、GB2312 、GBK 、UTF-8

```html
<!-- 可以通过meta标签设置网页的字符集，避免乱码问题 -->
<meta charset="utf-8">
```

### 2、基本框架

```html
<!-- 文档声明，声明当前网页的版本 -->
<!DOCTYPE HTML>

<!-- HTML的根标签，网页中的所有内容都要写在根标签中 -->
<html>

    <!-- head是网页的头部，head中的内容不会在网页中直接出现，主要用来帮助浏览器来解析网页 -->
    <head>
    
        <!-- meta标签用来设置网页的元数据，这里的meta标签用来设置字符集编码，避免乱码问题 -->
        <meta charset="utf-8">
        
        <!-- title的内容会显示在网页的标题栏中 -->
        <title>网页的标题</title>
    
    </head>
    
    <!-- body是html的子元素，表示网页的主体，网页中所有的可见内容都写在body中 -->
    <body>
    
        <!-- 此处是文本编辑区 -->
    
    </body>

</html>
```

### 3、文档的使用

> w3school网址：https://www.w3school.com.cn/index.html
>
> 菜鸟教程网址：https://www.runoob.com/
>
> 类似于java的API文档。



## 第三节：标签的学习

### 1、实体

> **在网页中有些特殊字符会失去我们想表达的意思，所以需要实体来编写这些特殊符号，类似于转义字符。**

```html
<!--
实体的语法：
	&实体的名字;
		&nbsp;	空格
		&gt;	小于号
		&lt;	大于号
		详见文档使用提供的网址。
-->
```

### 2、meta标签

> **meta标签主要用于设置网页中的元数据**
>
> - charset：指定网页的字符集
> - name：指定网页的数据名称
> - content：指定网页的数据内容
> - http-equiv：网页的重定向

```html
<!-- 字符集为utf-8，元数据的名称为keywords，值为"HTML5,前端" -->
<!-- keywords 表示网站的关键字，可以同时指定多个关键字 -->
<meta charset="utf-8" name="keywords" content="HTML5,前端">

<!-- 将页面重定向到另一个网站 -->
<!-- 只需要改动content里面的数据，3表示3秒之后执行跳转，url表示跳转到具体某个网页 -->
<meta http-equiv="refresh" content="3;url=https://www.baidu.com">


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8" http-equiv="refresh" content="3;https://www.baidu.com">
    <title>测试</title>
</head>
<body>
    <p>今天天气真不错！</p>
</body>
</html>
```

### 3、语义化标签

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>测试</title>
    </head>
    <body>
        <!--  标签所展示的内容，在页面中独占一行的元素称为块元素（block element） -->
        <!--  标签所展示的内容，在页面中不会独占一行的元素称为行内元素（inline element） -->
        <!--
            标题标签（块元素）：
                h1~h6，一共有六级标题
        -->
        <h1>一级标题</h1>
        <h2>二级标题</h2>
        <h3>三级标题</h3>
        <h4>四级标题</h4>
        <h5>五级标题</h5>
        <h6>六级标题</h6>

        <!--
            p标签表示页面中的一个段落（块元素）
        -->
        <p>今天天气不错！！！</p>
        <p>你说的对！！！</p>

        <!--
            hgroup标签用来为标题进行分组，可以将一组标题放在其中（块元素）
        -->
        <hgroup>
            <h1>少小离家老大回</h1>
            <h2>乡音未改鬓毛衰</h2>
        </hgroup>

        <!--
            em标签用于语音语调的加重，表现为斜体为加粗字样（行内元素）
        -->
        <p>今天的天气<em>真的很</em>不错！！！</p>

        <!--
            strong标签表示强调，表现为加粗体字样行内元素）
        -->
        <p>我今天<strong>必须完成</strong>作业！！！</p>

        <!--
            blockquote标签：表示长引用，表现为出现在下一行中，独占一行，并且自动缩进
        -->
        周恩来总理说：<blockquote>为中华之崛起而读书！！！</blockquote>

        <!--
            q标签：表示段引用，表现为出现在本行中，不会独占一行，自动加上双引号
        -->
        子曰：<q>学而时习之，不亦说乎！！！</q>

        <!--
            br标签：表示换行
        -->
        <br>        <!-- 一个br标签没啥效果，至少两个才有效果 -->
        <p>安能常少年！！！</p>
        
        <!--
            html5之后新加的标签（不常用）：
                header 表示网页的头部
                main 表示网页的主体，头部以下（一个页面只有一个main）
                footer 表示网页的底部
                nav 表示网页的导航
                aside 和主体相关的其他内容（侧边栏）
                article 表示一个独立的文章
                section 表示一个独立的区块，上面的标签不能表示时，用section
    	-->
        <header>网页的头部</header>
        <main>网页的主体</main>
        <footer>网页的底部</footer>
        <nav>网页的导航</nav>
        <aside>侧边栏</aside>
        <article>独立的文章</article>
        <section>独立的区块</section>

    	<!--
            常用的语义化标签：
                div 没有语义，就用来表示一个区块，目前最主要的布局元素
                span 行内元素，没有语义，一般用于在网页中选中文字
        -->
        <div>表示一个区块</div>
        <span>网页中选中文字</span>
    </body>
</html>

<!-- 更多语义化标签可以去w3school或者菜鸟教程学习 -->
```

> #### 块元素和行内元素
>
> #### 1、块元素：
>
> - 在网页中一般通过块元素对网页进行布局
>
> #### 2、行内元素：
>
> - 行内元素主要用来包裹文字
> - 一般情况下会在块元素中放行内元素
> - p标签中不能放任何的块元素
> - 块元素能放任何东西

### 4、列表

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>测试</title>
</head>
<body>
    <!--
        列表：
            - 有序列表：使用ol标签创建有序列表，使用li表示列表项
            - 无序列表：使用ul标签创建无序列表，使用li表示列表项
            - 定义列表：使用dl标签创建定义列表，使用dt表示定义的内容，使用dd对内容作解释说明

            列表之间可以互相嵌套
    -->
    <!-- 有序列表 -->
    <ol>
        <li>第一节</li>
        <li>第二节</li>
        <li>第三节</li>
    </ol>

    <!--无序列表-->
    <ul>
        <li>第一节</li>
        <li>第二节</li>
        <li>第三节</li>
    </ul>

    <!-- 定义列表 -->
    <dl>
        <dt>第一节</dt>        <!-- 定义内容 -->
        <dd>第一节学习顺序结构</dd>      <!-- 对内容作解释说明，自动转换到下一行，缩进 -->
        <dt>第二节</dt>
        <dd>第二节学习分支结构</dd>
        <dt>第三节</dt>
        <dd>第三节学习循环结构</dd>
    </dl>

    <!-- 列表的嵌套 -->
    <ul>
        <li>
            第一节
                <ul>
                    <li>第一小节</li>
                    <li>第二小节</li>
                    <li>第三小节</li>
                </ul>
        </li>
    </ul>
</body>
</html>
```

### 5、超链接

> #### 超链接的基础用法

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>测试</title>
</head>
<body>
    <!--
        超链接可以让我们从一个页面跳转到其他页面，或者是当前页面的其他位置
        使用 a 标签来定义超链接，在 a 标签中可以放处它自身外的任何元素
        属性：href 指定跳转的目标网址或位置
    -->
    <h2>初步使用超链接</h2>
    <a href="https://baidu.com">百度搜索超链接</a>
    <br><br>

    <h2>使用绝对路径超链接</h2>
    <!-- 绝对路径：直接可以到达的目标路径，例如各大网站的网址，直接输入便可到达 -->
    <a href="https://baidu.com">百度搜索超链接</a>
    <a href="https://www.bilibili.com/">哔哩哔哩超链接</a>
    <a href="https://www.csdn.net/">CSDN超链接</a>
    <br><br>

    <!--
        当需要跳转到一个服务器内部时，一般都要使用相对路径
            相对路径都会是哟个 . 或者 .. 作为开头
                ./
                ../
            ./ 可以省略，如果不写 ./ 也不写 ../ 就相当于写了 ./

            ./ 表示当前文件所在的位置目录

            ../ 表示当前文件所在目录的上一级目录
    -->
    <h2>使用相对路径超链接</h2>
    <a href="./本文件夹的超链接测试.html">本文件夹超链接测试页面</a>
    <a href="../上一级超链接测试.html">上一级的文件夹超链接测试页面</a>
    <br><br>

    <!--
        target属性，用来指定链接打开的位置
            可选值：
                _self 默认值，在当前页面打开超链接
                _blank 在新的窗口打开超链接
    -->
    <h2>超链接打开方式测试</h2>
    <a href="https://www.baidu.com" target="_self">当前窗口打开百度超链接</a>    <!-- _self 当前窗口打开 -->
    <a href="https://www.baidu.com" target="_blank">新窗口下打开百度超链接</a>    <!-- _blank 新窗口打开 -->
	<br><br>
       
</body>
</html>

<!-- 详见源代码 -->
```

> #### 超链接的其他用法

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>
</head>
<body>
    
    <a href="#bottom">到底部</a>       <!-- 点击即可到底部-->
    <br>
    
    <a href="#zhongjian">去第三自然段</a>      <!-- 点击即可到中间位置 -->
    <br>
    
    <!-- 可以使用javascript:;来作为href的值，此时点击没有任何反应 -->
    <a href="javascript:;">占位符</a>
    
    <p>开平元年正月丁亥，帝回自长芦，次于魏州。节度使罗绍威以帝回军，虑有不测之患，由是供亿甚至，因密以天人之望切陈之。帝虽拒而不纳，然心德之。壬寅，帝至自长芦。是日，有庆云覆于府署之上。甲辰，天子遣御史大夫薛贻矩来传禅代之意。贻矩谒帝，陈北面之礼，帝揖之升阶。贻矩曰：“殿下功德及人，三灵所卜已定。皇帝方议裁诏，行舜、禹之事，臣安敢违。”既而拜伏于砌下，帝侧躬以避之。 二月戊申，帝之家庙栋间有五色芝生焉，状若芙蓉，紫烟蒙护，数日不散。又，是月，家庙第一室神主上，有五色衣自然而生，识者知梁运之兴矣。唐乾符中，木星入南斗，数夕不退，诸道都统晋国公王铎观之，问诸知星者吉凶安在，咸曰：“金火土犯斗即为灾，唯木当为福耳！”或亦然之。 时有术士边冈者，洞晓天文，博通阴阳历数之妙，穷天下之奇秘，有先见之明，虽京房、管辂不能过也。铎召而质之，冈曰：“惟木为福神，当以帝王占之。然则非福于今，必当有验于后，未敢言之，请他日证其所验。”一日，又密召冈，因坚请语其详，至于三四，冈辞不获。铎乃屏去左右，冈曰：“木星入斗，帝王之兆也。木在斗中，‘朱’字也。以此观之，将来当有朱氏为君者也，天戒之矣。且木之数三，其祯也应在三纪之内乎！”铎闻之，不复有言。天后朝有谶辞云：“首尾三鳞六十年，两角犊子自狂颠，龙蛇相斗血成川。”当时好事者解云：“两角犊子，牛也，必有牛姓干唐祚。”故周子谅弹牛仙客，李德裕谤牛僧孺，皆以应图谶为辞。然“朱”字“牛”下安“八”，八即角之象也，故朱滔、朱泚构丧乱之祸，冀无妄之福，岂知应之帝也。 四月，唐帝御札敕宰臣张文蔚等备法驾奉迎梁朝。</p>
    <p>开平元年正月丁亥，帝回自长芦，次于魏州。节度使罗绍威以帝回军，虑有不测之患，由是供亿甚至，因密以天人之望切陈之。帝虽拒而不纳，然心德之。壬寅，帝至自长芦。是日，有庆云覆于府署之上。甲辰，天子遣御史大夫薛贻矩来传禅代之意。贻矩谒帝，陈北面之礼，帝揖之升阶。贻矩曰：“殿下功德及人，三灵所卜已定。皇帝方议裁诏，行舜、禹之事，臣安敢违。”既而拜伏于砌下，帝侧躬以避之。 二月戊申，帝之家庙栋间有五色芝生焉，状若芙蓉，紫烟蒙护，数日不散。又，是月，家庙第一室神主上，有五色衣自然而生，识者知梁运之兴矣。唐乾符中，木星入南斗，数夕不退，诸道都统晋国公王铎观之，问诸知星者吉凶安在，咸曰：“金火土犯斗即为灾，唯木当为福耳！”或亦然之。 时有术士边冈者，洞晓天文，博通阴阳历数之妙，穷天下之奇秘，有先见之明，虽京房、管辂不能过也。铎召而质之，冈曰：“惟木为福神，当以帝王占之。然则非福于今，必当有验于后，未敢言之，请他日证其所验。”一日，又密召冈，因坚请语其详，至于三四，冈辞不获。铎乃屏去左右，冈曰：“木星入斗，帝王之兆也。木在斗中，‘朱’字也。以此观之，将来当有朱氏为君者也，天戒之矣。且木之数三，其祯也应在三纪之内乎！”铎闻之，不复有言。天后朝有谶辞云：“首尾三鳞六十年，两角犊子自狂颠，龙蛇相斗血成川。”当时好事者解云：“两角犊子，牛也，必有牛姓干唐祚。”故周子谅弹牛仙客，李德裕谤牛僧孺，皆以应图谶为辞。然“朱”字“牛”下安“八”，八即角之象也，故朱滔、朱泚构丧乱之祸，冀无妄之福，岂知应之帝也。 四月，唐帝御札敕宰臣张文蔚等备法驾奉迎梁朝。</p>
    <p id="zhongjian">开平元年正月丁亥，帝回自长芦，次于魏州。节度使罗绍威以帝回军，虑有不测之患，由是供亿甚至，因密以天人之望切陈之。帝虽拒而不纳，然心德之。壬寅，帝至自长芦。是日，有庆云覆于府署之上。甲辰，天子遣御史大夫薛贻矩来传禅代之意。贻矩谒帝，陈北面之礼，帝揖之升阶。贻矩曰：“殿下功德及人，三灵所卜已定。皇帝方议裁诏，行舜、禹之事，臣安敢违。”既而拜伏于砌下，帝侧躬以避之。 二月戊申，帝之家庙栋间有五色芝生焉，状若芙蓉，紫烟蒙护，数日不散。又，是月，家庙第一室神主上，有五色衣自然而生，识者知梁运之兴矣。唐乾符中，木星入南斗，数夕不退，诸道都统晋国公王铎观之，问诸知星者吉凶安在，咸曰：“金火土犯斗即为灾，唯木当为福耳！”或亦然之。 时有术士边冈者，洞晓天文，博通阴阳历数之妙，穷天下之奇秘，有先见之明，虽京房、管辂不能过也。铎召而质之，冈曰：“惟木为福神，当以帝王占之。然则非福于今，必当有验于后，未敢言之，请他日证其所验。”一日，又密召冈，因坚请语其详，至于三四，冈辞不获。铎乃屏去左右，冈曰：“木星入斗，帝王之兆也。木在斗中，‘朱’字也。以此观之，将来当有朱氏为君者也，天戒之矣。且木之数三，其祯也应在三纪之内乎！”铎闻之，不复有言。天后朝有谶辞云：“首尾三鳞六十年，两角犊子自狂颠，龙蛇相斗血成川。”当时好事者解云：“两角犊子，牛也，必有牛姓干唐祚。”故周子谅弹牛仙客，李德裕谤牛僧孺，皆以应图谶为辞。然“朱”字“牛”下安“八”，八即角之象也，故朱滔、朱泚构丧乱之祸，冀无妄之福，岂知应之帝也。 四月，唐帝御札敕宰臣张文蔚等备法驾奉迎梁朝。</p>
    <p>开平元年正月丁亥，帝回自长芦，次于魏州。节度使罗绍威以帝回军，虑有不测之患，由是供亿甚至，因密以天人之望切陈之。帝虽拒而不纳，然心德之。壬寅，帝至自长芦。是日，有庆云覆于府署之上。甲辰，天子遣御史大夫薛贻矩来传禅代之意。贻矩谒帝，陈北面之礼，帝揖之升阶。贻矩曰：“殿下功德及人，三灵所卜已定。皇帝方议裁诏，行舜、禹之事，臣安敢违。”既而拜伏于砌下，帝侧躬以避之。 二月戊申，帝之家庙栋间有五色芝生焉，状若芙蓉，紫烟蒙护，数日不散。又，是月，家庙第一室神主上，有五色衣自然而生，识者知梁运之兴矣。唐乾符中，木星入南斗，数夕不退，诸道都统晋国公王铎观之，问诸知星者吉凶安在，咸曰：“金火土犯斗即为灾，唯木当为福耳！”或亦然之。 时有术士边冈者，洞晓天文，博通阴阳历数之妙，穷天下之奇秘，有先见之明，虽京房、管辂不能过也。铎召而质之，冈曰：“惟木为福神，当以帝王占之。然则非福于今，必当有验于后，未敢言之，请他日证其所验。”一日，又密召冈，因坚请语其详，至于三四，冈辞不获。铎乃屏去左右，冈曰：“木星入斗，帝王之兆也。木在斗中，‘朱’字也。以此观之，将来当有朱氏为君者也，天戒之矣。且木之数三，其祯也应在三纪之内乎！”铎闻之，不复有言。天后朝有谶辞云：“首尾三鳞六十年，两角犊子自狂颠，龙蛇相斗血成川。”当时好事者解云：“两角犊子，牛也，必有牛姓干唐祚。”故周子谅弹牛仙客，李德裕谤牛僧孺，皆以应图谶为辞。然“朱”字“牛”下安“八”，八即角之象也，故朱滔、朱泚构丧乱之祸，冀无妄之福，岂知应之帝也。 四月，唐帝御札敕宰臣张文蔚等备法驾奉迎梁朝。</p>
    <p>开平元年正月丁亥，帝回自长芦，次于魏州。节度使罗绍威以帝回军，虑有不测之患，由是供亿甚至，因密以天人之望切陈之。帝虽拒而不纳，然心德之。壬寅，帝至自长芦。是日，有庆云覆于府署之上。甲辰，天子遣御史大夫薛贻矩来传禅代之意。贻矩谒帝，陈北面之礼，帝揖之升阶。贻矩曰：“殿下功德及人，三灵所卜已定。皇帝方议裁诏，行舜、禹之事，臣安敢违。”既而拜伏于砌下，帝侧躬以避之。 二月戊申，帝之家庙栋间有五色芝生焉，状若芙蓉，紫烟蒙护，数日不散。又，是月，家庙第一室神主上，有五色衣自然而生，识者知梁运之兴矣。唐乾符中，木星入南斗，数夕不退，诸道都统晋国公王铎观之，问诸知星者吉凶安在，咸曰：“金火土犯斗即为灾，唯木当为福耳！”或亦然之。 时有术士边冈者，洞晓天文，博通阴阳历数之妙，穷天下之奇秘，有先见之明，虽京房、管辂不能过也。铎召而质之，冈曰：“惟木为福神，当以帝王占之。然则非福于今，必当有验于后，未敢言之，请他日证其所验。”一日，又密召冈，因坚请语其详，至于三四，冈辞不获。铎乃屏去左右，冈曰：“木星入斗，帝王之兆也。木在斗中，‘朱’字也。以此观之，将来当有朱氏为君者也，天戒之矣。且木之数三，其祯也应在三纪之内乎！”铎闻之，不复有言。天后朝有谶辞云：“首尾三鳞六十年，两角犊子自狂颠，龙蛇相斗血成川。”当时好事者解云：“两角犊子，牛也，必有牛姓干唐祚。”故周子谅弹牛仙客，李德裕谤牛僧孺，皆以应图谶为辞。然“朱”字“牛”下安“八”，八即角之象也，故朱滔、朱泚构丧乱之祸，冀无妄之福，岂知应之帝也。 四月，唐帝御札敕宰臣张文蔚等备法驾奉迎梁朝。 </p>
    
    <!--
        # 代表可以直接回到顶部的href的值

        id 属性（唯一不重复的）
            - 每一个标签都可以添加一个id属性
            - id属性就是元素的唯一标识，同一个页面中不能出现重复的id属性（字母开头，区分大小写）

        可以跳转到页面的其他位置，只需将href属性设置 #目标元素的id属性值
     -->
    <a id="bottom" href="#">回到顶部</a>    <!-- 点击即可到顶部，并设置了id值 -->
    
</body>
</html>
```

### 6、图片标签和格式

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>
</head>
<body>
    
     <!--
        - 使用img标签来引入外部图片，img标签是一个自结束标签
        - img属于替换元素，介于块元素和行内元素之间
        - 属性：
            - src属性指定图片的路径（和超链接规则一样），可以来自本地文件夹，也可以从网上获取图片链接
            - alt属性是对图片的描述，描述默认不可见，部分浏览器在图片加载失败时显示描述字样
                搜索引擎会根据alt中的内容来识别图片，如果不写alt属性则图片不会被搜索引擎所收录
            - width属性指定图片宽度（单位是像素）
            - height属性指定图片高度（单位是像素）
        - 图片格式：
            - jpeg（jpg）：支持颜色丰富，不支持动图，适合用来显示照片
            - gif：支持颜色少，支持简单透明，支持动图，适合颜色单一图片，动图
            - png：支持颜色丰富，支持复杂透明，不支持动图，适合颜色丰富，复杂透明图片（专为网页而生）
            - webp：由谷歌推出，具备其他图片格式的所有优点，缺点是兼容性不好
            - base64：将图片使用base64进行编码，可以直接将图片转换成字符，将编码放在src属性中

        - 注意：
            - PC端不建议修改图片大小，需要多大的就裁剪多大
            - 移动端需要对图片进行缩放（大图缩小）
     -->
    <img src="./测试相册/1.jpg" width="500" alt="流星">      <!-- 本地文件 -->
    <img src="https://img0.baidu.com/it/u=1739835453,1032590079&fm=26&fmt=auto&gp=0.jpg" width="500" 			 alt="五星红旗">    <!-- 获取网上的图片 -->
    
</body>
</html>
```

### 7、内联框架

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>
</head>
<body>
    <!--
        内联框架：用于向当前页面引入一个其他页面
            - src指定要引入的网页的路径
            - width和height设置宽度和高度
            - frameborder指内联框架样式，0表示无边框，1表示有边框（默认）
    -->
    
    <!-- 引入本地文件 -->
    <iframe src="../图片标签/测试相册/1.jpg" width="800" height="500" frameborder="0"></iframe> 
    <!-- 引入网上网页 -->
    <iframe src="https://qq.com" width="800" height="500" frameborder="0"></iframe>    
</body>
</html>
```

### 8、音视频播放

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>
</head>
<body>
    <!--
        audio标签用来引入一个音频文件（可以是本地或者网上）
            - 音视频文件引入时，默认是不允许用户自己控制播放停止的
            - controls 是否允许用户控制播放
            - autoplay 音频文件是否自动播放
                - 如果设置了autoplay，则音乐在打开页面会自动播放，但不建议使用
            - loop 音频是否循环播放
    -->
    <!-- 第一种方法：使用src指定文件路径
            <audio src="./音视频文件/Wake.mp3" controls autoplay loop></audio>
         第二种方法：使用source指定文件路径，可以指定多个文件，但只会执行一个文件（从上向下）
            <audio controls>
                <source src="./音视频文件/Wake.mp3">
                <source src="./音视频文件/烟花.mp4">
            </audio>
    -->

    <!--
        video标签用来引入一个视频文件（可以是本地或者网上）
        基本属性使用和audio一样
        第一种方法：
            <video src="./音视频文件/烟花.mp4" controls loop></video>
        第二种方法：
            <video controls loop autoplay>
                <source src="./音视频文件/烟花.mp4">
            </video>
    -->
    <!-- 网上的音视频可以直接导入到src中，或者把自己的音视频放到服务器中（价格贵） -->
</body>
</html>
```





# 第二章：CSS基础

## 第一节：CSS基本介绍

> **CSS是层叠样式表**
>
> **网页实际是一个多层结构。通过CSS可以分为层设置样式**
>
> **开发时不要写在body标签里，要写到head标签里**

### 1、CSS的三种编写位置

```html
HTML文件展示

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <!--
        第二种方式：内部样式表
            - 将样式编写到head中的style标签里
            - 通过css的选择器选中元素并为其设置样式
            - 可以对多个标签设置样式，并且修改只需修改一处即可
            - 缺点：
                - 只能对一个网页起作用，不能跨页面使用

        <style>
            p{      对所有body标签里的p标签生效
                color:blue;
                font-size: 30px;
            }
        </style>
    -->

    <!--
        第三种方式：外部样式表（最佳方式）
            - 可以将CSS样式编写到一个外部的CSS文件中
            - 通过link标签引入外部CSS文件
                - rel 表示引入外部文件
                - href 表示外部文件位置，和超链接一样的规则
            - 此方式可以是CSS样式文件得以复用
            - 将样式编写到外部文件中，可以使用到浏览器的缓存机制，加快网页的加载速度
    -->
    <link rel="stylesheet" href="./测试CSS.css">

</head>
<body>

    <!--
        第一种方式：内联样式或者行内样式（不推荐使用）
            - 在标签内部通过style属性设置元素样式
            - 以 : 表示样式值，以 ; 结尾 （px表示像素）
            - 缺点：
                - 这种方法只能对一个标签生效
                - 并且标签多时，维护起来很麻烦

        <p style="color: red; font-size: 30px;">少小离家老大回，乡音未改鬓毛衰。</p>
    -->

    <h1>我是一级标题</h1>
    <p>落霞与孤鹜齐飞，秋水共长天一色。</p>
    <p>剪不断，理还乱，是离愁，别是一般滋味在心头。</p>
    
</body>
</html>
```

```css
CSS文件展示

/* CSS语言的注释 */
h1{		/* 对所有body标签里的p标签生效 */
    color: greenyellow;
    font-size: 60px;
}
p{
    color: blue;
    font-size: 30px;
}

```

### 2、CSS基本语法

> ### 1、选择器
>
> #### 通过选择器可以选中页面中的指定元素，比如p的作用就是选中所有的p元素
>
> ### 2、声明块
>
> #### 通过声明块来指定元素的样式

### 3、文档流

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1">我是BOX1</div>
    <div class="box2">我是BOX2</div>

    <span>我是SPAN1</span>
    <span>我是SPAN2</span>

</body>
</html>
```

```css
/*
    文档流（normal flow）：
        - 网页是一个多层次结构，一层摞着一层
        - 通过CSS可以为每一层设置样式
        - 最底下的一层，成为文档流，文档流是网页的基础
            - 我们所创建的元素都是在文档流中创建的，并且进行排列

        - 对于我们来说，元素有两种状态
            - 在文档流中
                - 块元素
                    - 块元素在文档流中会独占一行
                    - 块元素自上到下垂直排列
                    - 默认宽度是父元素的全部（会把父元素撑满）
                    - 默认高度是被内容撑开（被子元素撑开）
                - 行内元素
                    - 行内元素不会独占一行，只占自身大小
                    - 行内元素自左向右水平排列，和我们的书写习惯一致
                    - 行内元素的宽度和高度都是被内容撑开
            - 不在文档流中（脱离文档流）
*/
.box1{
    width: 100px;
    background-color: red;
}
.box2{
    width: 100px;
    background-color: blue;
}

span{
    background-color: green;
}
```



## 第二节：CSS选择器的使用

### 1、常用选择器

==1、元素选择器==

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <!-- 引入CSS外部文件 -->
    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <h1>秋水共长天色，落霞与孤鹜齐飞</h1>
    <p>少小离家老大回</p>
    <p>乡音无改鬓毛衰</p>
    <p>儿童相见不相识</p>
    <p>笑问客从何处来</p>

</body>
</html>
```

```css
/*
    元素选择器
        作用：根据标签名来选中指定的元素
        语法：标签名{}
        例子：p{}  h1{}  div{}
        缺点：一选全选，会把所有相同标签设置成一个样式
*/
h1{
    color: red;
}
p{
    color: red;
}
```

==2、id选择器==

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <!-- 引入CSS外部文件 -->
    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <h1>秋水共长天色，落霞与孤鹜齐飞</h1>
    <p id="abc">少小离家老大回</p>
    <p id="def">乡音无改鬓毛衰</p>
    <p>儿童相见不相识</p>
    <p>笑问客从何处来</p>

</body>
</html>
```

```css
/*
    id选择器
        作用：根据元素的id属性值选中一个元素
        语法：#id属性值{}
        例子：#abc{}  #def{} （abc和def是我们设置的id值）
*/
#abc{
    color: red;
}
#def{
    color: blue;
}
```

==3、类选择器==

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <!-- 引入CSS外部文件 -->
    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <h1>秋水共长天色，落霞与孤鹜齐飞</h1>
    <!--
        class是一个标签的属性，它和id类似，不同的是class可以重复使用
            - 可以通过class属性来为元素分组
            - 可以同时为一个元素指定多个class属性（空格隔开）
    -->
    <p class="abc">少小离家老大回</p>
    <p class="abc">乡音无改鬓毛衰</p>
    <p>儿童相见不相识</p>
    <p>笑问客从何处来</p>

</body>
</html>
```

```css
/*
    类选择器
    	作用：根据元素的class属性选中一组元素
		语法： .class属性值{}
*/
.abc{
    color: red;
}
```

==4、通配选择器==

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <!-- 引入CSS外部文件 -->
    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <h1>秋水共长天色，落霞与孤鹜齐飞</h1>
    <p>少小离家老大回</p>
    <p>乡音无改鬓毛衰</p>
    <p>儿童相见不相识</p>
    <p>笑问客从何处来</p>

</body>
</html>
```

```css
/*
    通配选择器
        作用：选中页面中的所有元素
        语法：*{}
*/
*{
    color: red;
}
```

### 2、复合选择器

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="CSS测试.css">

</head>
<body>

    <!-- 交集选择器测试实例 -->
    <div class="red">我是div</div>
    <p class="red">我是p标签</p>

    <!-- 并集选择器测试实例 -->
    <h1>我是一级标签</h1>
    <span>我是span标签</span>

</body>
</html>
```

```css
/* 要求：将class为red的内容以红色显示，并且div标签字体大小设置为30px */
/*
    交集选择器
        - 作用：选中同时复合多个条件的元素
        - 语法：选择器1选择器2选择器3选择器n{}
        - 注意点：
            交集选择器中如果有元素选择器，必须使用元素选择器开头
*/
.red{
    color: red;
}
div.red{    /* div为元素选择器，.red为类选择器，两者结合 */
    font-size: 30px;
}


/*
    并集选择器（选择器分组）：
        - 作用：同时选择多个选择器对应的元素
        - 语法：选择器1, 选择器2, 选择器3, 选择器n{}
            - 也可以写成#b1, .p, h1, span, div{} 联合使用
*/
h1, span{
    color: blue;
}
```

### 3、父子兄弟选择器

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <!--
        父元素
            - 直接包含子元素的元素叫做父元素
        子元素
            - 直接被父元素包含的元素叫做子元素
        祖先元素
            - 直接或间接包含后代的元素叫做祖先元素
            - 一个元素的父元素也是它的祖先元素
        后代元素
            - 直接或间接被祖先元素包含的元素叫做后代元素
            - 子元素也是后代元素
        兄弟元素
            - 拥有相同父元素的元素是兄弟元素
    -->

    <div class="one">
        我是一个div
        <p>
            我是div中p标签
            <span>我是div中p标签里面的span标签</span>
        </p>
        <span>我是div中的span标签1</span>
        <span>我是div中的span标签2</span>
        <span>我是div中的span标签3</span>
    </div>

</body>
</html>
```

```css
/*
    要求：为div的子元素span设置字体为红色（div直接包含的span标签内容）
    子元素选择器
        - 作用：选中指定父元素的子元素
        - 语法：父元素 > 子元素

    div.one > span{
        color: red;
    }
*/


/*
    后代元素选择器
        - 作用：选中指定元素内的所有指定后代元素
        - 语法：祖先 后代
    div span{
    color: blue;
    }
*/


/*
    兄弟选择器（只会改变弟的样式，不会改变兄的样式）
        - 选择指定元素紧挨着的下一个兄弟
            - 语法：前一个 + 下一个
       	p + span{       选择p后面紧挨着的那个span标签的内容
            color: green;
        }

        - 选择指定元素后面的所有兄弟
            - 语法：兄 ~ 弟
        p ~ span{       选择p后面全部的span标签的内容
            color: green;
        }
*/
```

### 4、属性选择器

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <p title="abc">少小离家老大回</p>
    <p title="abcdef">乡音未改鬓毛衰</p>
    <p title="def">儿童相见不相识</p>
    <p title="abchello">笑问客从何处来</p>
    <p title="ABC">落霞与孤鹜齐飞</p>
    <p title="ABC">秋水共长天一色</p>

</body>
</html>
```

```css
/*
    属性选择器
        - 语法1：[属性名]     选择含有指定属性的元素
        p[title]{
            color: blueviolet;
        }

        - 语法2：[属性名=属性值]     选择指定属性和属性值的元素
        p[title="ABC"]{
            color: firebrick;
        }

        - 语法3：[属性名^=属性值]    选择属性值以指定值开头的全部元素
        p[title^="abc"]{
            color: blue;
        }

        - 语法4：[属性名$=属性值]    选择属性值以指定值结尾的全部元素
        p[title$="def"]{
            color: lime;
        }

        - 语法5：[属性名*=属性值]    选择属性值中含有指定值的全部元素
        p[title*="abc"]{
        color: brown;
        }
*/

```

### 5、伪类选择器

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <ul>
        <li>第一个</li>
        <li>第二个</li>
        <li>第三个</li>
        <li>第四个</li>
        <li>第五个</li>
    </ul>

</body>
</html>
```

```css
/*
    将ul里的某一个具体位置的li标签设置为红色
    伪类选择器：
        - 作用：用来描述一个元素的特殊状态
            - 比如：第一个元素、被点击的元素、鼠标移入的元素。。。

        - 特点：
            - 伪类一般情况下都是使用 : 开头
                - :first-child   第一个子元素
                ul > li:first-child{        第一个子元素
                    color: red;
                }

                - :last-child    最后一个子元素
                ul > li:last-child{         最后一个子元素
                    color: blue;
                }

                - :nth-child()   选中第n个子元素
                    - n     第n个，n的范围是0到正无穷
                    - 2n    表示选中偶数位的元素
                    - 2n+1（odd）  表示选中奇数位的元素
                ul > li:nth-child(2){       选择第2个子元素
                    color: blue;
                }

            - 以上这些伪类都是根据所有子元素进行排序的

            - 以下和上述用法一样，不同点是它们是在同类型元素中进行查找
                - :first-of-type
                - :last-of-type
                - :nth-of-type()

    :not()  否定伪类：将符合条件的元素从选择器中去除
        ul > li:not(:nth-child(3)){     修改除了第三个li标签的其他全部li标签的样式
            color: red;
        }
*/
```

### 6、超链接的伪类

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <!--
        超链接的状态：
            - 没有访问的状态（蓝色）
            - 访问过链接（紫色）
    -->
    <a href="https://www.baidu.com">访问过的超链接</a>
    <br>
    <a href="https://www.baidu.com">未访问过的超链接</a>
    <br>

</body>
</html>
```

```css
/*
    :link  用料表示没访问过的链接（正常连接）
*/
a:link{
    color: red;
}

/*
    :visited  用来表示访问过的连接
    由于隐私的原因，visited只能修改链接的颜色
*/
a:visited{
    color: blue;
}

/*
    :hover  用来表示鼠标移入的状态
*/
a:hover{
    color: aqua;
    font-size: 30px;
}

/*
    :active  用来表示鼠标点击时的的状态
*/
a:active{
    color: indigo;
}
```

### 7、伪元素

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div>Hello html,Hello World</div>
    <p>开平元年正月丁亥，帝回自长芦，次于魏州。节度使罗绍威以帝回军，虑有不测之患，由是供亿甚至，因密以天人之望切陈之。帝虽拒而不纳，然心德之。壬寅，帝至自长芦。是日，有庆云覆于府署之上。甲辰，天子遣御史大夫薛贻矩来传禅代之意。贻矩谒帝，陈北面之礼，帝揖之升阶。贻矩曰：“殿下功德及人，三灵所卜已定。皇帝方议裁诏，行舜、禹之事，臣安敢违。”既而拜伏于砌下，帝侧躬以避之。 二月戊申，帝之家庙栋间有五色芝生焉，状若芙蓉，紫烟蒙护，数日不散。又，是月，家庙第一室神主上，有五色衣自然而生，识者知梁运之兴矣。唐乾符中，木星入南斗，数夕不退，诸道都统晋国公王铎观之，问诸知星者吉凶安在，咸曰：“金火土犯斗即为灾，唯木当为福耳！”或亦然之。 时有术士边冈者，洞晓天文，博通阴阳历数之妙，穷天下之奇秘，有先见之明，虽京房、管辂不能过也。铎召而质之，冈曰：“惟木为福神，当以帝王占之。</p>

</body>
</html>
```

```css
/*
    伪元素：页面中一些特殊的并不真实存在的元素（特殊位置）
        - 使用： :: 开头
        - 语法：
            - ::first-letter 表示第一个字符
            - ::first-line   表示第一行字符
            - ::selection    表示选中的内容

            - ::before       表示元素的起始位置
            - ::after        表示元素的结尾位置
                - before和after必须结合content属性来使用
                - 用来添加一些内容，并且无法选中
*/
p::first-letter{
    font-size: 30px;
}

p::first-line{
    color: red;
}

p::selection{
    background-color: green;
}

div::before{
    content: "abc";
    color: red;
}

div::after{
    content: "def";
    color: blue;
}
```

### 8、继承的样式

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <p>
        我是一个p元素<br>
        <span>
            我是p元素类里面的span元素<br>
            <em>
                我是span里面的em元素<br>
            </em>
        </span>
    </p>
    <br>
    <div>
        我是一个div
        <span>我是div里面的span元素</span>
    </div>

</body>
</html>
```

```css
/*
    样式的继承
        - 含义：为一个元素设置的样式，同时也会应用到它的后代上
        - 作用范围：发生在祖先和所有后代之间
        - 作用：利用继承可以将一些样式统一设置到共同的祖先元素上，这样只需设置一次即可让所有元素都具有该样式
        - 注意：并不是所有的样式都会被继承
            - 比如：和背景相关的，布局相关的都不会被继承
*/
body{
    font-size: 30px;
}
p{
    color: red;
    background-color: yellow;
}
div{
    color: blue;
}
```

### 9、选择器的权重

|     选择器     |  优先级值  |
| :------------: | :--------: |
|   内联选择器   | 1，0，0，0 |
|    id选择器    | 0，1，0，0 |
| 类和伪类选择器 | 0，0，1，0 |
|   元素选择器   | 0，0，0，1 |
|   通配选择器   | 0，0，0，0 |
|   继承的样式   | 没有优先级 |

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <p id="red" class="blue" style="color: deepskyblue">选择器的权重问题。</p>

</body>
</html>
```

```css
/*
    - 问题：样式冲突（不同选择器选中了相同元素，设置不同的样式）
    - 解决方式：发生冲突时，具体哪个样式由选择器的权重（优先级）决定
    - 比较选择器时，将选择器的优先级相加计算，优先级值越高，则越优先显示（分组选择器是单独计算的）
        - 选择器累加不会超过其最大的数量级，类选择器再高也不会超过id选择器
        - 若优先级相同，则优先使用代码在最后的那个样式
    - 可以在某一个样式最后添加 !important; ，此时该样式获取到最高优先级，甚至超过内联选择器（不到万不得已不要用）
    - 简述：描述越详细具体，优先级越高
*/
p{      /* 元素选择器 */
    color: green;
}
#red{   /* id选择器 */
    color: red;
}
.blue{  /* 类选择器 */
    color: blue;
}
```



## 第三节：单位

### 1、像素和百分比

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1">
        <div class="box2"></div>
    </div>

</body>
</html>
```

```css
/*
    - 长度单位
        - 像素：
            - 屏幕（显示器）实际上是由一个个小点点构成
            - 不同屏幕的像素大小是不同的，像素越小的屏幕显示越清晰
        - 百分比：
            - 可以将属性值设置为相对父元素的属性的百分比
            - 可以是子元素跟随父元素的改变而改变
*/
.box1{
    width: 200px;       /* 宽度 */
    height: 300px;      /* 高度 */
    background-color: blue;
}

.box2{
    width: 50%;
    height: 50%;
    background-color: red;
}
```

### 2、em和rem

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1"></div>
    <div class="box2"></div>

</body>
</html>
```

```css
/*
    - em
        - em是相对于元素（自身的）的字体大小来计算的
        - 1em = 1font-size
        - em会根据字体大小的改变而改变
    - rem
        - rem是相对于根元素（html的）的字体大小来计算的
*/
.box1{
    width: 20em;
    height: 10em;
    background-color: blue;
}

.box2{
    width: 20rem;
    height: 10rem;
    background-color: red;
}
```

### 3、RGB值

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1"></div>
    <div class="box2"></div>
    <div class="box3"></div>

</body>
</html>
```

```css
/*
    颜色单位
        - 在CSS中可以直接使用颜色名来设置各种颜色
        - RGB值：直接使用数值来设置颜色
            - RGB通过三种颜色不同浓度来调配出不同的颜色
            - R：red   G：greed    B：blue
            - 每一种颜色的范围在0~255（0~100%）之间
            - 语法：RGB(红色,绿色,蓝色)
        - RGBA值：A表示不透明度
            - 在RGB的基础上增加了一个A的值
            - 用法：
                - 1表示完全不透明
                - 0表示完全透明
                - .5表示半透明
        - 十六进制的RGB值
            - 语法：#红色绿色蓝色
            - 颜色浓度通过 00-ff 表示
            - 如果颜色两位两位重复可以简写（#aabbcc --> #abc）
*/
.box1{
    width: 100px;
    height: 100px;
    background-color: rgb(120, 9, 23);
}
.box2{
    width: 100px;
    height: 100px;
    background-color: rgba(120, 9, 23, .5);
}
.box3{
    width: 100px;
    height: 100px;
    background-color: #0F7812;
}
```

### 4、HSL值

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1"></div>
    <div class="box2"></div>

</body>
</html>
```

```css
/*
    HSL值
        - H：色相（0~360）
        - S：饱和度，颜色的浓度（0~100%）
        - L：亮度，颜色的亮度（0~100%）
    HSLA值
        - HSL和上述一样
        - A:不透明度（0~100%）
*/
.box1{
    width: 100px;
    height: 100px;
    background-color: hsl(300, 60%, 70%);
}
.box2{
    width: 100px;
    height: 100px;
    background-color: hsla(300, 60%, 70%, .5);
}
```





# 第三章：盒子模型

## 第一节：盒子模型介绍

### 1、盒子模型简介

> ###         盒模型、盒子模型，框模型（box model）
>
> - CSS将页面中的所有元素都设置为一个个矩形的盒子
> - 将元素设置为矩形的盒子后，对页面的布局就变成了将不同的盒子摆放在不同的位置
> - 盒子的组成
>   - 内容区（content）
>   - 边框（border）
>   - 内边距（padding）
>   - 外边距（margin）
>   - 外边距（margin）

### 2、内容区

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box">我是一个div标签</div>

</body>
</html>
```

```css
/*
    - 内容区：网页中的所有文字和子元素都在内容区中排列
        - 内容区的大小由width（宽度）和height（高度）来决定
*/
.box{
    width: 200px;
    height: 200px;
    background-color: aqua;
}
```

### 3、边框

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1"></div>
    <div class="box2"></div>
    <div class="box3"></div>
    <div class="box4"></div>

</body>
</html>
```

```css
/*
    - 内容区：网页中的所有文字和子元素都在内容区中排列
        - 内容区的大小由width（宽度）和height（高度）来决定

    - 边框：边框属于盒子的边缘，出了边框都是盒子外面，边框里面都是盒子内部
        - 边框的大小会影响到盒子的大小
        - 设置边框要设置三个样式：
            - 边框宽度：border-width
                - 默认值是两到三个像素
                - border-width可以指定四个方向的宽度
                    - 四个值：上 右 下 左
                    - 三个值：上 右左 下
                    - 两个值： 上下 右左
                    - 一个值：上下左右
                - 可以直接指定四个方向的宽度
                    - border-top-width：上边宽度
                    - border-right-width：右边宽度
                    - border-bottom-width：下边宽度
                    - border-left-width：左边宽度
            - 边框的颜色：border-color
                - 默认值是黑色
                - 用来指定边框的颜色，同时和宽度一样，可以指定四个边的颜色，用法一样
            - 边框的样式：border-style
                - 默认值是none，没有边框
                - 指定边框的样式
                    - solid  实线
                    - dotted  点状虚线
                    - dashed  虚线
                    - double  双线
                - 和宽度一样，也存在四个方向，用法一样

    - border简写三个基础属性值，通过该属性一起设置相关变量，没有顺序要求
    - 可以通过border-top，border-right，border-bottom，border-left一起设置各个边的属性
*/
.box1{      /* 边框基本展示 */
    /* 内容区 */
    width: 200px;
    height: 200px;
    background-color: red;

    /* 边框 */
    border-width: 10px 15px 20px 25px;
    border-color: blue;
    border-style: solid;
}
.box2{      /* 边框宽度展示 */
    /* 内容区 */
    width: 200px;
    height: 200px;
    background-color: yellow;

    /* 边框 */
    border-top-width: 10px;
    border-right-width: 15px;
    border-bottom-width: 20px;
    border-left-width: 25px;
    border-color: green;
    border-style: solid;
}
.box3{      /* 边框样式展示 */
    /* 内容区 */
    width: 200px;
    height: 200px;
    background-color: blue;

    /* 边框 */
    border-width: 10px;
    border-color: aquamarine;
    border-style: solid dotted dashed double;
}
.box4{      /* 简写border边框语法展示 */
    /* 内容区 */
    width: 200px;
    height: 200px;
    background-color: blue;

    /* 边框 */
    border: 10px red solid;
}
```

### 4、内边距

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box">
        <div class="inner">内容区</div>
    </div>

</body>
</html>
```

```css
/*
    内边距
        - 内容区和边框之间的举例是内边距
        - 一共有四个方向
            - padding-top
            - padding-right
            - padding-bottom
            - padding-left
        - 内边距的设置会影响盒子的大小
        - 背景颜色会延申到内边距上
        - 一个盒子的可见大小是由内容区，边框和内边距共同决定的，计算大小时，三个部分全部相加
        - padding也可以直接简写，规则和边框一样
*/
.box{
    /* 内容区和边框 */
    width: 200px;
    height: 200px;
    background-color: blue;
    border: 10px red solid;

    /* 内边距 */
    padding-top: 50px;
}
.inner{
    width: 100%;
    height: 100%;
    background-color: yellow;
}
```

### 5、外边距

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1"></div>
    <div class="box2"></div>

</body>
</html>
```

```css
/*
    外边距
        - 和其他元素的距离
        - 外边距不会影响盒子的可见框大小，但是外边距会影响盒子的位置
        - 一共有四个方向的外边距
            - margin-top：上外边距，设置正值，元素向下移动
            - margin-right：默认情况下，设置此元素不会产生任何效果
            - margin-bottom：下外边距，设置正值，其下边的元素会向下移动
            - margin-left：左外边距，设置正值，元素向右移
            - margin也可以设置负值，代表元素向相反的方向走
        - 元素在页面中是按自左向右顺序排列的
            - 默认设置左和上边距会移动自已
            - 设置右和下会移动其他元素
        - margin简写属性
            - 可以同时设置四个方向的外边距，用法和前面的一样
            - 语法：margin:100px 表示四个方向的外边距都是100px
*/
.box1{
    /* 内容区和边框 */
    width: 200px;
    height: 200px;
    background-color: red;
    border: 10px blue solid;
    /* 外边距 */
    margin-top: 100px;
    margin-bottom: 100px;
    /* margin-bottom: -100px; */
    margin-left: 100px;
}
.box2{      /* 验证下外边距是否起作用 */
    /* 内容区 */
    width: 220px;
    height: 220px;
    background-color: green;
    /* 外边距 */
    margin-left: 100px;

}
```

### 6、外边距的折叠

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>
    <!-- 兄弟元素之间的展示 -->
    <div class="box1">1</div>
    <div class="box2">2</div>
    <br><br>

    <!-- 父子元素之间的展示 -->
    <div class="box3">
        <div class="box4"></div>
    </div>

</body>
</html>
```

```css
/*
    垂直外边距的重叠（折叠）
        - 相邻的垂直方向的外边距会发生重叠现象

        - 兄弟元素之间：
            - 兄弟元素之间的垂直外边距会取两者中较大值
            - 相邻元素一正一负，则取两者的和
            - 相邻元素都是负值，则取绝对值较大的

        - 父子元素之间：
            - 父子元素间的相邻外边距，子元素会传递给父元素（上外边距）
            - 父子外边距会影响页面的布局，必须要进行处理

*/
/* 兄弟元素之间的展示 */
.box1, .box2{
    width: 200px;
    height: 200px;
    font-size: 50px;
}
.box1{
    background-color: red;
    /* 设置一个下外边距 */
    margin-bottom: 100px;
}
.box2{
    background-color: blue;
    /* 设置一个上外边距 */
    margin-top: 100px;
}

/* 父子元素之间的展示*/
.box3{
    width: 200px;
    height: 200px;
    background-color: green;
}
.box4{
    width: 100px;
    height: 100px;
    background-color: yellow;
    margin-top: 100px;
}
```

### 7、行内元素的盒子模型

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <span class="s1">我是一个span元素</span>
    <div class="box1"></div>
    <a href="javascript:;">无效超链接</a>

</body>
</html>
```

```css
/*
    - 行内元素的盒子模型
        - 行内元素不支持设置宽度和高度
        - 行内元素可以设置padding，但是垂直方向的padding不会影响页面的布局
        - 行内元素可以设置border，但是垂直方向的border不会影响页面的布局
        - 行内元素可以设置margin，但是垂直方向的margin不会影响页面的布局

    - display 用来设置元素显示的类型
        - inline：将元素设置为行内元素
        - block：将元素设置为块元素
        - inline-block:将元素设置为行内块元素（行内块：既可以设置宽度和高度，又不会独占一行）（不推荐使用）
        - table：将元素设置为一个表格
        - none：元素不在页面中显示，隐藏元素，不会占据元素位置

    - visibility 用来设置元素显示的状态
        - visible：默认值，元素在页面中正常显示
        - hidden：元素在页面中隐藏，不显示，但依然会占据元素位置
*/
/* 行内盒子模型 */
.s1{
    background-color: green;
    /* padding: 100px; */
    /* border: 100px blue solid; */
    margin: 100px;
}
.box1{
    width: 200px;
    height: 200px;
    background-color: yellow;
}

/* display 和 visibility 用法展示 */
a{
    /* display: inline; */
    /* display: block; */
    /* display: inline-block */
    /* display: table */
    /* display: none */

    /* visibility: visible */
    /* visibility: hidden */
    width: 100px;
    height: 20px;
    background-color: aqua;
}

```

### 8、浏览器的默认布局

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box"></div>

    <p>我是第一个段落</p>
    <p>我是第二个段落</p>
    <p>我是第三个段落</p>

    <ul>
        <li>列表项1</li>
        <li>列表项2</li>
        <li>列表项3</li>
    </ul>

</body>
</html>
```

```css
/*
    - 默认样式：通常情况下，浏览器会为元素设置一些默认样式，默认样式会影响到页面布局，必须重新设置样式

    - 重置样式表：专门用来对浏览器的样式进行重置
        - reset.css 直接去除浏览器的全部默认样式
        - normalize.css 对默认样式进行统一，使页面在不同浏览器中展示的内容相同
*/
/* 去除div的边距 */
.box{
    width: 200px;
    height: 200px;
    border: 5px blue solid;
}
body{
    margin: 0;
}

/* 去除p的边距 */
p{
    margin: 0;
}

/* 去除ul里面li的边距 */
ul{
    margin: 0;
    list-style: none;       /* 去除项目符号 */
    padding: 0;
}

/* 最简单的去除样式的方法 */
*{
    margin: 0;
    padding: 0;
}
```





## 第二节：盒子模型的布局样式

### 1、水平方向的布局

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="outer">
        <div class="inner"></div>
    </div>

    <div class="x">
        <div class="y"></div>
    </div>

</body>
</html>
```

```css
/*
    水平方向的布局：
        - 元素在其水平方向上的位置由以下几个属性共同决定
            - margin-left
            - border-left
            - padding-left
            - width
            - padding-right
            - border-right
            - margin-right
            
        - 一个元素在其父元素中，必须满足以下等式
            (margin-left)+(border-left)+(padding-left)+(width)+(padding-right)+(border-right)+(margin-right)
            = 其父元素内容区的宽度（必须满足，在实例中等于800px）
            - 以上等式必须满足，如果相加结果使等式不成立，称为过度约束，则等式会自动调整
                - 如果这七个值中没有auto的情况，则浏览器会自动调整margin-right的值使等式成立
                - 这七个值中有三个可以设置为auto，分别是：width，margin-left，margin-right
                    - 如果某个值被设置为auto，浏览器则会自动调整那个auto的值使等式成立
                - 如果将一个宽度和一个外边距设置为auto，则宽度会调整到最大，设置为auto的外边距会自动为0
                - 如果将三个值都设置为auto，则外边距都是0，宽度最大
                - 如果将两个外边距设置为auto，宽度为固定值，则会将外边距设置为相同的值
                    - 利用这个特点设置元素在父元素的位置为水平居中
                        - width:某个像素大小;
                        - margin:0 auto;
*/
/* 未设置为auto的情况展示 */
.outer{
    width: 800px;
    height: 200px;
    border: 10px red solid;
}
.inner{
    width: 200px;
    height: 200px;
    background-color: yellow;
}

/* 设置为auto的情况展示 */
.x{
    width: 800px;
    height: 200px;
    border: 10px blue solid;
}
.y{
    width: auto;
    height: 200px;
    background-color: indigo;
}
```

### 2、垂直方向的布局

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="outer">
        <div class="inner"></div>
    </div>

</body>
</html>
```

```css
/*
    - 默认情况下，父元素的高度被撑开

    - 子元素使在父元素的内容区排列的
        - 如果子元素超过父元素，则会从父元素中溢出
        - 使用overflow属性来设置父元素进行溢出处理
        - 可选值：
            - visible：默认值，子元素会从父元素中溢出，在父元素外进行显示
            - hidden：溢出部分会被裁剪，不会显示出来
            - scroll：生成两个滚动条，通过滚动条查看内容
            - auto：根据需要生成滚动条
            - x：处理水平方向
            - y：处理垂直方向
*/
.outer{
    width: 200px;
    height: 200px;
    background-color: red;
    /* 父元素处理溢出 */
    /* overflow: visible; */
    /* overflow: hidden; */
    /* overflow:scroll; */
    /* overflow: auto; */
    /* overflow: x; */
    /* overflow: y; */
}
.inner{
    width: 100px;
    height: 400px;
    background-color: blue;
}
```

## 第三节：盒子的其他知识

### 1、盒子的大小

> - 默认情况下，盒子的可见大小由内容区，内边框和边框的大小共同决定
> - box-sizing 用来设置盒子尺寸的计算方式（设置width和height的作用）
>   - content-box：默认值，宽度和高度用来设置内容区的大小
>   - border-box：宽度和高度用来设置整个盒子的可见大小，width和height指的是内容区，内边框和边框的总大小

### 2、轮廓阴影和圆角

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <!-- 轮廓展示 -->
    <div class="box1"></div>
    <span>Hello!</span>
    <br><br>

    <!-- 阴影展示 -->
    <div class="box2"></div>
    <br><br>

    <!-- 圆角展示 -->
    <div class="box3"></div>

</body>
</html>
```

```css
/*
    - outline：用来设置轮廓线，用法的border一样
    - outline（轮廓）和border（边框）的不同点：轮廓不会影响可见框的大小
        - 一般用在鼠标移入时做过渡动画效果

    - box-shadow：用来设置元素的阴影效果，阴影不会影响页面的布局
        - 第一个值：水平偏移量，正值向右，负值向左
        - 第二个值：垂直偏移量，正值向下，负值向上
        - 第三个值：阴影的模糊半径
        - 第四个值：阴影颜色

    - border-radius：用来设置圆角，圆角设置圆的半径大小
        - 四个值：左上 右上 右下 左下
        - 三个值：左上 右上/左下（对角） 右下
        - 两个值：左上/右下（对角） 右上/左下（对角）
        - 也可以设置成百分比
        - 在指定某个方向时，可以设置成两个值，表示两个半径展现出来的圆角
*/

/* 轮廓展示 */
.box1{
    width: 100px;
    height: 100px;
    background-color: #c81623;
}
.box1:hover{
    outline: 10px black solid;
}

/* 阴影展示 */
.box2{
    width: 100px;
    height: 100px;
    background-color: #c81623;

    box-shadow: 10px 10px 10px rgba(0, 0, 0, .5);
}

/* 圆角展示 */
.box3{
    width: 100px;
    height: 100px;
    background-color: #c81623;

    border-radius: 10px 15px 20px 25px;    /* 设置全部位置圆角 */
    /* border-top-left-radius: 10px;        设置上左圆角 */
    /* border-top-right-radius: 10px;       设置上右圆角 */
    /* border-bottom-left-radius: 10px;     设置下左圆角 */
    /* border-bottom-right-radius: 10px;    设置下右圆角 */
}
```

## 第四节：浮动

### 1、浮动的介绍

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1"></div>
    <div class="box2"></div>
    <div class="box3"></div>

</body>
</html>
```

```css
/*
    - 通过设置浮动可以使一个元素向其父元素的左侧或者右侧移动

    - 使用float属性来设置元素的浮动
        - none：元素不浮动
        - left：元素向左浮动
        - right：元素向右移动

    - 注意：
        - 元素设置浮动后，水平布局的等式便不需要强制成立
        - 元素设置浮动以后，会完全从文档流中脱离，不会占用文档流的位置，所以该元素下边的元素会自动上移

    - 浮动元素的特点：
        - 浮动元素会完全脱离文档流，不再占据文档流的位置
        - 设置浮动以后，元素会向父元素的左侧（left）或右侧（right）移动
        - 浮动元素默认不会从父元素中移出
        - 浮动元素向左或右移动时，不会超出它前边的其他元素浮动元素（浮动元素间不会遮盖）
        - 如果浮动元素的上边是一个没有浮动的块元素，则浮动元素无法上移
        - 浮动元素不会超过它上边的浮动兄弟元素，最多就是和它一样高

    - 总结：
        - 浮动的主要目的是让元素可以水平排列
        - 通过浮动可以制作一些水平方向的布局
*/
.box1{
    width: 200px;
    height: 200px;
    background-color: red;

    float: left;    /* 设置浮动后那个等式便不需要成立，块元素也可以不独占一行 */
}

.box2{
    width: 200px;
    height: 200px;
    background-color: blue;
    float: left;    /* 设置元素浮动 */
}

.box3{
    width: 200px;
    height: 200px;
    background-color: yellow;
    float: left;    /* 设置元素浮动 */
}
```

### 2、浮动的特点补充

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <!-- 文字环绕图片展示 -->
    <div class="box1"></div>
    <p>中华人民共和国（the People's Republic of China），简称“中国”，成立于1949年10月1日 [1]  ，位于亚洲东部，太平洋西岸 [2]  ，是工人阶级领导的、以工农联盟为基础的人民民主专政的社会主义国家 [3]  ，以五星红旗为国旗 [4]  、《义勇军进行曲》为国歌 [5]  ，国徽内容为国旗、天安门、齿轮和麦稻穗 [6]  ，通用语言文字是普通话和规范汉字 [7]  ，首都北京 [8]  ，是一个以汉族为主体、56个民族共同组成的统一的多民族国家。
        中国陆地面积约960万平方千米，东部和南部大陆海岸线1.8万多千米，内海和边海的水域面积约470多万平方千米。海域分布有大小岛屿7600多个，其中台湾岛最大，面积35798平方千米 [2]  。中国同14国接壤，与8国海上相邻。省级行政区划为23个省、5个自治区、4个直辖市、2个特别行政区。 [2]
        中国是世界上历史最悠久的国家之一，有着光辉灿烂的文化和光荣的革命传统 [3]  ，世界遗产数量全球领先 [9]  。1949年新中国成立后，进入社会主义革命和建设时期，1956年实现向社会主义过渡，此后社会主义建设在探索中曲折发展 [10]  。“文化大革命”结束后实行改革开放，沿着中国特色社会主义道路，集中力量进行社会主义现代化建设 [3]  。经过长期努力，中国特色社会主义进入了新时代。 [11]
        中国是世界上人口最多的发展中国家，国土面积居世界第三位，是世界第二大经济体，并持续成为世界经济增长最大的贡献者，2020年经济总量突破100万亿元 [12-13]  [128]  。中国坚持独立自主的和平外交政策，是联合国安全理事会常任理事国，也是许多国际组织的重要成员，被认为是潜在超级大国之一。 [14]
    </p>
    <br><br>

    <!-- 文字浮动效果展示 -->
    <!-- 块元素展示 -->
    <div class="box2">Hello</div>
    <div class="box3">Hello</div>
    <br><br>
    <!-- 行内元素展示 -->
    <span>我是一个span标签</span>

</body>
</html>
```

```css
/*
    - 浮动元素不会盖住文字，文字会自动环绕在浮动元素的周围，所以可以利用这点设置文字环绕图片效果

    - 元素设置浮动以后，将会从文档流中脱离，元素的一些特点也会发生改变

    - 脱离文档流的特点：
        - 块元素：
            - 块元素不在独占一行
            - 脱离文档流之后，块元素的宽度和高度默认都被内容撑开
        - 行内元素：
            - 行内元素脱离文档流之后就会变成块元素，特点和块元素一样
        - 总结：脱离文档流之后，就不区分块元素和行内元素了
*/
*{      /* 清除默认样式 */
    margin: 0;
    padding: 0;
}

/* 文字环绕图片展示 */
.box1{
    width: 100px;
    height: 100px;
    background-color: red;

    float: left;
}

/* 文字浮动效果展示 */
.box2{      /* 块元素展示 */
    background-color: #bbffaa;
    float: left;
}
.box3{
    background-color: #c81623;
}

span{       /* 行内元素展示 */
    /*
        行内元素本来不支持设置宽度和高度，但是设置浮动后，便可以设置宽度和高度了，和块元素一样了
    */
    float: left;
    width: 100px;
    height: 100px;
    background-color: #3aff50;
}
```

### 3、简单的布局练习

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <!-- 创建头部 -->
    <header></header>

    <!-- 创建网页主体 -->
    <main>
        <!-- 设置左侧导航栏 -->
        <div class="left"></div>

        <!-- 设置中间主体文字 -->
        <div class="word"></div>

        <!-- 设置右边导航栏 -->
        <div class="right"></div>
    </main>

    <!-- 创建网页底部 -->
    <footer></footer>

</body>
</html>
```

```css
/* 设置三部分的共同样式 */
header, main, footer{
    width: 1000px;
    margin: 0 auto;         /* 使位置居中排列 */
}

/* 设置头部样式 */
header{
    height: 100px;
    background-color: yellow;
}

/* 设置主体样式 */
main{
    height: 300px;
    background-color: #ffffc4;
    margin: 10px auto;      /* 设置三个部分间的空隙 */
}

/* 设置底部样式 */
footer{
    height: 100px;
    background-color: green;
}

/* 设置左侧导航栏样式 */
.left{
    float: left;        /* 设置浮动样式 */
    width: 180px;       /* 使其左右留有间隙 */
    height: 94%;        /* 和其父元素保持相同 */
    margin: 9px 10px;   /* 设置垂直居中 */
    background-color: #cacaca;
}

/* 设置中间文字样式 */
.word{
    float: left;        /* 设置浮动样式 */
    width: 580px;       /* 使其左右留有间隙 */
    height: 94%;        /* 和其父元素保持相同 */
    margin: 9px 10px;   /* 设置垂直居中 */
    background-color: #25a4bb;
}

/* 设置右侧导航栏样式 */
.right{
    float: left;        /* 设置浮动样式 */
    width: 180px;       /* 使其左右留有间隙 */
    height: 94%;        /* 和其父元素保持相同 */
    margin: 9px 10px;   /* 设置垂直居中 */
    background-color: #898888;
}
```

## 第五节：高度塌陷（浮动的拓展）

### 1、高度塌陷和BFC

```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="../清除默认样式/reset.css">
    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="outer">
        <div class="inner"></div>
    </div>

    <div class="box"></div>

</body>
</html>
```

```css
/*
    - 高度塌陷问题：
        - 在浮动布局中，父元素的默认高度是被子元素撑开的
        - 当子元素浮动后，会完全脱离文档流，将无法撑开父元素的高度，导致父元素高度丢失
        - 父元素丢失以后，其下的元素会自动上移，导致页面的布局混乱，所以必须进行处理

    - BFC（Block Formatting Context）：块级格式化环境
        - BFC是一个CSS中的一个隐含属性，可以为一个元素开启BFC，此元素就变成一个独立的布局区域
        - 元素开启BFC后的特点：
            - 开启BFC的元素不会被浮动元素所覆盖
            - 开启BFC的元素子元素和父元素外边距不会重叠
            - 开启BFC的元素可以包含浮动的子元素
        - 通过一些方式开启BFC：
            - 设置元素的浮动（不推荐，副作用大）
            - 将元素设置为行内块元素（不推荐，副作用大）
            - 将元素的overflow设置为一个非visible的值
                - 常用overflow:hidden开启BFC，使其可以包含浮动元素
		- BFC不能直接去开启，都是通过某些属性间接去开启
*/

.outer{
    border: 10px red solid;
    /* float: left;                 设置元素的浮动开启BFC */
    /* display: inline-block;       将元素设置为行内块元素开启BFC */
    overflow: hidden;
}

.inner{
    width: 100px;
    height: 100px;
    background-color: green;
    /*float: left;*/
}

.box{
    width: 100px;
    height: 100px;
    background-color: yellow;
}
```

### 2、BFC的演示

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1">
        <div class="box3"></div>
    </div>

    <!-- <div class="box2"></div> -->

</body>
</html>
```

```css
.box1{
    width: 100px;
    height: 100px;
    background-color: red;
    /* 通过下面的float和overflow两种方式都可以为box3开启BFC */
    float: left;
    overflow: hidden;
}

.box2{
    width: 100px;
    height: 100px;
    background-color: blue;

    /* 此时box2被box1盖住，要为box2开启BFC */
    overflow: hidden;
}

.box3{
    width: 50px;
    height: 50px;
    background-color: yellow;
    margin-top: 50px;
}
```

### 3、clear的演示

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1">1</div>
    <div class="box2">2</div>
    <div class="box3">3</div>

</body>
</html>
```

```css
div{        /* 设置字体大小，方便对元素进行标识 */
    font-size: 30px;
}

.box1{
    width: 100px;
    height: 100px;
    background-color: #25a4bb;
    float: left;
}

.box3{
    width: 100px;
    height: 100px;
    background-color: #0F7812;

/*
    - 由于box1的浮动，导致box3位置的上移，使其位置发生了改变

    - 可以通过clear属性来清除浮动元素对当前元素的影响
        - 可选值
            - left：清除左侧浮动元素对当前元素的影响
            - right：清除右侧浮动元素对当前元素的影响
            - both：清除两侧中影响最大的一侧

        - 原理：设置清除浮动以后，浏览器会自动为元素设置一个上外边距，使其位置不受其他元素的影响
*/
    /* clear: left;         清除左侧浮动元素的影响，指1 */
    /* clear: right;        清除右侧浮动元素的影响，指2 */
    /* clear: both;         由于2的影响比1大，所以清除2对其的影响 */
}


.box2{
    width: 200px;
    height: 200px;
    background-color: #c81623;
    float: right;
}
```

### 4、after伪类解决高度塌陷

```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1">
        <div class="box2"></div>
    </div>

</body>
</html>
```

```css
.box1{
    border: 10px red solid;
}

.box2{
    width: 100px;
    height: 100px;
    background-color: orange;
    float: left;

}

/* 通过after解决高度塌陷问题 */
.box1::after{
    content: '';        /* 填入空内容 */
    display: block;     /* 使行内元素转换成块元素 */
    clear: both;        /* 清除浮动元素带来的影响 */
}
.box1{
    border: 10px red solid;
}

.box2{
    width: 100px;
    height: 100px;
    background-color: orange;
    float: left;

}

/* 通过after解决高度塌陷问题 */
.box1::after{
    content: '';        /* 填入空内容 */
    display: block;     /* 使行内元素转换成块元素 */
    clear: both;        /* 清除浮动元素带来的影响 */
}
```

### 5、clearfix类：解决高度塌陷和重叠问题（最推荐）

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1 clearfix">
        <div class="box2"></div>
    </div>

</body>
</html>
```

```css
.box1{
    width: 200px;
    height: 200px;
    background-color: #0F7812;
}

.box2{
    width: 100px;
    height: 100px;
    background-color: #c81623;
    margin-top: 100px;
}

/*
    这个样式可以同时解决 高度塌陷和重叠的问题，clearfix使自定义的类属性值
*/
.clearfix::before,
.clearfix::after{
    content: '';
    display: table;
    clear: both;
}
```





# 第四章：进阶基础知识

## 第一节：定位

### 定位简述

> -  定位是一种更加高级的布局方式
> - 通过定位可以将元素摆放到页面的任意位置
> - 使用position属性来设置定位
>   - static：默认值，元素是静止的，没有开启定位
>   - relative：开启元素的相对定位
>   - absolute：开启元素的绝对定位
>   - fixed：开启元素的固定定位
>   - sticky：开启元素的粘滞定位

### 1、相对定位

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1">1</div>
    <div class="box2">2</div>
    <div class="box3">3</div>

</body>
</html>
```

```css
/*
    - 相对定位：可视位置发生改变，但原本的位置不会发生变化，还在原地占据着
        - 当元素的position属性设置为relative时，就开启了该元素的相对定位
        - 相对定位特点：
            - 元素设置相对定位后，如果不设置偏移量，元素不会发生任何变化
            - 相对定位是参照原元素（左上角的点为坐标原点）在文档流中的位置进行定位的
            - 相对定位会提升元素的层级
            - 相对定位不会使元素脱离文档流，也不会元素的性质（块还是块元素，行内还是行内元素）

    - 偏移量（offset）
        - 元素设置相对定位以后，通过偏移量来设置元素的位置（对其他元素不产生任何影响）
        - 垂直方向的定位：top和bottom一般只设置一个
            - top：定位元素和定位位置上边的距离
            - bottom：定位元素和定位位置下边的距离
        - 水平方向的定位：left和right一般也只设置一个
            - left：定位元素和定位位置左边的距离
            - right：定位元素和定位位置右边的距离
*/

div{        /* 设置字体的大小 */
    font-size: 50px;
}

.box1{
    width: 200px;
    height: 200px;
    background-color: #c81623;
}

.box2{      /* 为该元素设置相对定位 */
    width: 200px;
    height: 200px;
    background-color: #0F7812;

    /* 设置position属性 */
    position: relative;         /* 开启该元素的相对定位 */
    /* 设置偏移量 */
    top: 100px;         /* 元素向下移动 */
    bottom: 100px;      /* 元素向上移动 */
    left: 100px;        /* 元素向右移动 */
    right: 100px;       /* 元素向左移动 */
}

.box3{
    width: 200px;
    height: 200px;
    background-color: #3d32bb;
}
```

### 2、绝对定位

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1">1</div>
    <div class="box5">      <!-- 测试用的祖先元素 -->
        5
        <div class="box4">      <!-- 测试用的祖先元素 -->
            4
            <div class="box2">2</div>   <!-- 为该元素设置绝对定位 -->
        </div>
    </div>

    <div class="box3">3</div>

</body>
</html>
```

```css
/*
    - 绝对定位
        - 当元素的position的属性值设置为absolute时，则开启了该元素的绝对定位
        - 绝对定位的特点：
            - 开启绝对定位后，如果不设置偏移量，该元素不会发生变化
            - 开启绝对定位后，元素从文档流中脱离
            - 绝对定位会改变元素的性质，行内变成块，块的宽高被内容撑开
            - 绝对定位会会使元素提升一个层级
            - 绝对定位元素使相对于其包含块进行定位的

    - 包含块（containing block）
        - 正常情况下：包含块的就是离当前元素最近的祖先块元素
        - 开启绝对定位的包含块：
            - 包含块就是离它最近的开启了定位的祖先元素
            - 如果所有的祖先元素都没有开启定位，则根元素就是它的包含块
            - html：根元素、初始包含块

    - 偏移量和相对定位的一样，也是top、bottom、left和right
*/

div{        /* 设置字体的大小 */
    font-size: 50px;
}

.box1{
    width: 200px;
    height: 200px;
    background-color: #c81623;
}

.box2{      /* 为该元素设置绝对定位 */
    width: 200px;
    height: 200px;
    background-color: #0F7812;

    /* 为该元素设置绝对定位 */
    position: absolute;
}

.box3{
    width: 300px;
    height: 300px;
    background-color: #3d32bb;
}

/* 设置测试用的box4和box5元素的样式 */
.box4{
    width: 300px;
    height: 300px;
    background-color: coral;
    /* position: relative;     为其开启相对定位 */
}
.box5{
    width: 400px;
    height: 400px;
    background-color: indigo;
    /* position: relative;     为其开启相对定位 */
}
```

### 3、固定定位

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1">1</div>
    <div class="box2">2</div>
    <div class="box3">3</div>

</body>
</html>
```

````css
/*
    - 固定定位
        - 当元素的position的属性值设置为fixed时，则开启了该元素的固定定位
        - 固定定位也是一种相对定位，大部分特点和相对定位一样
        - 固定定位的特点：
            - 固定定位永远参考于浏览器的视口进行定位
            - 固定定位的元素不会随着滚动体的滚动而滚动（类似广告、弹窗）
*/

div{        /* 设置字体的大小 */
    font-size: 50px;
}

.box1{
    width: 200px;
    height: 200px;
    background-color: #c81623;
}

.box2{      /* 为该元素设置固定定位 */
    width: 200px;
    height: 200px;
    background-color: #0F7812;

    /* 为该元素设置固定定位 */
    position: absolute;
}

.box3{
    width: 300px;
    height: 300px;
    background-color: #3d32bb;
}
````

### 4、粘滞定位(某些浏览器不支持，不推荐使用)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="item">
        <div>
            <a class="HC" target="_blank" href="https://www.w3school.com.cn/h.asp">HTML/CSS</a>
        </div>
        <div>
            <a class="BS" target="_blank" href="https://www.w3school.com.cn/b.asp">Browser Side</a>
        </div>
        <div>
            <a class="SS" target="_blank" href="https://www.w3school.com.cn/s.asp">Server Side</a>
        </div>
        <div>
            <a class="P" target="_blank" href="https://www.w3school.com.cn/p.asp">Programming</a>
        </div>
        <div>
            <a class="XML" target="_blank" href="https://www.w3school.com.cn/x.asp">XML</a>
        </div>
        <div>
            <a class="WB" target="_blank" href="https://www.w3school.com.cn/w.asp">Web Building</a>
        </div>
        <div>
            <a class="R" target="_blank" href="https://www.w3school.com.cn/r.asp">Reference</a>
        </div>
    </div>

</body>
</html>
```

```css
body{
    height: 1000px;
}

.item{      /* 设置容器的背景样式 */
    width: 1210px;      /* 设置宽度 */
    height: 48px;       /* 设置高度 */
    background-color: #E8E7E3;  /* 背景颜色 */
    margin: 100px auto;       /* 导航栏垂直居中 */

    
    /*
        - 粘滞定位
            - 当元素的position属性值设置为sticky时，则开启了该元素的粘滞定位
            - 粘滞定位和相对定位的特点基本一致，不同的是粘滞定位在到达一定高度后会将该元素固定
    */
    /* 开启粘滞定位 */
    position: sticky;
    top: 10px;      /* 当距离上方还有10px时，该元素固定 */
    
    
}

a {         /* 设置文字样式 */
    display: block;         /* 转换成块元素 */
    float: left;            /* 将全部超链接设置为浮动样式 */
    line-height: 48px;      /* 设置导航类垂直居中 */
    color: #898888;         /* 设置字体颜色 */
    text-align: center;     /* 文字水平居中方式 */
    text-decoration: none;  /* 去除超链接的下划线 */
}

a:hover{    /* 设置鼠标移入状态 */
    background-color: #3F3F3F;
    color: #CFCFCC;
}

/* 给每个超链接设置宽度和边框 */
.HC{
    width: 166px;
}
.BS{
    width: 191px;
}
.SS{
    width: 175px;
}
.P{
    width: 198px;
}
.XML{
    width: 113px;
}
.WB{
    width: 197px;
}
.R{
    width: 170px;
}
```

### 5、绝对定位的布局

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1">
        <div class="box2"></div>
    </div>

</body>
</html>
```

```css
/*
    - 水平布局：
        包含块内容区的宽度=（margin-left）+（border-left）+（padding-left）+（width）+（padding-right）+（border-right）+（margin-right）

    - 绝对定位的布局：
        - 水平布局的宽度=（left）+（margin-left）+（border-left）+（padding-left）+（width）+（padding-right）+（border-right）+（margin-right）+（right）
        - 垂直布局的高度=（top）+（margin-top / bottom）+（padding-top / bottom）+（border-top / bottom）+（height）
        - 当我们开启水平布局之后，宽度就需要加上 left 和 right 两个值，此时规则和之前一样
        - 当发生过度约束：
            - 如果9个值中没有auto，则会自动调整right值以使等式成立
            - 如果右auto，则会自动调整auto的值以使等式成立
            - 可以设置auto的值：margin、width、left和right

        - 因为left和right的值默认是auto，所以如果不知道left和right，则等式不满足时，会自动调整这两个值

*/

.box1{
    width: 500px;
    height: 500px;
    background-color: #25a4bb;

    position: relative;     /* 设置成相对定位 */
    overflow: hidden;       /* 设置溢出解决方法 */
}

.box2{
    width: 100px;
    height: 100px;
    background-color: orange;

    position: absolute;     /* 设置成绝对定位 */
    /* 设置水平居中 */
    left: 0;                /* 设置原点 */
    right: 0;
    margin-left: auto;      /* 设置左右自动调节属性 */
    margin-right: auto;

    /* 设置垂直居中 */
    top: 0;                 /* 设置原点 */
    bottom: 0;
    margin-top: auto;       /* 设置上下自动调节边距属性 */
    margin-bottom: auto;
}
```

### 6、层级

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1">1</div>
    <div class="box2">2</div>
    <div class="box3">3</div>

    <div class="box4">
        4
        <div class="box5">5</div>
    </div>


</body>
</html>
```

```css
/*
    - 对于开启了定位的元素，可以通过z-index属性来指定元素的层级，其参数是整数
        - z-index的值越大层级越高，层级越高越优先显示
        - 如果层级相同，则优先显示结构上靠下的元素
        - 祖先元素的层级再高，也永远盖不住后代元素
*/

div{           /* 设置共同属性 */
    font-size: 50px;        /* 设置字体大小 */
    position: absolute;     /* 为三个元素开启定位 */
}

.box1{
    background-color: #25a4bb;
    width: 200px;
    height: 200px;
    /* 设置层级 */
    z-index: 1;
}
.box2{
    width: 200px;
    height: 200px;
    background-color: rgba(255, 0, 0, .3);
    /* 设置偏移量 */
    top: 70px;
    left: 70px;
    /* 设置层级 */
    z-index: 2;
}
.box3{
    width: 200px;
    height: 200px;
    background-color: #333333;
    /* 设置偏移量 */
    top: 140px;
    left: 140px;
    /* 设置层级 */
    z-index: 3;
}


.box4{
    margin-top: 400px;      /* 设置上边距 */
    width: 300px;
    height: 300px;
    background-color: orange;

    position: absolute;
    z-index: 3;
}
.box5{
    width: 150px;
    height: 150px;
    background-color: sienna;

    position: absolute;
    /* 相比于父元素，该元素没有设置层级，但显示时，该元素还是在父元素的上层 */
}
```

## 第二节：字体

### 1、字体族

> - color：用来设置字体的颜色
> - font-size：用来设置字体的大小
>   - px：一个px代表一个像素
>   - em：相当于当前元素的一个font-size
>   - rem：相当于根元素的一个font-size
> - font-family：字体族（字体的格式）
>   - serif：衬线字体
>   - sans-serif：非衬线字体
>   - monospace：等宽字体
>   - font-family 可以同时指定多个字体样式，使用逗号隔开，使用优先级依次往后
> - 一般使用语句：font-family: Arial, "Microsoft Yahei", "Helvetica Neue", Helvetica, sans-serif;

### 2、图标字体

> ### 使用fontawesome图标网站方式

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <!-- 引入图标字体库 -->
    <link rel="stylesheet" href="./图标字体/css/all.css">
    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <!--
        fontaweome网站图标使用步骤
            - 下载：直接去fontawesome官网
            - 解压
            - 将css和webfonts文件夹移动到项目中
            - 将css文件夹中的all.css用link的方式引入到网页中
            - 使用图标字体
                - 直接通过类名去使用图标字体
                - 由于该图标是矢量图，所以不会失真，并且可以设置css样式
                - 举例：fas和fab是两个类型，必须要写，后面的是图标的名称
                    class="fas fa-bell"
                    class="fab fa-accessible-icon"

    -->
    <!-- 基础用法展示 -->
    <i class="fas fa-bell"></i>
    <i class="fab fa-accessible-icon"></i>
    <!--
        通过实体使用图标
            语法：&#x图标的编码;
    -->
    <i class="fas">&#xf0f3;</i>
    <br><br>

    <!-- 文字用法展示 -->
    <p>锄禾日当午</p>
    <p>汗滴禾下土</p>
    <p>谁知盘中餐</p>
    <p>粒粒皆辛苦</p>

</body>
</html>
```

```css
/* 基础用法展示 */
i{
    font-size: 100px;
    color: red;
}

i:hover{
    color: blue;
}

/*
    通过伪元素设置图标字体
        - 找到要设置图标的元素通过before或after选中
        - 在content中设置图标的编码，需要转义
        - 设置字体样式
            - fas：font-family: 'Font Awesome 5 Free';
            - fab：font-family: "Font Awesome 5 Brands"; font-wight: 900;
*/
p::before{
    content: '\f1b0';       /* 图标编号，需要加转义符号 */
    font-family: 'Font Awesome 5 Free';     /* 字体格式 */
    font-weight: 900;       /* 设置图标大小 */
    margin-right: 10px;      /* 设置右边距 */
    color: #1963ca;         /* 图标颜色 */
}
```

> ### 通过阿里巴巴矢量图标库（iconfont）方式

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <!-- 导入iconfont图标 -->
    <link rel="stylesheet" href="./iconfont图标/iconfont.css">
    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <i class="iconfont">&#xe637;</i>
    <i class="iconfont">&#xe624;</i>
    <i class="iconfont">&#xe627;</i>
    <i class="iconfont">&#xe62f;</i>

    <p class="iconfont-word">Hello,HTML5 and CSS3!</p>


</body>
</html>
```

```css
/* 只显示图标的使用方法 */
i.iconfont{
    font-size: 100px;
    color: red;
}

/* 结合文字的使用方法 */
p{          /* 设置文字样式 */
    font-size: 40px;
    color: blue;
}
p::before{
    content: '\e63d';       /* 添加图标编码 */
    font-family: 'iconfont';/* 设置图标格式 */
    font-size: 40px;
    color: #25a4bb;
    margin-right: 10px;     /* 设置右边距 */
}
```

### 3、行高与字体框

> - 行高指的是文字占有的实际高度，默认情况下被内容的大小撑开
> - 可以通过line-height来指定行高
>   - 行高可以指定一个大小（px、em）
>   - 可以指定一个整数（字体的指定倍数）
>   - 默认行高是1.3333 
> - 行高经常用来设置文字的行间距，行间距=行高-字体大小
>
> 
>
> - 字体框是字体存在的格子，设置font-size实际上就是在设置字体框的高度
>
>   
>
> - 行高会在字体框上平均分配

### 4、字体的简写属性

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div>今天天气真不错！</div>

</body>
</html>
```

```css
/*
    - font 可以设置字体的所有相关属性
        - 语法：
            - font：字体大小/行高  字体族
            - 行高 可以省略不写，不写是默认值

    - font-weight：设置字重，字体的加粗
        - normal：默认值，不加粗
        - bold：加粗

    - font-style：设置字体风格
        - normal：正常的
        - italic：斜体
*/

div{
    border: 2px red solid;
    font: 50px 'Times New Roman',Times, Serif;
    font-weight: bold;      /* 设置字重，字体的加粗 */
}
```

### 5、文字的水平和垂直对齐

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div>天功第一天道变化，消长万汇，契地之力，乃有成尔。天贵而地贱，天动而地静，贵者运机而贱者效力。上有其动，而下行其地矣。是以知天之施地匪专也，知地之应天有常也。生机动则应之以生，气机动则应之以气。机正则泰，机乱则否。万物列形而否泰交著，见之于地焉，岂止地之为乎？盖天道内而地道外者也。王者，天也；将，地也。将者，天也；士卒，地也。我，天也；敌，地也。由此观其所动，故负胜可知矣。王之於将也，阃外之寄，择贤授柄，举无所疑。将必内应其正，外务其顺。应以正则师律严，务以顺则臣节贞。举而御敌，讵有舆尸之患乎？君恃智以自用，倨礼而傲下，授柄匪人，任人不信，将不正应，内包犹豫之惑，外丧驭众之威矣。举而御敌，宁免失律之凶乎？将之为任也，智敌万人，苟无万人之用，与愚者同矣；勇冠三军，苟无三军之用，与懦者同矣。善为将者正而能变，刚而能恤，仁而能断，勇而能详，以策驭吏士，未有不振拔勋业，以戡祸乱者也。反是，则吏士外无攻，内多离散之势。勇怯见之吏士焉，岂吏士之为乎？我之於敌也，夫功拔战胜，使敌不敢抗衡者，岂敌怯乎？由我威令整，进退肃，赏罚明也。覆兵杀将，弱国削地者，岂敌强威乎？由我不严师律故也。夫如是，亦自上而及下，自内而迨外，其犹天地之用乎。故天必藉地力，然后运四气，正生杀也；贵必藉贱力，然后能立元功而建王业也。　　地利第二　　地之形，险易殊也；地之气，寒热异也。用形与气，在知逆顺焉。昧此道者，不能得地利必矣。</div>
    <p>
        今天的天气
        <span>
            真不错
        </span>
        ！！！
    </p>

</body>
</html>
```

```css
/* 水平对齐方式 */
div{
    width: 500px;
    border: 2px red solid;
    /*
        - text-align：文本的水平对齐
            - left：左对齐
            - right：右对齐
            - center：居中对齐
            - justify：两端对齐
    */
    text-align: center;
}

/* 垂直对齐方式 */
p{
    font-size: 50px;
    border: 2px red solid;
}
span{
    font-size: 20px;
    border: 2px blue solid;
    /*
        - vertical-align：文本的垂直对齐方式（消除图片与边框的距离）
            - baseline：默认值，基线对齐
            - top：顶部对齐
            - bottom：底部对齐
            - middle：居中对齐
    */
    vertical-align: middle;
}
```

### 6、其他文本样式

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1">
        今天天气真不错！
    </div><br><br>

    <div class="box2">
        HTML5是Web中核心语言HTML的规范，用户使用任何手段进行网页浏览时看到的内容原本都是HTML格式的，在浏览器中通过一些技术处理将其转换成为了可识别的信息。HTML5在从前HTML4.01的基础上进行了一定的改进，虽然技术人员在开发过程中可能不会将这些新技术投入应用，但是对于该种技术的新特性，网站开发技术人员是必须要有所了解的。 [1-2]
    </div>

</body>
</html>
```

```css
/*
    - text-decoration：文本修饰
        - none：默认值，什么都没有
        - underline：下划线
        - overline：上划线
        - line-through：删除线

    - white-space：设置网页如何处理空白
        - normal：默认值，正常
        - nowrap：不论多少文字，都不换行，和overflow配合使用
        - pre：保留文本所写的空白，和源码显示的一样

*/
.box1{
    font-size: 50px;
    text-decoration: underline red;     /* 第一个设置样式，第二个设置颜色 */
}

.box2{
    /* 以下四行要配合使用 */
    width: 300px;               /* 设置文字展示宽度 */
    white-space: nowrap;        /* 只显示一行文字，不换行 */
    overflow: hidden;           /* 裁剪掉多余的文字，和遮盖差不多 */
    text-overflow: ellipsis;    /* 将溢出的内容以省略号展示 */
}
```

## 第三节：背景

### 1、背景（一）

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box"></div>


</body>
</html>
```

```css
/*
    - background-color：设置背景颜色

    - background-image：设置背景图片路径
        - 可以同时设置背景图片和背景颜色，这时背景颜色就是背景图片的背景颜色
        - 如果背景图片小于元素，则背景图片会在元素中平铺，直到把元素铺满
        - 如果背景图片大于元素，则将有一部分图片无法正常显示
        - 如果背景图片和元素一样大，则正常显示

    - background-repeat：设置背景图片的重复方式
        - repeat：默认值，背景会沿x轴，y轴两个方向重复
        - repeat-x：背景会沿x轴方向重复
        - repeat-y：背景会沿y轴方向重复
        - no-repeat：背景图片不重复（有多大，显示多大）

    - background-position：设置背景图片的位置
        - 通过top、left、right、bottom、center设置位置（至少需要两个方位值连用）
            - 一般两个值连用，表示方位
            - 只用一个值，第二个值默认是center
        - 通过偏移量指定图片位置（以像素（px）为单位）
            - 第一个值：水平方向的偏移量
            - 第二个值：垂直方向的偏移量
*/
.box{
    /* 设置图片展示区域大小 */
    width: 600px;
    height: 600px;

    background-color: red;                      /* 设置图片背景颜色 */
    background-image: url("图片/素材.gif");      /* 设置图片路径 */
    background-repeat: no-repeat;               /* 设置图片重复方式 */
    background-position: center center;         /* 设置图片位置 */
}
```

### 2、背景（二）

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1">
        <div class="box2"></div>
    </div>


</body>
</html>
```

```css
/*
    - background-clip：设置背景范围
        - border-box：默认值，背景出现在边框下边
        - padding-box：背景不会出现在边框上，只出现在内容去和内边框间
        - content-box：背景只会出现在内容区

    - background-origin：背景图片偏移量计算的原点
        - padding-box：默认值，background-position从内边距开始计算
        - content-box：背景图片的偏移量从内容区开始计算
        - border-box：背景图片的偏移量从边框开始计算

    - background-size：设置图片的尺寸
        - 第一个值表示宽度
        - 第二个值表示高度
        - 只写一个，第二个值等比例缩放
        - 也可以设置为百分比形式
        - cover：图片比例不变，将图片展示区域铺满，图片可能显示不全
        - contain：图片比例不变，完整显示图片，有的位置会出现

    - background-attachment：背景图片是否跟随元素（滚动条）移动
        - scroll：默认值，背景图片会跟随元素移动
        - fixed：背景图片会固定到页面中，不会随元素移动，定位原点相对于视口

    - background：背景相关的简写属性，没有顺序要求
*/
.box1 {
    /* 设置图片展示区域大小 */
    width: 600px;
    height: 600px;
    /* 背景（一）知识 */
    background-color: #ffa526; /* 设置图片背景颜色 */
    /*background-image: url("图片/素材.gif");      !* 设置图片路径 *!*/
    background-repeat: no-repeat; /* 设置图片重复方式 */
    background-position: 0 0; /* 设置图片位置 */
    /* 背景（二）知识 */
    /*border: 10px red double;*/
    /*background-clip: content-box;*/

    background-image: url("图片/001.jpg"); /* 设置图片路径 */
    background-size: contain;
    overflow: auto;             /* 遮盖住子元素溢出部分 */
}

.box2{
    width: 300px;
    height: 1000px;
    background-color: #bbffaa;
    background-image: url("./图片/素材.gif");
    background-repeat: no-repeat;

    background-attachment: scroll;		/* 设置图片是否跟随元素移动 */
}
```

### 3、线性渐变

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1"></div>
    <div class="box2"></div>
    <div class="box3"></div>

</body>
</html>
```

```css
/*
    - 通过渐变可以设置一些复杂的背景颜色，可以实现从一个颜色向其他颜色过度的效果。渐变的是图片，需要通过background-image来设置。

    - linear-gradient()：线性渐变，颜色沿着一条直线发生改变
        - 第一个值是开头，第二个值、、、第n个值是结尾
        - 指定渐变方向，写在括号里最前面
            - to left：向左渐变
            - to right：向右渐变
            - to bottom：向下渐变
            - to top：向上渐变
            - xxxdeg：deg表示旋转度数
            - 也可以写两个方位值，比如to top left表示向左上渐变
            - turn：表示圈（.25turn）
        - 渐变可以同时指定多个颜色，多个颜色默认情况下平均分配
        - 可以手动指定分配情况

    - repeating-linear-gradient()：重复线性渐变，用法和上述用法一样

*/

div{        /* 全部设置成浮动，方便观察 */
    float: left;
    margin-right: 5px;
}

.box1{
    display: block;
    width: 400px;
    height: 400px;
    background-image: linear-gradient(to bottom, red, blue, yellow);
}

/* 手动分配颜色分布 */
.box2{
    width: 400px;
    height: 400px;
    /* 从父元素的第50个像素开始渐变，50像素之内，都是纯色 */
    background-image: linear-gradient(red 50px, blue);
}

/* 重复的线性渐变 */
.box3{
    width: 400px;
    height: 400px;
    background-image: repeating-linear-gradient(red 50px, blue 100px);
}
```

### 4、径向渐变

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1"></div>
    <div class="box2"></div>

</body>
</html>
```

```css
/*
    - radial-gradient()：径向渐变（呈放射性效果）
        - 默认情况下，径向渐变的形状根据元素可视的区域来决定
        - 基本用法和线性渐变的用法一样
        - 可以手动指定径向渐变的大小
            - circle：表示正圆，无论元素可视区域是不是正方形
            - ellipse：默认值，元素可视区域为正方形就是圆，为长方形就是椭圆
        - 可以指定元素的位置
            - radial-gradient(大小 at 位置, 颜色 位置, 颜色 位置, 、、、)
            - 大小：
                - circle：圆形
                - ellipse：椭圆
                - closest-side：近边和元素可视区域贴合
                - closest-cornet：近角和元素可视区域贴合
                - farthest-side：远边和元素可视区域贴合
                - farthest-cornet：远角和元素可视区域贴合
            - 位置：
                - center  top  left  bottom  right
*/

div{        /* 全部设置成浮动，方便观察 */
    float: left;
    margin-right: 5px;
}

.box1{
    width: 500px;
    height: 400px;
    background-image: radial-gradient(circle, red, blue);
}

/* 设置径向渐变的位置 */
.box2{
    width: 500px;
    height: 400px;
    background-image: radial-gradient(at 100px 100px, red, blue);
}
```

## 第四节：表格

### 1、表格的简介

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>
</head>
<body>

    <!--
        通过table标签来创建一个表格
            - 在table中使用tr表示表格中的一行，有几个tr就有几行
            - 在tr中使用td表示一个单元格，有几个td就有几个单元格
    -->
    <table border="1" width="50%" align="center">
        <tr>
            <td>A1</td>
            <td>B1</td>
            <td>C1</td>
        </tr>
        <tr>
            <td>A2</td>
            <td>B2</td>
            <!-- rowspan：纵向的合并单元格 -->
            <td rowspan="2">C2</td>
        </tr>
        <tr>
            <td>A3</td>
            <td>B3</td>
<!--            <td>C3</td>-->
        </tr>
        <tr>
            <td>A4</td>
            <!-- colspan：横向的合并单元格 -->
            <td colspan="2">B4</td>
<!--            <td>C4</td>-->
        </tr>
    </table>


</body>
</html>
```

### 2、长表格

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>
</head>
<body>

    <!--
        - 分层次写可以像块元素一样，不论位置在哪都不会变

        - 可以将一个表格分成三个部分
            - thead：头部
            - tbody：主体
            - tfoot：底部
    -->
    <table border="1" width="50%">
        <!-- 头部 -->
        <thead>
            <tr>
                <td>日期</td>
                <td>收入</td>
                <td>支出</td>
                <td>合计</td>
            </tr>
        </thead>
        <!-- 主体 -->
        <tbody>
            <tr>
                <td>2000.1.1</td>
                <td>500</td>
                <td>200</td>
                <td>300</td>
            </tr>
            <tr>
                <td>2000.1.2</td>
                <td>200</td>
                <td>100</td>
                <td>100</td>
            </tr>
            <tr>
                <td>2000.1.3</td>
                <td>300</td>
                <td>200</td>
                <td>100</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td></td>
                <td></td>
                <td>合计</td>
                <td>500</td>
            </tr>
        </tfoot>
    </table>

</body>
</html>
```

## 第五节：表单

### 1、表单的介绍

```html
<!-- 表单的介绍 -->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <!--
        表单：
            - 使用form标签来创建一个表单

        form属性：
            - action：表单要提交的服务器地址
    -->

    <form action="./表单演示服务器.html">
        <!-- 
            文本输入框：数据要提交到服务器中，必须要为元素指定一个name属性值
        -->
        文本框：<input type="text" name="数据提交文档">
        <br><br>

        <!--
            密码框：数据要提交到服务器中，必须要为元素指定一个name属性值
        -->
        密码框：<input type="password" name="123456">
        <br><br>

        <!--
            单选按钮
                - 通过name属性分组，实现单选效果
                - 像这种选择框，必须要指定一个value属性，value属性会作为用户填写的值传递给服务器
                - checked：单选按钮设置为默认选中状态
        -->
        单选按钮：<input type="radio" name="单选组" value="a" checked>
                 <input type="radio" name="单选组" value="b">
        <br><br>

        <!--
            多选按钮
                - 通过name属性分组，实现单选效果
                - 像这种选择框，必须要指定一个value属性，value属性会作为用户填写的值传递给服务器
                - checked：单选按钮设置为默认选中状态
        -->
        多选按钮：<input type="checkbox" name="多选组" value="1" checked>
                 <input type="checkbox" name="多选组" value="2" checked>
                 <input type="checkbox" name="多选组" value="3">
                 <input type="checkbox" name="多选组" value="4">
        <br><br>

        <!--
            下拉列表
                - value：设置选中的需要提交的数据
                - selected：设置默认选中项
        -->
        下拉列表：<select name="hello">
            <option value="1">选项一</option>
            <option selected value="2">选项二</option>
            <option value="3">选项三</option>
        </select>
        <br><br>

        <!--
            提交按钮
        -->
        提交按钮：<input type="submit" value="提交">
    </form>

</body>
</html>
```

```html
<!-- 表单的补充 -->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>
</head>
<body>

    <!--
        autocomplete：自动补全功能，on为打开，off为关闭，放在form标签里，所有文本框都适用
        readonly：设置成只读文本，不能修改其内容，数据会提交
        disabled：设置成禁用，数据不会提交
        autofocus：自动获取焦点
    -->

    <form action="./表单演示服务器.html">
        文本框：<input type="text" name="username" value="hello" autocomplete="off">   <!-- 默认值是hello -->
        <br><br>
        文本框：<input type="text" name="username" readonly>
        <br><br>
        文本框：<input type="text" name="username" disabled>
        <br><br>
        文本框：<input type="text" name="username" autofocus>
        <br><br>

        提交按钮：<input type="submit">
        <br><br>

        <!--
            普通按钮：仅仅可以点击，在没有js的帮助下不产生任何动作
        -->
        普通按钮：<input type="button" value="普通按钮">
        <br><br>

        <!--
            重置按钮：将文本框里的内容重置
        -->
        重置按钮：<input type="reset">
        <br><br>

        <p>上述三种按钮的另一种写法：</p>
        <button type="submit">提交</button>
        <button type="button">普通按钮</button>
        <button type="reset">重置</button>
        <br><br>

        <!--
            色彩框
        -->
        色彩框：<input type="color">
        <br><br>

        <!--
            电子邮件文本框：必须按照邮件格式才能提交
        -->
        电子邮件文本框：<input type="email">

    </form>

</body>
</html>
```

```html
<!-- 表单演示服务器 -->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>服务器</title>
</head>
<body>

    <h1>您的数据已经收到！！！</h1>

</body>
</html>
```

## 第六节：像素

### 1、像素简介

```html
<!--
    - 像素：屏幕是由一个一个发光的小点构成，这一个个的小点就是像素

    - 分辨率：1920 x 1080说的就是屏幕中小点的数量

    - 在前端开发中像素要分成两种情况讨论：CSS像素和物理像素
        - 物理像素，上述所说的小点 点就属于物理像素
        - CSS像素，编写网页时，我们所用像素都是CSS像素
        - 浏览器在显示网页时，需要将CSS像素转换为物理像素然后再呈现，一个css像素 最终由几个物理像素显示，由浏览器决定；默认情况下在pc端，一个css像素 = 一个物理像素

    - 视口(viewport)：视口就是屏幕中用来显示网页的区域
        - 可以通过查看视口的大小，来观察CSS像素和物理像素的比值
        - 默认情况下:
            - 视口宽度：1920px (CSS像素)  1920px (物理像素)，此时，css像素 和物理像素的比是1：1
            - 放大两倍的情况：视口宽度960px (CSS像素)  1920px (物理像素)，此时，css像 素和物理像素的比是1：2
-->
```

### 2、手机像素

```html
<!--
    - 在不通的屏幕，单位像素的大小是不同的，像素越小屏幕会越清晰
    	- 24寸 1920 x 1080
    	- iPhone6 4.7寸750 x 1334
    	- 智能手机的像素点远远小于计算机的像素点
    
	- 问题：一个宽度为900px的网页在iphone6中要如何显示呢?
    	- 默认情况下，移动端的网页都会将视口设置为980像素(css像素)，以确保pc端网页可以在移动端正常访问，但是如果网页的宽度超过了980,移动端的浏览器会自动对网页缩放以完整显示网页
-->
```

### 3、完美视口

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">

    <!-- 设置视口大小，device-width表示设备的宽度（完美视口） -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>index</title>

    <link rel="stylesheet" href="./index.css">

</head>
<body>

    <!--
        - 移动端默认的视口大小是980px(css像素)
            - 默认情况下，移动端的像素比就是  980/移动端 宽度(980/750)
            - 编写移动页面时，必须要确保有一个比较合理的像素比:
                - 1css像素对应2个物理像素
                - 1css像素对应3个物理像素
                - 可以通过meta标签来设置视口大小
                - 每一款移动设备设计时，都会有一个最佳的像素比，一般我们只需要将像素比设置为该值即可得到一个最佳效果
                - 将像素比设置为最佳像素比的视口大小我们称其为完美视口
                - 设置视口大小，device-width表示设备的宽度（完美视口）
                - 结论：以后再写移动端的页面，就把下面这个代码写上，设置完美视口
                    - <meta name="viewport" content="width=device-width, initial-scale=1.0">
    -->

</body>
</html>
```



## 第七节：响应式布局（媒体查询）

### 1、媒体查询简介

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>index</title>

    <link rel="stylesheet" href="./index.css">

</head>
<body>

    <!--
        - 响应式布局
            - 网页可以根据不同的设备或窗口大小呈现出不同的效果
            - 使用响应式布局，可以使一个网页适用于所有设备
            - 响应式布局的关键就是媒体查询
            - 通过媒体查询，可以为不同的设备或设备不同状态分别设置样式
    -->
    <div class="box"></div>

</body>
</html>
```

```css
/*
    - 媒体查询
        - 语法：@media 查询规则()
            - all：所有设备都生效
            - print：针对打印设备
            - screen：针对带屏幕的设备
            - speech：针对屏幕阅读器
            - 可以使用逗号连接多个媒体类型，这样它们之间就是一个或的关系
*/

@media all {
    .box{
        width: 200px;
        height: 200px;
        background-color: #FF6700;
    }
}
```

### 2、媒体查询特性

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>index</title>

    <link rel="stylesheet" href="./index.css">

</head>
<body>

</body>
</html>
```

```css
/*
    - 媒体查询特性
        - width：视口的宽度
        - height：视口的高度
        - min-width：视口的最小宽度（视口大于指定宽度生效）
        - max-width：视口的最大宽度（视口小于指定宽度生效）

    - 样式切换的分界点，称为断点，也就是网页样式会发生变化的点
        - 小于768：超小屏幕，max-width=768px
        - 大于768：小屏幕，min-width=768px
        - 大于992：中型屏幕，min-width=992px
        - 大于1200：大屏幕，min-width=1200px
*/

@media (width: 500px) {             /* 当视口为500px时，显示布局 */
    body{
        background-color: #FF6700;
    }
}
```









# 第五章：动画效果

## 第一节：过渡动画

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./默认样式清除程序/reset.css">
    <link rel="stylesheet" href="./CSS测试.css">
    
</head>
<body>

    <div class="box1">
        <div class="box2"></div>
        <div class="box3"></div>
    </div>

</body>
</html>
```

```css
/*
    过渡（transition）
        - 通过过渡可以指定一个属性发生变化的切换方式
        - 多个属性使用逗号隔开，如果所有属性都需要过渡，直接指定all

    - transition-property: 指定哪些属性需要进行过渡效果

    - transition-duration: 指定过渡效果持续的时间（1s = 1000ms），也可以分别对属性指定时间，但是要对应

    - transition-timing-function: 过渡的时序函数，指定过渡的执行方式
        - ease：默认值，先加速，再减速
        - linear：匀速运动
        - ease-in：加速运动
        - ease-out：减速运动
        - ease-in-out：先加速，再减速
        - cubic-bezier()：贝塞尔曲线，指定时序函数
            - 网址：https://cubic-bezier.com/#.17,.67,.83,.67，复制导航栏的数据
        - steps()：分布过渡效果
            - start：时间均分后，鼠标移入的开始就动
            - end：时间均分后，鼠标移入后过时间均分后才开始动

    - transition-delay: 过渡动画效果的延迟，等待一段时间后开始执行

    - transition: 简写属性，一次性写多个需求值，如果要写延迟，则两个的第一个是持续时间，第二个是延迟时间
*/

/* 设置子元素样式 */
.box2{
    background-color: #bbffaa;

    /*transition: height 2s;              !* 用两秒钟进行高度的变化 *!*/
    /*transition: all 2s;                     !* 用两秒钟进行全部属性的变化（高度和宽度） *!*/
    transition-property: all;
    transition-duration: 2s;
    transition-delay: 2s;

}
.box3{
    background-color: #FF6700;

    /*transition-timing-function: ease;         默认值，先加速，再减速 */
    /*transition-timing-function: linear;       匀速运动 */
    /*transition-timing-function: ease-in;      加速运动 */
    /*transition-timing-function: ease-out;     减速运动 */
    /*transition-timing-function: ease-in-out;  先加速，再减速 */
    /*transition-timing-function: cubic-bezier(0,1.95,1,-0.93);*/
    /*transition-timing-function: steps(4);      分四步执行过渡动画 */
    /*transition-timing-function: steps(2, start);      每步在一秒之前立马动 */
    /*transition-timing-function: steps(2, end);        每步在一秒之后才动 */
    transition-property: all;
    transition-duration: 2s;

}

/* 设置鼠标进入box1时，box2发生变化 */
.box1:hover div{
    width: 200px;                       /* 设置元素变大宽度 */
    height: 200px;                      /* 设置元素变大高度 */
    background-color: #f10215;          /* 设置元素变换颜色 */
    margin-left: 700px;                 /* 设置最终元素出现位置 */
}

/* 设置清除样式 */
*{
    padding: 0;
    margin: 0;
}

/* 设置box1样式 */
.box1{
    width: 800px;
    height: 600px;
    background-color: silver;
    overflow: hidden;
}

.box1 div{
    width: 100px;
    height: 100px;
    margin-top: 100px;              /* 设置初始位置 */
    margin-left: 0;                 /* 设置初始位置 */
}
```

## 第二节：关键帧

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="outer">
        <div class="box1"></div>
        <div class="box2"></div>
        <div class="box3"></div>
        <div class="box4"></div>
        <div class="box5"></div>
        <div class="box6"></div>
        <div class="box7"></div>
        <div class="box8"></div>
        <div class="box9"></div>
        <div class="box10"></div>
    </div>

</body>
</html>
```

```css
.outer{
    height: 500px;
    border-bottom: 10px black solid;
    margin: 50px auto;
    overflow: hidden;           /* 开启BFC，防止和子元素块一起运动 */
}

.outer div{
    float: left;
    width: 100px;
    height: 100px;
    border-radius: 50%;
    background-color: #bbffaa;

    /* 开启小球下落动画 */
    animation: ball 0.5s forwards infinite alternate;
}

/* 创建小球下落动画 */
@keyframes ball {
    from{       /* 开始加速下落 */
        margin-top: 0;
    }
    /*25%{        !* 总时间的25%时的动画状态。开始减速上升 *!*/
    /*    margin-top: 400px;*/
    /*    animation-timing-function: ease-in;     !* 减速 *!*/
    /*}*/
    /*50%{        !* 总时间的50%时的动画状态，开始加速下落 *!*/
    /*    margin-top: 200px;*/
    /*}*/
    /*70%{        !* 总时间的70%时的动画状态，开始减速上升 *!*/
    /*    margin-top: 400px;*/
    /*    animation-timing-function: ease-in;     !* 减速 *!*/
    /*}*/
    /*90%{        !* 总时间的90%的动画状态，开始加速下落 *!*/
    /*    margin-top: 350px;*/
    /*}*/
    to{         /* 最终停止状态 */
        margin-top: 400px;
    }
}

/* 设置小球颜色 */
div.box2{
    background-color: #FF6700;
    animation-delay: 0.1s;          /* 添加延迟 */
}
div.box3{
    background-color: #6cff8a;
    animation-delay: 0.2s;          /* 添加延迟 */
}
div.box4{
    background-color: #54b8ff;
    animation-delay: 0.3s;          /* 添加延迟 */
}
div.box5{
    background-color: #fffed6;
    animation-delay: 0.4s;          /* 添加延迟 */
}
div.box6{
    background-color: #ffd442;
    animation-delay: 0.5s;          /* 添加延迟 */
}
div.box7{
    background-color: #ff77a3;
    animation-delay: 0.6s;          /* 添加延迟 */
}
div.box8{
    background-color: #c62dff;
    animation-delay: 0.7s;          /* 添加延迟 */
}
div.box9{
    background-color: #71ff57;
    animation-delay: 0.8s;          /* 添加延迟 */
}
div.box10{
    background-color: #ff0a18;
    animation-delay: 0.9s;          /* 添加延迟 */
}
```

## 第三节：平移

### 1、基础平移

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1"></div>
    <div class="box2"></div>
    <div class="box3">Hello Web！</div>
    <div class="box4"></div>        <!-- 飘出样式演示 -->

</body>
</html>
```

```css
/*
    变形是指通过CSS来改变元素的形状或位置
        - 变形不会影响到页面的布局
        - transform：用来设置元素的变形效果
            - 平移：
                - translateX()：沿着X轴方向平移
                - translateY()：沿着Y轴方向平移
                - translateZ()：沿着Z轴方向平移
                    - 平移元素，百分比使相对于自身计算的
*/

.box1{
    width: 150px;
    height: 150px;
    margin: 0 auto;
    background-color: #bbffaa;

    /*transform: translateX(100px);           !* 向X轴正方向（向右）平移100个像素 *!*/
    /*transform: translateY(100px);           !* 向Y轴正方向（向下）平移100个像素 *!*/
}
.box2{
    width: 150px;
    height: 150px;
    margin: 0 auto;
    background-color: #ff374a;
}
.box3{                  /* 演示元素没有确定大小，仍可以居中的样式 */
    position: absolute;
    background-color: #3991ff;

    left: 50%;          /* 确定左边距 */
    top: 50%;           /* 确定上边距 */
    transform: translateX(-50%) translateY(-50%);        /* 设置平移数值 */
}

.box4{
    width: 200px;
    height: 200px;
    margin: 0 50px;
    background-color: #bbb65a;
    transition: all 0.2s;       /* 设置动画效果 */
}
/* 鼠标移入，展现飘出效果 */
.box4:hover{
    transform: translateY(-3px);        /* 设置平移量 */
    box-shadow: 0 5px 10px rgba(224, 224, 224, 1);      /* 设置阴影 */
}
```

### 2、Z轴平移

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box"></div>

</body>
</html>
```

```css
/*
    - Z轴平移：调整元素在Z轴的位置，正常情况就是调整元素和人之间的距离，距离越大，元素离人越近

    - Z轴平移属于立体效果，近大远小，默认情况下网页是不支持透视，如果想看见效果，必须设置视距
*/

/* 设置当前网页的视距为800px，人眼距离网页的距离 */
html{
    perspective: 800px;         /* 设置视距 */
}

/* 设置鼠标移入网页，出现动画效果 */
body:hover .box{
    transform: translateZ(150px);       /* 数值越大，离人越近 */
}

.box{
    width: 200px;
    height: 200px;
    background-color: #bbffaa;
    margin: 200px auto;

    transition: transform 2s;           /* 设置动画效果 */
}
```

## 第四节：旋转

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box"></div>

</body>
</html>
```

```css
/*
    旋转：可以使元素沿着x，y或z轴旋转指定的角度
        - rotateX()：以X轴为旋转轴
        - rotateY()：以Y轴为旋转轴
        - rotateZ()：以Z轴为旋转轴
        - backface-visibility：是否显示背面
*/

/* 设置当前网页的视距为800px，人眼距离网页的距离 */
html{
    perspective: 800px;         /* 设置视距 */
}

/* 设置鼠标移入网页，出现动画效果 */
body:hover .box{
    transform: rotateX(90deg) rotateY(90deg) rotateZ(90deg);          /* 以X轴为旋转轴 */
    /*transform: rotateY(90deg);*/
    /*transform: rotateZ(90deg);*/
    backface-visibility: visible;
}

.box{
    width: 200px;
    height: 200px;
    background-color: #bbffaa;
    margin: 200px auto;

    transition: 2s;           /* 设置动画效果 */
}
```





# 第六章：less

## 第一节：less简介

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <!--
        less是一门css的预处理语言
            - less是一个css的增强版，通过less可以编写更少的代码实现更强大的功能
            - 在less中添加了许多新的特性，也添加了许多对css的扩展
    -->
    <div class="box1">Hello!</div>
    <div class="box2">Hello!</div>
    <div class="box3">Hello!</div>

</body>
</html>
```

```css
/*
    css原生也支持变量的设置
        - 统一样式：利用宏定义，用变量代替具体的数值
            - 语法：--宏定义名称：需要设置的样式数值

        - 自动计算函数：calc(填写具体的表达式)
 */
html{
    --color: #ffff00;
}


/* 设置测试样式 */
.box1{
    width: calc(200px/2);
    height: 100px;
    background-color: var(--color);
}
.box2{
    width: 100px;
    height: 100px;
    color: var(--color);
}
.box3{
    width: 100px;
    height: 100px;
    border: 10px solid var(--color);
}


.box1{
    width: 200px;
    height: 200px;
}
```





# 第七章：弹性盒

## 第一节：弹性盒简介

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./reset.css">
    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <!--
        flex(弹性盒，伸缩盒)
            - 是CSS中的一种布局手段，它主要用来替代浮动来完成页面的布局
            - flex可以是元素具有弹性，让元素可以跟随页面大小的改变而改变
    -->
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>

</body>
</html>
```

```css
/*
    - 弹性容器：要使用弹性容器，必须先将一个元素通过display属性设置为弹性容器
        - display：flex          设置为弹性容器，会独占一行
        - display：inline-flex   设置为行内的弹性容器，不会独占一行

    - 弹性元素：
        - 弹性容器的子元素就是弹性元素（弹性项）
        - 一个元素可以同时是弹性容器和弹性元素，即父元素是弹性容器，自己也可以设置为弹性容器

    - 主轴：弹性元素的排列方向
    - 侧轴：与主轴垂直方向的轴

    - 弹性容器的属性
        - flex-direction：指定容器中弹性元素的排列方式
            - row：默认值，弹性元素在容器中水平排列（从左向右）
            - row-reverse：弹性元素在容器中反向水平排列（从右向左）
            - column：弹性元素方向纵向排列（自下向上）
            - column-reverse：弹性元素方向纵向排列（自下向上）

    - 弹性元素的属性
        - flex-flow：指定元素的伸展系数
            - 父元素的剩余空间，会按照比例进行分配
        - flex-shrink：指定弹性元素的收缩系数


*/

/* 弹性容器 */
ul{
    width: 800px;
    border: 10px #FF6700 solid;

    display: flex;                  /* 设置为弹性容器 */
    flex-direction: row;            /* 设置弹性容器的方向 */
}


/* 弹性元素 */
/* 设置li标签元素样式 */
li{
    width: 100px;                   /* 设置元素大小 */
    height: 100px;
    font-size: 50px;                /* 设置字体大小 */
    text-align: center;             /* 设置文字水平居中 */
    line-height: 100px;             /* 设置文字垂直居中 */
}

li:nth-child(1){
    background-color: #bbffaa;
}

li:nth-child(2){
    background-color: #25a4bb;
}

li:nth-child(3){
    background-color: yellow;
}
```

## 第二节：弹性容器样式

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./reset.css">
    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>

</body>
</html>
```

```css
/*
    - 弹性容器的属性
        - flex-wrap：设置弹性元素是否在弹性容器中自动换行
            - nowrap：默认值，元素不会自动换行
            - wrap：元素沿着辅轴方向自动换行
            - wrap-reverse：元素沿着辅轴的反方向换行

        - justify-content：设置主轴上的元素排列方式
            - flex-start：元素沿着主轴起边排列
            - flex-end：元素沿着主轴终边排列
            - center：元素居中排列
            - space-around：空白分布到元素两边（类似于同时设置margin-left和margin-tight）
            - space-between：空白均匀分布到元素间
            - space-evenly：空白分布到元素的一侧（类似于仅设置margin-left或margin-right的一个）

        - align-items：元素在辅轴上的对齐方式
            - stretch：默认值，将元素的长度设置为相同的值
            - flex-start：元素不会拉伸，沿着辅轴起边对齐
            - flex-end：元素不会拉伸，沿着辅轴终边对齐
            - center：居中对齐
            - baseline：基线对齐

        - align-content：设置辅轴在空白空间的分布
            - flex-start：元素靠上对齐，空白在下面
            - flex-end：元素靠下对齐，空白在上面
            - center：元素上下的空白相等
            - space-around：空白环绕在元素快周围
            - space-between：元素分布靠近四周，空白分布中间
*/

/* 弹性容器 */
ul{
    width: 800px;
    border: 10px #FF6700 solid;

    display: flex;                  /* 设置为弹性容器 */

    /* flex-wrap: nowrap;           设置自动换行 */
    justify-content: flex-start;
}


/* 弹性元素 */
/* 设置li标签元素样式 */
li{
    width: 200px;                   /* 设置元素大小 */
    height: 100px;
    font-size: 50px;                /* 设置字体大小 */
    text-align: center;             /* 设置文字水平居中 */
    line-height: 100px;             /* 设置文字垂直居中 */

    flex-shrink: 0;                 /* 设置缩短系数为零 */

    align-self: stretch;            /* 用来覆盖当前弹性元素上的align-items */
}

li:nth-child(1){
    background-color: #bbffaa;
}

li:nth-child(2){
    background-color: #25a4bb;
}

li:nth-child(3){
    background-color: yellow;
}
```

## 第三节：弹性元素样式

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./reset.css">
    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>


</body>
</html>
```

```css
/*
    - 弹性元素的属性
        - flex-grow：弹性元素的增长系数（按比例分配）

        - flex-shrink：弹性元素的缩减系数（按比例分配）
            - 缩减多少是根据缩减系数和元素大小来计算的

        - flex-basis：设置元素在主轴上的基础长度
            - 如果主轴是横向的，则该值指定的就是元素的宽度
            - 如果主轴是纵向的，则该值指定的就是元素的高度
            - 默认值是auto，表示参考元素自身的高度或宽度
            - 如果设置具体数值，则以该值为准

        - flex：简写属性
            - 顺序：增长  缩减  基础长度
            - initial：默认值（flex：0 1 auto）
            - auto：（flex：1 1 auto）
            - none：弹性元素没有弹性（flex：0 0 auto）

        - order：指定元素的排列顺序

*/

/* 弹性容器 */
ul{
    width: 800px;
    border: 10px #FF6700 solid;

    display: flex;                  /* 设置为弹性容器 */
}

/* 弹性元素 */
/* 设置li标签元素样式 */
li{
    width: 200px;                   /* 设置元素大小 */
    height: 100px;
    font-size: 50px;                /* 设置字体大小 */
    text-align: center;             /* 设置文字水平居中 */
    line-height: 100px;             /* 设置文字垂直居中 */

    /*flex-grow: 1;                   !* 弹性的增长系数 *!*/

    flex-basis: 100px;              /* 元素的基础长度 */
}

li:nth-child(1){
    background-color: #bbffaa;
    order: 3;
}

li:nth-child(2){
    background-color: #25a4bb;
    order: 1;
}

li:nth-child(3){
    background-color: yellow;
    order: 2;
}
```





























# 终章：练习

## 第一节：盒子模型：练习

### 1、京东右侧图片列表

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>京东右侧图片列表</title>

    <link rel="stylesheet" href="../默认样式清除程序/reset.css">    <!-- 清楚浏览器自带的默认眼视光hi -->
    <link rel="stylesheet" href="./CSS.css">        <!-- 导入自定义的样式 -->

</head>
<body>

    <div>
        <ul class="img-list">
            <li>
                <a href="https://pro.jd.com/mall/active/G6dB2UyBBfwfTVCBp3iMQQQ6GHi/index.html">
                    <img class="img1" src="./图片/宠物生活.jpg.webp" alt="宠物生活">
                </a>
            </li>
            <li>
                <a href="https://pro.jd.com/mall/active/4AfQf3FkPRGHhtqqKh9tsWyV97sy/index.html">
                    <img class="img2" src="./图片/厨卫家电.jpg.webp" alt="厨卫家电">
                </a>
            </li>
            <li>
                <a href="https://pro.jd.com/mall/active/mHMwHt4sHg2JiBs7Yeg8ogUPu4w/index.html">
                    <img class="img3" src="./图片/自营图书.jpg.webp" alt="自营图书">
                </a>
            </li>
        </ul>
    </div>
</body>
</html>
```

```css
.img-list{      /* 设置外部ul样式 */
    width: 190px;       /* 设置宽度 */
    height: 470px;      /* 设置高度 */
    background-color: red;
    overflow: hidden;   /* 裁剪溢出内容 */
}
.img-list li{       /* 设置图片的外边距 */
    margin-bottom: 10px;
}
.img-list img{      /* 设置图片大小 */
    width: 100%;
}
```

### 2、京东左侧文字列表

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="../默认样式清除程序/reset.css">    <!-- 清楚浏览器自带的默认眼视光hi -->
    <link rel="stylesheet" href="CSS测试.css">        <!-- 导入自定义的样式 -->

</head>
<body>

    <nav class="list-nav">
        <div class="item">
            <a target="_blank" href="https://jiadian.jd.com/">家用电器</a>
        </div>
        <div class="item">
            <a target="_blank" href="https://shouji.jd.com/">手机</a>
            <span class="span">/</span>
            <a target="_blank" href="https://wt.jd.com/">运营商</a>
            <span class="span">/</span>
            <a target="_blank" href="https://shuma.jd.com/">数码</a>
        </div>
        <div class="item">
            <a target="_blank" href="https://diannao.jd.com/">电脑</a>
            <span class="span">/</span>
            <a target="_blank" href="https://bg.jd.com/">办公</a>
        </div>
        <div class="item">
            <a target="_blank" href="https://channel.jd.com/home.html">家居</a>
            <span class="span">/</span>
            <a target="_blank" href="https://channel.jd.com/furniture.html">家具</a>
            <span class="span">/</span>
            <a target="_blank" href="https://jzjc.jd.com/">家装</a>
            <span class="span">/</span>
            <a target="_blank" href="https://channel.jd.com/kitchenware.html">厨具</a>
        </div>
        <div class="item">
            <a target="_blank" href="https://phat.jd.com/10-603.html">男装</a>
            <span class="span">/</span>
            <a target="_blank" href="https://phat.jd.com/10-507.html">女装</a>
            <span class="span">/</span>
            <a target="_blank" href="https://phat.jd.com/10-156.html">童装</a>
            <span class="span">/</span>
            <a target="_blank" href="https://channel.jd.com/1315-1345.html">内衣</a>
        </div>
        <div class="item">
            <a target="_blank" href="https://beauty.jd.com/">美妆</a>
            <span class="span">/</span>
            <a target="_blank" href="https://channel.jd.com/beauty.html">个人清洁</a>
            <span class="span">/</span>
            <a target="_blank" href="https://channel.jd.com/pet.html">宠物</a>
        </div>
        <div class="item">
            <a target="_blank" href="javascript:;">女鞋</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">箱包</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">钟表</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">女鞋</a>
        </div>
        <div class="item">
            <a target="_blank" href="javascript:;">男鞋</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">运动</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">户外</a>
        </div>
        <div class="item">
            <a target="_blank" href="javascript:;">房产</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">汽车</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">汽车用品</a>
        </div>
        <div class="item">
            <a target="_blank" href="javascript:;">母婴</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">玩具用品</a>
        </div>
        <div class="item">
            <a target="_blank" href="javascript:;">食品</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">酒类</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">生鲜</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">特产</a>
        </div>
        <div class="item">
            <a target="_blank" href="javascript:;">艺术</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">礼品鲜花</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">农资绿植</a>
        </div>
        <div class="item">
            <a target="_blank" href="javascript:;">医药保健</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">计生情趣</a>
        </div>
        <div class="item">
            <a target="_blank" href="javascript:;">图书</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">文娱</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">教育</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">电子书</a>
        </div>
        <div class="item">
            <a target="_blank" href="javascript:;">机票</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">酒店</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">旅游</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">生活</a>
        </div>
        <div class="item">
            <a target="_blank" href="javascript:;">理财</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">众筹</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">保险</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">白条</a>
        </div>
        <div class="item">
            <a target="_blank" href="javascript:;">安装</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">维修</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">清洗</a>
            <span class="span">/</span>
            <a target="_blank" href="javascript:;">二手</a>
        </div>
        <div class="item">
            <a target="_blank" href="javascript:;">工业品</a>
        </div>
    </nav>

</body>
</html>
```

```css
body{       /* 设置网页的背景，方便查看 */
    background-color: #cacaca;
}
.list-nav{     /* 设置基本框架样式 */
    width: 190px;   /* 设置宽度 */
    height: 450px;  /* 设置高度 */
    padding: 10px 0;    /* 设置padding */
    background-color: #daffe3;    /* 设置背景颜色 */
}

.list-nav .item{    /* 设置内部的item样式 */
    height: 25px;   /* 设置每行的行距 */
    /* 要让文字在父元素中水平居中，只需将父元素的line-height设置为和父元素相同的height即可 */
    line-height: 25px;  /* 设置文字水平居中 */
    padding-left: 15px;  /* 设置内边框距离 */
}
.item:hover{        /* 为item设置鼠标移入时的状态 */
    background-color: #d9d9d9;
}
.item a{        /* 设置超链接的样式 */
    font-size: 14px;    /* 设置超链接文字的大小 */
    color: black;     /* 设置超链接文字的颜色 */
    text-decoration: none;      /* 去除超链接的下划线 */
}
.item span{     /* 设置分割斜杠样式 */
    font-size: 14px;    /* 设置斜杠大小 */
    padding: -1px;      /* 设置内边框的距离 */
}
a:hover{        /* 改变鼠标移入时文字的状态 */
    color: #c81623;
}
```

### 3、网易的新闻列表

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="../默认样式清除程序/reset.css">    <!-- 清楚浏览器自带的默认眼视光hi -->
    <link rel="stylesheet" href="CSS测试.css">        <!-- 导入自定义的样式 -->

</head>
<body>

    <div class="news">
        <!-- 横条 -->
        <div class="x"></div>

        <!-- 标签容器 -->
        <div>
            <h2 class="title">
                <a target="_blank" href="https://money.163.com/">财经</a>
            </h2>
        </div>

        <!-- 图片容器 -->
        <div class="news-photo">
            <a class="photo" target="_blank" href="https://www.163.com/money/article/G74H2O2000259DLP.html">
                <img src="./图片/图片.webp" alt="美为阻中国进步下黑手">
                <p>美为阻中国进步下黑手</p>
            </a>
        </div>

        <!-- 新闻列表容器 -->
        <div class="list-news">
            <ul class="item">
                <li>
                    <a target="_blank" href="https://www.163.com/money/article/G74I3OHD00259HO8.html">A股展现攻击姿态，反弹空间有望扩展</a>
                </li>
                <li>
                    <a target="_blank" href="https://www.163.com/money/article/G74GOUJ400259DLP.html">由负转正！机构预测3月CPI同比涨0.2%</a>
                </li>
                <li>
                    <a target="_blank" href="https://www.163.com/money/article/G74GH9MM00259DLP.html">住建部放大招！约谈五大城市 炒房客慌了？</a>
                </li>
                <li>
                    <a target="_blank" href="https://www.163.com/money/article/G74BDJ1V002580S6.html">标普涨0.42%创历史新高 中概股集体反弹</a>
                </li>
            </ul>
        </div>
    </div>

</body>
</html>
```

```css
.news{          /* 设置news容器的样式 */
    width: 300px;           /* 设置容器的宽度 */
    height: 400px;          /* 设置容器的高度 */

    background-color: white;        /* 设置容器的背景颜色 */
    padding-left: 10px;     /* 整个大容器向右移动 */
}


.x{             /* 设置最上方的横条 */
    border-top: 5px #666666 solid;  /* 设置容器的上边框，方便与红色边框重合 */
}


.title{         /* 为h2标题容器设置样式 */
    display: inline-block;  /* 为了使边框和文字的宽度一致，需要将h2转换成行内元素 */
    height: 40px;           /* 设置文字的高度 */
    border-top: 5px red solid;  /* 设置上边框样式 */
    margin-top: -5px;        /* 设置外上边框，和灰色横条重合 */
    text-decoration: none;  /* 去除下划线 */
}
.title a{       /*设置字体样式  */
    font-size: 20px;        /* 字体大小 */
    font-weight: bold;      /* 字体粗细 */
    color: black;           /* 字体颜色 */
}


.news-photo{        /* 为图片容器设置样式 */
    width: 300px;           /* 图片的宽度 */
    height: 150px;          /* 图片的高度 */
    margin-top: 25px;       /* 外边框上边距 */
    overflow: hidden;       /* 隐藏放大后边缘区域 */
}
.photo p{       /* 设置图片上的标题 */
    font-size: 16px;        /* 字体大小 */
    font-weight: bold;      /* 字体粗细 */
    color: white;           /* 字体颜色 */
    padding-left: 15px;       /* 内边框左边距 */
    margin-top: -25px;      /* 外边框上边距，向上移动 */
}
.photo img{     /* 设置图片过渡动画 */
    transition: all 0.6s;   /* 设置图片放大的时间 */
}
.photo img:hover{   /* 设置鼠标移入图片样式 */
    transform: scale(1.1); /* 鼠标移入，图片放大效果 */
}


.list-news{         /* 为新闻列表设置样式 */
    margin-top: 25px;       /* 外边框上边距 */
    /*padding-left: 15px;     !* 左内边距 *!*/
}
.list-news li{      /* 为内部的item设置样式 */
    margin-bottom: 17px     /* 设置每行的行距 */
}
.item a::before{     /* 设置项目符号 */
    content: '■ ';          /* 添加内容 */
    color: rgba(166, 183, 203, 0.69);         /* 设置颜色 */
}
.item a{            /* 为文字设置样式 */
    color: #666666;         /* 设置文字颜色 */
    font-size: 14px;        /* 设置文字大小 */
}
.item a:hover{      /* 设置鼠标移入状态样式 */
    color: red;
}
```

## 第二节：浮动：练习

### 1、导航条练习

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="../清除默认样式文件/reset.css">
    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="item">
        <div>
            <a class="HC" target="_blank" href="https://www.w3school.com.cn/h.asp">HTML/CSS</a>
        </div>
        <div>
            <a class="BS" target="_blank" href="https://www.w3school.com.cn/b.asp">Browser Side</a>
        </div>
        <div>
            <a class="SS" target="_blank" href="https://www.w3school.com.cn/s.asp">Server Side</a>
        </div>
        <div>
            <a class="P" target="_blank" href="https://www.w3school.com.cn/p.asp">Programming</a>
        </div>
        <div>
            <a class="XML" target="_blank" href="https://www.w3school.com.cn/x.asp">XML</a>
        </div>
        <div>
            <a class="WB" target="_blank" href="https://www.w3school.com.cn/w.asp">Web Building</a>
        </div>
        <div>
            <a class="R" target="_blank" href="https://www.w3school.com.cn/r.asp">Reference</a>
        </div>
    </div>

</body>
</html>
```

```css
.item{      /* 设置容器的背景样式 */
    width: 1210px;      /* 设置宽度 */
    height: 48px;       /* 设置高度 */
    background-color: #E8E7E3;  /* 背景颜色 */
    margin: 100px auto;       /* 导航栏垂直居中 */
}

a{         /* 设置文字样式 */
    display: block;         /* 转换成块元素 */
    float: left;            /* 将全部超链接设置为浮动样式 */
    line-height: 48px;      /* 设置导航类垂直居中 */
    color: #898888;         /* 设置字体颜色 */
    text-align: center;     /* 文字水平居中方式 */
}

a:hover{    /* 设置鼠标移入状态 */
    background-color: #3F3F3F;
    color: #CFCFCC;
}

/* 给每个超链接设置宽度和边框 */
.HC{
    width: 166px;
}
.BS{
    width: 191px;
}
.SS{
    width: 175px;
}
.P{
    width: 198px;
}
.XML{
    width: 113px;
}
.WB{
    width: 197px;
}
.R{
    width: 170px;
}
```

## 第三节：定位练习

### 1、京东轮播图

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="默认样式清除程序/reset.css">
    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <ul class="item">
        <li><a href="javascript:;">
            <img src="图片/0de73ae9f5d183fb.jpg.webp" alt=""></a>
        </li>
        <li><a href="javascript:;">
            <img src="图片/7b02a4310d81b515.jpg.webp" alt=""></a>
        </li>
        <li><a href="javascript:;">
            <img src="图片/93afe6da257fd357.jpg.webp" alt=""></a>
        </li>
        <li><a>
            <img src="图片/9d3a0b74239347d6.jpg.webp" alt=""></a>
        </li>
        <li><a href="javascript:;">
            <img src="图片/b6410900fe0ef5fa.jpg.webp" alt=""></a>
        </li>
        <li><a href="javascript:;">
            <img src="图片/q.jpg" alt=""></a>
        </li>
        <li><a href="javascript:;">
            <img src="图片/q%20(1).jpg" alt=""></a>
        </li>
        <li><a href="javascript:;">
            <img src="图片/q%20(2).jpg" alt=""></a>
        </li>

        <!-- 设置导航点 -->
        <div class="pointer">
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
        </div>

    </ul>

</body>
</html>
```

```css
img{                /* 设置图片大小 */
    width: 590px;
}

.item{              /* 设置图片样式 */
    width: 590px;
    height: 470px;
    margin: 100px auto;     /* 居中排列 */
    position: relative;     /* 开启相对行为，成为子元素的包含块 */
}

.item li{           /* 开启定位 */
    position: absolute;
}

.pointer{           /* 设置导航点位置和层级 */
    z-index: 9999;          /* 设置层级 */
    position: absolute;     /* 开启绝对定位 */
    bottom: 20px;           /* 设置距底边距 */
    left: 10px;             /* 设置右边距 */
}

.pointer a{         /* 设置导航点样式 */
    float: left;        /* 设置为浮动样式，使其脱离文档流 */
    width: 10px;
    height: 10px;
    background-color: rgba(42, 104, 255, 0.8);
    margin: 0 4px;      /* 添加导航条间隔 */
    border-radius: 50%; /* 设置为圆形 */
    border: 2px solid transparent;      /* transparent设置背景为透明 */
    /* 将背景颜色设置到内容区，边框和内边距不在有背景颜色 */
    background-clip: content-box;
}

.pointer a:hover{       /* 设置导航点鼠标移入样式 */
    background-color: #6f80ca;          /* 设置导航点颜色 */
    border: 2px rgba(100, 204, 255, 0.3) solid;      /* 设置边框 */
}
```

## 第四节：综合练习一

### 1、京东顶部导航条(未完成状态)

``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <!-- 引入重置样式表 -->
    <link rel="stylesheet" href="./默认样式清除程序/reset.css">
    <!-- 引入图标库 -->
    <link rel="stylesheet" href="./图标/iconfont.css">
    <!-- 引入css样式 -->
    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="outer">     <!-- 外部导航条 -->
        <div class="inner clearfix">     <!-- 内部导航条 -->

            <div class="one">        <!-- 左侧图标和文字 -->
                <div>
                    <p>安徽</p>     <!-- 设置地点位置 -->
                </div>
                <div class="div1"></div>    <!-- 下拉框 -->
            </div>

            <div class="two">        <!-- 右侧文字按钮 -->
                <p class="x">你好，请登录</p>
                <p class="y">免费注册</p>
                <span>|</span><p class="box1">我的订单</p>
                <span>|</span><p class="box2">我的京东</p>
                <span>|</span><p class="box3">京东会员</p>
                <span>|</span><p class="box4">企业采购</p>
                <span>|</span><p class="box5">客户服务</p>
                <span>|</span><p class="box6">网站导航</p>
                <span>|</span><p class="box7">手机京东</p>
            </div>

        </div>
    </div>

</body>
</html>
```

```css
/* 设置最外部容器样式 */
.outer{
    width: auto;                    /* 宽度沾满 */
    line-height: 30px;              /* 高度设置为30px */
    background-color: #E3E4E5;          /* 背景颜色 */
}

/* 设置内部容器样式 */
.inner{
    width: 1190px;          /* 设置宽度 */
    margin: 0 auto;         /* 内部容器样式居中对齐 */
}

/* 解决高度塌陷问题 */
.clearfix::before,
.clearfix::after{
    content: '';
    display: table;
    clear: both;
}

/* 设置全部文字的共同样式 */
.inner p{
    float: left;            /* 设置浮动 */
    font-size: 12px;        /* 设置字体大小 */
    line-height: 30px;      /* 使文字居中对齐 */
    color: #9C9C9C;         /* 文字颜色 */
}

/* 设置竖线分隔符样式 */
.inner span{
    float: left;            /* 设置浮动 */
    font-size: 2px;         /* 设置竖线大小 */
    color: #CCCCCC;         /* 设置竖线颜色 */
    line-height: 30px;      /* 使竖线居中对齐 */
    margin: auto 4px;       /* 设置竖线的左右边距 */
}

/* 设置one的样式 */
.one{
    float: left;            /* 左浮动 */
}
.one p::before{
    content: '\e61a';       /* 图标编号 */
    font: 14px 'iconfont', 'sans-serif';    /* 设置样式 */
    color: #f10215;         /* 图标颜色 */
    margin-left: 3px;      /* 设置图标右边距 */
}

/* 设置two的样式 */
.two{                       /* 定位two容器的位置 */
    float: right;           /* 右浮动 */
    text-align: center;     /* 使文字居中排列 */
}
.two .x{
    width: 72px;            /* 设置文字宽度 */
    margin-right: 8px;      /* 设置右边距 */
}
.two .y{
    width: 48px;            /* 设置文字宽度 */
    margin-right: 14px;      /* 设置右边距 */
}
.two p:hover{
    color: #EE3443;
}

/* 设置导航栏文字宽度和居中样式 */
.two .box1,
.two .box3,
.two .box7{
    width: 62px;            /* 设置文字宽度 */
}
.two .box2,
.two .box4,
.two .box5,
.two .box6{
    width: 77px;            /* 设置文字宽度 */
}

/* 设置文字常红状态 */
.two .box4,
.two .y{
    color: #F01829;
}

/* 设置箭头图标 */
.two .box2::after,
.two .box4::after,
.two .box5::after,
.two .box6::after{
    content: '\e612';           /* 设置图标编码 */
    font: 12px 'iconfont', 'sans-serif';    /* 设置样式 */
    color: #A3A3A3;             /* 设置图标颜色 */
    margin-left: 2px;           /* 设置图标左边距 */
}

/* 设置鼠标移入文字变红样式 */
.one p:hover,
.two .box1:hover,
.two .box2:hover,
.two .box3:hover{
    color: #F01829;
}

/* 设置鼠标移入背景颜色变白样式 */
.one p:hover,
.two .box2:hover,
.two .box4:hover,
.two .box5:hover,
.two .box6:hover{
    background-color: #FFFFFF;
}
```

### 2、京东顶部导航条（完成状态）

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <!-- 引入重置样式表 -->
    <link rel="stylesheet" href="默认样式清除程序/reset.css">
    <!-- 引入图标库 -->
    <link rel="stylesheet" href="图标/fontawesome图标库/css/all.css">
    <link rel="stylesheet" href="图标/iconfont.css">
    <!-- 引入css样式 -->
    <link rel="stylesheet" href="CSS测试.css">

</head>
<body>

    <!-- 创建外围容器 -->
    <div class="outer">
        <!-- 创建内部容器 -->
        <div class="inner">
            <!-- 左侧菜单 -->
            <div class="left">
                <div class="city">
                    <i class="fas fa-map-marker-alt"></i>
                    <a href="javascript:;">北京</a>
                </div>

                <!-- 放置城市列表的下拉框 -->
                <div class="city-list">
                    <p style="color: red; font-size: 20px">这里显示的是城市列表！</p>
                </div>
            </div>

            <!-- 右侧菜单 -->
            <ul class="right">
                <li>
                    <a href="javascript:;">你好，请登录</a>
                    <a class="highlight" href="javascript:;">免费注册</a>
                </li>

                <li class="line"></li>     <!-- 分割线 -->
                <li>
                    <a href="javascript:;" class="box1">我的订单</a>
                </li>

                <li class="line"></li>     <!-- 分割线 -->
                <li>
                    <a href="javascript:;" class="box2">我的京东</a>
                    <i class="fas fa-angle-down"></i>
                </li>

                <li class="line"></li>     <!-- 分割线 -->
                <li>
                    <a href="javascript:;" class="box3">京东会员</a>
                </li>

                <li class="line"></li>     <!-- 分割线 -->
                <li>
                    <a href="javascript:;" class="box4 highlight">企业采购</a>
                    <i class="fas fa-angle-down"></i>
                </li>

                <li class="line"></li>     <!-- 分割线 -->
                <li>
                    <span class="box5">客户服务</span>
                    <i class="fas fa-angle-down"></i>
                </li>

                <li class="line"></li>     <!-- 分割线 -->
                <li>
                    <span class="box6">网站导航</span>
                    <i class="fas fa-angle-down"></i>
                </li>

                <li class="line"></li>     <!-- 分割线 -->
                <li>
                    <span class="box3">手机京东</span>
                </li>
            </ul>
        </div>
    </div>

</body>
</html>
```

```css
/* 解决高度塌陷问题 */
.inner::before,
.inner::after{
    content: '';
    display: table;
    clear: both;
}

/* 设置字体样式 */
.inner a,
.inner i,
.inner span{
    font-size: 12px;
    text-decoration: none;
    color: #999999;
}

/* 设置外部容器样式 */
.outer{
    width: 100%;            /* 设置宽度 */
    line-height: 30px;      /* 跟随内容改变高度 */
    height: 30px;           /* 将高度定死 */
    background-color: #E3E4E5;
    border-bottom: 1px #dddddd solid;
}

/* 设置内部容器样式 */
.inner{
    width: 1190px;          /* 固定宽度 */
    margin: 0 auto;         /* 水平居中 */
    position: relative;
}

/* 设置left的位置 */
.left{
    float: left;
}

/* 设置right的位置 */
.right{
    float: right;
}

/* 设置li的浮动样式 */
.right li{
    float: left;
}

/* 设置地点图标样式 */
.city i{
    font-size: 14px;
    color: #f10215;
}

/* 设置城市列表的下拉样式 */
.inner .city-list{
    display: none;          /* 初始状态为隐藏 */
    width: 320px;
    height: 430px;
    background-color: white;
    border: 1px solid rgb(204, 204, 204);
    /* 设置绝对定位，使其不占据页面的位置，防止把高度撑开 */
    position: absolute;
    top: 31px;
}

/* 设置鼠标移入，显示下拉框 */
.inner:hover .city-list{
    display: block;
}

/* 设置鼠标移入背景变白的效果 */
.inner:hover .city{
    background-color: white;
    border: 1px solid rgb(204, 204, 204);
    border-bottom: none;
    padding-bottom: 1px;
}

/* 设置city的效果 */
.city{
    border: 1px solid transparent;      /* 将边框颜色改为透明样式 */
    border-bottom: none;
    padding: 0 10px;
    position: relative;
    z-index: 1;
}

/* 设置鼠标移入样式，以及部分标签高亮样式 */
.inner a:hover,
.inner a.highlight{
    color: #f10215;
}

/* 设置分割线 */
.line{
    width: 1px;
    height: 10px;
    background-color: #999999;
    margin: 10px 12px 0;
}
```

## 第五节：背景：练习

### 1、渐变导航条和鼠标不同状态图标变化

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box1"></div>
    <br><br>

    <a href="javascript:;"></a>

</body>
</html>
```

```css
/* 渐变导航栏展示 */
.box1{
    width: 990px;
    height: 520px;
    margin: 0 auto;

    /* 普通写法 */
    /*
    background-image: url("./渐变图片/渐变背景图片.jpg");     导入背景图片
    background-repeat: repeat-x;        设置图片重复方式
    */

    /* 简写写法 */
    background: url("./渐变图片/渐变背景图片.jpg") repeat-x;
}

/* 图标不同状态展示 */
a:link{     /* 待点击时图标状态 */
    display: block;
    width: 208px;
    height: 72px;
    background-image: url("./不同状态图标/待点击图标.jpg");
}
a:hover{    /* 鼠标移入图标状态 */
    background-image: url("./不同状态图标/点击中图标.jpg");
}
a:active{   /* 点击完成时图标状态 */
    background-image: url("./不同状态图标/完成点击图标.jpg");
}
```

### 2、不同状态图标解决闪烁问题（雪碧图）

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <a href="javascript:;"></a>

</body>
</html>
```

```css
/*
    - 在点击图片时，若是存在多个图片，由于缓存问题，会出现闪烁问题，这时需要将多个图片拼凑成一个图片，一次性缓存。通过background-position移动图片位置，此技术叫做CSS-Sprite（雪碧图）。

    - 雪碧图的使用方法
        - 先确定要使用的图片
        - 测量图片的大小
        - 根据测量结果创建一个元素
        - 将雪碧图设置为元素的背景图片
        - 设置偏移量（background-position），以便显示正确的图片
*/

a:link{         /* 未点击图标时 */
    display: block;     /* 设置成块元素，用于显示图片 */
    width: 208px;
    height: 72px;
    background-image: url("./练习图片/综合图片.gif");
}

a:hover{        /* 点击图标时 */
    background-position: -208px 72px;       /* 通过移动图片位置，解决加载缓存出现闪烁的情况 */
}

a:active{        /* 点击图标完成时 */
    background-position: -416px 72px;       /* 通过移动图片位置，解决加载缓存出现闪烁的情况 */
}
```

## 第六节：综合练习二

### 1、电影卡片练习

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./默认样式清除程序/reset.css">
    <link rel="stylesheet" href="./图标/iconfont.css">
    <link rel="stylesheet" href="CSS测试.css">

</head>
<body>

    <div class="item clearfix">

        <div class="one">

        </div>

        <div class="two">
            <h2>Animation films</h2>
            <i>Animations</i>
            <p>Lorem lpsum is simply dummy text of the printing & typesetting industry.</p>
        </div>

        <div class="three">
            <i class="x"></i>
            <i class="y"></i>
            <i class="z"></i>
        </div>

    </div>

</body>
</html>
```

```css
/* 设置外部容器样式 */
.item{
    width: 250px;
    margin: 30px auto;
    box-shadow: 0 0 10px rgba(177, 177, 177, .5);
}
/* 解决高度塌陷，高度根据内容调整 */
.clearfix::before,
.clearfix::after{
    content: '';
    display: table;
    clear: both;
}


/* 设置图片 */
.one{
    width: 250px;
    height: 140px;
    background-image: url("./综合练习二图片/1.jpg");
    border-bottom: 1px rgba(177, 177, 177, .5) solid;
    vertical-align: bottom;     /* 解决图片与边框之间的白边问题 */
}

/* 设置中间文字框 */
.two h2{
    color: #A9AAA9;
    margin: 12px;
}
.two i{
    font-size: 15px;
    color: #BABBB9;
}
.two i::before{
    content: '\e607';
    font-family: 'iconfont';
    color: #BABBB9;
    font-size: 18px;
    margin: 0 5px 0 10px;
}
.two p{
    font-size: 15px;
    color: #BABBB9;
    margin: 24px 15px;
}

/* 设置底部图案 */
.three{
    float: none;
    border-top: 2px rgba(177, 177, 177, .2) solid;
}
.x{
    float: left;
    margin: 8px 0 9px 12px;
}
.y{
    float: left;
        margin: 8px 0;
}
.x::before,
.x::after{
    content: '\e632';
    font-family: 'iconfont';
    color: #B8C13C;
    font-size: 20px;
}
.y::before,
.y::after{
    content: '\e632';
    font-family: 'iconfont';
    color: #DBDCDB;
    font-size: 20px;
}
.z{
    float: right;
    margin: 9px 30px;
}
.z::before{
    content: '\e61f';
    font-family: 'iconfont';
    color: #DBDCDB;
    font-size: 20px;
}
```

## 第七节：综合练习三

### 1、复仇者联盟介绍

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="默认样式清除程序/reset.css">
    <link rel="stylesheet" href="CSS测试.css">

</head>
<body>

    <div class="item">复仇者联盟</div>
    <div class="outer">     <!-- 设置外部区域 -->
        <div class="inner">     <!-- 设置内部区域 -->
            <div class="img img1">
                <a target="_blank" href="https://baike.baidu.com/item/%E9%B9%B0%E7%9C%BC/15107237?fr=aladdin">
                    <img src="展示图片/鹰眼.jpg" alt="鹰眼">
                </a>
                <div class="box box1">我是鹰眼，我是一名神射手。</div>
            </div>
            <div class="img img2">
                <a target="_blank" href="https://baike.baidu.com/item/%E7%BB%BF%E5%B7%A8%E4%BA%BA/65931">
                    <img src="展示图片/浩克.jpg" alt="浩克">
                </a>
                <div class="box box2">我是浩克，我力大无比。</div>
            </div>
            <div class="img img3">
                <a target="_blank" href="https://baike.baidu.com/item/%E9%92%A2%E9%93%81%E4%BE%A0/303">
                    <img src="展示图片/钢铁侠.jpg" alt="gtx">
                </a>
                <div class="box box3">我是钢铁侠，我创造了很多钢铁战衣。</div>
            </div>
            <div class="img img4">
                <a target="_blank" href="https://baike.baidu.com/item/%E7%BE%8E%E5%9B%BD%E9%98%9F%E9%95%BF/3472">
                    <img src="展示图片/美国队长.jpg" alt="美国队长">
                </a>
                <div class="box box4">我是美国队长，我将用盾牌守护和平。</div>
            </div>
            <div class="img img5">
                <a target="_blank" href="https://baike.baidu.com/item/%E9%9B%B7%E7%A5%9E/8321769">
                    <img src="展示图片/雷神.jpg" alt="雷神">
                </a>
                <div class="box box5">我是雷神，我拥有控制雷电的力量。</div>
            </div>
            <div class="img img6">
                <a target="_blank" href="https://baike.baidu.com/item/%E9%BB%91%E5%AF%A1%E5%A6%87/19751743">
                    <img src="展示图片/黑寡妇.jpg" alt="黑寡妇">
                </a>
                <div class="box box6">我是黑寡妇，我是一名格斗高手。</div>
            </div>
        </div>
    </div>

</body>
</html>
```

```css
/*!* 解决高度塌陷和重贴问题 *!*/
/*.outer::before,*/
/*.outer::after{*/
/*    content: '';*/
/*    display: table;*/
/*    clear: both;*/
/*}*/
.item{
    width: 500px;
    height: 50px;
    font-size: 50px;
    color: red;
    text-align: center;
    margin: 20px auto;
    padding: 10px;
    border: 15px solid;
    border-color: red yellow;
}

/* 设置外部区域位置 */
.outer{
    width: 820px;
    box-shadow: 0 0 15px rgba(0, 0, 0, .8);    /* 设置阴影边框 */
    margin: 40px auto;
}

/* 设置内部区域位置 */
.inner{
    padding: 20px 20px 80px 20px;       /* 设置内边距 */
    overflow: hidden;
    position: relative;                 /* 父元素开启相对定位 */
}

/* 设置文字出现的共同样式 */
.inner .box{
    width: 400px;
    font: 20px "Microsoft YaHei";
    text-align: center;     /* 文字居中 */
    line-height: 40px;      /* 高度居中 */
    display: none;          /* 设置初始为隐藏状态 */
    border-radius: 15px;    /* 设置文字框圆角样式 */
    position: absolute;     /* 设置绝对定位，使其不占据页面位置 */
    bottom: 20px;           /* 设置偏移量 */
    left: 210px;
    right: 210px;
    /*margin: auto;*/
}

/* 设置图片样式 */
img{
    width: 120px;
    float: left;
    margin: 5px;
    transition: all 0.6s;   /* 设置图片放大的时间 */
}

/* 设置鼠标移入，图片放大的过渡动画 */
img:hover{
    transform: scale(1.1); /* 鼠标移入，图片放大效果 */
}

/* 设置鼠标移入，显示文字效果 */
.img:hover .box{
    display: block;
}

/* 设置具体的文字出现样式 */
.box1{
    background-color: orange;
}

.box2{
    background-color: #008000;
}

.box3{
    background-color: red;
}

.box4{
    background-color: #497cff;
}

.box5{
    background-color: yellow;
}

.box6{
    background-color: #adb1b1;
}
```

## 第八节：小米主页项目搭建

> 涉及的其他知识：
>
> 1. 设置网站的图标（在head栏提及）
> 2. 提升网站的访问速度（主要是删除对网页展示样式无用的代码）
>    1. 删除注释
>    2. 删除换行和空格
>    3. 总的来说于代码无关的东西能删就删

```html
<!-- index.html -->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>小米主页</title>

    <!-- 引入重置样式表 -->
    <link rel="stylesheet" href="./CSS文件/reset.css">
    <!-- 引入公共样式表 -->
    <link rel="stylesheet" href="./CSS文件/base.css">
    <!-- 引入页面样式表 -->
    <link rel="stylesheet" href="./CSS文件/index.css">
    <!-- 引入图标字体库 -->
    <link rel="stylesheet" href="./fontawesome图标库/css/all.css">
    <link rel="stylesheet" href="./iconfont图标库/iconfont.css">

    <!--
        设置网站的图标（在标题栏和收藏栏）
            - 网站的图片一般都储存在网站的根目录下，名字一般都是 favicon.ico
    -->
    <link rel="icon" href="./image/favicon.ico">

</head>
<body>

    <!-- 顶部导航条 -->
    <!-- 创建顶部导航条的外部容器 -->
    <div class="top-bar-wrapper">
        <!-- 创建内部容器 -->
        <div class="top-bar w clearfix">
            <!-- 右侧导航 -->
            <ul class="service">
                <li><a href="javascript:;">小米商城</a></li>
                <li class="line">|</li>
                <li><a href="javascript:;">MIUI</a></li>
                <li class="line">|</li>
                <li><a href="javascript:;">loT</a></li>
                <li class="line">|</li>
                <li><a href="javascript:;">云服务</a></li>
                <li class="line">|</li>
                <li><a href="javascript:;">天星数科</a></li>
                <li class="line">|</li>
                <li><a href="javascript:;">有品</a></li>
                <li class="line">|</li>
                <li><a href="javascript:;">小爱开放平台</a></li>
                <li class="line">|</li>
                <li><a href="javascript:;">企业团购</a></li>
                <li class="line">|</li>
                <li><a href="javascript:;">资质证照</a></li>
                <li class="line">|</li>
                <li><a href="javascript:;">协议规则</a></li>
                <li class="line">|</li>
                <li class="app-wrapper">
                    <a class="app" href="javascript:;">
                        下载app
                        <!-- 添加下拉二维码弹出层 -->
                        <div class="qrcode">
                            <img src="./image/二维码.png" alt="二维码">
                            <span>小米商城APP</span>
                        </div>
                    </a>
                </li>
                <li class="line">|</li>
                <li><a href="javascript:;">智能生活</a></li>
                <li class="line">|</li>
                <li><a href="javascript:;">Select Location</a></li>
            </ul>

            <!-- 购物车 -->
            <ul class="shout-cart">
                <li>
                    <a href="javascript:;">
                        <i class="fas fa-shopping-cart"></i>
                        购物车（0）
                        <div class="shopping-cart-list">
                            <p>目前没有你所选购的商品！</p>
                        </div>
                    </a>
                </li>
            </ul>

            <!-- 用户注册 -->
            <ul class="user-info">
                <li><a href="javascript:;">登录</a></li>
                <li class="line">|</li>
                <li><a href="javascript:;">注册</a></li>
                <li class="line">|</li>
                <li><a href="javascript:;">消息通知</a></li>
            </ul>

        </div>
    </div>

    <!-- 头部容器 -->
    <div class="header-wrapper">
        <div class="header w clearfix">
            <!-- 创建一个logo -->
            <h1 class="logo">
                <a href="javascript:;"></a>
            </h1>

            <!-- 创建中间导航条容器 -->
            <div class="nav-wrapper">
                <!-- 创建导航条 -->
                <ul class="nav">
                    <li class="all-goods-wrapper">
                        <a class="all-goods" href="javascript:;">全部商品分类</a>

                        <!-- 创建一个左侧导航栏 -->
                        <ul class="left-menu">
                            <li>
                                <a href="javascript:;">
                                    手机 电话卡
                                    <i class="fas fa-angle-right"></i>
                                </a>
                            </li>
                            <li>
                                <a href="javascript:;">
                                    电视 盒子
                                    <i class="fas fa-angle-right"></i>
                                </a>
                            </li>
                            <li>
                                <a href="javascript:;">
                                    笔记本 显示器
                                    <i class="fas fa-angle-right"></i></a>
                            </li>
                            <li>
                                <a href="javascript:;">
                                    家电 插线
                                    <i class="fas fa-angle-right"></i>
                                </a>
                            </li>
                            <li>
                                <a href="javascript:;">
                                    智能 路由器
                                    <i class="fas fa-angle-right"></i>
                                </a>
                            </li>
                            <li>
                                <a href="javascript:;">
                                    电源 配件
                                    <i class="fas fa-angle-right"></i>
                                </a>
                            </li>
                            <li>
                                <a href="javascript:;">
                                    健康 儿童
                                    <i class="fas fa-angle-right"></i>
                                </a>
                            </li>
                            <li>
                                <a href="javascript:;">
                                    耳机 音箱
                                    <i class="fas fa-angle-right"></i>
                                </a>
                            </li>
                            <li>
                                <a href="javascript:;">
                                    生活 箱包
                                    <i class="fas fa-angle-right"></i>
                                </a>
                            </li>
                        </ul>
                    </li>
                    <li class="show-goods"><a href="javascript:;">小米手机</a></li>
                    <li class="show-goods"><a href="javascript:;">Redmi红米</a></li>
                    <li class="show-goods"><a href="javascript:;">电视</a></li>
                    <li class="show-goods"><a href="javascript:;">笔记本</a></li>
                    <li class="show-goods"><a href="javascript:;">家电</a></li>
                    <li class="show-goods"><a href="javascript:;">路由器</a></li>
                    <li class="show-goods"><a href="javascript:;">智能硬件</a></li>
                    <li><a href="javascript:;">服务</a></li>
                    <li><a href="javascript:;">社区</a></li>
                    <!-- 创建弹出层 -->
                    <div class="goods-info"></div>
                </ul>
            </div>

            <!-- 创建搜索框容器 -->
            <div class="search-wrapper">
                <form class="search" action="#">
                    <input class="search-inp" type="text">
                    <button class="search-btn">
                        <i class="fas fa-search"></i>
                    </button>
                </form>
            </div>
        </div>

    </div>

    <!-- 创建banner容器 -->
    <div class="banner-wrapper">
        <div class="banner w">
            <!-- 创建图片容器 -->
            <ul class="img-list">
                <li>
                    <a href="javascript:;">
                        <img src="./image/轮播图/2.webp" alt="">
                    </a>
                </li>
                <li>
                    <a href="javascript:;">
                        <img src="./image/轮播图/3.webp" alt="">
                    </a>
                </li>
                <li>
                    <a href="javascript:;">
                        <img src="./image/轮播图/4.webp" alt="">
                    </a>
                </li>
                <li>
                    <a href="javascript:;">
                        <img src="./image/轮播图/5.webp" alt="">
                    </a>
                </li>
            </ul>

            <!-- 创建导航点容器 -->
            <div class="pointer">
                <a class="active" href="javascript:;"></a>      <!-- 设置默认导航点 -->
                <a href="javascript:;"></a>
                <a href="javascript:;"></a>
                <a href="javascript:;"></a>
            </div>

            <!-- 创建图片左右两侧小箭头样式 -->
            <div class="prev-next">
                <a class="prev" href="javascript:;"></a>    <!-- 切换到上一张 -->
                <a class="next" href="javascript:;"></a>    <!-- 切换到下一张 -->
            </div>

        </div>


    </div>

    <!-- 创建右侧工具条 -->
    <div class="right-tools">
        <div class="tools">
            <i class="iconfont">&#xe613;</i>
            <i class="iconfont">&#xe611;</i>
            <i class="iconfont">&#xe687;</i>
            <i class="iconfont">&#xe606;</i>
            <i class="iconfont">&#xe600;</i>
        </div>
    </div>

    <!-- 底部广告栏 -->
    <div class="bottom-wrapper w">
        <!-- 创建左侧超链接栏 -->
        <div class="left-link">
            <a class="link-1" href="Javascript:;">小米秒杀</a>
            <a class="link-2" href="Javascript:;">企业团购</a>
            <a class="link-3" href="Javascript:;">F码通道</a>
            <a class="link-4" href="Javascript:;">米粉卡</a>
            <a class="link-5" href="Javascript:;">以旧换新</a>
            <a class="link-6" href="Javascript:;">话费充值</a>
        </div>

        <!-- 创建右侧广告照片栏 -->
        <div class="right-link">
            <a href="Javascript:;">
                <img src="./image/底部广告图片/1.jpg" alt="">
            </a>
            <a href="Javascript:;">
                <img src="./image/底部广告图片/2.jpg" alt="">
            </a>
            <a href="Javascript:;">
                <img src="./image/底部广告图片/3.jpg" alt="">
            </a>
        </div>
    </div>

</body>
</html>
```

```css
/* index.css */

/* 顶部导航条容器 */
.top-bar-wrapper{
    width: 100%;
    height: 40px;
    line-height: 40px;
    background-color: #333333;
}

/* 设置超链接的颜色 */
.top-bar a{
    font-size: 12px;
    color: #b0b0b0;
    display: block;
}

/* 设置鼠标移入效果 */
.top-bar a:hover{
    color: #FFFFFF;
}

/* 设置分割线样式 */
.top-bar .line{
    color: #424242;
    font-size: 12px;
    margin: 0 8px;
}

/* 设置左侧导航栏 */
.service, .top-bar li{
    float: left;
}

/* 为app开启相对定位 */
.app{
    position: relative;
}

/* 设置鼠标移入，出现二维码框 */
.app:hover .qrcode{
    z-index: 9999;
    background-color: white;
    display: block;
    height: 148px;
}
.app:hover::after{
    z-index: 9999;
    display: block;
    height: 148px;
}

/* 设置app下的小三角 */
.app::after{
    display: none;              /* 初始状态设置为隐藏 */
    width: 0;
    height: 0;
    content: '';
    position: absolute;         /* 设置绝对定位 */
    bottom: 0;                  /* 设置偏移量 */
    left: 0;
    right: 0;
    margin: auto;
    border: 10px solid transparent;         /* 设置四个方向的边框 */
    border-top: none;           /* 去除上边框 */
    border-bottom-color: white;
}

/* 设置下载app的下拉框样式 */
.app .qrcode{
    z-index: 9999;
    /*display: none;              !* 初始状态设置为隐藏 *!*/
    width: 124px;
    /*height: 148px;*/

    /* 除display外第二种隐藏方式 */
    height: 0;
    overflow: hidden;

    position: absolute;
    left: -40px;
    line-height: 1;
    text-align: center;
    box-shadow: 0 0 10px rgba(0, 0, 0, .3);

    /* transition：用于为样式设置过渡动画效果 */
    transition: height 0.3s;        /* 该标签的高度出现动画为0.3s */
}

/* 设置app二维码图片样式 */
.app .qrcode img{
    width: 90px;
    margin: 18px 17px 12px;
}

/* 设置app二维码下方文字样式 */
.app .qrcode span{
    color: black;
    font-size: 14px;
}

/* 设置右侧导航栏 */
.shout-cart, .user-info{
    float: right;
}

/* 设置购物车样式 */
.shout-cart a{
    width: 120px;
    background-color: #424242;
    text-align: center;
    margin-left: 26px;
    position: relative;
}

/* 设置鼠标移入，购物车出现下拉框 */
.shout-cart:hover a,
.shout-cart:hover .shopping-cart-list{
    color: #FF6700;             /* 文字颜色 */
    background-color: white;    /* 背景颜色 */
    display: block;
    height: 100px;              /* 设置下拉框高度 */
}

/* 设置购物车下拉框内文字的样式 */
.shopping-cart-list p{
    font-size: 14px;
    color: black;
    line-height: 100px;
    text-align: center;
}

/* 设置购物车下拉框样式 */
.shopping-cart-list{
    z-index: 9999;
    /*display: none;              !* 设置初始状态为隐藏 *!*/
    float: none;
    width: 316px;
    height: 0;                  /* 设置初始状态为隐藏 */
    overflow: hidden;
    background-color: white;
    position: absolute;         /* 开启绝对定位 */
    top: 40px;
    right: 0;
    box-shadow: 0 5px 5px rgba(0, 0, 0, 0.3);
    transition: height 0.3s;    /* 添加过渡动画 */
}



/* 头部容器 */
.header{
    height: 100px;
    /*position: absolute;*/
    /*top: 0;*/
    /*left: 0;*/
    /*right: 0;*/
    margin: 0 auto;             /* 设置居中排列 */
}

/* 设置参考定位 */
.header-wrapper{
    position: relative;
}

/* 设置logo位置 */
.header .logo{
    float: left;
    /*line-height: 100px;*/
    margin-top: 22px;
    /* 固定容器的宽度和高度 */
    width: 56px;
    height: 56px;
    /*position: relative;*/
}

/* 设置logo样式 */
.header .logo a{
    display: block;
    width: 56px;
    height: 56px;
    background-image: url("../image/小米logo.png");
    transition: background-position 0.3s;       /* 设置过渡动画 */
}

/* 设置鼠标移入展示雪碧图过渡动画效果 */
a:hover{
    background-position: 56px 0;        /* 设置雪碧图出现位置 */
}


/* 设置中间导航栏属性 */
.header .nav-wrapper{
    float: left;
    margin-left: 7px;
}

/* 设置导航条 */
.header .nav{
    height: 100px;
    line-height: 100px;
    padding-left: 58px;
}

/* 设置文字样式 */
.nav-wrapper li a{
    font-size: 16px;
    margin-left: 20px;
    display: block;                     /* 转换成块元素，方便鼠标选择范围 */
}

/* 设置鼠标移入样式 */
.nav-wrapper li a:hover{
    color: #FF6700;
}

/* 隐藏全部商品文字 */
.all-goods{
    visibility: hidden;
}

/* 设置弹出层样式 */
.nav .goods-info{
    z-index: 9999;
    /*height: 228px;*/
    height: 0;                  /* 初始化隐藏图层 */
    overflow: hidden;
    position: absolute;
    top: 100px;
    left: 0;
    width: 100%;
    transition: height 0.3s;
}

/* 设置鼠标移入显示弹出层 */
/* 兄弟选择器，选择后面全部的兄弟元素 */
/* 分组选择器，挑选出禁止出现该样式的元素 */
/* 第一种写法 */
/*.nav li:not(:first-of-type):not(:nth-child(9)):not(:nth-child(10)):hover ~ .goods-info,*/
/* 第二种写法 */
.nav .show-goods:hover ~ .goods-info,
.goods-info:hover{
    height: 228px;
    box-shadow: 0 3px 8px rgba(0, 0, 0, 0.3);
    border-top: 1px solid rgb(224, 224, 224);
    background-color: #FF6700;
}


/* 设置左侧导航栏的各种样式 */
/* 设置导航条里子元素的li浮动，其他后代元素不浮动 */
.nav > li{
    float: left;
}

/* 设置父元素，开启相对定位 */
.all-goods-wrapper{
    position: relative;
}

/* 设置全部商品分类的li标签样式，防止被别的地方设置的样式覆盖 */
.all-goods-wrapper li a{
    margin-left: 0;
}

/* 设置左侧导航条的样式 */
.left-menu{
    z-index: 999;
    width: 234px;
    height: 380px;
    background-color: rgba(0, 0, 0, 0.6);       /* 设置一个透明的背景 */
    position: absolute;                 /* 开启绝对定位 */
    left: -121px;
    line-height: 1;                     /* 设置一倍行距 */
    padding: 20px 0;                    /* 设置上下内边距 */
}

.left-menu li{
    margin: 0;
}

/* 设置超链接样式 */
ul.left-menu li a{
    display: block;                     /* 转换成块元素，方便鼠标选择范围 */
    height: 42px;                       /* 设置每个超链接的行高 */
    line-height: 42px;                  /* 使每个超链接居中 */
    color: white;                       /* 设置文字颜色 */
    padding: 0 30px;                    /* 设置左右内边框边距 */
}

/* 设置右侧小箭头样式 */
.left-menu a i{
    float: right;                       /* 设置浮动 */
    line-height: 42px;                  /* 垂直居中排列 */
}

/* 设置鼠标移入特效 */
ul.left-menu li a:hover{
    color: white;
    background-color: #FF6700;
}


/* 设置搜索框容器 */
.search-wrapper{
    width: 296px;                   /* 设置搜索框的大小 */
    height: 50px;
    float: right;                   /* 设置浮动，脱离文档流 */
    margin-top: 25px;               /* 设置外边距，确定整个元素位置 */
}

/* 设置搜索文字框样式 */
.search-wrapper .search-inp{
    float: left;                    /* 设置浮动，脱离文档流 */
    width: 220px;
    height: 48px;
    padding: 0 10px;                /* 设置内边距，确定元素位置 */
    font-size: 16px;                /* 设置字体大小 */
    border: 1px rgb(224, 224, 224) solid;   /* 设置边框 */
    outline: none;                  /* 去除原本文字搜索框带有的轮廓线 */
}

/* 设置按钮框样式 */
.search-wrapper .search-btn{
    float: left;                    /* 设置浮动，脱离文档流 */
    padding: 0;                     /* 设置内边距，删除多余边框距离产生的小差距 */
    width: 52px;
    height: 50px;
    background-color: #FFFFFF;      /* 设置背景颜色 */
    color: #616161;                 /* 设置字体颜色 */
    font-size: 20px;                /* 设置字体大小 */
    border: 1px rgb(224, 224, 224) solid;   /* 设置边框 */
    border-left: none;                      /* 取消左边框，防止重合 */
}

/* 设置鼠标移入，按钮框变化样式 */
.search-wrapper .search-btn:hover{
    border: none;                   /* 取消边框，使背景颜色撑满元素块 */
    color: white;                   /* 图标颜色 */
    background-color: #FF6700;      /* 背景颜色 */
}

/* 设置input获取焦点后样式 */
/* 设置搜索框及其兄弟元素按钮框的样式 */
.search-wrapper .search-inp:focus,
.search-wrapper .search-inp:focus + button{
    border-color: #FF6700;
}


/* 设置banner样式 */
/* 为banner开启相对定位，方便下面元素进行定位 */
.banner{
    position: relative;
    height: 420px;                      /* 顶死高度，防止塌陷和子元素的定位 */
}

/* 为li标签设置绝对定位 */
.banner .img-list li{
    position: absolute;
}

/* 设置图片样式 */
.banner img{
    width: 100%;                        /* 设置图片宽度 */
    height: 420px;                      /* 设置图片大高度 */
    vertical-align: top;                /* 设置图片之间没有距离 */
}

/* 设置四个导航点的绝对定位 */
.pointer{
    position: absolute;
    bottom: 22px;
    right: 35px;
}

/* 设置四个导航点的a标签样式 */
.pointer a{
    float: left;                        /* 设置导航点浮动 */
    width: 6px;                         /* 设置导航点的宽度 */
    height: 6px;                        /* 设置导航点的高度 */
    background-color: rgba(0, 0, 0, 0.4);           /* 设置导航点颜色 */
    border: 2px solid rgba(255, 255, 255, 0.4);     /* 设置边框 */
    border-radius: 50%;                 /* 设置圆角 */
    margin-left: 6px;                   /* 设置导航点之间的间距 */

}

/* 设置鼠标移入，导航点变化 */
.pointer a:hover,
/* 设置默认导航点样式 */
.pointer a.active{
    border-color: rgba(0, 0, 0, 0.4);               /* 边框变化颜色 */
    background-color: rgba(255, 255, 255, 0.4);     /* 导航点变化颜色 */
}

/* 设置图片右侧的小箭头样式（雪碧图） */
.prev-next .prev{
    width: 50px;                            /* 设置图片显示宽度 */
    height: 88px;                           /* 设置图片显示高度 */
    background-image: url("../image/左右箭头/左箭头.png");     /* 引入图片 */
    background-position: -50px 0;            /* 设置需要展示图片的定位 */
    background-repeat: no-repeat;           /* 设置图片为非平铺展示 */
    position: absolute;                     /* 开启绝对定位 */
    top: 0;                                 /* 设置偏移量 */
    bottom: 0;
    margin: auto;                           /* 设置水平居中 */
    right: 0;                               /* 设置右边距 */
}

/* 设置图片左侧的小箭头样式（雪碧图） */
.prev-next .next{
    width: 50px;                            /* 设置图片显示宽度 */
    height: 88px;                           /* 设置图片显示高度 */
    background-image: url("../image/左右箭头/右箭头.png");     /* 引入图片 */
    background-position: -50px 0;            /* 设置需要展示图片的定位 */
    background-repeat: no-repeat;           /* 设置图片为非平铺展示 */
    position: absolute;                     /* 开启绝对定位 */
    top: 0;                                 /* 设置偏移量 */
    bottom: 0;
    margin: auto;                           /* 设置水平居中 */
    left: 234px;                               /* 设置右边距 */
}

/* 设置左右两侧图片鼠标移入变换样式 */
.prev-next .prev:hover,
.prev-next .next:hover{
    background-position: 0 0;               /* 设置图片定位 */
}


/* 创建右侧工具条 */
.right-tools{
    width: 60px;                            /* 设置总体宽度 */
    height: 300px;                          /* 设置总体高度 */
    position: fixed;                        /* 开启固定定位，相对于视口定位，不会随滚动条滚动而滚动 */
    top: 180px;                             /*设置距离顶部距离，相对于视口，而不是全局 */
    /* 下面两个结合使用 */
    right: 50%;                             /* 将right值设置为视口宽度的50% */
    margin-right: -673px;                   /* 一定为负值，中间宽度的一半（613）+本身宽度（60） */
}

/* 设置每个标签的样式 */
.right-tools i{
    display: block;                         /* 设置每个标签为块元素 */
    width: 60px;                            /* 设置每个框的宽度 */
    height: 60px;                           /* 设置每个框的高度 */
    border: 1px solid rgb(245, 245, 245);   /* 设置边框样式 */
}

/* 设置图标的共同样式 */
i.iconfont{
    font-size: 40px;                        /* 设置图标大小 */
    color: #999999;                         /* 设置图标颜色 */
    text-align: center;                     /* 设置图标水平居中 */
}


/* 设置底部广告栏样式 */
.bottom-wrapper{
    margin-top: 15px;                       /* 设置上边距 */
    height: 170px;                          /* 设置高度 */
}

/* 设置左侧超链接栏样式 */
.bottom-wrapper .left-link{
    float: left;                            /* 设置浮动 */
    width: 232px;                           /* 设置宽度 */
    height: 168px;                          /* 设置高度同父元素一致 */
    background-color: #5F5750;              /* 设置背景颜色 */
    margin-right: 2px;                      /* 设置右边距 */
    padding-top: 2px;                       /* 方便设置边框 */
    padding-left: 2px;
}

/* 设置超链接共同样式 */
.bottom-wrapper .left-link a{
    width: 76px;                            /* 设置元素框宽度 */
    height: 84px;                           /* 设置元素框高度 */
    display: block;                         /* 转换成款元素 */
    float: left;                            /* 设置浮动 */
    font-size: 16px;                        /* 设置字体大小 */
    color: #adb1b1;                         /* 设置文字颜色 */
    line-height: 83px;                      /* 设置垂直居中 */
    text-align: center;                     /* 设置水平居中 */
    position: relative;                     /* 开启相对定位，方便下面设置边框 */
}

/* 用伪元素选择器设置类似边框 */
.bottom-wrapper .left-link a::before{
    content: '';                            /* 设置需要填写的内容，此处为空 */
    position: absolute;                     /* 开启相对定位 */
    top: 0;
    left: 0;
    right: 0;
    margin: 0 auto;
    width: 64px;                            /* 设置宽度 */
    height: 1px;                            /* 设置高度 */
    background-color: rgba(177, 177, 177, 0.3);     /* 设置颜色和透明度 */
}
.bottom-wrapper .left-link a::after{
    content: '';
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    margin: auto 0;
    width: 1px;
    height: 70px;
    background-color: rgba(177, 177, 177, 0.3);
}

/* 设置鼠标移入变换样式 */
.bottom-wrapper .left-link a:hover{
    color: #FFFFFF;                         /* 设置文字变换颜色 */
    transition: color 0.3s;                 /* 设置变换速度 */
}

/* 设置右侧广告照片栏样式 */
.bottom-wrapper .right-link a img{
    width: 316px;                           /* 设置图片宽度 */
    float: left;                            /* 设置图片浮动样式 */
    margin-left: 14px;                      /* 设置左边距 */
}
```

```css
/* base.css */
/* 公共样式文件 */

/* 解决高度塌陷和重叠问题 */
.clearfix::before,
.clearfix::after{
    content: '';
    display: table;
    clear: both;
}

/* 去除所有超链接的下划线 */
a{
    text-decoration: none;
    color: #333333;
}

/* 设置公共字体样式 */
body{
    font: 14px/1.5 Helvetica Neue,Helvetica,Arial,Microsoft Yahei,Hiragino Sans GB,Heiti SC,WenQuanYi Micro Hei,sans-serif;
    color: #333333;
    min-width: 1226px;          /* 设置最小屏幕宽度 */
}

/* 设置一个类，用来表示屏幕的宽度 */
.w{
    width: 1226px;              /* 固定容器宽度 */
    margin: 0 auto;             /* 设置容器居中 */
}
```

## 第九节：过渡动画：练习

### 1、过渡动画练习

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box"></div>

</body>
</html>
```

```css
.box{
    height: 700px;
    width: 300px;               /* 总宽度是1200px，每个子图是300px */
    margin: 0 auto;             /* 设置图片居中 */
    background-image: url("./过渡动画练习图.png");     /* 引入图片 */

    transition: 2s steps(4);    /* 用时两秒，分四步进行 */
}

.box:hover{
    background-position: -1200px 0;     /* 设置最终出现的位置坐标 */
}
```

### 2、动画练习

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="box"></div>

</body>
</html>
```

```css
.box{
    width: 256px;
    height: 256px;
    margin: 100px auto;
    background-image: url("./动画.png");
    /* 开启执行动画 */
    animation: run 3s steps(6) infinite;        /* 关键帧名称  执行时间  分布执行步骤  循环次数 */
}

/* 创建关键帧 */
@keyframes run {
    /* 设置开始状态 */
    from{
        background-position: 0 0;
    }
    /* 设置结束状态 */
    to{
        background-position: -1536px 0;
    }
}
```

### 3、关键帧

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <div class="outer">
        <div class="box1"></div>
        <div class="box2"></div>
        <div class="box3"></div>
        <div class="box4"></div>
        <div class="box5"></div>
        <div class="box6"></div>
        <div class="box7"></div>
        <div class="box8"></div>
        <div class="box9"></div>
        <div class="box10"></div>
    </div>

</body>
</html>
```

```css
.outer{
    height: 500px;
    border-bottom: 10px black solid;
    margin: 50px auto;
    overflow: hidden;           /* 开启BFC，防止和子元素块一起运动 */
}

.outer div{
    float: left;
    width: 100px;
    height: 100px;
    border-radius: 50%;
    background-color: #bbffaa;

    /* 开启小球下落动画 */
    animation: ball 0.5s forwards infinite alternate;
}

/* 创建小球下落动画 */
@keyframes ball {
    from{       /* 开始加速下落 */
        margin-top: 0;
    }
    /*25%{        !* 总时间的25%时的动画状态。开始减速上升 *!*/
    /*    margin-top: 400px;*/
    /*    animation-timing-function: ease-in;     !* 减速 *!*/
    /*}*/
    /*50%{        !* 总时间的50%时的动画状态，开始加速下落 *!*/
    /*    margin-top: 200px;*/
    /*}*/
    /*70%{        !* 总时间的70%时的动画状态，开始减速上升 *!*/
    /*    margin-top: 400px;*/
    /*    animation-timing-function: ease-in;     !* 减速 *!*/
    /*}*/
    /*90%{        !* 总时间的90%的动画状态，开始加速下落 *!*/
    /*    margin-top: 350px;*/
    /*}*/
    to{         /* 最终停止状态 */
        margin-top: 400px;
    }
}

/* 设置小球颜色 */
div.box2{
    background-color: #FF6700;
    animation-delay: 0.1s;          /* 添加延迟 */
}
div.box3{
    background-color: #6cff8a;
    animation-delay: 0.2s;          /* 添加延迟 */
}
div.box4{
    background-color: #54b8ff;
    animation-delay: 0.3s;          /* 添加延迟 */
}
div.box5{
    background-color: #fffed6;
    animation-delay: 0.4s;          /* 添加延迟 */
}
div.box6{
    background-color: #ffd442;
    animation-delay: 0.5s;          /* 添加延迟 */
}
div.box7{
    background-color: #ff77a3;
    animation-delay: 0.6s;          /* 添加延迟 */
}
div.box8{
    background-color: #c62dff;
    animation-delay: 0.7s;          /* 添加延迟 */
}
div.box9{
    background-color: #71ff57;
    animation-delay: 0.8s;          /* 添加延迟 */
}
div.box10{
    background-color: #ff0a18;
    animation-delay: 0.9s;          /* 添加延迟 */
}
```

### 4、钟表

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./reset.css">
    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>
<!--    理论部分   -->
<!--    <div class="sec-wrapper">-->
<!--        <div class="sec"></div>-->
<!--    </div>-->

    <!-- 实战部分 -->
    <!-- 创建表的容器 -->
    <div class="clock">
        <!-- 创建时针 -->
        <div class="hour-wrapper">
            <div class="hour"></div>
        </div>

        <!-- 创建分针 -->
        <div class="min-wrapper">
            <div class="min"></div>
        </div>

        <!-- 创建原点样式 -->
        <div class="pointer"></div>
    </div>

</body>
</html>
```

```css
/*!* 理论部分 *!*/
/*!* 设置外部容器，使指针按一端为原点旋转 *!*/
/*.sec-wrapper{*/
/*    width: 500px;*/
/*    height: 500px;*/
/*    animation: test 60s;*/
/*}*/

/*.sec{*/
/*    !* 基础属性 *!*/
/*    height: 250px;*/
/*    width: 4px;*/
/*    background-color: red;*/
/*    margin: 0 auto;*/
/*}*/

/*!* 设置旋转角度 *!*/
/*@keyframes test { */
/*    from{*/
/*        transform: rotateZ(0);*/
/*    }*/
/*    to{*/
/*        transform: rotateZ(360deg)*/
/*    }*/
/*}*/


/* 实战部分 */
/* 设置表的样式 */
.clock{
    /* 设置基础属性 */
    width: 500px;
    height: 500px;
    margin: 0 auto;
    position: relative;                 /* 开启相对定位 */
    /*background: #bbffaa;                  表盘的背景颜色 */

    border-radius: 50%;                 /* 设置为圆形 */
    border: 10px solid black;           /* 设置表盘的边框 */
}

/* 将内部全部子元素设置居中样式 */
.clock > div{
    position: absolute;                 /* 开启绝对定位 */
    top: 0;                             /* 设置定位 */
    bottom: 0;
    left: 0;
    right: 0;
    margin: auto;
}

/* 设置动画样式 */
@keyframes clock-running {
    from{
        transform: rotateZ(0);          /* 设置开始角度 */
    }
    to{
        transform: rotateZ(360deg);     /* 设置结束角度 */
    }
}


/* 设置时针表盘基础样式 */
.hour-wrapper{
    height: 60%;                        /* 设置表盘大小 */
    width: 60%;
    /*background: #bbffaa;*/
    animation: clock-running 3600s infinite;    /* 开启动画，转一圈3600s */
}

/* 设置时针基础样式 */
.hour{
    height: 50%;                        /* 时针高度 */
    width: 6px;                         /* 时针宽度 */
    background-color: red;              /* 时针颜色 */
    margin: 0 auto;                     /* 时针在表盘内居中 */
}


/* 设置分针表盘基础样式 */
.min-wrapper{
    height: 90%;                        /* 设置表盘大小 */
    width: 90%;
    /*background: #bbffaa;*/
    animation: clock-running 60s steps(60) infinite;      /* 开启动画，转一圈60s */
}

/* 设置分针基础样式 */
.min{
    height: 50%;                        /* 时针高度 */
    width: 6px;                         /* 时针宽度 */
    background-color: red;              /* 时针颜色 */
    margin: 0 auto;                     /* 时针在表盘内居中 */
}


/* 设置原点样式 */
.pointer{
    width: 20px;                        /* 设置大小 */
    height: 20px;
    border-radius: 50%;                 /* 设置边距 */
    background-color: red;              /* 设置背景颜色 */
}
```

### 5、复仇者联盟

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./reset.css">
    <link rel="stylesheet" href="./CSS测试.css">

</head>
<body>

    <!-- 创建外部容器 -->
    <div class="cube">
        <!-- 引入图片 -->
        <div class="box1">
            <img src="./复仇者联盟/钢铁侠.png" alt="">
        </div>
        <div class="box2">
            <img src="./复仇者联盟/美国队长.png" alt="">
        </div>
        <div class="box3">
            <img src="./复仇者联盟/雷神.png" alt="">
        </div>
        <div class="box4">
            <img src="./复仇者联盟/黑寡妇.png" alt="">
        </div>
        <div class="box5">
            <img src="./复仇者联盟/浩克.png" alt="">
        </div>
        <div class="box6">
            <img src="./复仇者联盟/鹰眼.png" alt="">
        </div>
    </div>

</body>
</html>
```

```css
/* 设置视距 */
.html{
    perspective: 800px;
}

/* 设置外部容器基础样式 */
.cube{
    width: 300px;
    height: 300px;
    /*background-color: #bbffaa;*/
    margin: 200px auto;

    /* 设置3D变形效果 */
    transform-style: preserve-3d;
    transform: rotateX(45deg) rotateZ(45deg);

    /* 开启动画效果 */
    animation: test linear 20s infinite;
}

/* 添加动画效果 */
@keyframes test {
    from{
        transform: rotateX(0) rotateZ(0);           /* 设置开始旋转角度 */
    }
    to{
        transform: rotateX(1turn) rotateZ(1turn);   /* 设置旋转圈数 */
    }
}

/* 设置存放图片的div样式 */
.cube > div{
    width: 300px;                       /* 设置存放图片div容器的大小 */
    height: 300px;
    position: absolute;                 /* 开启绝对定位，脱离文档流 */
    opacity: 0.6;                       /* 为元素设置透明效果 */
}

/* 设置图片样式 */
img{

    width: 300px;                       /* 设置图片大小 */
    vertical-align: top;                /* 取消图片之间的边距 */
}

/* 设置每张图片的样式 */
.box1{
    transform: rotateY(90deg) translateZ(150px);
}
.box2{
    transform: rotateY(-90deg) translateZ(150px);
}
.box3{
    transform: rotateX(90deg) translateZ(150px);
}
.box4{
    transform: rotateX(-90deg) translateZ(150px);
}
.box5{
    transform: rotateY(0) translateZ(150px);
}
.box6{
    transform: rotateY(180deg) translateZ(150px);
}
```



## 第十节：弹性盒：练习

### 1、W3C导航条

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>测试</title>

    <link rel="stylesheet" href="./reset.css">
    <link rel="stylesheet" href="CSS测试.css">

</head>
<body>

    <ul class="nav">
        <li><a href="javascript:;">HTML/CSS</a></li>
        <li><a href="javascript:;">Browser Side</a></li>
        <li><a href="javascript:;">Server Side</a></li>
        <li><a href="javascript:;">Programming</a></li>
        <li><a href="javascript:;">XML</a></li>
        <li><a href="javascript:;">Web Building</a></li>
        <li><a href="javascript:;">Reference</a></li>
    </ul>

</body>
</html>
```

```css
/* 设置外部容器样式 */
.nav{
    width: 1210px;
    height: 46px;
    background-color: #adb1b1;
    margin: 200px auto;

    display: flex;          /* 设置弹性容器 */
}

/* 设置每个li元素块的自动增长系数 */
.nav li{
    flex-grow: 1;
}

/* 设置内部文字样式 */
.nav a{
    display: block;
    line-height: 46px;
    text-align: center;
    font-size: 16px;
    color: #FF6700;
}

.nav a:hover{
    background-color: #424242;
    color: white;
}
```

### 2、淘宝导航条

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>index</title>

    <link rel="stylesheet" href="./reset.css">
    <link rel="stylesheet" href="./index.css">

</head>
<body>

    <!-- 创建一个外层容器 -->
    <nav class="nav">
        <div class="nav-inner">
            <div class="item">
                <a href="javascript:;">
                    <img src="./image/1.png" alt="">
                    <span>天猫</span>
                </a>
            </div>
            <div class="item">
                <a href="javascript:;">
                    <img src="./image/2.png" alt="">
                    <span>天猫</span>
                </a>
            </div>
            <div class="item">
                <a href="javascript:;">
                    <img src="./image/3.png" alt="">
                    <span>天猫</span>
                </a>
            </div>
            <div class="item">
                <a href="javascript:;">
                    <img src="./image/4.png" alt="">
                    <span>天猫</span>
                </a>
            </div>
            <div class="item">
                <a href="javascript:;">
                    <img src="./image/5.png" alt="">
                    <span>天猫</span>
                </a>
            </div>
        </div>
        <div class="nav-inner">
            <div class="item">
                <a href="javascript:;">
                    <img src="./image/6.png" alt="">
                    <span>天猫</span>
                </a>
            </div>
            <div class="item">
                <a href="javascript:;">
                    <img src="./image/7.png" alt="">
                    <span>天猫</span>
                </a>
            </div>
            <div class="item">
                <a href="javascript:;">
                    <img src="./image/8.png" alt="">
                    <span>天猫</span>
                </a>
            </div>
            <div class="item">
                <a href="javascript:;">
                    <img src="./image/9.png" alt="">
                    <span>天猫</span>
                </a>
            </div>
            <div class="item">
                <a href="javascript:;">
                    <img src="./image/10.png" alt="">
                    <span>天猫</span>
                </a>
            </div>
        </div>
    </nav>

</body>
</html>
```

```css
/* 设置外层容器样式 */
.nav{
    width: 100%;
    height: 200px;
}

/* 设置每行的样式 */
.nav-inner{
    display: flex;                      /* 设置为弹性容器 */
    justify-content: space-around;      /* 设置主轴上的空白分布 */
}

/* 设置每个元素块的样式 */
.item{
    width: 10%;                         /* 设置图片占整个元素的比例 */
    /*background-color: yellow;*/
    /*flex: auto;*/
    text-align: center;                 /* 设置文字为居中样式 */
}

.item img{
    width: 100%;                        /* 设置照片的宽度和父元素的宽度一样 */
}

/* 设置字体样式 */
.item span{
    color: #333333;
    text-decoration: none;
    font-size: 16px;
}
```















































































