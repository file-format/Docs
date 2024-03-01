{
  "date": "2021-08-16",
  "keywords": [
"nrg tiedosto",
"nrg tiedostomuoto",
"mikä on nrg-tiedosto",
"tiedosto",
"nrg esimerkki",
"nrg tiedostopääte",
"laajennus",
"muoto",
"nrg alatunniste",
"tiedostomuoto nrg",
"Nero Burning Rom",
"Nero AG"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Opi NRG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata NRG-tiedostoja.",
  "title": "NRG - Levykuvatiedostomuoto",
  "linktitle": "NRG",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-nr-fig"
}
},
  "lastmod": "2021-08-16"
}

## Mikä on NRG-tiedosto?

Kuvatiedostomuotoa, joka on luotu käyttämällä optista levyä, pidetään NRG-tiedostomuodona. Nero on erityisesti luonut tämän muodon Nero Burning Rom -apuohjelmaa varten. Levykuvien tallentamiseen tätä muotoa pidetään sopivana näille tiedostoille. Nämä tiedostot voivat olla CD- tai DVD-levyn tarkan kopion muodossa tai niissä voi olla useita tiedostoja, jotka voidaan liittää levyksi. Muita suosittuja tiedostomuotoja, kuten [ISO](/compression/iso/)-tiedostomuotoja, nämä tiedostot voidaan muuntaa joihinkin perusapuohjelmiin. Useimmiten NRG-tiedostoja käytetään varmuuskopioiden tai kopioiden luomiseen joistakin tärkeistä tiedoista tai levyistä.

## NRG-tiedostomuoto ##

Nero AG on kehittänyt tämän tiedostomuodon levykuvamuodoksi. Siinä oli Nero Burning Rom -apuohjelman erityinen ominaisuus, koska se kehitettiin levykuvien tallentamiseen. Sen ensimmäinen versio määritettiin tallentamaan arvot 32-bittisinä kokonaislukuina. Sen toinen versio julkaistiin kuitenkin ja se sisälsi tuen 64-bittisille kokonaisluvuille.

## Tekniset ominaisuudet ##

Tiedoston alussa tämä muoto ei tallenna tietojaan otsikkona. Kuten alatunniste, se liitetään tiedoston loppuun. IFF-palojen muodossa kuvan tiedot tallennetaan. Ensimmäisen osan siirtymä voidaan saada lukemalla NRG-alatunniste tiedoston viimeisistä 8-12 tavusta. Kaikissa NRG-tiedostomuodon versioissa on paloja, DAOI, CD-teksti, istuntotietojen mediatyyppi, levytiedot, Relo ja siihen liitetty ketjun pää. Tavujärjestys on suuri ja kaikki kokonaislukuarvot ovat etumerkittömiä tallennushetkellä.

### Pääpalat ###

#### Vihjelehti ####

Tämä vihjearkki on helposti saatavilla kaikissa NRG-tiedostomuotoversioissa. **CUEX**:n pala tarkoittaa kiinteän kokoisen ketjutuksen lohkoja ja jokainen näistä edustaa vihjepistettä.

#### DAO-tiedot ####

Nämä tiedot ovat myös kaikissa NRG-muotoisissa versioissa. **DAOI**:n palaset tallentavat olennaiset tiedot kahteen osaan. Sen ensimmäinen osa koostuu vain istuntokohtaisista tiedoista. Sen toinen osa vain toistaa seurantaan liittyvät harmaat tiedot ja se on vain kerran jokaiselle kappaleelle.

#### CD-teksti ####

Tämä on saatavilla NRG:n toisessa versiossa. **CDTX**-kappale koostuu CD-tekstipaketin raakaketjutuksesta, jossa on 18 tavua jokaiselle.

#### Laajennetut kappaletiedot ####

Tämä on saatavilla kaikissa NRG-tiedostomuodon versioissa. Näitä paloja käytetään seurantatietojen tallentamiseen kerralla istuntojen radalle. Nämä tiedot toistetaan vain kerran kunkin raidan tapauksessa.

#### Istunnon tiedot ####

Tämä on saatavilla myös kaikissa NRG-tiedostomuodon versioissa. Istuntopalojen tietoja on hyödynnettävä istunnon kuvan nopeaan skannaamiseen ja sen jälkeen seurantaan.

#### Ketjun loppu ####

Lopun pala tarkoittaa signaaleja siitä, että nyt ei ole enää palasia joita pitäisi lukea ja tämä on myös saatavilla NRG:n kaikissa versioissa.


## Viitteet ##

* [NRG - Wikipedia](https://en.wikipedia.org/wiki/NRG_(file_format))



