{
"date": "2023-11-09",
   "keywords":[
"zoo",
"fichier zoo",
"fichier compressé zoo",
"comment ouvrir un fichier zoo",
"déposer",
"extension de fichier zoo",
"extension",
"déposer"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Fichier ZOO - Qu'est-ce qu'un fichier .zoo et comment l'ouvrir ?",
   "description":"Découvrez le format de fichier compressé ZOO et les API permettant de créer et d'ouvrir des fichiers ZOO.",
"linktitle": "ZOO",
   "menu":{
      "docs":{
         "identifier":"compression-zoo",
"parent": "compression"
}
},
"lastmod": "2023-11-09"
}

## Qu'est-ce qu'un fichier ZOO ?

Un fichier « .zoo » est un format d'archive utilisé pour compresser et stocker des fichiers et des répertoires ; est similaire à d'autres formats d'archives comme « .zip », « .tar » et « .rar ». Le format « .zoo » était populaire au début de l'informatique, mais il est devenu moins courant ces dernières années. Il a été initialement développé par **Rahul Dhesi** et était principalement utilisé sur les systèmes Unix et DOS.

Un fichier « .zoo » contient généralement un ou plusieurs fichiers et répertoires qui ont été compressés et archivés dans un seul fichier. Vous pouvez créer et extraire des fichiers « .zoo » à l'aide de divers outils logiciels prenant en charge ce format.

Les archives ZOO ont une fonctionnalité unique qui leur permet de stocker plusieurs versions du même fichier à condition que chaque version ait été modifiée à une date différente. Cela signifie que les utilisateurs de ZOO peuvent enregistrer et accéder aux itérations précédentes du fichier directement à partir des archives ZOO. Cette fonctionnalité permet aux utilisateurs de revenir à une version antérieure du fichier ou de comparer une version plus ancienne avec une version plus récente, offrant un moyen pratique de gérer les révisions et les modifications des fichiers au fil du temps.

## Opérations courantes des fichiers ZOO

Voici quelques opérations courantes associées aux fichiers `.zoo` :

1. **Création d'un fichier `.zoo` :** Vous pouvez utiliser un utilitaire de ligne de commande comme "zoo" pour créer un fichier `.zoo`. Par exemple, la commande suivante créera l'archive `.zoo` à partir du répertoire :
    








`zoo a -c répertoire archive.zoo/`
    








Dans cette commande, « a » signifie « ajouter », « -c » spécifie la compression et « archive.zoo » est le nom de l'archive de sortie.
    








2. **Extraction de fichiers d'un fichier `.zoo` :** Pour extraire le contenu de l'archive `.zoo`, vous pouvez utiliser une commande comme celle-ci :
    








`zoo et archive.zoo`
    








Cette commande extraira les fichiers du fichier `archive.zoo`.
    








3. **Liste du contenu d'un fichier `.zoo` :** Vous pouvez lister le contenu de l'archive `.zoo` sans les extraire en utilisant l'option "l" :
    








    








`zoo l archive.zoo`

## Comment ouvrir un fichier ZOO?

Les programmes qui ouvrent les fichiers ZOO incluent

- **zoo** (Gratuit) pour (Windows, Linux)

## Les références
* [Zoo (file format)](https://en.wikipedia.org/wiki/Zoo_(file_format))
