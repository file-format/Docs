{
  "date": "2019-10-11",
  "keywords": [
"tpl",
"comhad tpl",
"formáid comhaid tpl",
"cineál comhaid tpl",
"comhad",
"cineál",
"cad is comhad tpl ann"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TPL - Teimpléad Freastalaí Comhad HTTP",
  "description": "Foghlaim faoi cad is Comhad TPL agus API ann chun comhaid TPL a chruthú agus a oscailt.",
  "linktitle": "TPL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-tp-gal"
}
},
  "lastmod": "2021-02-29"
}

## Cad is comhad TPL ann?

Comhad teimpléid é comhad le síneadh .tpl cruthaithe agus úsáidte ag Freastalaí Comhad HTTP (HFS) ar clár feidhmchláir comhroinnte é chun comhaid a sheoladh agus a fháil thar an teicneolaíocht gréasáin HTTP in ionad an phrótacail FTP. Úsáidtear é chun leathanaigh [HTML](/web/html/) a thógáil go dinimiciúil bunaithe ar an bhfaisnéis teimpléid a shainmhínítear go bhfuil socruithe acu a bhfuil leagan amach, stíleanna agus scripteanna comhchosúla acu. Is féidir an comhad teimpléad céanna a shannadh d’fheidhmchláir óna dteastaíonn na socruithe céanna agus tabharfaidh HFS an leathanach iarrtha ar ais go dinimiciúil ar am rite bunaithe ar an gcomhad teimpléad seo.


## Formáid Comhaid TPL

Stóráiltear comhaid TPL i bhformáid atá inléite ag an duine agus tá HTML iontu atá inléite ag an duine mar Theanga Mharcála. Chomh maith le HTML, d'fhéadfadh go mbeadh CSS agus Javascript ag leibhéal an teimpléid i gcomhad TPL chun an leagan amach agus na gníomhartha atá le déanamh ag na leathanaigh go léir a ghintear ón gcomhad teimpléid seo a shainiú.

### Rannóga TPL

Tá an cód HTML, CSS nó JavaScript a úsáideann HFS i gcodanna TPL agus an leathanach aschuir á ghiniúint. Tosaíonn gach cuid le lúibíní cearnacha ([]) agus sainmhínítear é le comhartha céatadáin (%). D’fhéadfadh na hailt seo a leanas a bheith i gcomhad TPL.

#### Rannóg Stíl TPL

Áiríonn sé an fhaisnéis a bhaineann le stíliú a fhéadfaidh nó nach féidir tagairt do chomhaid CSS leabaithe a úsáid. Seo a leanas sampla den mhír stílithe.

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

#### Rannóg Naisc TPL

Tá faisnéis faoin URL sa rannán naisc agus féadann sé tagairtí d’imeachtaí mar chnaipe agus a ghníomh a áireamh.

```
[login-link]
<li><a href="%encoded-folder%~login" class=buttonx>Login</a></li>
[loggedin]
<li><a href="#" class=buttonx>Logged in as: %user%</a></li>
```

#### Rannóg Tráchta

Is chun tuairimí a ghiniúint atá an seciton tráchtanna de TPL agus sainmhínítear é mar seo a leanas.
```
[comment]
<div class=comment>%item-comment%</div>
```

#### Rannóg Uaslódála

Tugann an rannán uaslódáil an freagra HTML iarbhír ón bhfreastalaí bunaithe ar na socruithe teimpléid mar a thaispeántar sa sampla seo a leanas.

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

## Tagairtí

* [HFS]( https://www.rejetto.com/wiki/index.php/Refinements)

* [TPL Exmaple - Github]( https://github.com/heiswayi/hfs-templates/blob/master/HFSTemplate_myHFS.tpl)


