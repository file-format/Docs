{
  "date" : "2021-04-08",
  "keywords" :[ "fichier lzma", "format de fichier lzma", "qu'est-ce qu'un fichier lzma", "fichier", "exemple lzma", "extension de fichier lzma","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - Format de fichier compressé LZMA",
  "description":"Qu'est-ce qu'un fichier LZMA et les API qui peuvent créer et ouvrir des fichiers LZMA.",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## Qu'est-ce qu'un fichier LZMA ?

Un fichier avec l'extension .lzma est un fichier d'archive compressé créé à l'aide de la méthode de compression LZMA (algorithme de chaîne de Lempel-Ziv-Markov). Ceux-ci sont principalement trouvés/utilisés sur le système d'exploitation Unix et sont similaires à d'autres algorithmes de compression tels que [ZIP](/fr/compression/zip/) pour minimiser la taille du fichier. LZMA est un format de fichier hérité, qui est ou a été remplacé par le format .xz. Le type MIME du format .lzma est \`application/x-lzma'. Ce format de fichier a été conçu par Igor Pavlov pour être utilisé dans le SDK LZMA.

## Format de fichier LZMA

Le fichier LZMA se compose de deux parties principales :

1. En-tête
1. Données compressées


### En-tête LZMA

Les fichiers LZMA ont un en-tête de 13 octets qui est suivi des données compressées LZMA. L'en-tête LZMA se compose de :

* Propriétés
* Taille du dictionnaire
* Taille non compressée

#### Propriétés de l'en-tête LZMA

Le champ Propriétés contient trois propriétés. Une abréviation est indiquée entre parenthèses, suivie de la plage de valeurs de la propriété. Le domaine est composé de

1) le nombre de bits de contexte littéral (lc, [0, 8]);
2) le nombre de bits de position littérale (lp, [0, 4]); et
3) le nombre de bits de position (pb, [0, 4]).

#### Taille du dictionnaire LZMA

Ceci est stocké sous la forme d'un entier petit boutien 32 bits non signé avec des valeurs comprises entre 2 ^ n et 2 ^ n + 2 ^ (n-1). LZMA Utils peut décompresser des fichiers avec n'importe quelle taille de dictionnaire.

#### Taille non compressée
La taille non compressée est stockée sous forme d'entier little endian 64 bits non signé. Une valeur spéciale de 0xFFFF_FFFF_FFFF_FFFF indique que la taille non compressée est inconnue. La valeur est représentée par le marqueur de fin de charge utile (\*) si et seulement si la taille non compressée est inconnue.

## Références

* [Algorithme de chaîne Lempel–Ziv–Markov](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)
