{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - Fichier de langage de balisage ColdFusion",
  "description" :"Découvrez ce qu'est un fichier CFML et les API qui peuvent créer et ouvrir des fichiers CFML.",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## Qu'est-ce qu'un fichier CFML ?

Un fichier avec l'extension .cfml est un fichier ColdFusion Markup Language utilisé pour créer une page Web. Il fait référence à un ensemble de règles utilisées pour définir comment l'application ColdFusion sera développée par le programmeur. ColdFusion est un langage de programmation utilisé pour créer des applications Web côté serveur rapidement et avec moins que d'autres technologies telles que [ASP](/fr/web/asp/), [PHP](/fr/web/php/), etc. Certains Parmi les applications pouvant ouvrir les fichiers CML, citons Adobe ColdFusion 2018, Adobe ColdFusion Builder et Adobe Dreamweaver.

## Format de fichier CFML - Plus d'informations

Les fichiers CFML sont des fichiers de balisage et contiennent des éléments Web sous forme de balises. Ce sont des fichiers texte qui peuvent être ouverts et modifiés dans n'importe quel éditeur de texte. Les fichiers CFML se composent de plusieurs balises similaires à [HTML](/fr/web/html/) et comprennent généralement une balise d'ouverture et une balise de fermeture. Ces balises peuvent également contenir un ou plusieurs attributs.

### Syntaxe des balises

Voici la syntaxe généralisée des balises CFML.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

La plupart des balises acceptent les attributs et sont définies comme suit.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Certaines de ces balises acceptent également plusieurs attributs avec la syntaxe suivante.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## Exemple de code CFML

Voici un exemple qui utilise une balise CFML réelle - la balise `cfoutput` :

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Références

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

