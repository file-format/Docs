{
"date": "2023-03-22",
  "keywords": [
"fichier cnf",
"qu'est-ce qu'un fichier cnf",
"comment ouvrir le fichier cnf",
"déposer",
"extension de fichier CNF",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier CNF - Fichier de configuration MySQL",
  "description":"Découvrez le format CNF et les API permettant de créer et d'ouvrir des fichiers CNF.",
"linktitle": "CNF",
  "menu": {
    "docs": {
      "identifier": "settings-cnf",
"parent" : "settings"
}
},
"lastmod": "2023-03-22"
}

## Qu'est-ce qu'un fichier CNF ?

Un fichier CNF (également appelé fichier de configuration) dans MySQL est utilisé pour stocker les paramètres de configuration du serveur MySQL. L'emplacement du fichier CNF peut varier en fonction du système d'exploitation et de la méthode d'installation utilisée. La configuration comprend généralement divers paramètres tels que le codage des caractères par défaut, les délais d'attente, les configurations de cache et de tampon, qui peuvent être ajustés pour optimiser les performances de la base de données en fonction de l'utilisation.

## Format de fichier CNF – Plus d’informations

Vous pouvez créer CNF en suivant les étapes suivantes dans MySQL :

1. Ouvrez un éditeur de texte, par exemple le Bloc-notes, et créez un nouveau fichier.
2. Ajoutez les options de configuration souhaitées au fichier, une par ligne. Voici un exemple:

```
[mysqld]
datadir=/var/lib/mysql
socket=/var/lib/mysql/mysql.sock
user=mysql
symbolic-links=0

[client]
user=root
password=password123
```

3. Enregistrez le fichier avec une extension .cnf, par exemple « mysql.cnf ».
4. Déplacez le fichier vers le répertoire approprié. Par exemple, sur les systèmes Linux, le répertoire peut être /etc/mysql/conf.d/ ou /etc/mysql/.
5. Redémarrez le serveur MySQL pour que les nouveaux paramètres de configuration prennent effet.

Assurez-vous de tester toutes les modifications apportées au fichier CNF dans un environnement hors production avant de les implémenter dans un environnement de production.

## Comment ouvrir le fichier CNF?

Le fichier CNF est un fichier texte et peut être ouvert facilement à l’aide de n’importe quel éditeur de texte comme le Bloc-notes. Vous pouvez également l'ouvrir en cliquant avec le bouton droit et en sélectionnant "Ouvrir avec" dans le menu. Une fois le fichier ouvert, vous pouvez modifier les paramètres de configuration selon vos besoins. CNF contient divers paramètres liés au serveur MySQL, par exemple le numéro de port, les options de journalisation et la taille des tampons. Une fois que vous avez modifié les paramètres, enregistrez les modifications et fermez l'éditeur de texte. Enfin, redémarrez le serveur MySQL pour que les modifications prennent effet.

Notez qu'il est important d'être prudent lors de la modification du fichier de configuration MySQL, car des paramètres incorrects peuvent entraîner un comportement imprévisible du serveur, voire ne pas démarrer du tout. Il est recommandé de faire une sauvegarde du fichier d'origine avant d'apporter des modifications, afin de pouvoir le restaurer si nécessaire.

## Les références
* [MySQL](https://en.wikipedia.org/wiki/MySQL)

