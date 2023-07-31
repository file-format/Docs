{
  "date" : "2020-08-20",
  "keywords" :[ "fichier cff", "format de fichier cff", "qu'est-ce qu'un fichier cff", "fichier", "exemple cff", "extension de fichier cff","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - Format de fichier de police compact",
  "description":"En savoir plus sur le format de fichier CFF et les API pour créer et ouvrir des fichiers CFF.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Qu'est-ce qu'un fichier CFF ?

Un fichier avec l'extension .cff est un format de police compact et est également connu sous le nom de PostScript Type 1 ou CIDFont. CFF agit comme un conteneur pour stocker plusieurs polices ensemble dans une seule unité appelée FontSet. La conception des polices CFF permet d'intégrer un code de langage PostScript qui permet une flexibilité et une extensibilité supplémentaires du format pour une utilisation avec des environnements d'impression. Les fichiers de police CFF peuvent être ouverts et convertis à l'aide d'API telles que [Aspose.Font](https://products.aspose.com/font).

## Format de fichier CFF

Les fichiers CFF sont des fichiers binaires qui contiennent une disposition de données structurées, des types de données définis, un en-tête, une organisation de glyphes et des dictionnaires de tables. Vous trouverez plus de détails à ce sujet dans les [spécifications du format de police compacte](https://learn.microsoft.com/en-us/typography/opentype/spec/cff).

### Disposition des données
La disposition des données du format de fichier CFF est comme indiqué ci-dessous.

|Entrée|Commentaires|
---|---|
|En-tête|–|
|NomINDEX|–|
|Haut INDEX DICT|–|
|INDEX de chaîne|–|
|INDICE global des sous-titres|–|
|Encodages–Charsets|–|
|FDSelect|CIDFonts uniquement|
|CharStrings INDEX|par police|
|Font DICT INDEX|par police, CID Fonts uniquement|
|DICT privé|par police|
|Local Subr INDEX|par police ou par DICT privé pour CIDFonts|
|Avis de droit d'auteur et de marque|–|

### Types de données

Les types de données CFF sont indiqués dans le tableau suivant.

|Nom|Gamme|Description|
---|---|---|
|Carte8|0 –255|Numéro non signé de 1 octet|
|Carte16|0 – 65535|numéro non signé de 2 octets|
|Décalage|varie|Décalage de 1, 2, 3 ou 4 octets (spécifié par le champ OffSize)|
|OffSize|1–4|nombre non signé de 1 octet spécifie la taille d'un ou plusieurs champs de décalage|
|SID|0 – 64999|Identifiant de chaîne de 2 octets|

### Entête

Les données binaires commencent par un en-tête ayant le format indiqué dans le tableau suivant.

|Type|Nom|Description|
---|---|---|
|Card8|major|Version majeure du format (à partir de 1)|
|Card8|minor|Formater la version mineure (commençant à 0)|
|Carte8|taillehdr| Taille de l'en-tête (octets) |
|OffSize|offSize|Décalage absolu (0) taille|

## Références

* [Tableau des formats de police compacts](https://learn.microsoft.com/en-us/typography/opentype/spec/cff)
* [Format de fichier CFF](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [Jeu de cartes CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

