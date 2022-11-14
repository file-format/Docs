{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier ZIM - Fichier d'archive OpenZIM",
  "description":"En savoir plus sur le format de fichier ZIM et les API qui peuvent créer et ouvrir des fichiers ZIM.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Qu'est-ce qu'un fichier ZIM ? ##

Les fichiers avec l'extension .zim sont des archives créées pour stocker le contenu Wiki hors ligne. Il est considéré comme le format de fichier ouvert le plus approprié pour stocker Wikipedia sur une clé USB. Il stocke le contenu du site dans un format compact. Son nom vient de "Zeno IMproved", qui était l'ancien format de fichier Zeno. ZIM est maintenu par le projet [openZIM ](https://openzim.org/) qui est sponsorisé par Wikimedia CH et soutenu par la Wikimedia Foundation. Les fichiers ZIM peuvent être ouverts par des applications telles que Kiwix et ZIMReader. Le projet OpenZIM a hébergé la mise en œuvre du format de fichier ZIM sur [Github](https://github.com/openzim) pour la contribution de la communauté OpenSource.

## Spécifications du format de fichier ZIM

Le format de fichier ZIM a été développé en plus du [format de fichier Zeno](https://openzim.org/wiki/Zeno_file_format) et n'est pas rétrocompatible. Les spécifications de format du format de fichier ZIM sont [disponibles en ligne](https://openzim.org/wiki/ZIM_file_format) par openZIM pour la référence du développeur. OpenZIM a fourni une implémentation open source C++, [LibZim](https://openzim.org/wiki/Zimlib), pour lire et écrire des fichiers ZIM.

Le format de fichier ZIM utilise la compression LZMA2 pour rendre le contenu compact.

{{< figure src="../ZIM_File_Format.jpeg" alt="Format de fichier ZIM" >}}


### En-tête ZIM

Un fichier ZIM commence par un en-tête qui est à l'offset 0. Tous les constituants sont basés sur little-endian et tous les entiers sont des entiers non signés, c'est-à-dire uint_16, uint_32, uint_64.

|Nom du champ |Type| Décalage| Longueur| Descriptif|
---|---|---|---|---|
|magicNumber| entier| 0| 4| Le nombre magique pour reconnaître le format de fichier doit être 72173914 (0x44D495A) |
|majorVersion| entier| 4| 2| Version majeure du format de fichier ZIM (5 ou 6) |
|minorVersion| entier| 6| 2| Version mineure du format de fichier ZIM |
|uuid| entier| 8| 16| identifiant unique de ce fichier zim |
|articleCount| entier| 24| 4| nombre total d'articles |
|clusterCount| entier| 28| 4| nombre total de grappes |
|urlPtrPos| entier| 32| 8| position de la liste de pointeurs de répertoire triée par URL |
|titlePtrPos| entier| 40| 8| position de la liste de pointeurs de répertoires triée par Titre|
|clusterPtrPos| entier| 48| 8| position de la liste des pointeurs de cluster|
|mimeListPos| entier| 56| 8| position de la liste des types MIME (également taille de l'en-tête) |
|mainPage| entier| 64| 4| page principale ou 0xffffffff si pas de page principale|
|dispositionPage| entier| 68| 4| page de mise en page ou 0xffffffffff si pas de page de mise en page|
|checksumPos| entier| 72| 8| pointeur vers la somme de contrôle md5 de ce fichier sans la somme de contrôle elle-même. Cela pointe toujours 16 octets avant la fin du fichier.|

## Références ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)

