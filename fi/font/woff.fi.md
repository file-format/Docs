{
  "date": "2020-08-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF - Web Open File Format",
  "description": "WOFF-tiedosto on avoin fonttimuoto, joka on luotu Web Open Font Format -muodossa.",
  "linktitle": "WOFF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-wof-fif"
}
},
  "lastmod": "2020-09-30"
}

## Mikä on WOFF-tiedosto?

Tiedosto, jonka pääte on .woff, on web-fonttitiedosto, joka perustuu Web Open Font Format (WOFF) -muotoon. Siinä on muotokohtainen pakattu säilö, joka perustuu joko TrueType (.TTF)- tai OpenType (.OTT) -kirjasintyyppeihin. WOFF otettiin käyttöön tarkoituksena erottaa verkkofontit työpöytäsovelluksissa käytetyistä fonttitiedostoista. Lisäksi muoto on tarkoitettu vähentämään kirjasimien siirron viivettä palvelimelta asiakkaan tietokoneelle verkon kautta. Saatavilla on useita työkaluja, jotka voivat muuntaa WOFF-tiedostoja TTF- ja muihin fonttitiedostomuotoihin.

## WOFF-tiedostomuoto

WOFF-kirjasinmuoto pakkaa kirjasintietotaulukot taulukkopohjaisista sfnt-rakenteista, joita käytetään eri kirjasintyypeissä, kuten TrueType, OpenType ja Open Font Format. Se on kuin säilö näille kirjasintyypeille, ja siinä on myös tilaa sisällyttää kirjasimen metatiedot ja yksityiseen käyttöön sisällytettävät tiedot. Muuntimet käyttävät sfnt-tiedostoja WOFF-muotoiseksi tiedostoksi ja käyttäjäagentit palauttavat koodatun tiedoston käytettäväksi verkkoasiakirjan kanssa. On huomattava, että palautetut fonttitiedot vastaavat tarkasti syötettyä kirjasinmuotoa kaikilta osin.

WOFF-tiedostojen apuohjelmat sisältävät usein lisäominaisuuksia, kuten kuvion osajoukkoja, vahvistusta tai fonttiominaisuuksien lisäyksiä, mutta se ei ole välttämätöntä. Sekä luojan että käyttöagentin on varmistettava, että taustalla olevien fonttitietojen kelpoisuus säilyy.

### WOFF-tiedostorakenne

WOFF-tiedostorakenne on samanlainen kuin sfnt-fonttien. Se perustuu taulukkohakemistoon, joka sisältää kunkin fonttitietotaulukon pituudet ja siirtymät. Kaikkia taulukoita seurataan tämän alustavan tiedon jälkeen. Tiedosto sisältää kirjasintietokannan, joka on sama kuin alkuperäisissä fonteissa. Taulukoiden järjestys on myös sama, mutta jokainen voidaan pakata. WOFF-taulukkohakemisto kuitenkin korvaa alkuperäisen taulukkohakemiston.

WOFF-tiedosto koostuu seuraavista:

 * WOFFHeader - Tiedoston ylätunniste, jossa on perusfonttityyppi ja -versio, sekä metatietojen ja yksityisten tietolohkojen siirtymät.
 * TableDirectory - Fonttitaulukkojen hakemisto, joka ilmoittaa kunkin WOFF-tiedoston alkuperäisen koon, pakatun koon ja kunkin taulukon sijainnin.
 * FontTables - Fonttitietotaulukot syötetystä sfnt-fontista, pakattu kaistanleveysvaatimusten vähentämiseksi.
 * ExtendedMetadata – valinnainen laajennettu metadata, joka on esitetty XML-muodossa ja pakattu WOFF-tiedostoon tallentamista varten.
 * PrivateData – valinnainen yksityisten tietojen lohko fontisuunnittelijan, valimon tai toimittajan käytettäväksi.

### WOFF-otsikko
WOFF-otsikko käsittää tunnisteen allekirjoituksen, joka ilmaisee, minkä tyyppistä dataa tiedosto sisältää. WOFF-otsikko ja sen kentät ovat seuraavat.

|Tyyppi|Kentän nimi|Kuvaus|
---|---|---|
|UInt32|allekirjoitus |0x774F4646 'wOFF' |
|UInt32| flavor |Syötefontin sfnt-versio.|
|UInt32| pituus |WOFF-tiedoston kokonaiskoko.|
|UInt16| numTables |Syötteiden lukumäärä fonttitaulukkojen hakemistossa.|
|UInt16| varattu |Varattu; asetettu nollaan.|
|UInt32| totalSfntSize |Pakkaamattomien fonttitietojen, mukaan lukien sfnt-otsikon, hakemiston ja fonttitaulukoiden (mukaan lukien täyte) tarvittava kokonaiskoko.|
|UInt16| majorVersion |WOFF-tiedoston pääversio.|
|UInt16| minorVersion |WOFF-tiedoston sivuversio.|
|UInt32| metaOffset |Siirtymä metatietolohkoon, WOFF-tiedoston alusta.|
|UInt32| metaLength |Pakatun metatietolohkon pituus.|
|UInt32| metaOrigLength |Metatietolohkon pakkaamaton koko.|
|UInt32| privOffset |Siirtymä yksityiseen tietolohkoon, WOFF-tiedoston alusta.|
|UInt32| privLength |Yksityisen tietolohkon pituus.|

## Viitteet

 * [w3 WOFF-tiedostomuoto](https://www.w3.org/TR/WOFF/)

