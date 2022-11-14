{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Base de données Btrieve" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier BTR et les API qui peuvent créer et ouvrir des fichiers BTR.",
  "title" :"BTR - Fichier de base de données Btrieve",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Qu'est-ce qu'un fichier BTR ?

Un fichier avec l'extension .btr est un fichier de base de données créé par l'application de base de données transactionnelle [Btrieve](https://www.actian.com/). Contrairement aux systèmes de gestion de bases de données relationnelles (RBMS), Btrieve est basé sur la méthode d'accès séquentiel indexé (ISAM), qui est un moyen de stocker des données pour une récupération rapide. Le fichier BTR stocke une collection d'enregistrements et est utilisé pour générer des rapports selon les besoins. Les fichiers BTR peuvent être ouverts à l'aide de Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility et Legend Software BTRIEVE Viewer.

## Structure du fichier BTR - Plus d'informations

La structure de données interne et l'alignement de chaque octet dans la structure d'un fichier BTR ne sont pas accessibles au public. Cependant, Btrieve
fournit l'[API Btrieve](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) qui peut être utilisée pour lire les informations des fichiers BTR. Il est compatible avec les langages de programmation et les environnements de développement suivants.

* Embarcadero C/C++
* Embarcadero Delphes
* GNU C/C++
* Micro Focus COBOL
* Microsoft Visual Basic
* Microsoft Visual C++
* Watcom C/C++

La récupération des données d'un fichier BTR dépend du fichier DDF qui lui est associé. Sans le DDF, il ne sera pas facile de récupérer les informations d'un tel fichier.

## Références

* [Btrieve - Wikipédia](https://en.wikipedia.org/wiki/Btrieve)
* [Introduction aux API Btreive](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

