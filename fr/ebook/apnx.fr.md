{
  "date" : "2021-03-11",
  "keywords" :[ "APNX", "Amazon Page Number Index", "extension", "fichier", "format", "eBook", "Amazon Kindle" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier Amazon APNX et les API qui peuvent créer et ouvrir des fichiers APNX.",
  "title" :"APNX - Index des numéros de pages Amazon",
  "linktitle" : "APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## Qu'est-ce qu'un fichier APNX ? ##

Le fichier Amazon Page Number Index qui utilise l'extension .apnx est un type de fichier eBook ; utilisé par Amazon Kindle. Ces fichiers sont en fait appelés fichiers de pagination utilisés par les appareils Kindle. Ainsi, les fichiers APNX sont généralement créés pour marquer les pages des livres électroniques Kindle. La fonction de pagination a été lancée sur les appareils Amazon Kindle depuis son firmware 3.1. Il examine le fichier APNX pour les index de page, puis le mappe avec les numéros de page du livre imprimé d'origine. Ces fichiers sont enregistrés dans les appareils Kindle avec les fichiers Amazon eBooks. Vous ne pouvez pas ouvrir ou modifier les fichiers APNX.

## Spécifications du format de fichier APNX ##

### Disposition

|octets| contenu| commentaires|
---|---|---|
|4 |00010001 | Identificateur de format. Valeur de 65537 petit-boutiste.|
|4 |début du suivant | Le décalage après l'emplacement de fin du premier en-tête. Commence une nouvelle séquence d'informations d'en-tête |
|4 |longueur| Longueur du premier en-tête |
|N |premier en-tête | Chaîne contenant l'en-tête de contenu. Il commence la séquence suivante |
|2 |inconnu | Toujours 1|
|2 |longueur | Longueur du deuxième en-tête |
|2 |nombre de pages | Nombre total d'octets après le deuxième en-tête qui représentent les pages. Ce total inclut les octets qui sont ignorés par le pageMap.|
|2 |inconnu | Toujours 32|
|N |deuxième en-tête | Chaîne contenant l'en-tête de mappage de page |
|4*N |remplissage | Le premier nombre donné dans l'en-tête de mappage de page indique le nombre d'octets 0.|
|4*N |liste de pages ||

### En-tête de contenu

L'en-tête de contenu consiste en une chaîne entourée de {} contenant des paires clé/valeur :

|contenu| commentaires|
---|---|
|contentGuid| Guid.|
|asin | Identifiant Amazon pour la version Kindle du livre.|
|cdeType | Type de cde MOBI. Devrait toujours être EBOK pour les ebooks.|
|IDrévisionfichier | Révision de ce fichier.|

#### Exemple
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### En-tête de mappage de page
L'en-tête de mappage de page consiste en une chaîne entourée de {} contenant des paires clé, valeur.

|contenu | commentaires|
---|---|
|asin | L'ISBN 10 pour le livre papier auquel les pages correspondent|
|pageCarte| Tuple à trois valeurs. Ressemble à : "(N,N,N)\
1) Nombre d'octets après l'en-tête qui commence la séquence de numérotation des pages\
2) inconnu\
3) inconnu\|
#### Exemple
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Liste des pages

La liste des pages est une séquence de décalages dans le HTML brut. Chaque
La valeur est le début d'une nouvelle page. Chaque entrée est un gros boutiste de 4 octets
int.



## Références

* [Format de fichier Amazon APNX](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX - par MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)

