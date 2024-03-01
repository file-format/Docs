{
  "date": "2019-10-11",
  "keywords": [
"JAR",
".jar",
"mikä on jar-tiedosto",
"kuinka avata jar-tiedosto",
"laajennus",
"tiedosto",
"jar tiedosto",
"jar tiedostomuoto",
".jar laajennus"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JAR - Java-arkistotiedostomuoto",
  "description": "Opi JAR-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata JAR-tiedoston.",
  "linktitle": "JAR",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ja-fir"
}
},
  "lastmod": "2020-09-10"
}

## Mikä on JAR-tiedosto?

Tiedosto, jonka tunniste on .jar, on Java-arkistotiedosto, joka sisältää useita eri sovelluksiin liittyviä tiedostoja yhtenä tiedostona. Tämä tiedostomuoto luotiin vähentämään ladatun Java-sovelman lataamisen nopeutta selaimeen HTTP-tapahtuman kautta välttämällä useiden HTTP-yhteyksien luomista. Yksi JAR-tiedosto voi sisältää Java-luokkatiedostoja ([.class](/programming/class/)), [images](/image/) ja [sounds](/audio/). Sovelluksen kehittäjä voi allekirjoittaa JAR-tiedoston sisällä olevat yksittäiset kohteet digitaalisesti niiden alkuperän todentamiseksi. JAR-tiedostoja käytetään säännöllisesti luomaan toimivia sovellusliittymiä, jotka sisältävät tiettyjä kyseiseen sovellusliittymään liittyviä toimintoja.

## JAR-tiedostomuoto

JAR files are based on the popular [ZIP file format](/compression/zip/) that archives its individual content files in a single file. JAR file format supports compressions, resulting in a smaller file size for downloading and hence further improves the download time. The [JAR file specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) artilce by Oracle gives complete details about the internal specifications of JAR files.

### Manifest-tiedosto

Kun JAR-tiedosto luodaan, sen sisään luodaan automaattisesti manifestitiedosto, joka sisältää metatietotiedot JAR-tiedoston sisällöstä. Tämä tiedosto näyttää JAR-tiedoston sisällä pakatun sisällön. Tyypillinen manifestitiedosto näyttää seuraavalta, joka näyttää JAR-tiedostoon sisältyvät kansiot ja luokat.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Manifestin tekniset tiedot

Oracle määrittelee manifestin tekniset tiedot seuraavasti.

`manifest-tiedosto`: pääosion rivinvaihto \*individual-section

`main-section`: version-info rivinvaihto \*main-attribute

`versio-info`: Manifest-Version : version-number

`version-numero` : numero+{.numero+}*

`main-attribute`: (mikä tahansa laillinen päämäärite) rivinvaihto

`individual-section`: Nimi : arvo rivinvaihto \*perentry-attribuutti

`perentry-attribute`: (kaikki lailliset perentry-attribuutit) rivinvaihto

`uusi rivi` : CR LF | LF | CR (ei seuraa LF)

numero: {0-9}

### Suoritettava JAR

JAR-tiedostot voivat sisältää myös sovelluksen, jonka Java Virtual Machine (JVM) voi suorittaa samalla tavalla kuin mikä tahansa muu sovellus Microsoft Windows -käyttöjärjestelmässä. Tässä tapauksessa JVM:n on tiedettävä sovelluksen aloituspiste, joka on mikä tahansa luokka, jolla on julkinen staattinen void -päämenetelmä. Luettelotiedosto tunnistaa tällaisen luokan Main-Class-otsikolla seuraavassa muodossa:

```
Main-Class: com.example.MyClassName
```



## Viitteet

 * [JAR File Overview](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
 * [JAR-tiedostomuoto](https://en.wikipedia.org/wiki/JAR_(file_format))

