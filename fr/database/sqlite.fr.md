{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier SQLITE et les API qui peuvent créer et ouvrir des fichiers SQLITE.",
  "title" :"Format de fichier SQLite",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Qu'est-ce qu'un fichier SQLite ?

Un fichier avec l'extension .sqlite est un fichier de base de données SQL léger créé avec le logiciel [SQLite](https://www.sqlite.org/index.html). Il s'agit d'une base de données dans un fichier lui-même et implémente un moteur de base de données [SQL](/fr/database/sql/) autonome, complet et hautement fiable. Les fichiers de base de données SQLite peuvent être utilisés pour partager des contenus riches entre les systèmes en échangeant simplement ces fichiers sur le réseau. Presque tous les mobiles et ordinateurs utilisent SQLite pour stocker et partager des données, et c'est le choix du format de fichier pour les applications multiplateformes. En raison de son utilisation compacte et de sa facilité d'utilisation, il est fourni avec d'autres applications. Les liaisons SQLite existent pour les langages de programmation tels que C, [C#](/fr/programming/cs/), [C++](/fr/programming/cpp/), [Java](/fr/programming/java/), [PHP](/fr/programming/php/), et plein d'autres.

## Format de fichier SQLite

SQLite est en réalité une bibliothèque de langage C qui implémente le SGBDR SQLite en utilisant le format de fichier SQLite. Avec l'évolution de nouveaux appareils chaque jour, son format de fichier a été maintenu rétrocompatible pour s'adapter aux appareils plus anciens. Le format de fichier SQLite est considéré comme un format d'archivage à long terme pour les données.

### Le fichier de base de données

Une base de données SQLite est entièrement maintenue via deux fichiers.
* Fichier de base de données principal - Contient l'état complet de la base de données SQLite
* Rollback Journal - Stocke des informations supplémentaires dans un second fichier et est utilisé lors de l'exécution de transactions. Dans le cas où SQLite est en mode WAL, un fichier journal de tête d'écriture est maintenu.

#### Fichier journal

Ce fichier est destiné à conserver toutes les informations conservées au cas où la dernière transaction n'aurait pas pu être effectuée dans des cas tels qu'une panne informatique. Ce fichier est utilisé pour restaurer le fichier de base de données dans un état cohérent.

####Pages

Le fichier de base de données SQLite principal comprend une ou plusieurs pages. À tout moment, chaque page de la base de données principale a un usage unique qui est l'un des suivants :

* La page de l'octet de verrouillage
* Une page de liste gratuite
* Une page tronc freelist
* Une page feuille de liste libre
* Une page b-tree
* Une page intérieure du tableau b-tree
* Une page de feuille de tableau b-arbre
* Une page intérieure d'index b-tree
* Une page feuille index b-tree
* Une page de débordement de charge utile
* Une page de carte de pointeur

La taille des fichiers de base de données SQLite peut aller de quelques kilo-octets à quelques giga-octets.

### En-tête SQLite

L'en-tête de la base de données SQLite se trouve dans les 100 premiers octets du fichier de base de données. Chaque fichier de base de données SQLite valide commence par 16 octets (en hexadécimal) :53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Les détails des champs d'en-tête sont comme dans le tableau suivant.

|Décalage|Taille|Description|
---|---|---|
|0|16|La chaîne d'en-tête : "Format SQLite 3\000"|
|16|2|Taille de la page de la base de données en octets. Doit être une puissance de deux entre 512 et 32768 inclus, ou la valeur 1 représentant une taille de page de 65536.|
|18|1|Version d'écriture du format de fichier. 1 pour l'héritage ; 2 pour WAL.|
|19|1|Version de lecture du format de fichier. 1 pour l'héritage ; 2 pour WAL.|
|20|1|Octets d'espace "réservé" inutilisé à la fin de chaque page. Généralement 0.|
|21|1|Fraction de charge utile embarquée maximale. Doit être 64.|
|22|1|Fraction de charge utile intégrée minimale. Doit être 32.|
|23|1|Fraction de charge utile de feuille. Doit être 32.|
|24|4|Compteur de changement de fichier.|
|28|4|Taille du fichier de base de données en pages. La "taille de la base de données d'en-tête".|
|32|4|Numéro de page de la première page principale de la liste libre.|
|36|4|Nombre total de pages de liste libre.|
|40|4|Le cookie de schéma.|
|44|4|Le numéro de format du schéma. Les formats de schéma pris en charge sont 1, 2, 3 et 4.|
|48|4|Taille du cache de pages par défaut.|
|52|4|Le numéro de page de la plus grande page d'arborescence racine en mode de vide automatique ou de vide incrémental, ou zéro dans le cas contraire.|
|56|4|Encodage du texte de la base de données. Une valeur de 1 signifie UTF-8. Une valeur de 2 signifie UTF-16le. Une valeur de 3 signifie UTF-16be.|
|60|4|La "version utilisateur" telle que lue et définie par le pragma user_version.|
|64|4|Vrai (non nul) pour le mode de vide incrémentiel. Faux (zéro) sinon.|
|68|4|L'"ID d'application" défini par PRAGMA application_id.|
|72|20|Réservé pour extension. Doit être zéro.|
|92|4|Le numéro de version valide pour.|
|96|4|SQLITE_VERSION_NUMBER|

## Références ##

* [Format de fichier SQLite - SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - Wikipédia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite - Spécifications du langage C](https://www.sqlite.org/c3ref/intro.html)

