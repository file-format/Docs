{
  "date" : "2019-12-12",
  "keywords" :["KF8", "extension", "fichier", "format", "eBook", "Format de fichier Kindle", "Structure de fichier AZW3"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier AZW3 et les API qui peuvent créer et ouvrir des fichiers AZW3.",
  "title" :"Qu'est-ce qu'un fichier AZW3 ?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## Qu'est-ce qu'un fichier AZW3 ?

AZW3, également connu sous le nom de Kindle Format 8 (**KF8**), est la version modifiée du format de fichier numérique [AZW](/fr/ebook/azw/) développé pour les appareils Amazon Kindle. Le format est une amélioration des anciens fichiers AZW et est utilisé sur les appareils Kindle Fire uniquement avec une rétrocompatibilité pour le format de fichier ancêtre, c'est-à-dire [MOBI](/fr/ebook/mobi/) et AZW. Amazon a introduit le format KFX (KF version 10) après KF8 qui est utilisé sur les derniers appareils Kindle. Les fichiers AZW3 ont le type de média Internet application/vnd.amazon.mobi8-ebook. Les fichiers AZW3 peuvent être convertis en un certain nombre d'autres formats de fichiers tels que [PDF](/fr/pdf/), [EPUB](/fr/ebook/epub/), [AZW](/fr/ebook/azw/), [DOCX](/fr/ traitement de texte/docx/) et [RTF](/fr/traitement de texte/rtf/).

## Format de fichier AZ3/KF8 ##

Les fichiers KF8 sont de nature binaire et conservent la structure d'un format de fichier MOBI en tant que fichier PDB. Comme mentionné précédemment, un fichier KF8 peut être composé à la fois d'un MOBI et d'une version KF8 plus récente d'EPUB plus tard. Les détails internes du format ont été décodés par [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), qui est un script Python qui analyse la base de données compilée finale et en extrait les fichiers source MOBI ou AZW. Les fichiers AZW3 (KF8) ciblent également la version EPUB3 avec la rétrocompatibilité pour EPUB. KF8 compile les fichiers EPUB et génère une structure binaire basée sur le format de fichier PDB.

## Références ##

* [KF8 - Par Wikipédia](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle Unpack] (https://github.com/kevinhendricks/KindleUnpack)

