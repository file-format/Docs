{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - Format de fichier de fragments JSP",
  "description":"En savoir plus sur le format de fichier JSPF et les API qui peuvent créer et ouvrir des fichiers JSPF.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## Qu'est-ce qu'un fichier JSPF ?
Le fichier avec l'extension .jspf est appelé fragment JSP ; un fichier statique inclus dans un autre fichier JSP. Les fichiers JSPF ne sont pas compilés seuls, cependant, ils sont compilés avec la page dans laquelle ils sont inclus. Sa syntaxe est similaire au code Java Server Pages (JSP). Il contient juste un fragment de JSP ; pas inclus tout le document JSP entier.

## Format de fichier JSPF
Le terme "segment JSP" est utilisé à la place car le terme "fragment JSP" est surchargé dans la spécification JSP 2.0. Les fragments JSP peuvent utiliser les extensions .jsp ou .jspf et doivent être placés soit dans **/WEB-INF/jspf** soit avec le reste des fichiers statiques. Les fragments JSP qui ne sont pas des pages complètes doivent utiliser l'extension .jspf et doivent être placés dans **/WEB-INF/jspf**

### Organisation des fichiers JSP ou fragment JSP
Un fichier JSP contient les sections suivantes dans l'ordre dans lequel elles sont répertoriées :

1. Commentaires d'ouverture
2. Directive(s) de page JSP
3. Directive(s) facultative(s) sur la bibliothèque de balises
4. Déclaration(s) JSP facultative(s)
5. Code HTML et JSP

Un fichier JSP ou JSPF commence tous deux par un commentaire de style côté serveur appelé **Commentaire d'ouverture** :

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Ce commentaire ne peut être visible que côté serveur car il est supprimé lors du rendu de la page JSP.

## Quand utiliser le fichier JSP Fragment ?
Lorsqu'une page JSP nécessite une structure certaine mais complexe qui peut également être réutilisée dans d'autres pages JSP, une façon de gérer cela est de la diviser en morceaux, en utilisant le modèle Composite View (la section Patterns de Java Blueprints). Par exemple, une page JSP a parfois la disposition logique suivante dans sa structure de présentation :

{{< figure src="../jspf.png" alt="Format de fichier JSPF" >}}

Dans cette situation, cette page JSP composite peut être convertie en différents modules, chacun étant appelé un fragment JSP distinct. Les fragments JSP peuvent ensuite être placés aux emplacements appropriés dans la page JSP composite. Par conséquent, le fichier JSPF est utilisé lorsque des directives d'inclusion statiques sont utilisées pour inclure une page qui ne serait pas appelée par elle-même, les fichiers avec l'extension .jspf doivent être placés dans le répertoire /WEB-INF/jspf/ de l'archive de l'application Web ( guerre).

## Exemple JSPF
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## Références

* [Conventions de code pour les pages JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

