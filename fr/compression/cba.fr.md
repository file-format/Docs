{
"date": "2023-05-24",
  "keywords": [
"fichier cba",
"qu'est-ce qu'un fichier cba",
"comment créer un fichier CBA",
"que contient le fichier CBA",
"quel est le format du fichier cba",
"déposer",
"extension de fichier CBA",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier CBA - Archives de bandes dessinées",
  "description":"Découvrez le format CBA et les API permettant de créer et d'ouvrir des fichiers CBA.",
"linktitle": "CBA",
  "menu": {
    "docs": {
      "identifier": "compression-cba",
"parent": "compression"
}
},
"derniermod": "2023-05-24"
}

## Qu'est-ce qu'un fichier CBA ?

Un fichier Comic Book Archive (CBA), également connu sous le nom de fichier Comic Book Archive ou Comic Book Reader, est un format populaire utilisé pour stocker et distribuer des bandes dessinées numériques. Il contient généralement une collection de pages de bandes dessinées individuelles ou d'images regroupées dans un seul fichier pour une organisation et une lecture faciles.

L'un des formats courants pour créer des fichiers d'archives de bandes dessinées est le format TAR (Tape Archive). TAR est un format d'archivage de fichiers utilisé dans les environnements Unix et Linux. Il combine plusieurs fichiers en un seul fichier souvent utilisé à des fins de sauvegarde.

## Comment créer un fichier CBA ?

Pour créer un fichier Comic Book Archive à l'aide de l'outil d'archivage TAR, vous devez généralement suivre ces étapes :

1. Rassemblez toutes les pages ou images de bandes dessinées que vous souhaitez inclure dans les archives.
2. Ouvrez une invite de commande ou une fenêtre de terminal.
3. Accédez au répertoire où se trouvent les pages/images de bandes dessinées.
4. Utilisez la commande TAR avec les options appropriées pour créer l'archive. Par exemple, la commande pourrait ressembler à ceci :

```
tar -cf comicbook.cbt page1.jpg page2.jpg page3.jpg
```

Dans cet exemple, l'option -c indique à TAR de créer une nouvelle archive et l'option -f spécifie le nom du fichier de sortie (comicbook.cbt dans ce cas). Après avoir spécifié les options, vous fournissez les noms des fichiers que vous souhaitez inclure dans l'archive (page1.jpg, page2.jpg, page3.jpg).

5. Après avoir exécuté la commande, l'outil TAR créera le fichier Comic Book Archive (comicbook.cbt dans cet exemple) dans le répertoire actuel.

Une fois que vous disposez du fichier Comic Book Archive, vous pouvez utiliser divers logiciels ou applications de lecture de bandes dessinées pour ouvrir et lire une bande dessinée sur votre ordinateur ou appareil. Ces applications fournissent généralement des fonctionnalités telles que la navigation dans les pages, le zoom et la création de favoris pour améliorer l'expérience de lecture.

## Que contient le fichier CBA ?

Un fichier Comic Book Archive (CBA) créé à l'aide de l'outil d'archivage TAR contient une collection de pages ou d'images de bandes dessinées individuelles regroupées dans un seul fichier. Le contenu spécifique des archives dépend de la bande dessinée emballée.

En règle générale, un fichier d'archive de bande dessinée comprend les éléments suivants :

- **Pages de bandes dessinées :** Le contenu principal des archives est constitué des pages de bandes dessinées elles-mêmes. Ces pages sont généralement enregistrées sous forme de fichiers image individuels, tels que JPEG ou PNG, représentant chaque page de la bande dessinée. Les pages sont disposées dans un ordre spécifique pour maintenir le flux narratif de la bande dessinée.
- **Métadonnées :** Certains formats d'archives de bandes dessinées peuvent inclure des métadonnées sur la bande dessinée, telles que le titre, l'auteur, l'éditeur, la date de publication et la description. Ces informations permettent d'identifier et de catégoriser la bande dessinée.
- **Fichiers supplémentaires :** En plus des pages de bande dessinée et des métadonnées, l'archive peut contenir d'autres fichiers supplémentaires liés à la bande dessinée. Ces fichiers peuvent inclure des pochettes, des images promotionnelles, du contenu bonus ou des fichiers texte fournissant des informations ou des commentaires supplémentaires.

## Quel est le format du fichier CBA ?

Le format de fichier Comic Book Archive (CBA) créé à l'aide de l'outil d'archivage TAR est généralement au format TAR. TAR, abréviation de Tape Archive, est un format d'archivage de fichiers couramment utilisé dans les systèmes Unix et Linux. Il n'est pas spécifique à la bande dessinée mais constitue un format d'archivage à usage général.

Le format TAR est un moyen simple de regrouper plusieurs fichiers dans un seul fichier d'archive. Il ne fournit pas de compression par lui-même, de sorte que le fichier TAR résultant peut être volumineux par rapport à d'autres formats compressés comme ZIP ou RAR. Cependant, les fichiers TAR peuvent être compressés à l'aide d'outils supplémentaires ou combinés avec des algorithmes de compression comme gzip ou bzip2 pour réduire la taille du fichier.

Le format TAR préserve la structure des fichiers, les autorisations des fichiers et les horodatages des fichiers inclus. Il stocke les fichiers de manière séquentielle dans les archives, permettant une extraction facile de fichiers individuels ou d'archives entières.

## Les références
* [Archives de bandes dessinées](https://en.wikipedia.org/wiki/Comic_book_archive)

