{
  "date": "2020-11-11",
  "keywords": [
"BAK",
"laajennus",
"tiedosto",
"tiedosto muoto",
"BAK-tiedostotyyppi",
"BAK tiedostopääte",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"Tietokantatiedostot"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi BAK-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata BAK-tiedostoja.",
  "title": "BAK-tiedostomuoto - tietokannan varmuuskopiotiedosto",
  "linktitle": "BAK",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ba-fik"
}
},
  "lastmod": "2020-12-04"
}

## Mikä on BAK-tiedosto?

Tiedosto, jonka laajennus on .bak, on yleensä varmuuskopiotiedosto, jota eri ohjelmistotyökalut käyttävät tietojen varmuuskopioiden tallentamiseen. Tietokannan näkökulmasta Microsoft SQL Server käyttää BAK-tiedostoa tietokannan sisällön tallentamiseen. Kaikki tietokantaan liittyvät tiedot ja tiedostot tallennetaan tässä tiedostomuodossa, jotta ne voidaan hakea siltä varalta, että tietokanta voi jostain syystä vioittua tai vaurioitua. Varmuuskopiotiedostot voidaan tallentaa ja indeksoida muille palvelimille turvallisuussyistä. Useat sovellukset voivat luoda BAK-tiedostoja, kuten SQL Server Management Studio, Transact-SQL ja Windows PowerShell.

## BAK-tiedostomuoto

BAK-tiedoston sisäisiä yksityiskohtia ei tunneta, mutta yleisesti oletetaan, että se perustuu Microsoft Tape Format (MTF) -muotoon. MTF-määritykset ovat saatavilla, ja niihin voi viitata tiedoston rakenteen ymmärtämiseksi. Asiakirjassa on tietoja MTF-tallennustilasta kaikille, joilla on yleistä tietoa tallennustilan hallinnan toiminnoista, nauha-asemista ja tiedostojärjestelmistä.

### Tietojoukot

Tietojoukko on kokoelma objekteja, jotka on kirjoitettu tallennusvälineelle (nauhalle, optiselle levylle jne.) tietojen varmuuskopioinnin tai palautuksen aikana. Tietojoukot koostuvat useista tietovälineistä, jos dataa on paljon.

### MTF:n peruselementit

MTF-tiedosto koostuu joistakin peruselementeistä, jotka muodostavat sen rakennuspalikoita. Nämä elementit ovat:

#### Kuvauslohkot

Kuvauslohkoja (DBLK) käytetään muodon hallintaan ja ne muodostavat MTF-tiedoston ensisijaisen perustan. Yksi MTF-tiedosto määrittää useita DBLK:ita kullekin yksilölliselle roolille. Jokainen DBLK on muuttuvapituinen tietolohko, joka on jaettu seuraaviin neljään osaan:

 * Common Block Header - Kiinteäpituinen rakenne, joka on yhteinen kaikille DBLK:ille. Tämä on ainoa vaadittu lohkootsikko.
 * DBLK Type Information - Kiinteä pituus lohko, joka on määritetty määritettävän DBLK-tyypin mukaan
 * Käyttöjärjestelmän tiedot - Tietyt tiedot, jotka on määritelty DBLK:n ja käyttöjärjestelmien tyypin perusteella
 * DBLK-tiedot - Vaihtuvapituiset DBLK-tiedot, joita ei voida tallentaa kiinteän pituisten DBLK-tietojen kanssa.

{{< figure src=../bak.png alt=Microsoft SQL -varmuuskopiotiedostomuoto >}}

#### Datavirta

MTF-tiedoston tietovirtoja käytetään tietojen kapseloimiseen ja kohdistamiseen. Se koostuu stream-otsikosta, jota seuraa Stream Data. Stream-otsikko voi kapseloida vain yhden tyyppisen stream-datan.

{{< figure src="../bak_datastream.png" alt="Microsoft SQL -varmuuskopiotiedostomuoto" >}}

#### Tiedostomerkit

Tiedostomerkkiä käytetään loogiseen erotteluun ja nopeaan pääsyyn median sisällä. Tiedostomerkit emuloidaan laiteohjaimella tai käyttämällä Soft Filemark Descriptor -lohkoa, jos käytettävä laite ei tarjoa tiedostomerkkejä.

## Muut BAK-tiedostot

Tässä on muita tiedostotyyppejä, jotka käyttävät **.bak**-tiedostotunnistetta.

**Tietokanta**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

**Peli**
- {{HYPERLINKKI1}}

**Sekalaista**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

**Asetukset**
- {{HYPERLINKKI1}}

## Viitteet ##

* [[MS-BCP]: joukkokopiomuoto](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)


