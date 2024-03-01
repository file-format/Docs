{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF2-tiedosto - Web Open Font Format 2.0 -tiedosto",
  "description": "Opi, mikä on WOFF2-tiedosto ja API:t, jotka voivat luoda ja avata WOFF2-tiedoston.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-fi2"
}
},
  "lastmod": "2023-01-10"
}

## Mikä on WOFF2-tiedosto?

WOFF2 on fonttitiedostomuoto, joka on pakattu versio Web Open Font Formatista (WOFF). Se kehitettiin tapana pienentää verkkofonttien tiedostokokoa, jolloin ne latautuvat nopeammin ja käyttävät vähemmän kaistanleveyttä. WOFF2 käyttää Brotli-nimistä pakkausalgoritmia fonttitietojen pakkaamiseen, mikä voi johtaa tiedostokokoihin, jotka ovat huomattavasti pienempiä kuin vastaavat [WOFF](/font/woff/)-kirjasimet. Tätä muotoa tukevat useimmat nykyaikaiset verkkoselaimet, kuten Chrome, Firefox, Safari, Opera ja Edge (versiosta 14 alkaen).

## WOFF2-tiedostomuoto - lisätietoja

WOFF2-fonttitiedoston sisäinen tiedostorakenne koostuu useista eri osista, mukaan lukien otsikosta, metatiedoista, taulukkohakemistosta ja itse fonttitiedoista.

 1. Otsikko sisältää tietoja tiedoston yleisestä muodosta, mukaan lukien versionumero ja tiedostossa olevien taulukoiden lukumäärä.

 1. Metatiedot-osio sisältää tietoja, kuten fontin nimen, tekijänoikeudet ja muita kirjasimiin liittyviä tietoja.

 1. Taulukkohakemisto sisältää tietoa fontin muodostavista eri taulukoista, mukaan lukien niiden sijainti tiedostossa ja pituus.

 1. Itse fonttitiedot on jaettu useisiin eri taulukoihin, joista jokainen sisältää erityistä tietoa kirjasimesta, kuten sen merkit ja niitä vastaavat kuviot. Nämä taulukot voivat sisältää:

 * Glyf-taulukko sisältää todelliset fontin ääriviivat, mukaan lukien kunkin merkin muodon ja koon.
 * Päätaulukko sisältää yleistä tietoa kirjasimesta, kuten sen versionumeron, suunnittelukoon ja niin edelleen.
 * Hmtx-taulukko sisältää tietoja kirjasimen mittareista, mukaan lukien merkkien leveydet ja sijainnit.
 * Jokainen taulukko pakataan ja tallennetaan WOFF2-tiedostomuotoon sen jälkeen, kun se on valmis koodausprosessin.

Kokonaisuudessaan rakenne on suunniteltu mahdollistamaan nopea jäsennys ja dekoodaus, jotta verkkoselaimet voivat ladata ja näyttää fontin verkkosivustolla nopeasti ja tehokkaasti.

### WOFF2-otsikko
WOFF-otsikko käsittää tunnisteen allekirjoituksen, joka ilmaisee, minkä tyyppistä dataa tiedosto sisältää. WOFF-otsikko ja sen kentät ovat seuraavat.

|Tyyppi|Kentän nimi|Kuvaus|
---|---|---|
|UInt32|allekirjoitus |0x774F4632 'wOF2' |
|UInt32| flavor |Syötefontin sfnt-versio.|
|UInt32| pituus |WOFF-tiedoston kokonaiskoko.|
|UInt16| numTables |Syötteiden lukumäärä fonttitaulukkojen hakemistossa.|
|UInt16| varattu |Varattu; asetettu nollaan.|
|UInt32| totalSfntSize |Pakkaamattomien fonttitietojen, mukaan lukien sfnt-otsikon, hakemiston ja fonttitaulukoiden (mukaan lukien täyte) tarvittava kokonaiskoko.|
|UInt32| totalCompressedSize Pakatun tietolohkon kokonaispituus.|
|UInt16| majorVersion |WOFF-tiedoston pääversio.|
|UInt16| minorVersion |WOFF-tiedoston sivuversio.|
|UInt32| metaOffset |Siirtymä metatietolohkoon, WOFF-tiedoston alusta.|
|UInt32| metaLength |Pakatun metatietolohkon pituus.|
|UInt32| metaOrigLength |Metatietolohkon pakkaamaton koko.|
|UInt32| privOffset |Siirtymä yksityiseen tietolohkoon, WOFF-tiedoston alusta.|
|UInt32| privLength |Yksityisen tietolohkon pituus.|


## Viitteet
 * [w3 WOFF2-tiedostomuoto](https://www.w3.org/TR/WOFF2/)

