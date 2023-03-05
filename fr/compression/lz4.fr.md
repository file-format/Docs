{
  "date" : "2021-04-08",
  "keywords" :[ "fichier lz4", "format de fichier lz4", "qu'est-ce qu'un fichier lz4", "fichier", "exemple lz4", "extension de fichier lz4","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ4 - Format de fichier compressé LZ4",
  "description":"En savoir plus sur le format de fichier LBR et les API qui peuvent créer et ouvrir des fichiers LZ4.",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Qu'est-ce qu'un fichier LZ4 ?

Un fichier avec l'extension .lz4 est un fichier d'archive compressé créé avec des applications/utilitaires prenant en charge la compression [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)). L'algorithme LZ4 se concentre sur le compromis entre la vitesse et le taux de compression. Les archives LZ4 compressées peuvent être créées à l'aide de l'utilitaire de ligne de commande LZ4 et peuvent être décompressées à l'aide de celui-ci.

## Format de fichier LZ4

Le format de fichier LZ4, basé sur l'algorithme de compression LZ4, est indépendant du type de processeur, du système d'exploitation, du système de fichiers et du jeu de caractères. Il convient à la compression de fichiers et à la compression de streaming à l'aide de l'algorithme LZ4. L'implémentation initiale du format LZ4 a été réalisée en langage [C](/fr/programming/c/) par Yann Collet en 2011 et est disponible pour référence développeur sur [Github](https://github.com/lz4/lz4) .

### Format de trame LZ4

La structure générale du format de fichier LZ4 est illustrée ci-dessous.

|NbMagique|F. Descripteur| Bloc|(...)|FinMarque |C. Somme de contrôle|
---|---|---|---|---|---|
|4 octets| 3-15 octets||| 4 octets | 0-4 octets |

#### Nombre magique

4 octets, format Little endian. Valeur : 0x184D2204

#### Descripteur de trame

Le descripteur de trame se compose de 3 à 15 octets et constitue la partie la plus importante des spécifications. Ensemble, les champs Magic_Number et Frame_Descriptor sont appelés en-tête de trame LZ4, et sa taille varie entre 7 et 19 octets. C'est comme indiqué ci-dessous.

|FLG| BD| (Taille du contenu) | (ID de dictionnaire)| SC|
---|---|---|---|---|
|1 octet| 1 octet | 0 - 8 octets | 0 - 4 octets | 1 octet |

#### Blocs de données

Chaque bloc de données suit l'ordre suivant.

|Taille de bloc| données| (Bloquer la somme de contrôle) |
---|---|---|
|4 octets| |0 - 4 octets|

#### Marque de fin

Le flux de blocs se termine lorsque le dernier bloc de données est suivi de la valeur 32 bits 0x00000000.

#### Somme de contrôle du contenu

Le Content_Checksum vérifie la validité du contenu décodé correctement et est effectué en utilisant le résultat de l'algorithme xxHash-32. Il valide les résultats de la transmission réussie de tous les blocs dans le bon ordre et sans aucune erreur.

## Références

* [Format de trame LZ4](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [Algorithme de compression LZ4 - Wikipédia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

