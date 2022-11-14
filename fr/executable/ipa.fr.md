{
  "date" : "2021-08-30",
  "keywords" :[ "fichier ipa", "format de fichier ipa", "qu'est-ce qu'un fichier ipa", "fichier", "exemple ipa", "extension de fichier ipa","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier IPA et les API qui peuvent créer et ouvrir des fichiers IPA.",
  "title" :"IPA - Fichier de package d'application iOS",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## Qu'est-ce qu'un fichier IPA ?
Un fichier avec l'extension .ipa appartient à iOS et est appelé fichier de package d'application. Il s'agit d'un fichier d'archive (compressé à l'aide de la compression [ZIP](/fr/compression/zip/) qui stocke une application iOS, mais cette application ne peut être installée que sur un appareil iOS ou MacOS basé sur ARM, tel qu'un iPad, iPhone ou Ipod touch. Principalement, iTunes, Apple Configurator 2 ou tout autre logiciel tiers peuvent être utilisés pour installer les fichiers IPA.

## Format de fichier IPA
Les développeurs IOS qui développent les applications à l'aide d'Apple Xcode connaissent bien les fichiers IPA, car ils doivent empaqueter leurs applications développées sous forme de fichiers IPA, soit à des fins de test de déploiement de l'App Store. Bien que les fichiers IPA soient connus pour être installés en tant qu'applications iOS, vous pouvez également les décompresser pour afficher les données d'application contenues. Étant donné qu'un fichier IPA ne contient qu'un seul binaire pour l'architecture ARM des téléphones mobiles et qu'il ne contient pas de binaire pour l'architecture x86, de nombreux fichiers .ipa ne peuvent pas être installés sur le simulateur iPhone.
### Structure d'un fichier .ipa
L'exemple suivant montre la structure d'une IPA :

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Ce qui précède est une structure intégrée que iTunes et App Store doivent reconnaître. Selon cette structure :
- Le répertoire Payload contient toutes les données de l'application.
- Le fichier iTunes Artwork est une image PNG de 512 × 512 pixels, contenant l'icône de l'application à afficher dans iTunes et l'application App Store sur l'iPad.
- L'iTunesMetadata.plist contient diverses informations, allant du nom et de l'ID du développeur, aux informations de copyright, à l'identifiant du bundle, au nom de l'application, au genre, à la date de sortie, à la date d'achat, etc.
- Le dossier META-INF ne contient que des métadonnées sur le programme utilisé pour créer l'IPA.


## Références

* [.ipa - par Wikipédia](https://en.wikipedia.org/wiki/.ipa)


