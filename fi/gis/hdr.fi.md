{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "HDR-tiedosto - ESRI BIL -otsikkotiedostomuoto",
  "description":"Mikä on HDR-tiedosto?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr-fi",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Mikä on HDR-tiedosto?

HDR-tiedosto on GIS-otsikkotiedosto, joka sisältää .BIL (Band-interleaved by line) -tiedoston otsikkotiedot. Se kuvaa kuvatietoja ja sillä on sama nimi kuin kuvatiedostolla. HDR-tiedosto koostuu joukosta merkintöjä, joista jokainen kuvaa tietyn kuvan määritteen. HDR-tiedosto kuvaa BIL-tiedoston asettelua ja muotoilua käännettäväksi reaalimaailman koordinaatteiksi yhdessä erillisen georeferenssitiedoston kanssa.

## HDR-tiedostomuoto

HDR-tiedostot tallennetaan ASCII-tekstitiedostomuodossa. Se sisältää joukon merkintöjä, joissa jokainen merkintä kuvaa tietyn kuvan määritteen. Jokaisella HDR-tiedostolla on seuraava muoto:

```
<keyword> <value>
```

`<keyword> ` - Se osoittaa määritetyn määritteen
`<value> ` - Se on arvo, johon määrite asetetaan

Otsikon merkintöjen järjestystä ei ole rajoitettu. Jokaisen merkinnän on kuitenkin oltava rivin erillisellä rivillä, jotta se noudattaa HDR-lukijoiden käyttämää jäsennysmenetelmää.

## Yhteenveto HDR-tiedostossa käytetyistä avainsanoista

|Avainsana |Hyväksyttävä arvo |Oletus|
---|---|---|
|nrows |mikä tahansa kokonaisluku > 0| ei mitään
|ncols |mikä tahansa kokonaisluku > 0| ei mitään
|nbands |mikä tahansa kokonaisluku > 0| 1
|nbittiä |1, 4, 8, 16, 32| 8
|byteorder| I = Intel;M = Motorola |sama kuin isäntäkone|
|layout| bil, bip, bsq| bil|
|ohita tavua| mikä tahansa kokonaisluku ≥ 0| 0
|ulxmap |mikä tahansa reaaliluku| 0|
|ulymap |mikä tahansa reaaliluku |nrows - 1|
|xdim |mikä tahansa reaaliluku| 1
|ydim |mikä tahansa reaaliluku| 1
|kaistan tavut |mikä tahansa kokonaisluku > 0| pienin kokonaisluku ≥ (ncols x nbits) / 8|
|tavuja yhteensä |mikä tahansa kokonaisluku > 0| bil:lle: nbands x bandrowbytes;for bip: pienin kokonaisluku ≥ (ncols x nbands x nbits) / 8|
|kaistan välitavua |mikä tahansa kokonaisluku ≥ 0| 0|

## Viitteet

* [HRD-tiedostomuoto - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)


