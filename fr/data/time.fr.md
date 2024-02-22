{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Fichier TIME - Qu'est-ce qu'un fichier .time ? Heure à laquelle le fichier a été créé sous Linux",
  "description" : "En savoir plus sur le fichier TIME et connaître l'heure à laquelle le fichier a été créé sous Linux",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-fr",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Qu'est-ce qu'un fichier TIME ?

Le format de fichier TIME était utilisé par un système Web appelé LIGHT, qui aidait les utilisateurs à enregistrer, organiser et partager leur vie. Essentiellement, il stockait une collection de publications et représentait un dossier sur la page de vie de l'utilisateur au sein du système.

## Comment savoir quand un fichier a été créé sous Linux

Sous Linux, vous pouvez utiliser la commande `stat` pour savoir quand un fichier a été créé. Voici comment procéder :

Ouvrez un terminal et tapez la commande suivante :

```
stat <file_path>
```

Remplacer `<file_path> ` avec le chemin d'accès au fichier qui vous intéresse. Par exemple :

```
stat /path/to/your/file.txt
```

Cette commande affichera diverses informations sur le fichier, y compris son heure de création. Recherchez la ligne qui commence par « Naissance » ou « Fichier : ». L'heure de « naissance » indique quand le fichier a été créé sur le système de fichiers.

Voici un exemple de ce à quoi pourrait ressembler le résultat :

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

Dans cet exemple, l'heure « Naissance » indique la date à laquelle le fichier a été créé.

