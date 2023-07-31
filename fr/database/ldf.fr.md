{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier LDF et les API qui peuvent créer et ouvrir des fichiers LDF.",
  "title" :"LDF - Format de fichier de base de données principale SQL Server",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Qu'est-ce qu'un fichier LDF ?

Un fichier avec l'extension .ldf est un fichier journal géré par Microsoft SQL Server qui est un système de gestion de base de données relationnelle (RDBMS). Toutes les transactions effectuées sur les fichiers de base de données primaires ([MDF](/fr/database/mdf/))(telles que l'insertion, la mise à jour, la suppression) sont enregistrées dans le fichier LDF. Les fichiers LDF sont des composants essentiels de toute base de données. En cas de défaillance du système, le fichier journal est utilisé pour restaurer la base de données dans un état cohérent. La taille du fichier journal des transactions peut augmenter si les transactions ne sont pas entièrement validées. Les fichiers LDF peuvent être ouverts avec l'application logicielle Microsoft SQL Server.

## Opérations enregistrées dans le fichier LDF

Un fichier journal SQL enregistre les opérations suivantes :

* Le début et la fin de chaque transaction.

* Chaque modification de données de données (insertion, mise à jour ou suppression). Cela inclut également les modifications apportées par les procédures stockées système ou les instructions DDL (Data Definition Language) à n'importe quelle table, y compris les tables système.

* Chaque étendue et allocation ou désallocation de page.

* Création ou suppression d'une table ou d'un index.

## Format de fichier LDF

Le fichier LDF se compose d'enregistrements de transaction SQL Server qui sont organisés sous forme de chaîne d'enregistrements de journal. Chaque enregistrement de journal a un numéro de séquence de journal (LSN) supérieur au LSN de l'enregistrement précédent. Les chaînes sont concaténées les unes après les autres dans le fichier. En raison des ordinateurs modernes à grande vitesse, les enregistrements peuvent être insérés là où le LSN2 existe dans le fichier journal avant LSN1. Étant donné que les opérations sont enregistrées dans une série, la modification décrite par LSN2 a été effectuée après l'enregistrement de journal LSN1. Les enregistrements d'une transaction particulière sont liés en amont à l'aide de pointeurs qui sont utilisés et accélèrent l'annulation de la transaction.
 

## Références

* [Fichiers de base de données et groupes de fichiers](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Guide d'architecture et de gestion des journaux de transactions](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql- serveur-ver15)

