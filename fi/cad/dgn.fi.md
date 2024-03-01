{
  "date": "2020-01-12",
  "keywords": [
"DGN",
"Tiedosto",
"Muoto",
"Avata",
"Lukea",
"API",
"MicroStation",
"Intergraph Interactive Graphics Design System"
],
  "author":{
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DGN - MicroStation CAD -suunnittelutiedostomuoto",
  "description": "Opi DGN-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata DGN-tiedostoja.",
  "linktitle": "DGN",
  "menu":{
    "docs":{
      "parent": "cad",
      "identifier": "cad-dg-fin"
}
},
  "lastmod": "2020-01-12"
}

## Mikä on DGN-tiedosto?

Tiedosto, jonka tunniste on .dgn (Design) on CAD-sovellusten, kuten MicroStation ja Intergraph Interactive Graphics Design System, luoma ja tukema piirustustiedosto. Sitä käytetään rakennusprojektien, kuten moottoriteiden, siltojen ja rakennusten, suunnittelun luomiseen ja tallentamiseen. Muoto on samanlainen kuin Autodeskin [DWG](/cad/dwg/)-tiedostomuoto, ja sitä pidetään sen kilpailijana. DNG-tiedostot voidaan tallentaa joko Intergraph Standard -tiedostomuodossa tai V8 DGN:nä. DGN voidaan muuntaa useisiin muihin muotoihin, kuten DWG, [BMP](/image/bmp/), [JPEG](/image/jpeg/), [PDF](/pdf/), [GIF](/image/gif/) ja muihin. Se voidaan avata Autodesk AutoCADilla, Bentley Viewilla ja Bentley Systems MicroStationilla muiden ohjelmistosovellusten, kuten Corel PaintShop Photo Pro- ja IMSI TurboCAD Deluxe -versioiden lisäksi.

## V8 DGN -tiedostomuoto

MicroStation V8 DGN -tiedosto koostuu yhdestä tai useammasta mallista. Malli on säiliö elementeille. V8 DGN poistaa kaikki tiedostomuotoon perustuvat rajoitukset, jotka olivat olemassa MicroStationin aiemmissa versioissa. Seuraavassa on luettelo DGN-tiedostomuodon parannuksista.

 * DGN-tiedoston tasojen lukumäärän rajoitus on poistettu, ja jokainen taso on nimetty ja tallennettu elementiksi.
 * DGN-tiedoston fyysisellä enimmäiskoolla ei ole rajoituksia, ja sitä rajoittaa vain käyttöjärjestelmä (esim. NT-raja on 4 Gt)
 * Yhden elementin enimmäiskoko on 128 kt.
 * Solun enimmäiskokoa ei ole rajoitettu.
 * Solujen nimet on rajoitettu noin 500 merkkiin.
 * DGN-tiedostoon liitettävien viitteiden määrää ei ole rajoitettu.
 * Viivamerkkijonossa, muodossa tai pistekäyrässä voi olla enintään 5 000 kärkeä.
 * Monimutkaisen ketjun tai monimutkaisen muodon komponenttien lukumäärää ei ole rajoitettu.
 * DGN-tiedoston grafiikkaryhmien lukumäärää ei ole rajoitettu.
 * Aita on yhdensuuntainen sen näkymän kanssa, johon se on sijoitettu.
 * Yksi tekstirivi voi sisältää 65 535 merkkiä.
 * Tekstisolmun enimmäiskokoa ei ole rajoitettu.
 * DGN-tiedoston tekstisolmujen lukumäärää ei ole rajoitettu.
 * Jokaisella elementillä on yksilöllinen 64-bittinen tunniste, joka ei muutu elementin elinkaaren aikana.
 * Jokaisella elementillä on aikaleima, joka osoittaa viimeisimmän muutoksen ajan.

## Viitteet

* [DNG – Wikipedia](https://en.wikipedia.org/wiki/DGN)

* [MicroStation V8 DGN File Format](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

