{
  "date": "2020-01-10",
  "keywords": [
"c",
".c",
"mikä on ac-tiedosto",
"kuinka avata c-tiedosto",
"laajennus",
"tiedosto",
"c tiedosto",
"c-tiedostomuoto",
"c tiedostopääte"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "C - C-kielen ohjelmointitiedosto",
  "description": "Opi C-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata C-tiedostoja.",
  "linktitle": "C",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--fic"
}
},
  "lastmod": "2020-01-10"
}

## Mikä on C-tiedosto?

C-tunnisteella tallennettu tiedosto on C-ohjelmointikielellä kirjoitettu lähdekooditiedosto. **C-tiedosto** sisältää kaikki sovelluksen toiminnot lähdekoodin muodossa. Lähdekoodin ilmoitus kirjoitetaan otsikkotiedostoihin, jotka on tallennettu tunnisteella [.h](/programming/h/). C++ on C-kielen moderni muoto ja sitä käytetään useimpien ohjelmistojen kehittämiseen nykyään.

## Lyhyt historia

C-kieli syntyi UNIX-käyttöjärjestelmän erilaisten apuohjelmien luomisen seurauksena. Denis Ritchie, mies tämän ohjelmointikielen luomisen takana, työ alkoi alun perin 1960-luvulla ja 1970-luvun alussa.

## C Tiedostomuoto

C-tiedostot on kirjoitettu pelkkää tekstitiedostomuotoa noudattaen ohjelmointikielen syntaksia. Tyypillisessä C-tiedostossa on:

 * tuontilauseke tiedoston yläreunassa tuodaksesi otsikkotiedostot
 * yksi tai useampi menetelmä halutun toiminnallisuuden toteuttamiseksi

### Otsikkojen tuonti

Otsikkotiedostot, joiden tarkenne on .h, sisältävät tarvittavat include-lausekkeet muiden toimintotiedostojen sisällyttämiseksi projektiin. Lisäksi nämä sisältävät toteutustiedostossa määriteltyjen menetelmien ilmoitukset. Otsikkotiedostot sisällytetään alla olevan include-lausekkeen avulla.

```
#include <filename.h>
```

### Lähdekoodin käyttöönotto

Toiminnallisten vaatimusten varsinainen toteutus on koodattu menetelmiksi C-tiedostoon. Jokaisella C-tiedoston menetelmällä on palautustyyppi, menetelmän nimi ja sillä voi olla joitain syöttöparametreja. Jos palautustyyppi ei ole mitätön, menetelmä saattaa palauttaa jonkin arvon.

### C-koodiesimerkki
Tässä on ac-esimerkkiohjelma:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **Referenssit** ##

* [Luokkien toteutus – Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)


