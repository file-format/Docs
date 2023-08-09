{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier NSF et les API qui peuvent créer et ouvrir des fichiers NSF.",
  "title" :"Format de fichier NSF - Format de base de données Lotus Notes",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Qu'est-ce qu'un fichier NSF ?

Un fichier avec l'extension .nsf (Notes Storage Facility) est un format de fichier de base de données utilisé par le [logiciel IBM Notes](https://en.wikipedia.org/wiki/HCL_Domino), qui était auparavant connu sous le nom de Lotus Notes. Il définit le schéma pour stocker différents types d'objets tels que les e-mails, les rendez-vous, les documents, les formulaires et les vues. Toutes ces informations sont contenues dans un seul fichier NSF pour la collaboration commerciale similaire à un fichier PST/OST. Certaines des applications pouvant ouvrir les fichiers NSF incluent IBM Lotus Notes et IBM Domino.

## Spécifications du format de fichier NSF

Les fichiers NSF sont de nature binaire et leurs spécifications sont disponibles auprès de Joachim Metz sur [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc). Selon ces détails, un fichier NSF comprend :

* En-tête de fichier
* En-tête de base de données

De plus, il se compose de :

* Superbloc
* Bloc de description de bucket
* Bitmap
* Seau de vecteur de relocalisation d'enregistrement
* Seaux récapitulatifs
* Ensembles non récapitulatifs


### En-tête de fichier NSF

L'en-tête du fichier NSF a une taille de 6 octets. Cela consiste en:

|Décalage|Taille|Valeur|Description|
---|---|---|---|
0|2|0x1a 0x00|Signature|
2|4| |La taille de l'en-tête de la base de données|

### En-tête de la base de données

L'en-tête de la base de données NSD contient les valeurs confirmées suivantes.

* Informations sur la base de données
* Identifiant de la base de données (DBID)
* Informations de réplication
* Indicateurs de tampon d'informations de base de données
* Titre
* Catégories
* Classer
* Classe de conception (nom du modèle)
* Identifiants de notes spéciales
* Rembourrage
* Informations de la base de données 2
* Informations de la base de données 3
* Informations de la base de données 4
* Informations de la base de données 5
* Rembourrage
* Identifiant d'instance de base de données (DBIID)
* Historique de réplication

## Références

* [Format NSF - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

