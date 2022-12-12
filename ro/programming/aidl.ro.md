{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier AIDL - Fișier limbaj de definire a interfeței Android",
  "description":"Aflați despre ce este formatul de fișier AIDL cu exemple și API-uri care pot crea și deschide fișiere AIDL.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Ce este un fișier AIDL?

Un fișier AIDL (Android Interface Definition Language) permite dezvoltatorilor Android să stabilească comunicarea între diferite aplicații. Pe baza interfeței de programare, atât clientul, cât și serviciul sunt de acord să comunice utilizând comunicarea între procese (IPC). Fișierul AIDL conține codul sursă [Java](/ro/programming/java/) pentru definirea acestor interfețe și contracte de comunicare între aplicații.

Puteți deschide fișiere AIDL cu Google Android Studio sau orice editor de text, cum ar fi Microsoft Notepad și Notepad++.

## Format de fișier AIDL - Mai multe informații

AIDL sunt fișiere text care conțin interfețele de comunicare între aplicații. Sistemul de operare Android nu permite unui proces să acceseze memoria altui proces. Acest lucru determină procesele să-și împartă obiectele în primitive pentru înțelegerea sistemului de operare subiacent și să stabilească procesul de structuri de comunicare pentru dezvoltator.

### Ce tipuri de date sunt acceptate de AIDL?

AIDL acceptă următoarele tipuri de date în mod implicit.

* Toate tipurile primitive din limbajul de programare Java (cum ar fi int, long, char, boolean și așa mai departe)
* șir
* CharSequence
* Lista
* Hartă

## Exemplu de fișier AIDL

Mai jos este un exemplu de fișier AIDL.

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
## Referințe

* [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

