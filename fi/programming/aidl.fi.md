{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AIDL-tiedosto - Android-käyttöliittymän kielitiedosto",
  "description":"Opi AIDL-tiedostomuodosta esimerkkien ja sovellusliittymien avulla, jotka voivat luoda ja avata AIDL-tiedostoja.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl-fi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Mikä on AIDL-tiedosto?

AIDL (Android Interface Definition Language) -tiedoston avulla Android-kehittäjät voivat muodostaa viestinnän eri sovellusten välillä. Ohjelmointirajapinnan perusteella sekä asiakas että palvelu sopivat kommunikoivansa IPC:n (Interprocess communication) avulla. AIDL-tiedosto sisältää [Java](/programming/java/) lähdekoodin näiden rajapintojen ja sovellusten välisen viestinnän sopimusten määrittämiseksi.

Voit avata AIDL-tiedostoja Google Android Studiolla tai millä tahansa tekstieditorilla, kuten Microsoft Notepad ja Notepad++.

## AIDL-tiedostomuoto - lisätietoja

AIDL ovat tekstitiedostoja, jotka sisältävät liitännät sovellusten välistä viestintää varten. Android-käyttöjärjestelmä ei salli yhden prosessin käyttää toisen prosessin muistia. Tämä saa prosessit jakamaan objektinsa primitiivisiksi taustalla olevan käyttöjärjestelmän ymmärtämiseksi ja kehittämään viestintärakenteiden prosessin.

### Mitä tietotyyppejä AIDL tukee?

AIDL tukee seuraavia tietotyyppejä oletuksena.

 * Kaikki Java-ohjelmointikielen primitiivityypit (kuten int, long, char, boolean ja niin edelleen)
 * merkkijono
 * CharSequence
 * Lista
 * Kartta

## Esimerkki AIDL-tiedostosta

Seuraavassa on esimerkki AIDL-tiedostosta.

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
## Viitteet

 * [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

