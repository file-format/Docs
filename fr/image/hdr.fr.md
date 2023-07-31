{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier HDR - Qu'est-ce qu'un fichier image HDR ?",
  "description":"En savoir plus sur le format de fichier HDR et les API qui peuvent créer et ouvrir des fichiers HDR.",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## Qu'est-ce qu'un fichier HDR ?

Un fichier HDR est un format de fichier d'image raster à plage dynamique élevée (HDR) pour stocker des photos d'appareils photo numériques. Il permet aux éditeurs de photos d'améliorer la couleur et la luminosité des images numériques qui ont une plage dynamique limitée. Cette modification peut améliorer la luminosité dans les coins, ce qui donne une image proche du naturel. Les fichiers HDR sont généralement enregistrés sous forme d'images raster 32 bits. Adobe Photoshop peut créer et ouvrir des fichiers HDR.

Les fichiers HDR sont également appelés HDRI.

## Format de fichier HDR - Plus d'informations

Le format de fichier HDR est basé sur le format de fichier original Radiance Picture (.pic). Les données de pixels d'un fichier HDR sont généralement stockées non compressées, mais dans certains cas, elles sont compressées à l'aide d'un système d'encodage simple.

### Structure des fichiers HDR

Un fichier image HDR se compose des trois sections suivantes :

* **En-tête :** Un fichier HDR est identifié par les premiers octets du fichier image, c'est-à-dire "#?RADIANCE".
* **Chaîne de résolution :** L'en-tête est suivi d'une seule ligne de résolution composée de 4 valeurs ; une étiquette X et Y suivie chacune d'une valeur numérique entière. L'ordre des X et Y indique une rotation. La combinaison de X et Y avec des valeurs positives et négatives couvre toutes les orientations et rotations d'image possibles.
* **Données de pixels :** Les données de pixels d'un fichier HDR sont soit non compressées, soit compressées à l'aide d'un encodage standard.

## API HDR/HDRI open source

* **[imageinfo](https://github.com/xiaozhuai/imageinfo )** - Bibliothèque d'en-tête unique super rapide multiplateforme [C++](/fr/programming/cpp/) pour obtenir la taille et le format de l'image sans chargement/décodage.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - Bibliothèque Rust pour obtenir la taille et le format de l'image sans chargement/décodage. Prend en charge [.avif](/fr/image/avif/), [.bmp](/fr/image/bmp/), [.cur](/fr/image/cur/), [.dds](/fr/image/dds/), [. gif](/fr/image/gif/), hdr (pic), [heic (heif)](/fr/image/heic/), [.icns](/fr/image/icns/), [.ico](/fr/image/ico /), [.jp2](/fr/image/jp2/), [jpeg (jpg)](/fr/image/jpeg/), [jpx](/fr/image/jpx/), ktx, [png](/fr/image/png /), [psd](/fr/image/psd/), qoi, tga, tiff (tif) et webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - Implémentation Java de HdrHistogram.

## Références

* [Éclat HDR](http://paulbourke.net/dataformats/pic/)
* [imageinfo](https://github.com/xiaozhuai/imageinfo)

