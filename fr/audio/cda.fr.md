{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "fichier", "extension", "format", "qu'est-ce qu'un fichier cda", "musique", "format de fichier cda", "spécification du format de fichier cda"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier CDA et les API qui peuvent créer, convertir et ouvrir des fichiers CDA.",
  "title" :"CDA - Fichier de raccourci de piste audio CD",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Qu'est-ce qu'un fichier CDA ?

Un fichier avec l'extension .cda est un petit fichier stub généré par Microsoft Windows pour chaque piste audio d'un CD audio. Ces fichiers contiennent des informations typiques telles que les temps de piste et un raccourci Windows qui permet aux utilisateurs d'accéder aux pistes audio spécifiques. Les fichiers CDA ne sont pas de la musique, mais ils pointent vers un fichier musical existant quelque part sur le stockage. Nous pouvons le dire comme un raccourci d'un fichier audio qui se trouve sur un CD.

## Format de fichier CDA

Le format de fichier CDA est utilisé pour indiquer à un ordinateur quel fichier audio lire sur un CD. Ainsi, les fichiers CDA deviennent inutiles séparés d'un CD qu'ils représentent. Les fichiers CDA sont généralement considérés comme des ressources RIFF. Il n'y a qu'un seul bloc nommé "CDDA" et contenant un seul bloc de données appelé "FMT" dans la version actuelle du fichier .cda. Ce bloc a une longueur de 24 octets. L'identifiant créé par Windows est utilisé par le lecteur de CD associé à Windows 95 et Windows 98 et son lecteur ne peut pas se connecter à FreeDB ou CDDB. Pour qu'il puisse afficher le titre de la chanson et le nom de l'artiste, vous devez entrer manuellement ces informations dans le fichier cdplayer.ini.

### Organisation d'un fichier CDA

Le tableau suivant affiche les informations sur les décalages typiques :
| décalage | longueur | contenu |
---|---|---|
| 0x00 | 4 | les 4 caractères ASCII "RIFF" |
| 0x04 | 4 | la taille du chunk suivant : toujours 36 (44 - 8), sur 4 octets (ordre Intel) |
| 0x08 | 4 | identifiant du bloc : les 4 caractères ASCII "CDDA" |
| 0x0C | 4 | les 3 caractères ASCII "fmt" suivis d'un espace |
| 0x10 | 4 | longueur du chunk : toujours 24, sur 4 octets (ordre Intel) |
| 0x14 | 2 | version du format CD, sur 2 octets (commande Intel). En mai 2006, toujours égal à 1. |
| 0x016 | 2 | numéro de la gamme, sur 2 octets (commande Intel). La première piste porte le numéro 1. |
| 0x18 | 4 | identifiant calculé par Windows pour cdplayer.exe. |
| 0x1c | 4 | décalage de plage, en nombre d'images (ordre Intel) |
| 0x20 | 4 | durée de la piste, nombre total d'images (ordre Intel) |
| 0x24 | 1 | position de la plage : images |
| 0x25 | 1 | position de plage : secondes |
| 0x26 | 1 | position de la plage : minutes |
| 0x27 | 1 | un octet nul (valeur binaire 0) |
| 0x28 | 1 | durée de la piste : images |
| 0x29 | 1 | durée de la piste : secondes |
| 0x2a | 1 | durée du morceau : minutes |
| 0x2b | 1 | un octet nul (valeur binaire 0) |

## Références

* [Fichier .cda - Par Wikipédia](https://en.wikipedia.org/wiki/.cda_file)

