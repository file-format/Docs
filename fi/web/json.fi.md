---
date: 2019-10-11
keywords: json, .json, json file format, how to open json files, javascript object notation, json data format, .json file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JSON-tiedostomuoto - Mikä on JSON-tiedostoe?
linktitle: JSON
description: Lansaita JSON-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata JSON-tiedostons.
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Mikä on JSON-tiedosto?

JSON (JavaScript Object Notation) on avoin standardi tiedostomuoto tietojen jakamiseen, joka käyttää ihmisen luettavaa tekstiä tietojen tallentamiseen ja lähettämiseen. JSON-tiedostot tallennetaan .json-tunnisteella. JSON vaatii vähemmän muotoilua ja on hyvä vaihtoehto {{HYPERLINKKI}}:lle. JSON on johdettu JavaScriptistä, mutta se on kielestä riippumaton tietomuoto. JSONin luomista ja jäsentämistä tukevat monet nykyaikaiset ohjelmointikielet. *application/json* on JSON:n mediatyyppi.

## JSON-tiedostomuoto - lyhyt historia

There was a need for real-time server to client communication that lead to the creation of JSON. The JSON format was first specified by Douglas Crockford in March 2001. JSON perustui standardiin ECMA-262 3rd Edition – joulukuu 1999, joka on JavaScriptin osajoukko.

The first edition of JSON standard ECMA-404 was published in October 2013 by Ecma International. RFC 7159 became the main reference for JSON's Internet uses in 2014. Marraskuussa 2017 ISO/IEC 21778:2017 julkaistiin kansainvälisenä standardina. RFC 8259 julkaisi 13. joulukuuta 2017 The Internet Engineering Task Force, joka on Internet Standard STD 90:n nykyinen versio.

## JSON-tiedostorakenne

JSON-tiedot kirjoitetaan **avain/arvo**-pareina. Avain ja arvo erotetaan kaksoispisteellä (:) keskellä, avain on vasemmalla ja arvo oikealla. Eri avain/arvo-parit erotetaan toisistaan pilkulla (,). Avain on merkkijono, jota ympäröivät lainausmerkit, esimerkiksi nimi. Arvot voivat olla seuraavan tyyppisiä.

- Numero.
- String: Unicode-merkkien sarja lainausmerkeillä ympäröitynä.
- Boolean: Totta vai tarua.
- `Array`: Esimerkiksi hakasulkeilla ympäröity arvoluettelo

``` json
[ Omena, Banaani, Orange ]
```

- Object: kokoelma avain/arvo-pareja, joita ympäröivät kiharat aaltosulkeet, esimerkiksi

``` json
{nimi: Jack, ikä: 30, favoriteSport : Jalkapallo}
```

JSON-objekteja voidaan myös upottaa edustamaan tietojen rakennetta. Alla on esimerkki JSON-objektista.

### JSON-muotoesimerkki

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## Mikä on JSON-tiedoston enimmäiskoko?

JSON-tiedoston enimmäiskokoa ei käytännössä ole rajoitettu. Se voi olla niin pitkä kuin säilytettävä sisältö vaatii tilaa.

Kun on kyse JSON-tiedostomuodon käyttämisestä tiedon siirtämiseen Internetin kautta, on oltava varovainen tietokoneen käytettävissä olevien resurssien suhteen. Jos siirretään suuria JSON-tietoja, siirtoon vaikuttaa, jos asiakasselaimen muisti on rajallinen.


Teknisissä määrityksissä ei ole tiukkaa rajaa, mutta sinun on oltava varovainen, ettet kuluta resursseja käyttäjien tietokoneilta, koska se heikentää nopeasti heidän käyttökokemustaan ja he todennäköisesti hylkäävät sovelluksesi.

## JSON vs XML

**XML** on toinen yleinen ja laajalti käytetty tiedostomuoto tiedonvaihtoon Internetissä. Mitä tulee tietojen vaihtoon sovellusten välillä, kehittäjillä on mahdollisuus käyttää sekä XML- että JSON-tiedostomuotoja. JSON on kuitenkin otettu kätevimmäksi tapaksi tietojen vaihtoon sovellusten välillä Internetin kautta seuraavista syistä.

 1. JSON tarjoaa selkeän ja helpommin luettavan näkymän tiedoista XML-tiedostomuotoihin verrattuna
 1. JSON vähentää tiedonsiirron ylimääräisiä kustannuksia Internetissä, koska siinä on vähemmän merkkejä saman tietojoukon määrittämiseen verrattuna XML:ään
 1. Nykyaikaiset ohjelmointikielet tarjoavat sisäänrakennettuja jäsentimiä JSON-vastauksen jäsentämiseksi verkossa.

## UKK

 * **Mihin JSON-tiedostoa käytetään?** JSON-tiedostomuotoa voidaan käyttää välimuotoisena tiedostomuotona datan tallentamiseen, joka on luotu esimerkiksi verkkosivustolla lähetetystä lomakkeesta. Sitä käytetään myös tietomuototiedostona mille tahansa ohjelmointikielelle ja se tarjoaa yhteentoimivuuden erityyppisten tietojen välillä.
 * **Ovatko JSON- ja XML-tiedostot samat?** Ei oikeastaan. JSON eroaa XML:stä siinä, että JSON on lyhyempi, se voidaan lukea ja korjata nopeasti, se voi käyttää taulukoita eikä käytä lopputunnistetta.
 * **Can I convert JSON to CSV?** Yes, there are certain online converter apps such as **GroupDocs Conversion apps** that can [convert JSON to CSV](https://products.groupdocs.app/conversion/json-to-csv).
 * **Kuinka muuntaa JSON PDF-muotoon?** Voit käyttää verkkosovelluksia, kuten Asopse.app for Cells [muuntaa JSON-tiedosto PDF-muotoon](https://products.aspose.app/cells/conversion/json-to- pdf).
 * **Kuinka avata JSON-tiedosto Wordissa?** Voit käyttää verkkosovelluksia, kuten Aspose.app for Words, [muuntaaksesi JSON-tiedoston Wordiksi] (muuntaaksesi JSON-muodon WORD-muotoon Androidissa Javan kautta).

## Tiesitkö?

You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about JSON or Web file formats, you can post your findings in [Web File Format News](https://news.fileformat.com/t/Web) section for people to learn more form these.

## Viitteet

- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

