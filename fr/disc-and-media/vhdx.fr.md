{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"En savoir plus sur le format de fichier VHDX et les API qui peuvent créer et ouvrir des fichiers VHDX.",
  "title" :"Format de fichier VHDX - Qu'est-ce qu'un fichier VHDX ?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## Qu'est-ce qu'un fichier VHDX ?

Un fichier VHDX est un fichier image disque au format de fichier Virtual Hard Disk v2. Il contient un système d'exploitation complet qui peut être chargé et utilisé comme n'importe quelle machine normale pour tester des logiciels ou exécuter des logiciels nécessitant un système d'exploitation spécifique. Un VHDX, bien qu'il s'agisse d'une image disque complète, est stocké dans un seul fichier. Les logiciels de machine virtuelle tels que Parallels Desktop, Windows Virtual Machine et Virtual Box peuvent charger et ouvrir l'image disque.

Le fichier VHDX peut être converti en [VHD](/fr/disc-and-media/vhd/) avec Hyper-V Manager, ou en [VDI](/fr/disc-and-media/vdi/) avec VirtualBox.

## Format de fichier VHDX - Plus d'informations

Les détails du format de fichier VHDX sont entièrement documentés et disponibles en ligne sous [Spécifications du format de fichier VHDX](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477 ) sur la documentation Microsoft. Il s'agit d'une extension du format VHD et inclut des fonctionnalités améliorées. Le format de fichier VHDX fournit des fonctionnalités supplémentaires qui sont disponibles au niveau des couches de fichier du disque dur virtuel et du disque dur virtuel. Il est plus optimisé et donne de meilleurs résultats pour la configuration et les capacités du matériel de stockage. Les fichiers VHDX peuvent être ouverts

### Prise en charge des disques durs virtuels dans VHDX

Il prend en charge trois types de disques durs virtuels.

1. **Disque dur virtuel fixe** - Disque dur virtuel avec une taille de données fixe allouée. La taille du disque dur virtuel ne change pas avec l'ajout ou la suppression de données.

1. **Disque dur virtuel dynamique** - Disque dur virtuel avec une taille de disque dynamique. Sa taille est à tout moment aussi grande que les données réelles qui y sont écrites et les métadonnées. Sa taille de fichier augmente dynamiquement à mesure que des données y sont ajoutées ou supprimées.

1. **Disque dur virtuel de différenciation** - Représente le disque dur virtuel actuel sous la forme d'un ensemble de blocs modifiés par rapport à un fichier de disque dur virtuel parent.

## Références

* [Spécifications du format de fichier VHDX] (https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - par Wikipédia](https://en.wikipedia.org/wiki/VHD_(file_format))

