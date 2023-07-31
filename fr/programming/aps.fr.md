{
  "date" : "2021-04-22",
  "keywords": [ "aps file", "visual studio aps file", "extension", "format","aps file visual studio","aps file extension","how to open aps file","APS file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APS - Fichier de ressources Visual C++",
  "description":"En savoir plus sur le format de fichier APS avec un exemple APS et des API qui peuvent créer et ouvrir des fichiers APS.",
  "linktitle" : "APS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Qu'est-ce qu'un format de fichier APS ?
Un fichier APS est créé par Visual C++, une application de développement logiciel de Microsoft. Il enregistre la représentation binaire d'une ressource incorporée au projet et permet à l'application de charger plus rapidement les ressources. Vous pouvez facilement trouver ces fichiers avec l'extension de fichier .aps. En fait, les éditeurs de ressources ne lisent pas directement les fichiers resource.h, c'est pourquoi le compilateur de ressources les compile dans des fichiers .aps qui sont consommés par les éditeurs de ressources.

## Format de fichier APS
Le format de fichier APS n'est qu'une étape de compilation et ne stocke que des données symboliques. Les informations non symboliques telles que les commentaires sont ignorées pendant le processus de compilation. Par exemple, lorsque vous enregistrez, l'éditeur de ressources écrase le fichier de script de ressources et le fichier resource.h. Toutes les modifications apportées aux ressources elles-mêmes restent incorporées dans le fichier de script de ressources, mais les commentaires seront toujours perdus une fois le fichier de script de ressources écrasé.


## Références

* [Fichiers de ressources (C++)](https://learn.microsoft.com/en-us/cpp/windows/resource-files-visual-studio?view=msvc-160)
 


