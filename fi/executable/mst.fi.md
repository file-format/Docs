{
  "date": "2021-06-30",
  "keywords": [
"mst-tiedosto",
"mst-tiedostomuoto",
"mikä on mst-tiedosto",
"tiedosto",
"mst esimerkki",
"mst tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi MST-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MST-tiedostoja.",
  "title": "MST - Windows Installer -pakettitiedosto",
  "linktitle": "MST",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ms-fit"
}
},
  "lastmod": "2021-06-30"
}

## Mikä on MST-tiedosto?
.mst-tunnisteella varustettuja tiedostoja käytetään MSI-paketin sisällön muuntamiseen. Järjestelmänvalvojat käyttävät niitä yleisesti mukautettujen asetusten soveltamiseen olemassa olevaan MSI-tiedostoon. MST-tiedostoja käytetään yhdessä alkuperäisen MSI-paketin kanssa ohjelmistojen jakelujärjestelmissä, kuten ryhmäkäytännöissä. MST-tiedostoja käytetään yleensä ohjelmistokehityksessä ja -testauksessa niiden kehitteillä olevien ohjelmistoversioiden määrittämiseen.

## MST-tiedostomuoto
MST- tai Transform-tiedostoa käytetään keräämään asennusvaihtoehdot ohjelmille, jotka käyttävät tiedostossa Microsoft Windows Installeria. Näitä tiedostoja käytetään yleisesti Installer (MSIEXEC.EXE) -komentorivillä tai ohjelmistoasennuksen ryhmäkäytännössä. Microsoft Active Directory -toimialueella. MST-tiedostoja voidaan käyttää myös käärittyjen suoritettavien asennusohjelmien kanssa. Yleinen tapaus on, että joku haluaa välittää komentorivin parametreja paketoidulle asennusohjelmalle. Tätä varten tarvitset MST-tiedoston, joka lisää WRAPPED_ARGUMENTS-ominaisuuden ominaisuustaulukkoon. Näitä tiedostoja ei voi luoda tai muokata yleisillä muokkausohjelmilla. Tätä tarkoitusta varten on saatavilla erityisiä työkaluja.

### Kuinka käyttää MST-tiedostoja?
MST-tiedostoja voidaan luoda erilaisilla työkaluilla, ja Ocraa käytetään yleensä MST-tiedostojen luomiseen. Sitten asetuksia voidaan mukauttaa tarpeen mukaan ja tallentaa ne tiettyyn paikkaan. Tämän jälkeen MST-tiedostoja voidaan käyttää yhdessä MSI-tiedostojen kanssa. Jos haluat testata näitä tiedostoja; käytä seuraavaa syntaksia komentorivillä

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### MUUNTAA omaisuutta

Voit myös käyttää Windowsin asennusohjelman **TRANSFORMS**-ominaisuutta, joka on itse asiassa luettelo muutoksista, joita asennusohjelma käyttää pakettia asentaessaan. Asennusohjelma suorittaa muunnokset samassa järjestyksessä kuin ne on lueteltu TRANSFORM-ominaisuudessa. Muunnokset voidaan määrittää tiedostonimellä .mst-tunnisteella tai täydellä polulla. Jos haluat määrittää useamman kuin yhden muunnoksen, erota kukin tiedostonimi tai puolipiste seuraavan esimerkin mukaisesti.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Viitteet 

* [MST Transformation Files](https://www.exemsi.com/documentation/mst-transformation-files/)

* [TRANSFORMS-ominaisuus](https://learn.microsoft.com/en-us/windows/win32/msi/transforms)



