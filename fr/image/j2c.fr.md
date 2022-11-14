{
  "date" : "2019-10-11",
  "keywords" :[ "fichier j2c", "format de fichier j2c", "qu'est-ce qu'un fichier j2c", "fichier", "exemple j2c", "extension de fichier j2c","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"En savoir plus sur le format de fichier J2C et les API qui peuvent créer et ouvrir des fichiers J2C.",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## Qu'est-ce qu'un fichier J2C ?

Un fichier avec l'extension .j2c est une variante du format de fichier JPEG et est compressé avec la compression par ondelettes. Il a un système de marqueurs et de segments presque identique au format de fichier JPEG 2000. Le format de fichier J2C est tel que défini dans la partie 1 du support JPEG 2000 qui prend en charge la compression avec et sans perte. Le flux codé JPEG 2000 a été conçu pour être intégré dans [JP2](/fr/image/jp2/) ou un autre format de fichier, bien qu'il puisse apparaître seul dans un fichier. Un fichier J2C peut être ouvert avec Adobe Photoshop 2020, Adobe Illustrator 2020 et Corel Paintshop Pro.

## Format de fichier J2C

Le format de fichier J2C est le même que celui de JPEG 2000 qui est souvent enregistré sous .jp2 et .jpc. Cela fait que les fichiers J2C suivent la même approche d'encodage des métadonnées au format XML où la norme 12234-1 est utilisée comme référence entre les balises Exif et les composants XML. Il est encore amélioré par l'extension JPEG 2000 partie 2 qui combine le mécanisme d'animation et les configurations de flux de code en une seule image. Ces fichiers au format de fichier étendu sont enregistrés sous [.jpx](/fr/image/jpx/).

### Mise en page d'un fichier JPEG2000

JPEG2000 prend en charge une variété d'applications basées sur la conformité aux formats de fichiers extensibles. Bien que le type le plus simple puisse contenir une seule image, les types plus complexes peuvent inclure une série d'images, empilées les unes sur les autres ou séquencées dans le temps.

#### Boîte JP2
Il s'agit du bloc de construction de niveau supérieur du format de fichier JP2 et contient des champs de type et de longueur dans l'en-tête, ainsi qu'une section de données. Le type de boîtier le plus notable est le boîtier de flux codé contigu. Cette boîte stocke dans sa section de données le flux codé JPEG2000.

#### JPEG2000 CodeStream

Le JPEG2000 CodeStream est une séquence d'octets nécessaire pour décoder l'image compressée JPEG2000. Dans le cas où le fichier n'a rien d'autre que ce flux codé, il est appelé un fichier de flux codé brut. Habituellement, un flux codé JPEG est l'application de l'algorithme de compression JPEG2000 sur une image, bien que ce ne soit pas le seul moyen.

#### Pièces de carreaux ####

Une image codée en JPEG2000 est une collection d'unités de données appelées paquets. Ces paquets sont conservés dans le flux codé à l'intérieur de groupes de paquets appelés éléments de pavé. Avant d'encoder une image, l'encodeur divise l'image en une grille rectangulaire de blocs, appelés tuiles, où chaque tuile est encodée séparément indépendamment des autres tuiles.

{{< figure src="../JPEG2000_Codestream.png" alt="Format de fichier JPEG2000" >}}

## Compression J2C
JPEG 2000 utilise la technologie de compression par ondelettes, ce qui le rend rapide sur la base du fait que relativement peu de pixels sont affichés dans n'importe quelle fenêtre ou fenêtre où le spectateur affiche l'image. Cela peut être accentué par le fait que seuls quelques mégaoctets de pixels apparaîtront à l'écran pour des images de très grande taille (en gigaoctets). Cela permet d'extraire et de restituer rapidement uniquement la partie des données d'image qui est nécessaire pour remplir les pixels d'affichage. Cela nécessite également une technologie de décompression à grande vitesse pour accélérer le mécanisme de récupération d'image afin de créer l'imagerie requise à la volée.

J2C tire parti de la décompression rapide et ne récupère que les informations nécessaires pour que les données de pixels restituent rapidement une partie des images visibles sur les écrans. J2C est conçu principalement pour la visualisation des données et non pour les éditer.

## Identification J2C
Les fichiers JPEG 2000 ont des octets de signature `FF 4F FF 51`.

### Types mimes
Les types MIME enregistrés pour les fichiers JPEG 2000 incluent :
* image/j2c
* image/jpx
* image/jpm
* vidéo/mj2

## Améliorations par rapport à la norme JPEG
Les améliorations par rapport à la norme JPEG incluent :
* Performances de compression supérieures
* Représentation à plusieurs résolutions
* Transmission progressive par pixel et précision de résolution
* Choix de compression sans perte ou avec perte
* Résilience aux erreurs, format de fichier flexible
* Prise en charge de la plage dynamique élevée
* Informations spatiales du canal latéral

## Références ##
* [Taubman, David; Marcellin, Michel (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

