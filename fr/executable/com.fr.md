{
  "date" : "2021-06-29",
  "keywords" :[ "fichier com", "qu'est-ce qu'un fichier com", "fichier", "exemple com", "extension de fichier com","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier COM et les API qui peuvent créer et ouvrir des fichiers COM.",
  "title" :"COM - Format de fichier de commande DOS",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## Qu'est-ce qu'un fichier COM ?
Les fichiers COM sont simplement utilisés pour exécuter un ensemble de commandes ou d'instructions. Un fichier COM consiste en un programme exécutable qui peut être exécuté à partir de Windows ou de MS-DOS. De même qu'un fichier EXE, le fichier COM est également enregistré au format binaire, mais il est différent du fichier EXE car il n'a ni en-tête ni métadonnées et sa taille maximale est de 64 Ko environ. Lorsque le fichier COM s'exécute pour la première fois sur un système 32 bits, il vous invite à installer le composant NT Virtual DOS Machine (NTVDM). Le fichier COM peut être exécuté sur la version 64 bits de Microsoft Windows avec une machine virtuelle prenant en charge l'environnement MS-DOS.

## Format de fichier COM
Le format de fichier COM est un format exécutable binaire utilisé dans Microsoft Windows ou MS-DOS. Sa structure consiste simplement en un ensemble d'instructions; il n'a pas d'en-tête et ne contient pas de métadonnées standard. Il stocke toutes ses données et son code dans un seul segment et son binaire a une taille maximale de 64 Ko. Ce format de fichier ne se déplace pas lorsque vous essayez de le relancer. Ainsi, le système d'exploitation le charge à une adresse prédéfinie. De plus, il est possible de créer un fichier COM à exécuter sous les deux systèmes d'exploitation sous la forme d'un **fat binary**. Il n'y a pas de compatibilité réelle au niveau de l'instruction. Les instructions au point d'entrée sont sélectionnées pour être égales en fonctionnalités mais différentes dans les deux systèmes d'exploitation, et faire en sorte que le programme en cours d'exécution, saute à la section du système d'exploitation en cours d'utilisation. Il s'agit essentiellement de deux programmes différents avec la même procédure dans un seul fichier, précédés d'un code sélectionnant celui à utiliser.
### Exemple de fichier COM
Lors de l'exécution d'un fichier COM, les instructions sont lues à partir du premier octet et sont suivies consécutivement jusqu'à ce que les dernières instructions soient trouvées. Voici un exemple de code ASM :

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## Références

* [Fichier COM - par Wikipewdia](https://en.wikipedia.org/wiki/COM_file)

