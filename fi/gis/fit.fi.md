{
  "date": "2022-05-06",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FIT-tiedostomuoto - Garmin-toimintotiedosto",
  "description": "Opi FIT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata FIT-tiedostoja.",
  "linktitle": "FIT",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-fi-fit"
}
},
  "lastmod": "2022-05-06"
}

## Mikä on FIT-tiedosto?

FIT-tiedosto on Garminin puettavien urheilulaitteiden luoma GIS-tiedosto. Sitä käytetään henkilön toiminnan tallentamiseen, kun hän liikkuu näillä laitteilla. Toimintatiedot sisältävät GPS-laitteen tallentaman sijainnin ja ajan. FIT-tiedostoja käytetään myös tallennettujen aktiviteettitietojen siirtämiseen verkkosovellusliittymien avulla. Tästä syystä FIT-tiedostot ovat yleisimmin käytetty tiedostomuoto kuntotietojen jakamiseen muiden kuntoilualustojen kanssa. Muita yleisiä tiedostomuotoja ovat [GPX](/gis/gpx/), TCX ja [KML](/gis/kml/).

## FIT-tiedostomuoto - lisätietoja

FIT-tiedostot tallennetaan levylle binääritiedostoina Garmin-laitteiden tallentamien tietojen kanssa. FIT-tiedostoon tallennetut tiedot sisältävät:

 * Treffiaika
 * Urheilutyypit
 * Kierros- ja jakotiedot
 * GPS-reitti
 * Anturin tiedot
 * Tapahtumat aktiiviselle istunnolle

Toimintatiedot voidaan tallentaa tiedostoon reaaliajassa tai viedä, kun toiminnan tallennus on valmis.

### FIT-toimintaviestit

FIT-toimintotiedosto voi sisältää joitain vaadittuja viestityyppejä. Seuraavat ovat aktiviteettitiedoston pakolliset viestit.

|Viesti|Tarkoitus|
---|---|
|Tiedostotunnus| Kaikki FIT-tiedostotyypit vaativat File Id -sanoman, ja sen odotetaan olevan tiedoston ensimmäinen viesti. Toimintotiedostojen Tyyppi-ominaisuuden arvoksi tulee asettaa 4.|
|Toiminta| FIT Activity -tiedostossa vaaditaan yksi Activity-viesti. Toimintoviestiin sisältyvät paikallinen aikaleima ja istuntojen määrä -ominaisuudet. Paikallista aikaleimaa käytetään määrittämään aikavyöhykkeen siirtymä, jota voidaan käyttää kaikkiin tiedoston aikaleimoihin. Useimmat laitteet tallentavat FIT-tiedostoja reaaliajassa ja istuntojen määrä on tuntematon tallennuksen loppuun asti. Tästä johtuen Activity-viesti on usein tiedoston viimeinen viesti.|
|Istunto| Toimintatiedostot sisältävät yhden tai useamman istuntoviestin. Istuntoviesti on yhteenvetoviestityyppi. Aloitusaika, Kulunut kokonaisaika, Ajastimen kokonaisaika ja Aikaleima ovat pakollisia kenttiä kaikille yhteenvetoviesteille.|
|Kierrä| Kierrosviestit edustavat kierroksia tai intervalleja istunnon sisällä. Kierrosviesti on yhteenvetoviestityyppi. Aloitusaika, Kulunut kokonaisaika, Ajastimen kokonaisaika ja Aikaleima ovat pakollisia kenttiä kaikille yhteenvetoviesteille.|
|Ennätys| Tallennusviestit sisältävät GPS-koordinaatin, nopeuden, matkan, sykkeen, tehon jne.|

## FIT-tiedosto Hyödyllisiä resursseja

 * [FIT-toimintotiedostojen purkaminen](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
 * [FIT-toimintotiedostojen koodaus](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 
## Viitteet ##

* [FIT-toimintotiedosto](https://developer.garmin.com/fit/file-types/activity/)


