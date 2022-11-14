{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml","fichier dhtml", "format de fichier dhtml", "type de fichier dhtml", "fichier", "type", "qu'est-ce qu'un fichier dhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML - Format de fichier HTML dynamique",
  "description":"En savoir plus sur le format de fichier DHTML et les API qui peuvent créer et ouvrir des fichiers DHTML.",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier DHTML ?

Un fichier avec une extension .dhtml est un fichier [HTML](/fr/web/html/) dynamique utilisé pour créer le contenu dynamique d'une page Web. Un élément Web créé en DHTML est événementiel et ne nécessite pas de recharger la page. Dans la plupart des cas, un fichier DHTML est utilisé pour créer le contenu dynamique d'une page Web, tel que des menus déroulants, des calques flottants, des boutons de survol et d'autres contenus dynamiques. Vous rencontrez des éléments html dynamiques presque quotidiennement dans votre vie lorsque vous passez la souris sur un élément de menu et cela ouvre d'autres options de sous-menu. DHTML utilise des technologies Web telles que [HTML](/fr/web/html/), [Javascript](/fr/web/js/), HTML DOM, HTML Events et [CSS](/fr/web/css/) pour obtenir la dynamique comportement des éléments.

## Format de fichier DHTML

Les fichiers DHTML sont des fichiers de texte brut qui contiennent du code DHTML pour implémenter le comportement dynamique des éléments Web.


### DOM DHTML

Le modèle d'objet de document DHTML (DOM) est basé sur le DOM HTML qui est une arborescence avec des éléments, des attributs et du texte, comme illustré dans l'image suivante.

{{< figure src="../dhtml.png" alt="DOM HTML" >}}

Le nœud `Document` peut être utilisé pour appeler plusieurs fonctions afin d'implémenter différentes fonctionnalités. L'exemple suivant utilise simplement la méthode document.write() de JavaScript dans le DHTML.

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

Ce code écrit le texte "Hello World" à afficher dans le navigateur.

### Événements DHTML

|S.No.|Événement|Occurrence|
---|---|---|
|1|onabort|Cela se produit lorsque l'utilisateur abandonne le chargement de la page ou du fichier multimédia.|
|2|onblur|Il se produit lorsque l'utilisateur quitte un objet HTML.|
|3|onchange|Il se produit lorsque l'utilisateur modifie ou met à jour la valeur d'un objet.|
|4|onclick|Il se produit ou se déclenche lorsqu'un utilisateur clique sur un élément HTML.|
|5|ondblclick|Il se produit lorsque l'utilisateur clique deux fois de suite sur un élément HTML.|
|6|onfocus|Cela se produit lorsque l'utilisateur se concentre sur un élément HTML. Ce gestionnaire d'événements fonctionne à l'opposé de onblur.|
|7|onkeydown|Il se déclenche lorsqu'un utilisateur appuie sur une touche d'un clavier. Ce gestionnaire d'événements fonctionne pour toutes les clés.|
|8|onkeypress|Il se déclenche lorsque les utilisateurs appuient sur une touche d'un clavier. Ce gestionnaire d'événements n'est pas déclenché pour toutes les clés.|
|9|onkeyup|Cela se produit lorsqu'un utilisateur relâche une touche d'un clavier après avoir appuyé sur un objet ou un élément.|
|10|onload|Il se produit lorsqu'un objet est complètement chargé.|
|11|onmousedown|Il se produit lorsqu'un utilisateur appuie sur le bouton d'une souris sur un élément HTML.|
|12|onmousemove|Cela se produit lorsqu'un utilisateur déplace le curseur sur un objet HTML.|
|13|onmouseover|Il se produit lorsqu'un utilisateur déplace le curseur sur un objet HTML.|
|14|onmouseout|Il se produit ou se déclenche lorsque le pointeur de la souris est déplacé hors d'un élément HTML.|
|15|onmouseup|Il se produit ou se déclenche lorsque le bouton de la souris est relâché sur un élément HTML.|
|16|onreset|Il est utilisé par l'utilisateur pour réinitialiser le formulaire.|
|17|onselect|Il se produit après avoir sélectionné le contenu ou le texte sur une page Web.|
|18|onsubmit|Il est déclenché lorsque l'utilisateur clique sur un bouton après la soumission d'un formulaire.|
|19|onunload|Il se déclenche lorsque l'utilisateur ferme une page Web.|

## Références

* [HTML dynamique - Wikipédia](https://en.wikipedia.org/wiki/Dynamic_HTML)

