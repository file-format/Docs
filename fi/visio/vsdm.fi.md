{
  "date" : "2019-10-11",
  "keywords" : [ "vsdm file", "vsdm file format", "what is a vsdm file", "file", "vsdm example", "vsdm file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSDM - Microsoft Visio -piirustustiedostomuoto",
  "description":"Opi VSDM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata VSDM-tiedostoja.",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsdm-fi",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Mikä on VSDM-tiedosto?

Tiedostot, joiden laajennus on .vsdm, ovat piirustustiedostoja, jotka on luotu makroja tukevalla Microsoft Visio -sovelluksella. VSDM-tiedostot ovat OPC/XML-piirustuksia, jotka ovat samanlaisia kuin VSDX, mutta tarjoavat myös mahdollisuuden suorittaa makroja, kun tiedosto avataan. Makrot ovat käyttäjän määrittämiä toimintoja/vaiheita, jotka on kehitetty Visual Basic for Applicationsissa (VBA) ja joita voidaan käyttää toistuvien tehtävien suorittamiseen. VSDM-tiedostomuoto otettiin käyttöön Microsoft Visio 2013:n lanseerauksen yhteydessä. Visio-tiedostoja käytetään piirustusten luomiseen, jotka sisältävät visuaalisia objekteja, vuokaavioita, UML-kaavioita, tietokulkuja, organisaatiokaavioita, ohjelmistokaavioita, verkkoasettelua, tietokantamalleja, objektien kartoituksia ja muita vastaavia tietoja. Visiolla luodut tiedostot voidaan myös viedä eri tiedostomuotoihin, kuten [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) ja muihin.

## VSDM-tiedostomuoto

VSDM-tiedostot perustuvat Open Packaging Conventions ja XML:ään, ja kehittäjät voivat hyötyä tästä muodosta oppimalla käsittelemään näitä tiedostoja ohjelmallisesti. Muoto perii monia samoja XML-rakenteita kuin sen osat Visio XML Drawing -tiedostomuodosta (.vdx). Yhteentoimivuus Visio-tiedostojen kanssa on lisääntynyt huomattavasti, koska kolmannen osapuolen ohjelmistot voivat käsitellä Visio-tiedostoja tiedostomuototasolla.

Jokaista Visio-tiedostoa kutsutaan paketiksi, joka sisältää muita tiedostoja tai osia. Paketin osa voi olla XML-tiedosto, kuva tai jopa VBA-ratkaisu. Paketin sisältämät osat voidaan jakaa asiakirja- ja suhde-osiin.

### Asiakirja ###

Asiakirjan osat sisältävät Visio-tiedoston todellisen sisällön ja metatiedot, kuten tiedoston nimen, ensimmäisen sivun ja kaikki sen sisältämät muodot sekä jopa muotojen tietoyhteydet. Paketissa olevat kuvat ja tekstitiedostot katsotaan asiakirjan osiksi.

### Suhteet ###

Visio-tiedoston suhdeosat tallennetaan \_rels-kansioon, ja ne kuvaavat, kuinka paketin osat liittyvät kuhunkin. Se tarjoaa myös tiedoston rakenteen. Itsenäinen XML-dokumentti käyttää elementtien ylä- ja alasuhdetta määrittääkseen entiteettien suhteen toisiinsa. Kelvollinen Visio 2013 -tiedostomuoto sisältää oikean joukon osia ja paketti sisältää osien väliset suhteet.

Suhdeosat ovat XML-dokumentteja, jotka kuvaavat paketin eri asiakirjaosien välisiä suhteita. Ne määrittelevät yhteyden kahden kohteen välillä: määritetyn lähteen (määritetty suhdetiedoston nimen ja sijainnin mukaan) ja määritetyn kohdeasiakirjan osan. Suhdeosia käytetään esimerkiksi kuvaamaan, mitkä muotopohjat liittyvät tiedostoon, kuinka sivut liittyvät tiedostoon ja toisiinsa tai miten kuvat ja objektit liittyvät tiettyyn sivuun.

## Viitteet ##

* [Johdatus Visio-tiedostomuotoon](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


