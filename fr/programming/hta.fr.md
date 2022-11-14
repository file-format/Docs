{
  "date" : "2021-09-16", 
  "keywords" :[ "hta", "fichier", "extension", "format de fichier", "implémentation hta", "Guide de programmation", "exemple hta", "Application HTML", "Application Hypertext Markup Language", "Fichiers HTA", "Application Microsoft HTML"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTA - Fichiers d'application HTML",
  "description":"En savoir plus sur le format de fichier HTA et les API qui peuvent créer et ouvrir des fichiers HTA.",
  "linktitle" : "HTA",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-16"
}

## Qu'est-ce qu'un fichier HTA ?

Le HTMLA signifie **Hypertext Markup Language Application** est un programme compatible avec Microsoft Windows. Le code source de ce programme comprend plusieurs langages de script tels que [HTML](/fr/web/html/) et [JavaScript](/fr/web/js/). Pour l'interface utilisateur, une application HTML est préférée tandis que pour répondre aux exigences de la logique du programme, tout autre langage de script est utilisé.

Une application HTML est indépendante du modèle de sécurité du navigateur Internet et fonctionne comme une application entièrement fiable. L'extension utilisée pour les fichiers concernant ces applications est HTA. Ces applications incluent des fonctionnalités de HTML ainsi que les propriétés d'autres langages de script.


## Bref historique ##

Le HTA a été introduit pour la première fois en 1999 par Microsoft avec la sortie d'Internet Explorer 5. Il était compatible avec Internet Explorer et ne pouvait donc être exécuté que sur le système d'exploitation Windows. Cette technologie a été brevetée en 2003. Les fichiers HTA sont exécutés comme n'importe quel autre fichier .exe. Les fichiers HTA sont également compatibles avec la version mise à jour actuelle de Windows 11.


## Spécification technique ##

Les HTA ont le même format que n'importe quelle autre page HTML, tandis que certains attributs sont utilisés pour contrôler les styles des bordures ou des icônes des programmes. Par ailleurs, des arguments sont fournis pour le lancement de l'HTA. Ces applications peuvent être exécutées à l'aide d'un programme nommé mshta.exe. Il est accessible par un simple double-clic sur le fichier. Ces programmes s'exécutent automatiquement avec Internet Explorer. Outre d'autres spécifications, celles-ci ne sont pas indépendantes du navigateur du moteur Trident mais sont indépendantes d'Internet Explorer. Cela signifie que ceux-ci peuvent être exécutés sans utiliser Internet Explorer.

Les balises sont utilisées dans un souci de personnalisation de l'apparence de ces applications. La conversion de l'application Microsoft HTML au format HTA est plus facile, c'est-à-dire que vous n'avez qu'à changer l'extension. Comme nous savons que ces applications sont entièrement fiables, elles comportent donc plus de fonctionnalités et d'avantages par rapport aux simples fichiers HTML. Les éditeurs de texte peuvent être utilisés pour créer HTA. Ces éditeurs peuvent être acquis par Microsoft ou toute autre source fiable.


## Exemple de format de fichier HTA ##

```
<HTML>
<HEAD>
<HTA:APPLICATION ID="HelloExample" 
   BORDER="bold" 
   BORDERSTYLE="complex"/>
<TITLE>HTA - Hello World</TITLE>
</HEAD>
<BODY>
<H2>HTA - Hello World</H2>
</BODY>
</HTML>

```

## Référence ##

* [HTA - par Wikipédia](https://en.wikipedia.org/wiki/HTML_Application)



