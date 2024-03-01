{
  "date": "2021-06-29",
  "keywords": [
"CUR",
"laajennus",
"tiedosto",
"muoto",
"kuva",
"Laitteesta riippumaton bittikartta",
"Kohdistimen tiedostomuoto",
"Kursori",
"Windows",
"sovellus"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CUR - Kohdistimen tiedostomuoto",
  "description": "Opi CUR-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CUR-tiedostoja.",
  "linktitle": "CUR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-cu-fir"
}
},
  "lastmod": "2021-06-29"
}

## Mikä on CUR-tiedosto? ##

CUR-tiedosto on staattinen Microsoft Windowsin kohdistintiedostomuoto. Pohjimmiltaan ne ovat kiinteitä kuvia, jotka ovat identtisiä ICO (kuvake) -tiedostojen kanssa kaikilta osin paitsi laajennuksesta. Sekä CUR että [ICO](/image/ico/) on määritetty Device-Independent Bitmap [DIB](/image/dib/) (Device-Independent Bitmap) -määrityksen perusteella. Oletusarvot sekä mukautetut kohdistimet, kuten Windows-hiiren osoitin Windows-käyttöjärjestelmälle, tallennetaan CUR-tiedostoihin. Se voi olla nuoli normaalikäyttöön, pyörivä tiimalasi havainnollistamaan odotusaikoja tai I-palkki tekstin muokkausta varten. CUR-tiedostot toimitetaan mukautetun työpöytäteeman asennuspaketin mukana varmistaakseen, että Windowsin kohdistin vastaa mukautettua työpöytäteemaa.

## Tekniset ominaisuudet ##

CUR-tiedostot ovat binäärisiä järjestelmätiedostoja, jotka löytyvät laitteista, jotka toimivat Microsoft Windows -käyttöjärjestelmässä. CUR-osoitinkuvia on eri vakiokokoisina, kuten 16×16, 32×32 jne. CUR-tiedostot ovat hyvin samanlaisia kuin ICO-tiedostot; molemmat koostuvat pienistä paikallaan olevista kuvista. Vain CUR- ja ICO-tiedostojen tunniste eroaa. Lisäksi hotspotin selitys CUR-tiedoston otsikossa eroaa ICO-tiedostosta. Hotspot tulkitsee pikselien siirtymän vasemmasta yläkulmasta kohtaan, johon osoitat hiirtä. Windows-järjestelmät käyttävät edelleen CUR-tiedostoja, mutta nyt animoiduilla kohdistimilla on yleensä tiedostotunniste ANI CUR:n sijaan.

## Lyhyt historia ##

CUR-tiedosto on tehty ICO-tiedostosta. Ensimmäinen CUR-tiedostomuoto sisällytettiin Microsoftin Windows 1.0 -käyttöjärjestelmään vuonna 1981 helpottamaan kaupallista käyttöä. Pian otettiin käyttöön enemmän interaktiivisia osoittimia, joiden avulla käyttäjät voivat muuttaa kohdistinasetuksiaan esiasennetuista vaihtoehdoista. CUR-tiedostoa on kuitenkin helppo muokata itse, vaikka sinulla olisi riittämätön tekninen tietämys.


## CUR-esimerkki ##

CUR-tiedostot löytyvät osoitteesta *C:\Windows\Cursors*:

{{< figure src="../cur.png" alt="CUR-tiedostomuoto" >}}

