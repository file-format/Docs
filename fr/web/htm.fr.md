{
  "date" : "2019-10-11",
  "keywords" :[ "htm","fichier htm", "format de fichier htm", "type de fichier htm", "fichier", "type", "qu'est-ce qu'un fichier htm" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier HTML",
  "description" :"Votre guide de format de fichier pour savoir ce qu'est un fichier HTM et les API qui peuvent les créer et les ouvrir.",
  "linktitle" : "HTM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier HTM ?

Les fichiers avec l'extension **.htm** représentent le langage de balisage hypertexte pour créer des pages Web à afficher dans des navigateurs Web tels que Google Chrome, Internet Explorer, Firefox et un certain nombre d'autres. Il définit les balises pour la création de pages statiques à publier sur le World Wide Web (WWW) pour l'accès par d'autres. Ces balises indiquent aux navigateurs comment afficher le contenu d'une page Web. Ces pages peuvent contenir du texte brut, des images, des hyperliens vers d'autres pages, des vidéos et d'autres informations multimédias. Lorsqu'une page Web est publiée, vous pouvez consulter le code de balisage qui la sous-tend en affichant la source de sa page. Les navigateurs modernes permettent d'inspecter chaque section d'une page Web où chaque sous-division ou élément de balisage dans la source HTM est élaboré.

## Bref historique de HTM

Depuis sa création et son premier rôle, les spécifications HTML ont été maintenues par le World Wide Web Consortium (W3C) depuis 1996. En 2000, elles sont également devenues une norme internationale (ISO/IEC 15445:2000). En 1999, HTML 4.01 a été publié. En 2004, le groupe de travail sur la technologie d'application hypertexte Web (WHATWG) a commencé à travailler sur la version HTML5 qui est devenue un livrable conjoint avec le W3C en 2008. Elle a été achevée et normalisée le 28 octobre 2014.

## Format de fichier HTML

Un document HTML 4 est composé de trois parties :

1. une ligne contenant les informations de version HTML
1. une section d'en-tête déclarative
1. un corps, qui contient le contenu réel du document. Le corps peut être implémenté par l'élément BODY ou l'élément FRAMESET pour contenir le corps dans des cadres

Chaque section peut être précédée ou suivie d'espaces blancs, de nouvelles lignes, d'onglets et de commentaires. Un exemple de document HTML simple est illustré ci-dessous :

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Information sur la version

La première ligne de code,<!DOCTYPE html> , s'appelle une déclaration de type de document et indique au navigateur dans quelle version de HTML la page est écrite. Selon la version de HTML, il existe un certain nombre de déclarations de type de document différentes qui nomment la définition de type de document (DTD) utilisée pour le document. Chaque DTD diffère des autres par les éléments qu'elle prend en charge et diffère comme suit :

* HTML 4.01 Strict - inclut tous les éléments et attributs qui n'ont pas été [obsolètes](https://www.w3.org/TR/html401/conform.html#deprecated) ou qui n'apparaissent pas dans les documents de jeu de cadres
* HTML 4.01 Transitional - inclut tout ce qui se trouve dans la DTD stricte ainsi que les éléments et attributs obsolètes (dont la plupart concernent la présentation visuelle
* Jeu de cadres HTML 4.01 - comprend également tout ce qui se trouve dans la DTD de transition plus les cadres

Pour **HTML5**, les informations de version sont simplement comme indiqué ci-dessous.

```
<!DOCTYPE html>
```

### Informations d'en-tête

L'en-tête d'un document HTML peut inclure un certain nombre d'éléments HTML qui ne sont pas rendus par le navigateur. Ces éléments sont soit des métadonnées décrivant des informations sur la page, soit des sections utilisées pour récupérer des informations à partir de ressources externes telles que des feuilles de style CSS ou des fichiers JavaScript. L'en-tête d'une page est représenté par \<head> balise et se termine par \</head> étiquette.

<html>Pour définir le titre de la page, le \<title> L'élément est le seul requis dans les balises \<head>. Le même est utilisé par les moteurs de recherche pour identifier le titre d'une page. </html>

### Informations sur le corps

Il s'agit de la section principale du fichier qui contient tout le contenu du fichier rendu par les navigateurs. Le corps HTML peut contenir des balises qui peuvent faire référence à divers blocs de construction sous la forme de balises. Il peut contenir plusieurs types d'informations différents comme du texte, des images, des couleurs, des graphiques, etc. De plus, des éléments audio et vidéo peuvent également être intégrés dans le corps html pour être rendus par les navigateurs. En présence d'applications de feuilles de style modernes pour la représentation visuelle, les attributs de présentation de BODY tels que la couleur d'arrière-plan, la couleur du lien, la couleur du texte, etc. ont été dépréciés. Ainsi, les mêmes effets peuvent être obtenus en utilisant des feuilles de style comme indiqué ci-dessous :

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

Les feuilles de style en ligne sont faciles à intégrer et pour des applications rapides aux effets visuels, les feuilles de style externes facilitent le déploiement unique et l'accès à de nombreux endroits.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### Éléments HTML

Comme mentionné précédemment, le contenu du corps HTML est représenté par des balises, également appelées éléments HTML. Chaque balise peut avoir des informations supplémentaires sous la forme d'attributs qui sont écrits comme
```
<tag attribute1#"value1" attribute2#"value2">
```
bien qu'il ne soit pas nécessaire d'avoir des attributs avec chaque balise. Si les attributs ne sont pas mentionnés, les valeurs par défaut sont utilisées dans chaque cas. Voici quelques exemples d'éléments :

#### Entête

```
<head>
  <title>The Title</title>
</head>
```

#### Titres

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Paragraphes

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## Références

* [La structure globale du document HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

