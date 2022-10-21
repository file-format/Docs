{
  "date" : "2019-10-11",
  "keywords" :[ "tpl", "tpl-Datei", "tpl-Dateiformat", "tpl-Dateityp", "Datei", "Typ", "was ist eine tpl-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TPL - HTTP-Dateiservervorlage",
  "description" :"Erfahren Sie, was TPL-Dateien und APIs zum Erstellen und Öffnen von TPL-Dateien sind.",
  "linktitle" :"TPL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Was ist eine TPL-Datei?

Eine Datei mit der Erweiterung .tpl ist eine Vorlagendatei, die von HTTP File Server (HFS) erstellt und verwendet wird, einem File-Sharing-Anwendungsprogramm zum Senden und Empfangen von Dateien über die Webtechnologie HTTP anstelle des FTP-Protokolls. Es wird verwendet, um [HTML](/de/web/html/)-Seiten dynamisch basierend auf den Vorlageninformationen zu erstellen, die so definiert sind, dass sie Einstellungen mit ähnlichem Layout, Stil und Skripten haben. Anwendungen, die dieselben Einstellungen erfordern, kann dieselbe Vorlagendatei zugewiesen werden, und HFS gibt die angeforderte Seite dynamisch zur Laufzeit basierend auf dieser Vorlagendatei zurück.


## TPL-Dateiformat

TPL-Dateien werden in einem für Menschen lesbaren Format gespeichert und enthalten HTML, das eine für Menschen lesbare Auszeichnungssprache ist. Zusätzlich zu HTML kann eine TPL-Datei auch CSS und Javascript auf Vorlagenebene enthalten, um das Layout und die Aktionen zu definieren, die von allen Seiten ausgeführt werden sollen, die aus dieser Vorlagendatei generiert werden.

### TPL-Abschnitte

TPL-Abschnitte enthalten den HTML-, CSS- oder JavaScript-Code, der von HFS beim Generieren der Ausgabeseite verwendet wird. Jeder Abschnitt beginnt mit eckigen Klammern ([]) und wird durch Prozentzeichen (%) definiert. Eine TPL-Datei kann die folgenden Abschnitte haben.

#### Abschnitt TPL-Stil

Es enthält Informationen zum Styling, die Referenzen zu eingebetteten CSS-Dateien verwenden können oder nicht. Ein Beispiel für den Styling-Bereich ist wie folgt.

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

#### Abschnitt TPL-Link

Der Linkabschnitt enthält Informationen über die URL und kann Verweise auf Ereignisse wie Schaltfläche und ihre Aktion enthalten.

```
[login-link]
<li><a href="%encoded-folder%~login" class=buttonx>Login</a></li>
[loggedin]
<li><a href="#" class=buttonx>Logged in as: %user%</a></li>
```

#### Kommentarbereich

Der Kommentarabschnitt von TPL Includes dient zum Generieren von Kommentaren und ist wie folgt definiert.
```
[comment]
<div class=comment>%item-comment%</div>
```

#### Upload-Bereich

Der Upload-Abschnitt gibt die tatsächliche HTML-Antwort vom Server basierend auf den Vorlageneinstellungen zurück, wie im folgenden Beispiel gezeigt.

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

## Verweise

* [HFS](https://www.rejetto.com/wiki/index.php/Refinements)
* [TPL-Beispiel – Github](https://github.com/heiswayi/hfs-templates/blob/master/HFSTemplate_myHFS.tpl)

