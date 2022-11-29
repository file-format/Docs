{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AIDL File - Android Interface Definition Language File",
  "description":"Lär dig mer om vad AIDL-filformat är med exempel och API:er som kan skapa och öppna AIDL-filer.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Vad är en AIDL fil?

En AIDL-fil (Android Interface Definition Language) låter Android-utvecklare upprätta kommunikation mellan olika appar. Baserat på programmeringsgränssnittet kommer både klienten och tjänsten överens om att kommunicera med interprocess communicate (IPC). AIDL-filen innehåller [Java](/sv/programming/java/) källkod för att definiera dessa gränssnitt och kontrakt för kommunikation mellan appar.

Du kan öppna AIDL-filer med Google Android Studio eller vilken textredigerare som helst som Microsoft Notepad och Notepad++.

## AIDL-filformat - Mer information

AIDL är textfiler som innehåller gränssnitten för kommunikation mellan appar. Android OS tillåter inte en process att komma åt minnet för en annan process. Detta leder till att processerna delar upp sina objekt i primitiver för att förstå det underliggande operativsystemet och etablera processen för kommunikationsstrukturer för utvecklare.

### Vilka datatyper stöds av AIDL?

AIDL stöder följande datatyper som standard.

* Alla primitiva typer i Java-programmeringsspråket (som int, long, char, boolean, och så vidare)
* Sträng
* CharSequence
* Lista
* Karta

## Exempel på AIDL-fil

Följande är ett exempel på en AIDL-fil.

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
## Referenser

* [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

