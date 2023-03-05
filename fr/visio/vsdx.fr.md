{
  "date" : "2019-10-11",
  "keywords" :[ "fichier vsdx", "format de fichier vsdx", "qu'est-ce qu'un fichier vsdx", "fichier", "exemple vsdx", "extension de fichier vsdx","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDX",
  "description":"En savoir plus sur le format de fichier VSDX et les API qui peuvent créer et ouvrir des fichiers VSDX.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier VSDX ?

Les fichiers avec l'extension .vsdx représentent le format de fichier Microsoft Visio introduit à partir de Microsoft Office 2013. Il a été développé pour remplacer le format de fichier binaire, [.VSD](/fr/image/vsd/), qui est pris en charge par les versions antérieures de Microsoft Visio. Il est également pris en charge sur Visio Services dans Microsoft SharePoint Server 2013 et ne nécessite pas de format de fichier intermédiaire pour la publication sur SharePoint Server. Les fichiers Visio sont utilisés pour créer des dessins contenant des objets visuels, des organigrammes, un diagramme UML, un flux d'informations, des organigrammes, des diagrammes de logiciels, la disposition du réseau, des modèles de base de données, le mappage d'objets et d'autres informations similaires. Les fichiers générés à l'aide de Visio peuvent également être exportés vers différents formats de fichiers tels que [PNG](/fr/image/png/), [BMP](/fr/image/bmp/), [PDF](/fr/pdf/) et autres.

## Format de fichier ##

Les fichiers VSDX sont basés sur les conventions Open Packaging et XML et les développeurs peuvent bénéficier de ce format en apprenant à travailler avec ces fichiers par programmation. Le format hérite d'un grand nombre des mêmes structures XML que ses parties du format de fichier Visio XML Drawing (.vdx). L'interopérabilité avec les fichiers Visio est considérablement accrue car les logiciels tiers peuvent manipuler les fichiers Visio au niveau du format de fichier.

Certains autres types de fichiers qui composent le format de fichier Visio 2013 incluent :

* .vsdm (dessin compatible avec les macros Visio)
* .vssx (gabarit Visio)
* .vssm (gabarit prenant en charge les macros Visio)
* .vstx (modèle Visio)
* .vstm (modèle compatible avec les macros Visio)

Sous le capot, le format de fichier Visio 2013 utilise un moyen structuré pour stocker les données d'application avec les ressources associées dans une archive telle que [ZIP](/fr/compression/zip/). Le fichier ZIP peut être extrait à l'aide de n'importe quel utilitaire d'extraction standard où il contient également d'autres types de fichiers. Vous pouvez simplement remplacer l'extension de fichier .vsdx par .zip dans l'exploration de Windows pour voir le contenu du fichier VSDX.

Chaque fichier Visio est appelé package contenant d'autres fichiers ou parties. Une partie de package peut être un fichier XML, une image ou même une solution VBA. Les parties du package peuvent être divisées en parties "document" et "relation".

### Document ###

Les parties de document contiennent le contenu réel et les métadonnées du fichier Visio, comme le nom du fichier, la première page et toutes les formes qu'il contient, et même les connexions de données pour les formes. Les images et les fichiers texte du package sont considérés comme des parties de document.

### Des relations ###

Les parties de relation d'un fichier Visio sont stockées dans le dossier "\_rels" et décrivent comment les parties du package sont liées à chacune. Il fournit également la structure du fichier. Un document XML autonome utilise la relation parent/enfant des éléments pour déterminer la relation des entités entre elles. Un format de fichier Visio 2013 valide contient le jeu correct de pièces et le package contient les relations entre les pièces.

Les parties de relation sont des documents XML qui décrivent les relations entre différentes parties de document au sein du package. Ils définissent une association entre deux éléments : une source spécifiée (définie par le nom et l'emplacement du fichier de relations) et une partie de document cible spécifiée. Par exemple, les parties de relation sont utilisées pour décrire quelles formes maîtresses sont associées au fichier, comment les pages sont liées au fichier et entre elles, ou comment les images et les objets sont liés à une page spécifique.

## Références ##

* [Introduction au format de fichier Visio](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

