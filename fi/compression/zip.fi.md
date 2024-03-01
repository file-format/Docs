{
  "date": "2019-12-09",
  "keywords": [
"POSTINUMERO-tiedosto",
"zip-tiedostomuoto",
"mikä on zip-tiedosto",
"tiedosto",
"zip esimerkki",
"zip tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "POSTINUMERO",
  "description": "What is a POSTINUMERO file and APIs that can create and open POSTINUMERO files.",
  "linktitle": "POSTINUMERO",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-zi-fip"
}
},
  "lastmod": "2019-12-09"
}

## Mikä on POSTINUMERO-tiedosto? ##

A file with .zip extension is an archive that can hold one or more files or directories. The archive can have compression applied to the included files in order to reduce the POSTINUMERO file size. POSTINUMERO file format was made public back in February 1989 by Phil Katz for achieving archiving of files and folders. The format was made part of [PKPOSTINUMERO](https://www.pkware.com/pkzip) utility, created by PKWARE, Inc. Right after the availability of [available specifications](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT), many companies made POSTINUMERO file format part of their software utilities including Microsoft (since Windows 7), Apple (Mac OS X ) and many others.

## POSTINUMERO-tiedostomuodon lyhyt historia

POSTINUMERO-tiedostomuodon historia juontaa juurensa tapaukseen, jossa System Enhancement Associates (SEA) on nostanut kanteen PKWAREa vastaan, koska se käytti ARC-apuohjelmaa ilman tavaramerkkinsä ja tuotteen ulkoasun ja käyttöliittymän tekijänoikeuksia. Ennen tätä Phil Katz oli kirjoittanut SEA:n lähdekoodin uudelleen ja julkaissut PKXARC:n, ARC-poiminnan, ja PKARCin, tiedostopakkausohjelman, ilmaisohjelmina MS-DOS-pohjaisille järjestelmille. Hävittyään oikeudenkäynnissä PKWARE ei voinut enää käyttää mitään ARC:hen liittyvää. Tästä syntyi uuden tiedostopakkauksen luominen, nimeltään POSTINUMERO, joka tehtiin osaksi PKWARE, Inc:n PKPOSTINUMERO-apuohjelmaa.

Katz julkaisi POSTINUMERO-tiedostomuotomääritykset julkisuuteen säilyttäen samalla pakkaus- ja purkuapuohjelmansa eli PKPOSTINUMERO:n omistusoikeudet. POSTINUMERO-pakkausjärjestelmä pystyi (ja pystyy) arkistoimaan tiedostoja kansioon 32-bittisen syklisen redundanssitarkistusalgoritmin ([CRC](https://en.wikipedia.org/wiki/Cyclic_redundancy_check)) avulla tiedostokokojen pakkaamiseksi. Toisin kuin ARC, .POSTINUMERO-kansiot sisälsivät hakemistotiedoston, joka toimi salakirjoittajan koodikirjana ja sisältää pakattujen tiedostojen hahmontamiseen tarvittavat tiedot.

## Tuetut pakkausmenetelmät POSTINUMERO:ssä

.POSTINUMERO-tiedostomuodon määritysten mukaan seuraavia pakkausmenetelmiä tuetaan.

* Store - ei sisällä pakkausta

* Kutista

* Vähennys (Tämä tarkoittaa pakkauskertoimia tasosta 1 tasoon 4)

* Räjähtää

* Tyhjennä

* Deflat64

* BPOSTINUMERO2

* LZMA (EFS)

* WavPack

* PPMd versio I, Rev 1


DEFLATE is the commonly used compression method which is a lossless date compression algorithm that uses a combination of the LZ77 and Huffman coding and is detailed in [RFC 1951](https://tools.ietf.org/html/rfc1951).

## POSTINUMERO-tiedostomuodon tekniset tiedot

POSTINUMERO-tiedostot voivat tallentaa useita tiedostoja käyttämällä erilaisia pakkaustekniikoita, ja samalla ne tukevat tiedoston tallentamista ilman pakkausta. Jokainen tiedosto tallennetaan/pakkataan erikseen, mikä auttaa purkamaan ne tai lisäämään uusia ilman koko arkiston pakkausta tai purkamista.

### Yleinen POSTINUMERO-tiedostomuoto

Jokainen Zip-tiedosto on rakennettu seuraavalla tavalla:


|POSTINUMERO-tiedostomuoto
---|
|Paikallinen tiedoston otsikko 1
|Tiedostotiedot 1
|Datakuvaaja 1
|Paikallinen tiedoston otsikko 2
|Tiedostotiedot 2
|Datakuvaaja 2
| ....
| ....
|Paikallinen tiedoston otsikko N
|Tiedostotiedot N
|Datakuvaaja N
|Arkiston salauksenpurkuotsikko
|Arkistoi ylimääräiset tiedot
|Keskihakemisto

POSTINUMERO-tiedostomuoto käyttää 32-bittistä CRC-algoritmia arkistointitarkoituksiin. Pakattujen tiedostojen hahmontamiseksi POSTINUMERO-arkistossa on lopussa hakemisto, joka säilyttää sisältämien tiedostojen merkinnät ja niiden sijainnin arkistotiedostossa. Siten se toimii koodauksena pakattujen tiedostojen tekemiseen tarvittavien tietojen kapseloimiseksi. POSTINUMERO-lukijat käyttävät hakemistoa tiedostoluettelon lataamiseen lukematta koko POSTINUMERO-arkistoa. Muoto säilyttää kaksi kopiota hakemistorakenteesta, mikä tarjoaa paremman suojan tietojen katoamista vastaan.

Jokainen POSTINUMERO-arkiston tiedosto esitetään erillisenä merkintänä, jossa jokainen merkintä koostuu paikallisesta tiedoston otsikosta ja sen jälkeen pakatuista tiedostotiedoista. Arkiston lopussa oleva hakemisto sisältää viittaukset kaikkiin näihin tiedostomerkintöihin. POSTINUMERO-tiedostolukijoiden tulisi välttää paikallisten tiedostojen otsikoiden lukemista ja kaikenlaiset tiedostoluettelot tulee lukea hakemistosta. Tämä hakemisto on ainoa kelvollisten tiedostomerkintöjen lähde arkistossa, koska tiedostoja voidaan liittää myös arkiston loppuun. Tästä syystä, jos lukija lukee POSTINUMERO-arkiston paikalliset otsikot alusta alkaen, se voi lukea virheellisiä (poistettuja) merkintöjä, samoin kuin ne, jotka eivät ole osa arkistosta poistettavaa hakemistoa.

Keskushakemiston tiedostomerkintöjen järjestyksen ei tarvitse olla sama kuin arkiston tiedostomerkintöjen järjestys.

### POSTINUMERO-tiedoston merkinnät

POSTINUMERO-tiedoston merkinnät on järjestetty peräkkäin, jolloin jokainen merkintä koostuu:

* Paikallinen tiedoston otsikko

* Valinnaiset lisätietokentät

* Käyttäjätiedot (valinnaisesti pakattu / valinnaisesti salattu)


Kunkin merkinnän paikallinen tiedoston otsikko edustaa tietoja tiedostosta, kuten kommentti, tiedostokoko ja tiedoston nimi. Lisätietokentät (valinnainen) voivat sisältää tietoja POSTINUMERO-muodon laajennettavuusvaihtoehdoista.

#### Paikallinen tiedoston otsikko

Paikallisella tiedoston otsikolla on erityinen kenttärakenne, joka koostuu monitavuisista arvoista. Kaikki arvot tallennetaan pieni-endian tavujärjestyksessä, jossa kentän pituus laskee pituuden tavuina. Kaikki POSTINUMERO-tiedoston rakenteet käyttävät 4-tavuisia allekirjoituksia jokaiselle tiedostolle. Keskushakemiston allekirjoituksen loppu on 0x06054b50 ja se voidaan erottaa sen omalla ainutlaatuisella allekirjoituksella. Seuraava on paikalliseen tiedoston otsikkoon tallennettujen tietojen järjestys.


|Offset|Tavut|Kuvaus
---|---|---|
|0|4|Paikallisen tiedoston otsikon allekirjoitus # 0x04034b50 (lukea pienenä loppunumerona)
|4|2|Poimittava versio (minimi)
|6|2|Yleinen bittimerkki
|8|2|Pakkausmenetelmä
|10|2|Tiedosto viimeisimmän muokkauksen aika
|12|2|Tiedosto viimeisin muokkauspäivä
|14|4|CRC-32
|18|4|Pakattu koko
|22|4|Pakkaamaton koko
|26|2|Tiedoston nimen pituus (n)
|28|2|Ylimääräinen kentän pituus (m)
|30|n|Tiedoston nimi
|30+n|m|Lisäkenttä

#### Keskihakemistotiedoston otsikko


|Offset|Tavut|Kuvaus
---|---|---|
|0|4|Keskihakemistotiedoston otsikon allekirjoitus # 0x02014b50
|4|2|Version tekijä
|6|2|Poimittava versio (minimi)
|8|2|Yleinen bittimerkki
|10|2|Pakkausmenetelmä
|12|2|Tiedosto viimeisimmän muokkauksen aika
|14|2|Tiedosto viimeisin muokkauspäivä
|16|4|CRC-32
|20|4|Pakattu koko
|24|4|Pakkaamaton koko
|28|2|Tiedoston nimen pituus (n)
|30|2|Ylimääräinen kentän pituus (m)
|32|2|Tiedoston kommentin pituus (k)
|34|2|Levyn numero, josta tiedosto alkaa
|36|2|Sisäiset tiedostomääritteet
|38|4|Ulkoiset tiedostomääritteet
|42|4|Paikallisen tiedoston otsikon suhteellinen siirtymä. Tämä on tavumäärä ensimmäisen levyn, jolla tiedosto esiintyy, alun ja paikallisen tiedoston otsikon alun välillä. Tämän ansiosta keskushakemistoa lukeva ohjelmisto voi paikantaa tiedoston sijainnin POSTINUMERO-tiedoston sisällä.
|46|n|Tiedoston nimi
|46+n|m|Lisäkenttä
|46+n+m|k|Tiedosta kommentti

#### Keskushakemistotietueen loppu


|Offset|Tavut|Kuvaus
---|---|---|
|0|4|Keskihakemiston allekirjoituksen loppu # 0x06054b50
|4|2|Tämän levyn numero
|6|2|Levy, josta keskushakemisto alkaa
|8|2|Tällä levyllä olevien keskushakemistotietueiden lukumäärä
|10|2|Keskushakemistotietueiden kokonaismäärä
|12|4|Keskihakemiston koko (tavuina)
|16|4|Keskihakemiston alun siirtymä suhteessa arkiston alkuun
|20|2|Kommentin pituus (n)
|22|n|Kommentoi

## Viitteet

* [PKWARE POSTINUMERO File Format Specifications](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [PKZip-tiedoston rakenne](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)


