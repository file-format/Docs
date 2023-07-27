{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "extension", "fichier", "format", "système", "Initiation", "extension de répertoire", "programmes", "ordinateur", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - Format de fichier d'initiation",
  "description":"En savoir plus sur le format de fichier INI et les API qui peuvent créer et ouvrir des fichiers INI.",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Qu'est-ce qu'un fichier INI ? ##

Un fichier INI est un document de configuration de message pour les programmes informatiques qui contient des clés publiques pour les caractéristiques et les sections qui organisent les attributs dans un cadre et une grammaire. Ces documents de configuration de format de fichier système tirent leur nom de l'extension de répertoire du système d'exploitation MS-DOS INI, qui signifie initiation. Il a popularisé cette forme de configuration logicielle. De nombreux programmes sur d'autres applications logicielles utilisent divers ajouts de noms de fichiers, tels que CONF et [CFG](/fr/system/cfg/), bien que le format ait établi une norme non officielle dans de nombreuses situations de configuration.

## Bref historique des fichiers INI##

Initialement, la principale technique de configuration du programme de Windows était un format de fichier texte composé de lignes de texte avec une paire cruciale par ligne, divisée en sections. Les pilotes de périphériques, les polices de caractères et les lanceurs de démarrage étaient tous stockés dans ce format. Les paramètres individuels étaient également couramment stockés dans les fichiers INI par les applications.
Jusqu'à Windows 3.1x, le format était pris en charge sur les plates-formes Microsoft Windows 16 bits. À partir de Windows 95, Microsoft a commencé à encourager les développeurs à utiliser le registre Windows au lieu des fichiers INI pour la configuration.

## Fichier INI - Spécifications du format de fichier

### Clés/Propriétés ###

La clé/propriété est l'élément le plus basique d'un fichier INI. Un symbole égal (=) sépare le nom et la valeur de chaque clé. À gauche du signe égal se trouve l'endroit où le nom s'affiche. Le symbole égal et le point-virgule sont des lettres discrètes dans le système Windows et ne peuvent donc pas être utilisés dans la clé. N'importe quel caractère peut être utilisé dans la valeur.

```
name=value
```

### Sections ###

Le commentaire de section apparaît entre crochets ([]) sur sa propre ligne. Après la définition de la section, toutes les clés sont liées à cette section. Les sections se terminent à la toute prochaine désignation de section ou à la fin du document ; il n'y a pas de séparateur spécifique de "fin de section". Les sections ne peuvent pas être empilées ; ils ne peuvent être nommés qu'une seule fois et n'ont pas besoin d'être liés.

```
[section]
a=a
b=b
```

### Modification des fonctionnalités ###

Le format de fichier INI n'a pas de définition acceptée à l'échelle mondiale. De nombreuses applications informatiques comportent des fonctions en plus de celles déjà citées. La liste ci-dessous comprend certaines caractéristiques communes qui peuvent ou non être incluses dans un programme individuel.

* Commentaires
* Caractères d'échappement
* Noms en double


## Exemple INI ##

L'exemple de fichier INI se présente comme suit :

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Référence ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

