{
  "date": "2021-07-15",
  "keywords": [
"LNK",
"laajennus",
"tiedosto",
"muoto",
"järjestelmä",
"LNK tiedosto",
"linkki",
"LNK tiedostot",
"LNK asiakirjat",
"sovellus",
"ohjelmia"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "LNK - Linkkitiedostomuoto",
  "description": "Opi LNK-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata LNK-tiedostoja.",
  "linktitle": "LNK",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-ln-fik"
}
},
  "lastmod": "2021-07-15"
}

## Mikä on LNK-tiedosto? ##

LNK-tiedosto, joka on analoginen Mac-järjestelmän identiteetin kanssa, on Windows-vaihtoehto tai linkki, joka toimii yhteytenä alkuperäiseen kuvatiedostokansioon tai -ohjelmaan. Se sisältää pikakuvakkeen tyypin, sijainnin ja tiedostonimen sekä kohdeasiakirjan avaavan sovelluksen ja ylimääräisen pikanäppäimen.

Suorita Windowsissa tiedosto, kansio tai suoritettava ohjelma ja valitse Luo pikakuvake. Tiedostomuodon sijainti ja Alku-hakemisto ovat LNK-tiedostojen kaksi perusominaisuutta. LNK-tiedostojen tiedostomuoto on peitetty, ja kaareva nuoli osoittaa, että ne ovat pikakuvakkeita.

## LNK-tiedostomuoto ##

LNK-tiedostomuodoissa on yleensä sama kuvake kuin niiden kohdetiedostoissa, mutta niihin on lisätty pieni kierretty nuoli, joka osoittaa, että tiedosto osoittaa eri sijaintiin. Kun pikakuvaketta kaksoisnapsautetaan, se käyttäytyy kuin käyttäjä olisi kaksoisnapsauttanut varsinaista tiedostoa.

Sovellusten pikakuvakkeita sisältävillä LNK-tiedostoilla voi olla ominaisuuksia, jotka vaikuttavat ohjelman toimintaan. Jos haluat muuttaa määritteitä, napsauta pikakuvaketiedostoa hiiren kakkospainikkeella ja valitse **Ominaisuudet** ja muuta sitten Kohde-kenttää.

Tiedostotunnisteiden sijaan LNK-tiedostot ovat Windows Explorerin laajennuksia. Päätelaitteena .lnk-dokumentteja voidaan käyttää vain Windowsin Resurssienhallinnassa tiedoston korvaamiseen, ja niillä on muitakin tarkoituksia Windowsin Resurssienhallinnassa paikallisen asiakirjan pikakuvakkeen lisäksi. Nämä tiedostot alkavat myös kirjaimella L.

Vaikka pikakuvakkeet linkittävät tiettyihin tiedostoihin ja hakemistoihin niitä luodessaan, ne voivat muuttua käyttökelvottomiksi, jos kohde muutetaan toiseen paikkaan. Explorer alkaa korjata pikakuvakekansiota, joka osoittaa kuolleeseen kohteeseen, kun se avataan.


## Tekniset tiedot ##

Vain kun Piilota tunnistettujen tiedostotyyppien laajennukset -kansion katseluasetusta ei ole valittu, Windows ei näytä .lnk-dokumenttitunnistetta asiakirjan pikakuvakkeille. Vaikka se ei ole suositeltavaa, voit ottaa tiedostotunnisteen näyttämisen käyttöön poistamalla NeverShowExt-ominaisuuden HKEY_CLASSES_ROOT\lnk-tiedoston Windowsin rekisterikohdasta.

Voit tehdä sen seuraavasti:

* Avaa Registration Editor kirjoittamalla Regedit tehtäväpalkin hakukenttään ja valitsemalla ohjelma
* Siirry sovelluksessa kohtaan Computer\HKEY HKEY_CLASSES_ROOT\lnkfile
* Tee varmuuskopio tuotteesta napsauttamalla sitä hiiren kakkospainikkeella ja valitsemalla Vie
* Valitse ja poista NeverShowExt-attribuutti
* Windows on käynnistettävä uudelleen


## Viite ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
