{
  "date": "2019-10-11",
  "keywords": [
"pottitiedosto",
"pot-tiedostomuoto",
"mikä on pot-tiedosto",
"tiedosto",
"potti esimerkki",
"pot tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "POT - Microsoft PowerPOint Template File Format",
  "description": "Learn about POT file format and APIs that can create and open POT files.",
  "linktitle": "POT",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pot"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on POT-tiedosto?

.POT-tunnisteella varustetut tiedostot edustavat PowerPoint 97-2003 -versioilla luotuja Microsoft PowerPoint -mallitiedostoja. Näillä Microsoft PowerPointin versioilla luodut tiedostot ovat binäärimuodossa verrattuna Office OpenXML -tiedostomuodoissa PowerPointin uudempia versioita käyttäviin tiedostoihin. Luotuja tiedostoja voidaan siis käyttää luomaan esityksiä, joilla on sama asettelu ja muut asetukset, joita tarvitaan uusiin tiedostoihin. Nämä asetukset voivat sisältää tyylejä, taustoja, väripalettia, fontteja ja oletusasetuksia. Tällaisia tiedostoja luodaan, jotta voidaan luoda valmiita mallitiedostoja virallista käyttöä varten.

## Tiedostomuodon tiedot ##

File format specifications for POT file format are not available individually by Microsoft. However, the template format is the same as that of the binary [PPT](/presentation/ppt/) file format and can be opened in MS PowerPoint for editing purpose. A POT file is identified by HEX identifier as follow:

```
D0 CF 11 E0 A1 B1 1A E1 00 00 00 00
```

POT-tiedostomuotoon liittyvät MIME-tyypit ovat:

* application/vnd.ms-powerpoint [virallinen]

* sovellus/mspowerpoint

* Application/x-mspowerpoint

* sovellus/powerpoint

* sovellus/x-powerpoint

* application/x-dos_ms_powerpnt

* sovellus/potti

* Application/x-soffic


## Viitteet ##

* [PPT-tiedostomuodon tiedot](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)

* [[MS-OSHARED]: Officen yleiset tietotyypit ja objektirakenteet](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)

* [[MS-OFFCRYPTO] - Office Document Cryptography Structure](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)

* [PowerPoint-tiedostomuodot](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)


