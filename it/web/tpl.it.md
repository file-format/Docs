{
  "date" : "2019-10-11",
  "keywords" :[ "tpl","file tpl", "formato file tpl", "tipo di file tpl", "file", "tipo", "cos'è un file tpl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TPL - Modello di file server HTTP",
  "description" :"Scopri cos'è il file TPL e le API per creare e aprire file TPL.",
  "linktitle" : "TPL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Che cos'è un file TPL?

Un file con estensione .tpl è un file modello creato e utilizzato da HTTP File Server (HFS), che è un programma applicativo di condivisione file per inviare e ricevere file tramite la tecnologia Web HTTP anziché il protocollo FTP. Viene utilizzato per creare pagine [HTML](/it/web/html/) in modo dinamico in base alle informazioni del modello definite per avere impostazioni con layout, stile e script simili. Le applicazioni che richiedono le stesse impostazioni possono essere assegnate allo stesso file modello e HFS restituirà la pagina richiesta in modo dinamico in fase di esecuzione in base a questo file modello.


## Formato file TPL

I file TPL sono archiviati in un formato leggibile dall'uomo e contengono HTML che è un linguaggio di markup leggibile dall'uomo. Oltre all'HTML, un file TPL può contenere anche CSS e Javascript a livello di modello per definire il layout e le azioni che devono essere eseguite da tutte le pagine generate da questo file modello.

### Sezioni RC

Le sezioni TPL contengono il codice HTML, CSS o JavaScript utilizzato da HFS durante la generazione della pagina di output. Ogni sezione inizia con parentesi quadre ([]) ed è definita dal segno di percentuale (%). Un file TPL può avere le seguenti sezioni.

#### Sezione stile TPL

Include le informazioni relative allo stile che possono o meno utilizzare riferimenti ai file CSS incorporati. Un esempio di sezione styling è il seguente.

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

#### Sezione collegamento TPL

La sezione del collegamento contiene informazioni sull'URL e può includere riferimenti a eventi come il pulsante e la sua azione.

```
[login-link]
<li><a href="%encoded-folder%~login" class=buttonx>Login</a></li>
[loggedin]
<li><a href="#" class=buttonx>Logged in as: %user%</a></li>
```

#### Sezione commenti

La sezione commenti di TPL include è per la generazione di commenti ed è definita come segue.
```
[comment]
<div class=comment>%item-comment%</div>
```

#### Carica sezione

La sezione di caricamento restituisce la risposta HTML effettiva dal server in base alle impostazioni del modello come mostrato nell'esempio seguente.

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

## Riferimenti

* [HFS](https://www.rejetto.com/wiki/index.php/Refinements)
* [Esempio TPL - Github](https://github.com/heiswayi/hfs-templates/blob/master/HFSTemplate_myHFS.tpl)

