{
  "date": "2019-10-11",
  "keywords": [
"aex",
"aex tiedosto",
"tiedosto muoto",
"tiedostotyyppi",
"mikä on aex-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AEX - Alpha Five Compiled Global Functions -tiedosto",
  "description": "Opi tuntemaan, mikä on AEX-tiedosto ja API:t, jotka voivat luoda ja avata AEX-tiedostoja.",
  "linktitle": "AEX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ae-fix"
}
},
  "lastmod": "2021-12-07"
}

## Mikä on AEX-tiedosto?

AEX-tiedosto (.aex-tunniste) on käännetty [Xbasic](https://documentation.alphasoftware.com/documentation/pages/Ref/Xbasic/index.xml)-tiedosto, joka sisältää käännetyn ohjelmakoodin yleisille funktioille. Sitä voidaan käyttää verkkosovelluksissa kutsumalla niitä palvelinpuolen [.a5w](/web/a5w/)-sivuilta. AEX-tiedostot ladattiin ja purettiin kutsumalla A5W-tiedostoista a5w_load_aex- ja a5w_unload_aex-funktioita. Uudessa toteutuksessa nämä tiedostot ladataan kuitenkin muistiin sisällyttämällä ne a5_application.5i-tiedostoon. Xbasic-ohjelmointikieltä käyttää Alpha Anywhere -ohjelmisto mobiili- ja verkkosovellusten kehittämiseen.

## AEX-tiedostomuoto - lisätietoja

AEX-tiedostot tallennetaan levylle binääritiedostomuodossa ja sisältävät Xbasicilla kirjoitetun funktiokoodin. Xbasicin komentosarjakäskyt määrittävät suorituksen rakenteen ja kulun, mukaan lukien toistuvan toiminnon suorittamisen tai pysäyttämisen tai valinnan kahden tai useamman vaiheen välillä olosuhteiden perusteella. {{HYPERLINKKI}}:sta saat tarkempia tietoja siitä.

## Viitteet

 * [Alpha Five](https://www.alphasoftware.com/)
 * [Alpha Five Documentation](https://documentation.alphasoftware.com/documentation/pages/index.html)
 * [Xbasic Guide](https://documentation.alphasoftware.com/pages/Guides/Xbasic/index.xml)

