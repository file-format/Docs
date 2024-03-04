{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AIDL failas – „Android“ sąsajos apibrėžimo kalbos failas",
  "description":"Sužinokite, kas yra AIDL failo formatas, naudodamiesi pavyzdžiu ir API, kurios gali kurti ir atidaryti AIDL failus.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl-lt",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Kas yra AIDL failas?

AIDL (Android Interface Definition Language) failas leidžia Android kūrėjams užmegzti ryšį tarp skirtingų programų. Remdamiesi programavimo sąsaja, klientas ir paslauga sutinka bendrauti naudodami tarpprocesinį ryšį (IPC). AIDL faile yra [Java](/programming/java/) šaltinio kodas, skirtas apibrėžti šias sąsajas ir ryšio tarp programų sutartis.

AIDL failus galite atidaryti naudodami Google Android Studio arba bet kurią teksto rengyklę, pvz., Microsoft Notepad ir Notepad++.

## AIDL failo formatas – daugiau informacijos

AIDL yra tekstiniai failai, kuriuose yra sąsajų, skirtų bendrauti tarp programų. Android OS neleidžia vienam procesui pasiekti kito proceso atminties. Dėl to procesai padalija objektus į primityvus, kad suprastų pagrindinę operacinę sistemą ir sukurtų komunikacijos struktūrų procesą kūrėjui.

### Kokius duomenų tipus palaiko AIDL?

Pagal numatytuosius nustatymus AIDL palaiko šiuos duomenų tipus.

 * Visi primityvūs Java programavimo kalbos tipai (pvz., int, long, char, boolean ir pan.)
 * Styga
 * CharSequence
 * Sąrašas
 * Žemėlapis

## AIDL failo pavyzdys

Toliau pateikiamas AIDL failo pavyzdys.

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
## Nuorodos

 * [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

