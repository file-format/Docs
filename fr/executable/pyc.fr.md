{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier PYC et les API qui peuvent créer et ouvrir des fichiers PYC.",
  "title" :"Format de fichier PYC - Fichier compilé Python",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## Qu'est-ce qu'un fichier PYC ?

Un fichier PYC est un fichier de sortie compilé généré à partir du code source écrit en langage de programmation Python. Lorsque le fichier PY est exécuté à l'aide de l'interpréteur Python, il est converti en bytecode pour l'exécution. Dans le même temps, le bytecode compilé est également enregistré en tant que fichier .pyc afin de le réutiliser ultérieurement à partir du cache, le cas échéant.

## Structure du format de fichier PYC

Les fichiers PYC sont en bytecode et leurs spécifications de format de fichier ne sont pas disponibles publiquement. Cependant, l'enquête de certaines sources montre que la [structure d'un fichier PYC](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A% 20marshalled%20code%20object.) se compose de :

* `Un nombre magique de quatre octets` r - Simplement deux octets qui changent à chaque modification du code de marshaling, puis deux octets de 0d0a.
* `Un horodatage de modification de quatre octets` - Horodatage de modification Unix du fichier source qui a généré le .pyc, afin qu'il puisse être recompilé si la source change.
* `A marshalled code object` - la sortie de marshal.dump de l'objet de code résultant de la compilation du fichier source.

## Références

* [La structure des fichiers .pyc](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A%20marshalled%20code%20object.)

