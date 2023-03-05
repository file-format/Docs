{
  "date" : "2019-10-11",
  "keywords" :[ "fichier odg", "format de fichier odg", "qu'est-ce qu'un fichier odg", "fichier", "exemple odg", "extension de fichier odg","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier ODG",
  "description":"En savoir plus sur le format de fichier ODG et les API qui peuvent créer et ouvrir des fichiers ODG.",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier ODG ?

Le format de fichier ODG est utilisé par l'application Draw d'Apache OpenOffice pour stocker les éléments de dessin sous forme d'image vectorielle. Il suit les spécifications de format de fichier basées sur XML décrites par Advancement of Structural Information Standards (OASIS). ODG représente les dessins sous forme d'images vectorielles à l'aide de points, de lignes et de courbes. Outre OpenOffice, LibreOffice et d'autres applications prennent également en charge le travail avec le format de fichier ODG. Les autres formats pris en charge par OpenOffice, par exemple, incluent [ODT](/fr/word-processing/odt/), ODF, [ODP](/fr/presentation/odp/) et [ODS](/fr/spreadsheet/ods/).


## Spécifications du format de fichier ODG

Le format de fichier ODG est basé sur le format OpenDocument qui est un format de document XML structuré avec un schéma bien défini.
Chaque composant structurel d'un format OpenDocument est représenté par un élément auquel sont associés des attributs. La structure basée sur XML est commune à tous les types de documents tels qu'un document texte, une feuille de calcul ou un fichier de dessin. Un document peut contenir différents styles. Une structure de fichier OpenDocument se compose des éléments suivants.
* Racine du document
* Métadonnées du document
* Types d'élément de corps et de document
* Paramètres de l'application
* Scénarios
* Déclarations de police de caractères
* Modes
* Styles de page et mises en page

## Racines du document ##

Un élément racine de document contient le document entier et est l'élément principal d'un fichier au format OpenDocument. Les mêmes types d'éléments racine de document s'appliquent à tous les types de documents tels que le texte, les documents, les feuilles de calcul et les documents de dessin.

### Éléments racine ###
Un document XML unique est représenté par son propre élément racine. Les cinq différents éléments racine pris en charge sont les suivants.

`<office:document> ` - Document bureautique complet dans un seul document XML.
`<office:document-content> ` - Contenu du document et styles automatiques utilisés dans le contenu.
`<office:document-styles> ` - Styles utilisés dans le contenu du document et styles automatiques utilisés dans les styles eux-mêmes.
`<office:document-meta> ` - Documenter les méta-informations, telles que l'auteur ou l'heure de la dernière action d'enregistrement.
`<office:document-settings> ` - Paramètres spécifiques à l'application, tels que la taille de la fenêtre ou les informations sur l'imprimante.

### Métadonnées de document ODG ###
L'OpenDocument contient tous les éléments de métadonnées dans le \<office:meta> élément. Ces informations générales sur un document sont contenues au début du document et les applications peuvent mettre à jour plusieurs instances des mêmes éléments.

### Élément de corps et types de document ###
Le corps du document indique le type de contenu contenu dans le document à l'aide de l'élément de type de document. Ces types de documents sont :
* documents texte
* documents de dessin
* documents de présentation
* feuilles de calcul
* documents graphiques
* documents images

### Paramètres de l'application ###
Les paramètres des applications bureautiques représentent différents paramètres liés à la configuration du document ou à l'apparence visuelle du document. Chaque catégorie est représentée par un `<config:config-item-set> `. Voici des exemples de ces catégories de paramètres :
* Paramètres du document, par exemple l'imprimante par défaut
* Afficher les paramètres, par exemple le niveau de zoom

### Scénarios ###
Il est courant qu'un document contienne plusieurs scripts. Chaque script dans un fichier OpenDocument est représenté par un `<office:script> `élément. Ces éléments de script sont contenus dans un seul `<office:scripts> `élément. Les scripts ne mettent pas à jour un document pendant le chargement du document.
### Déclarations des polices ###

Une déclaration de police contient des informations sur les polices utilisées par l'auteur d'un document. Ces informations permettent de localiser ces polices sur d'autres systèmes.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Modes ###
Les styles suivants sont pris en charge par le format OpenDocument.

`Styles communs` - Les représentations XML de ces styles sont appelées styles
`Styles automatiques` - Contient des propriétés de formatage qui, dans la vue de l'interface utilisateur d'un document, sont attribuées à un objet tel qu'un paragraphe.
`Mater Styles` - un style commun qui contient des informations de formatage et du contenu supplémentaire qui s'affiche avec le contenu du document lorsque le style est appliqué. Un exemple de style maître sont les pages maîtres.

## Références ##
* [Format de document ouvert OASIS pour les applications Office](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Format OpenDocument - Wikipédia](https://en.wikipedia.org/wiki/OpenDocument)

