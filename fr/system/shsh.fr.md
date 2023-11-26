{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier SHSH - Format de fichier Blob SHSH pour iPhone/iPod Touch",
  "description":"Découvrez ce qu'est un fichier SHSH.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Qu'est-ce qu'un fichier SHSH ?

Un fichier SHSH, également connu sous le nom de Signature HaSH, est une signature numérique utilisée par Apple pour authentifier et vérifier les mises à jour du micrologiciel des appareils iOS tels que les iPhones, iPads et iPods.

## Différence entre les formats de fichiers SHSH et SHSH2

Comme un fichier SHSH2, le fichier SHSH contient un identifiant unique pour l'appareil appelé « ECID » (Exclusive Chip ID), ainsi que des informations sur la version du firmware installée sur l'appareil. Cependant, les fichiers SHSH étaient utilisés dans les anciennes versions d'iOS (avant iOS 10) et ont depuis été remplacés par des fichiers SHSH2.

## Format de fichier SHSH - Plus d'informations

Les fichiers SHSH sont enregistrés sur le disque au format de fichier binaire. Les détails de la structure de fichier interne de ce format de fichier ne sont pas disponibles publiquement.

Les fichiers SHSH sont importants pour les utilisateurs qui souhaitent rétrograder le micrologiciel de leur appareil vers une version précédente qui n'est plus signée par Apple. En enregistrant les fichiers SHSH pour une version spécifique du micrologiciel alors qu'il est encore signé par Apple, les utilisateurs peuvent les utiliser ultérieurement pour contourner la vérification de signature d'Apple et installer cette version du micrologiciel sur leur appareil. Ce processus est également connu sous le nom de « jailbreak ».

## Les références

* [SHSH Blob - Par Wikipédia](https://en.wikipedia.org/wiki/SHSH_blob)
* [Épargnant TSS](https://tsssaver.1conan.com/v2/)

