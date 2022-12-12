{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AIDL File - Android Interface Definition Language File",
  "description":"Zjistěte, co je formát souboru AIDL, s příklady a rozhraními API, která mohou vytvářet a otevírat soubory AIDL.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Co je soubor AIDL?

Soubor AIDL (Android Interface Definition Language) umožňuje vývojářům Androidu navázat komunikaci mezi různými aplikacemi. Na základě programovacího rozhraní se klient i služba dohodnou na komunikaci pomocí meziprocesové komunikace (IPC). Soubor AIDL obsahuje [Java](/cs/programming/java/) zdrojový kód pro definování těchto rozhraní a smlouvy pro komunikaci mezi aplikacemi.

Soubory AIDL můžete otevřít pomocí Google Android Studio nebo libovolného textového editoru, jako je Microsoft Notepad a Notepad++.

## Formát souboru AIDL – Další informace

AIDL jsou textové soubory, které obsahují rozhraní pro komunikaci mezi aplikacemi. OS Android neumožňuje jednomu procesu přístup k paměti jiného procesu. To vede procesy k rozdělení svých objektů do primitiv pro pochopení základního operačního systému a vytvoření procesu komunikačních struktur pro vývojáře.

### Jaké datové typy podporuje AIDL?

AIDL standardně podporuje následující datové typy.

* Všechny primitivní typy v programovacím jazyce Java (jako je int, long, char, boolean atd.)
* Tětiva
* CharSequence
* Seznam
* Mapa

## Příklad souboru AIDL

Následuje příklad souboru AIDL.

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
## Reference

* [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

