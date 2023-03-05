{
  "date" : "2019-10-11",
  "keywords" :[ "fichier psd", "format de fichier psd", "qu'est-ce qu'un fichier psd", "fichier", "exemple psd", "extension de fichier psd","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :" PSD - Format de fichier image Photoshop ",
  "description":"En savoir plus sur le format de fichier PSD et les API qui peuvent créer et ouvrir des fichiers PSD.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier PSD ?

PSD, Photoshop Document, représente le format de fichier natif d'Adobe Photoshop utilisé pour la conception et le développement de graphiques. Les fichiers PSD peuvent inclure des calques d'image, des calques de réglage, des masques de calque, des annotations, des informations sur les fichiers, des mots-clés et d'autres éléments spécifiques à Photoshop. Les fichiers Photoshop ont l'extension par défaut .PSD et ont une hauteur et une largeur maximales de 30 000 pixels et une limite de longueur de deux gigaoctets.

## Spécifications du format de fichier PSD ##

Les données d'un fichier PSD sont stockées dans l'ordre des octets big endian. Cela implique d'échanger les entiers courts et longs lors de la lecture ou de l'écriture sur la plate-forme Windows. Le format de fichier Photoshop est divisé en cinq parties principales. Il comporte de nombreux marqueurs de longueur qui peuvent être utilisés pour passer d'une section à la suivante. Les marqueurs de longueur sont généralement complétés par des octets pour arrondir à l'intervalle de 2 ou 4 octets le plus proche. Les cinq grandes parties sont :

* En-tête de fichier
* Données du mode couleur
* Ressources d'images
* Informations sur les calques et les masques
* Données d'image

Pour des raisons de conformité, les données doivent être écrites dans tous ces champs de la section, car Photoshop peut essayer de lire l'intégralité de la section. Cela implique également que des zéros soient écrits dans les champs ignorés lors de l'écriture dans un fichier. Le champ de longueur dans les sections délimitées par la longueur doit être utilisé pour décider quand arrêter la lecture. Dans la plupart des cas, le champ de longueur indique le nombre d'octets, et non d'enregistrements, qui suivent. Les points suivants doivent être rappelés lors de la lecture d'un fichier.

* Les valeurs de la colonne "Longueur" dans tous les tableaux sont en octets.
* Toutes les valeurs définies comme chaîne Unicode se composent de :
* Un champ de longueur de 4 octets, représentant le nombre de caractères dans la chaîne (pas d'octets).
* La chaîne de valeurs Unicode, deux octets par caractère.

### En-tête de fichier ###

L'en-tête du fichier contient les propriétés de base de l'image.

|Longueur|Description
---|---|
|4|Signature : toujours égale à '8BPS' . N'essayez pas de lire le fichier si la signature ne correspond pas à cette valeur.
|2|Version : toujours égal à 1. N'essayez pas de lire le fichier si la version ne correspond pas à cette valeur. (~*~*PSB~*~* la version est 2.)
|6|Réservé : doit être égal à zéro.
|2|Le nombre de canaux dans l'image, y compris les canaux alpha. La plage prise en charge va de 1 à 56.
|4|La hauteur de l'image en pixels. La plage prise en charge va de 1 à 30 000.
|4|La largeur de l'image en pixels. La plage prise en charge va de 1 à 30 000.
|2|Profondeur : le nombre de bits par canal. Les valeurs prises en charge sont 1, 8, 16 et 32.
|2|Le mode couleur du fichier. Les valeurs prises en charge sont : Bitmap # 0 ; Niveaux de gris # 1 ; Indexé # 2; RVB # 3 ; CMJN # 4; Multicanal # 7; Bichromie # 8; Labo n°9.

### Section des données du mode couleur ###

La section des données du mode couleur est structurée comme suit :


|Longueur|Description
---|---|
|4|La longueur des données de couleur suivantes
|variable|Les données de couleur

Les données du mode couleur ne sont disponibles que pour la couleur indexée et la bichromie telles que définies par le champ de mode dans la section En-tête de fichier. Pour tous les autres modes, cette section est représentée par des valeurs mises à zéro sur 4 octets. Pour les images couleur indexées, la longueur est de 768 et les données de couleur contiennent la table des couleurs de l'image, dans un ordre non entrelacé. Pour les images Duotone, les données de couleur contiennent la spécification bichromie (dont le format n'est pas documenté). D'autres applications qui lisent les fichiers Photoshop peuvent traiter une image bicolore comme une image grise et conserver uniquement le contenu des informations bicolores lors de la lecture et de l'écriture du fichier.

### Section des ressources d'images ###

La troisième section du fichier contient des ressources d'image. Il commence par un champ de longueur, suivi d'une série de blocs de ressources.


|Longueur|Description
---|---|
|4|Longueur de la section des ressources d'image. La longueur peut être nulle.
|Variable|Ressources d'image (blocs de ressources d'image)

Les ressources d'image sont utilisées pour stocker des données non pixelisées associées à des images telles que des trajectoires d'outils de stylet. Ils sont appelés blocs de ressources car ils contiennent des données stockées dans les ressources du Macintosh dans les premières versions de Photoshop. La structure de base des blocs de ressources d'image est illustrée ci-dessous :


|Longueur|Description
---|---|
|4|Signature : '8BIM'
|2|Identifiant unique de la ressource. ID de ressource d'image contient une liste d'ID de ressource utilisés par Photoshop.
|Variable|Nom : chaîne Pascal, complétée pour rendre la taille égale (un nom nul se compose de deux octets de 0)
|4|Taille réelle des données de ressources qui suivent
|Variable|Les données de ressources, décrites dans les sections sur les types de ressources individuelles. Il est rembourré pour uniformiser la taille.

Les ressources d'image utilisent plusieurs numéros d'identification standard.

### Informations sur les calques et les masques ###

La quatrième section d'un fichier Photoshop contient des informations sur les calques et les masques tels que le nombre de calques, les canaux dans les calques, les plages de fusion, les clés de calque de réglage, les calques d'effets et les paramètres de masque. S'il n'y a pas de couches ou de masques, cette section est représentée par un champ de 4 octets mis à zéro. Une attention particulière doit être accordée à la longueur des sections lors de la lecture de cette section en raison des valeurs mises à zéro. La disposition de la section Calque et Masque est la suivante :


|Longueur|Description
---|---|
|4|Longueur de la section d'informations sur le calque et le masque. (La longueur du PSB est de 8 octets.)
|Variable|Informations sur le calque
|Variable|Informations sur le masque de calque global
|Variable|Série de blocs étiquetés contenant divers types de données.

#### Informations sur la couche ####

Le tableau suivant montre l'organisation de haut niveau des informations de couche.


|Longueur|Description
---|---|
|4|Longueur de la section d'informations sur les calques, arrondie à un multiple de 2. (La longueur du PSB est de 8 octets.)
|2|Nombre de couches. S'il s'agit d'un nombre négatif, sa valeur absolue est le nombre de calques et le premier canal alpha contient les données de transparence pour le résultat fusionné.
|Variable|Informations sur chaque couche. Voir Enregistrements de couche décrit la structure de ces informations pour chaque couche.
|Variable|Données d'image de canal. Contient un ou plusieurs enregistrements de données d'image pour chaque couche. Les calques sont dans le même ordre que dans les informations sur les calques

### Données d'image ###

Les données de pixel d'image sont contenues dans la section Données d'image du fichier. La disposition des données dans la section Données d'image est dans l'ordre planaire, c'est-à-dire d'abord toutes les données rouges, puis toutes les données vertes, etc. Chaque plan est stocké dans l'ordre des lignes de balayage, sans octets de remplissage. La section des données d'image est organisée dans un format comme indiqué dans le tableau suivant.

|Longueur|Description
---|---|
|2|Méthode de compression : *0 = Données d'image brutes * 1 = RLE compressé les données d'image commencent par le nombre d'octets pour toutes les lignes de balayage (lignes * canaux), chaque nombre étant stocké sous la forme d'une valeur à deux octets. Les données compressées RLE suivent, chaque ligne de balayage étant compressée séparément. La compression RLE est le même algorithme de compression utilisé par la routine Macintosh ROM PackBits et la norme TIFF. *2 = ZIP sans prédiction *3 = ZIP avec prédiction.
|Variable|Les données de l'image. Ordre planaire = RRR GGG BBB, etc.

## Références ##

* [Spécifications du format de fichier PSD - Par Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Format de fichier Adobe Photoshop](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

