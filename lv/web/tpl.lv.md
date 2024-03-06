{
  "date": "2019-10-11",
  "keywords": [
"tpl",
"tpl failu",
"tpl faila formātā",
"tpl faila tips",
"failu",
"veids",
"kas ir tpl fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TPL — HTTP failu servera veidne",
  "description": "Uzziniet, kas ir TPL fails un API, lai izveidotu un atvērtu TPL failus.",
  "linktitle": "TPL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-tp-lvl"
}
},
  "lastmod": "2021-02-29"
}

## Kas ir TPL fails?

Fails ar paplašinājumu .tpl ir veidnes fails, ko izveido un izmanto HTTP failu serveris (HFS), kas ir failu koplietošanas lietojumprogramma, lai nosūtītu un saņemtu failus, izmantojot tīmekļa tehnoloģiju HTTP, nevis FTP protokolu. To izmanto, lai dinamiski izveidotu [HTML](/web/html/) lapas, pamatojoties uz veidnes informāciju, kurai ir definēti iestatījumi ar līdzīgu izkārtojumu, stilu un skriptiem. Lietojumprogrammām, kurām nepieciešami vienādi iestatījumi, var piešķirt vienu un to pašu veidnes failu, un HFS dinamiski atgriezīs pieprasīto lapu izpildlaikā, pamatojoties uz šo veidnes failu.


## TPL faila formāts

TPL faili tiek glabāti cilvēkiem lasāmā formātā un satur HTML, kas ir cilvēkiem lasāma iezīmēšanas valoda. Papildus HTML TPL failā var būt arī veidnes līmeņa CSS un Javascript, lai noteiktu izkārtojumu un darbības, kas jāveic visām lapām, kas ģenerētas no šī veidnes faila.

### TPL sadaļas

TPL sadaļās ir HTML, CSS vai JavaScript kods, ko izmanto HFS, ģenerējot izvades lapu. Katra sadaļa sākas ar kvadrātiekavām ([]) un tiek noteikta ar procentuālo zīmi (%). TPL failam var būt šādas sadaļas.

#### TPL stila sadaļa

Tajā ir iekļauta ar stilu saistīta informācija, kas var vai nevar izmantot iegulto CSS failu atsauci. Veidošanas sadaļas piemērs ir šāds.

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

#### TPL saišu sadaļa

Saites sadaļā ir informācija par URL, un tajā var būt ietvertas atsauces uz notikumiem, piemēram, pogu un tās darbību.

```
[login-link]
<li><a href="%encoded-folder%~login" class=buttonx>Login</a></li>
[loggedin]
<li><a href="#" class=buttonx>Logged in as: %user%</a></li>
```

#### Komentāru sadaļa

TPL komentāru sadaļa ir paredzēta komentāru ģenerēšanai, un tā ir definēta šādi.
```
[comment]
<div class=comment>%item-comment%</div>
```

#### Augšupielādes sadaļa

Augšupielādes sadaļa atgriež faktisko HTML atbildi no servera, pamatojoties uz veidnes iestatījumiem, kā parādīts nākamajā piemērā.

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

## Atsauces

* [HFS](https://www.rejetto.com/wiki/index.php/Refinements)

* [TPL Exmaple — Github](https://github.com/heiswayi/hfs-templates/blob/master/HFSTemplate_myHFS.tpl)


