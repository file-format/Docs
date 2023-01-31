{
  "date" : "2022-11-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AVL - Fichier de légende ArcView",
  "description":"En savoir plus sur le format de fichier AVL et les API qui peuvent créer et ouvrir des fichiers AVL.",
  "linktitle" : "AVL",
  "menu" : {
    "docs" : {
      "identifier":"gis-avl",
      "parent" : "gis"
}
},
  "lastmod" : "2022-11-30"
}

## Qu'est-ce qu'un fichier AVL ?

Un fichier AVL est un fichier de légende qui contient une clé pour une carte générée avec le logiciel ESRI ArcView GIS (Geographic Information System). Il contient des informations de symbologie de référence utilisées dans la carte correspondante pour l'accès. Un fichier AVL peut contenir plus d'informations telles que la symbologie, les paramètres d'affichage, tels que la transparence, les propriétés d'affichage dépendantes de l'échelle, les informations sur la table jointe/liée, la requête de définition, les propriétés d'étiquetage pour les couches d'entités et les propriétés d'affichage d'annotation pour les couches d'annotations en fonction du type. sorte de couche.

Un fichier AVL peut être référencé à partir du fichier du projet ArcView [.APR](/fr/gis/apr/).

## Format de fichier AVL - Plus d'informations

Les fichiers AVL sont enregistrés au format de fichier texte brut. Cela signifie que vous pouvez ouvrir des fichiers AVL dans n'importe quel éditeur de texte tel que Notepad, Notepad ++ et Apple TextEdit. Une fois ouvert, vous pouvez non seulement visualiser le contenu du fichier mais aussi le modifier.

### Différence entre les fichiers .LYR et .AVL

* **Différence de format de fichier** - .lyr est un fichier binaire alors que .avl est un fichier texte
* ** Différence de contenu ** - Un fichier .lyr contient plus d'informations qu'un fichier .avl. Un fichier AVL stocke uniquement les informations de symbologie, tandis qu'un fichier LYR stocke toutes les informations disponibles dans la boîte de dialogue des propriétés de la couche dans ArcMap.

## Références

* [Différence entre les fichiers .lyr et .avl](https://support.esri.com/en/technical-article/000005936)

