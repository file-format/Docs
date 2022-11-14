{
  "date" : "2021-06-29",
  "keywords" :[ "ICNS", "extension", "fichier", "format", "image", "Image d'icône Apple", "macOS", "Apple", "Icône" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICNS - Image d'icône Apple",
  "description":"En savoir plus sur le format de fichier ICNS et les API qui peuvent créer et ouvrir des fichiers ICNS.",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Qu'est-ce qu'un fichier ICNS ? ##

Un format d'icône utilisé par les programmes macOS est appelé fichier ICNS. Il autorise les bandes alpha 1 bit et 8 bits et enregistre une ou plusieurs images, généralement réalisées à partir de documents [PNG](/fr/image/png). L'icône du programme dans le navigateur et l'interface macOS s'affiche à l'aide de fichiers ICNS.

En fonction de l'emplacement, la même icône de style peut avoir plusieurs paramètres. Le format ICNS a subi de nombreuses modifications et a évolué au point où il peut maintenant être utilisé comme base pour divers formats compatibles. Voici quelques autres points importants que vous devez savoir :

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource et Mac OS Icons Resource sont quelques-uns des autres noms.
* Pour les informations sur les icônes, une source dans la branche des ressources est utilisée.
* Dans la plupart des cas, un fichier contient de nombreuses images. 1612 pixels carrés et 1024, 512, 256, 128, 48, 32 et 16 pixels carrés sont des tailles d'image prises en charge.


## Format de fichier ICNS ##

Le format de données ICNS est une capsule pour une ou plusieurs images, prenant en charge des bandes de 1 bit et de nombreux états d'image.
Le système d'exploitation peut redimensionner les images d'icônes pour s'adapter à la taille d'affichage requise. Les images d'icônes plus grandes sont généralement enregistrées en tant que fichiers [JPEG](/fr/image/jpeg/) 2000 ou [PNG](/fr/image/png). Un type de fichiers ICNS compressés et non compressés est possible.

Un en-tête et des données d'icône binaires constituent la structure d'un fichier ICNS. L'en-tête contient 8 octets de données, dont quatre sont le littéral magique et quatre sont la longueur du fichier. Le type et la taille de chaque image d'icône sont stockés dans la section de données d'icône, qui est suivie par les données d'image binaires. La taille de l'image détermine la taille de la section binaire.

## Spécification technique ##

### Entête ###

|Décalage|Taille|Objectif
---|---|---|
|0|4|Litéral magique, doit être "icns" (0x69, 0x63, 0x6e, 0x73)
|4|4|Longueur du fichier, en octets, msb en premier


### Données d'icône ###

|Décalage|Taille|Objectif
---|---|---|
|0|4|Type d'icône
|4|4|Longueur des données, en octets (y compris le type et la longueur), msb en premier
|8|Variable|Données d'icône

### Compression ###

Les données de pixel sont compressées dans une certaine mesure. Les pixels 32 bits ("is32", "il32", "ih32", "it32") et ARGB ("ic04", "ic05") sont souvent compressés (par canal) de la même manière que PackBits.

|Valeur principale|Octets de queue|Résultat (non compressé)
---|---|---|
|0 - 127|1 - 128|1 - 128 octets
|128 - 255|1 octet|3 - 130 copies

## Référence ##

* [ICNS - Wikipédia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)

