{
  "date": "2021-07-30",
  "keywords": [
"dlg tiedosto",
"dlg tiedostomuoto",
"mikä on dlg-tiedosto",
"tiedosto",
"dlg esimerkki",
"dlg tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "DLG - Shapefile Shape Index Format",
  "description": "Opi DLG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DLG-tiedostoja.",
  "linktitle": "DLG",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-dl-fig"
}
},
  "lastmod": "2021-07-30"
}

## Mikä on DLG-tiedosto?
Tiedosto, jonka laajennus on .dlg, sisältää Digital Line Graphin, joka on kartografinen karttaominaisuus, joka esitetään digitaalisessa vektorimuodossa ja jota hallinnoi US Geological Survey (USGS). DLG-tiedostot ovat saatavilla kahdessa eri muodossa:
1. **Valinnainen muoto**: Helppokäyttöinen muoto, joka sisältää 80-tavun loogisen tietueen pituuden, UTM-maakoordinaattijärjestelmän ja topologian linkit, jotka sisältyvät linja-, solmu- ja alueelementteihin.
2. **Spatial Data Transfer Standard (SDTS) -muoto**: muoto, joka helpottaa paikkatietojen siirtämistä eri tietokonejärjestelmien välillä.

## DLG tiedostomuoto
DLG-tiedostomuoto on suunniteltu USGS-kartoille, ja ne lähetetään suuressa, keskikokoisessa ja pienessä mittakaavassa jopa yhdeksällä eri ominaisuuskategorialla. DLG-tiedostot ovat valinnaisia ja Spatial Data Transfer Standard (SDTS) -muotoja, joissa on topologinen rakenne käytettäväksi kartoitus- ja GIS-sovelluksissa.
### DLG-tiedostomuodon tekniset tiedot
DLG-tiedostot jaetaan kolmessa eri mittakaavassa:

1. **Suuri mittakaava** - vastaavat yleensä:
- USGS 7,5 - 7,5 minuuttia
- 1:24 000 ja 1:25 000 mittakaavassa topografiset nelikulmakartat
- 1:63 360 mittakaavassa Alaskalle
- 1:30 000 mittakaavassa Puerto Ricossa
 
2. **Keskiaste** - johdettu USGS:stä: 
- 30 - 60 minuuttia
- 1:100 000 mittakaavan karttasarja
3. **Pieni mittakaava** – johdettu USGS:n 1:2 000 000 mittakaavan poikkileikkauskartoista Yhdysvaltain kansallisatlasista
### Tietoluokat
Nine different categories of layers, or features, are available in DLG files:
1. Julkinen maanmittausjärjestelmä (PLSS)
2. Rajat (BD)
3. Kuljetus (TR)
4. Hydrografia (HY)
5. Hypsografia (HP)
6. Ei-kasviperäiset piirteet (NV)
7. Kyselyohjaus ja merkit (SM) 
8. Ihmisen tekemät ominaisuudet (MS) 
9. Kasvillinen pintapeite (SC)

Laajamittainen DLG-tiedostot tarjoavat kaikki yhdeksän kerrosta, kun taas keskikokoiset tarjoavat viisi kerrosta PLSS, BD, TR, HY ja HP. Pienen mittakaavan DLG:t tarjoavat viisi kerrosta: PLSS, BD, TR, HY ja MS.

## Viitteet

* [Digitaalinen viivakaavio - Wikipedia)](https://en.wikipedia.org/wiki/Digital_line_graph)



