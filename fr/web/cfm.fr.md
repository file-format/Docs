{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "extension", "fichier", "format", "système", "Cold Fusion Markup Language", "langue", "pages Web CFM", "moteur CFML", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - Balisage de la fusion à froid",
  "description":"En savoir plus sur le format de fichier CFM et les API qui peuvent créer et ouvrir des fichiers CFM.",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Qu'est-ce qu'un fichier CFM ? ##

Les pages Web et les fichiers utilisés dans **Cold Fusion Markup Language** contiennent des extensions de CFM et sont nommés pages Web CFM. Ce langage de script de développement Web s'exécute sur Google App Engine, .NET Framework et JVM. Il peut contenir un langage de programmation ou le code du langage. Lorsque l'utilisateur accède à l'une de ses pages, le serveur Web de ColdFusion l'exécute. CFScript (qui est proche de JavaScript) ou des balises peuvent être utilisés pour écrire du CFML. CFML peut être utilisé pour générer d'autres langages en dehors de [HTML](/fr/web/html/) comme [CSS](/fr/web/css/), [JavaScript](/fr/web/js/), [XML](/fr/web/xml/), et plus encore.

L'utilisation de ce langage et des balises qu'il supporte se fait principalement dans le développement d'applications web dynamiques. Les fichiers peuvent être exécutés directement dans le navigateur en ligne si une erreur survient lors de l'utilisation hors ligne de la plateforme de développement de l'application.
 

CFML fonctionne de manière à ce que des extensions de fichier de serveur spécifiques (.cfc, .cfm) soient données pour être traitées par le moteur CFML. Si les moteurs sont basés sur Java, cela est réalisé à l'aide de servlets Java. Le moteur de CFML ne traite que les fonctions et les balises et renvoie les fonctions et le texte en dehors des balises CFML au serveur Web sans aucun changement.


## Bref historique ##

En 1995, il a d'abord été créé par une société nommée Allaire. En 2005, Adobe l'a acquis et il fournit encore aujourd'hui des services pour le développement de ColdFusion. Au fil des années, il a été développé et amélioré par de nombreuses personnes et entreprises. En 2012, une fondation nommée OpenCFML a été lancée. Plus tard, en 2015, l'ancien Railo a fourni ses services pour améliorer les performances de CFM et a réduit les ressources pour une meilleure fonctionnalité. La mise à jour la plus récente de celui-ci a été lancée en 2020 et devrait se poursuivre jusqu'en 2028.

## Format de fichier CFM ##

Le code des fichiers CFM et des pages Web comprend principalement les balises comme HTML mais avec une légère différence. Ces fichiers sont responsables de l'exécution de diverses opérations que les scripts ColdFusion permettent d'exécuter.
* Ces fichiers peuvent être consultés et exécutés directement sur Windows et macOS à l'aide du navigateur de n'importe quel système d'exploitation.
* Adobe ColdFusion fournit la plate-forme pour le développement de pages Web et d'applications dynamiques sur PC.
* N'importe quel éditeur de texte comme le Bloc-notes ou tout autre éditeur de texte dans un système d'exploitation peut être utilisé pour ouvrir ces fichiers car ces fichiers sont basés sur du texte.
* Lorsqu'un fichier CFM est ouvert dans un éditeur de texte, il affiche un code composé de balises et de scripts que l'on ne comprendrait pas à moins d'être un développeur Web.

## Exemple d'utilisation CFM ##

Ce qui suit montre un exemple d'utilisation simple du fichier CFM.

### Document CFM ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## Références ##

- [CFM - Wikipédia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

