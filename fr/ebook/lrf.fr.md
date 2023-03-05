{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "fichier", "extension", "format", "eBook", "Livre numérique" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier LRF et les API qui peuvent créer et ouvrir des fichiers LRF.",
  "title" :"Format de fichier LRF - Un fichier de lecteur portable Sony",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Qu'est-ce qu'un fichier LRF ?

Un fichier avec l'extension .lrf est un fichier eBook à large bande (BBeB) qui contient des données pour un Sony BBeB, notamment du texte, des images et des données de pagination. Le fichier est enregistré dans un format binaire compressé qui contient un en-tête, un nombre spécifié d'objets et un index d'objet. Les fichiers LRF et LRX contiennent les deux formats de livre BBeB disponibles. Les fichiers LRF ne sont pas chiffrés et peuvent être compilés à partir de fichiers [LRX](/fr/ebook/lrf/). Les fichiers LRF peuvent être convertis à partir de plusieurs autres types de fichiers, notamment PDF et HTML. Si votre ordinateur ne peut pas ouvrir le fichier LRF, vous n'avez probablement pas le logiciel installé pour ouvrir ou modifier les fichiers LRF. Les programmes pouvant ouvrir les fichiers LRF sont Calibre, BookDesigner, Makelrf et Canon Book Creator pour Windows, Calibre pour Linux, Calibre et Sony Reader pour Macintosh.

## Bref historique

Le type de fichier LRF est avant tout associé à Line Rider par [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). Le Line Rider est un jouet de physique Internet et a été inventé en septembre 2006 par un étudiant universitaire slovène, Boštjan Čadež. Les liseuses de livres électroniques de marque Sony (telles que les lecteurs Sony PRS-500 et Sony Librie) utilisent l'extension de fichier LRF pour leurs documents et textes. Ce type de fichier propriétaire est désormais obsolète, ainsi que les fichiers LRS et LRX associés. Ces trois types de fichiers constituaient le livre électronique BroadBand (BBeB), qui a été abandonné en 2010 lorsque Sony a commencé à vendre ses livres électroniques au format EPUB.

## Format de fichier LRF

Les spécifications détaillées du format de fichier LRF sont disponibles sur [archive Web](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). Un fichier LRF se compose de :
* un en-tête
* un certain nombre d'objets
* un index d'objet.

Toutes ces valeurs sont dans l'ordre Intel (LSB en premier).

### En-tête LRF

|Offset (hex) |Taille(octets) |Nom/signification| Valeur d'exemple|
---|---|---|---|
|0 |8| Signature FRL| 4C 00 52 00 46 00 00 00 = "LRF" en Unicode|
|8 |2| édition ?| 999 dans la plupart des fichiers |
|A |2| "Psuedo-cryptage" |octet de clé 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| Nombred'objets |342|
|18 |8| DécalageIndexObjet| 0x00093440|
|20 |4| inconnu | 0|
|24 |1| Drapeaux| (16 - de l'arrière vers l'avant, 1 = de l'avant vers l'arrière) 16|
|25 |1| inconnu |(remplissage ?) 0|
|26 |2| inconnu | 1600|
|28 |2| inconnu | (remplissage ?) 0|
|2A |2| Hauteur ?| 600|
|2C |2| Largeur ?| 800|
|2E |1| inconnu | 24|
|2F |1| inconnu |(remplissage ?) 0|
|30 |0x14| inconnu | zéros |
|44 |4| ID d'objet du seul objet PlaneStream (0x1E) | 0x0042|
|48 |4| inconnu |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Références

* [Format de fichier LRF](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - Par Wikipédia](https://en.wikipedia.org/wiki/BBeB)

