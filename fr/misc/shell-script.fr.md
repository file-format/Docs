{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Script Shell - Comment l'exécuter sur Ubuntu et Linux",
  "description":"Découvrez ce qu'est Shell Script et comment l'exécuter sur Ubuntu et Linux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-fr",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Qu’est-ce que le script Shell ?

Les scripts Shell impliquent l'écriture d'une série de commandes dans un fichier texte brut, souvent appelé **Script Shell**. Ces scripts sont exécutés par un shell, qui est un interpréteur de ligne de commande. Les coquilles les plus courantes comprennent

1. Bash (Bourne Again SHell)
2. Zsh (coque Z)
3. Poisson.

Les scripts Shell peuvent aller de simples lignes simples à des programmes complexes, et ils sont utilisés pour effectuer une grande variété de tâches, telles que la manipulation de fichiers, l'administration système et l'automatisation de tâches répétitives.

## Avantages des scripts Shell :

1.  **Automation :** Les scripts Shell permettent aux utilisateurs d'automatiser les tâches répétitives, ce qui permet de gagner du temps et de réduire les risques d'erreur humaine.
    
2.  **Personnalisation :** Les utilisateurs peuvent créer des scripts adaptés à leurs besoins spécifiques, offrant un haut degré de personnalisation.
    
3.  **Traitement par lots :** Les scripts Shell sont excellents pour gérer les tâches de traitement par lots, dans lesquelles plusieurs commandes doivent être exécutées en séquence.
    
4.  **Administration système :** les scripts Shell sont couramment utilisés pour les tâches d'administration système, telles que les sauvegardes, la rotation des journaux et l'installation de logiciels.

## Écrire un script Shell simple :

Créons un script shell de base qui imprime un message de bienvenue. Ouvrez un éditeur de texte et créez un fichier nommé « greeting.sh ». Ajoutez les lignes suivantes :

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Enregistrez le fichier et rendez-le exécutable en exécutant la commande suivante dans le terminal :

```
chmod +x greeting.sh
```

Maintenant, vous pouvez exécuter le script :

```
./greeting.sh
```

Le résultat devrait être :

```
Hello, welcome to the world of shell scripting!
```

## Exécution de scripts Shell sur Ubuntu et Linux :

Nous allons maintenant discuter de **comment exécuter un fichier .sh sous Ubuntu et Linux**.

1.  **Rendre le script exécutable :** Avant d'exécuter un script shell, assurez-vous qu'il est exécutable. Utilisez la commande `chmod` comme indiqué précédemment.
    
2.  ** Accédez au répertoire des scripts :** Ouvrez un terminal et utilisez la commande `cd` pour accéder au répertoire contenant votre script shell.
    
3.  **Exécutez le script :** Exécutez le script en tapant « ./scriptname.sh » dans le terminal, en remplaçant « scriptname » par le nom réel de votre script.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **À l'aide de la commande Bash :** Si votre script commence par `#!/bin/bash` (appelé **shebang**), vous pouvez également l'exécuter à l'aide de la commande `bash`.

```
bash greeting.sh
```

## Que signifie $@ dans Shell Script ?

Dans le script shell, `$@` représente tous les arguments de ligne de commande passés au script. Il est souvent utilisé pour référencer une liste d’arguments en tant qu’entités distinctes. Lorsqu'il est utilisé entre guillemets doubles, comme `$@`, il préserve les arguments individuels, en tenant compte des espaces et des caractères spéciaux.

Voici une brève explication :

- `$@` : représente tous les paramètres de position (arguments) passés au script ou à la fonction. Chaque argument est traité comme un mot distinct.
    
- `$@` : Lorsqu'il est entre guillemets, préserve la séparation des arguments, autorisant les espaces ou les caractères spéciaux dans les arguments individuels.
    

Voici un exemple simple pour illustrer :

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Lorsque vous exécutez ce script avec des arguments, par exemple :

```
bash example.sh arg1 "argument 2" arg3
```

Cela produirait :

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Comme vous pouvez le voir, `$@` représente tous les arguments et `$@` préserve les arguments individuels, même s'ils contiennent des espaces.

