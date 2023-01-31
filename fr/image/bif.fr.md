{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier BIF - Format d'image de diapositive entière Ventana",
  "description":"En savoir plus sur le format de fichier BIF et les API qui peuvent créer et ouvrir des fichiers BIF.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## Qu'est-ce qu'un fichier BIF ?

Un fichier BIF est un fichier d'image raster qui contient l'image de l'échantillon de diapositive. Il se compose de plusieurs images TIFF qui sont combinées par des applications de visualisation de diapositives en une seule image composite. Les fichiers BIF sont créés par le scanner de diapositives numérique Ventana Medical Systems et sont entièrement conformes à la variante BigTIFF de la définition [TIFF](/fr/image/tiff/) v 6.0.

## Format de fichier BIF

Un fichier BIF est enregistré en tant que fichier image binaire et comprend jusqu'à 200 000 x 200 000 pixels. Cela peut conduire à des fichiers de grande taille, dépassant la limite de taille de 4 Go imposée par les pointeurs de fichiers 32 bits définis par la norme TIF. Avec les pointeurs de fichiers 64 bits, cependant, cette barrière de taille de fichier est surmontée par la variante BigTIFF de la norme TIFF.

### Qui utilise le fichier BIF ?

Les fichiers BIF sont utilisés par les scanners de diapositives numériques pour numériser et créer des copies numériques de spécimens de diapositives. Si vous êtes un pathologiste, vous pouvez ouvrir ces fichiers BIF dans des applications de visualisation de diapositives. Avec un niveau élevé de détails et des données haute résolution, vous pouvez effectuer un zoom avant et arrière sur une image de diapositive pour afficher les sections d'échantillons avec plus ou moins de détails. Le fichier de métadonnées [XML](/fr/web/xml/) présent dans ces fichiers définit comment les images doivent être combinées et l'image qui doit être utilisée comme vignette du fichier.

## Comment ouvrir le fichier BIF ?

Vous pouvez ouvrir les fichiers BIF avec :

* OpenSlide (multiplateforme)
* ImageJ (multiplateforme)
* Visionneuse NetScope (Windows)

## Références ##

* [Livre blanc Roche Digital Pathology BIF](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

