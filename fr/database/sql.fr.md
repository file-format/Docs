{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier SQL et les API qui peuvent créer et ouvrir des fichiers SQL.",
  "title" :"Format de fichier SQL - Un fichier de données de langage de requête structuré",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Qu'est-ce qu'un fichier SQL ?

Un fichier avec l'extension .sql est un fichier SQL (Structured Query Language) qui contient du code pour fonctionner avec des bases de données relationnelles. Il est utilisé pour écrire des instructions SQL pour les opérations CRUD (créer, lire, mettre à jour et supprimer) sur les bases de données. Les fichiers SQL sont courants lorsque vous travaillez avec des bases de données de bureau et Web. Il existe plusieurs alternatives à SQL telles que Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL et plusieurs autres. Les fichiers SQL peuvent être ouverts par les éditeurs de requêtes de Microsoft SQL Server, MySQL et d'autres éditeurs de texte brut tels que le Bloc-notes sur le système d'exploitation Windows.

## Bref historique

* Développé et introduit par Donal D. Chamberlin et Raymond F. Boyce chez IBM au début des années 1970
* Utilisé pour stocker et récupérer des données à partir du système de gestion de base de données quasi-relationnel original d'IBM, System R
* A commencé à être utilisé dans la base de produits commerciaux sur leur prototype System R, y compris System/38, SQL/DS et DB2, qui étaient disponibles dans le commerce en 1979, 1981 et 1983, respectivement.
* Officiellement adopté par les groupes de normes ANSI et ISO en tant que norme "Database Language SQL" pour les systèmes de gestion de bases de données relationnelles (RDBMS) d'ici 1986

## Format de fichier SQL

Les fichiers SQL sont au format texte brut et peuvent comprendre plusieurs éléments de langage. Plusieurs instructions peuvent être ajoutées à un seul fichier SQL si leur exécution est possible sans dépendre les unes des autres. Ces commandes SQL peuvent être exécutées par des éditeurs de requêtes pour effectuer des opérations CRUD.

### Éléments du langage SQL

Les éléments du langage SQL sont répertoriés ci-dessous.

|Élément|Description|
---|---|
|Clauses| Composants constitutifs des instructions et des requêtes.|
|Expressions| Peut produire soit des valeurs scalaires, soit des tableaux composés de colonnes et de lignes de données|
|Prédicats| Spécifiez les conditions qui peuvent être évaluées selon la logique à trois valeurs SQL (3VL) (vrai/faux/inconnu) ou les valeurs de vérité booléennes et sont utilisées pour limiter les effets des instructions et des requêtes, ou pour modifier le déroulement du programme.|
|Requêtes| Récupérez les données en fonction de critères spécifiques. C'est un élément important de SQL.|
|Déclarations| Peut avoir un effet persistant sur les schémas et les données, ou peut contrôler les transactions, le déroulement du programme, les connexions, les sessions ou les diagnostics.|

### Exemple SQL
L'instruction SQL suivante crée une table nommée **DATA**, suivie de commandes "INSERT" supplémentaires pour insérer des enregistrements dans cette table.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## Références ##

* [SQL par Wikipédia](https://en.wikipedia.org/wiki/SQL)
* [Syntaxe SQL](https://en.wikipedia.org/wiki/SQL_syntax)

