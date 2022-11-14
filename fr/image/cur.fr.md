{
  "date" : "2021-06-29",
  "keywords" :[ "CUR", "extension", "fichier", "format", "image", "Bitmap indépendant du périphérique", "Format de fichier du curseur", "Curseur", "Windows", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CUR - Format de fichier de curseur",
  "description":"En savoir plus sur le format de fichier CUR et les API qui peuvent créer et ouvrir des fichiers CUR.",
  "linktitle" : "CUR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Qu'est-ce qu'un fichier CUR ? ##

Un fichier CUR est un format de fichier de curseur Microsoft Windows statique. Fondamentalement, ce sont des images fixes identiques aux fichiers ICO (icônes) à tous points de vue, à l'exception de l'extension. CUR et [ICO](/fr/image/ico/) sont établis sur la base de la spécification Device-Independent Bitmap [DIB](/fr/image/dib/) (Device-Independent Bitmap). Le curseur par défaut, ainsi que le curseur personnalisé tel que le pointeur de la souris Windows pour le système d'exploitation Windows, sont stockés dans des fichiers CUR. Il peut s'agir d'une flèche pour une utilisation normale, d'un sablier tournant pour illustrer les périodes d'attente ou d'une barre en I pour l'édition de texte. Les fichiers CUR sont fournis avec le pack d'installation des thèmes de bureau personnalisés pour garantir que le curseur Windows correspond au thème de bureau personnalisé.

## Spécifications techniques ##

Les fichiers CUR sont des fichiers système binaires qui peuvent être trouvés sur les appareils fonctionnant sur le système d'exploitation Microsoft Windows. Les images de pointeur CUR sont disponibles dans différentes tailles standard telles que 16 × 16, 32 × 32, etc. Les fichiers CUR sont très similaires aux fichiers ICO. les deux consistent en de petites images fixes. Seule l'extension des fichiers CUR et ICO est différente. De plus, l'explication d'un hotspot dans l'en-tête du fichier CUR est distincte du fichier ICO. Le hotspot interprète le décalage de pixel du coin supérieur gauche à l'endroit où vous pointez la souris. Les systèmes Windows utilisent toujours les fichiers CUR, mais maintenant les curseurs animés ont généralement l'extension de fichier ANI au lieu de CUR.

## Bref historique ##

Le fichier CUR est créé à partir du fichier ICO. Le premier format de fichier CUR a été intégré au système d'exploitation Windows 1.0 de Microsoft en 1981 pour faciliter l'utilisation commerciale. Bientôt, des curseurs plus interactifs ont été introduits permettant aux utilisateurs de modifier leurs préférences de curseur à partir des options préinstallées disponibles. Cependant, il est facile d'éditer un fichier CUR par vous-même même si vous avez des connaissances techniques insuffisantes.


## Exemple CUR ##

Les fichiers CUR peuvent être trouvés à *C:\Windows\Cursors* :

{{< figure src="../cur.png" alt="Format de fichier CUR" >}}

