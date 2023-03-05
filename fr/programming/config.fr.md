{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - Fichier de configuration",
  "description":"En savoir plus sur le format de fichier CONFIG avec l'exemple CONFIG et les API qui peuvent créer et ouvrir des fichiers CONFIG.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Qu'est-ce qu'un fichier CONFIG ?
Un fichier CONFIG est appelé fichier de configuration ; utilisé pour configurer les paramètres et les réglages primaires de plusieurs logiciels informatiques. Certains logiciels ne lisent leurs **fichiers de configuration** qu'au démarrage. D'autres vérifient périodiquement les fichiers de configuration pour les changements.

## Format de fichier de configuration
Le **format de fichier CONFIG** est utilisé pour les processus serveur, les applications logicielles et les paramètres du système d'exploitation. Un programmeur peut écrire du code pour demander à un logiciel de lire les fichiers de configuration encore et encore après un certain temps et d'appliquer les modifications au processus en cours. Il n'y a pas de normes définitives ou de conventions fortes pour la syntaxe des fichiers CONFIG. Par exemple, le fichier Web.config de Microsoft appartient au format de fichier CONFIG, qui consiste en un jeu de balises basé sur [XML](https://docs.fileformat.com/web/xml/) ; peut être modifié avec Microsoft Visual Studio ou tout autre éditeur de texte.

## Exemples de fichiers de configuration :
Étant donné que les fichiers de configuration ne sont pas créés en suivant des règles, normes ou conventions, ces fichiers peuvent avoir été écrits en utilisant différents formats. Un fichier .config peut être basé sur XML, [JSON](https://docs.fileformat.com/web/json/) ou tout autre format. Voici des exemples de fichiers de configuration pour des systèmes d'exploitation et des logiciels bien connus :

### Fichiers de configuration sous Linux
Chaque programme Linux est un fichier exécutable contenant la liste des **opcodes** que le processeur exécute pour accomplir des opérations typiques. Les opérations de presque tous les programmes peuvent être personnalisées selon vos besoins en modifiant ses fichiers de configuration. Plusieurs fichiers de configuration du système Linux se trouvent dans le répertoire /etc. Les fichiers de configuration peuvent être classés dans les catégories suivantes :
|Catégorie|Exemple| Commentaires|
---|---|---|
|Fichiers d'accès|/etc/host.conf|Indique au serveur de domaine du réseau comment rechercher les noms d'hôtes.|
|Démarrage et connexion/déconnexion|/etc/rc.d/rc.local|Non officiel. Peut être appelé depuis rc, rc.sysinit ou /etc/inittab.|
|Système de fichiers|/etc/mtools.conf|Configuration de toutes les opérations (mkdir, copier, formater, etc.) sur un système de fichiers de type DOS.|
|Administration système|/etc/shells|Contient la liste des "shells" possibles disponibles pour le système.|
|Réseau|/etc/gated.conf|Configuration pour gated. Utilisé uniquement par le démon gated.|
|Commandes système|/etc/logrotate.conf|Configuration pour le Dynamic Linker.|
|Daemons|/etc/httpd.conf|Le fichier de configuration d'Apache, le serveur Web. Ce fichier n'est généralement pas dans /etc.|
|Programmes utilisateur| /etc/lynx.cfg| Paramètres proxy|
### Exemple de fichier AWS CONFIG
Les paramètres de configuration et les informations d'identification fréquemment utilisés peuvent être enregistrés dans des fichiers CONFIG gérés par l'AWS CLI. Le fichier CONFIG doit être un fichier en texte brut qui utilise le format suivant :
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### Exemple de fichier de configuration SSH
Le fichier de configuration côté client OpenSSH est nommé CONFIG et il est stocké dans le répertoire .ssh. Le fichier SSH CONFIG se compose de la structure suivante :
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Exemple de fichier de configuration Python
Un fichier Python CONFIG pourrait ressembler à ceci :

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## Références

* [Comprendre les fichiers de configuration Linux](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Paramètres de fichier de configuration et d'informations d'identification](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Fichiers de configuration en Python](https://martin-thoma.com/configuration-files-in-python/)

