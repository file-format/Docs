{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AIDL-bestand - Android-interfacedefinitietaalbestand",
  "description":"Meer informatie over wat AIDL-bestandsindeling is met voorbeelden en API's die AIDL-bestanden kunnen maken en openen.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Wat is een AIDL-bestand?

Met een AIDL-bestand (Android Interface Definition Language) kunnen Android-ontwikkelaars communicatie tot stand brengen tussen verschillende apps. Op basis van de programmeerinterface komen zowel de klant als de service overeen om te communiceren via interprocescommunicatie (IPC). AIDL-bestand bevat [Java](/nl/programming/java/) broncode voor het definiëren van deze interfaces en contracten voor communicatie tussen apps.

U kunt AIDL-bestanden openen met Google Android Studio of een teksteditor zoals Microsoft Notepad en Notepad++.

## AIDL-bestandsindeling - Meer informatie

AIDL zijn tekstbestanden die de interfaces voor communicatie tussen apps bevatten. Android OS staat niet toe dat een proces toegang krijgt tot het geheugen van een ander proces. Dit leidt ertoe dat de processen hun objecten in primitieven splitsen om het onderliggende besturingssysteem te begrijpen en het proces van communicatiestructuren voor de ontwikkelaar tot stand te brengen.

### Welke gegevenstypen worden ondersteund door AIDL?

AIDL ondersteunt standaard de volgende gegevenstypen.

* Alle primitieve typen in de programmeertaal Java (zoals int, long, char, boolean, enzovoort)
* Snaar
* CharSequence
* Lijst
* Kaart

## AIDL-bestandsvoorbeeld

Hieronder volgt een voorbeeld van een AIDL-bestand.

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
## Referenties

* [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

