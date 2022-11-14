{
  "date" : "2019-12-12",
  "keywords" :[ "EPUB", "fichier", "extension", "format", "E-Book", "Livre numérique" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier EPUB et les API qui peuvent créer et ouvrir des fichiers EPUB.",
  "title" :"Qu'est-ce qu'un fichier EPUB ?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Qu'est-ce qu'un fichier EPUB ?

Les fichiers avec l'extension .epub sont un format de fichier de livre électronique qui fournit un format de publication numérique standard pour les éditeurs et les consommateurs. Le format est maintenant si courant qu'il est pris en charge par de nombreux lecteurs électroniques et applications logicielles. Par exemple, sur Mac OS, le logiciel **Books** préinstallé fournit la prise en charge pour l'ouverture de ces fichiers. De plus, de nombreux logiciels compatibles sont disponibles pour les smartphones, les tablettes et les ordinateurs. Les normes de fichiers EPUB sont gérées par le [International Digital Publishing Forum](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). La version EPUB 3 est également approuvée par le Book Industry Study Group (BISG), une association commerciale de premier plan pour les meilleures pratiques normalisées, la recherche, l'information et les événements, pour l'emballage du contenu.

## Bref historique du format de fichier EPUB

* **Octobre 2007** - EPUB 2.0 a été approuvé
* **Septembre 2010** - La mise à jour de maintenance a été publiée
* **Octobre 2011** - Les spécifications EPUB 3.0 sont entrées en vigueur
* **Juin 2014** - Une mise à jour de maintenance mineure a été publiée pour remplacer la version 3.0
* **Janvier 2017** - EPUB 3.1 est entré en vigueur

## Format de fichier EPUB

Le format de fichier EPUB est une archive qui peut être renommée en extension [ZIP](/fr/compression/zip/) et son contenu peut être visualisé en extrayant l'archive avec n'importe quel extracteur d'archive. Il s'agit d'un format ouvert basé sur XML et composé de fichiers HTML, d'images, de feuilles de style CSS et d'autres éléments. Il peut également être converti en PDF, Mobi et plusieurs autres formats de fichiers via un certain nombre d'applications logicielles et d'API.

{{< figure src="../epub.png" alt="Format de fichier EPUB" >}}

**E-Book EPUB ouvert avec l'application Mac OS Books**

Le format de fichier EPUB est basé sur les trois normes ouvertes suivantes.

### Structure Publique Ouverte (OPS) ###

Un fichier EPUB 2.0 utilise XHTML 1.1 pour construire le contenu d'une publication. Cela signifie essentiellement qu'un fichier EPUB se compose d'une ou plusieurs pages Web. Même si vous pouvez inclure tout le contenu d'un livre ou d'un journal sur une seule page, il est préférable qu'un tel fichier ne dépasse pas 300K, à la fois pour des raisons de performances et de compatibilité. Comme pour les pages Web classiques, le style et la mise en page sont définis à l'aide de feuilles de style en cascade (CSS). Dans les fichiers EPUB, un sous-ensemble (série limitée de commandes) de CSS2 doit être utilisé. De nombreuses nouvelles fonctionnalités de CSS3, telles que les cases arrondies ou les ombres portées, ne sont pas encore disponibles. Pour une compatibilité descendante, un créateur peut également utiliser DTBook au lieu de XHTML pour encoder le contenu.

### Format d'emballage ouvert (OPF) ###

Cette partie des spécifications traite des informations structurelles telles que les métadonnées (qui est l'auteur et l'éditeur, quel est le titre, ..), le manifeste (une liste de tous les fichiers à l'intérieur d'un fichier epub) et la table des matières. Ces données sont toutes intégrées à l'aide de XML.

### Format de conteneur ouvert (OCF) ###

Comme les descriptions ci-dessus auraient dû le préciser, un document EPUB se compose d'une série de fichiers. Les spécifications OCF définissent comment tous ces fichiers finissent par être regroupés dans un seul fichier conteneur. La compression ZIP est utilisée pour cela.

## Formats de fichiers image pris en charge ##

Le format de fichier EPUB prend en charge les formats de fichier image suivants.

* [GIF](/fr/image/gif/)
* [JPG](/fr/image/jpeg/)
* [PNG](/fr/image/png/)
* [SVG](/fr/page-description-language/svg/)

## Références ##

* [EPUB - Par Wikipédia](https://en.wikipedia.org/wiki/EPUB)

