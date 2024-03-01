{
  "date": "2020-03-16",
  "keywords": [
"DWF",
"Tiedosto muoto",
"Avata",
"Lukea",
"Luoda",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Learn about DWF file format and APIs that can create and open DWF files.",
  "title": "DWF File Format",
  "linktitle": "DWF",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dwf"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on DWF-tiedosto?

Design Web Format (DWF) edustaa 2D/3D-piirustusta pakatussa muodossa suunnittelutiedostojen katseluun, tarkistamiseen tai tulostamiseen. Se sisältää grafiikkaa ja tekstiä osana suunnittelutietoja ja pienentää tiedoston kokoa sen pakatun muodon vuoksi. Pienempi tiedostokoko tekee monipuolisen suunnittelutiedon jakelusta ja viestimisestä tehokasta. DWF ei vaadi vastaanottajan tietävän alkuperäisen piirustuksen luoneen CAD-ohjelmiston käytöstä. DWF-tiedostomuodon sisältö voi olla yksinkertaista ja sisältää vain yhden arkin tai tarpeeksi monimutkainen kirjasimia, värejä ja kuvia varten.

## Lyhyt historia ##

Autodesk esitteli DWF-tiedostomuodon vuonna 1995 osana Netscape Navigation -laajennusta, WHIP. Muoto kehittyi vain 2D-muodosta sisältämään 3D-sisällön ajan myötä. Monet kolmannen osapuolen sovellukset käyttävät myös tätä muotoa.

## DWF-tiedostomuoto ##

DWF on avoin, suojattu muoto, joka on suunniteltu erityisesti monipuolisten suunnittelutietojen jakamiseen. Se on riippumaton alkuperäisestä sovellusohjelmistosta, laitteistosta ja käyttöjärjestelmästä, jota käytetään suunnittelutietojen luomiseen. Näin tiimin jäsenet, jotka eivät käytä CAD-sovelluksia, voivat osallistua digitaalisiin prosesseihin tarkastelemalla rakennus-, GIS- tai tuotesuunnitelmia. DWF-tiedostoarkisto koostuu useista XML- ja binääritiedostoista, jotka on pakattu yhteen pakattuun arkistoon, joka on luotu [ZIP](/compression/zip/)-pakkauksella. Voit nimetä DWF-tiedostotunnisteen uudelleen ZIP:ksi ja tarkastella tiedoston sisältöä. DWF-paketti voi sisältää monenlaista suunnittelutietoa, kuten 2D-grafiikkaa, 3D-grafiikkaa, pakettien ja osien metatietoja ja muita resurssitiedostoja.

**DWF metadata files** – XML files that contain information pertaining to metadata and structure (author, title, creation time, section dependencies, section ordering, resource file descriptions, roles, mimetypes, etc.) and pertaining to the section (page information, design metadata, etc.).  The structural metadata is used to create logical objects (collections of files to represent a part or page, etc.).

**Resurssitiedostot** – media- tai muut sisältötiedostot, joihin viitataan paketin/osion metatiedoista ja jotka ovat yleensä suunnittelutietojen esityksiä eri muodoissa (ZGL, W2D, [JPG](/image/jpeg/), [PNG](/image/png/), AVI, XML, [TXT](/word-processing/txt/), [DOC](/word-processing/doc/) jne.)

### Tiedostomuodon tiedot ###

DWF-tiedostot on järjestetty kolmeen pääosaan alla olevan kuvan mukaisesti.

* Tiedoston tunnisteotsikko

* Tiedoston tietolohko

* Tiedoston lopetustraileri


#### Tiedostotunnisteen otsikko ####

The file identifier header allows for identification of DWF files by applications. It also identifies which version of DWF specifications was used for encoding the file. It is a 12 byte header that is arranged as follow:


|tavu|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Merkki|(|D|W|F|(välilyönti)|V|0|0|.|3|0|)

Tässä on yhteenveto tästä taulukosta:

* Otsikon kuusi ensimmäistä tavua edustavat aina ASCII-merkkejä "(DWF V"

* Seuraavat 5 tavua sisältävät tietoja versionumerosta, esim. "00.30" ja muodon pää- ja sivuversion arvot


DWF-tiedoston luovien sovellusten tulee määrittää pienin mahdollinen versionumero, jota lukijasovelluksen on tuettava voidakseen käyttää tietoja oikein.

#### Tiedoston tietolohko ####

Tiedostodatalohko alkaa DWF-tiedoston 13. tavusta ja on sarja opkoodi- ja operandipareja, kuten seuraavassa taulukossa.

|Kenttä 1|Kenttä 2|Kenttä 3|Kenttä 4|Kenttä 5|Kenttä 5
--- | --- |--- | --- |--- | --- |
|opcode|operand|opcode|operand|opcode|operand

DWF-tiedosto voi sisältää opkoodi-operandi-pareja luettavissa ASCII-koodina sekä koodibinaarina tai näiden yhdistelmänä. Kaikilla DWF-operaatioilla on luettavissa oleva ASCII-operaatiokoodi/operandimuoto, ja useimmilla operaatioilla on myös koodattu binaarinen opkoodi/operandimuoto. Opcodes ovat yksitavuisia, mikä mahdollistaa yli 200 toimintoa. Laajennettu ASCII ja laajennettu binääri ovat poikkeustapauksia. Opcodes-arvot voivat vaihdella välillä 0-255 joitakin poikkeuksia lukuun ottamatta. Lukuun ottamatta kahta erikoistyyppistä opkoodia, laajennettu ASCII ja laajennettu binääri, tiedostonlukijan on osattava laskea operandin pituus.

##### Kielletyt opkoodit #####

Seuraavien ASCII-esityksiä ei voida käyttää opkoodeina:

Seuraavia ASCII-esityksiä ei voida käyttää opkoodeina:

* Välilyönti (0x20)

* Tab (0x09)

* Tavuviiva (0x2D)

* ASCII-numerot 0-9 (0x30 - 0x39)

* Vaunu paluu (0x0D)

* Rivinsyöttö (0x0A)

* Yksi lainausmerkki (0x27)

* Tuplalainausmerkki (0x22)

* Jakso (0x2E)

* Sulkumerkit (0x28 ja 0x29)

* Kiharat hakasulkeet (0x7B ja 0x7D)

* Hakasulkeet (0x5B ja 0x5D)

* Kenoviiva (0x5C)


#### Tiedoston lopetustraileri ####

DWF:n tiedoston lopetustraileri on yksinkertaisesti erityinen opkoodi, joka osoittaa tiedoston lopun. Jotkut sovellukset voivat tallentaa muita kuin DWF-tietoja lopetuskoodin jälkeen. Traileri on seuraavanlainen:


|tavu|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Merkki|(|E|n|d|0|f|D|W|F|)

## Viitteet ##

* [DWF - Wikipedia](https://en.wikipedia.org/wiki/Design_Web_Format)

* [WHIP-tietomuoto](http://paulbourke.net/dataformats/whip/)

* [https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1](https://learn.microsoft.com/en-us/archive/blogs /opc/adventures-in-packaging-episode-1)


