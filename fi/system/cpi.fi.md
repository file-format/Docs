{
   "date":"2023-10-18",
   "keywords":[
"cpi",
"cpi-tiedosto",
"cpi-koodisivun tietotiedosto",
"kuinka avata cpi-tiedosto",
"tiedosto",
"cpi tiedostopääte",
"laajennus",
"tiedosto"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CPI-tiedostomuoto - Koodisivun tietotiedosto",
   "description":"Opi CPI Codepage Information -tiedostomuodosta ja API:ista, jotka voivat luoda ja avata CPI-tiedostoja.",
   "linktitle":"CPI",
   "menu":{
      "docs":{
         "identifier":"system-cpi-fi",
         "parent":"system"
}
},
   "lastmod":"2023-10-18"
}

## Mikä on CPI-tiedosto?

.cpi-tiedosto Microsoft Windows- ja DOS-käyttöjärjestelmissä on yleensä **Koodisivun tietotiedosto.** Nämä tiedostot sisältävät tietoja tekstin koodaukseen ja merkistöjen yhdistämiseen käytetyistä koodisivuista. Koodisivut ovat välttämättömiä tekstin näyttämisessä ja käsittelyssä eri kielillä ja merkistöillä.

Windows- ja DOS-ympäristöissä koodisivuja käytetään määrittämään, kuinka merkit esitetään ja koodataan eri kielillä ja alueilla. Nämä koodisivut määrittävät, kuinka merkit tallennetaan muistiin ja näytetään näytöllä. Jokaisella koodisivulla on yksilöllinen tunniste, ja .cpi-tiedostot tallentavat tietoja näistä koodisivuista, mukaan lukien tiedot, kuten merkkikartoitukset ja kirjasintiedot.

.cpi-tiedostoja löytyy yleisesti Windows- tai DOS-järjestelmähakemistoista, ja niillä on ratkaiseva rooli, jotta käyttöjärjestelmä pystyy näyttämään tekstiä oikein eri kielialueilla ja merkistöissä. Ne auttavat järjestelmää ymmärtämään, kuinka tulkita ja renderöidä merkkejä eri kielistä ja koodauksista.

## Koodisivun tietotiedostot

Tarkastellaanpa tarkemmin koodisivutietotiedostoja (.cpi) ja niiden toimintaa MS-DOS:n ja Microsoft Windowsin aiempien iteraatioiden puitteissa:

1.  **Merkkikoodaus ja koodisivut**: Koodisivut ovat tärkeä osa tekstin koodausta ja näyttöä tietokoneessa. Ne määrittelevät merkkikoodauksen tietylle kielelle tai merkistölle. Jokainen koodisivu määrittää numeroarvot (koodipisteet) merkeille, jolloin tietokone voi esittää ja näyttää ne. Esimerkiksi koodisivua 437 käytetään yleisesti Yhdysvalloissa ja Länsi-Euroopassa, kun taas koodisivua 850 käytetään Latin-1-koodaukseen.
    
2.  **Järjestelmän alustus**: Järjestelmän alustuksen aikana (kun tietokone käynnistetään), MS-DOS ja Windowsin vanhemmat versiot lukevat .cpi-tiedostoja määrittääkseen, mitä koodisivuja tuetaan. Nämä tiedot olivat tärkeitä tekstin toiston, näppäimistön syöttämisen ja merkistöjen muuntamisen kannalta.
    
3.  **Näyttö- ja näppäimistötuki**: Nämä tiedostot tarjoavat tietoa siitä, kuinka merkit tulee näyttää näytöllä ja mitä merkistöjä tai koodisivuja tulee tukea näppäimistön syöttämiseen. Eri koodisivut määrittelevät erilaisia merkistöjä, joten nämä tiedostot auttavat käyttöjärjestelmää käsittelemään käyttäjän syötettä ja näyttämään tekstiä oikein.
    
4.  **Lokalisointi**: `.cpi`-tiedostot ovat välttämättömiä käyttöjärjestelmän lokalisoinnissa. Niiden avulla järjestelmä mukautuu eri kieliin, alueisiin ja merkistöihin, jolloin käyttäjät ympäri maailmaa voivat käyttää MS-DOS:ia tai Windowsia haluamillaan kielillä.
    
5.  **Useita .cpi-tiedostoja**: Tietokoneessa, jossa on monikielinen tuki, saatat löytää useita .cpi-tiedostoja, jotka vastaavat eri koodisivuja. Esimerkiksi järjestelmässä voi olla 437.cpi Yhdysvalloille, 850.cpi Latin-1:lle, 852.cpi Keski-Euroopalle ja niin edelleen. Asianmukainen tiedosto ladataan käyttäjän kielen tai valitun koodisivun perusteella.
    
6.  **Fonttitiedot**: Merkkikartoitusten lisäksi nämä tiedostot voivat sisältää kirjasintietoja, jotka määrittävät kullekin koodisivulle käytettävän fontin. Tämä on tärkeää, jotta teksti hahmonnetaan sopivalla tyylillä ja koossa.
    
7.  **Vanhat järjestelmät**: `.cpi`-tiedostot olivat yleisempiä MS-DOS:n ja Windowsin vanhemmissa versioissa. Nykyaikaiset Windows-versiot (kuten Windows 10 ja uudemmat) käyttävät yleensä Unicodea tekstin koodaukseen, joka tukee monenlaisia merkkejä ja kieliä. Unicode yksinkertaistaa tekstinkäsittelyä monikielisissä ympäristöissä ja on vakiona nykyaikaisissa ohjelmistoissa.

## Kuinka avata CPI -tiedosto?

.CPI (Code Page Information) -tiedoston avaaminen ei ole tyypillistä käyttäjän toimintaa, eikä näitä tiedostoja yleensä ole tarkoitettu avattavaksi manuaalisesti. Käyttöjärjestelmä käyttää niitä tekstin koodauksen ja merkistöjen hallintaan, ja järjestelmä käyttää ja käyttää niiden sisältöä automaattisesti.

Jos olet kuitenkin kiinnostunut tarkastelemaan .CPI-tiedoston sisältöä tiedoksi, voit yrittää avata sen tekstieditorilla tai heksadesimaalikatseluohjelmalla. Näin voit yrittää avata .CPI-tiedoston:

1.  **Tekstieditori**: Voit käyttää tekstieditoria, kuten Muistio-ohjelmaa (Windows) tai mitä tahansa pelkkä tekstieditoria muissa käyttöjärjestelmissä .CPI-tiedoston avaamiseen ja tarkastelemiseen. Muista, että .CPI-tiedostojen sisältöä ei ole tarkoitettu ihmisen luettavaksi ja saatat nähdä sarjan merkkejä, joita on vaikea tulkita.
    
2.  **Heksadesimaalinen katseluohjelma**: Heksadesimaalista katseluohjelmaa tai heksadesimaalieditoria voidaan käyttää .CPI-tiedoston sisällön avaamiseen ja tarkastamiseen sen raakabinäärimuodossa. Hex-editorit tarjoavat yksityiskohtaisemman kuvan tiedoston tiedoista, mikä voi olla hyödyllistä, jos yrität ymmärtää sen rakennetta. Esimerkkejä tällaisista ohjelmistoista ovat HxD, Hex Fiend (macOS) ja 010 Editor.

## Muut CPI-tiedostot

Tässä on muita tiedostotyyppejä, jotka käyttävät **.cpi**-tiedostotunnistetta.

**Video ja järjestelmä**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

## Viitteet
* [Koodisivu](https://en.wikipedia.org/wiki/Code_page)


