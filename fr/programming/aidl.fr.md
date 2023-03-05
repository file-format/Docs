{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier AIDL - Fichier de langage de définition d'interface Android",
  "description":"Découvrez ce qu'est le format de fichier AIDL avec des exemples et des API qui peuvent créer et ouvrir des fichiers AIDL.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Qu'est-ce qu'un fichier AIDL ?

Un fichier AIDL (Android Interface Definition Language) permet aux développeurs Android d'établir une communication entre différentes applications. Sur la base de l'interface de programmation, le client et le service conviennent de communiquer à l'aide de la communication interprocessus (IPC). Le fichier AIDL contient le code source [Java](/fr/programming/java/) pour définir ces interfaces et contrats de communication entre les applications.

Vous pouvez ouvrir des fichiers AIDL avec Google Android Studio ou n'importe quel éditeur de texte tel que Microsoft Notepad et Notepad++.

## Format de fichier AIDL - Plus d'informations

AIDL sont des fichiers texte qui contiennent les interfaces de communication entre les applications. Android OS ne permet pas à un processus d'accéder à la mémoire d'un autre processus. Cela conduit les processus à diviser leurs objets en primitives pour comprendre le système d'exploitation sous-jacent et établir le processus de structures de communication pour le développeur.

### Quels types de données sont pris en charge par AIDL ?

AIDL prend en charge les types de données suivants par défaut.

* Tous les types primitifs du langage de programmation Java (tels que int, long, char, boolean, etc.)
* Chaîne de caractères
* Séquencecar
* Liste
* Carte

## Exemple de fichier AIDL

Voici un exemple de fichier AIDL.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## Références

* [Langage de définition d'interface Android (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

