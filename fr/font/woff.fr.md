{
  "date" : "2020-08-20",
  "keywords" :[ "fichier woff", "format de fichier woff", "qu'est-ce qu'un fichier woff", "fichier", "exemple woff", "extension de fichier woff","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - Format de fichier ouvert sur le Web",
  "description":"Un fichier WOFF est un format de police ouvert créé dans le Web Open Font Format.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## Qu'est-ce qu'un fichier WOFF ?

Un fichier avec l'extension .woff est un fichier de polices Web basé sur le Web Open Font Format (WOFF). Il a un conteneur compressé spécifique au format basé sur les types de police TrueType (.TTF) ou OpenType (.OTT). WOFF a été introduit dans le but de différencier les polices Web des fichiers de polices utilisés dans les applications de bureau. En outre, le format visait à réduire la latence du transfert des polices du serveur à l'ordinateur du client via le réseau. Plusieurs outils sont disponibles pour convertir les fichiers WOFF en TTF et en d'autres formats de fichiers de polices.

## **Format de fichier WOFF**

Le format de police WOFF compresse les tables de données de police des structures sfnt basées sur des tables utilisées dans différents types de police tels que TrueType, OpenType et Open Font Format. C'est comme un conteneur pour ces types de polices et il a également la possibilité d'inclure les métadonnées de la police et les données à usage privé à inclure dans le conteneur. Les convertisseurs utilisent les fichiers sfnt dans un fichier au format WOFF et les agents utilisateurs restaurent le fichier encodé pour l'utiliser avec le document Web. Il convient de noter que les données de police restaurées correspondent exactement au format de police d'entrée sous tous ses aspects.

Les utilitaires de fichiers WOFF contiennent souvent des fonctionnalités supplémentaires telles que le sous-ensemble de glyphes, la validation ou l'ajout de fonctionnalités de police, mais ce n'est pas nécessaire. Les agents créateur et utilisateur doivent s'assurer que la validité des données de police sous-jacentes est préservée.

### Structure du fichier WOFF

La structure du fichier WOFF est similaire à celle des polices sfnt. Il est basé sur un répertoire de tables contenant les longueurs et les décalages de chaque table de données de police. Tous les tableaux sont suivis après ces informations initiales. Le fichier contient une base de données de polices identique à celle des polices d'origine. L'ordre des tableaux est également le même mais chacun peut être compressé. Le répertoire de la table WOFF remplace cependant le répertoire de la table d'origine.

Un fichier WOFF se compose des éléments suivants :

* WOFFHeader - En-tête de fichier avec le type et la version de police de base, ainsi que les décalages vers les métadonnées et les blocs de données privés.
* TableDirectory - Répertoire des tables de polices, indiquant la taille d'origine, la taille compressée et l'emplacement de chaque table dans le fichier WOFF.
* FontTables - Les tables de données de police de la police sfnt d'entrée, compressées pour réduire les besoins en bande passante.
* ExtendedMetadata - Un bloc facultatif de métadonnées étendues, représenté au format XML et compressé pour le stockage dans le fichier WOFF.
* PrivateData - Un bloc facultatif de données privées que le concepteur de polices, la fonderie ou le fournisseur peut utiliser.

### En-tête WOFF
L'en-tête WOFF comprend une signature d'identification qui indique le type de données incluses dans le fichier. L'en-tête WOFF avec ses champs est le suivant.

|Type|Nom du champ|Description|
---|---|---|
|UInt32|signature |0x774F4646 'wOFF' |
|UInt32| saveur |La "version sfnt" de la police d'entrée.|
|UInt32| length |Taille totale du fichier WOFF.|
|UInt16| numTables |Nombre d'entrées dans le répertoire des tables de polices.|
|UInt16| réservé |Réservé ; mis à zéro.|
|UInt32| totalSfntSize |Taille totale nécessaire pour les données de police non compressées, y compris l'en-tête sfnt, le répertoire et les tables de polices (y compris le rembourrage).|
|UInt16| majorVersion |Version majeure du fichier WOFF.|
|UInt16| minorVersion |Version mineure du fichier WOFF.|
|UInt32| metaOffset |Décalage vers le bloc de métadonnées, depuis le début du fichier WOFF.|
|UInt32| metaLength |Longueur du bloc de métadonnées compressées.|
|UInt32| metaOrigLength |Taille non compressée du bloc de métadonnées.|
|UInt32| privOffset |Décalage vers le bloc de données privé, depuis le début du fichier WOFF.|
|UInt32| privLength |Longueur du bloc de données privé.|


## **Références**
* [Format de fichier w3 WOFF] (https://www.w3.org/TR/WOFF/)

