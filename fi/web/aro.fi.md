{
  "date": "2021-12-09",
  "keywords": [
"aro",
".aro-tiedosto",
"aro tiedostomuoto",
"tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on .aro-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ARO-tiedostomuoto - SteelArrow-verkkosovellustiedosto",
  "description": "Opi mikä on ARO-tiedosto ja API:t, jotka voivat luoda ja avata ARO-tiedostoja.",
  "linktitle": "ARO",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ar-fio"
}
},
  "lastmod": "2021-12-09"
}

## Mikä on ARO-tiedosto?

ARO-tiedosto on palvelinpuolen web-sivutiedosto, joka luodaan SteelArrow Web Application -sovelluksella. Se sisältää [HTML](/web/html/)- ja SteelArrow-tageja ja komentosarjoja. Nämä suoritetaan palvelimella täydellisen vastaussivun luomiseksi ennen niiden lähettämistä käyttäjän selaimeen. ARO-tiedostot sisältävät lähes 95 % HTML-sisällöstä, kun taas loput ovat SteelArrow-koodia. Jotta ARO-tiedostot toimisivat sinulle, SteelArrow Web Applications -palvelimen tulee olla asennettuna ja käynnissä web-palvelinkoneessa.

## ARO tiedostomuoto

ARO files are written in HTML markup language file with embedded JavaScript code and Java applets. [SteelArrow tags](http://www.steelarrow.com/docs/basics1.aro) are the basic building blocks for development of web pages. Though these don't change the display of the page, they are used to fill the page with data. In addition, they may also be used to control the output with conditional statements.

### Esimerkki ARO-tunnisteesta

The<SAOUTPUT> ARO-tunnisteen avulla kehittäjät voivat tulostaa data-arvoja missä tahansa skriptin kohdassa. Sillä voidaan esimerkiksi saada PARAM-taulukon tulos<SAOUTPUT VALUE=PARAM[]> jotka voidaan näyttää HTML:ssä<BODY> tag.

## Viitteet

* [SteelArrow tags](http://www.steelarrow.com/docs/basics.aro)

