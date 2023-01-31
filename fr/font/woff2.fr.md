{
  "date" : "2023-01-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier WOFF2 - Fichier Web Open Font Format 2.0",
  "description":"Découvrez ce qu'est un fichier WOFF2 et les API qui peuvent créer et ouvrir un fichier WOFF2.",
  "linktitle" : "WOFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2023-01-10"
}

## Qu'est-ce qu'un fichier WOFF2 ?

WOFF2 est un format de fichier de police qui est une version plus compressée du Web Open Font Format (WOFF). Il a été développé pour réduire la taille des fichiers des polices Web, leur permettant de se charger plus rapidement et d'utiliser moins de bande passante. WOFF2 utilise un algorithme de compression appelé Brotli pour compresser les données de police, ce qui peut entraîner des tailles de fichier nettement inférieures à celles des polices [WOFF](/fr/font/woff/) équivalentes. Ce format est pris en charge par la plupart des navigateurs Web modernes, notamment Chrome, Firefox, Safari, Opera et Edge (à partir de la version 14).

## Format de fichier WOFF2 - Plus d'informations

La structure de fichier interne d'un fichier de police WOFF2 est composée de plusieurs parties différentes, notamment un en-tête, des métadonnées, un répertoire de table et les données de police elles-mêmes.

1. L'en-tête contient des informations sur le format général du fichier, notamment le numéro de version et le nombre de tables présentes dans le fichier.

1. La section des métadonnées contient des informations telles que le nom de la police, le copyright et d'autres informations relatives à la police.

1. Le répertoire des tables contient des informations sur les différentes tables qui composent la police, y compris leur emplacement dans le fichier et leur longueur.

1. Les données de police elles-mêmes sont divisées en plusieurs tables différentes, chacune contenant des informations spécifiques sur la police, telles que ses caractères et leurs glyphes correspondants. Ces tableaux peuvent comprendre :

* La table 'glyf' contient les contours réels des polices, y compris la forme et la taille de chaque caractère.
* Le tableau 'head' contient des informations générales sur la police, telles que son numéro de version, sa taille de conception, etc.
* La table 'hmtx' contient des informations sur les métriques de la police, y compris les largeurs et les positions des caractères.
* Chaque tableau est compressé et stocké au format de fichier WOFF2 après avoir terminé le processus d'encodage.

La structure globale est conçue pour permettre une analyse et un décodage rapides, afin que les navigateurs Web puissent charger et afficher rapidement et efficacement la police sur un site Web.

### En-tête WOFF2
L'en-tête WOFF comprend une signature d'identification qui indique le type de données incluses dans le fichier. L'en-tête WOFF avec ses champs est le suivant.

|Type|Nom du champ|Description|
---|---|---|
|UInt32|signature |0x774F4632 'wOF2' |
|UInt32| saveur |La "version sfnt" de la police d'entrée.|
|UInt32| length |Taille totale du fichier WOFF.|
|UInt16| numTables |Nombre d'entrées dans le répertoire des tables de polices.|
|UInt16| réservé |Réservé ; mis à zéro.|
|UInt32| totalSfntSize |Taille totale nécessaire pour les données de police non compressées, y compris l'en-tête sfnt, le répertoire et les tables de polices (y compris le rembourrage).|
|UInt32| totalCompressedSize Longueur totale du bloc de données compressé.|
|UInt16| majorVersion |Version majeure du fichier WOFF.|
|UInt16| minorVersion |Version mineure du fichier WOFF.|
|UInt32| metaOffset |Décalage vers le bloc de métadonnées, depuis le début du fichier WOFF.|
|UInt32| metaLength |Longueur du bloc de métadonnées compressées.|
|UInt32| metaOrigLength |Taille non compressée du bloc de métadonnées.|
|UInt32| privOffset |Décalage vers le bloc de données privé, depuis le début du fichier WOFF.|
|UInt32| privLength |Longueur du bloc de données privé.|


## Références
* [Format de fichier w3 WOFF2] (https://www.w3.org/TR/WOFF2/)

