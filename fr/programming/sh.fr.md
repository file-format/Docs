{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - Fichier de script shell bash",
  "description":"En savoir plus sur le format de fichier SH et les API qui peuvent créer et ouvrir des fichiers SH.",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Qu'est-ce qu'un fichier SH ?

Un fichier avec l'extension .sh est un fichier de commandes de langage de script qui contient un programme informatique à exécuter par le shell Unix. Il peut contenir une série de commandes qui s'exécutent séquentiellement pour effectuer des opérations telles que le traitement de fichiers, l'exécution de programmes et d'autres tâches similaires. Ceux-ci sont exécutés à partir de l'interface de ligne de commande par l'utilisateur ou par lots pour effectuer plusieurs opérations en même temps. Les fichiers de script peuvent être ouverts dans des éditeurs de texte tels que Notepad, Notepad++, Vim, Apple Terminal et d'autres applications similaires sous Windows, MacOS et Linux OS.

## Format de fichier SH

Les fichiers SH sont écrits en texte brut selon la syntaxe définie. Ces fichiers de script prennent en charge :

* `Commentaires` - Les commentaires commencent par un # et sont ignorés par le shell.
* `Raccourcis` - Ceux-ci peuvent être utilisés pour renommer une commande pour une exécution courte et facile.
* `Tâches par lots` - Plusieurs commandes peuvent être exécutées automatiquement qui, autrement, devraient être saisies manuellement. Cela évite d'avoir à attendre qu'un utilisateur déclenche chaque étape de la séquence.
* `Généralisation` - En utilisant des boucles simples, une plus grande généralisation est obtenue pour des opérations telles que la conversion d'images d'un format à un autre.

## Exemple de fichier SH

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## Comment exécuter le fichier SH ?
Les fichiers SH s'exécutent généralement sous Linux, même sous Windows, vous devez vous connecter à un terminal Linux à l'aide de logiciels tels que Putty pour exécuter les fichiers sh. Voici les étapes pour exécuter un fichier SH sur un terminal Linux.

1. Ouvrez le terminal Linux et accédez au répertoire où se trouve le fichier SH.
2. En utilisant la commande `chmod`, définissez l'autorisation d'exécution sur votre script (si elle n'est pas déjà définie).
3. Exécutez le script en utilisant l'un des éléments suivants
1. `./nomfichier.sh`
2. `sh nomfichier.sh`
3. `nom-script-bash-ici.sh`

## Références

* [Bashscripting pour les débutants](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)

