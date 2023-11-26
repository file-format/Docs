
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"4ème fichier - Format de fichier de la quatrième langue",
  "description":"Découvrez ce qu'est le format de fichier .4ème avec un exemple et les API qui peuvent créer et ouvrir des 4èmes fichiers.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Qu'est-ce qu'un 4ème fichier ?

Un fichier avec l'extension de fichier .4th est un fichier de programmation créé pour le **Forth Programming Language**. Il contient le code source des programmes écrits dans le langage de programmation Forth et génère la sortie lorsque le programme est exécuté. Il s'agit simplement d'un autre fichier de langage de programmation similaire au fichier source [C](/fr/programming/c/) et [C++](/fr/programming/cpp/).

## 4ème format de fichier - Plus d'informations


### Exemple de code du 4ème langage de programmation

Voici un exemple de programme simple écrit en Forth qui calcule la factorielle d'un nombre donné :

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

Dans cet exemple, le mot factoriel prend un seul argument n et renvoie sa factorielle. Le mot dup duplique la valeur en haut de la pile, drop supprime la valeur en haut de la pile et * multiplie les deux valeurs en haut de la pile. Les constructions if et start/jusqu'à contrôlent le flux du programme.

Pour utiliser ce programme, vous devez entrer la définition dans l'interpréteur Forth, puis appeler le mot factoriel avec le numéro dont vous souhaitez trouver la factorielle :

```
10 factorial .
```
Cela donnerait la sortie 3628800, qui est le factoriel de 10.

## Les références

* [Forth Langage de programmation](https://en.wikipedia.org/wiki/Forth_(programming_langage))

