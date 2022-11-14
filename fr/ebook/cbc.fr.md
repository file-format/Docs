{
  "date" : "2019-12-12",
  "keywords" :[ "CBC", "extension", "fichier", "format", "Bandes dessinées", "Format de fichier de bandes dessinées", "eBook" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier CBC et les API qui peuvent créer et ouvrir des fichiers CBC.",
  "title" :"CBC - Format de fichier de collection de bandes dessinées",
  "linktitle" : "CBC",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-03"
}

## Qu'est-ce qu'un fichier CBC ?

Un fichier avec l'extension .cbc est une collection compressée de fichiers de bandes dessinées pour les livres électroniques et contient des fichiers [CBZ](/fr/ebook/cbz/) et [CBR](/fr/ebook/cbr/). Il est utilisé par [Calibre](https://calibre-ebook.com/), une application de conversion de livres électroniques, qui est un gestionnaire de livres électroniques open source multiplateforme et vous permet de gérer vos livres électroniques et de les convertir en différents formats. . Un fichier CBC contient un fichier .txt, comics.txt, qui répertorie les autres fichiers faisant partie de l'archive. Plusieurs applications sont disponibles en ligne pour convertir les fichiers CBC en [AZW3](/fr/ebook/azw3), [EPUB](/fr/ebook/epub/), [FB2](/fr/ebook/fb2/), [MOBI](/fr/ebook/ mobi/), [TXT](/fr/word-processing/txt/), [PDF](/fr/pdf/) et d'autres formats de fichiers populaires.

## Format de fichier SRC

Les fichiers CBC sont des archives compressées qui contiennent CBZ, CBR et un fichier texte pour répertorier le contenu. Le fichier texte, comics.txt est encodé en UTF8 et contient une liste des fichiers CBC à utiliser par les lecteurs pour organiser leurs collections. Un fichier CBC a généralement plusieurs attributs qui permettent l'organisation de cette collection tels que Comic, Category, Publisher, Series, Edition et Artist.

Le contenu d'un exemple de fichier CBC est répertorié comme suit :

* comics.txt - Fichier texte contenant la liste des fichiers CBR et CBZ
* 1.cbz
* 2.cbz
* 3.cbz
* Fichier(s) CBZ

où le fichier comics.txt répertorie le contenu comme suit :

* 1.cbz : premier chapitre
* 2.cbz : deuxième chapitre
* 3.cbz : troisième chapitre

Les lecteurs traitent le fichier comics.txt et génèrent la table des matières en fonction des données fournies.

## Références

* [Calibre](https://calibre-ebook.com/)

