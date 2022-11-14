{
  "date" : "2021-04-08",
  "keywords" :[ "fichier dar", "format de fichier dar", "qu'est-ce qu'un fichier dar", "fichier", "exemple dar", "extension de fichier dar","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - Format de fichier de l'archiveur de disque",
  "description":"En savoir plus sur le format de fichier DAR et les API qui peuvent créer et ouvrir des fichiers DAR.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Qu'est-ce qu'un fichier DAR ?

Un fichier avec l'extension .dar est une archive compressée créée à l'aide de l'archive DAR Disk. Il peut créer une sauvegarde/archivage pour un disque complet ou un groupe de fichiers. Il a été créé pour remplacer le format de fichier [TAR](/fr/compression/tar/) sur le système d'exploitation UNIX et peut être créé en tant que fichiers d'archive fractionnés pour un grand nombre de fichiers. L'archive DAR prend en charge l'option de suppression des fichiers du système qui sont liés aux fichiers principaux de l'archive. Ses capacités de fournir une sauvegarde différentielle, incrémentielle et décrémentielle le rendent supérieur aux fichiers TAR.

## Format de fichier DAR

Les fichiers DAR sont des archives compressées qui peuvent utiliser n'importe quelle compression par fichier telle que [gzip](/fr/compression/gz/), [bzip2](/fr/compression/bz2/), lzo, xz ou lzma. Le format de fichier exact d'un fichier DAR dépend du type de formatage utilisé pour compresser le contenu de l'archive. Il permet également le cryptage optionnel Blowfish, Twofish, AES, Serpent, Camellia, ainsi que le cryptage et la signature à clé publique (OpenPGP).

### Fonctionnalités DAR

Certaines des fonctionnalités du format de fichier DAR sont les suivantes.

* Prend en charge tout type d'inode (répertoire, fichiers simples, liens symboliques, périphériques spéciaux, tubes nommés, sockets, portes, ...)
* Prend en charge les inodes liés en dur (fichiers simples liés en dur, périphériques char, périphériques de bloc, liens symboliques liés en dur)
* Prend soin des fichiers clairsemés
* Prend en charge les attributs étendus du fichier Linux,
* Prend en charge le fichier ACL Linux
* Prend en charge les fourches de fichiers Mac OS X
* Prend en charge certains attributs spécifiques au système de fichiers, tels que la date de naissance du système de fichiers HFS + et les attributs immuables, de journalisation des données, de suppression sécurisée, de fusion sans queue, non supprimables et noatime du système de fichiers ext2/3/4.
* Compression par fichier avec gzip, bzip2, lzo, xz ou lzma (par opposition à la compression de l'archive entière). Un individu peut choisir de ne pas compresser les fichiers déjà compressés en fonction de leur suffixe de nom de fichier.
* Extraction rapide des fichiers de n'importe où dans l'archive
* Liste rapide du contenu de l'archive grâce à l'enregistrement du catalogue de fichiers dans l'archive
* Sauvegarde en direct du système de fichiers : détecte lorsqu'un fichier a été modifié alors qu'il était lu pour la sauvegarde et peut réessayer de l'enregistrer jusqu'à un nombre maximum donné de tentatives
* Fichier de hachage (MD5, SHA1 ou SHA-512) généré à la volée pour chaque tranche, le fichier résultant est compatible avec md5sum ou sha1sum, pour pouvoir vérifier rapidement l'intégrité de chaque tranche
* Indépendant du système de fichiers : il peut être utilisé pour restaurer un système sur une partition de taille différente et/ou sur une partition avec un système de fichiers différent[5]

## Références

* [DAR](http://dar.linux.free.fr/)
* [Archiveur de disque DAR](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

