{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "fichier", "extension", "format", "Perl", "langage Perl", "fichiers PL", "programmation"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier PL et les API qui peuvent créer et ouvrir des fichiers PL.",
  "title" :"Fichier PL - Format de fichier de script Perl",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## Qu'est-ce qu'un fichier PL ?

Un fichier avec l'extension .pl est un fichier Perl Script qui est un langage de script. Ceux-ci sont compilés et exécutés à l'aide du logiciel Perl Interpreter. Un fichier de script PL contient des lignes de code, des variables et des commentaires. Les langages de script sont relativement difficiles à
comprendre à d'autres formats de fichiers de programmation tels que [PHP](/fr/programming/php/). Les fichiers PL peuvent être créés et sont compatibles avec Windows, macOS et Linux.

## Brève histoire du langage de script Perl

Cette langue a été utilisée pour la première fois en 1987, de sorte que ces fichiers ont leur origine cette année-là. En 1989, Perl 2 est sorti. Plus tard, il a été mis à jour et a été modifié jusqu'à la version 5.35, et la prochaine version devrait être publiée l'année prochaine.

Dans chaque mise à jour, des outils ont été ajoutés sur la fonctionnalité, les performances et l'apparence de la langue et des fichiers. Il y a eu de nombreuses révisions sur les versions au cours de ces années. C'était à l'origine un langage de script de base, mais il comprend maintenant de nombreux autres modules. A l'origine, c'était un langage très simple, mais les scripts de ce langage étaient assez difficiles à comprendre car ils étaient compacts.

## Spécifications des extensions de format de fichier Perl

Il existe certaines propriétés ou spécifications de ces fichiers de programmation, dont certaines sont les suivantes :

* Le code inclus dans ces fichiers est au format texte brut et utilisé pour le développement de scripts
* Le script du serveur, l'analyse du texte et l'administration du serveur sont les principaux aspects couverts par le script de ce langage
* De nombreux programmes populaires associés à ce langage sont Active state Active Perl et Bare Bones BBEdit (compatible avec Mac OS)
* Ce langage est considéré comme un langage de haut niveau
* Pour Win32, l'utilisateur peut avoir à installer la distribution binaire native du langage
* Il nécessite certains outils de script pour devenir exécutable dans divers kits de ressources Windows
* Visual Studio .NET est un cadre célèbre pour le développement de langages de programmation. L'outil Active State connu sous le nom de Visual Perl est utilisé pour ajouter Perl dans Visual studio
* Dans les fichiers, la première ligne du code source décrit les informations de l'interpréteur utilisé. Les fichiers PL commencent généralement par la ligne **#!/usr/bin/perl** qui indique à votre ordinateur d'exécuter ce script à l'aide d'un interpréteur Perl installé sur l'ordinateur


## Exemples de scripts PL

```
#!/usr/bin/perl
print "Hello, world\n";
```

Cela imprimera

```
Hello, World
```

### Commentaire sur une seule ligne ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Commentaire sur plusieurs lignes ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Affectation de variables ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Affectation de variables scalaires ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Opérations scalaires simples ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Références ##

- [Python (langage de programmation) - Wikipédia](https://en.wikipedia.org/wiki/Python_(langage_de_programmation))

