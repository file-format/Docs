{
  "date" : "2021-06-21",
  "keywords" :[ "UDL", "extension", "fichier udl", "format de fichier udl", "Type de fichier de base de données", "Format de fichier de base de données", "qu'est-ce qu'un fichier udl" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier UDL et les API qui peuvent créer et ouvrir des fichiers UDL.",
  "title" :"UDL - Fichier de liaison de données universelle Microsoft",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## Qu'est-ce qu'un fichier UDL ?
Le fichier avec l'extension .udl est appelé fichier Microsoft Universal Data Link ; spécification des attributs de connexion ; utilisé par les applications Windows pour établir une connexion avec la base de données. Le fichier UDL contient la chaîne de connexion pour une source de données OLE DB ; avec nom d'utilisateur et mot de passe et propriétés de chaîne de connexion essentielles. Pour éviter de spécifier directement les propriétés à la main dans une chaîne de connexion, une boîte de dialogue Propriétés des liaisons de données peut être utilisée pour enregistrer les informations de connexion dans un fichier .udl comme alternative.

## Format de fichier UDL
Fondamentalement, un fichier UDL (Universal Data Link) est un simple fichier texte composé d'une chaîne de connexion à une base de données avec des attributs ou des propriétés particuliers. Une fois le fichier UDL créé, il peut être testé à l'aide de SQL Server Management Studio pour vérifier la connectivité.

### Propriétés de la chaîne de connexion
Les propriétés suivantes peuvent être définies dans un UDL pour garantir la bonne connectivité :

- **Nom du serveur** : emplacement du serveur sur lequel se trouve la base de données à laquelle vous souhaitez accéder.
- **Options d'authentification**
- **Authentification Windows** : authentification auprès de SQL Server à l'aide des informations d'identification du compte Windows de l'utilisateur actuellement connecté.
- **Authentification SQL Server** : Authentification à l'aide d'un identifiant de connexion et d'un mot de passe.
- **Active Directory - Integrated** : authentification intégrée avec une identité Azure Active Directory ; peut également être utilisé pour l'authentification Windows auprès de SQL Server.
- **Active Directory - Mot de passe** : authentification par ID utilisateur et mot de passe avec une identité Azure Active Directory.
- **Active Directory - Universal with MFA support** : Authentification interactive avec une identité Azure Active Directory.
- **Active Directory - Principal de service** : authentification avec un principal de service Azure Active Directory.
- **Server SPN** : si vous utilisez une connexion approuvée, vous pouvez spécifier un nom principal de service (SPN) pour le serveur.
- **Nom d'utilisateur** : saisissez l'ID utilisateur à utiliser pour l'authentification lorsque vous vous connectez à la source de données.
- **Mot de passe** : saisissez le mot de passe à utiliser pour l'authentification lorsque vous vous connectez à la source de données.
- **Mot de passe vide** : lorsque cette case est cochée, permet au fournisseur spécifié d'utiliser un mot de passe vide dans la chaîne de connexion.
- **Autoriser l'enregistrement du mot de passe** : autorise l'enregistrement du mot de passe avec la chaîne de connexion.
- **Utiliser un cryptage fort pour les données** : les données transmises via la connexion seront cryptées.
- **Certificat du serveur de confiance** : le certificat du serveur sera validé.
- **Database** : nom de la base de données à laquelle vous souhaitez accéder.
- **Joindre un fichier de base de données comme nom de base de données** : spécifie le nom du fichier principal pour une base de données pouvant être jointe.

## Références ##

* [Composants d'accès aux données Microsoft](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [Configuration de la liaison de données universelle (UDL)](https://docs.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

