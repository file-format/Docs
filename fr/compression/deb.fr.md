{
  "date" : "2021-04-08",
  "keywords" :[ "fichier deb", "format de fichier deb", "qu'est-ce qu'un fichier deb", "fichier", "exemple deb", "extension de fichier deb","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Archive tar compressée Bzip",
  "description":"En savoir plus sur le format de fichier DEB et les API qui peuvent créer et ouvrir des fichiers DEB.",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Qu'est-ce qu'un fichier DEB ?

Un fichier avec l'extension .deb est un format de fichier de package binaire Debian disponible pour la distribution de packages logiciels sur le système d'exploitation Linux. Il se compose de deux fichiers d'archive [TAR](/fr/compression/tar/). Le DPKG fournit le mécanisme pour lire et installer les packages DEB. Les packages DEB peuvent être installés à l'aide de l'interface de gestion du logiciel du package APT. Les fichiers DEB ont le type de média Internet comme `application/vnd.debian.binary-package`.

## Format de fichier DEB

Un fichier DEB se compose de deux fichiers d'archive [TAR](/fr/compression/tar/). Une archive contient les informations de contrôle et une autre contient les données installables.

### Organisation du paquet

Le fichier DEB est un fichier d'archive **ar** qui a une valeur magique de ` !<arch> `. Depuis Debian 0.93, le mécanisme d'archivage des fichiers DEB contient trois fichiers dans un ordre spécifique.

1. `Debian Binary` - Il est destiné à avoir une série de lignes, séparées par des retours à la ligne. À l'heure actuelle, une seule ligne est présente qui décrit le numéro de version. Le numéro de version actuel est 2.0.
1. `Control Archive` - Il contient une archive control.tar contenant des scripts de responsable et des méta-informations sur le paquet telles que le nom du paquet, la version, les dépendances et le responsable.
1. `Data Archive` - Il s'agit d'une archive tar nommée data.tar et contient les fichiers multimédias installables réels. L'archive peut être compressée avec gz, bz2, lzma ou xz, et l'extension de fichier de l'archive de données change en conséquence.

### Archive de contrôle

L'archive de contrôle peut inclure le contenu comme suit.

* `control` - Il contient une brève description du paquet ainsi que d'autres informations telles que ses dépendances.
* `md5sums` - Il contient les sommes de contrôle MD5 de tous les fichiers du package afin de détecter les fichiers corrompus ou incomplets.
* `conffiles` - Il répertorie les fichiers du paquet qui doivent être traités comme des fichiers de configuration. Les fichiers de configuration ne sont pas écrasés lors d'une mise à jour, sauf indication contraire.
* `preinst`, postinst, prerm et postrm - Scripts facultatifs exécutés avant ou après l'installation ou la suppression du package
* `config` est un script facultatif qui prend en charge le mécanisme de configuration debconf.
* `shlibs` - C'est une liste de dépendances de bibliothèques partagées.

## Références

* [DEB - Wikipédia](https://en.wikipedia.org/wiki/Deb_(file_format))
* [Format du paquet binaire Debian](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

