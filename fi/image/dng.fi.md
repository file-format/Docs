{
  "date": "2019-10-11",
  "keywords": [
"dng tiedosto",
"dng tiedostomuoto",
"mikä on dng-tiedosto",
"tiedosto",
"dng esimerkki",
"dng tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DNG - Digitaalikameran kuvatiedostomuoto",
  "description": "Opi DNG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DNG-tiedostoja.",
  "linktitle": "DNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dn-fig"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on DNG-tiedosto?

DNG is a digital camera image format used for the storage of raw files. It has been developed by Adobe in September 2004. Se on pohjimmiltaan kehitetty digitaaliseen valokuvaukseen. DNG on [TIFF](/image/tiff/)/EP-standardimuodon laajennus ja käyttää metatietoja merkittävästi. Käsitelläkseen digitaalikameroiden raakadataa joustavuuden ja taiteellisen ohjauksen avulla valokuvaajat valitsevat kameran raakatiedostot. JPEG- ja TIFF-muodot tallentavat kameran käsittelemät kuvat, joten näissä muodoissa ei ole paljon muokkaustilaa.

## DNG-tiedostomuodon historia ja versiot

Till now there have been 5 versions of DNG specification so far. Version 1.0.0.0 was launched in September 2004 along with the release of "2.3" (ACR and DNG Converter). In February 2005 version 1.1.0.0 was published.  In May 2008 version 1.2.0.0 was released and was used in "4.4". Version 1.3.0.0 was published in June 2009. Versio 1.4.0.0 ilmestyi vuonna 2012.

## DNG-tiedostomuoto

Kameran raakatiedostot tallentavat käsittelemättömän tai vähän prosessoitua dataa suoraan anturista. Koska ne ovat samanlaisia kuin filminegatiivit, kameran raaka-muodot tunnetaan myös nimellä digitaaliset negatiivit. Raakaformaattien etu on loppukäyttäjän lisääntynyt taiteellinen hallinta. Käyttäjä voi säätää erilaisia parametrialueita vaatimusten mukaan, kuten valkotasapaino, sävykartoitus, kohinanvaimennus, teroitus ja niin edelleen. Toisaalta kameran raakatiedosto on käsiteltävä mihin tahansa käyttöön minkä tahansa ohjelmiston tai muuntimen kautta.

Koska kameran raakatiedostoille ei ollut saatavilla vakiomuotoa, se aiheutti useita ongelmia loppukäyttäjälle. Adobe käsitteli nämä ongelmat ja määritti ei-omistusoikeudellisen muodon camera raw -tiedostoille. Muoto tunnetaan nimellä Digital Negative tai DNG. DNG:tä voidaan käyttää monenlaisissa laitteistoissa ja ohjelmistoissa raakatiedostojen käsittelyyn. Lisäksi DNG:tä voidaan käyttää myös välimuotona sellaisten kuvien tallentamiseen, jotka on otettu alun perin kameroilla, joilla on omat raaka-formaatit.

### DNG-tiedostomuodon tekniset tiedot

Tässä osiossa kuvaamme DNG-muotoa TIFF 6.0:n laajennuksena.

* **Tiedostolaajennukset**: DNG käyttää ".DNG"- tai ".TIF"-laajennuksia.

* **SubIFD-puut**: DNG ei tue SubIFD-ketjuja, sen sijaan DNG suosittelee SubIFD-puiden käyttöä TIFF-EP-spesifikaatioiden mukaisesti. Paras laatu ja resoluutio voivat käyttää NewSubFileType-arvoa 0, kun taas huonolaatuisten pikkukuvien NewSubFileType on yhtä suuri kuin 1. On myös suositeltavaa, vaikka ei vaadita, että ensimmäisellä IFD:llä on oltava heikkolaatuinen tai huonolaatuinen pikkukuva.

* **Tavujärjestys**: DNG-lukijoiden on tuettava tavujärjestystä, myös tietyn kameramallin tiedostoille.

* **Maitetut pikselit**: Useimmat kameran anturit laskevat täysin peitetyt pikselit anturin reunassa mustan koodauksen avulla. Nämä pikselit voidaan joko sisällyttää tai leikata ennen kuvan tallentamista DNG-muotoon. Jos peitettyjä pikseleitä ei leikata, näiden pikselien alue on mainittava ActiveArea-tunnisteessa. Näistä pikseleistä kerättyjä tietoja mustan koodaustasosta tulee käyttää joko ennen raakatietojen tallentamista tai ne voidaan sisällyttää DNG-tiedostoon, jossa määritetään mustan taso.

* **Vialliset pikselit**: Ennen kuin käsittelet raakadataa DNG-muodossa, vialliset pikselit tulee sulkea pois.

* **Metatiedot**: Metatiedot voidaan sisällyttää DNG:hen jollakin seuraavista tavoista:  

** Käyttämällä TIFF-EP- tai EXIF-metatietotunnisteita
** IPTC-metatietotunnisteen (33723) kautta
** XMP-metatietotunnisteen käyttäminen (700)
* **Suojatut tiedot**: Tavallisesti toimittajat sisällyttävät omistusoikeudelliset tiedot raakatiedostoon omien muuntimiensa käyttöön. DNG tallentaa omat tietonsa yksityisiin tunnisteisiin, yksityisiin IFD-levyihin ja yksityiseen MakerNoteen. Toimittajien on käytettävä DNGPrivateData- ja MakerNoteSafety-tageja varmistaakseen, että DNG-tiedostoja muokkaavat sovellukset säilyttävät nämä omistusoikeudelliset tiedot.


Seuraavassa on joitain tärkeitä TIFF-tunnisteiden rajoituksia ja laajennuksia.

**BitsPerSample**

8-32 bittiä/näyte on tuettu. Jokaisella näytteellä on oltava sama syvyyden, kun SamplesPerPixel ei ole yhtä suuri kuin 1. Mutta jos BitsPerSample ei ole 8 tai 16 tai 32, bitit on pakattava tavuiksi käyttämällä TIFF:n oletusarvoista FillOrder-arvoa 1 (big-endian).

**Puristus**

Kahta pakkaustunnisteen arvoa tuetaan:

* Arvo # 1: Pakkaamaton data.

* Arvo # 7: JPEG-pakattu data, joko perustason DCT JPEG tai häviötön JPEG-pakkaus.


**Photometric Interpretation**

Seuraavia arvoja tuetaan vain pikkukuva- ja esikatselu-IFD:ille:

* 1 = BlackIsZero. Oletetaan olevan gamma 2.2 -väriavaruudessa.

* 2 = RGB. Oletetaan olevan sRGB-väriavaruudessa.

* 6 = YCbCr. Käytetään JPEG-koodattuihin esikatselukuviin.


Seuraavia arvoja tuetaan raaka-IFD:lle, ja niiden oletetaan olevan kameran alkuperäinen väriavaruus:

* 32803 # CFA (Color Filter Array).

* 34892 # LinearRaw.


**Suuntautuminen**

Orientaatiotagia käytetään tiedostoselaimissa, jotta ne voivat pyörittää DNG-tiedostoja häviöttömästi. DNG-lukijoiden on tuettava kaikkia mahdollisia suuntauksia, mukaan lukien peilatut suunnat.

## Ominaisuudet DNG:n uusimmassa versiossa

DNG-versiossa 1.4 lokakuuta 2012 on seuraavat lisäominaisuudet.

* Oletuskäyttäjän rajaus

* Läpinäkyvyys

* liukuluku (HDR)

* Häviöinen pakkaus

* Välityspalvelimet


## Viitteet ##

* [DNG-tiedot – Adobe](https://web.archive.org/web/20170829200857/http://wwwimages.adobe.com/content/dam/Adobe/en/products/photoshop/pdfs/dng_spec_1.4.0 .0.pdf)

* [Digitaalinen negatiivi - Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)

* [DNG – digitaalikameran raakadatan julkinen arkistomuoto](https://helpx.adobe.com/camera-raw/digital-negative.html)


