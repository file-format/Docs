{
  "date": "2021-03-08",
  "keywords": [
"RB",
"Nuvo Median Rocket eBook -laite",
"file",
"laajennus",
"muoto",
"eBook"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi Nuvo Median Rocket eBook -laitteen RB-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata RB-tiedostoja.",
  "title": "RB - Rocket eBook File",
  "linktitle": "RB",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-r-fib"
}
},
  "lastmod": "2021-03-08"
}

## Mikä on RB-tiedosto?

The file with extension .rb holds the Rocket eBook content. The Rocket eBook is actually a device made by Nuvo Media; they released this device in 1998. Vaikka Rocket eBook pystyy näyttämään kuvia, mutta vain mustavalkoisena. Sen näyttö on 106 dpi tai 480 x 320 pikseliä 4,5 x 3 tuuman kosketusnäytöllä. Rocket eBook muodostaa yhteyden tietokoneeseen sarjaportin kautta e-kirjojen lataamista varten RB-tiedostomuodossa. RB-tiedostot pystyvät käyttämään DRM:ää, mutta tätä tekniikkaa ei käytetä nykyaikaisissa e-kirjoissa. RB-tiedosto sisältää perinteisesti HTML-tiedoston kuvineen ja pseudo-OPF-tiedoston, jossa on kaikki metatiedot (.info).

## RB-tiedostomuodon ## tekniset tiedot

Maaginen luku (heksadesimaalilukuna) näkyy tiedoston ensimmäisissä 4 tavussa: B0 0C B0 0C.

Näyttää siltä, että seuraavat kaksi tavua ovat versionumero, kuten 02 00, joka tarkoittaa pääversiota 2 ja sivuversiota 0.

Seuraavat neljä tavua sisältävät tekstin NUVO, jota seuraa 4 tavua 00h.

The next 4-byte is the date when the book was created, encoded as an int16. Tämä asettaa meidät offsetille 0Eh. ORocketLibraryn vanha versio koodasi vuoden täyden arvon (eli 1999 oli CF 07, 2000 oli D0 07). Uusimmassa versiossa tm_year on tallennettu sanatarkasti, eli 100 vuodelle 2000 (64 00). Vuoden jälkeen tulee int8, joka edustaa 1-suhteellista kuukauden numeroa, ja int8, joka edustaa kuukauden päivää.

Seuraavat 6 tavua ovat 00h. Ajan asetusta varten nämä voidaan varata.

Sisällystaulukon absoluuttinen siirtymä sisältyy int32:een offsetissa 18h.

Tämän jälkeen on int32, joka sisältää .rb-tiedoston pituuden. Tätä käytetään määrittämään, ovatko tiedostot täydellisiä vai eivät.

Tämä koko tavupala (20 h - 128 h) näyttää tarvitsevan vain salattua otsikkoa. Salaamattomissa nimikkeissä ne ovat aina nolla.

Useimmissa tapauksissa sisällysluettelo seuraa (siirtymä 128). Se alkaa ToC:n sivu-merkintöjen (.rb-tiedostoosien) int32-määrällä. Jokainen merkintä koostuu nimestä (nolla täytetään 32 tavuun), jota seuraa 3 int32:ta: datasegmentin pituus, sijainti .rb-tiedostossa ja tämän merkinnän lippu. Nykyään tunnetut arvot ovat: 1 (salattu), 2 (tietosivu) ja 8 (deflatoitu). Kaikki nimet on räätälöity tarpeen mukaan, jotta ne ovat ainutlaatuisia.

## Viitteet

* [E-Reader - MobileRead](https://en.wikipedia.org/wiki/E-reader)


