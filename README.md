# MDN - HTML
## [开始学习 HTML ](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Getting_started)
**重点：块级元素和内联元素**
1. 什么是 HTML?<br>
HTML (HyperText Markup Language) 不是一门编程语言，而是一种用来告知浏览器如何组织页面的**标记语言**,它由一系列的**元素（elements）**组成，这些元素可以用来包围不同部分的内容，使其以某种方式呈现或者工作。
2. 一个 HTML 元素<br>
![](https://mdn.mozillademos.org/files/16475/element.png)

   1. 嵌套元素:把元素放到其它元素之中<br>
   `<p>我的猫咪脾气<strong>爆</strong>:)</p>`
   2. **块级元素** <br>
   块级元素在页面中以块的形式展现 —— 相对与其前面的内容它会出现在新的一行，其后的内容也会被挤到下一行展现。块级元素通常用于展示页面上结构化的内容，例如段落、列表、导航菜单、页脚等等。<br>
   `<p>第四</p><p>第五</p><p>第六</p>`
   <p>第四</p><p>第五</p><p>第六</p>
   <br>
   
   3. **内联元素**<br>
   内联元素通常出现在块级元素中并包裹文档内容的一小部分，而不是一整个段落或者一组内容。内联元素不会导致文本换行.<br>
   `<em>第一</em><em>第二</em><em>第三</em>`<br>
   <em>第一</em><em>第二</em><em>第三</em>
   <br>
   
   4. 空元素<br>
   元素只有一个标签，通常用来在此元素所在位置插入/嵌入一些东西。<br>
3. 属性
![](https://mdn.mozillademos.org/files/16476/attribute.png)
   1. 布尔属性: 没有值的属性，它是合法的,他们只能有跟它的属性名一样的属性值。<br>
   2. 省略包围属性值的引号: <br>
   3. 单引号或者双引号
4. HTML中的空白
5. 实体引用： 在HTML中包含特殊字符<br>
`<`  ==  `&lt` ,  
`>`	==  `&gt` ,  
`"`	==  `&quot` ,  
`'`	==  `&apos` ,  
`&`	==  `&amp` ,  
6. HTML注释 <br>
`<!-- 注释 -->`

## [<head>标签里有什么? Metadata-HTML中的元数据](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML)
1. 什么是HTML 头部:<br>
HTML 头部是包含在 <head> 元素里面的内容。元素head 里面的内容不会在浏览器中显示，它的作用是包含一些页面的元数据。<br>
   1. 元数据：<title>元素  是用来表示整个HTML文档大致内容的元数据（不是文档的内容）
   2. 元数据：<meta>元素  指定了文档的字符编码 —— 在这个文档中被允许使用的字符集。 utf-8 是一个通用的字符集，它包含了任何人类语言中的大部分的字符。<meta> 元素包含了`name` 和`content` 特性：
   <br>name 指定了meta 元素的类型； 说明该元素包含了什么类型的信息。
   <br>content 指定了实际的元数据内容。
   3. 增加自定义图标 
      1. 将其保存在与网站的索引页面相同的目录中，以.ico格式保存.
      2. `<link rel="shortcut icon" href="favicon.ico" type="image/x-icon">`添加到HTML <head>中以引用它
   4. 应用CSS和JavaScript <br>
   `<link rel="stylesheet" href="my-css-file.css">`
   `<script src="my-js-file.js"></script>`
2. 为文档设定主语言
   1. `<html lang="en-US">`
   2. `<p>Japanese example: <span lang="jp">ご飯が熱い。</span>.</p>`
   
## [HTML 文字处理基础](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/HTML_text_fundamentals)
1. 基础: 标题和段落<br>
`<h1>我是文章的标题</h1>`
`<p>我是一个段落。</p>`
   1. 编辑结构层次规范化<br>
      1. 每个页面使用一次`<h1>`这是顶级标题
      2. 在层次结构中以正确的顺序使用标题。
      3. 在可用的六个标题级别中，您应该旨在每页使用不超过三个，除非您认为有必要使用更多。

   2. 为什么我们需要结构化?
      1. 对用户友好，便于查找
      2. 对您的网页建立索引的搜索引擎将标题的内容视为影响网页搜索排名的重要关键字。没有标题，您的网页在SEO（搜索引擎优化）方面效果不佳。
      3. 严重视力障碍者通常不会阅读网页；他们用听力来代替。屏幕阅读器（screen reader）通过朗读标题来提供文档的概述，让用户能快速找到他们需要的信息。
      4. 使用CSS样式化内容，或者使用JavaScript做一些有趣的事情，你需要包含相关内容的元素，所以CSS / JavaScript可以有效地定位它。
2. 列表 Lists
   1. 无序 Unordered `ul`
   2. 有序 Ordered   `ol`
   3. 列表项         `li`
   4. 嵌套列表 Nesting lists 将一个列表嵌入到另一个列表是完全可以的
3. 重点强调
   1. 强调 `<em>（emphasis）元素`
   2. 非常重要 `<strong>`
   3. 斜体字、粗体字、下划线. `<i>`, `<b>`, `<u>`
   
## [建立超链接](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks)
1. 什么是超链接?
任何网络内容都可以转换为链接，点击（或激活）超链接将使网络浏览器转到另一个网址`URL`。
2. 链接的解析
   1. 使用title属性添加支持信息
3. 统一资源定位器(URL)与路径(path)快速入门
   1. 统一资源定位器（英文：Uniform Resource Locator，简写：URL）是一个定义了在网络上的位置的一个文本字符串。
   2. URL使用路径查找文件。
4. 文档片段
   1. 超链接可以链接到html文档的特定部分（被称为文档片段），而不仅仅是文件的顶部。<br>
   `<h2 id="Mailing_address">Mailing address</h2>`<br>
   `<p>Want to write us a letter? Use our <a href="contacts.html#Mailing_address">mailing address</a>.</p>`
   2. 绝对链接和相对链接
      1. 绝对链接 指向由其在Web上的绝对位置定义的位置，包括 协议 and 域名. 
      2. 相对URL： 指向与您链接的文件相关的位置.
   3. 电子邮件链接
   `<a href="mailto:nowhere@mozilla.org">Send email to nowhere</a>`
## [高阶文字排版](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting)
1. 描述列表<br>
目的是标记一组项目及其相关描述，例如术语和定义，或者是问题和答案等。
<br>闭合标签`<dl>`
<br>每一项都用 `<dt>`
<br>每个描述都用 `<dd>`
2. 引用<br>
   1. 块引用
   个块级内容（一个段落、多个段落、一个列表等）从其他地方被引用，你应该把它用`<blockquote>`元素包裹起来表示，并且在`cite`属性里用`URL`来指向引用的资源。
   
   ```
      <blockquote cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote">
      <p>The <strong>HTML <code>&lt;blockquote&gt;</code> Element</strong> (or <em>HTML Block
      Quotation Element</em>) indicates that the enclosed text is an extended quotation.</p>
      </blockquote>
   ```
   2. 行内引用
   行内元素用同样的方式工作，除了使用`<q>`元素<br>
   ```
      <p>The quote element — <code>&lt;q&gt;</code> — is 
      <q cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q">intended
      for short quotations that don't require paragraph breaks.</q></p>
   ```
   3. [引文](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting#%E5%BC%95%E6%96%87)
3. 缩略语 `<abbr>` <br>
`<p>我们使用 <abbr title="超文本标记语言（Hypertext Markup Language）">HTML</abbr> 来组织网页文档。</p>`
4. 标记联系方式 `<address>` 为了标记编写HTML文档的人的联系方式
5. 上标和下标  `<sub>` 和`<sup>`
6. 展示计算机代码
有大量的HTML元素可以来标记计算机代码：<br>
* `<code>`: 用于标记计算机通用代码。
* `<pre>`: 对保留的空格（通常是代码块）——如果您在文本中使用缩进或多余的空白，浏览器将忽略它，您将不会在呈现的页面上看到它。但是，如果您将文本包含在<pre></pre>标签中，那么空白将会以与你在文本编辑器中看到的相同的方式渲染出来。
- `<var>`: 用于标记具体变量名。
- `<kbd>`: 用于标记输入电脑的键盘（或其他类型）输入。
- `<samp>`: 用于标记计算机程序的输出。

7. 标记时间和日期 `<time>`<br>
`<time datetime="2016-01-20">2016年1月20日</time>`

## [文档与网站架构](https://developer.mozilla.org/zh-CN/docs/learn/HTML/Introduction_to_HTML/%E6%96%87%E4%BB%B6%E5%92%8C%E7%BD%91%E7%AB%99%E7%BB%93%E6%9E%84)
1. 文档的基本组成区段（Section）<br>
- 标题栏
- 导航栏
- 主内容
- 侧边栏
- 页脚
2. 用于构建内容的 HTML<br>
- `<header>`：标题栏。
- `<nav>`：导航栏。
- `<main>`：主内容。主内容中还可以有各种子内容区段，可用`<article>`、`<section>` 和 `<div>` 等元素表示。
- `<aside>`：侧边栏，经常嵌套在 `<main>` 中。
- `<footer>`：页脚。

3. HTML 布局元素细节<br>
- `<main>` 存放每个页面独有的内容。每个页面上只能用一次` <main>`，且直位于` <body>` 中。最好不要把它嵌套进其它元素。
- `<article>` 包围的内容即一篇文章，与页面其它部分无关（比如一篇博文）。
- `<section>` 与 `<article>` 类似，但 `<section> `更适用于组织页面使其按功能（比如迷你地图、一组文章标题和摘要）分块。一般的最佳用法是：以 标题 作为开头；也可以把一篇 `<article>` 分成若干部分并分别置于不同的 `<section>` 中，也可以把一个区段 `<section>` 分成若干部分并分别置于不同的 `<article>` 中，取决于上下文。
- `<aside>` 包含一些间接信息（术语条目、作者简介、相关链接，等等）。
- `<header>` 是简介形式的内容。如果它是 `<body>` 的子元素，那么就是网站的全局页眉。如果它是 `<article>` 或`<section>` 的子元素，那么它是这些部分特有的页眉（此 `<header>` 非彼 标题）。
- `<nav>` 包含页面主导航功能。其中不应包含二级链接等内容。
- `<footer>` 包含了页面的页脚部分。
4. 无语义元素<br>
对于一些要组织的项目或要包装的内容，现有的语义元素均不能很好对应,HTML提供了 <div> 和 <span> 元素。<br>
- `<span>` 是一个内联的`inline`无语义元素，最好只用于无法找到更好的语义元素来包含内容时，或者不想增加特定的含义时。
- `<div>` 是一个块级无语义元素，应仅用于找不到更好的块级元素时，或者不想增加特定的意义时。
5. 换行与水平分割线
` <br>` 和 `<hr>`
















