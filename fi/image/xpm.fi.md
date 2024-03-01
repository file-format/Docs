{
  "date": "2019-10-11",
  "keywords": [
"xpm tiedosto",
"xpm tiedostomuoto",
"mikä on xpm-tiedosto",
"tiedosto",
"xpm esimerkki",
"xpm tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XPM - X PixMap -tiedostomuoto",
  "description": "Opi XPM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata XPM-tiedostoja.",
  "linktitle": "XPM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-xp-fim"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on XPM-tiedosto?

Tiedosto, jonka pääte on .xpm, on kuvatiedostomuoto, jota käytti X Windows -järjestelmä. Se tukee läpinäkyviä pikseleitä ja yleensä kohdistaa kuvakkeiden kuvakarttojen luomiseen. Se tukee yksivärisiä, gra-scale- ja värillisiä pixmap-tietoja. Nämä on suunniteltu käsin muokattaviksi, ja ne voidaan sisällyttää [C](/programming/c/)-koodiin. Tätä tarkoitusta varten XPM-tiedostot ovat pelkkää tekstitiedostomuotoa ja noudattavat C-ohjelmointikielen syntaksia. XPM-tiedostoja voidaan avata erilaisilla kuvien katseluohjelmilla, kuten
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView ja Canvas X.

## XPM tiedostomuoto

XPM-tiedostomuoto käyttää C-syntaksia, jotta nämä voidaan integroida C- ja C++-ohjelmiin. Se koostuu seuraavista kuudesta eri osasta.

 * \<Values>
 * \<Colors>
 * \<Pixels>
 * \<Extensions>

Osat ovat itse asiassa joukko merkkijonoja seuraavasti.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Seuraavassa on kunkin osan yksityiskohdat.

`<Values> ` - Tämä osio on merkkijono, joka sisältää neljä tai kuusi kokonaislukua, jotka ovat kantaluvussa 10 ja vastaavat:

 * pixmap leveys ja korkeus
 * värien määrä
 * merkkien määrä pikseliä kohden
 * valinnaiset hotspot-koordinaatit ja XPMEXT-tunniste

`<Colors> ` - Tämä osio sisältää yhtä monta merkkijonoa kuin on värejä. Jokainen merkkijono on seuraava:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Tämä osio koostuu<height> jouset ja<width> \*<chars_per_pixel> hahmoja. Joka<chars_per_pixel> pituuden merkkijonon tulee olla jokin aiemmin määritetyistä ryhmistä<Colors> osio.

`<Extension> ` - Laajennusosio on merkittävä, jos se ei ole tyhjä<Values> osio. Se voi koostua useista<Extension> alajaksot, jotka voivat olla seuraavia kahta tyyppiä:

 * yksi itsenäinen merkkijono, joka koostuu seuraavasti: XPMEXT<extension-name><extension-data>
 * tai useista merkkijonoista koostuva lohko: XPMEXT<extension-name><related extension-data composed of several strings>

## Viitteet

* [XPM - Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)

* [XPM-opas](http://www.xfree86.org/current/xpm.pdf)


