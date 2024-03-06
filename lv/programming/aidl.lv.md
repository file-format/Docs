{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AIDL fails — Android saskarnes definīcijas valodas fails",
  "description":"Uzziniet par AIDL faila formātu, izmantojot piemēru un API, kas var izveidot un atvērt AIDL failus.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl-lv",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Kas ir AIDL fails?

AIDL (Android Interface Definition Language) fails ļauj Android izstrādātājiem izveidot saziņu starp dažādām lietotnēm. Pamatojoties uz programmēšanas saskarni, gan klients, gan pakalpojums piekrīt sazināties, izmantojot starpprocesu saziņu (IPC). AIDL failā ir [Java](/programming/java/) pirmkods, lai definētu šīs saskarnes un līgumus saziņai starp lietotnēm.

Varat atvērt AIDL failus, izmantojot Google Android Studio vai jebkuru teksta redaktoru, piemēram, Microsoft Notepad un Notepad++.

## AIDL faila formāts — vairāk informācijas

AIDL ir teksta faili, kas satur saskarnes saziņai starp lietotnēm. Android OS neļauj vienam procesam piekļūt cita procesa atmiņai. Tas liek procesiem sadalīt savus objektus primitīvos, lai izprastu pamatā esošo operētājsistēmu un izveidotu komunikācijas struktūru procesu izstrādātājam.

### Kādus datu tipus atbalsta AIDL?

AIDL pēc noklusējuma atbalsta šādus datu tipus.

 * Visi primitīvie veidi Java programmēšanas valodā (piemēram, int, long, char, Boolean un tā tālāk)
 * Stīga
 * CharSequence
 * Saraksts
 * Karte

## AIDL faila piemērs

Tālāk ir sniegts AIDL faila piemērs.

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
## Atsauces

 * [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

