{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AIDL File - Android Interface Definition Language File",
  "description":"Lær om, hvad AIDL-filformat er med eksempler og API'er, der kan oprette og åbne AIDL-filer.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl-da",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Hvad er en AIDL fil?

En AIDL-fil (Android Interface Definition Language) giver Android-udviklere mulighed for at etablere kommunikation mellem forskellige apps. Baseret på programmeringsgrænsefladen accepterer både klienten og tjenesten at kommunikere ved hjælp af interprocess communicate (IPC). AIDL-filen indeholder [Java](/programming/java/) kildekode til at definere disse grænseflader og kontrakter for kommunikation mellem apps.

Du kan åbne AIDL-filer med Google Android Studio eller en hvilken som helst teksteditor såsom Microsoft Notepad og Notepad++.

## AIDL-filformat - flere oplysninger

AIDL er tekstfiler, der indeholder grænseflader til kommunikation mellem apps. Android OS tillader ikke én proces at få adgang til hukommelsen for en anden proces. Dette får processerne til at opdele deres objekter i primitiver for forståelse af det underliggende operativsystem og etablere processen med kommunikationsstrukturer for udvikleren.

### Hvilke datatyper understøttes af AIDL?

AIDL understøtter som standard følgende datatyper.

 * Alle primitive typer i Java-programmeringssproget (såsom int, long, char, boolean og så videre)
 * Snor
 * CharSequence
 * Liste
 * Kort

## Eksempel på AIDL-fil

Følgende er et eksempel på en AIDL-fil.

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
## Referencer

 * [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

