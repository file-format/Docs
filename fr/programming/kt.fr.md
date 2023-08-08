---
date: 2019-10-11
keywords: kt, .kt, format de fichier kotlin, comment ouvrir des fichiers kotlin, comment exécuter des fichiers kotlin, format de fichier .kt, fichier kt, extension de fichier kotlin, extension .kt, kotlin vs java
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier KT
linktitle: KT
description: "Découvrez le format de fichier KT et les API qui peuvent créer et ouvrir des fichiers KT."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Qu'est-ce qu'un fichier KT ? ##

Un code source écrit en Kotlin est enregistré avec l'extension .kt, communément appelée **extension de fichier Kotlin**. Le Kotlin est un langage de programmation multiplateforme à usage général développé par JetBrains pour être entièrement interopérable avec [Java](/fr/programming/java/). La marque Kotlin est protégée par la Fondation Kotlin.

Kotlin a été annoncé comme le langage de programmation préféré pour le développement d'applications Android par Google le 7 mai 2019. Android Studio 3.0 a commencé à prendre en charge Kotlin comme alternative au développement d'applications Android en octobre 2017.

## Bref historique du format de fichier Kotlin KT ##

Kotlin a été dévoilé par JetBrains en juillet 2011 en tant que nouveau langage de programmation pour JVM. Le responsable de JetBrains, Dmitry Jemerov, a déclaré que la plupart des langages manquaient de fonctionnalités qu'ils recherchaient, à l'exception de Scala, mais que la lenteur de la compilation de Scala était un inconvénient. L'un des principaux objectifs de Kotlin était de compiler aussi rapidement que Java. Le projet Kotlin a été open-source sous licence Apache 2 en février 2012.

La version 1.0 de Kotlin est sortie le 15 février 2015. Android a annoncé une prise en charge de premier ordre de Kotlin sur Android lors de Google I/O 2017. Kotlin 1.2 est sorti le 28 novembre 2017 avec la possibilité de partager du code entre les plateformes JVM et JavaScript. Kotlin 1.3 est sorti le 29 octobre 2018 avec la prise en charge de la programmation asynchrone. Google a annoncé que Kotlin serait le langage de programmation préféré pour le développement d'applications Android le 7 mai 2019. Kotlin 1.4 est sorti en août 2020 avec quelques légères modifications pour prendre en charge l'interopérabilité avec Swift/Objective-C.

## Syntaxe Kotlin ##

Kotlin a été conçu pour être meilleur que Java mais toujours interopérable avec le code Java pour permettre une migration progressive de Java vers Kotlin.

* Les points-virgules sont facultatifs dans Kotlin. Une nouvelle ligne suffit pour indiquer la fin de l'instruction.
* Kotlin prend en charge deux types de variables, en lecture seule, définies par le mot-clé *val*, et modifiables, définies par le mot-clé *var*.
* Les cours sont privés et définitifs par défaut. Pour dériver d'une classe, la classe de base doit être déclarée avec le mot clé *open*.
* Kotlin prend également en charge la programmation procédurale.
* Le point d'entrée du programme Kotlin est la fonction "principale" similaire à Java, C#, etc.

### Exemple de syntaxe ###

Voici un exemple de syntaxe Kotlin.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

Dans le code ci-dessus, le mot-clé **fun** définit la fonction nommée main. A l'intérieur de la fonction, une variable en lecture seule 'audience' est déclarée avec le mot-clé **val**. En utilisant la méthode **println**, "Hello World from Kotlin" est imprimé sur la console. La valeur de la variable audience est injectée dans la chaîne avec le signe **$**.

## Kotlin contre Java
Le Kotlin est un langage officiel pour écrire des applications Android offrant de nombreuses fonctionnalités avancées, mais de nombreux développeurs Java experts ne montrent toujours pas leur intérêt à passer à Kotlin. Ils pensent qu'ils peuvent tout faire avec Java uniquement. Voici donc la comparaison entre deux technologies qui peuvent convaincre les développeurs java de changer :

| Paramètre | Java | Kotlin |
|--------------------|-----------|---------------- -|
| Objets singletons | √ | √ |
| Types de caractères génériques | √ | Χ |
| compilation | Codes byte | Machine virtuelle |
| Expression lambda | Χ | √ |
| Tableau invariant | Χ | √ |
| Champs non privés | √ | Χ |
| Lancements intelligents | Χ | √ |
| Sécurité nulle | Χ | √ |
| Membres statiques | √ | Χ |

## Références ##

- [Kotlin (langage de programmation) - Wikipédia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

