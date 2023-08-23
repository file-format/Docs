{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier MPG",
  "keywords" :["MPG", "fichier", "extension", "format", "format vidéo","qu'est-ce qu'un format de fichier mpg", "format de fichier mpg", "lecteur de fichier mpg","compression mpeg", "vidéo ", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"En savoir plus sur le format de fichier MPG et les API qui peuvent créer et montrer comment ouvrir les fichiers MPG.",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-26"
}

## Qu'est-ce qu'un format de fichier MPG ? ##

Le fichier avec une extension .mpg appartient au groupe d'extensions de fichiers pour la compression audio et vidéo MPEG-1 ou MPEG-2. La vidéo MPEG-1 Partie 2 n'est pas facilement disponible, et cette extension (format de fichier MPG) pointe généralement vers un flux de programme MPEG défini dans MPEG-1 et MPEG-2, ou un flux de transport MPEG défini dans MPEG-2 . D'autres extensions telles que .m2ts existent également en spécifiant le conteneur précis, dans ce cas, MPEG-2 TS, mais cela a peu de pertinence pour les médias MPEG-1. Le [.mp3](/audio/mp3/) est l'extension la plus courante pour les fichiers contenant de l'audio MP3. Un fichier MP3 est un flux typique d'audio brut ; la manière traditionnelle de baliser les fichiers MP3 consiste à écrire des données de flux dans des segments "garbage" de chaque image, qui enregistrent les informations multimédias mais sont ignorées par le **lecteur de fichiers mpg**. Il s'agit d'une technique similaire utilisée pour baliser les fichiers AAC, mais moins prise en charge de nos jours.

## Compression MPEG ##

Le nom MPEG signifie Moving Pictures Experts Group. MPEG est un outil de compression vidéo, qui implique la compression d'images et de sons, ainsi que la synchronisation des deux.
Il existe actuellement plusieurs normes MPEG.

- MPEG-1 est proposé pour des débits intermédiaires, de l'ordre de 1,5 Mbit/sec.
- MPEG-2 est proposé pour des débits élevés d'au moins 10 Mbit/sec.
- MPEG-3 a été proposé pour la compression HDTV mais s'est avéré redondant et a été fusionné avec MPEG-2.
- MPEG-4 est proposé pour les très faibles débits inférieurs à 64 Kbit/sec.


## Flux de programme au format de fichier MPG ##

Le flux de programme est un conteneur pour multiplexer l'audio numérique, la vidéo, etc. Le format de flux de programme est spécifié dans la 1ère partie de MPEG-1 (ISO/IEC 11172-1) et la 1ère partie de MPEG-2, Systems (norme ISO/IEC 13818-1/ITU-T H.222.0). Le flux de programme MPEG-2 est basé sur l'analogique et similaire à la couche des systèmes ISO/IEC 11172 et compatible avec l'aval.

### Détails de codage ###

Voici les détails de codage du format d'en-tête de pack de flux de programme MPEG-2 partiel :

| Nom | Nombre de bits | Descriptif |
---|---|---|
| octets de synchronisation | 32 | 0x000001BA |
| marqueurs | 2 | 01b pour la version MPEG-2. Les bits de marqueur pour la version MPEG-1 sont 4 bits avec la valeur 0010b. |
| Horloge système [32..30] | 3 | Référence d'horloge système (SCR) bits 32 à 30 |
| marqueur | 1 | 1 bit toujours défini. |
| Horloge système [29..15] | 15 | Bits d'horloge système 29 à 15 |
| marqueur | 1 | 1 bit toujours défini. |
| Horloge système [14..0] | 15 | Bits d'horloge système 14 à 0 |
| marqueur | 1 | 1 bit toujours défini. |
| Extension SCR | 9 | |
| marqueur | 1 | 1 bit toujours défini. |
| débit binaire | 22 | En unités de 50 octets par seconde. |
| marqueurs | 2 | 11 Bits toujours activés. |
| réservé | 5 | réservé pour une utilisation future |
| longueur de farce | 3 | |
| octets de bourrage | 8 * longueur de farce | |
| en-tête système (optionnel) | 0 ou plus | si le code de démarrage de l'en-tête système suit : 0x000001BB |

Le tableau suivant montre le format d'en-tête système partiel :

| Nom | Nombre d'octets | Descriptif |
---|---|---|
| octets de synchronisation | 4 | 0x000001BB |
| longueur de l'en-tête | 2 | |
| taux liés et bits de marqueur | 3 | |
| audio lié et drapeaux | 1 | |
| drapeaux, marqueur et vidéo liés | 1 | |
| Restriction de débit de paquets et octet réservé | 1 | |


## Références ##

- [MPEG-1 - Wikipédia](https://en.wikipedia.org/wiki/MPEG-1)



