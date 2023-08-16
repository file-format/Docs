{
  "date" : "2023-01-17",
  "keywords" :[ "DSN", "qu'est-ce qu'un fichier DSN", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier DSN et les API qui peuvent créer et ouvrir des fichiers DSN.",
  "title" :"Format de fichier DSN - Fichier de nom de source de base de données",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Qu'est-ce qu'un fichier DSN ?

DSN signifie "Nom de la source de données" et c'est un format de fichier utilisé pour stocker les informations de connexion à la base de données. Les fichiers DSN sont généralement utilisés conjointement avec ODBC (Open Database Connectivity) et permettent un accès facile à une base de données spécifique en fournissant les informations nécessaires pour s'y connecter, telles que le nom du serveur, le nom d'utilisateur et le mot de passe. Le fichier est généralement en texte brut et peut être créé et modifié à l'aide d'un éditeur de texte. Il peut être utilisé sur divers systèmes d'exploitation comme Windows, Linux et Mac.

## Comment créer un fichier DSN ?

La méthode de création d'un fichier DSN peut varier en fonction du système d'exploitation et des outils disponibles. Les étapes suivantes fournissent un aperçu général du processus de création d'un fichier DSN sur un système Windows.

1. Ouvrez l'administrateur de source de données ODBC en recherchant "Sources de données ODBC" dans le menu Démarrer.
2. Sélectionnez l'onglet "System DSN" et cliquez sur le bouton "Add".
3. Sélectionnez le pilote approprié pour la base de données à laquelle vous souhaitez vous connecter et cliquez sur "Terminer".
4. Remplissez les informations nécessaires pour vous connecter à la base de données, telles que le nom du serveur, le nom d'utilisateur et le mot de passe.
5. Cliquez sur "OK" pour enregistrer le fichier DSN.

Vous pouvez également créer un fichier DSN manuellement en créant un fichier texte brut avec l'extension .dsn et en saisissant les informations de connexion nécessaires au format :

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Vous pouvez ensuite utiliser le chemin de ce fichier comme DSN dans votre code/script pour vous connecter à la base de données.

## Programmes qui ouvrent le fichier DSN

Un fichier DSN est un fichier texte brut qui stocke les informations utilisées pour se connecter à une base de données, telles que le nom du serveur, le nom d'utilisateur et le mot de passe. Il est généralement utilisé en conjonction avec ODBC (Open Database Connectivity) pour fournir un accès facile à une base de données spécifique.

Pour ouvrir et afficher le contenu d'un fichier DSN, vous pouvez utiliser n'importe quel éditeur de texte tel que le Bloc-notes, Sublime Text, Atom, etc. Ces programmes vous permettront d'ouvrir le fichier DSN et d'afficher les informations de connexion qui y sont stockées.

Cependant, pour utiliser le fichier DSN pour se connecter à une base de données et exécuter des opérations telles que SELECT, INSERT, UPDATE, DELETE, etc., un programme prenant en charge ODBC, tel qu'un langage de programmation tel que Python, Java, C# ou un outil de gestion de base de données tel que Microsoft Access , SQL Server Management Studio est requis. Ces programmes peuvent utiliser les informations du fichier DSN pour se connecter à la base de données et effectuer l'opération souhaitée.

## Références

* [Qu'est-ce qu'un DSN (nom de source de données) ?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30-606e-2436fe26e89f)


