{
  "date" : "2021-05-03",
  "keywords" :[ "SDF", "fichier sdf", "qu'est-ce qu'un fichier sdf", "comment ouvrir un fichier sdf", "extension", "fichier", "format de fichier sdf", "type de fichier de base de données", "format de fichier de base de données ", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier SDF et les API qui peuvent créer et ouvrir des fichiers SDF.",
  "title" :"SDF - Fichier de base de données compact SQL Server",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## Qu'est-ce qu'un fichier SDF ?
Un fichier avec l'extension .sdf contient la base de données Microsoft SQL Server Compact (SQL CE), également appelée base de données relationnelle compacte. produit par Microsoft pour les applications conçues pour les appareils mobiles et les ordinateurs de bureau. Il prend en charge les systèmes d'exploitation 32 et 64 bits et le contenu complet de la base de données est inclus dans un seul fichier SDF et peut occuper plus de 4 Go d'espace disque. Pour des raisons de sécurité, un fichier .sdf peut être crypté avec un cryptage 128 bits. Le runtime SQL CE installe un accès multi-utilisateur parallèle au fichier .sdf. Le fichier SDF peut être copié via **QuickOnce** ou simplement il peut être copié vers la destination pour le déploiement du système.

## Format de fichier SDF
Un fichier SDF contient une base de données généralement appelée base de données relationnelle compacte. Un fichier SDF contient toutes les informations relatives à la base de données et SQL Server Compact est un moteur de base de données léger et gratuit qui est utilisé pour gérer les fichiers .sdf. La taille du fichier .sdf ne doit pas dépasser la limite de 4 Go de taille. Les fichiers SDF ne stockent pas les informations sur les procédures stockées, les déclencheurs ou les vues. Les applications utilisant une base de données SQL CE n'ont pas besoin de spécifier le chemin d'accès à un fichier SDF dans la chaîne de connexion ADO.NET, à la place, il peut être mentionné comme |DataDirectory|\database_name.sdf, définissant le répertoire de données défini dans le manifeste d'assemblage pour l'application
La convention de dénomination .sdf est facultative et n'importe quelle extension peut être utilisée pour enregistrer le fichier. La configuration d'un mot de passe pour le fichier de base de données est une étape facultative. Pour compresser ou réparer la base de données, le fichier doit être enregistré avec l'option **base de données compactée/réparée**.

## Références

* [SQL Server Compact - Wikipédia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [Utilisation de SQL Server Compact pour les applications Web ASP.NET](https://learn.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


