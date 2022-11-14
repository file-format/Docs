{
  "date" : "2019-12-10",
  "keywords" :[ "XLSB", "fichier", "extension", "format de fichier", "Fichier tableur binaire Excel" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Votre guide de format de fichier pour savoir ce qu'est un fichier XLSB et les API qui peuvent les créer et les ouvrir.",
  "title" :"Qu'est-ce qu'un fichier XLSB ?",
  "linktitle" : "XLSB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Qu'est-ce qu'un fichier XLSB ?

Le format de fichier XLSB spécifie le format de fichier binaire Excel, qui est une collection d'enregistrements et de structures qui spécifient le contenu du classeur Excel. Le contenu peut inclure des tableaux de nombres non structurés ou semi-structurés, du texte, ou à la fois des nombres et du texte, des formules, des connexions de données externes, des graphiques et des images. Contrairement à [XLSX](/fr/spreadsheet/xlsx/) (qui est basé sur le format de fichier Open XML), le XLSB représente un fichier de classeur Excel binaire. Les fichiers XLSB peuvent être lus et écrits plus rapidement, ce qui les rend utiles pour travailler avec des fichiers volumineux. XLSB est rarement utilisé pour stocker des classeurs car XLSX (et auparavant [XLS](/fr/spreadsheet/xls/)) sont les formats de fichiers sélectionnés par l'utilisateur les plus courants pour enregistrer des classeurs. Il peut être ouvert par Microsoft Office 2007 et supérieur.

## Spécifications du format de fichier XLSB ##

Les spécifications de format de fichier pour le format de fichier XLSB ont été rendues publiques en 2008 en tant que version 1.0. Depuis lors, les spécifications ont été révisées plusieurs fois et la dernière version des spécifications (v 10.0) a été publiée en avril 2018. Les spécifications sont disponibles publiquement par Microsoft sous [[MS-XLSB] - Spécifications du format de fichier binaire Excel](https:/ /msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) et doit être consulté par quiconque pour lire ou écrire des fichiers au format de fichier XLSB.

## Structure du fichier XLSB ##

Un fichier XLSB est un package composé d'un ensemble de pièces. Ces parties contiennent des informations sur le contenu d'un classeur, y compris les données du classeur et la structure du package. Certaines parties contiennent des informations stockées à l'aide d'enregistrements binaires, certaines au format XML, tandis que d'autres contiennent des informations stockées sous forme de flux binaire d'octets. Chaque enregistrement binaire contient zéro ou plusieurs champs structurés contenant les données du classeur.

#### Forfait ####

Un package XLSB est une archive [ZIP](/fr/compression/zip/) qui doit contenir exactement une partie du classeur. Cette partie doit être la cible d'une relation dans cette partie de relation de package. La partie classeur est la partie de départ du document XLSB.

#### Partie ####

Une partie est un flux d'octets auquel est associé un type de contenu qui spécifie la nature et le type de contenu stocké dans la partie. Certaines parties stockent des informations au format binaire tandis que d'autres stockent des informations au format XML. La section [énumération des pièces](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) du document de spécifications répertorie les pièces valides, les types de contenu et les relations obligatoires/facultatives entre toutes les pièces dans un paquet.

#### Relation ####

Une ressource source et une ressource cible sont liées par une relation. Une relation peut être :

**Relation de package :** où la cible est une partie et la source est le package dans son ensemble

**Relation partie à partie :** où la cible est une partie et la source est une partie du package

**Relation explicite :** où une ressource est référencée à partir du contenu d'une partie source en faisant référence à la valeur d'attribut ID d'un élément de relation

**relation implicite** est une relation qui n'est pas explicite

**Relation interne :** où la cible fait partie du package

**Relation externe :** où la cible est une ressource externe ne figurant pas dans le package

#### Enregistrement ####

Un enregistrement est le bloc de construction de base utilisé pour stocker des informations sur les fonctionnalités d'un classeur. Chaque enregistrement binaire est une séquence d'octets de longueur variable. Un enregistrement binaire se compose de trois composants :

* un type d'enregistrement
* une taille d'enregistrement, et
* les données d'enregistrement spécifiques à ce type d'enregistrement.

**Type d'enregistrement :** Le type d'enregistrement indique le type d'enregistrement spécifié par l'enregistrement. Il précise également la structure des données d'enregistrement propre à cet enregistrement. Les types d'enregistrement valides sont répertoriés dans la section [Record Enumeration](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) du document de spécifications. Le type d'enregistrement doit être un ou deux octets et doit être supérieur ou égal à 128 et inférieur à 16384.

**Taille d'enregistrement :** La taille d'enregistrement spécifie le nombre d'octets qui spécifie la taille totale des données d'enregistrement. Cette valeur DOIT être comprise entre un et quatre octets. Cette valeur DOIT être d'un octet si le bit de poids fort de l'octet de poids faible est égal à 0 ; sinon, cette valeur DOIT être supérieure à un octet. Si le nombre d'octets est supérieur à un octet, le bit de poids fort de chaque octet successif spécifie si un octet supplémentaire est utilisé. Si le bit de poids fort du deuxième octet est égal à 1, alors cette valeur DOIT utiliser un troisième octet supplémentaire. Si le bit de poids fort du troisième octet est égal à 1, alors cette valeur DOIT utiliser un quatrième octet supplémentaire. Le bit de poids fort du quatrième octet DOIT être ignoré. La valeur se compose des sept bits de poids faible de chaque octet combinés. Les bits de poids faible et les moins significatifs sont contenus dans le premier octet, et chaque octet successif contient des bits d'ordre supérieur à l'octet précédent.

**Données d'enregistrement :** Le composant de données d'enregistrement contient des champs qui correspondent à un type d'enregistrement particulier et comprennent le reste de l'enregistrement. L'ordre et la structure des champs pour un type d'enregistrement donné répertorié dans Énumération d'enregistrements sont spécifiés dans la section correspondante pour ce type d'enregistrement dans Enregistrements. La taille totale du composant de données d'enregistrement DOIT être égale à la taille de l'enregistrement. Les champs du composant de données d'enregistrement peuvent contenir des valeurs simples, des tableaux de valeurs, des structures de plusieurs champs, des tableaux de champs et des tableaux de structures.

#### Exemple d'enregistrement XLSB ####

Le type et la taille d'enregistrement suivants spécifient un enregistrement **BrtCommentText** d'une taille de 200 octets :

11111101 00000100 11001000 00000001 [Champs d'enregistrement]

Le premier octet est 11111101, spécifiant une valeur basse de 125 et indiquant que le type d'enregistrement nécessite un deuxième octet. Le deuxième octet est 00000100, spécifiant une valeur élevée de 4 * 128, ce qui équivaut à 512. La valeur du type d'enregistrement est 125 + 512, ou 637, ce qui correspond à un type d'enregistrement **BrtCommentText**. L'octet suivant est 11001000, spécifiant une valeur basse de 72 et que la taille de l'enregistrement nécessite un deuxième octet. Le deuxième octet est 00000001, spécifiant une valeur supérieure de 1 * 128 et indiquant que la taille de l'enregistrement ne nécessite pas d'octet supplémentaire. La taille d'enregistrement est 72 + 128, ou 200, ce qui spécifie la taille totale, en octets, du composant de données d'enregistrement. Les champs du composant de données d'enregistrement sont spécifiés par **BrtCommentText**.

## Références ##

* [[MS-XLSB] - Format de fichier binaire Excel (.xlsb)](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)

