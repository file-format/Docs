{
  "date": "2019-10-11",
  "keywords": [
".mel",
"Maya upotettu kieli",
"tiedosto",
"laajennus",
"tiedosto muoto",
"Maya 3D",
"Ohjelmointiopas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MEL - Maya Embedded Language -tiedostomuoto",
  "description": "Opi MEL-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MEL-tiedostoja.",
  "linktitle": "MEL",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-me-fil"
}
},
  "lastmod": "2021-03-08"
}

## Mikä on MEL-tiedosto?

Tiedosto, jonka laajennus on .mel (Maya Embedded Language), on komentosarjakieli, jota Autodesk Maya käyttää graafisten käyttöliittymien luomiseen. Sen avulla voit automatisoida graafisten elementtien luomisen käyttämällä suoritettavia komentosarjoja Mayan graafisen käyttöliittymän lisäksi. MEL antaa sinulle mahdollisuuden luoda graafisia käyttöliittymiä ilman ohjelmoinnin oppimista. Tämä saavutetaan luomalla makroja ja mukautettuja toimintoja, jotka nopeuttavat toistuvia tehtäviä. Näiden toimintojen ja komentosarjojen avulla voit luoda mukautettuja mallinnuksia, animaatioita, dynamiikkaa ja tehtävien hahmontamista. Autodesk Maya 2020:lla voidaan avata ja tarkastella EML-tiedoston sisältöä.

## MEL-tiedostomuoto - lisätietoja

Ohjelmoijan [reference manual](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) on kehittäjien saatavilla Mayan dokumentaatioosiossa. MEL perustuu UINX:n kaltaisiin komentotulkkikomentoihin asioiden saavuttamiseksi. Komentosarjaan perustuvat komennot tekevät siitä epäolennaisen tavanomaisen ja olioohjelmoinnin (OOP) kannalta, jolloin tietorakenteita, funktioiden kutsumista tai OOP:n käyttöä ei käytetä kuten muissa kielissä.

Seuraavassa on joitakin keskeisiä kohtia MEL:stä.

Kommentit - Jokaisen MEL:n lauseen on päätyttävä puolipisteeseen (;), myös lohkon lopussa.

Palauttavat arvot - Arvon palauttavan lausekkeen ilmoittaminen ei tulosta automaattisesti arvoa MEL:ssä. Sen sijaan se aiheuttaa virheen.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Komennot luomiseen, muokkaamiseen ja poistamiseen` - Samaa komentoa käytetään asioiden luomiseen, muokkaamiseen tai olemassa olevien asioiden tiedusteluihin. Lippu kuitenkin ohjaa, mitä (luo, muokkaa tai kysy) komento tekee.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
Palauta arvo funktiosta - Funktion syntaksi palauttaa automaattisesti arvon. Jos haluat saada palautusarvon komennon syntaksilla, sinun on lisättävä komento takalainausmerkkeihin.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Viitteet

 * [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

