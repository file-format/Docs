{
  "date": "2021-02-25",
  "keywords": [
"ttc tiedosto",
"ttc tiedostomuoto",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "TTC - TrueType-kokoelman tiedostomuoto",
  "description": "TrueType Collection (TTC) -tiedosto yhdistää useita fontteja yhdeksi tiedostoksi. Sekä Apple että Microsoft käyttivät TTF:ää Mac- ja Windows-käyttöjärjestelmissä.",
  "linktitle": "TTC",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-tt-fic"
}
},
  "lastmod": "2021-02-25"
}

## Mikä on TTC-tiedosto?
TTC on lyhenne TrueType Collection on True Type -muodon laajennus. TTC-tiedosto voi yhdistää useita fonttitiedostoja siihen. Nämä tiedostot ovat hyödyllisiä useiden kirjasimien yhdistämiseen, joilla on useita yhteisiä kuvioita. Ennen Windows 2000:ta TTC-tiedostoja käytettiin kiinan-, japanin- ja koreankielisissä Windows-versioissa, mutta myöhemmin tuki oli saatavilla kaikille alueille.


## Fonttikokoelmatiedoston rakenne 
TTC-tiedosto koostuu TTC-otsikkotaulukosta, taulukkohakemistoista ja useista OpenType-taulukoista. TTC-otsikko on löydettävä tiedoston alusta. Jokaiselle kirjasimelle on oltava täydellinen taulukkohakemisto. TableDirectory-muodon tulee olla samanlainen kuin ei-kokoelmatiedostossa. Taulukkomäärät kaikissa TTC-tiedoston hakemistoissa lasketaan TTC-tiedoston alusta.
TTC-tiedoston taulukoihin viitataan niiden vastaavien fonttien taulukkohakemiston kautta. Muutaman OpenType-taulukon on näytettävä useita kertoja, kerran jokaista TTC:hen lisättyä fonttia kohti. Kun taas muut taulukot voivat jakaa useat kirjasimet TTC-tiedostossa.

### TTC-otsikko
TTC Header -taulukosta on tähän mennessä saatavilla kaksi versiota:
- Versiota 1.0 käytetään TTC-tiedostoille ilman digitaalista allekirjoitusta.
- Versiota 2.0 voidaan käyttää TTC-tiedostoille digitaalisella allekirjoituksella tai ilman.
Tässä ovat molempien versioiden TTC-otsikkotaulukot:

**TTC-otsikon versio 1.0:**

|Tyyppi|Nimi|Kuvaus|
---|---|---|
|TAG|ttcTag|Fonttikokoelman tunnusmerkkijono: 'ttcf' (käytetään kirjasimille, joissa on CFF- tai CFF2-ääriviivat sekä TrueType-ääriviivat)|
|uint16|majorVersion|TTC-otsikon pääversio, = 1.|
|uint16|minorVersion|TTC-otsikon sivuversio, = 0.|
|uint32|numFonts|TTC:n fonttien määrä|
|Offset32|tableDirectoryOffsets[numFonts]|Jokaisen kirjasimen TableDirectory-siirtymien joukko tiedoston alusta alkaen|

**TTC-otsikon versio 2.0:**

|Tyyppi|Nimi|Kuvaus|
---|---|---|
|TAG|ttcTag |Fonttikokoelman tunnusmerkkijono: 'ttcf'|
|uint16| majorVersion |TTC-otsikon pääversio, = 2.|
|uint16| minorVersion |TTC-otsikon sivuversio, = 0.|
|uint32| numFonts |TTC:n fonttien määrä|
|Offset32| tableDirectoryOffsets[numFonts] |TableDirectory-siirtymien joukko jokaiselle kirjasimelle tiedoston alusta alkaen|
|uint32| dsigTag |Tagi, joka ilmaisee, että DSIG-taulukko on olemassa, 0x44534947 ('DSIG') (nolla, jos ei allekirjoitusta)|
|uint32| dsigLength |DSIG-taulukon pituus (tavuina) (nolla, jos ei allekirjoitusta)|
|uint32| dsigOffset |DSIG-taulukon siirtymä (tavuina) TTC-tiedoston alusta (nolla, jos ei allekirjoitusta)|

## Viitteet
 * [OpenType-fonttitiedosto](https://learn.microsoft.com/en-us/typography/opentype/spec/otff)
 * [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

