{
  "date" : "2019-12-10",
  "keywords" :[ "DIF", "fichier", "extension", "format de fichier", "Fichier d'échange de données", "Feuille de calcul" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Votre guide de format de fichier pour savoir ce qu'est une extension de fichier DIF et les API qui peuvent créer et ouvrir des fichiers DIF.",
  "title" :"DIF - Format de fichier d'échange de données",
  "linktitle" : "DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Qu'est-ce qu'un fichier DIF ?

DIF signifie Data Interchange Format qui est utilisé pour importer/exporter des données de feuilles de calcul entre différentes applications. Ceux-ci incluent Microsoft Excel, OpenOffice Calc, StarCalc et bien d'autres. Il stocke les données contenues dans une seule feuille de calcul qui est la seule limitation de ce format de fichier.

## Bref historique du format de fichier DIF ##

Le format de fichier DIF a été développé par Software Arts, Inc. au début des années 1980. Les spécifications de format de fichier pour DIF ont été incluses dans VisiCalc, le premier tableur pour ordinateurs personnels. Ces spécifications étaient protégées par copyright en 1981 et étaient une marque déposée de Software Arts Products Corp.

## Format de fichier DIF ##

DIF stocke le contenu de la feuille de calcul dans un fichier texte ASCII qui lui permet d'être visualisé et modifié avec un éditeur de texte. Le format a sa place dans la liste des formats de sérialisation des données pour ses caractéristiques d'échange de données. Un fichier DIF se compose de 2 sections ; un en-tête et des données.

Tout dans DIF est représenté par un morceau de 2 ou 3 lignes. Les en-têtes obtiennent un bloc de 3 lignes ; données, 2.

* Les blocs d'en-tête commencent par un identifiant de texte composé uniquement de majuscules, de caractères alphabétiques uniquement et de moins de 32 lettres. La ligne suivante doit être une paire de nombres et la troisième ligne doit être une chaîne entre guillemets.
* Les blocs de données commencent par une paire de nombres et la ligne suivante est une chaîne entre guillemets ou un mot-clé.

### Valeurs ###

Une valeur occupe deux lignes, la première une paire de nombres et la seconde une chaîne ou un mot-clé. Le premier chiffre de la paire indique le type :

* −1 – type directif, le deuxième nombre est ignoré, la ligne suivante est l'un de ces mots clés :
** BOT - début de tuple (début de ligne)
** EOD – fin des données
* 0 - type numérique, la valeur est le deuxième nombre, la ligne suivante est l'un de ces mots-clés :
** V – valide
** NA – non disponible
** ERREUR - erreur
** VRAI - vraie valeur booléenne
** FALSE – fausse valeur booléenne
* 1 – type chaîne, le deuxième nombre est ignoré, la ligne suivante est la chaîne entre guillemets doubles

### Bloc d'en-tête DIF ###

Le bloc d'en-tête d'un fichier DIF comprend une ligne d'identification suivie des deux lignes d'une valeur. Les valeurs numériques dans les blocs d'en-tête utilisent uniquement une chaîne vide au lieu des mots-clés de validité. Les détails de ces morceaux d'en-tête sont les suivants.

* TABLE - une valeur numérique suit la version, la deuxième ligne inutilisée de la valeur contient un commentaire de générateur
* VECTEURS - le nombre de colonnes suit comme une valeur numérique
* TUPLES - le nombre de lignes suit sous forme de valeur numérique
* DATA - après une valeur numérique fictive de 0, les données du tableau suivent, chaque ligne précédée d'une valeur BOT, le tableau entier terminé par une valeur EOD

### Exemple DIF ###

L'exemple suivant montre le contenu d'une feuille de calcul simple et sa représentation DIF équivalente.


|Nom|Âge
---|---|
|Bob|34
|Feuille|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Références ##

* [ DIF - Par Wikipédia] (https://en.wikipedia.org/wiki/Data_Interchange_Format)

