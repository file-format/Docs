{
  "date": "2021-08-09",
  "keywords": [
"cso tiedosto",
"cso tiedostomuoto",
"mikä on cso-tiedosto",
"tiedosto",
"cso esimerkki",
"cso tiedostopääte",
"laajennus",
"muoto",
"iso",
"DAX-pakkaus"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi CSO-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CSO-tiedostoja.",
  "title": "CSO - Pakattu ISO-levykuva",
  "linktitle": "CSO",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-cs-fio"
}
},
  "lastmod": "2021-08-09"
}

## Mikä on CSO-tiedosto?

.cso-tunnisteella varustettu tiedosto on pakattu ISO-kuvatiedosto. CSO on vaihtoehto DAX-pakkausmenetelmälle; tunnetaan myös nimellä CISO; oli ensimmäinen tapa pakata [ISO](/compression/iso/)-tiedostoja ja se on yleensä suositeltu tapa arkistoida PlayStation Portable -sisältöä. Tämä muoto käyttää Deflate-pakkausta, joka voi sisältää jopa yhdeksän pakkaustasoa. Kuvien luomiseen käytetään ohjelmistoja, kuten Prometheus ja YACC.

## CSO-tiedostomuoto

CSO-tiedostomuoto oli ensimmäinen ISO-pakkausmenetelmä muistitilan säästämiseksi. Parannuksia tehtiin ajoittain paremman pakkauksen saavuttamiseksi. CSO käyttää Deflate-pakkausta, jossa on yhdeksän esiasetustasoa, yleensä jokainen taso pystyy käsittelemään 2 KiB-lohkoa erikseen. Vaikka korkeimmat pakkaustasot voivat hidastaa ja pitkiä latausaikoja ohjelmistoissa, jotka riippuvat suuresti levyn suoratoistosta, myös alemmat tasot voivat suorittaa huomattavaa pakkausta.

### CSO-tiedostorakenne

CSO-tiedostomuoto sisältää 24-tavun otsikon, tietolohkoja ja indeksitaulukon. Little-endian oletetaan tavua suuremmille kentille. PlayStation Portablen arkkitehtuurin endianness on esitetty alla.

#### Otsikko

| Offset (tavuja) | Nimi | Koko (tavuina) | Tarkoitus |
----------|----------|--------------|---------|
| 0x0 | Magic | 4 | Aina CISO tai 0x4F534943 luettaessa 32-bittisenä kokonaislukuna. Tätä kenttää käytetään CSO-tiedoston tunnistamiseen. Huomaa, että tämä kenttä voi olla erilainen muille CSO:n johdannaisille, esimerkiksi ZSO käytti taikakoodia ZISO. |
| 0x4 | Otsikon koko | 4 | Alkuperäisessä CSO v1 -tiedostomuodossa tämä kenttä jätetään huomiotta, joten sen ei tarvitse olla tarkka. v2- ja ZSO-muoto edellyttävät kuitenkin, että tämä kenttä on aina 0x18 (24 tavua). |
| 0x8 | Pakkaamaton koko | 8 | Alkuperäisen pakkaamattoman ISO-arvon koko tavuina. |
| 0x10 | Lohkon koko | 4 | Kunkin tietolohkon koko tavuina ennen pakkausta. Yleensä 2048 tavua, sama kuin kunkin ISO 9660 -sektorin koko. |
| 0x14 | Version | 1 | The version of the file format in use. For the "v1" format, the value can be either 0 or 1. v2-muodossa tämän on oltava 2. Lisäksi ZSO-muoto edellyttää tämän olevan 1. |
| 0x15 | Hakemiston tasaus | 1 | Kunkin indeksimerkinnän kohdistus, määritetty bitteinä. |
| 0x16 | Varattu | 2 | Tämä kenttä on käyttämätön. V1-muodossa tämä kenttä ohitetaan, ja se voi sisältää mielivaltaisia arvoja. V2-muodossa tämän kentän on oltava nolla. |

#### Hakemistotaulukko

Indeksitaulukko sisältää useita 4-tavuisia merkintöjä, jotka osoittavat kunkin tietolohkon sijainnin, ja ylimääräisen, viimeisen merkinnän, joka osoittaa tiedoston loppuun.
Kunkin merkinnän sisältö on seuraava:
| Bittinen | Pituus | Naamio | Nimi | Tarkoitus |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFFF | Asema | Tämä kenttä, kun sitä siirretään vasemmalle otsikossa annetulla indeksikohduksella, antaa paikan, josta tietolohko alkaa. |
| 31 | 1 | 0x80000000 | Puristustyyppi | ZSO-muodossa on samanlainen semantiikka, vain että 0 edustaa LZ4:ää Deflate-arvon sijaan. v2-muodossa. Lohkon katsotaan olevan implisiittisesti pakkaamaton, jos lohkon koko on yhtä suuri tai suurempi kuin tiedoston otsikossa määritetty lohkokoko. |

#### Tietolohkot

Datalohkot koostuvat pakkaamattomasta tai pakatusta tiedosta. Lohkon koko lasketaan hankkimalla sen sijainti ja vähentämällä se sitten seuraavan lohkon paikasta. Jos indeksin kohdistus on suurempi kuin nolla, on todennäköistä, että lohkon koko on suurempi kuin sen sisältämä data.


## Viitteet 

* Ei käytössä


