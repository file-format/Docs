{
  "date" : "2021-26-08",
  "keywords" :[ "fichier dcr", "format de fichier dcr", "qu'est-ce qu'un fichier dcr", "fichier", "exemple dcr", "extension de fichier dcr","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCR - Fichier d'image RAW d'appareil photo numérique",
  "description":"En savoir plus sur le format de fichier DCR et les API qui peuvent créer et ouvrir des fichiers DCR.",
  "linktitle" : "DCR",
  "menu" : {
    "docs" : {
      "identifier":"image-dcr",
      "parent" : "image"
}
},
  "lastmod" : "2021-26-08"
}

## Qu'est-ce qu'un fichier DCR ? ##
Un fichier avec l'extension dcr contient le contenu d'une photographie numérique enregistrée au format Kodak Digital Camera RAW (DCR). Le DCR est l'abréviation de **Digital Camera Raw** ; contient la version non compressée et sans perte des données d'images capturées par un appareil photo numérique Kodak. Les photographes professionnels aiment utiliser ces fichiers, car ils stockent des images de meilleure qualité que les formats d'image compressés de faible qualité.

## Format de fichier DCR
Le DCR est un format propriétaire développé par Eastman Kodak Company ; appelé simplement Kodak. Un fichier image Digital Camera Raw (DCR) contient des données minimalement traitées provenant du capteur d'image d'un appareil photo numérique. Ces fichiers ne sont pas encore traités et ne sont donc pas prêts à être imprimés ou édités avec un éditeur graphique bitmap.
Habituellement, un convertisseur brut traite l'image dans un espace colorimétrique interne à large gamme où la précision et le raffinement peuvent être apportés avant la conversion en un format de fichier raster tel que TIFF ou JPEG pour le stockage, l'impression ou une manipulation ultérieure.
### Contenu du fichier
La structure des fichiers bruts suit souvent un modèle générique :
- Un en-tête de fichier court qui contient un indicateur de l'ordre des octets du fichier.
- Les métadonnées du capteur de la caméra qui sont nécessaires pour interpréter les données d'image du capteur, y compris les attributs du CFA, la taille du capteur et son profil de couleur.
- Métadonnées d'image qui peuvent être utiles pour l'inclusion dans n'importe quel environnement ou base de données CMS. Certains fichiers bruts contiennent une section de métadonnées standardisée avec des données au format Exif.
- Une vignette d'image.
- Une conversion JPEG pleine taille de l'image, qui est utilisée pour prévisualiser le fichier sur le panneau LCD de l'appareil photo.
- Dans le cas de numérisations de films cinématographiques, soit le code temporel, le code clé ou le numéro d'image dans la séquence de fichiers qui représente la séquence d'images dans une bobine numérisée.
- Les données d'image du capteur
### Données d'image du capteur
Le fichier brut joue le même rôle dans la photographie numérique que le film photographique joue dans la photographie argentique. Les fichiers bruts contiennent donc les données en pleine résolution telles que lues à partir de chacun des pixels du capteur d'image de l'appareil photo. Le capteur de la caméra est presque constamment recouvert d'un CFA (Color Filter Array). Il peut être utilisé dans la conversion d'images à plage dynamique élevée lorsque des données au format brut sont disponibles ; comme alternative plus simple à l'approche HDI multi-exposition consistant à capturer trois images distinctes.


## Références ##

* [Format d'image brute - Par Wikipedia](https://en.wikipedia.org/wiki/Raw_image_format)
* [Qu'est-ce qu'un fichier DCR](https://expertphotography.com/dcr-file/)

