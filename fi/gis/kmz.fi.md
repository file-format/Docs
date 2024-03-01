{
  "date": "2019-10-11",
  "keywords": [
"kmz tiedosto",
"mikä on kmz-tiedosto",
"tiedosto",
"kmz esimerkki",
"kmz tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "KMZ - KML-zip-tiedostomuoto",
  "description": "Lisätietoja KMZ-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata KMZ-tiedostoja.",
  "linktitle": "KMZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-km-fiz"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on KMZ-tiedosto?

KMZ (KML Zipped) -tiedosto on esitys pakatusta [KML](/gis/kml/)-tiedostosta, joka sisältää paikkatietoa, jota voidaan tarkastella GIS-sovelluksissa, kuten Google Earthissa. Paikkamerkitsimien tiedot esitetään tiedostossa leveys- ja pituusasteina sekä mukautettu nimi. Yksittäinen pakattu KMZ-tiedosto voidaan jakaa helposti muiden käyttäjien kanssa. KMZ-tiedostot voivat sisältää myös 3D-mallitietoja mallin maantieteellistä esittämistä varten. KMZ-tiedosto voidaan avata Google Mapsissa tallentamalla tiedosto online-sijaintiin ja kirjoittamalla URL-osoite Google Mapsin hakukenttään.

## Tiedostorakenne ##

The contents of a MKZ file consist of a main KML file and zero or more associated files. It can be extracted using standard decompression utility like WinZIP. KMZ file format is also compressed to an archive with compression ratio of 10:1. Voit viedä tietoja Google Earthista, kuten sovelluksista, suoraan KMZ-tiedostomuotoon. Pääasiallisen KML-tiedoston nimi on **doc.kml**. KMZ-tiedoston pakkaamisen aikana siihen voidaan lisätä useita KML-tiedostoja, mutta tästä ei ole hyötyä, koska Google Earth etsii ensimmäistä KML-tiedostoa KMZ-tiedostoa avattaessa ja lukee sen. Se ohittaa kaikki muut arkistosta löytyneet KML-tiedostot. Varmistaaksesi, että Google Earth lukee halutun KML-tiedoston, vain yksi KML-tiedosto on suositeltavaa sijoittaa KMZ-tiedoston sisään.

Kuvat, mallit, tekstuurit, äänitiedostot ja muut resurssit, joihin doc.kml-tiedostossa viitataan, sijoitetaan toiseen alikansioon pääkansion sisällä. Tämä voi myös olla monimutkainen riippuen tukitiedostojen määrästä. Linkit näihin resursseihin voivat olla suhteellisia tai absoluuttisen viittauksen kautta.

### Suhteellinen viittaus ###

Kun resurssit sijoitetaan pääasiakirjan doc.kml viereen pääkansion alikansioon, suhteellinen viittaus voi viitata näihin tukitiedostoihin seuraavan esimerkin mukaisesti (vain kuvake).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Absoluuttinen viittaus ###

Resursseihin voi myös ehdottomasti viitata. Absoluuttiset viittaukset sisältävät linkitetyn tiedoston täydellisen URL-osoitteen. Kun tiedostot lähetetään keskuspalvelimelle, absoluuttinen viittaus varmistaa, että ne pysyvät yksiselitteisinä verrattuna suhteelliseen viittaukseen. Paikallisiin tiedostoihin ei suositella viittaamista ehdottomasti, koska nämä linkit katkeavat, kun tiedostot siirretään uuteen järjestelmään. Esimerkki absoluuttisesta viittauksesta on seuraava:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Katso myös ##

* [GeoJSON](/gis/geojson/)


## Viitteet ##

* [Google Earth- ja KMZ-tiedostot](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)


