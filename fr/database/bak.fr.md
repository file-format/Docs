{
  "date" : "2020-11-11",
  "keywords" :[ "BAK", "extension", "fichier", "format de fichier", "Type de fichier BAK", "Extension de fichier BAK", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier BAK et les API qui peuvent créer et ouvrir des fichiers BAK.",
  "title" :"Format de fichier BAK - Fichier de sauvegarde de la base de données",
  "linktitle" : "BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-12-04"
}

## Qu'est-ce qu'un fichier BAK ?

Un fichier avec l'extension .bak est généralement un fichier de sauvegarde utilisé par différents outils logiciels pour stocker des sauvegardes de données. Du point de vue de la base de données, un fichier BAK est utilisé par Microsoft SQL Server pour stocker le contenu d'une base de données. Toutes les données et tous les fichiers associés à la base de données sont stockés dans ce format de fichier pour être récupérés au cas où la base de données serait corrompue ou invalide pour une raison quelconque. Les fichiers de sauvegarde peuvent être stockés et indexés sur d'autres serveurs à des fins de sécurité. Plusieurs applications peuvent créer des fichiers BAK tels que SQL Server Management Studio, Transact-SQL et Windows PowerShell.

## Format de fichier BAK

Les détails internes d'un fichier BAK ne sont pas connus, mais il est largement admis qu'il est basé sur le format de bande Microsoft (MTF). Les spécifications MTF sont disponibles et peuvent être référencées pour comprendre la structure du fichier. Le document fournit des détails sur le stockage MTF à toute personne ayant des connaissances générales sur les opérations de gestion du stockage, les lecteurs de bande et les systèmes de fichiers.

### Ensembles de données

Un ensemble de données est un ensemble d'objets écrits sur un support de stockage (bande, disque optique, etc.) lors de la sauvegarde ou de la restauration des données. Les ensembles de données comprennent plusieurs médias en cas de grand volume de données.

### Éléments fondamentaux du MTF

Un fichier MTF se compose de certains éléments fondamentaux qui constituent ses blocs de construction. Ces éléments sont :

#### Blocs de description

Les blocs de description (DBLK) sont utilisés pour le contrôle du format et constituent les fondations primaires d'un fichier MTF. Un seul fichier MTF définit plusieurs DBLK pour chaque rôle unique. Chaque DBLK est un bloc de données de longueur variable divisé en quatre parties :

* `Common Block Header` - Structure de longueur fixe commune à tous les DBLK. C'est le seul en-tête de bloc requis.
* `DBLK Type Information` - Bloc de longueur fixe spécifique au type de DBLK en cours de définition
* `Données du système d'exploitation` - Données spécifiques définies en fonction du type de DBLK et des systèmes d'exploitation
* `Information DBLK` - Informations spécifiques DBLK de longueur variable qui ne peuvent pas être enregistrées avec les informations DBLK de longueur fixe.

 {{< figure src="../bak.png" alt="Format de fichier de sauvegarde Microsoft SQL" >}}

#### Flux de données

Les flux de données dans un fichier MTF sont utilisés pour l'encapsulation et l'alignement des données. Il comprend un en-tête de flux, suivi des données de flux. Un en-tête de flux ne peut encapsuler qu'un seul type de données de flux.

{{< figure src="../bak_datastream.png" alt="Format de fichier de sauvegarde Microsoft SQL" >}}

#### Marques de fichiers

Une marque de fichier est utilisée pour une séparation logique et un accès rapide au sein d'un média. Les marques de fichiers sont émulées par le pilote de périphérique ou par l'utilisation du bloc Soft Filemark Descriptor dans le cas où le périphérique utilisé ne fournit pas de marques de fichiers.

## Références ##

* [[MS-BCP] : format de copie en masse](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

