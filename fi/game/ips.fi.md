{
   "date":"2023-09-21",
   "keywords":[
"ips",
"ips-tiedosto",
"ips sisäinen korjausjärjestelmän korjaustiedosto",
"mikä on ips-tiedosto",
"kuinka avata ips-tiedosto",
"ips tiedostopääte",
"laajennus",
"tiedosto"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"IPS-tiedostomuoto - Sisäinen korjausjärjestelmän korjaustiedosto",
   "description":"Opi IPS Internal Patching System Patch File -muodosta ja API:ista, jotka voivat luoda ja avata IPS-tiedostoja.",
   "linktitle":"IPS",
   "menu":{
      "docs":{
         "identifier":"game-ips-fi",
         "parent":"game"
}
},
   "lastmod":"2023-09-21"
}

## Mikä on IPS-tiedosto?

IPS-tiedosto viittaa tyypillisesti sisäiseen korjausjärjestelmän korjaustiedostoon. IPS on lyhenne sanoista International Patching System, ja se on tiedostomuoto, jota käytetään korjausten luomiseen ja käyttämiseen ROM-tiedostoille (Read-Only Memory), usein videopelien emuloinnin ja ROM-hakkeroinnin yhteydessä.

Näin se toimii:

- **Alkuperäinen ROM:** Aloitat alkuperäisestä ROM-tiedostosta, joka on olennaisesti kopio videopelistä tai ohjelmistosta, joka on tallennettu ROM-muotoon. Tämä tiedosto on yleensä vain luku -tilassa, joten et voi muokata sitä suoraan.

- **IPS-korjaustiedosto:** IPS-korjaustiedosto sisältää muutokset, jotka haluat soveltaa alkuperäiseen ROM-muistiin. Nämä muutokset voivat olla virheenkorjauksia, käännöksiä tai muita muutoksia.

- **Patch Application:** Muutosten käyttöönottoa varten tarvitset apuohjelman tai ohjelman, joka voi lukea IPS-korjaustiedoston ja asentaa sen alkuperäiseen ROM-muistiin. Tämä prosessi olennaisesti korjaa alkuperäisen ROM-tiedoston IPS-tiedostossa määritetyillä muutoksilla ja luo muokatun ROM-tiedoston.

- **Muokattu ROM:** Tuloksena on muokattu ROM, joka sisältää muutokset IPS-korjaustiedostosta. Tätä muokattua ROM-muistia voidaan sitten käyttää emulaattorissa tai yhteensopivassa laitteistossa pelin pelaamiseen halutuilla muokkauksilla.

Näitä korjaustiedostoja käytetään tyypillisesti pelien muutosten tai parannusten tekemiseen, ja ne voivat sisältää erilaisia muutoksia, mukaan lukien grafiikan, mallien ja muiden pelitietojen muutokset. IPS-tiedostot soveltuvat erityisen hyvin suhteellisen pienille, tyypillisesti alle 16 megatavua kooltaan korjauksille.

Seuraavassa osiossa tutkimme IPS-tiedostoihin liittyviä ohjelmistosovelluksia.

## Kuun IPS

Lunar IPS on suosittu ja käyttäjäystävällinen apuohjelma, jota käytetään IPS (Internal Patching System) -korjausten luomiseen ja asentamiseen ROM-tiedostoille. Tässä on joitain tärkeimpiä ominaisuuksia ja tietoja Lunar IPS:stä:

- **Pach Creation:** Lunar IPS:n avulla käyttäjät voivat luoda IPS-korjauksia määrittämällä muutokset, jotka he haluavat tehdä alkuperäiseen ROM-tiedostoon. Voit valita alkuperäisen ROM:n ja muokatun version, ja Lunar IPS luo IPS-korjaustiedoston näiden kahden tiedoston välisten erojen perusteella.

- **Patch Application:** Kun sinulla on IPS-korjaustiedosto, Lunar IPS antaa sinun asentaa sen alkuperäiseen ROM-muistiin. Tämä prosessi olennaisesti korjaa ROMin IPS-tiedostossa määritetyillä muutoksilla ja luo muokatun ROM:n.

- **Kevyt:** Lunar IPS on pieni ja kevyt ohjelma, mikä tarkoittaa, että se ei kuluta paljon järjestelmäresursseja ja se on nopea ladata ja suorittaa.

## IPSWin

IPSWin on ensisijaisesti Windows-käyttäjille suunniteltu apuohjelma, joka helpottaa IPS (Internal Patching System) -korjausten luomista ja soveltamista ROM-tiedostoihin. Se on suoraviivainen ja käyttäjäystävällinen työkalu, joka sopii niille, jotka haluavat korjata ROM-levyjä helposti. Tässä vähän tietoa IPSWinistä:

- **Pach Creation:** IPSWinin avulla käyttäjät voivat luoda IPS-korjauksia vertaamalla kahta ROM-tiedostoa: alkuperäistä ROM-muistia ja muokattua ROM-muistia. Se tunnistaa näiden kahden tiedoston väliset erot ja luo IPS-korjaustiedoston, joka sisältää kyseiset muutokset.

- **Patch Application:** Tämän apuohjelman avulla käyttäjät voivat myös käyttää olemassa olevia IPS-korjaustiedostoja alkuperäisiin ROM-levyihin. Valitsemalla sopivan IPS-korjauksen ja alkuperäisen ROM-levyn, IPSWin yhdistää muutokset uudeksi ROM-tiedostoksi ja luo korjatun version.

## Kuinka avata IPS-tiedosto?

IPS-tiedostoja avaavia ohjelmia ovat mm

- Kuun IPS
- IPSWin
- MultiPatch

## Muut IPS-tiedostot

Tässä on muita tiedostotyyppejä, jotka käyttävät **.ips**-tiedostotunnistetta.

- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

## Viitteet
* [Lunar IPS](https://www.romhacking.net/utilities/240/)
