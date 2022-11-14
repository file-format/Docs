{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier AWK - Fichier de script AWK",
  "description":"En savoir plus sur le format de fichier AWK et les API qui peuvent créer et ouvrir des fichiers AWK.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Qu'est-ce qu'un fichier AWK ?

Un fichier AWK est un fichier de script créé pour l'application de traitement de texte **AWK** fournie avec les systèmes d'exploitation Unix et Linux. Il contient des instructions logiques pour effectuer des actions sur le texte ou le contenu d'un fichier, telles que la correspondance, le remplacement et l'impression de texte. Cela permet de générer des rapports et du texte formaté à partir du fichier d'entrée. L'utilitaire awk se trouve généralement dans /usr/bin/awk sur la plupart des distributions Linux/Unix.

## Comment créer un script AWK ?

Un fichier AWK peut être créé ou ouvert dans n'importe quel éditeur de texte sous Linux/Unix OS. Un nouveau fichier de script AWK peut être créé comme suit.

```
$ vi script.awk
```

Cela ouvrira le fichier AWK dans l'éditeur de texte. Entrez quelques instructions dans l'éditeur de texte comme suit.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
La première ligne de ce contenu textuel est expliquée comme suit.

* \# ! - appelé "Shebang", qui spécifie un interpréteur pour les instructions d'un script
* /usr/bin/awk – est l'interpréteur
* -f - option d'interpréteur, utilisée pour lire un fichier programme

## Comment exécuter le script AWK ?

Enregistrez le fichier et rendez le script exécutable en lançant la commande ci-dessous :
```
$ chmod +x script.awk
```

Le script peut ensuite être exécuté comme suit.

```
$ ./script.awk
```

qui se traduit par la sortie suivante.

```
Writing my first Awk executable script!
```

## Référence ##

* [Écrire des scripts à l'aide du langage de programmation Awk] (https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

