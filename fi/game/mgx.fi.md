{
  "date": "2021-09-08",
  "keywords": [
"mgx tiedosto",
"mgx tiedostomuoto",
"mikä on mgx-tiedosto",
"tiedosto",
"mgx esimerkki",
"mgx tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi Age of Empires 2 Expansion Replay MGX -tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MGX-tiedostoja.",
  "title": "MGX - Age of Empires 2 -laajennuksen uusinta",
  "linktitle": "MGX",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mg-fix"
}
},
  "lastmod": "2021-09-08"
}

## Mikä on MGX-tiedosto?

Tiedosto, jonka pääte on .mgx, on tallennettu tiedosto Age of Empires II: The Conquerors -peliin, joka voidaan toistaa Age of Empires II -ohjelmassa. Se sisältää täydellisen tallenteen käyttäjän pelaamasta kampanjasta. Se voidaan ladata ja toistaa Age of Empires II -ohjelmassa. Kun peli on pelattu uudelleen, se näyttää kaikki tapahtumat ja skenaariot, jotka käyttäjä suunnitteli kampanjaa varten ja pelasi.

## MGX-tiedostomuoto - lisätietoja

The internal file format of the MGX file have been worked out and available as partially validated information on [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format). The specifications outline the details in the following sections.

### Rakenteen määritelmät

GPX-tiedostomuodon rakennemääritelmien uskotaan perustuvan {{HYPERLINKKI}}:iin, jotka tarjoavat tavan lukea ja kirjoittaa strukturoitua binaaridataa. Tämä antaa ohjelmoijalle mahdollisuuden määrittää binääritietojen muodon, jonka BinData sitten lukee ja kirjoittaa.

### MGX Messaging

MGX-viestintä perustuu kahdentyyppisiin viesteihin.

 * GAMESTART - määrittää pelin aloituskomennot, eikä sitä ole vielä vahvistettu
 * CHAT - kuvaa pelin sisäisiä chat-viestejä. Sekä pelaajat että itse peli (Gaia) voivat lähettää pelin sisäisiä viestejä.

### PELITOIMENPITEET

Useita {{HYPERLINKKI}} on haettu ja joiden tiedot ovat saatavilla.

## Viitteet

* [Age of Empires 2: The Conquerors – Savegame-tiedostomuodon määritykset](https://github.com/stefan-kolb/aoc-mgx-format)


