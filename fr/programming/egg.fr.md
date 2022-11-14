{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier EGG - Fichier de distribution Python",
  "description":"En savoir plus sur le format de fichier EGG et les API qui peuvent créer et ouvrir des fichiers EGG.",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## Qu'est-ce qu'un fichier EGG ?

Un fichier EGG, également connu sous le nom d'œufs Python, est un ancien format de distribution des distributions Python. Il s'agit d'une archive compressée [ZIP](/fr/compression/zip/) avec l'extension .egg et contient les fichiers source de l'application Python ainsi que des méta-informations sur la distribution. Les fichiers EGG sont une alternative à un fichier exécutable Windows [EXE](/fr/executable/exe/) mais sont multiplateformes. Cet ancien format pour les distributions Python a été remplacé par le nouveau format de fichier Wheel (WHL) au début de 2010.

## Format de fichier œuf

Les fichiers EGG sont enregistrés sous forme d'archives ZIP compressées. Cela signifie que si vous remplacez l'extension .egg par .zip, vous pourrez l'ouvrir avec des utilitaires de décompression standard tels que Corel WinZIP, Microsoft Explorer ou RARLAB WinRAR.

Les fichiers EGG peuvent être créés à l'aide du package **distutils** disponible par Python. **SetupTools** est un autre outil capable de créer et d'ouvrir des fichiers EGG. Les fichiers EGG peuvent être installés en tant que package à l'aide de **easy_install**.

`REMARQUE - Le format de fichier EGG est devenu obsolète au profit du nouveau format de fichier WHL de roue.`

## Référence ##

* [ŒUFS Python] (https://python101.pythonlibrary.org/chapter38_eggs.html)

