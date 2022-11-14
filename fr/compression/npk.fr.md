{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier NPK",
  "description":"En savoir plus sur le format de fichier NPK et les API qui peuvent créer et ouvrir des fichiers NPK.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## Qu'est-ce qu'un fichier NPK ?

Un fichier NPK est un fichier de package de mise à niveau logicielle utilisé par les routeurs **MikroTik** pour la mise à niveau du système d'exploitation du routeur. Il s'agit d'une archive binaire compressée chargée dans le routeur pour l'installation des mises à jour logicielles. Les informations contenues dans un fichier NPK incluent des informations réseau telles que l'adresse IP et le service IP, les informations sur les connecteurs (interfaces Ethernet et port série), la configuration de la messagerie, la configuration du pont et la gestion des utilisateurs locaux.

## Format de fichier NPK

Les fichiers NPK sont stockés sous forme d'archive binaire compressée. Il s'agit d'un format de fichier fermé utilisé uniquement par MikroTik. Il n'est pas prévu de créer des modules complémentaires RouterOS via des tiers. Les fichiers NPK sont conservés par MikroTik lui-même et des versions mises à niveau de ceux-ci peuvent être téléchargées à partir des sections de téléchargement du site Web [MikroTik](https://mikrotik.com/download).

Lorsqu'un fichier NPK est téléchargé sur un routeur, le système d'exploitation du routeur n'entre en vigueur que s'il est redémarré. Par conséquent, un redémarrage est nécessaire pour que le système d'exploitation du routeur soit mis à niveau.

## Références

* [MikroTik - Mise à niveau du système d'exploitation du routeur] (https://mikrotik.com/download)
* [Comment créer des fichiers NPK] (https://forum.mikrotik.com/viewtopic.php?t=87126)

