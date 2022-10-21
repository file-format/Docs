{
  "date" : "2019-10-11",
  "keywords" :["tpl","tpl文件","tpl文件格式","tpl文件类型","文件","类型","什么是tpl文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TPL - HTTP 文件服务器模板",
  "description" :"了解什么是 TPL 文件以及用于创建和打开 TPL 文件的 API。",
  "linktitle" : "TPL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## 什么是一 .tpl 文件？

扩展名为 .tpl 的文件是由 HTTP 文件服务器 (HFS) 创建和使用的模板文件，该文件是一个文件共享应用程序，用于通过 Web 技术 HTTP 而不是 FTP 协议发送和接收文件。它用于根据定义为具有类似布局、样式和脚本设置的模板信息动态构建 [HTML](/zh/web/html/) 页面。可以为需要相同设置的应用程序分配相同的模板文件，HFS 将根据此模板文件在运行时动态返回请求的页面。


## TPL 文件格式

TPL 文件以人类可读的格式存储，并包含人类可读的标记语言 HTML。除了 HTML，TPL 文件还可能包含模板级 CSS 和 Javascript，以定义从该模板文件生成的所有页面要执行的布局和操作。

### TPL 部分

TPL 部分包含 HFS 在生成输出页面时使用的 HTML、CSS 或 JavaScript 代码。每个部分都以方括号 ([]) 开头，并由百分号 (%) 定义。 TPL 文件可能包含以下部分。

#### TPL 样式部分

它包括样式相关的信息，这些信息可能会或可能不会使用嵌入的 CSS 文件参考。样式部分的示例如下。

```
[style]
.row { color: #666 }
span.size_file { font-size:10px; color:#666 }
.button, .big, .little, th { font-weight:normal; font-size:9pt; color:#222; }
#back { background:#222;border:1px solid #000;padding:5px;margin-top:10px;}
.little { font-size: 8pt; color:#2F4F4F;margin-top:10px; }
.path_title { color: #999;margin-top:10px; }
img { border-style:none }
.row { background:#f8f8f8;}
.row a { text-decoration:none; }
.comment { font-size:7pt; color:#666; background:#f3f3f3; padding:3px; border:1px solid #ccc; margin-top:2px; }
.column { color:#222; font-size:13pt; font-weight:bold; padding-bottom:0; }
.flag { font-weight:bold; font-size:8pt; background:#fff; color:#990000; text-align:center; border:1px solid #ff0000; }
.text { color:#222; }
span.desc { color: #999; }
#everything { margin-top:20px;border-top:1px solid #ccc;padding-top:10px; }
html {
font-size: 62.5%;
}
body {margin:0px; padding:0px; background-color:#fff; color:#222; font-family:"Lucida Grande", "Tahoma", "Helvetica", "Arial", sans-serif; font-size:120%;quotes:"\201C" "\201E" "\2018" "\2019";}
table, tr, td {font-size: inherit;}
a:link {color: #222;}
a:visited {color: #666;}
a:hover {	color: #000;}
a:active {}
a:focus {}
img, a img {border: none;}
#path {color: #333;background-color: #f8f8f8; border-bottom: 1px solid #ccc;padding: 3px 8px;margin: 0px;}
#path li {display: inline;padding-left: 13px; padding-right: 3px; background-image: url(arrow.gif);background-repeat: no-repeat;background-position: 1px 5px;}
#path span {font-weight: bold;}
#header {margin: 24px 48px;}
#header h1 {font-size: 250%;color: #222;  margin: 0;margin-bottom: 6px;}
#header h2 {font-size: 120%;color: #aaa;  margin: 0;}
#content { margin: 24px 48px;}
#footer {    margin-top: 48px;    border-top: 1px solid #ccc;    padding: 6px;    text-align: center;    color: #888;    font-size: 80%;}
#footer a {color: #888;}
```

#### TPL 链接部分

链接部分包含有关 URL 的信息，并且可以包括对事件的引用，例如按钮及其操作。

```
[login-link]
<li><a href="%encoded-folder%~login" class=buttonx>Login</a></li>
[loggedin]
<li><a href="#" class=buttonx>Logged in as: %user%</a></li>
```

#### 评论区

TPL 的评论部分包括用于生成评论，定义如下。
```
[comment]
<div class=comment>%item-comment%</div>
```

#### 上传部分

上传部分根据模板设置从服务器返回实际的 HTML 响应，如下例所示。

```
[upload]
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">
<html><head>
<title>myHFS</title>
<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">
<style type="text/css">\n%style%\n</style>
</head>
<body>
<ul id=path>
<li><strong>Folder:</strong> <a href="/">root</a>%folder%</li>
</ul>
<div id=header>
<h1>myHFS</h1>
<h2>Final HFS Template Framework for Ishare USM Community</h2>
</div>
<div id=content>

<h3>myHFS Rules</h3>
<p>I'm sharing stuffs unpaid, so please respect me by understanding these rules: </p>
<ul class="contacts">
<li>Sorry if your downloading activity was suddenly interrupted/disconnected. It might be due to some technical problems.</li>
<li>Be nice. Don't use IDM or any download manager program with many connections. Set it to 1 or you will be banned from my server.</li>
<li>Anything I shared here is the right of my freedom. Good or bad, the decision is in your hands. I'm not be responsible for any consequences.</li>
</ul>
<p class=credit>Sharing among my university fellows is an unique culture here, in Engineering Campus, USM. Sharing via LAN by using HFS software is the best underground activity for everyone. Sharing is loving!</p>
</div>

</body></html>
```

## 参考

* [HFS](https://www.rejetto.com/wiki/index.php/Refinements)
* [TPL 示例-Github](https://github.com/heiswayi/hfs-templates/blob/master/HFSTemplate_myHFS.tpl)

