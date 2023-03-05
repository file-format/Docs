{
  "date" : "2021-08-17",
  "keywords" :[ "fichier udf", "format de fichier udf", "qu'est-ce qu'un fichier udf", "fichier", "exemple udf", "extension de fichier udf","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"En savoir plus sur le format de fichier UDF et les API qui peuvent créer et ouvrir des fichiers UDF.",
  "title" :"UDF - Fichier de format de disque universel",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## Qu'est-ce qu'un fichier UDF ?
Le fichier avec l'extension .udf est un format d'imagerie de disque généralement utilisé pour enregistrer des fichiers sur un support optique ; peut être utilisé pour graver des DVD, des CD et d'autres supports optiques ; stocke une collection de fichiers en utilisant la structure de répertoires spécifiée dans la norme UDF ; permet de supprimer et de modifier des fichiers sur le disque cible même après leur écriture. L'Optical Storage Technology Association a établi le système de fichiers UDF comme norme pour former un système de fichiers commun pour tous les supports optiques, tels que les supports optiques réinscriptibles et les supports en lecture seule.

## Format de fichier UDF
Le format de fichier UDF est un système de fichiers ouvert indépendant du fournisseur pour le stockage de données informatiques pour une large gamme de supports. Il a été couramment utilisé pour les DVD et les nouveaux formats de disques optiques. Habituellement, le logiciel maîtrise un système de fichiers UDF dans un processus par lots et l'écrit sur un support optique en une seule passe. Cependant, lorsqu'il écrit des paquets sur un support réinscriptible, l'UDF permet de créer, de supprimer et de modifier des fichiers sur le disque de la même manière qu'un système de fichiers à usage général le ferait sur des supports amovibles tels que des lecteurs flash ou des disquettes.
### Spécifications UDF
La norme UDF définit les trois variantes de système de fichiers suivantes :

- **Plain Build** : Il s'agit du format d'origine pris en charge dans toutes les révisions UDF. Introduit dans la première version de la norme, ce format peut être utilisé sur tout type de disque permettant un accès aléatoire en lecture ou en écriture, comme les DVD+RW, les disques durs et les supports DVD-RAM.
- **VAT build** : utilisé spécifiquement pour l'écriture sur un support non réinscriptible. La TVA est une structure supplémentaire sur le disque qui permet l'écriture par paquets ; c'est-à-dire remapper des blocs physiques lorsque des fichiers ou d'autres données sur le disque sont modifiés ou supprimés. Pour les supports à écriture unique, le disque entier est virtualisé, ce qui rend la nature à écriture unique transparente pour l'utilisateur ; le disque peut être traité de la même manière que l'on traiterait un disque réinscriptible.
- **Build épargné (RW)** : utilisé spécifiquement pour écrire sur un support réinscriptible. Il ajoute une table de réserve supplémentaire pour gérer les défauts qui se produiront éventuellement sur les parties du disque qui ont été réécrites plusieurs fois. Ce tableau enregistre la trace des secteurs usés et les remappe sur ceux qui fonctionnent. La gestion des défauts d'UDF ne s'applique pas aux systèmes qui implémentent déjà une autre forme de gestion des défauts, comme Mount Rainier (MRW) pour les disques optiques ou un contrôleur de disque pour un disque dur.
 




## Références


* [Format d'imagerie Windows - par Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


