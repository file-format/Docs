{
  "date": "2019-12-10",
  "keywords": [
"CSV",
"tiedosto",
"laajennus",
"tiedosto muoto",
"Pilkuilla erotetut arvot",
"Laskentataulukko"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lisätietoja CSV-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CSV-tiedostoja.",
  "title": "CSV-tiedostomuoto",
  "linktitle": "CSV",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-cs-fiv"
}
},
  "lastmod": "2019-12-10"
}

## Mikä on CSV-tiedosto?

Tiedostot, joissa on .csv (Comma Separated Values) -tunniste, edustavat pelkkiä tekstitiedostoja, jotka sisältävät tietueita tietueista, joissa on pilkuilla erotetut arvot. Jokainen CSV-tiedoston rivi on uusi tietue tiedoston sisältämistä tietuejoukosta. Tällaisia tiedostoja luodaan, kun tiedonsiirto on tarkoitettu tallennusjärjestelmästä toiseen. Koska kaikki sovellukset tunnistavat pilkuilla erotetut tietueet, tällaisten tiedostojen tuonti tietokantaan tapahtuu erittäin kätevästi. Lähes kaikki taulukkolaskentasovellukset, kuten Microsoft Excel tai OpenOffice Calc, voivat tuoda CSV-tiedoston ilman paljon vaivaa. Tällaisista tiedostoista tuodut tiedot järjestetään laskentataulukon soluihin esitettäväksi käyttäjälle.

## Lyhyt historia ##

Seuraavassa on joitain nopeita faktoja CSV-tiedostomuodon alkuperästä ja historiasta.

* 1972 - IBM Fortran (laajennettu H-tason kääntäjä) tuki niitä OS/360:ssa


* 1978 - FORTRAN 77 tuki luetteloohjattua syöttöä/tulostusta, joka käytti pilkkuja ja välilyöntejä erottimissa


* 2005 – CSV standardisoitiin [RFC4180](https://tools.ietf.org/html/rfc4180) MIME-sisältötyypiksi.


* 2013 - RFC4180:n puutteet käsiteltiin W3C-suosituksella


* 2015 - W3C teki ensimmäiset suositusluonnokset CSV-metatietostandardeista, jotka alkoivat suosituksesta joulukuussa 2015


## Muunna CSV-tiedostot ##

CSV-tiedostoja voidaan muuntaa useisiin eri tiedostomuotoihin käyttämällä sovelluksia, jotka voivat avata nämä tiedostot. Esimerkiksi Microsoft Excel voi tuoda tietoja CSV-tiedostomuodosta ja tallentaa ne XLS-, [XLSX](/spreadsheet/xlsx/)-, [PDF](/pdf/)-, [TXT](/word-processing/txt/)-, XML- ja [HTML](/web/html/)-tiedostomuotoihin. Vastaavasti muut työpöytä- ja verkkopalvelut tarjoavat mahdollisuuden viedä CSV-tiedostoja HTML-, ODS- ja [RTF](/word-processing/rtf/)-muotoihin.

## CSV-tiedostomuoto ##

CSV-tiedostomuodon tiedetään olevan määritetty kohdassa {{HYPERLINKKI}}. Se määrittää minkä tahansa tiedoston CSV-yhteensopivaksi, jos:

* Jokainen tietue sijaitsee erillisellä rivillä, jota rajaa rivinvaihto (CRLF). Esimerkiksi:

  * aaa,bbb,ccc CRLF
  * zzz,yyy,xxx CRLF
* Tiedoston viimeisessä tietueessa voi olla rivinvaihto. Esimerkiksi:

  * aaa,bbb,ccc CRLF
  * zzz,yyy,xxx
* Tiedoston ensimmäiseksi riviksi voi ilmestyä valinnainen otsikkorivi, joka on samassa muodossa kuin tavalliset tietuerivit. Tämä otsikko sisältää nimet, jotka vastaavat tiedoston kenttiä ja sen tulee sisältää sama määrä kenttiä kuin tietueet muussa tiedostossa (otsikkorivin olemassaolo tai puuttuminen tulee ilmoittaa tämän valinnaisen "header"-parametrin kautta. MIME-tyyppi). Esimerkiksi:

  * kentän_nimi,kentän_nimi,kentän_nimi CRLF
  * aaa,bbb,ccc CRLF
  * zzz,yyy,xxx CRLF
* ﻿Ylätunnisteessa ja jokaisessa tietueessa voi olla yksi tai useampia pilkuilla erotettuja kenttiä. Jokaisella rivillä tulee olla sama määrä kenttiä koko tiedostossa. Välilyöntejä pidetään osana kenttää, eikä niitä pidä jättää huomiotta. Tietueen viimeisen kentän jälkeen ei saa olla pilkkua. Esimerkiksi:

  * aaa,bbb,ccc
* Jokainen kenttä voi olla lainausmerkkien sisällä tai ei (jotkin ohjelmat, kuten Microsoft Excel, eivät kuitenkaan käytä lainausmerkkejä ollenkaan). Jos kenttiä ei ole suljettu lainausmerkeillä, lainausmerkkejä ei välttämättä näy kenttien sisällä. Esimerkiksi:\

  * aaa,bbb,ccc CRLF
  * zzz,yyy,xxx
* Kentät, jotka sisältävät rivinvaihtoja (CRLF), lainausmerkkejä ja pilkkuja, tulee laittaa lainausmerkkeihin. Esimerkiksi:

  * aaa,b CRLF
  * bb,ccc CRLF
  * zzz,yyy,xxx
* Jos kenttien sisällä käytetään kaksoislainausmerkkejä, kentän sisällä oleva kaksoislainausmerkki on vältettävä lisäämällä sen eteen toinen lainausmerkki. Esimerkiksi:

  * aaa,bbb,ccc

Nykyajan käytön valossa erotin ei kuitenkaan rajoitu vain pilkkuun, vaan se voi olla myös puolipiste, sarkain tai välilyönti. Sovellukset, kuten Microsoft Excel, tarjoavat mahdollisuuden määrittää erotinmerkin tietueiden tuomiseksi CSV-tiedostosta.

## Viitteet

* [RFC 4180](https://tools.ietf.org/html/rfc4180)

* [RFC 2048](https://tools.ietf.org/html/rfc2048)

* [CSV – Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)


