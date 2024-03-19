{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Découvrez le format de fichier NMONEY et les API permettant de créer et d'ouvrir des fichiers NMONEY.",
  "title" :"Fichier NMONEY - Format de fichier de compte Denaro",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## Qu'est-ce qu'un fichier NMONEY ?

Un fichier NMONEY est un fichier de base de données de stockage de données financières qui contient des antécédents de transactions financières. Il a été développé par Nickvision et a été utilisé dans le logiciel Nickvision Denaro, un logiciel financier personnel. Les données stockées dans un fichier NOMONEY incluent les informations sur les transactions de crédit et de débit sur un compte.

Les fichiers NOMONEY peuvent être ouverts avec l'application [Github](https://github.com/NickvisionApps/Denaro).

## À propos de Denaro Software

Denaro a été initialement développé par [Nickvision](https://nickvision.org/) en tant que produit qui a ensuite été converti en une application logicielle open source hébergée sur [Github](https://github.com/NickvisionApps/Denaro) . Depuis lors, l'application a été modifiée et mise à jour uniquement sur Github. L'application est développée en C# dans l'interface utilisateur Windows avec le SDK Windows App (WinUI 3 pour le moment).

### Fonctionnalités offertes par Denaro

* Gérez plusieurs comptes simultanément avec son interface à onglets la plus populaire et la plus familière
* Filtrer les transactions par type, groupe ou date
* Répétez les transactions telles que les factures qui surviennent chaque mois
* Transférer de l'argent d'un compte à un autre
* Exportez les données d'un compte sous forme de fichier CSV et importez un fichier CSV, OFX ou QIF pour ajouter des transactions à un compte

## Format de fichier Denaro - Plus d'informations

Les fichiers Denaro sont enregistrés sur disque au format de fichier binaire. Les données financières sont stockées sous forme de fichier de base de données au format de fichier **.SQLITE3**. SQLITE est un fichier de base de données SQL léger créé avec le logiciel SQLite. Il fournit un moteur de base de données autonome capable de fournir une base de données complète et hautement fiable. Les fichiers de base de données SQLite peuvent être utilisés pour partager des contenus riches entre systèmes en échangeant simplement ces fichiers sur le réseau. Des liaisons SQLite existent pour les langages de programmation tels que C, [C#](/fr/programming/cs/), [C++](/fr/programming/cpp/), [Java](/fr/programming/java/), [PHP](/fr/programming/php/), et bien d’autres.

## Les références

* [Nickvision](https://nickvision.org/)
* [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

