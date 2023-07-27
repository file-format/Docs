{
  "date" : "2021-01-21",
  "keywords" :[ "fichier ai", "format de fichier ai", "qu'est-ce qu'un fichier ai", "fichier", "exemple ai", "extension de fichier ai","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI - Fichier d'illustration Adobe Illustrator",
  "description":"En savoir plus sur le format de fichier AI et les API qui peuvent créer et ouvrir des fichiers AI.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## Qu'est-ce qu'un fichier AI ?

Un fichier avec une extension .ai est un fichier Adobe Illustrator Artwork qui contient des graphiques vectoriels sur une seule page. il utilise des points pour créer des chemins pour afficher les données d'image, ce qui le protège contre la perte de qualité d'image si elle est agrandie. Le format de fichier AI est basé sur le format de fichier PGF qui est similaire aux fichiers AI. Le format AI trouve son utilisation principale pour les logos et les supports d'impression, et ses versions initiales étaient considérées comme similaires à celles des fichiers [EPS](/fr/page-description-language/eps/). Les fichiers AI peuvent être ouverts avec les outils Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro et CorelDraw Graphics.

## Format de fichier IA

AI est le format de fichier propriétaire d'Adobe Illustrator et utilise l'approche à double chemin similaire à PGF pour enregistrer des fichiers compatibles EPS. Les [spécifications du format de fichier Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) fournissent une référence du développeur pour les détails internes de ce format de fichier. Tous Les documents (fichiers) créés par Adobe Illustrator sont des documents en langage PostScript et comportent deux parties principales conformes aux conventions de structuration des documents : un "prologue" et un "script".

### Prologue

La section prolog encapsule les informations nécessaires à l'interprétation du fichier. Un exemple serait la zone de délimitation qui contient toutes les marques sur la page. Il contient également des informations sur les ressources telles que les polices et les définitions de procédure. Ces ressources sont logiquement regroupées en ensembles appelés procsets et contiennent des méthodes explicites pour initialiser et terminer leurs procédures.

### Scénario

Les éléments graphiques de la page sont décrits par le script. Un script contient des références aux opérateurs et aux procédures du prologue, ainsi que des opérandes et des données. Les trois sections logiques d'un script incluent :

* Séquence d'installation - qui initialise et active les ressources définies dans le prologue
* Séquence d'opérateurs descriptifs
* Bande-annonce qui désactive les ressources

Les opérateurs du script sont des séquences d'éléments graphiques écrits dans le langage défini par les procsets du prologue. Ces séquences sont constituées de collections d'éléments de données, de définitions d'attributs graphiques et d'appels aux procédures définies dans les procsets.

### Balises d'objets

Les balises d'objet sont utilisées pour attacher des informations personnalisées à un objet d'art Adobe Illustrator. Les balises se composent d'un :

* Identifiant de balise
*Type de balise
* Données

## Références
* [Spécifications du format de fichier Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [Format de fichier AI par PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)

