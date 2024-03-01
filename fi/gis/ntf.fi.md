{
  "date": "2021-07-28",
  "keywords": [
"ntf tiedosto",
"ntf tiedostomuoto",
"mikä on ntf-tiedosto",
"tiedosto",
"ntf esimerkki",
"ntf tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "NTF - National Transfer Format -tiedostot",
  "description": "Opi NTF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata NTF-tiedostoja.",
  "linktitle": "NTF",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-nt-fif"
}
},
  "lastmod": "2021-07-28"
}

## Mikä on NTF-tiedosto?
Tiedostoja, joiden tunniste on .ntf, kutsutaan **National Transfer Format (NTF)** -tiedostoiksi. enimmäkseen UK Ordnance Surveyn (OS) käyttämä; erityisesti geospatiaalisen tiedon siirtoon. Sitä hallinnoi British Standards Institute. Siitä on tullut Ordnance Surveyn digitaalisten tietojen standardisiirtomuoto. Ison-Britannian National Grid -projektio, joka on eräänlainen Transverse Mercator, sisältää kaikki NTF-tiedostojen geoviittaustiedot.

## NTF tiedostomuoto
The NTF file format is owned by Ordnance Survey in the United Kingdom; supported by the GDB library for import. The Present version of the NTF file format is 2.0. Tämä tiedostomuoto otettiin käyttöön **PCIDSK**-vektorisegmentin rajoituksen korjaamiseksi, sillä siinä on vain yksi attribuuttikenttä rakennetta kohti, mutta on olemassa useita attribuutteja, jotka voidaan poimia vektoritiedoilla. Voit kiertää NTF-tiedostomuodossa on kaksi segmenttiä. Jokainen segmentti koostuu samoista vektoreista, mutta eri ominaisuuksilla. NTF-vektoritiedoston ensimmäinen segmentti sisältää vektorit, joiden attribuutti on ominaisuuskoodinumero. Toinen segmentti sisältää vektorit, joiden arvo on attribuuttina.

### Koordinaattien viittausjärjestelmä
GDB-kirjasto edustaa rasteri- ja vektoridataa sopivilla TM-projektio-ominaisuuksilla:

- Viitepituusaste: 49,0
- Viiteleveysaste: 2.0
- Väärä Easting: 400 000
- Väärä pohjoinen: -100 000
- Mittakaava: 0,9996012717
- Ellipsoidi: Airy 1830 (E009)
NTF-tiedostojen päivittämiseen tai kirjoittamiseen ei ole saatavilla tukea, eikä DTM-tiedostoja voi linkittää.

### Esimerkki Ogrinfosta
Seuraava esimerkki käyttää **ogrinfoa** NTF-tiedostossa tasonumeroiden hakemiseen:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Viitteet

* [Ison-Britannian kansallinen siirtomuoto (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)

* [Web Mapping - kuvittanut Tyler Mitchell](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)


