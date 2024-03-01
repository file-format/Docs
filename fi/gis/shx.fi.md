{
  "date": "2021-07-29",
  "keywords": [
"shx tiedosto",
"shx tiedostomuoto",
"mikä on shx-tiedosto",
"tiedosto",
"shx esimerkki",
"shx tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "SHX - Shapefile Shape Index Format",
  "description": "Opi SHX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata SHX-tiedostoja.",
  "linktitle": "SHX",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sh-fix"
}
},
  "lastmod": "2021-07-29"
}

## Mikä on SHX-tiedosto?
SHX-tiedosto kuuluu shape index -muotoon, joka on ominaisuusgeometrian sijaintiindeksi, joka mahdollistaa nopean etsimisen eteen- ja taaksepäin. SHX on suora pääsy offset-tiedosto. Tässä tiedostossa ei ole tietoja, vain kopio ensimmäisistä sadasta tavusta, tietueen numero ja siirtymä kyseisen tietueen aloitustavuun shp:ssä. Huomaa, että tiedosto, jonka laajennus on .shx, ei yhdistä {{HYPERLINKKI}}- ja {{HYPERLINKKI2}}-tiedostoja.

## SHX-tiedostomuoto
SHX-muoto sisältää ominaisuusgeometrian sijaintiindeksin ja 100-tavuisen otsikon, joka on samanlainen kuin SHP-tiedosto, ja sen jälkeen minkä tahansa määrän 8-tavuisia kiinteän pituisia tietueita, jotka sisältävät seuraavat kaksi kenttää:
| Tavua | Tyyppi | Endianness | Käyttö |
-------|-------|------------|---------------------------------|
| 0-3 | int32 | iso | Tietueen siirtymä (16-bittisillä sanoilla) |
| 4–7 | int32 | iso | Tietueen pituus (16-bittisillä sanoilla) |

Tämä indeksi mahdollistaa hakemisen taaksepäin muototiedostossa etsimällä ensin taaksepäin muotoindeksistä ja sitten lukemalla tietueen siirtymän. Tätä siirtymää voidaan käyttää etsimään oikeaa sijaintia SHP-tiedostossa. Voit myös etsiä eteenpäin; mielivaltaisen määrän tietueita samalla menetelmällä. On kuitenkin mahdollista luoda täydellinen indeksi yhdessä SHP-tiedoston kanssa, mutta se voi lisätä mahdollisuuksia saada SHP-tiedosto vioittumaan nopeasti.


## Viitteet

* [Shapefile - Wikipedia)](https://en.wikipedia.org/wiki/Shapefile)



