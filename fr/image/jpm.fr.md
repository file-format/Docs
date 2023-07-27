{
  "date" : "2019-11-25",
  "keywords" :[ "fichier jpm", "format de fichier jpm", "qu'est-ce qu'un fichier jpm", "fichier", "exemple jpm", "extension de fichier jpm","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPM - Format de fichier composé JPEG 2000",
  "description":"En savoir plus sur le format de fichier JPM et les API qui peuvent créer et ouvrir des fichiers JPM.",
  "linktitle" : "JPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-08"
}

## Qu'est-ce qu'un fichier JPM ?

JPM fait référence au système de codage d'image JPEG 2000, partie 6, qui est utilisé pour l'imagerie de documents. Il est basé sur la norme de contenu raster mixte (ISO/IEC 16485) et contient des images fixes en couches qui utilisent JPEG 2000 et d'autres encodages. En plus de ses propres spécifications, le format de fichier JPM hérite des fonctionnalités de son parent, c'est-à-dire le format de fichier [jp2](/fr/image/jp2/).

## Format de fichier JPM

Le format de fichier JPM est défini par [ISO/IEC 15444-6:2003](https://www.iso.org/standard/61124.html) -- l'image JPEG 2000 système de codage -- Partie 6 : Format de fichier image composé. Une image composée peut contenir des images numérisées, des images synthétiques ou les deux, nécessitant une combinaison de méthodes de compression à tons continus et à deux niveaux. Le format de fichier JPM définit un modèle de composition qui décrit la méthode de combinaison de plusieurs images pour générer une image composée à l'aide du modèle d'imagerie multicouche Mixed Raster Content (MRC), défini dans ITU-T T.44 | ISO/CEI 16485.

### Spécifications JPM
La norme de format de fichier JPM spécifie qu'il s'agit d'un conteneur binaire pour représenter une image composée par laquelle plusieurs images peuvent être combinées en une seule image. Il définit le mécanisme de regroupement de plusieurs images dans une hiérarchie d'objets de mise en page, de pages et de collections de pages pour stocker JPEG 2000 et d'autres formats de données d'image compressées. Le format comprend le mécanisme d'incorporation des métadonnées (souvent appelées métadonnées structurelles dans les projets de bibliothèque numérique).

## Références

* [Rec. T.805](https://www.itu.int/rec/T-REC-T.805/en)
* [ISO/IEC 15444-6:2013](https://www.iso.org/standard/61124.html)
* [Wikipédia:JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000)

