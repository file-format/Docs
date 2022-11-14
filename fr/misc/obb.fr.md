{
  "date" : "2022-02-16",
  "keywords" :[ "fichier obb", "format de fichier obb", "qu'est-ce qu'un fichier obb", "fichier", "exemple obb", "extension de fichier obb","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier OBB - Fichier Blob binaire opaque Android",
  "description":"En savoir plus sur le format de fichier OBB et les API qui peuvent créer et ouvrir des fichiers OBB.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## Qu'est-ce qu'un fichier OBB ?

Un fichier OBB est un fichier d'extension qui contient des données supplémentaires en plus du fichier Android [APK](/fr/compression/apk/). Google Play Store ne permet pas d'avoir un fichier APK Android d'une taille supérieure à 100 Mo. Mais certaines applications peuvent nécessiter l'hébergement de graphiques haute définition, de fichiers multimédias ou d'autres actifs volumineux en plus des fichiers APK. C'est là qu'interviennent les types de fichiers OBB. Google Play permet de joindre ces fichiers d'extension en complément du fichier APK.

## Format de fichier OBB

Les fichiers OBB sont enregistrés en tant que fichiers binaires avec les fichiers APK. Lorsqu'un APK accompagne les fichiers OBB, Google Play héberge les fichiers d'extension sur son serveur et aucun coût supplémentaire n'est facturé au développeur. Ces fichiers supplémentaires sont stockés dans le stockage partagé de l'appareil sur une carte SD ou une partition pouvant être montée sur USB lorsque l'application est téléchargée pour l'installation.

Les fichiers OBB sont téléchargés et installés lors du téléchargement. Mais dans certains cas, ceux-ci sont téléchargés pour être installés lors de la première exécution de l'application.

### Taille de fichier maximale OBB

Google Play Store vous permet de télécharger des fichiers d'extension OBB d'une taille allant jusqu'à 2 Go. Il est recommandé de télécharger les fils de grande taille sous forme de fichiers compressés [ZIP](/fr/compression/zip/) pour un téléchargement efficace via Internet.

Ces fichiers d'extension peuvent être hébergés soit en tant que fichier d'extension principal ** principal ** pour les ressources supplémentaires requises par l'application, soit en tant que fichier d'extension de correctif facultatif destiné à de petites mises à jour du fichier d'extension principal.

## Références

* [Développeurs Android - Fichiers d'extension](https://developer.android.com/google/play/expansion-files)

