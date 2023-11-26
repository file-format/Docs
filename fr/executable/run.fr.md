{
  "date" : "2023-01-31",
  "keywords" :["fichier d'exécution", "qu'est-ce qu'un fichier d'exécution", "fichier", "comment ouvrir le fichier d'exécution", "extension de fichier d'exécution", "extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Découvrez le format de fichier RUN et les API permettant de créer et d'ouvrir des fichiers RUN.",
  "title" :"Format de fichier RUN - Fichier exécutable Linux",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## Qu'est-ce qu'un fichier RUN ?

Le format de fichier .run est couramment utilisé pour distribuer des programmes d'installation de logiciels ou d'applications dans l'environnement Linux. Pour installer le logiciel, vous devrez rendre le fichier exécutable, ce qui peut être fait à l'aide de la commande suivante :

```bash
chmod +x file_name.run 
```

Ensuite, vous pouvez exécuter le fichier à l'aide de la commande suivante :

```bash
./file_name.run 
```

Le processus d'installation peut varier en fonction du fichier et du programme spécifiques que vous essayez d'installer.

Le format de fichier .run est un type de script shell utilisé pour distribuer des programmes d'installation de logiciels ou d'applications dans l'environnement Linux. Il s'agit d'un package autonome qui comprend tout le nécessaire pour installer le logiciel, notamment les fichiers binaires, les bibliothèques et les fichiers de configuration.

Il est important de noter que les fichiers .run peuvent également contenir du code malveillant, c'est donc toujours une bonne idée de vérifier la source du fichier et de l'analyser à la recherche de virus avant de l'exécuter.

De plus, certains fichiers .run peuvent nécessiter des privilèges root pour être exécutés et installés, vous devrez donc peut-être utiliser la commande « sudo » pour exécuter le fichier avec des autorisations élevées :

```bash
sudo ./filename.run
```

## Comment ouvrir le fichier RUN?

Pour ouvrir un fichier .run, vous devez le rendre exécutable, ce qui peut être fait avec la commande "chmod" :

```bash
chmod +x filename.run 
```

Une fois le fichier rendu exécutable, vous pouvez l'exécuter en tapant :

```bash
./filename.run
```

Exécuter un fichier .run n’est pas la même chose que l’ouvrir dans un éditeur de texte. L’exécution d’un fichier .run exécutera ses instructions, qui peuvent aller de l’installation d’un programme à l’exécution d’un script. Pour afficher le contenu d'un fichier .run, vous devez l'ouvrir dans un éditeur de texte, tel que nano ou vim :

```
nano filename.run
```
ou
```
vim filename.run
```

## Les références
* [Comment exécuter des fichiers .bin et .run dans Ubuntu](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


