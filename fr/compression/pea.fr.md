{
  "date" : "2021-04-21",
  "keywords" :[ "fichier pea", "format de fichier pea", "qu'est-ce qu'un fichier pea", "fichier", "exemple pea", "extension de fichier pea","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - Format de fichier d'archive PeaZip",
  "description":"En savoir plus sur le format de fichier PEA et les API qui peuvent créer et ouvrir des fichiers PEA.",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## Qu'est-ce qu'un fichier PEA ?

Un fichier avec l'extension .pea, acronyme de Pack, Encrypt, and Authenticate, est une archive [zip](/fr/compression/zip/) créée avec l'application logicielle d'archivage [PeaZip](https://peazip.github.io/). Il offre une compression et une sortie de volumes multiples, et offre un modèle de sécurité flexible grâce au cryptage authentifié et à la cryptographie. Cela assure à la fois la confidentialité et l'authentification des données. L'utilitaire PeaZip est disponible en tant que moteur open source qui peut être compilé pour différents systèmes d'exploitation selon les besoins.

## Format de fichier PEA

Les [spécifications du format de fichier PEA](https://peazip.github.io/pea_help.pdf) sont accessibles au public pour référence par les développeurs. Les archives PEA sont des fichiers binaires avec un modèle de sécurité flexible et des contrôles d'intégrité redondants allant des sommes de contrôle aux hachages cryptographiquement forts. Cela définit trois niveaux de communication différents à contrôler :

* Flux - le flux de données de sortie réel qui est formé par plusieurs fichiers d'entrée et peut être écrit sur plusieurs volumes de sortie
* Objets - fichiers d'entrée et dossiers envoyés à l'archive .pea
* Volumes - fichier d'archive de sortie pouvant être étendu à une taille définie par l'utilisateur

Chacun d'entre eux est facultatif et peut être intégré selon les besoins de l'utilisateur. Le format de fichier PEA peut stocker un seul flux contenant un nombre illimité d'objets. Chaque flux a une taille maximale de 2^64 octets.

Les fichiers PEA offrent une vérification d'intégrité facultative et un cryptage authentifié à l'aide d'AES en mode EAX ou HMAC, alternativement Twofish et Serpent en mode EAX.

### En-tête d'archive PEA

L'en-tête de l'archive est de 10 octets et est structuré comme suit.

|Octets|Description|
---|---|
|1 | Champ d'octet magique pour la désambiguïsation du format de fichier : $EA|
|1 | Numéro de version |
|1 | Numéro de révision|
|1 | Schéma de contrôle du volume |
|1 | Déclarer le système d'exploitation où le flux a été construit|
|1 | Déclaration de l'encodage de la date et de l'heure du système d'exploitation |
|1 | Déclaration de l'encodage des caractères du nom des objets |
|1 | Déclarer le type de CPU (encodé en 7 bits) et le endianness (en msb) |
|1 | Réservé pour une utilisation future |

## Références

* [Spécifications du format de fichier PEA](https://peazip.github.io/pea_help.pdf)
* [Format de fichier PEA](https://peazip.github.io/pea-file-format.html#.pea_specifications)

