{
  "date" : "2019-10-11",
  "keywords" :[ "asp", "fichier asp", "format de fichier asp", "type de fichier asp", "fichier", "type", "qu'est-ce qu'un fichier asp" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - Format de fichier des pages du serveur actif",
  "description" :"Découvrez ce qu'est un fichier ASP et les API qui peuvent les créer et les ouvrir.",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier ASP ?

ASP signifie Active Server Pages qui est un cadre de développement pour la création de pages Web. Il permet à un code informatique d'être exécuté par un serveur interne pour servir les requêtes Web. Lorsqu'une requête est générée pour un fichier ASP par un navigateur Web, le serveur lit le fichier et exécute tout code/script qu'il contient pour générer le résultat **[HTML](/fr/web/html/)** qui est renvoyé au navigateur pour l'affichage.

Contrairement aux pages HTML, qui sont des pages statiques servies par le serveur, les fichiers ASP génèrent des contenus dynamiques lors de l'exécution qui peuvent impliquer des demandes de données à partir d'une base de données. Les pages ASP utilisent généralement l'extension .asp plutôt que .html. Étant donné que le code/script à l'intérieur d'un fichier ASP est exécuté côté serveur, le navigateur demandeur ne peut pas voir le code utilisé pour créer la page servie. Tous les navigateurs modernes sont capables d'afficher les pages générées en conséquence. Étant construites sur la technologie Microsoft, les pages créées avec ASP sont hébergées sur des serveurs Microsoft Internet Information Services (IIS).

## Bref historique du format de fichier ASP
ASP n'a subi que quelques révisions avant d'être remplacé par ASP.NET, un moyen plus moderne et plus efficace de développer et de gérer des pages côté serveur. La prise en charge d'ASP est incluse par défaut avec Internet Information Services (IIS). ASP a été publié en trois versions différentes avec des améliorations dans chacune d'elles.

* ASP 1.0 a été publié en décembre 1996 dans le cadre d'IIS 3.0
* ASP 2.0 a été publié en septembre 1997 dans le cadre d'IIS 4.0
* ASP 3.0 a été publié en novembre 2000 dans le cadre d'IIS 5.0

## Objets fonctionnels ASP

Les fichiers ASP utilisent des objets côté serveur pour traiter les demandes des utilisateurs et générer des pages de sortie à servir aux utilisateurs. Chaque objet possède un ensemble de collections, de propriétés et de méthodes pour traiter les requêtes et les réponses. Ces objets comprennent :

### Objet de requête

Lorsqu'un navigateur demande une page à un serveur, cela s'appelle une requête. L'objet Request est utilisé pour obtenir des informations d'un visiteur.

### Objet de réponse

L'objet ASP Response est utilisé pour envoyer la sortie à l'utilisateur à partir du serveur.

### Objet serveur

L'objet ASP Server est utilisé pour accéder aux propriétés et aux méthodes sur le serveur. Il permet les connexions aux bases de données (ADO), au système de fichiers et à l'utilisation des composants installés sur le serveur.

### Objet de session

Un objet de session est comme un lien entre le navigateur de l'utilisateur demandant une page au serveur et le serveur lui-même. Ceci est réalisé par un cookie créé par ASP et envoyé à l'ordinateur de l'utilisateur. L'objet Session stocke des informations sur ou modifie les paramètres d'une session utilisateur. Les informations stockées dans un objet Session sont partagées sur toutes les pages d'une application. Les informations communes stockées dans les variables de session sont le nom, l'identifiant et les préférences. Le serveur crée un nouvel objet Session pour chaque nouvel utilisateur et détruit l'objet Session lorsque la session expire.

### Objet d'application

L'objet Application contient des informations qui seront utilisées par de nombreuses pages de l'application (comme les informations de connexion à la base de données). Les informations sont accessibles depuis n'importe quelle page. Les informations peuvent également être modifiées en un seul endroit et les modifications seront automatiquement répercutées sur toutes les pages. L'objet Application est utilisé pour stocker et accéder aux variables de n'importe quelle page, tout comme l'objet Session.

### Objet ASPError

L'objet ASPError a été implémenté dans ASP 3.0 et est disponible dans IIS5 et versions ultérieures. L'objet ASPError est utilisé pour afficher des informations détaillées sur toute erreur qui se produit dans les scripts d'une page ASP.

**Remarque :** L'objet ASPError est créé lorsque Server.GetLastError est appelé, de sorte que les informations sur l'erreur ne sont accessibles qu'à l'aide de la méthode Server.GetLastError.

## Références

* [ASP - Par W3C](https://www.w3schools.com/asp/default.asp)
* [Création de pages ASP simples](https://docs.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))

