{
  "date": "2021-08-17",
  "keywords": [
"udf tiedosto",
"udf-tiedostomuoto",
"mikä on udf-tiedosto",
"tiedosto",
"udf esimerkki",
"udf tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi UDF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata UDF-tiedostoja.",
  "title": "UDF - Universal Disk Format -tiedosto",
  "linktitle": "UDF",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-ud-fif"
}
},
  "lastmod": "2021-08-17"
}

## Mikä on UDF-tiedosto?
Tiedosto, jonka pääte on .udf, on levykuvantamismuoto, jota käytetään tyypillisesti tiedostojen tallentamiseen optiselle tietovälineelle. voidaan käyttää DVD-, CD- ja muiden optisten tietovälineiden polttamiseen; tallentaa kokoelman tiedostoja käyttäen UDF-standardissa määritettyä hakemistorakennetta; mahdollistaa tiedostojen poistamisen ja muokkaamisen kohdelevyllä myös sen jälkeen, kun ne on kirjoitettu. Optical Storage Technology Association asetti UDF-tiedostojärjestelmän standardiksi muodostamaan yhteinen tiedostojärjestelmä kaikille optisille tietovälineille, kuten uudelleenkirjoitettavalle optiselle medialle ja vain luku -medialle.

## UDF-tiedostomuoto 
UDF-tiedostomuoto on avoin toimittajaneutraali tiedostojärjestelmä tietokonetietojen tallentamiseen useille eri medioille. Sitä on käytetty yleisesti DVD-levyille ja uudemmille optisille levyformaateille. Yleensä ohjelmisto hallitsee UDF-tiedostojärjestelmän eräprosessissa ja kirjoittaa sen optiselle tietovälineelle yhdellä kertaa. Kun UDF kuitenkin kirjoittaa paketteja uudelleenkirjoitettavalle tietovälineelle, se sallii tiedostojen luomisen, poistamisen ja muuttamisen levylle samalla tavalla kuin yleiskäyttöinen tiedostojärjestelmä tekisi siirrettävälle tietovälineelle, kuten flash-asemille tai levykkeille.
### UDF-tiedot
UDF-standardi määrittelee seuraavat kolme tiedostojärjestelmämuunnelmaa:

- **Plain Build**: Tämä on alkuperäinen muoto, jota tuetaan kaikissa UDF-versioissa. Se esiteltiin standardin ensimmäisessä versiossa. Tätä muotoa voidaan käyttää minkä tahansa tyyppisillä levyillä, jotka mahdollistavat satunnaisen luku- tai kirjoituskäytön, kuten DVD+RW-levyt, kiintolevyt ja DVD-RAM-levyt.
- **VAT build**: Used specifically for writing to write-once media. The VAT is an additional structure on the disc that allows packet writing; that is, remapping physical blocks when files or other data on the disc are modified or deleted. For write-once media, the entire disc is virtualized, making the write-once nature transparent for the user; the disc can be treated the same way one would treat a rewritable disc.
- **Spared (RW) build**: Käytetään erityisesti kirjoittamiseen uudelleenkirjoitettavalle medialle. Se lisää ylimääräisen Säästötaulukon hallitsemaan vikoja, jotka lopulta ilmenevät levyn osissa, jotka on kirjoitettu uudelleen useita kertoja. Tämä taulukko tallentaa kuluneet sektorit ja kartoittaa ne uudelleen toimiviksi. UDF:n vianhallinta ei koske järjestelmiä, joissa on jo käytössä toinen vianhallintamuoto, kuten Mount Rainier (MRW) optisille levyille tai levyohjain kiintolevylle.
 



## Viitteet 

* [Windows Imaging Format - Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)



