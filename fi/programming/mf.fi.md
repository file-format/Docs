{
  "date": "2019-10-11",
  "keywords": [
"mf tiedosto",
"mf",
"laajennus",
"muoto",
"mf tiedostomuoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MF - Java Manifest -tiedostomuoto",
  "description": "Opi MF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MF-tiedostoja.",
  "linktitle": "MF",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-m-fif"
}
},
  "lastmod": "2020-09-10"
}

## Mikä on MF-tiedosto?

Mf-päätteinen tiedosto on Java Manifest -tiedosto, joka sisältää tietoja yksittäisistä [JAR](/programming/jar/)-tiedostomerkinnöistä. Itse MF-tiedosto sisältyy JAR-tiedostoon ja sisältää kaikki laajennuksen ja pakettiin liittyvät määritelmät. JAR-tiedostoja voidaan tuottaa käytettäväksi suoritettavana tiedostona. Tässä tapauksessa mainfest-tiedosto määrittää sovelluksen pääluokan, joka sisältää **`public static void main`** -käskyn. Manifest-tiedostot ovat nimeltään MANIFEST.MF, ja ne voidaan avata millä tahansa tekstieditorilla Windows-, MacOS- ja Linux-käyttöjärjestelmissä.

## Manifest-tiedostomuodon tekniset tiedot

[Manifest file format specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) are available by Oracle in their guide for JAR file format. A Manifest file comprises of main sections that are followed by a list of sections for individual JAR file entries. Each section follows some rules and restrictions.

### Pääosat

Pääosio:

* sisältää tietoja JAR-tiedoston suojauksesta ja määrityksistä

* sisältää tietoja sovelluksesta tai laajennuksesta, johon JAR-tiedosto kuuluu

* määrittää tärkeimmät attribuutit jokaiselle yksittäiselle luettelokohdalle


**Huomautus**: Mitään tämän osan attribuuttia ei voi nimetä Nimi.

### Yksittäiset osiot

Yksittäinen osio määrittelee erilaisia attribuutteja JAR-tiedoston paketeille tai tiedostoille. Jokaisen osion on aloitettava attribuutilla nimeltä Nimi, jonka arvon on oltava suhteellinen polku tiedostoon tai absoluuttinen URL-osoite, joka viittaa arkiston ulkopuolisiin tietoihin.

### Manifestin tekniset tiedot

|Asenteet|Kuvaus|
---|---|
|manifest-tiedosto|pääosion rivinvaihto *yksittäinen osio|
|main-section|version-info rivinvaihto *main-attribute|
|versio-info|Manifest-versio : version-numero|
|versionumero|numero+{.numero+}*|
|main-attribute|(kaikki lailliset pääattribuutit) rivinvaihto|
|individual-section|Nimi : arvo rivinvaihto *perentry-attribute|
|perentry-attribute|(kaikki lailliset perentry-attribuutit) rivinvaihto|
|uusirivi|CR LF | LF | CR (ei sen jälkeen LF)|
|numero|{0-9}|

## Viitteet

 * [Oracle - JAR File Format](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
 * [JAR-tiedostomuoto](https://en.wikipedia.org/wiki/JAR_(file_format))

