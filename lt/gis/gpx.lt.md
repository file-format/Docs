{
  "date": "2019-10-11",
  "keywords": [
"gpx failą",
"kas yra gpx failas",
"failą",
"gpx pavyzdys",
"gpx failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GPX – GPX Exchange failo formatas",
  "description": "Sužinokite apie GPX failo formatą ir API, kurios gali kurti ir atidaryti GPX failus.",
  "linktitle": "GPX",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gp-ltx"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra GPX failas?

Failai su GPX plėtiniu yra GPS Exchange formatas, skirtas keistis GPS duomenimis tarp programų ir interneto paslaugų internete. Tai lengvas XML failo formatas, kuriame yra GPS duomenų, ty kelio taškai, maršrutai ir takeliai, kuriuos turi importuoti ir raudonos spalvos kelios programos. GPX failo formatas yra atviras, jį palaiko įvairios programos ir GPS įrenginiai. GPS duomenis iš tokių failų galima įkelti ir rodyti žemėlapių programose geografiniais tikslais.

## GPX failo formatas ##

GPX failą sudaro platumos ir ilgumos vietos duomenys, aukščio reikšmės ir kita galbūt kita aprašomoji informacija. Vietos duomenys išreiškiami dešimtainiais laipsniais, o aukštis – metrais. GPX failo laikas nurodomas koordinuotu pasauliniu laiku (UTC), naudojant ISO 8601 formatą. GPX failo naudojimo pranašumai yra šie:

* GPX leidžia keistis duomenimis su augančiu Windows, MacOS, Linux, Palm ir PocketPC programų sąrašu.

* GPX galima paversti kitais failų formatais naudojant paprastą tinklalapį arba konvertavimo programą.

* GPX yra pagrįstas XML standartu, todėl daugelis naujų jūsų naudojamų programų (pvz., Microsoft Excel) gali nuskaityti GPX failus.

* GPX leidžia kiekvienam žiniatinklio naudotojui lengvai kurti naujas funkcijas, kurios iš karto veiks su jūsų mėgstamomis programomis.


[GPX Schema](https://www.topografix.com/GPX/1/1/gpx.xsd) rodomas GPX failo formato vaizdas.

### Esminiai duomenys ###

Toliau pateikiami pagrindiniai duomenys, kurie yra GPX failo, skirto GPS duomenims atvaizduoti, dalis.

* **Kelio taškai**: maršruto taškas yra WGS84 (GPS) taško koordinatės ir atspindi OGR tipo wkbPoint savybių sluoksnį.

* **Maršrutai**: atstovauja OGR tipo wkbLineString funkcijų sluoksniui. Jame yra kelio taškų, kurie yra tarpiniai taškai, rodantys posūkio ar etapo taškus, vedančius į tikslą, sąrašas

* **Tracks**: takeliai yra OGR tipo wkbMultiLineString funkcijų sluoksnis. Jis sudarytas iš bent vieno segmento, kuriame yra kelio taškai sutvarkytame taškų, apibūdinančių kelią, sąraše. Jį sudaro maršruto taškų, kurie reiškia nenutrūkstamą GPS sekimą, sąrašas.


### GPX pavyzdinis failas ###

Toliau pateiktame GPX faile rodomas GPS duomenų išdėstymas GPX faile ir gali būti geras supratimas apie GPX failo turinį.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## Nuorodos Nr.

* [GPX failo formatas](https://www.topografix.com/gpx.asp)

* [GPX – Vikipedija](https://en.wikipedia.org/wiki/GPS_Exchange_Format)


