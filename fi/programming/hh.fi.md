{
  "date": "2019-10-11",
  "keywords": [
"h",
".HH",
"mikä on .hh-tiedosto",
"kuinka avata .hh-tiedosto",
"laajennus",
"tiedosto",
".hh tiedosto",
".hh-tiedostomuoto",
".hh tiedostopääte",
"Esimerkki .HH-tiedostosta"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HH - C++-otsikkotiedostomuoto",
  "description": "Opi HH-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata HH-tiedoston.",
  "linktitle": "HH",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-h-fih"
}
},
  "lastmod": "2021-06-20"
}

## Mikä on HH-tiedosto?

Tiedosto, jonka pääte on .hh, on C++-otsikkotiedosto, joka sisältää muuttujien, vakioiden ja funktioiden ilmoitukset. Näitä ilmoituksia käyttävät vastaavat C++-toteutustiedostot, jotka yleensä tallennetaan [.cpp](/programming/cpp/)-tiedostoina, jotka sisältävät varsinaisen käyttäjälogiikan toteutuksen. .hh-otsikkotiedostoihin viitataan toteutuksen CPP-tiedostoissa käyttämällä #include-direktiiviä. Voit lisätä mahdollisimman monta otsikkotiedostoa C++-projektiisi sisällyttääksesi projektitason ilmoitukset.

## .HH tiedostomuoto

.hh-tiedosto on pelkkä tekstitiedosto, joka luodaan pitäen mielessä otsikkotiedoston määrittelysäännöt. Yleisimmät .hh-tiedostossa ilmoitetut tiedot ovat seuraavat.

**`Muuttujat`** – Object Oriented Programming (OOP) -ohjelmoinnin tapauksessa luokan otsikkotiedosto sisältää määritelmät kaikista luokkatason muuttujista, jotka ovat käytettävissä toteutuksen lähdekooditiedostoissa.
**`Methode Declaration`** - Kaikki menetelmäilmoitukset sisältyvät .h-otsikkotiedostoihin, jotta niitä voidaan käyttää useissa toteutustiedostoissa.
**`Non-inline Function Definitions`** - Otsikkotiedostot voivat sisältää myös ei-inline-menetelmien määritelmiä.
**`Viestikartat`** - Otsikkotiedosto voi sisältää myös viestikarttoja MFC-lähdekoodin toteutuksen tapauksessa. Tällöin viestikartat on linkitetty toiminnallisuuden toteutukseen, joka on linkitetty käyttöliittymäelementteihin, kuten painike, valintaruutu, valintanapit jne.

## Ero .H- ja .HH-tiedostojen välillä

Ilmeisesti .h- ja .hh-otsikkotiedostojen välillä ei ole muuta eroa kuin suositeltu tapa käyttää näitä vastaaville kielille, esim. {{HYPERLINKKI}} tai C++. Otsikkotiedostojen nimeäminen näiden kielten mukaan auttaa sinua erottamaan ne toisistaan suuressa projektissa, joka voi olla sekoitus C- ja C++-toteutuksia.

Lisäksi, jos otsikot on erotettu laajennuksella, editori voi käyttää vastaavaa muotoilua automaattisesti.

Kaiken kaikkiaan näiden kahden tiedostomuodon erottamisesta ei ole haittaa, mutta siitä on hyötyä, ja sitä kehotetaan noudattamaan C- ja C++-erottelussa.

### Yläsuojat

Otsikkotiedostot voivat aiheuttaa monimutkaisia virheitä, jos samaan tiedostoon sisältyy useita ilmoituksia muiden otsikkotiedostojen lisäämisen seurauksena. Nämä kaksoismääritykset aiheuttavat kääntäjävirheitä. Tämä ongelmallinen tilanne voidaan välttää otsikkovartijaksi kutsutulla mekanismilla, jotka ovat ehdollisia käännösdirektiivejä, kuten alla on esitetty.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Tämän otsikon avulla esiprosessori tarkistaa, onko ANY_UNIQUE_NAME_HERE_HPP jo määritetty. Jos otsikko sisällytetään toistuvasti samaan tiedostoon, otsikon sisältö ohitetaan.

## Viitteet

* [Header Fileers – Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

* [.h- ja .hh-tiedostomuotojen ero](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)


