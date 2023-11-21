{
"date": "2023-06-12",
  "keywords": [
"bak",
"fichier bak",
"Sauvegarde de la base de données Microsoft SQL Server",
"qu'est-ce qu'un fichier bak",
"comment ouvrir le fichier bak",
"déposer",
"extension de fichier bak",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier BAK - Sauvegarde de la base de données Microsoft SQL Server",
  "description":"Découvrez le format de sauvegarde BAK SQL Server et les API permettant de créer et d'ouvrir des fichiers BAK.",
"linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
"parent": "base de données"
}
},
"lastmod": "2023-06-12"
}

## Qu'est-ce qu'un fichier BAK ?

Un fichier « .bak », dans le contexte de Microsoft SQL Server, est un format de fichier de sauvegarde utilisé pour stocker des copies d'une base de données SQL Server. Ces fichiers contiennent un instantané de la base de données à un moment précis, y compris son schéma, ses données et d'autres informations associées. Ils sont générés à l'aide de la fonctionnalité de sauvegarde et de restauration intégrée de SQL Server et répondent à plusieurs objectifs cruciaux :

1. **Récupération de données :** les fichiers .bak offrent un moyen de récupérer une base de données en cas de perte de données, de corruption ou d'autres problèmes. En restaurant une base de données à partir d'un fichier .bak, vous pouvez la rétablir à un état antérieur, minimisant ainsi les temps d'arrêt et la perte de données.

2. **Migration et clonage :** Les fichiers de sauvegarde sont souvent utilisés pour migrer des bases de données entre des serveurs ou créer des copies de bases de données à des fins de test, de développement ou de création de rapports. Ils offrent un moyen cohérent et efficace de déplacer des bases de données entre environnements.

3. **Récupération ponctuelle :** SQL Server vous permet d'effectuer une récupération ponctuelle à l'aide de fichiers .bak. Cela signifie que vous pouvez restaurer une base de données à un moment précis, ce qui peut être crucial pour la conformité réglementaire ou l'audit des données.

4. **Reprise après sinistre :** les fichiers .bak constituent un élément essentiel de la planification de la reprise après sinistre. Ils garantissent que vos données sont en sécurité et peuvent être restaurées rapidement en cas de panne matérielle, de catastrophe naturelle ou d'autres événements catastrophiques.

## Créer un fichier .BAK dans SQL Server

Pour créer un fichier .bak dans SQL Server, vous utilisez généralement des commandes SQL Server Management Studio (SSMS) ou Transact-SQL (T-SQL) telles que BACKUP DATABASE ou BACKUP LOG. Voici un exemple simplifié de la façon dont vous pouvez créer une sauvegarde de base de données à l'aide de T-SQL :

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Restaurer un fichier .BAK dans SQL Server

Pour restaurer une base de données à partir d'un fichier .bak, vous pouvez utiliser la commande RESTORE DATABASE :

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Comment ouvrir le fichier BAK dans SQL Server ?

Pour ouvrir et accéder aux données stockées dans un fichier « .bak », vous devez généralement le restaurer sur une instance de Microsoft SQL Server. Voici les étapes générales pour ouvrir un fichier « .bak » à l'aide de SQL Server Management Studio (SSMS) :

1. **Lancez SQL Server Management Studio** : ouvrez SSMS sur votre ordinateur. Vous pouvez généralement le trouver dans votre menu Démarrer ou en recherchant « SQL Server Management Studio ».

2. **Connectez-vous à une instance SQL Server** : dans SSMS, connectez-vous à l'instance SQL Server sur laquelle vous souhaitez restaurer la base de données. Vous aurez besoin des autorisations nécessaires pour effectuer cette opération.

3. **Restaurer la base de données** :

un. Dans le volet Explorateur d'objets sur le côté gauche, développez l'instance SQL Server.

b. Développez le nœud "Bases de données".

c. Faites un clic droit sur "Bases de données" et sélectionnez "Restaurer la base de données".

4. **Spécifiez la source et la destination** :

un. Dans la page "Général" de la boîte de dialogue "Restaurer la base de données", saisissez un nom pour la nouvelle base de données dans le champ "Vers la base de données". Ce sera le nom de la base de données restaurée.

b. Dans la section "Source", choisissez "Périphérique" comme type de support de sauvegarde.

c. Cliquez sur le bouton "..." à côté du champ "Périphérique" pour rechercher le fichier ".bak" que vous souhaitez restaurer.

d. Sélectionnez le fichier ".bak" que vous souhaitez ouvrir et cliquez sur "OK".

5. **Options de restauration** : vérifiez et configurez les options de restauration selon vos besoins. Vous pouvez spécifier s'il faut écraser une base de données existante, définir des options de récupération, etc. Assurez-vous de définir ces options en fonction de vos besoins.

6. **Lancer la restauration** : Une fois que vous avez configuré les options de restauration, cliquez sur le bouton "OK" dans la boîte de dialogue "Restaurer la base de données". SQL Server commencera le processus de restauration.

7. **Accéder à la base de données restaurée** : après une restauration réussie, vous pouvez accéder à la base de données restaurée dans SQL Server Management Studio comme n'importe quelle autre base de données. Vous pouvez exécuter des requêtes, afficher des tables et travailler avec les données de la base de données.

## Autres fichiers BAK

Voici d'autres types de fichiers qui utilisent l'extension de fichier **.bak**.

**Base de données**
- [BAK - Fichier de sauvegarde de la base de données](/fr/database/bak/)
-[BAK - Swiftpage Act! Sauvegarde de la base de données](/fr/database/bak-act/)

**Jeu**
- [BAK - Terraria World ou sauvegarde du joueur](/fr/game/bak-terraria/)

**Divers**
- [BAK - Fichier de sauvegarde](/fr/misc/bak-backup/)
- [BAK - Sauvegarde des signets Chromium](/fr/misc/bak-chromium/)
- [BAK - Sauvegarde du score de Finale 2012](/fr/misc/bak-finale/)
- [BAK - Sauvegarde MobileTrans](/fr/misc/bak-mobiletrans/)
- [BAK - Sauvegarde du projet vidéo VEGAS](/fr/misc/bak-vegas/)

**Paramètres**
- [BAK - Sauvegarde du lanceur Holo](/fr/settings/bak-holo/)

## Les références
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
