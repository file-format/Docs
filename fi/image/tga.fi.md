{
  "date": "2019-10-11",
  "keywords": [
"tga tiedosto",
"tga tiedostomuoto",
"mikä on tga-tiedosto",
"tiedosto",
"tga esimerkki",
"tga tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TGA-tiedostomuoto - TARGA-graafinen kuvatiedosto",
  "description": "Opi TGA-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata TGA-tiedostoja.",
  "linktitle": "TGA",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-tg-fia"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on TGA-tiedosto?

Tiedosto, jonka laajennus on .tga, on rasterigrafiikkamuoto, ja sen on luonut Truevision Inc. Se on suunniteltu TARGA (Truevision Advanced Raster Adapter) -korteille ja tarjosi Highcolor/truecolor-näyttötuen IBM-yhteensopiville tietokoneille. Se tukee 8, 16, 24 ja 32 bittiä pikseliä kohden ja 8-bittistä alfakanavaa. Se tukee myös häviötöntä RLE-pakkausta, jota voidaan käyttää kuvan koon pienentämiseen. Digitaaliset valokuvat ja tekstuurit käyttävät TGA-kuvamuotoa.

## Lyhyt historia

TGA-tiedostomuodon muodosti vuonna 1984 AT&T EPICenter (myöhemmin purettu ja muodostettu itsenäiseksi kokonaisuudeksi nimeltä Truevision), joka työskenteli AT&T:n värikehyspuskureille kehittämien uusien teknologioiden markkinoinnissa. EPICenter työsti jo kahta ensimmäistä korttiaan, VDA (Video Display Adapter) ja ICB (image capture board), joiden kahden tiedostotyypin, .vda ja .icb, työstö oli jo käynnissä. Nämä tiedostomuodot kodifioitiin ja vähemmän laaja-alainen tiedostomuoto TGA otettiin käyttöön. TGA oli laajennus jo käytössä olleelle ja tarjosi tietoja, kuten leveyden, korkeuden, pikselin syvyyden, liittyvän värikartan ja kuvan alkuperän.

TGA:n 2.0-versio, joka julkaistiin vuonna 1989, sisälsi useita parannettuja ominaisuuksia, kuten:

 * Pikkukuvat
 * Alfa kanava
 * Gamma-arvo
 * Textual Metadata

TGA:n 2.0-version tärkeimpiä avustajia ovat muun muassa Truevisionin Shawn Steiner, Kevin Fiedly ja David Spoelstra.

## TGA TARGA -tiedostomuodon tekniset tiedot

TGA-tiedosto koostuu kahdesta pääosasta:

 * Otsikko
 * Väripikselin tiedot

Kaikki arvot TGA-tiedostossa ovat littl-endian muotomäärittelyjen mukaisesti.

### TGA-otsikko

TGA-tiedoston otsikko koostuu seuraavista viidestä kentästä.

|Kentän nro|Pituus |Kentän nimi |Kuvaus|
---|---|---|---|
|1| 1 tavu |ID-pituus| Kuvatunnuskentän pituus (0-255)|
|2| 1 tavu |Värikartan tyyppi| Onko värikartta mukana (0 - tarkoittaa, että tämä kuva ei sisällä värikarttatietoja. 1 - osoittaa, että värikartta sisältyy tähän kuvaan.)|
|3| 1 tavu |Kuvatyyppi| Pakkaus ja värityypit (0 - ei kuvatietoja. 1 - pakkaamaton, värikartoitettu kuva, 2 - pakkaamaton, todellinen värikuva, 9 - ajonpituuskoodattu, värikartoitettu kuva, 11 - ajonpituuskoodattu, mustavalkoinen kuva )|
|4| 5 tavua |Värikartan määrittely| Kuvaa värikartan|
|5| 10 tavua |Kuvamääritys| Kuvan mitat ja muoto|

### Kuva- ja värikarttatiedot

|Kenttä nro. |Pituus |Kenttä |Kuvaus|
---|---|---|---|
|6 |Kuvan ID pituuskentästä| Kuvan tunnus| Valinnainen kenttä, joka sisältää tunnistetiedot|
|7 |Värikartan määrittelykentästä| Värikarttatiedot| Hakutaulukko, joka sisältää värikarttatiedot|
|8 |Kuvan määrittelykentästä| Kuvatiedot| Tallennettu kuvakuvaajan mukaan|

### Kehittäjäalue (valinnainen)

TGA-versio 2.0 tukee lisäparannuksia/lisäominaisuuksia, joihin monet kehittäjät halusivat tallentaa lisää tietoa. Tiedot ovat valinnaisia, joten jos TGA-dekooderi ei pysty tulkitsemaan sitä, se jätetään huomioimatta.

### Laajennusalue (valinnainen)

|Kenttä nro| Pituus| Kenttä |Kuvaus|
---|---|---|---|
|10| 2 tavua |Laajennuksen koko |Laajennusalueen koko tavuina, aina 495|
|11| 41 tavua| Tekijän nimi | Tekijän nimi. Jos sitä ei käytetä, tavuiksi tulee asettaa NULL (\0) tai välilyöntejä|
|12| 324 tavua| Tekijän kommentti| Kommentti, joka on järjestetty neljään riviin, joista jokainen koostuu 80 merkistä plus NULL|
|13| 12 tavua| Päivämäärä/aikaleima |Päivämäärä ja aika, jolloin kuva luotiin|
|14| 41 tavua| Työtunnus||
|15| 6 tavua| Työaika| Tunnit, minuutit ja sekunnit tiedoston luomiseen (laskutus jne.)|
|16| 41 tavua| Software ID |Sovellus, joka loi tiedoston.|
|17| 3 tavua| Ohjelmistoversio||
|18| 4 tavua| Avaimen väri||
|19| 4 tavua| Pikselin kuvasuhde||
|20| 4 tavua| Gamma-arvo||
|21| 4 tavua| Color correction offset |Tavujen määrä tiedoston alusta värinkorjaustaulukkoon, jos sellainen on|
|22| 4 tavua| Postimerkki | Tavujen määrä tiedoston alusta postimerkkikuvaan, jos sellainen on|
|23| 4 tavua| Skannausviivan siirtymä| Tavujen määrä tiedoston alusta tarkistusrivitaulukkoon, jos sellainen on|
|24| 1 tavu| Attribuuttien tyyppi| Määrittää alfakanavan|

### Tiedoston alatunniste (valinnainen)

Tiedoston viimeiset 26 tavua edustavat alatunnistetta, mikä tarkoittaa, että se on todennäköisesti TGA version 2 tiedosto.

|Kenttä nro| Pituus| Kenttä| Kuvaus|
---|---|---|---|
|28| 4 tavua| Jatkeen offset| Poikkeama tavuina tiedoston alusta|
|29| 4 tavua| Kehittäjäalueen offset| Poikkeama tavuina tiedoston alusta|
|30| 16 tavua| Allekirjoitus| Sisältää TRUEVISION-XFILE|
|31| 1 tavu| | Sisältää .|
|32| 1 tavu| | Sisältää NULL|


## Viitteet

 * [TGA 2.0 File Format Specifications](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
 * [TGA Wikipediasta](https://en.wikipedia.org/wiki/Truevision_TGA)

