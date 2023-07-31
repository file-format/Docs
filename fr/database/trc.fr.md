{
  "date" : "2021-08-24",
  "keywords" :[ "fichier trc", "format de fichier trc", "qu'est-ce qu'un fichier trc", "fichier", "exemple trc", "extension de fichier trc","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier TRC et les API qui peuvent créer et ouvrir des fichiers TRC.",
  "title" :"TRC - Fichier de suivi SQL Server",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Qu'est-ce qu'un fichier TRC ?
Un fichier avec l'extension .trc contient les résultats de trace de l'activité d'une base de données du serveur Miscrosoft SQL. Ces fichiers sont créés par un logiciel SQL Server Profiler ; généralement fourni avec le logiciel Microsoft SQL Server. Les administrateurs de base de données peuvent analyser une séquence d'instructions de base de données et peuvent consulter le journal de suivi si des erreurs ou des avertissements sont suspectés. Ces fichiers se trouvent généralement dans le dossier LOG typique de MSSQL à l'intérieur du répertoire Program Files sur un système d'exploitation Windows.

## Format de fichier TRC
Le format de fichier TRC est utilisé par SQL Server Profiler pour générer automatiquement une nouvelle trace des instructions récemment exécutées par le serveur MS SQL. Le SQL Server Profiler utilise le modèle par défaut pour toute nouvelle trace. Cependant, le logiciel comprend plusieurs modèles prédéfinis pour surveiller certains types d'événements. SQL Server Profiler peut également être utilisé pour créer des modèles qui définissent les classes d'événements et les colonnes de données à inclure dans les traces.

### Modèles prédéfinis
Voici la liste de certains modèles prédéfinis inclus dans SQL Server Profiler :
- **SP_Counts** : capture le comportement d'exécution des procédures stockées au fil du temps.
- **Standard** : Point de départ générique pour la création d'une trace.
- **TSQL** : capture toutes les instructions Transact-SQL soumises à SQL Server par les clients et l'heure d'émission.
- **TSQL_Duration** : capture toutes les instructions Transact-SQL soumises à SQL Server par les clients, leur temps d'exécution et les regroupe par durée.
- **TSQL_Grouped** : utilisé pour enquêter sur les requêtes d'un client ou d'un utilisateur particulier.
- **TSQL_Locks** : utilisé pour résoudre les blocages, verrouiller le délai d'expiration et verrouiller les événements d'escalade.
- **TSQL_Replay** : utilisé pour effectuer des réglages itératifs, tels que des tests de performances.
- **TSQL_SPs** : permet d'analyser les étapes des composants des procédures stockées.
- **Tuning** : permet de produire une sortie de trace que Database Engine Tuning Advisor peut utiliser comme charge de travail pour régler les bases de données.
### Corréler une trace avec les données du journal des performances Windows
Le SQL Server Profiler peut être utilisé pour ouvrir un journal de performances Microsoft Windows, pour choisir les compteurs à corréler avec une trace et afficher les compteurs de performances sélectionnés à côté de la trace dans l'interface graphique du MS SQL Server Profiler. Pour indiquer les données du journal de performances qui sont en corrélation avec l'événement de trace sélectionné, une barre verticale rouge dans le volet de la fenêtre de données du Moniteur système du Générateur de profils SQL Server.


## Références ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

