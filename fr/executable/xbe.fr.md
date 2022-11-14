{
  "date" : "2021-08-31",
  "keywords" :[ "fichier xbe", "format de fichier xbe", "qu'est-ce qu'un fichier xbe", "fichier", "exemple xbe", "extension de fichier xbe","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier XBE et les API qui peuvent créer et ouvrir des fichiers XBE.",
  "title" :"XBE - Fichier de package d'application iOS",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## Qu'est-ce qu'un fichier XBE ?
Un fichier ayant l'extension .xbe est une application exécutable à partir d'un disque de jeu vidéo Xbox. Les fichiers XBE sont les principaux fichiers exécutés dans le système Xbox et ne sont généralement pas censés être ouverts sur un ordinateur, mais ils peuvent être ouverts sur un PC à l'aide d'un programme d'émulation Xbox. Ces fichiers sont généralement créés par les développeurs de jeux, puis signés par Microsoft. La structure du fichier est similaire à celle des fichiers Windows PE, mais certaines modifications importantes en fonction des paramètres XBox sont appliquées pour le rendre exécutable sur XBox.

## Format de fichier XBE
Le fichier XBE est composé d'un en-tête d'image, d'une collection d'en-têtes de section, d'un certificat, de données de stockage local de thread, d'une collection de versions de bibliothèque, d'un bitmap Microsoft et des sections contenant le code et les ressources.

### En-tête de l'image
L'en-tête de l'image comprend les informations qui expliquent où se trouvent les autres composants de l'exécutable dans le fichier et comment l'exécutable doit être traité et chargé.

### Tableau TLS
La table TLS comprend toutes les informations nécessaires au XBE pour configurer correctement le stockage local des threads. Il est fondamentalement unique au répertoire TLS trouvé dans les fichiers PE32 et peut être directement copié à partir de là. Cette table peut être omise, si le fichier XBE n'utilise pas de stockage local de thread, et le champ respectif dans l'en-tête de l'image mis à zéro.

| Décalage | Taille | Nom | Descriptif |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Début des données brutes | Adresse absolue (c'est-à-dire pas une RVA) de début des données variables TLS dans l'image du programme. |
| 0x0004 | 0x0004 | Fin des données brutes | Adresse absolue (c'est-à-dire pas une RVA) de la fin des données variables TLS dans l'image du programme. |
| 0x0008 | 0x0004 | Adresse de l'index | Adresse absolue (c'est-à-dire pas une RVA) de la variable Index TLS. |
| 0x000C | 0x0004 | Adresse des rappels | Adresse absolue (c'est-à-dire pas une RVA) de la table des fonctions de rappel TLS à terminaison nulle. |
| 0x0010 | 0x0004 | Taille du remplissage zéro | Le nombre d'octets suivant les données brutes qui doivent être mis à zéro en mémoire. |
| 0x0014 | 0x0004 | Caractéristiques | Décrit l'alignement. |

### Certificat

Un certificat est obligatoire pour chaque exécutable Xbox contenant des informations sur les titres :
 


- Heure et date de création du certificat
- Identifiant du titre
- Nom du titre
- ID de titres alternatifs
- Types de supports autorisés à partir desquels l'exécutable peut être exécuté (HD, DVD, CD, etc.)
- Région de jeu
- Notes de jeu
- Numéro de disque
- Version
- Données brutes de clé LAN utilisées pour System Link
- Données brutes de la clé de signature (utilisées pour signer les sauvegardes)
- Clés de signature alternatives
- Taille originale du certificat
- Nom du service en ligne (non présent dans les premiers exécutables)
- Drapeaux de sécurité d'exécution (non présents dans les premiers exécutables)
 


### Types de médias autorisés
Types de média à partir desquels l'exécutable autorise l'exécution. Les valeurs suivantes sont connues :
| Type de média | Valeur |
---------------------|------------|
| DISQUE_DUR | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDIA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MASQUE_MEDIA | 0x00FFFFFF |

### Sections
Les sections sont exprimées par les en-têtes de section. Les en-têtes de section commencent juste après le certificat et contiennent des informations sur l'emplacement des sections réelles dans le fichier. Au moins deux sections sont toujours présentes dans un exécutable Xbox :


- .texte


- .rdata


## Références



* [Xbe - Exécutable XBox](https://xboxdevwiki.net/Xbe)


