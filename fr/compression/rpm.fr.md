{
  "date" : "2021-04-08",
  "keywords" :[ "fichier rpm", "format de fichier rpm", "qu'est-ce qu'un fichier rpm", "file", "rpm example", "rpm file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - Fichier du gestionnaire de packages Red Hat",
  "description":"En savoir plus sur le format de fichier RPM et les API qui peuvent créer et ouvrir des fichiers RPM.",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Qu'est-ce qu'un fichier RPM ?

Un fichier avec l'extension .rpm est un package du système d'exploitation Red Hat Linux pour les installations de programmes sur les systèmes Linux. Le gestionnaire de packages Red Hat utilise le format de fichier RPM et est un système de gestion de packages gratuit et open source. Bien que les fichiers RPM puissent être utilisés tels quels pour l'installation de programmes, ceux-ci peuvent être convertis en d'autres formats de packages tels que [DEB](/fr/compression/deb/) à l'aide du programme Debian appelé Alien.

## Format de fichier RPM

Un fichier RPM est un binaire qui peut contenir un ensemble de fichiers. La plupart du temps, les fichiers RPM sont des "RPM binaires" qui sont les exécutables compilés du logiciel. Le fichier RPM peut contenir des RPM source (SRPM) qui peuvent être utilisés pour créer le package à partir du code source. Le format de fichier RPM se compose de quatre sections.

* Lead - Il identifie le fichier en tant que fichier RPM
* Signature - Elle peut être utilisée pour garantir l'intégrité et/ou l'authenticité
* En-tête - Contient des métadonnées, notamment le nom du package, la version, l'architecture, la liste des fichiers, etc.
* File Archive - Également connu sous le nom de charge utile, qui est généralement au format cpio, compressé avec [GZIP](/fr/compression/gz/)

## Références

* [RPM - Wikipédia](https://rpm.org)
* [Documentation RPM](https://rpm.org/documentation.html)

