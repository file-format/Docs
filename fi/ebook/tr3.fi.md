{
  "date": "2021-04-10",
  "keywords": [
"TR3",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"eBook",
"TomeRaider",
"Yadabyte"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Opi TR3-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata TR3-tiedostoja.",
  "title": "TR3 - TomeRaider 3 eBook File",
  "linktitle": "TR3",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-tr-fi3"
}
},
  "lastmod": "2021-04-10"
}

## Mikä on TR3-tiedosto? ##

TR3-tiedosto on TomeRaider 3 eBook, joka tukee nopeaa hakua ja pakkausta. Se voi toimia oikein TomeRaideriin liittyvän ohjelman kautta. Yadabyte on tämän ohjelmiston kehittäjä, brittiläinen ohjelmisto- ja verkkokehitysyritys, jonka kotipaikka on Yhdistyneessä kuningaskunnassa. TomeRaider eBook Reader -sovellusta voidaan käyttää näiden TR3-tiedostojen asianmukaiseen toimintaan ja sisällön hallintaan. Tämä asiaan liittyvä eBook-lukija voidaan asentaa tietokoneisiin, joissa on Microsoft Windows -pohjaiset järjestelmät ja monet siirrettävät gadgetit. TR3-tiedosto kuuluu eBook Files -ryhmään, jota käytetään käyttöjärjestelmissä, kuten Windows 10, Windows 7, Windows 8 / 8.1, Windows Vista, Windows XP.

TR3-kohtaiset **HTML-tunnisteet** ovat seuraavat:

|Tagi|Kuvaus|
---|---|
|\<new> |Jos haluat luoda TomeRaider-tiedostoja tekstitiedostoista, uusi tunniste riittää.<new> -tunniste määrittää sivujen alun.|
|\<CATDEF> ... \</CATDEF> |määrittää luokan nimen|
|\<META> ... \</META> |on tunniste, jota käytetään määrittelemään kaikki tiedostomuodossa käytetyt metatiedot. Tämä tunniste sisältää useita parametreja.|
|\<EXPMSG> |Tämä tunniste ohjaa sanomaa, joka tulee näkyviin, kun tiedosto on vanhentunut. Aina kun käyttäjä yrittää tarkastella sivua sen jälkeen, kun tiedosto on vanhentunut, vanhenemisviesti tulee näkyviin todellisen sivun tekstin sijaan.|
|\<DIEMSG> |Tämä tunniste on samanlainen kuin EXPMSG. Sitä käytetään näyttämään viesti, kun tiedosto kuolee.|
|\<ENGMSG> |Tätä tunnistetta käytetään luomaan viesti, joka näytetään salatuille sivuille. Viesti tulee näkyviin sivun tekstin sijaan, jos käyttäjä yrittää avata salatun sivun ennen sen lukituksen avaamista.|
|\<expmsg> ,\<diemsg> ja \<encmsg> |Ohitettu sivun tekstissä. Ne on sijoitettava tiedoston otsikko-osioon ennen ensimmäistä<new> tag.|
|\<SELECTION> . \</ SELECTION> |Käytetty tukemaan kyselyitä. Tämän tagin on oltava ennen ensimmäistä<new> tag. Se kokoaa valintatiedot käyttäjän kyselyä varten.|
|\<catset> . \</catset> | Käytetään luokkien nimeämiseen kullekin aiheelle.|


## Ongelmia avattaessa TR3-tiedostoa ##

Tässä on luettelo yleisistä ongelmista, joita saattaa ilmetä ja jotka voivat aiheuttaa tiedostomuodon toimintahäiriöitä:

* Vioittunut tiedosto
* Viruksen saastunut tiedosto
* Virheelliset linkit TR3-tiedostoon arkistokäytöissä
* Järjestelmässä ei ole pääsyoikeutta tiedostojen avaamiseen
* Vanhentunut asema järjestelmässäsi
* TR3:n raportin poistaminen Windowsin arkistosta
* Yhteyden ottaminen kehittäjään voi olla parempi vaihtoehto paremman tuloksen saamiseksi

