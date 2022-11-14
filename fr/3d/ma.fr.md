{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "fichier ma", "format de fichier ma", "format de fichier", "3d","téléchargement de fichier ma", "fichier .ma", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier MA et les API qui peuvent ouvrir et créer des fichiers MA.",
  "title" :"Format de fichier MA",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## Qu'est-ce qu'un fichier MA ?

Un fichier avec l'extension .ma est un fichier de projet 3D créé avec l'application Autodesk Maya. Il contient une grande liste de commandes textuelles pour spécifier des informations sur le fichier. Un fichier **.ma** peut être ouvert et modifié dans n'importe quel éditeur de texte pour résoudre tout problème avec les commandes au cas où un fichier serait corrompu. Ces fichiers contiennent des informations permettant de définir les informations de la scène 3D telles que la géométrie, l'éclairage, l'animation et le rendu.

## Format de fichier MA

Les fichiers MA sont enregistrés sur le disque au format texte ASCII contrairement aux fichiers MB qui sont enregistrés au format de fichier binaire sur le disque. Une référence détaillée pour le format de fichier MA est disponible dans [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) et peut être consultée à pour référence du développeur.

### En-tête de fichier MA

L'en-tête du fichier MA commence par une section de commentaires qui donne les informations de création du fichier et la date de modification. Les lecteurs de fichiers Maya ignorent ce bloc car il est uniquement utilisé à des fins d'information. Un en-tête doit cependant commencer par les six premiers caractères comme "//Maya".

L'en-tête du fichier ASCII ressemble à ce qui suit.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Références de fichiers

La section des références de fichier d'un fichier .ma contient des informations sur tous les autres fichiers Maya qui sont référencés dans ce fichier. Chaque fichier référencé peut être lu à l'aide d'une seule commande de fichier contenue dans le même fichier. La syntaxe de la commande file lorsqu'elle est utilisée pour le référencement est :

```
file -r -rpr prefixString fileName;
```
ou

```
file -r -ns nameSpace fileName
```
Voici un exemple de chaîne.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Cet exemple montre que l'objet soleil contenu dans le fichier `solar` serait accessible dans ce fichier en utilisant le nom "solar_sun".

### Conditions

La section Exigences d'un fichier .ma se compose d'une série de commandes requises et indique des informations telles que la version et les informations de plug-in requises pour lire les fichiers. Un exemple de section des exigences est le suivant.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


La section suivante précise les exigences. Il s'agit d'une série de commandes requirements. Cette section du fichier indique à Maya quel logiciel est nécessaire pour charger correctement le fichier. Plus précisément, quelle version de Maya et quels plug-ins.

## Téléchargement du fichier MA
Il est un peu difficile de trouver et de télécharger le fichier MA d'un modèle 3D. Par conséquent, vous pouvez télécharger un exemple de fichier MA à partir d'ici :

- [Sample.ma](../sample.ma)


## Références

* [Organisation des fichiers Maya ASCII - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

