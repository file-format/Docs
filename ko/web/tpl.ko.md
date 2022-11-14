{
  "date" : "2019-10-11",
  "keywords" :[ "tpl","tpl 파일", "tpl 파일 형식", "tpl 파일 형식", "파일", "유형", "tpl 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TPL - HTTP 파일 서버 템플릿",
  "description" :"TPL 파일이 무엇이며 TPL 파일을 만들고 여는 API에 대해 알아보세요.",
  "linktitle" : "TPL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## .TPL 파일이란?

확장자가 .tpl인 파일은 FTP 프로토콜 대신 웹 기술 HTTP를 통해 파일을 보내고 받는 파일 공유 응용 프로그램인 HTTP 파일 서버(HFS)에서 만들고 사용하는 템플릿 파일입니다. 레이아웃, 스타일 및 스크립트가 유사한 설정을 갖도록 정의된 템플릿 정보를 기반으로 [HTML](/ko/web/html/) 페이지를 동적으로 빌드하는 데 사용됩니다. 동일한 설정이 필요한 응용 프로그램에 동일한 템플릿 파일을 할당할 수 있으며 HFS는 이 템플릿 파일을 기반으로 런타임 시 요청된 페이지를 동적으로 반환합니다.


## TPL 파일 형식

TPL 파일은 사람이 읽을 수 있는 형식으로 저장되며 사람이 읽을 수 있는 마크업 언어인 HTML을 포함합니다. HTML 외에도 TPL 파일에는 템플릿 수준 CSS 및 Javascript가 포함되어 이 템플릿 파일에서 생성된 모든 페이지에서 수행할 레이아웃 및 작업을 정의할 수 있습니다.

### TPL 섹션

TPL 섹션에는 출력 페이지를 생성하는 동안 HFS에서 사용하는 HTML, CSS 또는 JavaScript 코드가 포함됩니다. 각 섹션은 대괄호([])로 시작하고 백분율 기호(%)로 정의됩니다. TPL 파일에는 다음 섹션이 있을 수 있습니다.

#### TPL 스타일 섹션

여기에는 포함된 CSS 파일 참조를 사용하거나 사용하지 않을 수 있는 스타일링 관련 정보가 포함됩니다. 스타일링 섹션의 예는 다음과 같다.

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

#### TPL 링크 섹션

링크 섹션에는 URL에 대한 정보가 포함되어 있으며 버튼 및 해당 작업과 같은 이벤트에 대한 참조를 포함할 수 있습니다.

```
[login-link]
<li><a href="%encoded-folder%~login" class=buttonx>Login</a></li>
[loggedin]
<li><a href="#" class=buttonx>Logged in as: %user%</a></li>
```

#### 댓글 섹션

TPL 포함의 주석 섹션은 주석을 생성하기 위한 것으로 다음과 같이 정의됩니다.
```
[comment]
<div class=comment>%item-comment%</div>
```

#### 업로드 섹션

업로드 섹션은 다음 예제와 같이 템플릿 설정을 기반으로 서버에서 실제 HTML 응답을 반환합니다.

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

## 참고문헌

* [HFS](https://www.rejetto.com/wiki/index.php/Refinements)
* [TPL 예시 - Github](https://github.com/heiswayi/hfs-templates/blob/master/HFSTemplate_myHFS.tpl)

