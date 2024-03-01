{
  "date": "2021-09-08",
  "keywords": [
"pcc-tiedosto",
"pcc-tiedostomuoto",
"mikä on pcc-tiedosto",
"tiedosto",
"pcc esimerkki",
"pcc tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi Mass Effect PCC-tiedostomuodosta ja API:ista, jotka voivat luoda ja avata PCC-tiedostoja.",
  "title": "PCC - Mass Effect -pakettitiedosto",
  "linktitle": "PCC",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-pc-fic"
}
},
  "lastmod": "2021-09-08"
}

## Mikä on PCC-tiedosto?

.pcc-tiedosto on [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3)-tiedosto, joka sisältää pelitietoja pelin sisällön, kuten mallien, pintakuvioiden ja huoneiden, muokkaamiseksi. Mass Effect 2 ja 3 ovat ensimmäisiä räiskintäpelejä, jotka perustuvat Unreal Engine 3 -pelimoottoriin. Pelin kehitti alun perin [Bioware](https://www.bioware.com/about/), joka piti suurimman osan peliresursseista omassa PCC-tiedostomuodossaan. Biowaren osti Electronic Arts, johtava kansainvälinen interaktiivisen viihteen kustantaja.

## PCC-tiedostomuoto - lisätietoja

PCC-tiedostot sisältävät pakattuja ja/tai pakkaamattomia rakenteita, jotka vaikuttavat tiedostojen yleiseen järjestykseen.

### Pakattu PCC-rakenne

Pakattu PCC-tiedosto koostuu taulukoista ja tiedoista, jotka on segmentoitu paloiksi. Jokainen pala sisältää vaihtelevan määrän pakattuja lohkoja.

 * Chunks Header - 16 tavun yhteinen otsikko, joka sisältää tietoja paloista.
 * Chunk Header - 16-tavuinen otsikko, joka sisältää tietoja lohkolomakkeen sisältämistä raaka-pakatuista tiedoista.

### Pakkaamaton PCC-rakenne

Pakkaamattomat PCC-tiedostot on jaettu seuraaviin viiteen osaan.

 * Otsikko - sisältää perustiedot PCC-tiedoston rakenteesta.
 * Nimitaulukko - sisältää paketin sisällä olevan nimen, mukaan lukien tuontiluokat, vienti- ja vientiominaisuudet.
 * Import Table - sisältää kaikki PCC:n tuomat luokat ja objektit.
 * `Export Table` - sisältää kaikki pakettiin tallennetut objektit. Jokainen vienti voi vaihdella kooltaan.

## Viitteet

 * [Me3Explorer – PCC-tiedostomuoto](https://me3explorer.fandom.com/wiki/PCC_File_Format)
 * [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3)
 * [Bioware](https://www.bioware.com/about/)

