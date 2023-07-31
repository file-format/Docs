{
  "date" : "2019-10-11",
  "keywords" :[ "fichier vsdm", "format de fichier vsdm", "qu'est-ce qu'un fichier vsdm", "fichier", "exemple vsdm", "extension de fichier vsdm","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDM - Format de fichier de dessin Microsoft Visio",
  "description":"En savoir plus sur le format de fichier VSDM et les API qui peuvent créer et ouvrir des fichiers VSDM.",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsdm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier VSDM ?

Les fichiers avec l'extension .vsdm sont des fichiers de dessin créés avec l'application Microsoft Visio qui prend en charge les macros. Les fichiers VSDM sont des dessins OPC/XML similaires à VSDX mais offrent également la possibilité d'exécuter des macros lorsque le fichier est ouvert. Les macros sont des actions/étapes définies par l'utilisateur qui sont développées dans Visual Basic pour Applications (VBA) et peuvent être utilisées pour effectuer des tâches répétitives. Le format de fichier VSDM a été introduit avec le lancement de Microsoft Visio 2013. Les fichiers Visio sont utilisés pour créer des dessins contenant des objets visuels, des organigrammes, un diagramme UML, un flux d'informations, des organigrammes, des diagrammes de logiciels, la disposition du réseau, des modèles de base de données, le mappage d'objets et autres informations similaires. Les fichiers générés à l'aide de Visio peuvent également être exportés vers différents formats de fichiers tels que [PNG](/fr/image/png/), [BMP](/fr/image/bmp/), [PDF](/fr/pdf/) et autres.

## Format de fichier VSDM

Les fichiers VSDM sont basés sur les Open Packaging Conventions et XML et les développeurs peuvent bénéficier de ce format en apprenant à travailler avec ces fichiers par programmation. Le format hérite d'un grand nombre des mêmes structures XML que ses parties du format de fichier Visio XML Drawing (.vdx). L'interopérabilité avec les fichiers Visio est considérablement accrue car les logiciels tiers peuvent manipuler les fichiers Visio au niveau du format de fichier.

Chaque fichier Visio est appelé package contenant d'autres fichiers ou parties. Une partie de package peut être un fichier XML, une image ou même une solution VBA. Les parties du package peuvent être divisées en parties "document" et "relation".

### Document ###

Les parties de document contiennent le contenu réel et les métadonnées du fichier Visio, comme le nom du fichier, la première page et toutes les formes qu'il contient, et même les connexions de données pour les formes. Les images et les fichiers texte du package sont considérés comme des parties de document.

### Des relations ###

Les parties de relation d'un fichier Visio sont stockées dans le dossier "\_rels" et décrivent comment les parties du package sont liées à chacune. Il fournit également la structure du fichier. Un document XML autonome utilise la relation parent/enfant des éléments pour déterminer la relation des entités entre elles. Un format de fichier Visio 2013 valide contient le jeu correct de pièces et le package contient les relations entre les pièces.

Les parties de relation sont des documents XML qui décrivent les relations entre différentes parties de document au sein du package. Ils définissent une association entre deux éléments : une source spécifiée (définie par le nom et l'emplacement du fichier de relations) et une partie de document cible spécifiée. Par exemple, les parties de relation sont utilisées pour décrire quelles formes maîtresses sont associées au fichier, comment les pages sont liées au fichier et entre elles, ou comment les images et les objets sont liés à une page spécifique.

## Références ##

* [Introduction au format de fichier Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

