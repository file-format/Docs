{
  "date": "2019-10-11",
  "keywords": [
"kmz failą",
"kas yra kmz failas",
"failą",
"kmz pavyzdys",
"kmz failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "KMZ – KML ZIP failo formatas",
  "description": "Sužinokite apie KMZ failo formatą ir API, kurios gali kurti ir atidaryti KMZ failus.",
  "linktitle": "KMZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-km-ltz"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra KMZ failas?

KMZ (KML Zipped) failas yra suglaudinto [KML](/gis/kml/) failo, kuriame yra geoerdvinės informacijos, matomos GIS programose, pvz., Google Earth, atvaizdas. Informacija apie vietos žymes faile pateikiama kaip platuma ir ilguma kartu su pasirinktiniu pavadinimu. Vieną supakuotą KMZ failą galima lengvai bendrinti su kitais vartotojais. KMZ failuose taip pat gali būti 3D modelio duomenų, skirtų modelio geografiniam vaizdavimui. KMZ failą galima atidaryti Google žemėlapiuose išsaugant failą internetinėje vietoje ir įvedus URL Google žemėlapių paieškos laukelyje.

## Failo struktūra ##

The contents of a MKZ file consist of a main KML file and zero or more associated files. It can be extracted using standard decompression utility like WinZIP. KMZ file format is also compressed to an archive with compression ratio of 10:1. Galite eksportuoti duomenis iš Google žemės, pavyzdžiui, programų, tiesiai į KMZ failo formatą. Pagrindinis KML failas pavadintas **doc.kml**. Pakuojant KMZ failą, prie jo galima pridėti daugiau nei vieną KML failą, tačiau tai nebus naudinga, nes atidarydama KMZ failą Google Earth ieško pirmojo KML failo ir jį nuskaito. Jis nepaiso kitų archyve rastų KML failų. Norint įsitikinti, kad Google žemė nuskaito norimą KML failą, į KMZ failą rekomenduojama įdėti tik vieną KML failą.

Vaizdai, modeliai, tekstūros, garso failai ir kiti ištekliai, nurodyti doc.kml faile, dedami į kitą pagrindinio aplanko poaplankį. Tai taip pat gali būti sudėtinga, atsižvelgiant į palaikomųjų failų skaičių. Nuorodos į šiuos sudedamuosius išteklius gali būti santykinės arba absoliučiomis nuorodomis.

### Santykinė nuoroda ###

Kai ištekliai dedami šalia pagrindinio doc.kml pagrindinio aplanko poaplankyje, santykinė nuoroda gali nurodyti šiuos pagalbinius failus, kaip parodyta toliau pateiktame pavyzdyje (tik piktogramai).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Absoliuti nuoroda ###

Ištekliai taip pat gali būti visiškai nurodyti. Absoliučiose nuorodose yra visas susieto failo URL. Kai failai paskelbiami centriniame serveryje, absoliuti nuoroda užtikrina, kad jos išliktų nedviprasmiškos, palyginti su santykinėmis nuorodomis. Nerekomenduojama visiškai nurodyti vietinių failų, nes šios nuorodos nutrūks, kai failai bus perkelti į naują sistemą. Absoliučios nuorodos pavyzdys yra toks:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Taip pat žiūrėkite ##

* [GeoJSON](/gis/geojson/)


## Nuorodos Nr.

* [Google Earth ir KMZ failai](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)


