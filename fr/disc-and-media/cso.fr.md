{
  "date" : "2021-08-09",
  "keywords" :[ "fichier cso", "format de fichier cso", "qu'est-ce qu'un fichier cso", "fichier", "exemple cso", "extension de fichier cso","extension", "format", "iso", "compression DAX " ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"En savoir plus sur le format de fichier CSO et les API qui peuvent créer et ouvrir des fichiers CSO.",
  "title" :"CSO - Image disque ISO compressée",
  "linktitle" : "CSO",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-09"
}

## Qu'est-ce qu'un fichier CSO ?

Un fichier avec l'extension .cso est un fichier image ISO compressé. Le CSO est une alternative à la méthode de compression DAX ; également connu sous le nom de RSSI ; était la première méthode pour compresser les fichiers [ISO](/fr/compression/iso/) et est généralement la méthode préférée pour archiver les éléments PlayStation Portable. Ce format utilise la compression Deflate, qui peut inclure jusqu'à neuf couches de compression. Des logiciels tels que Prometheus et YACC sont utilisés pour créer les images.

## Format de fichier OSC

Le format de fichier CSO a été la première méthode de compression ISO pour économiser plus d'espace mémoire. Des améliorations ont été apportées de temps en temps pour une meilleure compression. Le CSO utilise la compression Deflate avec neuf niveaux de préréglages, généralement, chaque niveau peut gérer 2 blocs de KiB individuellement. Alors que les niveaux de compression les plus élevés peuvent ralentir et allonger les temps de chargement dans les logiciels qui dépendent fortement de la diffusion de disques, les niveaux inférieurs peuvent également effectuer une compression substantielle.

### Structure du fichier CSO

Le format de fichier CSO contient un en-tête de 24 octets, des blocs de données et une table d'index. Little-endian est supposé pour les champs supérieurs à un octet. L'architecture endianness de PlayStation Portable est donnée ci-dessous.

#### Entête

| Décalage (octets) | Nom | Taille (octets) | Objectif |
----------|----------|--------------|---------|
| 0x0 | Magie | 4 | Toujours CISO, ou 0x4F534943 lorsqu'il est lu comme un entier 32 bits. Ce champ est utilisé pour identifier un fichier CSO. Notez que ce champ peut être différent pour les autres dérivés de CSO, par exemple, ZSO a utilisé le code magique ZISO. |
| 0x4 | Taille de l'en-tête | 4 | Pour le format de fichier CSO "v1" d'origine, ce champ est ignoré et n'a donc pas besoin d'être précis. Cependant, le format "v2" et ZSO exigent que ce champ soit toujours 0x18 (24 octets). |
| 0x8 | Taille non compressée | 8 | La taille de l'image ISO originale non compressée en octets. |
| 0x10 | Taille du bloc | 4 | Taille de chaque bloc de données en octets avant compression. Généralement 2048 octets, identique à la taille de chaque secteur ISO 9660. |
| 0x14 | Version | 1 | La version du format de fichier en cours d'utilisation. Pour le format "v1", la valeur peut être 0 ou 1. Pour le format "v2", cela doit être 2. De plus, le format ZSO exige que ce soit 1. |
| 0x15 | Alignement d'index | 1 | L'alignement de chaque entrée d'index, spécifié en bits. |
| 0x16 | Réservé | 2 | Ce champ est inutilisé. Dans le format "v1", ce champ est ignoré et peut contenir des valeurs arbitraires. Dans le format "v2", ce champ doit être nul. |

#### Table d'index

La table d'index contient plusieurs entrées de 4 octets, qui indiquent la position de chaque bloc de données, et une dernière entrée supplémentaire qui pointe vers la fin du fichier.
Le contenu de chaque entrée est le suivant :
| peu | Longueur | Masque | Nom | Objectif |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFF | Poste | Ce champ, lorsqu'il est décalé vers la gauche par l'alignement d'index donné dans l'en-tête, donne la position où commence le bloc de données. |
| 31 | 1 | 0x80000000 | Type de compression | Le format ZSO a une sémantique similaire, sauf que 0 représente LZ4 au lieu de Deflate. Au format "v2". Le bloc est implicitement considéré comme non compressé si la taille du bloc est égale ou supérieure à la taille de bloc spécifiée dans l'en-tête du fichier. |

#### Blocs de données

Les blocs de données comprennent les données non compressées ou compressées. La taille d'un bloc est calculée en obtenant sa position, puis en la soustrayant de la position du bloc suivant. Si l'alignement d'index est supérieur à zéro, il est probable que la taille du bloc soit supérieure aux données qu'il contient.


## Références

* N/A

