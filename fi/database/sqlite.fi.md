{
  "date": "2019-12-12",
  "keywords": [
"SQLite",
"laajennus",
"tiedosto",
"tiedosto muoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"Tietokantatiedostot"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi SQLITE-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata SQLITE-tiedostoja.",
  "title": "SQLite-tiedostomuoto",
  "linktitle": "SQLITE",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sqlit-fie"
}
},
  "lastmod": "2020-11-09"
}

## Mikä on SQLite-tiedosto?

Tiedosto, jonka laajennus on .sqlite, on kevyt SQL-tietokantatiedosto, joka on luotu [SQLite](https://www.sqlite.org/index.html)-ohjelmistolla. Se on itse tiedostossa oleva tietokanta ja toteuttaa itsenäisen, monipuolisen, erittäin luotettavan [SQL](/database/sql/)-tietokantamoottorin. SQLite-tietokantatiedostoja voidaan käyttää monipuolisen sisällön jakamiseen järjestelmien välillä yksinkertaisesti vaihtamalla nämä tiedostot verkon yli. Lähes kaikki matkapuhelimet ja tietokoneet käyttävät SQLitea tietojen tallentamiseen ja jakamiseen, ja se on tiedostomuoto valinta monikäyttöisille sovelluksille. Kompaktin käytön ja helpon käytettävyyden ansiosta se toimitetaan muiden sovellusten mukana. SQLite-sidoksia on olemassa ohjelmointikielille, kuten C, [C#](/programming/cs/), [C++](/programming/cpp/), [Java](/programming/java/), [PHP](/programming/php/) ja monille muille.

## SQLite-tiedostomuoto

SQLite on todellisuudessa C-kielikirjasto, joka toteuttaa SQLite RDBMS:n SQLite-tiedostomuodolla. Uusien laitteiden kehittyessä joka päivä, sen tiedostomuoto on pidetty taaksepäin yhteensopivana vanhojen laitteiden kanssa. SQLite-tiedostomuotoa pidetään tietojen pitkän aikavälin arkistointimuotona.

### Tietokantatiedosto

SQLite-tietokantaa ylläpidetään täysin kahden tiedoston kautta.
 * Päätietokantatiedosto - Sisältää SQLite-tietokannan täydellisen tilan
 * Palautuspäiväkirja - Tallentaa lisätietoja toiseen tiedostoon ja sitä käytetään tapahtumien suorittamisen aikana. Jos SQLite on WAL-tilassa, kirjoituspään lokitiedostoa ylläpidetään.

#### Päiväkirjatiedosto

Tämä tiedosto on tarkoitettu säilyttämään kaikki ylläpidetyt tiedot siltä varalta, että viimeistä tapahtumaa ei voitu suorittaa loppuun esimerkiksi tietokoneen kaatumisen vuoksi. Tätä tiedostoa käytetään tietokantatiedoston palauttamiseen yhdenmukaiseen tilaan.

#### Sivut

SQLite-päätietokantatiedosto koostuu yhdestä tai useammasta sivusta. Jokaisella päätietokannan sivulla on milloin tahansa yksi käyttökerta, joka on yksi seuraavista:

 * Lukitustavusivu
 * Freelist-sivu
   * Freelist runkosivu
   * Vapaalistan lehtisivu
 * B-puun sivu
   * Pöytä b-puun sisäsivu
   * Taulukko b-puun lehtisivu
   * Hakemiston b-puun sisäsivu
   * B-puun lehtisivu
 * Hyötykuorman ylivuotosivu
 * Osoitinkarttasivu

SQLite-tietokantatiedostojen koko voi vaihdella muutamasta kilotavusta muutamaan gigatavuun.

### SQLite-otsikko

The SQLite database header is located in the first 100 bytes of the database file. Every valid SQLite database file starts with 16 bytes (in hex):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Otsikkokenttien tiedot ovat kuten seuraavassa taulukossa.

|Offset|Koko|Kuvaus|
---|---|---|
|0|16|Otsikkomerkkijono: SQLite-muoto 3\000|
|16|2|Tietokannan sivun koko tavuina. On oltava potenssi kaksi välillä 512–32768, tai arvon 1, joka edustaa sivukokoa 65536.|
|18|1|Tiedostomuodossa kirjoitusversio. 1 perinnölle; 2 WAL:lle.|
|19|1|Tiedostomuodon lukuversio. 1 perinnölle; 2 WAL:lle.|
|20|1|Tavua käyttämätöntä varattua tilaa jokaisen sivun lopussa. Yleensä 0.|
|21|1|Mainin upotetun hyötykuorman osuus. Täytyy olla 64.|
|22|1|Sisäänrakennetun hyötykuorman vähimmäisosuus. Täytyy olla 32.|
|23|1|Lehtien hyötykuorman osuus. Täytyy olla 32.|
|24|4|Tiedostojen muutoslaskuri.|
|28|4|Tietokantatiedoston koko sivuina. Otsikon sisäisen tietokannan koko.|
|32|4|Ensimmäisen vapaalistan runkosivun sivunumero.|
|36|4|Vapaalistan sivujen kokonaismäärä.|
|40|4|Kaavaeväste.|
|44|4|Kaavamuodon numero. Tuetut skeemamuodot ovat 1, 2, 3 ja 4.|
|48|4|Sivun välimuistin oletuskoko.|
|52|4|Suurin b-puun juurisivun sivunumero automaattityhjiö- tai inkrementaalityhjiötilassa tai muuten nolla.|
|56|4|The database text encoding. A value of 1 means UTF-8. Arvo 2 tarkoittaa UTF-16le. Arvo 3 tarkoittaa UTF-16be.|
|60|4|Käyttäjäversio, jonka user_version pragma lukee ja asettaa.|
|64|4|True (ei nolla) inkrementaalista tyhjiötilaa varten. Epätosi (nolla) muuten.|
|68|4|PRAGMA application_id.|:n asettama sovellustunnus.
|72|20|Varattu laajennusta varten. Täytyy olla nolla.|
|92|4|Versio-valid-for number.|
|96|4|SQLITE_VERSION_NUMBER|

## Viitteet ##

* [SQLite-tiedostomuoto - SQLite](https://www.sqlite.org/fileformat2.html)

* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)

* [SQLite - C Language Specs](https://www.sqlite.org/c3ref/intro.html)


