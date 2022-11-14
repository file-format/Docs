{
  "date" : "2019-10-11",
  "keywords" :[ "tpl","fichier tpl", "format de fichier tpl", "type de fichier tpl", "fichier", "type", "qu'est-ce qu'un fichier tpl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TPL - Modèle de serveur de fichiers HTTP",
  "description" :"Découvrez ce qu'est le fichier TPL et les API pour créer et ouvrir des fichiers TPL.",
  "linktitle" : "TPL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Qu'est-ce qu'un fichier TPL ?

Un fichier avec l'extension .tpl est un fichier modèle créé et utilisé par HTTP File Server (HFS) qui est un programme d'application de partage de fichiers pour envoyer et recevoir des fichiers via la technologie Web HTTP au lieu du protocole FTP. Il est utilisé pour créer des pages [HTML](/fr/web/html/) dynamiquement en fonction des informations de modèle définies pour avoir des paramètres avec une mise en page, un style et des scripts similaires. Les applications qui nécessitent les mêmes paramètres peuvent se voir attribuer le même fichier de modèle et HFS renverra dynamiquement la page demandée lors de l'exécution en fonction de ce fichier de modèle.


## Format de fichier TPL

Les fichiers TPL sont stockés dans un format lisible par l'homme et contiennent du HTML qui est un langage de balisage lisible par l'homme. En plus du HTML, un fichier TPL peut également contenir du CSS et du Javascript au niveau du modèle pour définir la mise en page et les actions à effectuer par toutes les pages générées à partir de ce fichier de modèle.

### Sections TPL

Les sections TPL contiennent le code HTML, CSS ou JavaScript utilisé par HFS lors de la génération de la page de sortie. Chaque section commence par des crochets ([]) et est définie par un signe de pourcentage (%). Un fichier TPL peut avoir les sections suivantes.

#### Section de style TPL

Il inclut les informations relatives au style qui peuvent ou non utiliser la référence des fichiers CSS intégrés. Un exemple de section de style est le suivant.

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

#### Section de lien TPL

La section de lien contient des informations sur l'URL et peut inclure des références à des événements tels que le bouton et son action.

```
[login-link]
<li><a href="%encoded-folder%~login" class=buttonx>Login</a></li>
[loggedin]
<li><a href="#" class=buttonx>Logged in as: %user%</a></li>
```

#### Section des commentaires

La section de commentaires de TPL inclut la génération de commentaires et est définie comme suit.
```
[comment]
<div class=comment>%item-comment%</div>
```

#### Section de téléchargement

La section de téléchargement renvoie la réponse HTML réelle du serveur en fonction des paramètres du modèle, comme illustré dans l'exemple suivant.

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

## Références

* [HFS](https://www.rejetto.com/wiki/index.php/Refinements)
* [Exemple TPL - Github](https://github.com/heiswayi/hfs-templates/blob/master/HFSTemplate_myHFS.tpl)

