{
  "date" : "2021-02-15",
  "keywords" :[ "fichier asf", "format de fichier asf", "qu'est-ce qu'un fichier asf", "fichier", "exemple asf", "extension de fichier asf","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - Format de fichier des systèmes avancés",
  "description":"En savoir plus sur le format de fichier ASF et les API qui peuvent créer et ouvrir des fichiers ASF.",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Qu'est-ce qu'un fichier ASF ?

Un fichier avec l'extension .asf est un format de fichier multimédia pour stocker et lire des flux multimédias numériques sur le réseau. Il s'agit d'un format de fichier conteneur qui peut contenir à la fois du contenu vidéo et audio pour le streaming en ligne. Vous trouverez rarement des fichiers ASF, et plus probablement les fichiers Windows Media Audio ([WMA](/fr/audio/wma/)) et Windows Media Video ([WMV](/fr/video/wmv/)) qui spécifient tous deux des fichiers ASF ayant un contenu encodé avec les codecs respectifs. Les fichiers multimédias Windows peuvent être créés et lus à l'aide du SDK du format Windows Media.

## Format de fichier ASF

Un fichier ASF peut comprendre plusieurs flux indépendants ou dépendants. Cela peut inclure plusieurs flux audio pour l'audio multicanal ou plusieurs flux vidéo à débit binaire. Les multiples débits binaires rendent les flux adaptés à la transmission sur différentes largeurs de bande. De plus, les flux d'un fichier ASF peuvent être au format compressé ou non compressé. La meilleure compression est obtenue avec les codecs Microsoft Windows Media Audio et Video 9 Series. Les spécifications complètes du format de fichier ASF sont disponibles sur [site Web de Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### Structure de fichier de niveau supérieur ASF

Les fichiers ASF contiennent logiquement trois types d'objets de niveau supérieur :

* `Header Object` - obligatoire et doit être placé au début de chaque fichier ASF
* `Data Object` - obligatoire et doit suivre l'objet d'en-tête
* `Index Object(s)` - facultatif, mais utile pour fournir un accès aléatoire basé sur le temps aux fichiers ASF

L'image suivante montre la structure de fichier de niveau supérieur des fichiers ASF.

![ASF File Structure](../asf.png "ASF File Structure")

#### Objet d'en-tête de niveau supérieur ASF

L'objet Header fournit une séquence d'octets bien connue au début des fichiers ASF et peut éventuellement contenir des métadonnées telles que des informations bibliographiques. Il contient toutes les informations nécessaires pour interpréter correctement les informations contenues dans l'objet de données. L'objet d'en-tête peut inclure plusieurs objets standard, y compris, mais sans s'y limiter :

* Objet de propriétés de fichier - Contient des attributs de fichier globaux.
* Objet Stream Properties - Définit un flux multimédia numérique et ses caractéristiques.
* Objet d'extension d'en-tête - Permet d'ajouter des fonctionnalités supplémentaires à un fichier ASF tout en maintenant la compatibilité ascendante.
* Objet de description de contenu - Contient des informations bibliographiques.
* Objet de commande de script - Contient des commandes pouvant être exécutées sur la chronologie de lecture.
* Objet marqueur - Fournit des points de saut nommés dans un fichier.

L'objet d'en-tête est représenté à l'aide de la structure suivante :

|Nom du champ |Type de champ |Taille (bits)|
---|---|---|
|Identifiant d'objet| GUID | 128|
|Taille de l'objet| QWORD| 64|
|Nombre d'objets d'en-tête| DWORD | 32|
|Réservé1| OCTET | 8|
|Réservé2| OCTET | 8|

#### Objet de données de niveau supérieur ASF

Toutes les données multimédias numériques d'un fichier ASF sont contenues dans l'objet de données et sont stockées sous la forme de paquets de données ASF. Chaque paquet de données est d'une longueur fixe et contient des données pour un ou plusieurs flux multimédias numériques.

#### Objets d'index de niveau supérieur ASF

Les objets d'index de niveau supérieur ASF ont les deux types suivants :

* `Simple Index Object` - Contient un index temporel des données vidéo dans un fichier ASF. L'intervalle de temps entre les entrées d'index est constant et est stocké dans l'objet d'index simple.
* `Index Object` - Fait référence à l'Index Object, à l'Index Object Media et à l'Index Timecode Object, dont les formats sont similaires. Comme l'objet d'index simple, l'objet d'index indexe par le temps avec un intervalle de temps fixe mais n'est pas limité aux flux vidéo.

## Références

* [Format de fichier ASF - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [Format de fichier QuickTime - Wikipédia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

