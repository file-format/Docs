{
  "date": "2023-08-03",
  "keywords": [
"usr",
"usr-tiedosto",
"mikä on usr-tiedosto",
"kuinka avata usr-tiedosto",
"tiedosto",
"usr tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "USR-tiedostomuoto - Lowrance GPS-datatiedosto",
  "description": "Opi USR-muodosta ja sovellusliittymistä, jotka voivat luoda ja avata USR-tiedostoja.",
  "linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr-fi",
      "parent": "gis"
}
},
  "lastmod": "2023-08-03"
}

## Mikä on USR-tiedosto?

.usr-tiedostopääte liittyy myös Lowrance GPS -laitteisiin. Sitä käytetään erityisesti GPS-tietojen tallentamiseen muodossa, joka tunnetaan nimellä User Data Format (USR-muoto), jota Lowrance GPS-laitteet käyttävät.

Kun käytät Lowrance GPS-yksikköä, voit tallentaa reittipisteet, jäljet ja reitit .usr-tiedostoina. Nämä tiedostot sisältävät yleensä tietoja, kuten leveysasteen, pituusasteen, korkeuden, aikaleiman ja muita GPS-toimintoihisi liittyviä tietoja.

Tässä on joitain yleisiä .usr-tiedostojen käyttötapoja Lowrance GPS -laitteissa:

- **Reittipisteet:** Reittipisteet ovat GPS:ään merkittyjä paikkoja, kuten maamerkkejä, suosikkikalastuspaikkoja tai kiinnostavia kohteita. Voit tallentaa nämä sijainnit .usr-tiedostoina, ja ne voidaan tuoda, viedä tai jakaa muiden Lowrance GPS-käyttäjien kanssa.

- ** Jäljet:** Jäljet edustavat GPS-liikkeiden tallennettua reittiä. Voit tallentaa jälkilokisi .usr-tiedostoina, jolloin voit tarkastella ja analysoida reittejäsi myöhemmin tai jakaa ne muiden kanssa.

- **Reitit:** Reitit ovat ennalta määritettyjä polkuja, jotka voit luoda ja tallentaa GPS-laitteellesi. Nämä reitit voidaan myös tallentaa .usr-tiedostoina myöhempää käyttöä tai jakamista varten.

Voit hallita .usr-tiedostoja Lowrance GPS -laitteessasi käyttämällä yleensä ohjelmistoja, kuten Lowrancen Insight Planner tai Lowrance GPS Utility GPS-tietojen tuomiseen, viemiseen ja käsittelemiseen.

## USR-tiedostomuoto - lisätietoja

Lowrance iFinder GPS -laitteissa .usr-tiedostot luodaan ja tallennetaan laitteeseen asetetulle MultiMediaCard (MMC) -muistikortille. Nämä tiedostot sisältävät käyttäjätietoja, kuten reittipisteitä, jälkiä ja reittejä.

Voit siirtää .usr-tiedostot MMC:stä tietokoneeseen seuraavasti:

- **Poista MMC:** Irrota MultiMediaCard (MMC) varovasti Lowrance iFinder GPS -laitteesta.

- **Aseta MMC tietokoneeseen:** Aseta muistikortti tietokoneesi kortinlukijapaikkaan sopivalla MMC-kortinlukijalla.

- **Etsi .usr-tiedostot:** Kun tietokoneesi tunnistaa MMC:n, sinun pitäisi pystyä käyttämään siihen tallennettuja tiedostoja. Etsi .usr-tiedostoja, jotka sisältävät GPS-tietosi.

- **Muuntaminen GPSBabelilla:** Jos haluat muuntaa .usr-tiedostot toiseen GPS-muotoon, voit käyttää GPSBabelia, joka on ilmainen ja avoimen lähdekoodin työkalu erilaisten GPS-tiedostomuotojen kanssa työskentelemiseen. GPSBabel tukee monenlaisia syöttö- ja tulostusmuotoja, joten voit muuntaa .usr-tiedostot muotoihin, jotka ovat yhteensopivia muiden GPS-ohjelmistojen tai -laitteiden kanssa.

Voit ladata GPSBabelin viralliselta verkkosivustolta (http://www.gpsbabel.org/) ja asentaa sen tietokoneellesi. Asennuksen jälkeen voit käyttää ohjelmiston komentorivikäyttöliittymää tai graafista käyttöliittymää (jos saatavilla) muunnoksen suorittamiseen.

Jos esimerkiksi haluat muuntaa .usr-tiedostot GPX-muotoon, voit käyttää seuraavaa komentoa:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

Yllä oleva komento kehottaa GPSBabelia lukemaan syöttötiedoston input.usr Lowrance USR -muodossa ja kirjoittamaan tulostiedoston output.gpx GPX-muodossa.

- **Käännettyjen tiedostojen tuonti/käyttö:** Muuntamisen jälkeen sinulla on GPS-tietosi uudessa muodossa (esim. GPX), jota voit käyttää muiden tätä muotoa tukevien GPS-ohjelmistojen tai -laitteiden kanssa.

## Kuinka avata USR-tiedosto?

Ohjelmat, jotka avaavat tai viittaavat USR-tiedostoihin, sisältävät

- GPSBabel (Windows)
- GPSBabel (Mac)
- GPSBabel (Linux)

## Viitteet
* [Lowrance Electronics](https://en.wikipedia.org/wiki/Lowrance_Electronics)


