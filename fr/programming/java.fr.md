---
date: 2019-10-11
keywords: java, .java, format de fichier java, comment ouvrir des fichiers java, comment exécuter des fichiers java, fichier java, exemple de code java
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier Java
linktitle: Java
description: "Découvrez le format de fichier Java et les API qui peuvent créer et ouvrir des fichiers Java."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Qu'est-ce qu'un fichier Java ? ##
Un fichier contenant le code source Java et enregistré avec l'extension de fichier .java est appelé fichier Java. Java est l'une des technologies les plus utilisées pour le développement de jeux, d'applications mobiles, Web et de bureau. Étant donné que Java est indépendant de la plate-forme, il fonctionne parfaitement sur Windows, Mac, Linux, Raspberry Pi, etc. Le Java est très similaire à C # et C ++, il est donc plus facile de basculer entre ces langages.

## Bref historique ##

Le projet Java a été lancé en juin 1991 par James Gosling, Mike Sheridan et Patrick Naughton. Java s'appelait initialement Oak. Il a ensuite été renommé Green et finalement Java. James Gosling a conçu Java avec une syntaxe similaire à C/C++. La première version publique de Java a été publiée en 1996 par Sun Microsystems. Il pouvait fonctionner sur tous les systèmes populaires, ce qui a rapidement rendu Java populaire. Avec la sortie de Java 2 en décembre 1998, plusieurs configurations pour différents types de plates-formes ont été construites. Les versions étaient les suivantes

- J2EE (Java EE) : pour les solutions d'entreprise
- J2ME (Java ME) : Pour les applications mobiles
- J2SE (Java SE) : pour les applications de bureau

Le 19 novembre 2006, Java Virtual Machine (JVM) a été lancé par Sun en tant que logiciel libre et open source. Après qu'Oracle Corporation a acquis Sun Microsystems en 2009-2010, James Gosling a démissionné d'Oracle le 2 avril 2010.

## Comment lancer/exécuter du code Java ##

Pour exécuter le code Java, il doit d'abord être compilé. Pour cela, le SDK Java est requis. Le SDK Java compile le code Java dans un fichier de classe de bytecode. Il existe des IDE comme Eclipse et IntelliJ Idea qui facilitent le travail avec les fichiers Java en fournissant la complétion de code et une interface facile à utiliser pour compiler et exécuter le code Java.

## Format de fichier Java ##

La syntaxe de Java a été fortement influencée par C et C++ mais contrairement à C++, Java a été construit presque exclusivement comme un langage orienté objet. En Java, tout le code est écrit dans des classes et chaque élément de données est un objet. Contrairement à C++, Java ne prend pas en charge la surcharge d'opérateurs ou l'héritage multiple.

### Exemple de code Java ###

Voici un exemple de syntaxe Java.

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
Dans le code ci-dessus, le mot clé **public** désigne le modificateur d'accès. Il indique que cette classe peut être accessible par les classes en dehors de la hiérarchie des classes. Le modificateur d'accès peut également être **protected** (accessible dans le même package) ou **private** (les méthodes ne sont accessibles que par la même classe). Le **statique** devant la méthode indique que la méthode peut être invoquée sans instance spécifique de la classe. Le **void** indique que la méthode ne renverrait rien. Pour imprimer la chaîne sur la console. La commande System.out.println est utilisée. Dans cette commande, la classe *System* a un champ statique *out* qui est une instance de la classe *PrintStream* contenant la méthode *println*.

Le nom de fichier des fichiers Java doit être le même que le nom de la classe. Ainsi, le fichier Java pour l'exemple de code serait nommé *ExampleApp.java*.

## Références ##

- [Java (langage de programmation) - Wikipédia](https://en.wikipedia.org/wiki/Java_(programming_language))

