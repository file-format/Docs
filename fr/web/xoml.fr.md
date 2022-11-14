{
  "date" : "2019-10-11",
  "keywords" :["xoml", "Fichier", "Extension", "Format de fichier", "Extension de fichier", "Langage de balisage objet extensible"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XOML - Format de fichier de flux de travail Windows",
  "description":"En savoir plus sur le format de fichier XOML et les API qui peuvent créer et ouvrir des fichiers XOML.",
  "linktitle" : "XOML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier XOML ?

XOML est l'acronyme de Extensible Object Markup Language et est un format de sérialisation pour les objets de flux de travail de Windows Workflow Foundation. Basé sur **[XAML](/fr/web/xaml/)**, il est principalement utilisé pour créer des interfaces utilisateur en clair **[XML](/fr/web/xml/)**. Ceux-ci sont utilisés pour déclarer le flux de travail pour l'interface utilisateur et sont compilés avec le fichier séparé contenant la logique d'implémentation. Il contient une structure arborescente qui définit un nœud de flux de travail racine, des sous-éléments imbriqués et des segments de code intégrés. Lorsqu'un nouveau flux de travail est créé avec Visual Studio pour .NET, vous avez la possibilité de choisir s'il doit être au format Code ou au format Code Separated. Si vous sélectionnez le dernier, l'IDE créera deux fichiers pour vous ; l'un au format XOML (composé de la disposition et des paramètres du flux de travail), et l'autre au format [.CS](/fr/programming/cs/)/[.VB](/fr/programming/vb/) où réside le code de programmation.

