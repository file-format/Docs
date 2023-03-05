{
  "date" : "2023-01-09",
  "keywords" :[ "ABCDDB", "qu'est-ce qu'un fichier ABCDDB", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier ABCDDB et les API qui peuvent créer et ouvrir des fichiers ABCDDB.",
  "title" :"Format de fichier ABCDDB - Fichier de base de données de la liste de contacts du carnet d'adresses Apple",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Qu'est-ce qu'un fichier ABCDDB ?

Le fichier avec l'extension **.ABCDDB** signifie Apple Address Book Contact List Database. Il appartient à l'application **Carnet d'adresses** également connue sous le nom de **Contacts**. Il s'agit d'une application intégrée et incluse avec les systèmes d'exploitation iOS et macOS. L'application Contacts permet aux utilisateurs d'enregistrer et d'organiser les informations relatives à leurs contacts, y compris les individus, les entreprises et les organisations. Cette application permet aux utilisateurs de garder une trace de détails tels que les noms, adresses, numéros de téléphone et adresses e-mail, ainsi que de classer leurs contacts en groupes.

## Relation avec SQLite et chemin typique

Le carnet d'adresses d'Apple (également connu sous le nom de contacts) stocke les informations de contact sous forme de vCards dans le dossier de métadonnées. **Le fichier _ABCDDB_ est en fait _SQLite 3 datafile_**.

SQLite est un système de gestion de base de données populaire conçu pour être léger et autonome. Il est utilisé dans de nombreux types de logiciels et d'appareils. SQLite est un type de SGBDR, ce qui signifie qu'il stocke les données dans des tables qui sont liées les unes aux autres via des clés. Il peut gérer une gamme de types de données, y compris des nombres entiers, des nombres à virgule flottante, des chaînes et des données binaires. De plus, SQLite prend en charge les transactions, qui permettent aux utilisateurs d'effectuer plusieurs opérations de base de données ensemble comme une seule unité de travail.

Le fichier avec l'extension ABCDDB est généralement stocké ici

`~/Bibliothèque/Application Support/AddressBook/AddressBook-v22.abcddb`

## Réparer la base de données de contacts corrompue

Veuillez d'abord effectuer la sauvegarde avant d'essayer de le faire. Veuillez alors naviguer jusqu'à

`~/Bibliothèque/Application Support/Carnet d'adresses`

Dans ce répertoire, vous trouverez trois fichiers dont celui avec l'extension .abcddb

- `carnet d'adresses-v22.abcddb`
- `carnet d'adresses-v22.abcddb-wal`
- `carnet d'adresses-v22.abcddb-shm`

Supprimez tous ces fichiers et rouvrez les contacts, ils recommenceront à fonctionner.

## Restaurer la base de données du carnet d'adresses à partir de la sauvegarde

Supposons que les contacts de votre base de données AddressBook soient stockés dans `addressbook-v22.abcddb`

- Sauvegardez d'abord les données de votre carnet d'adresses et quittez toutes les applications.
- Déplacez votre fichier de base de données dans le sous-répertoire `~/Library/Application Support/AddressBook`
- Lancez **Carnet d'adresses.app**.

## Exporter les données du fichier ABCDDB vers Microsoft Access

Étant donné que le fichier est un fichier de données SQLite 3, vous pouvez exporter les données du fichier abcddb dans Microsoft Access à l'aide du connecteur ODBC.

Le connecteur ODBC SQLite est une bibliothèque logicielle et un pilote qui permettent aux applications prenant en charge l'interface ODBC de se connecter à une base de données SQLite. Il comprend une bibliothèque qui définit l'interface ODBC et un pilote qui traduit cette interface en appels à l'API SQLite. Pour utiliser le connecteur ODBC SQLite, vous devez d'abord l'installer, puis configurer une source de données ODBC sur votre ordinateur. Une fois ces étapes terminées, toute application équipée du support ODBC pourra se connecter à la source de données et récupérer les données de la base de données SQLite.

## Références
* [Réparer la base de données de contacts corrompue](https://discussions.apple.com/docs/DOC-10581)
* [Base de données de contacts pour Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
* [Comment puis-je ouvrir ou exporter un fichier abcddb dans Windows 7 Excel ?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-dans-windows-7-excel)
