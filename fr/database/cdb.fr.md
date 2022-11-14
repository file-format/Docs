{
  "date" : "2021-06-16",
  "keywords" :[ "CDB", "extension", "fichier cdb", "format de fichier cdb", "Type de fichier de base de données", "Format de fichier de base de données", "qu'est-ce qu'un fichier cdb" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier CDB et les API qui peuvent créer et ouvrir des fichiers CDB.",
  "title" :"CDB - Fichier de base de données constante",
  "linktitle" : "CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-16"
}

## Qu'est-ce qu'un fichier CDB ?
Les fichiers CDB sont utilisés dans des applications critiques comme le courrier électronique. Le CDB signifie "base de données constante", un package rapide, fiable et simple pour créer ou lire des bases de données constantes. Le remplacement de la base de données est sûr contre les pannes du système. Les utilisateurs n'ont pas besoin de s'arrêter pendant une réécriture. CDB fonctionne comme un tableau associatif (sur disque), mappant les clés aux valeurs et permet de stocker plusieurs valeurs dans une seule clé.

## Format de fichier CDB
Le format de fichier CDB stocke les nombres, les décalages, les longueurs et les valeurs de hachage au format Little Endian sous forme d'entiers 32 bits non signés. Les clés et les données sont considérées comme des chaînes d'octets opaques sans traitement spécial. Au début de la base de données, l'en-tête de taille fixe représente 256 tables de hachage en listant leur position dans le fichier et leur longueur en slots. Habituellement, les données sont stockées sous la forme d'une séquence d'enregistrements, chaque enregistrement stocke la longueur de la clé, la longueur des données, la clé et les données. Il n'y a pas de règles de tri ou d'alignement. Les enregistrements sont suivis d'un ensemble de 256 tables de hachage de longueurs variables. Étant donné que zéro est une longueur valide, il peut y avoir moins de 256 tables de hachage physiquement stockées dans la base de données, mais rien n'est considéré comme 256 tables. Les tables de hachage se composent d'une série d'emplacements, chacun contenant une valeur de hachage et un décalage d'enregistrement. Les "emplacements vides" ont un décalage de zéro.

### Structure
La base de données CDB consiste en un ensemble de données complet dans un seul fichier informatique. Il contient trois parties :
- Un en-tête de taille fixe
- Données
- Un ensemble de tables de hachage.

Les recherches sont disponibles uniquement pour les clés exactes. Les recherches agissent à l'aide de l'algorithme suivant :

- Hachez la clé.
- Déterminez à quelle table de hachage et à quel emplacement cet enregistrement doit se trouver.
- Testez l'emplacement indiqué dans la table de hachage.

Pour les recherches de clés avec plus d'une valeur, des valeurs supplémentaires peuvent être trouvées en reprenant simplement la recherche à l'emplacement suivant.

#### Fonctionnalités

La structure de la base de données CDB offre plusieurs fonctionnalités :

##### Recherches rapides
Une recherche réussie dans une énorme base de données ne prend normalement que deux accès au disque et une recherche infructueuse n'en prend qu'un.
##### Faible surcharge
Une base de données utilise 2048 octets, 24 octets par enregistrement et l'espace pour les clés et les données.
##### Aucune limite aléatoire
CDB peut gérer n'importe quelle base de données jusqu'à 4 gigaoctets. Puisqu'il n'y a pas d'autres restrictions, les enregistrements n'ont même pas besoin de tenir en mémoire. Les bases de données sont stockées dans un format indépendant de la machine.
##### Remplacement rapide de la base de données atomique
La commande **cdbmake** peut réécrire une base de données entière en deux ordres de grandeur, plus rapidement que les autres packages de hachage.
##### Vidages rapides de la base de données
**cdbdump** peut imprimer le contenu d'une base de données dans un format compatible cdbmake.


## Références ##

* [cdb (logiciel) - Wikipédia](https://en.wikipedia.org/wiki/Cdb_(logiciel))
* [Spécification CDB](http://cr.yp.to/cdb.html)

