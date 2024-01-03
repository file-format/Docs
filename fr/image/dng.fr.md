{
  "date" : "2019-10-11",
  "keywords" :[ "fichier dng", "format de fichier dng", "qu'est-ce qu'un fichier dng", "fichier", "exemple dng", "extension de fichier dng","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DNG - Format de fichier d'image d'appareil photo numérique",
  "description":"En savoir plus sur le format de fichier DNG et les API qui peuvent créer et ouvrir des fichiers DNG.",
  "linktitle" : "DNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier DNG ?

DNG est un format d'image d'appareil photo numérique utilisé pour le stockage de fichiers bruts. Il a été développé par Adobe en septembre 2004. Il a été essentiellement développé pour la photographie numérique. DNG est une extension du format standard [TIFF](/fr/image/tiff/)/EP et utilise les métadonnées de manière significative. Afin de manipuler les données brutes des appareils photo numériques avec la facilité de la flexibilité et du contrôle artistique, les photographes optent pour les fichiers bruts de l'appareil photo. Les formats JPEG et TIFF stockent des images qui sont traitées par l'appareil photo, par conséquent, il n'y a pas beaucoup de place pour la modification dans ces formats.

## Historique et versions du format de fichier DNG

Jusqu'à présent, il y a eu jusqu'à présent 5 versions de la spécification DNG. La version 1.0.0.0 a été lancée en septembre 2004 avec la sortie de "2.3" (ACR et DNG Converter). En février 2005, la version 1.1.0.0 a été publiée. En mai 2008, la version 1.2.0.0 a été publiée et a été utilisée dans "4.4". La version 1.3.0.0 a été publiée en juin 2009. La version 1.4.0.0 est apparue en 2012.

## Format de fichier DNG

Alors que les fichiers Camera Raw capturent des données non traitées ou peu traitées directement à partir du capteur. Comme ils sont similaires aux négatifs sur film, les formats Camera Raw sont également appelés «négatifs numériques». L'avantage des formats bruts est le contrôle artistique accru pour l'utilisateur final. L'utilisateur peut ajuster diverses plages de paramètres en fonction des exigences telles que la balance des blancs, la cartographie des tons, la réduction du bruit, la netteté, etc. D'autre part, le fichier Camera Raw doit être traité pour toute utilisation via n'importe quel logiciel ou via un convertisseur.

Comme il n'y avait pas de format standard disponible pour les fichiers Camera Raw, cela créait de multiples problèmes pour l'utilisateur final. Ces problèmes ont été résolus par Adobe et ont défini un format non propriétaire pour les fichiers Camera Raw. Le format est connu sous le nom de Digital Negative ou DNG. DNG peut être utilisé par une large gamme de matériels et de logiciels pour le traitement de fichiers bruts. De plus, DNG peut également être utilisé comme format intermédiaire pour stocker des images qui ont été capturées à l'origine par des appareils photo ayant leurs propres formats bruts propriétaires.

### Spécifications du format de fichier DNG

Dans cette section, nous décrirons le format DNG comme une extension du TIFF 6.0.

* **Extensions de fichier** : DNG utilise les extensions ".DNG" ou ".TIF".
* **Arbres SubIFD** : DNG ne prend pas en charge les chaînes SubIFD, mais DNG recommande l'utilisation d'arbres SubIFD comme indiqué dans les spécifications TIFF-EP. La qualité et la résolution les plus élevées peuvent utiliser NewSubFileType de 0, tandis que les vignettes de qualité réduite doivent utiliser NewSubFileType égal à 1. Il est également recommandé, mais pas obligatoire, que le premier IFD ait une vignette de faible qualité ou résolution.
* **Ordre des octets** : l'ordre des octets doit être pris en charge par les lecteurs DNG, également pour les fichiers d'un modèle d'appareil photo particulier.
* ** Pixels masqués ** : la plupart des capteurs de caméra calculent les pixels entièrement masqués au bord du capteur via un codage noir. Ces pixels peuvent être inclus ou coupés avant que l'image ne soit stockée au format DNG. Si les pixels masqués ne sont pas coupés, la zone de ces pixels doit être mentionnée dans la balise ActiveArea. Les informations recueillies à partir de ces pixels sur le niveau d'encodage du noir doivent être utilisées avant le stockage des données brutes ou peuvent être incluses dans le fichier DNG spécifiant le niveau de noir.
* **Pixels défectueux** : avant de stocker des données brutes au format DNG, les pixels défectueux doivent être exclus.
* **Métadonnées** : les métadonnées peuvent être incluses dans DNG de l'une des manières suivantes :
** En utilisant des balises de métadonnées TIFF-EP ou EXIF
** Via la balise de métadonnées IPTC (33723)
** Utilisation de la balise de métadonnées XMP (700)
* **Données exclusives** : normalement, les fournisseurs incluent des données exclusives dans un fichier brut destiné à être utilisé par leurs propres convertisseurs. DNG stocke ses données propriétaires dans des balises privées, des IFD privés et dans une MakerNote privée. Les fournisseurs doivent utiliser les balises DNGPrivateData et MakerNoteSafety pour s'assurer que les applications qui modifient les fichiers DNG conservent ces données propriétaires.

Voici quelques restrictions et extensions importantes des balises TIFF.

**Bits par échantillon**

8 à 32 bits/échantillon sont pris en charge. Il doit y avoir la même profondeur pour chaque échantillon lorsque SamplesPerPixel n'est pas égal à 1.Mais si BitsPerSample n'est pas égal à 8 ou 16 ou 32, alors les bits doivent être compressés en octets en utilisant le FillOrder par défaut TIFF de 1 (big-endian).

**Compression**

Deux valeurs de balise de compression sont acceptées :

* Valeur # 1 : Données non compressées.
* Valeur # 7 : données compressées JPEG, soit DCT JPEG de base, soit compression JPEG sans perte.

**Interprétation photométrique**

Les valeurs suivantes sont prises en charge uniquement pour les miniatures et les aperçus IFD :

* 1 = NoirEstZéro. Supposé être dans un espace colorimétrique gamma 2.2.
* 2 = RVB. Supposé être dans l'espace colorimétrique sRGB.
* 6 = YCbCr. Utilisé pour les images d'aperçu encodées en JPEG.

Les valeurs suivantes sont prises en charge pour l'IFD brut et sont supposées être l'espace colorimétrique natif de la caméra :

* 32803 # CFA (réseau de filtres de couleur).
* 34892 # Linéaire Brut.

**Orientation**

La balise d'orientation est utilisée pour les navigateurs de fichiers afin qu'ils puissent effectuer une rotation sans perte des fichiers DNG. Les lecteurs DNG doivent prendre en charge toutes les orientations possibles, y compris les orientations en miroir.

## Fonctionnalités de la dernière version de DNG

DNG Version 1.4 Octobre 2012 a les fonctionnalités avancées suivantes.

* Recadrage utilisateur par défaut
* Transparence
* Virgule flottante (HDR)
* La compression avec perte
* Procurations

## Références ##

* [Spécifications DNG - Par Adobe](https://web.archive.org/web/20170829200857/http://wwwimages.adobe.com/content/dam/Adobe/en/products/photoshop/pdfs/dng_spec_1.4.0.0.pdf)
* [Négatif numérique - Wikipédia](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG - Le format d'archivage public pour les données brutes des appareils photo numériques](https://helpx.adobe.com/photoshop/digital-negative.html)

