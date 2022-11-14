{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Créer un fichier - Fichier de script Xcode Makefile",
  "description":"En savoir plus sur le format XCode MakeFile et les API qui peuvent créer et ouvrir des fichiers MakeFile.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## Qu'est-ce qu'un fichier MAKE ?

Un fichier MAKE est un fichier de script XCode qui organise la compilation du code. Il est utilisé pour compiler et lier des programmes à partir de plusieurs fichiers de code source. Cela aide à décider quelles parties d'une grande application doivent être recompilées lorsque l'application doit être mise à jour. Faites en sorte que les fichiers utilisent une série d'instructions pour s'exécuter en fonction des fichiers qui ont été modifiés.

## Exemple de format de fichier MAKE

Le contenu suivant est exécuté à l'aide de l'utilitaire Make et les sorties sont les suivantes.

```
hello:
	echo "hello world"
```
**Créer une sortie**

```
$ make
echo "hello world"
hello world
```

## Références
* [XCode et Make - Forums Apple](https://developer.apple.com/forums/thread/657458)
* [Guide d'Object-C] (https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

