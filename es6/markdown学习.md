#标题
<font color=#0099ff size=12 face="黑体">类 Setext 形式是用底线的形式，利用 = （最高阶标题）和 - （第二阶标题）</font>
This is an H1
=============
This is an H2
-------------
类 Atx 形式则是在行首插入 1 到 6 个 # ，对应到标题 1 到 6 阶

# 这是h1

##这是h2

######这是h6

#区块引用 Blockquotes

Markdown 标记区块引用是使用类似 email 中用 > 的引用方式。
如果你还熟悉在 email 信件中的引言部分，你就知道怎么在 Markdown 
文件中建立一个区块引用，那会看起来像是你自己先断好行，然后在每行的最前面加上 > ：

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
>> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
>Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
> 

Markdown 也允许你偷懒只在整个段落的第一行最前面加上 > 
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

#列表

Markdown 支持有序列表和无序列表。

无序列表使用星号、加号或是减号作为列表标记：

*   Red
*   Green
*   Blue 
> 等同于
-   Red
-   Green
-   Blue 
> 等同于
+   Red
+   Green
+   Blue 
> 要存在一个空格
1. red
2. green
3. blue
5. white

######列表项目标记通常是放在最左边，但是其实也可以缩进，最多 3 个空格，项目标记后面则一定要接着至少一个空格或制表符。
*   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
viverra nec, fringilla in, laoreet vitae, risus.
*   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
Suspendisse id sem consectetuer libero luctus adipiscing.

######列表项目可以包含多个段落，每个项目下的段落都必须缩进 4 个空格或是 1 个制表符：

######如果要在列表项目内放进引用，那 > 就需要缩进

######如果要放代码区块的话，该区块就需要缩进两次，也就是 8 个空格或是 2 个制表符：

#代码区块

######要在 Markdown 中建立代码区块很简单，只要简单地缩进 4 个空格或是 1 个制表符就可以
这是一个普通段落：
    
    这是一个代码区块。
    
Here is an example of Application:

    tell application "Foo"
        beep
    end tell

#分隔线

你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：

***
* * *
*****
---
--------------

#区段元素

##链接

Markdown 支持两种形式的链接语法： 行内式和参考式两种形式。

不管是哪一种，链接文字都是用 [方括号] 来标记。

要建立一个行内式的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可，例如：

行内式：This is [an example](http://example.com/ "Title") inline link.

参考式：链接是在链接文字的括号后面再接上另一个方括号，而在第二个方括号里面要填入用以辨识链接的标记：

This is [an example][id] reference-style link.

你也可以选择性地在两个方括号中间加上一个空格：

接着，在文件的任意处，你可以把这个标记的链接内容定义出来：

[id]:http://example.com/ "optional Title Here"

链接内容定义的形式为：

1. 方括号（前面可以选择性地加上至多三个空格来缩进），里面输入链接文字
2. 接着一个冒号
3. 接着一个以上的空格或制表符
4. 接着链接的网址
5. 选择性地接着 title 内容，可以用单引号、双引号或是括弧包着

隐式链接标记功能让你可以省略指定链接标记，这种情形下，链接标记会视为等同于链接文字，要用隐式链接标记只要在链接文字后面加上一个空的方括号，如果你要让 "Google" 链接到 google.com，你可以简化成：

[Google][]
然后定义链接内容：

[Google]: http://google.com/

##强调

Markdown 使用星号（*）和底线（_）作为标记强调字词的符号，被 * 或 _ 包围的字词会被转成用 `<em>` 标签包围，用两个 * 或 _ 包起来的话，则会被转成`<strong>`

你用什么符号开启标签，就要用什么符号结束。

*single asterisks* 

_single underscores_

**double asterisks**

__double underscores__

如果你的 * 和 _ 两边都有空白的话，它们就只会被当成普通的符号。

##代码

如果要标记一小段行内代码，你可以用反引号把它包起来（`），例如：

Use the `printf()` function.

##图片

Markdown 使用一种和链接很相似的语法来标记图片，同样也允许两种样式： 行内式和参考式。

行内式的图片语法看起来像是：

![all text](/path/to/img.jpg "Optional title")

![Alt text](/path/to/img.jpg "Optional title")

详细叙述如下：

一个惊叹号 !
接着一个方括号，里面放上图片的替代文字
接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上 选择性的 'title' 文字。
参考式的图片语法则长得像这样：

![Alt text][id]

「id」是图片参考的名称，图片参考的定义方式则和连结参考一样：

[id]: url/to/image  "Optional title attribute"

#其它

##自动链接

Markdown 支持以比较简短的自动链接形式来处理网址和电子邮件信箱，只要是用方括号包起来， Markdown 就会自动把它转成链接。一般网址的链接文字就和链接地址一样，例如：

<http://example.com/>

##反斜杠

Markdown 可以利用反斜杠来插入一些在语法中有其它意义的符号，例如：如果你想要用星号加在文字旁边的方式来做出强调效果（但不用 <em> 标签），你可以在星号的前面加上反斜杠

\*literal asterisks\*
Markdown 支持以下这些符号前面加上反斜杠来帮助插入普通的符号：

* \\   反斜线

* \`   反引号

* \*   星号

* \_   底线

* \{}  花括号

* \[]  方括号
* \()  括弧
* \#   井字号
* \+   加号
* \-   减号
* \.   英文句点
* \!   惊叹号

#表格

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

### 流程图
```flow
st=>start: Start
e=>end
op=>operation: My Operation
cond=>condition: Yes or No?

st->op->cond
cond(yes)->e
cond(no)->op
```


字体、字号、颜色

1. <font face="黑体">我是黑体字</font>

2. <font face="微软雅黑">我是微软雅黑</font>

3. <font face="STCAIYUN">我是华文彩云</font>

4. <font color=#0099ff size=12 face="黑体">黑体</font>

5. <font color=#00ffff size=3>null</font>

6. <font color=gray size=5>gray</font>
