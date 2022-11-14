{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - Langage de définition de rapport côté client",
  "keywords" :[ "rdlc", "langage de définition de rapport", "format mkv", "XSD", "langage de définition de rapport côté client"],
  "description":"En savoir plus sur le format de fichier RDLC qui est une représentation XML d'une définition de rapport SQL Server Reporting Services.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Qu'est-ce qu'un fichier RDLC ? ##

Le RDLC signifie Report Definition Language Client side. En fait, il s'agit d'une extension du fichier de rapport créé à l'aide de la technologie de création de rapports de Microsoft. La version SQL Server 2005 de Report Designer est utilisée pour créer ces fichiers. Le contrôle **ReportViewer** côté client peut exécuter directement les rapports RDLC.

## Fichiers RDL VS RDLC
|Fichiers .rdl |Fichiers .rdlc|
---|---|
|Les fichiers RDL sont créés par la version SQL Server 2005 de Report Designer|Les fichiers RDLC sont créés par la version Visual Studio 2005 de Report Designer|
|Il est utilisé dans SQL Server Reporting Services|Il est utilisé dans Visual Studio|
|C'est un rapport distant|C'est un rapport local|
|Besoin d'une instance de Reporting Services pour l'exécuter|Pas besoin d'une instance de Reporting Services|

## Création de fichiers de définition de rapport client (.rdlc)
Le contrôle ReportViewer est utilisé pour exécuter les fichiers de définition de rapport client (.rdlc) à l'aide de la capacité de traitement intégrée du contrôle. Les rapports client que vous exécutez en mode de traitement local peuvent être facilement créés dans votre projet d'application. Voici les approches pour créer le rapport :

- Utilisez l'**Assistant de rapport** pour créer une nouvelle définition de rapport client (.rdlc).

- Créez un nouveau fichier de définition de rapport client (.rdlc) à l'aide de Visual Studio.

- Générer une définition de rapport par programmation.


Vous ne pouvez prévisualiser un rapport qu'en l'exécutant dans un contrôle **ReportViewer**. Veuillez noter que vous pouvez ouvrir et modifier la définition du rapport à tout moment, puis créer ou déployer l'application pour vérifier les résultats.

## Références ##

- [Création de fichiers de définition de rapport client (.rdlc)](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

