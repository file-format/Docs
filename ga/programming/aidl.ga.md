{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Comhad AIDL - Comhad Teanga Sainmhíniú Comhéadain Android",
  "description":"Foghlaim faoi cad is formáid comhaid AIDL ann le sampla agus APIanna ar féidir comhaid AIDL a chruthú agus a oscailt.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl-ga",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Cad is comhad ADL ann?

Ligeann comhad AIDL (Teanga Sainmhíniú Comhéadain Android) d'fhorbróirí Android cumarsáid a bhunú idir aipeanna éagsúla. Bunaithe ar an gcomhéadan ríomhchlárúcháin, aontaíonn an cliant agus an tseirbhís araon cumarsáid a dhéanamh ag baint úsáide as cumarsáid idirphróisis (IPC). Tá [Java](/programming/java/) cód foinse i gcomhad AIDL chun na comhéadain agus na conarthaí cumarsáide seo a shainiú idir aipeanna.

Is féidir leat comhaid AIDL a oscailt le Google Android Studio nó le haon eagarthóir téacs ar nós Microsoft Notepad agus Notepad++.

## Formáid Chomhaid AIDL - Tuilleadh Eolais

Is comhaid téacs iad AIDL ina bhfuil na comhéadain le haghaidh cumarsáide idir aipeanna. Ní cheadaíonn Android OS do phróiseas amháin rochtain a fháil ar chuimhne próisis eile. Mar thoradh air seo déantar na próisis a roinnt ina n-ábhar primitives chun tuiscint a fháil ar an gcóras oibriúcháin bunúsach agus chun an próiseas struchtúir cumarsáide a bhunú don fhorbróir.

### Cad iad na Cineálacha Sonraí a dtacaíonn AIDS leo?

Tacaíonn AIDL leis na cineálacha sonraí seo a leanas de réir réamhshocraithe.

 * Gach cineál primitive sa teanga ríomhchlárúcháin Java (cosúil le slánuimhir, fada, gual, boolean, agus mar sin de)
 * Teaghrán
 * Seicheamh Carachtair
 * Liosta
 * Léarscáil

## Sampla Comhad AIDL

Seo a leanas sampla de chomhad AIDL.

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
## Tagairtí

 * [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

