{
"date": "20/04/2023",
  "keywords": [
"fichier ldb",
"qu'est-ce qu'un fichier ldb",
"quelles informations contient ldb",
"quel est le but du fichier ldb",
"extension ldb",
"déposer",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier LDB - Fichier de verrouillage Microsoft Access",
  "description":"Découvrez le format LDB et les informations qu'il contient.",
"linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
"parent": "divers"
}
},
"derniermod": "20/04/2023"
}

## Qu'est-ce qu'un fichier LDB ?

Un fichier LDB est un fichier de verrouillage utilisé par Microsoft Access pour empêcher plusieurs utilisateurs de modifier simultanément la même base de données. Lorsque l'utilisateur ouvre une base de données Access, Access crée un fichier LDB correspondant dans le même répertoire que la base de données. Ce fichier contient des informations sur qui utilise actuellement la base de données et quels enregistrements ils modifient.

Le fichier LDB est automatiquement créé par Microsoft Access lors de l'ouverture de la base de données et est supprimé lors de la fermeture de la base de données. Il est important de noter que le fichier LDB ne doit jamais être supprimé manuellement car cela pourrait entraîner des problèmes avec la base de données.

Si vous rencontrez des problèmes avec la base de données Microsoft Access, une solution potentielle consiste à essayer de supprimer le fichier LDB associé à cette base de données. Cela libérera tous les verrous qui pourraient vous empêcher d'accéder à la base de données. Cependant, assurez-vous de faire une sauvegarde de la base de données avant d'essayer, car la suppression du fichier LDB peut entraîner une perte ou une corruption des données si elle n'est pas effectuée correctement.

## Format de fichier LDB - Plus d'informations

Un fichier LDB dans Microsoft Access contient des informations sur les utilisateurs qui accèdent actuellement à la base de données, telles que leur nom d'utilisateur, le nom de leur ordinateur et l'heure de connexion. Le fichier LDB contient également des informations sur les verrous placés sur la base de données, tels que les enregistrements en cours de modification par quel utilisateur.

Voici une liste plus détaillée des types d'informations pouvant être trouvées dans un fichier LDB :

- **Nom d'utilisateur** - le nom de l'utilisateur qui accède actuellement à la base de données
- **Nom de l'ordinateur** - le nom de l'ordinateur à partir duquel l'utilisateur accède à la base de données.
- **Heure de connexion** - l'heure à laquelle l'utilisateur a ouvert la base de données pour la première fois
- **Verrouillages d'enregistrement** - informations sur les enregistrements en cours de modification par quel utilisateur
- **Verrouillages d'objets** - informations sur les objets de base de données (tels que les tables, les formulaires ou les rapports) qui sont actuellement modifiés par quel utilisateur.
- **Informations de connexion** : informations sur la manière dont l'utilisateur est connecté à la base de données (par exemple, s'il utilise une connexion locale ou réseau)

Les informations contenues dans le fichier LDB sont utilisées par Microsoft Access pour empêcher plusieurs utilisateurs d'apporter simultanément des modifications contradictoires à la même base de données. Lorsqu'un utilisateur tente de modifier un enregistrement ou un objet déjà verrouillé par un autre utilisateur, Microsoft Access affiche un message indiquant que l'objet est déjà utilisé. Le fichier LDB est mis à jour à mesure que les utilisateurs ouvrent et ferment la base de données et apportent des modifications aux objets verrouillés.

## Les références
* [Qu'est-ce qu'un fichier LDB ?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

