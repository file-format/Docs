{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier HTACCESS - Format de fichier Apache HTACCESS",
  "description" :"Votre guide de format de fichier pour savoir ce qu'est un fichier HTACCESS",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier HTACCESS ?

Un fichier HTACCESS est un fichier de configuration Apache qui fournit un mécanisme pour autoriser les modifications de configuration pour différents dossiers/répertoires d'un site Web. Il comprend des directives de configuration applicables au répertoire et aux sous-répertoires.

Un fichier HTACCESS effectue un certain nombre de vérifications telles que la définition de la page d'index d'un site Web, la liste de la page d'erreur 404 (Page non trouvée), l'exécution des redirections de page 301 ou 302, le blocage de l'accès à partir d'une adresse IP spécifique ou d'autres sites Web. L'utilisation de fichiers .htaccess ralentit donc les performances globales de votre serveur Apache HTTP.

## Format de fichier HTTPACCESS

Les fichiers HTACCESS sont stockés sur le disque au format de fichier texte brut. Cela signifie que vous pouvez ouvrir et modifier ces fichiers dans n'importe quel éditeur de texte. Il n'y a pas de nom avant le "." dans un fichier .htaccess, indiquant qu'il s'agit d'un fichier caché dans le dossier.

## Utilisations courantes d'un fichier HTTPACCESS

Cinq utilisations courantes d'un fichier HTACCESS sont les suivantes.

### Mod_Rewrite

Un fichier HTACCESS peut être utilisé pour désigner et modifier la manière dont les URL et les pages Web d'un site Web sont affichées pour les utilisateurs.

### Authentification

L'authentification peut être réalisée avec .htaccess en créant un fichier passowrd appelé .htpasswd. Cela permet aux visiteurs du site de fournir un mot de passe s'ils souhaitent visiter une certaine section de la page Web.

### Pages d'erreur personnalisées

Vous pouvez créer des pages d'erreur personnalisées telles que 400 Bad Request, 401 Authorization Required, 403 Forbidden Page, 404 File not Found et 500 Internal Error with .htaccess file. Cependant, cela ralentira les performances du serveur car toutes ces vérifications seront exécutées lors de l'accès aux pages.

###Types MIME

Les fichiers Apache HTACCESS peuvent être modifiés pour inclure les types MIME (Multipurpose Internet Mail Extensions). Cela permet à votre serveur de prendre en charge la livraison de fichiers d'application qui n'étaient pas pris en charge par le site.

### SSI

Server Side Include (SSI) permet de gagner beaucoup de temps sur un site Web. SSI peut être activé en insérant le code suivant dans votre fichier .htaccess.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Exemple de fichier Apache HTACCESS

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Références

* [Tutoriel Apache HTTP Server : fichiers .htaccess](https://httpd.apache.org/docs/current/howto/htaccess.html)

