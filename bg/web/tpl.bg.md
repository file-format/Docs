{
  "date" : "2019-10-11",
  "keywords" :[ "tpl", "tpl файл", "tpl файлов формат", "tpl файлов тип", "файл", "тип", "какво е tpl файл" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TPL – Шаблон за HTTP файлов сървър",
  "description" :"Научете какво е TPL файл и API за създаване и отваряне на TPL файлове.",
  "linktitle" : "TPL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Какво е TPL файл?

Файл с разширение .tpl е шаблонен файл, създаден и използван от HTTP File Server (HFS), който е приложна програма за споделяне на файлове за изпращане и получаване на файлове през уеб технологията HTTP вместо FTP протокола. Използва се за динамично изграждане на [HTML](/bg/web/html/) страници въз основа на информацията за шаблона, която е дефинирана да има настройки с подобно оформление, стил и скриптове. Приложенията, които изискват същите настройки, могат да получат същия файл с шаблон и HFS ще върне исканата страница динамично по време на изпълнение въз основа на този файл с шаблон.


## TPL файлов формат

TPL файловете се съхраняват в четим от човека формат и съдържат HTML, който е четим от човек език за маркиране. В допълнение към HTML, TPL файлът може също да съдържа CSS на ниво шаблон и Javascript, за да дефинира оформлението и действията, които да се извършват от всички страници, генерирани от този шаблонен файл.

### Раздели на TPL

Секциите на TPL съдържат HTML, CSS или JavaScript кода, който се използва от HFS при генериране на изходната страница. Всеки раздел започва с квадратни скоби ([]) и се определя със знак за процент (%). TPL файл може да има следните секции.

#### Секция за стил на TPL

Той включва информация, свързана със стила, която може или не може да използва препратка към вградени CSS файлове. Пример за раздел за стилизиране е както следва.

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

#### Секция за връзка с TPL

Разделът за връзка съдържа информация за URL адреса и може да включва препратки към събития като бутон и неговото действие.

```
[login-link]
<li><a href="%encoded-folder%~login" class=buttonx>Login</a></li>
[loggedin]
<li><a href="#" class=buttonx>Logged in as: %user%</a></li>
```

#### Секция за коментари

Разделът за коментари на TPL включва предназначен за генериране на коментари и е дефиниран както следва.
```
[comment]
<div class=comment>%item-comment%</div>
```

#### Секция за качване

Разделът за качване връща действителния HTML отговор от сървъра въз основа на настройките на шаблона, както е показано в следния пример.

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

## Препратки

* [HFS](https://www.rejetto.com/wiki/index.php/Refinements)
* [TPL Exmaple - Github](https://github.com/heiswayi/hfs-templates/blob/master/HFSTemplate_myHFS.tpl)

