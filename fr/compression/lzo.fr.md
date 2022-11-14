{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "Compressé", "Fichier", "Extension", "Format de fichier", "Lempel-Ziv-Oberhume" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier LZO",
  "description":"En savoir plus sur le format de fichier LZO et les API qui peuvent créer et ouvrir des fichiers LZO.",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Qu'est-ce qu'un fichier LZO ? ##

Un fichier avec l'extension .lzo est combiné avec des fonctionnalités d'archivage de fichiers qui peuvent réduire la taille de tous les fichiers dans le fichier compressé. Tous les fichiers compressés peuvent comprendre un ou plusieurs fichiers voire des groupes de classeurs avec plusieurs fichiers de nature et de dimensions différentes. La taille d'un fichier compressé est inférieure à la taille commune de tous les fichiers et dossiers stockés dans un fichier compressé LZO. Tous les fichiers compressés LZO sont stockés au format LZO et sont explicitement exécutés avec les fonctionnalités de compression utilisées par le logiciel de compression et de décompression de fichiers LZOP. Toutes les spécifications de compression sont combinées dans ce programme de compression et de décompression de fichiers qui provient de la bibliothèque de compression de fichiers Lempel-Ziv-Oberhume. Une vitesse de décompression plus rapide et des taux de compression développés sont également combinés dans ces fichiers LZO.

## Spécification LZO ##

Markus Franz Xaver Johannes Oberhumer a développé l'algorithme "lzop" original, basé sur des algorithmes antérieurs d'Abraham Lempel et Jacob Ziv, en 1996. Cette bibliothèque implémente une variété d'algorithmes avec les caractéristiques suivantes :

* Compression plus rapide que DEFLATE
* Décompression rapide
* Tampons supplémentaires nécessaires lors de la compression (de taille 8 Ko ou 64 Ko, selon le niveau de compression)
* Les tampons source et destination représentent toute la mémoire nécessaire à la décompression
* Fournit un contrôle sur le taux de compression et la vitesse de compression

En tant qu'algorithme de compression de bloc, LZO effectue une compression superposée ainsi qu'une décompression sur place. Pour obtenir une compression superposée, la taille de bloc de compression et de décompression doit correspondre. L'algorithme de compression LZO divise les données d'entrée en correspondances (un dictionnaire glissant) et en littéraux qui ne correspondent pas, donnant de bons résultats avec des données hautement redondantes et des résultats acceptables avec des données non compressibles, augmentant seulement les données incompressibles de 1/64 de l'original Taille.

## Problèmes pour ouvrir un fichier LZO ##

Voici les quelques problèmes qui peuvent entraîner un mauvais fonctionnement du format de fichier LZO :
  


* Le fichier peut être corrompu. Pour résoudre ce problème, téléchargez à nouveau le fichier ou demandez à l'expéditeur de renvoyer le fichier à nouveau
* La deuxième raison est le fichier infecté dans ce cas, analysez le fichier correctement
* Liens incorrects vers le fichier LZO
* Suppression de la description du LZO
* Pas assez de ressources matérielles
* Pilotes obsolètes de l'équipement
  


## Références ##

* [LZO - Par Wikipédia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

