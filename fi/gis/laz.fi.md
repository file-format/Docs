{
  "date": "2023-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LAZ - Pakattu LIDAR-tiedonvaihtotiedosto",
  "description": "Opi LAZ-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata LAZ-tiedostoja.",
  "linktitle": "LAZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-la-fiz"
}
},
  "lastmod": "2023-07-18"
}

## Mikä on LAZ-tiedosto?

LAZ-tiedostomuoto on pakattu versio LAS (Lidar LASer) -tiedostomuodosta, joka on suunniteltu erityisesti lidar-pistepilvitietojen tallentamiseen. LAZ-tiedostot säilyttävät samat tiedot ja rakenteen kuin LAS-tiedostot, mutta käyttävät häviötöntä pakkaustekniikkaa tiedoston koon pienentämiseksi säilyttäen samalla alkuperäisen tiedon tarkkuuden.

## LAZ-tiedostomuoto - lyhyt historia

LAZ-tiedostomuoto kehitettiin vastaamaan kasvavaan kysyntään suurten lidar-tietosarjojen tehokkaan tallennuksen ja siirron osalta. Pakkaamalla LAS-tiedostoja LAZ-tiedostot pienentävät merkittävästi kokoaan, mikä helpottaa niiden hallintaa ja siirtämistä. Pakkaus saadaan aikaan käyttämällä eri algoritmien yhdistelmää, kuten entropiakoodausta ja muuttuvapituista koodausta, Lidar-pisteattribuuttien esittämiseksi kompaktimmin.

## LAZ tiedostomuoto

Pakkaamisesta huolimatta LAZ-tiedostot säilyttävät kyvyn palauttaa alkuperäiset LAS-tiedot täysin ilman tietojen menetystä. Tämä tarkoittaa, että kun LAZ-tiedosto on purettu, sitä voidaan käsitellä ja analysoida samalla tavalla kuin pakkaamatonta LAS-tiedostoa. Pakkaus- ja purkuprosessi suoritetaan tyypillisesti LAZ-muotoa tukevilla erikoisohjelmistoilla tai kirjastoilla.

LAZ-tiedostomuoto säilyttää yhteensopivuuden LAS-tiedostojen kanssa, mikä varmistaa yhteentoimivuuden lidar-ohjelmistojen ja käsittelytyökalujen välillä. Tämä tarkoittaa, että sovellukset, jotka voivat lukea ja käsitellä LAS-tiedostoja, voivat yleensä käsitellä LAZ-tiedostoja ilman muutoksia. Lisäksi LAZ-tiedostot sisältävät edelleen tiedoston otsikon, muuttuvapituisia tietueita (VLR) ja pistetietotietueita, säilyttäen saman rakenteen kuin LAS-tiedostot.

## LAZ-tiedostomuodon edut

**Pienempi tiedostokoko:** LAZ-pakkaus pienentää merkittävästi lidar-tietojoukkojen tiedostokokoa, mikä tekee niistä helpommin hallittavissa ja helpompia tallentaa ja siirtää.

**Tietojen eheys:** LAZ-pakkaus on häviötöntä, mikä tarkoittaa, että purettu data on tarkka kopio alkuperäisestä LAS-tiedosta, mikä varmistaa, että tietoja tai tarkkuutta ei menetetä.

**Yhteentoimivuus:** LAZ-tiedostot ovat yhteensopivia LAS-tiedostojen kanssa, mikä mahdollistaa saumattoman integroinnin olemassa olevien lidar-ohjelmistojen ja työnkulkujen kanssa.

**Tehokas käsittely:** Pienentyneen koonsa ansiosta LAZ-tiedostot voidaan ladata ja käsitellä nopeammin, mikä parantaa kokonaiskäsittely- ja analysointiaikoja.

LAZ-tiedostomuoto on otettu laajalti käyttöön lidar-yhteisössä pakatun lidar-tietojen tallennuksen ja vaihdon standardina. Se tarjoaa tasapainon tehokkaan tietojen pakkaamisen ja tietojen eheyden välillä, mikä mahdollistaa suurten lidar-tietosarjojen helpomman käsittelyn säilyttäen samalla alkuperäisen tiedon tarkkuuden ja laadun.

## Viitteet

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
