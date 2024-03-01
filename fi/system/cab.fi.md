{
  "date": "2021-06-29",
  "keywords": [
"OHJAAMO",
"laajennus",
"tiedosto",
"muoto",
"järjestelmä",
"Windows-kaappitiedosto",
"Microsoft",
"Asentaja",
"Perustaa",
"AdvPak"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CAB - Windows Cabinet File",
  "description": "Opi CAB-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CAB-tiedostoja.",
  "linktitle": "CAB",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-ca-fib"
}
},
  "lastmod": "2021-06-29"
}

## Mikä on CAB-tiedosto? ##

Tiedosto, jonka tunniste on .cab, kuuluu Windows Cabinet -tiedostoon, joka kuuluu järjestelmätiedostojen luokkaan. Se on tiedosto, joka on tallennettu arkistotiedostomuodossa Microsoft Windowsin versioissa, jotka tukevat pakattuja dataalgoritmeja, kuten [LZX](/compression/lzx/), Quantum ja [ZIP](/compression/zip/). Tiedosto on erittäin tärkeä, kun käyttäjä tai kehittäjä haluaa sisältää ja jakaa ohjelmiston asennustietoja ja tiedostoja. Häviöttömän tiedonpakkauksen ominaisuudet ja näihin tiedostoihin sisältyvä digitaalinen sertifikaatti tekevät tästä tiedostosta täydellisen tällaisten tiedostojen tallentamiseen ja jakamiseen. Se tukee erilaisia Microsoftin asennusohjelmia, kuten Device Installer, SetUp API ja AdvPak.

## Lyhyt historia ##

CAB-tiedosto on Microsoftin kehittämä tietojen pakkaustiedostotyyppi. Sitä kutsuttiin alun perin nimellä Diamond, mutta sitten se tunnettiin yleisesti nimellä CAB-tiedosto, lyhenne sanasta Cabinet.

## Tekniset tiedot ##

CAB-tiedosto voi yleensä sisältää enintään 65 535 kansiota, jotka puolestaan voivat sisältää enintään 65 536 tiedostoa kukin. CAB-tiedostojen tallennusmekanismi on aikaa ja tilaa säästävä, koska se tallentaa jokaisen kansion pakattuna lohkona sen sijaan, että pakkaa ja tallentaa jokaista tiedostoa erikseen. Tyhjiä kansioita ei voi tallentaa CAB-arkistokansioihin. CAB-tiedoston on ensin kehittänyt Microsoft, ja sitä käytetään useissa asennusohjelmissa, kuten InstallShieldissä hieman erilaisessa muodossa. CAB-tiedostot yhdistetään yleensä itsepurkautuviin ohjelmiin. Microsoft CAB -tiedostot ovat helposti tunnistettavissa niiden ainutlaatuisen merkin ansiosta, joka auttaa muodon tunnistamisessa. Ainutlaatuinen merkki kaikille Microsoft CAB -tiedostoille on nelisanainen etuliite, MSCF. Nähdessään tämän koodin käyttäjä voi helposti erottaa Microsoft CAB -tiedoston muista tiedostoista ja käyttää sitä vastaavasti kompressoreissa tai versioissa. Tiedostot voidaan pakata useammilla ohjelmistoasennustiedoilla tai nykyiset tiedot voidaan purkaa oikealla ohjelmistolla.


## CAB-esimerkki ##

Seuraava esimerkki havainnollistaa tiedostojen ja kansioiden välistä suhdetta CAB-tiedostorakenteessa:

{{< figure src="../cab.png" alt="CAB-tiedostomuoto" >}}

## Viite ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
