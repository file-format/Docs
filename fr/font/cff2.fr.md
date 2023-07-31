{
  "date" : "2020-08-20",
  "keywords" :[ "fichier cff2", "format de fichier cff2", "qu'est-ce qu'un fichier cff2", "fichier", "exemple cff2", "extension de fichier cff2","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF2 - Format de fichier de police compact version 2",
  "description":"En savoir plus sur le format de fichier CFF2 et les API pour créer et ouvrir des fichiers CFF2.",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Qu'est-ce qu'un fichier CFF2 ?

Le format de fichier CFF2 est la version 2.0 du format de fichier CFF et permet un stockage efficace des contours de glyphes et des métadonnées similaires au format de fichier CFF. CFF2 diffère de CFF en ce qu'il est destiné à être utilisé dans le contexte d'une police OpenType en tant que table 'sfnt' avec la balise CFF2. Il ne peut pas être utilisé en tant que programme autonome et dépend des données d'autres tables OpenType.

## Format de fichier CFF2

Les [spécifications du format de fichier CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2) contiennent des détails sur la disposition des données internes, les types de données, les tableaux et d'autres informations internes sur le format de fichier. Il peut être référé pour la référence du développeur. Certains des détails à ce sujet sont les suivants.

### Disposition des données

Les données binaires du format de fichier CFF2 sont logiquement organisées en un certain nombre de structures de données distinctes. La disposition dans les données binaires est comme indiqué dans le tableau suivant.

|Entrée |Commentaires|
---|---|
|En-tête |Emplacement fixe|
|Haut DICT| Emplacement fixe|
|INDICE mondial des sous-titres| Emplacement fixe |
|Variante |Magasin|
|FDSelect |Présent uniquement s'il y a plus d'une police DICT dans la police DICT INDEX.|
|Font DICT INDEX ||
|Tableau de polices DICT| Inclus dans la police DICT INDEX.|
|DICT privé| Un par police DICT.|

Seules les trois premières structures sont basées sur des emplacements fixes. Les autres sont atteints via des décalages et leur ordre peut être modifié.

### Types de données

Le format de fichier CFF2 utilise les types de données suivants.

|Nom |Gamme |Description|
---|---|---|
|uint8 |0 à 255 |nombre non signé 8 bits|
|uint16 |0 à 65535| Numéro non signé 16 bits |
|uint32 |0 à 4294967295| Numéro non signé 32 bits |
|Décalage |varie| Décalages de 1, 2, 3 ou 4 octets (spécifiés par le champ OffSize dans une table d'index) |
|OffTaille |1 à 4| Un nombre non signé de 1 octet spécifie la taille d'un ou plusieurs champs Décalage |

Il stocke toutes les données numériques multi-octets et les champs de décalage dans l'ordre des octets big-endian. Le format CFF2 est exempt d'octets de remplissage car il ne respecte aucune restriction d'alignement.

### Données DICT

Les fichiers CFF2 contiennent les données du dictionnaire de polices sous forme de paires clé-valeur dans un format tokenisé compact. Les clés de dictionnaire sont codées sous forme d'opérateurs de 1 ou 2 octets et les valeurs de dictionnaire sont codées sous forme d'opérandes numériques de taille variable. Trois structures utilisent le format de données DICT : `Top DICT`, `Font DICT` et `Private DICT`. Un certain nombre de types d'opérandes entiers de tailles variables sont définis et codés comme indiqué dans le tableau suivant (le premier octet de l'opérande est b0, le second est b1, etc.).

|Taille |plage b0 |Plage de valeurs |Calcul de la valeur|
---|---|---|---|
|1 |32 à 246| -107 à +107 |b0 - 139|
|2 |247 à 250| +108 à +1131 |(b0 - 247) * 256 + b1 + 108|
|2 |251 à 254| -1131 à -108| -(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 à +32767| b1 << 8 | b2|
|5 |29| -(2^31) à +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Entête

Les données binaires commencent par un en-tête ayant le format indiqué dans le tableau ci-dessous.

|Type |Nom |Description|
---|---|---|
|uint8| version majeure| Mettre en forme la version majeure. Réglez sur 2.|
|uint8| version mineure| Formater la version mineure. Mettre à zéro.|
|uint8| headerSize| Taille de l'en-tête (octets).|
|uint16| topDictLength| Longueur de la structure Top DICT en octets.|

## Références

* [Format de fichier CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

