{
  "date" : "2019-10-11",
  "keywords" : [ "vstm file", "vstm file format", "what is a vstm file", "file", "vstm example", "vstm file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSTM - Microsoft Visio -mallin tiedostomuoto",
  "description":"Opi VSTM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata VSTM-tiedostoja.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstm-fi",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Mikä on VSTM-tiedosto?

VSTM-laajennuksella varustetut tiedostot ovat Microsoft Visiolla luotuja mallitiedostoja, jotka tukevat makroja. Toisin kuin VSDX-tiedostot, VSTM-malleista luodut tiedostot voivat suorittaa makroja, jotka on kehitetty Visual Basic for Applications (VBA) -koodilla. Asiakirjan perusasetuksia varten voidaan luoda mallitiedosto, jota voidaan käyttää lisädokumenttien luomiseen näillä asetuksilla. Visio-tiedostoja käytetään piirustusten luomiseen, jotka sisältävät visuaalisia objekteja, vuokaavioita, UML-kaavioita, tietokulkuja, organisaatiokaavioita, ohjelmistokaavioita, verkkoasetteluja, tietokantamalleja, objektikartoitusta ja muuta vastaavaa tietoa. Visiolla luodut tiedostot voidaan myös viedä eri tiedostomuotoihin, kuten PNG, BMP, PDF ja muihin.

## Tiedosto muoto ##

VSTM-tiedostot perustuvat Open Packaging Conventions ja XML:ään, ja kehittäjät voivat hyötyä tästä muodosta oppimalla käsittelemään näitä tiedostoja ohjelmallisesti. Muoto perii monia samoja XML-rakenteita kuin sen osat Visio XML Drawing -tiedostomuodosta (.vdx). Yhteentoimivuus Visio-tiedostojen kanssa on lisääntynyt huomattavasti, koska kolmannen osapuolen ohjelmistot voivat käsitellä Visio-tiedostoja tiedostomuototasolla.

Jokaista Visio-tiedostoa kutsutaan paketiksi, joka sisältää muita tiedostoja tai osia. Paketin osa voi olla XML-tiedosto, kuva tai jopa VBA-ratkaisu. Paketin sisältämät osat voidaan jakaa asiakirja- ja suhde-osiin.

### Asiakirja ###

Asiakirjan osat sisältävät Visio-tiedoston todellisen sisällön ja metatiedot, kuten tiedoston nimen, ensimmäisen sivun ja kaikki sen sisältämät muodot sekä jopa muotojen tietoyhteydet. Paketissa olevat kuvat ja tekstitiedostot katsotaan asiakirjan osiksi.

### Suhteet ###

Visio-tiedoston suhdeosat tallennetaan _rels-kansioon, ja ne kuvaavat, kuinka paketin osat liittyvät kuhunkin. Se tarjoaa myös tiedoston rakenteen. Itsenäinen XML-dokumentti käyttää elementtien ylä- ja alasuhdetta määrittääkseen entiteettien suhteen toisiinsa. Kelvollinen Visio 2013 -tiedostomuoto sisältää oikean joukon osia ja paketti sisältää osien väliset suhteet.

Suhdeosat ovat XML-dokumentteja, jotka kuvaavat paketin eri asiakirjaosien välisiä suhteita. Ne määrittelevät yhteyden kahden kohteen välillä: määritetyn lähteen (määritetty suhdetiedoston nimen ja sijainnin mukaan) ja määritetyn kohdeasiakirjan osan. Suhdeosia käytetään esimerkiksi kuvaamaan, mitkä muotopohjat liittyvät tiedostoon, kuinka sivut liittyvät tiedostoon ja toisiinsa tai miten kuvat ja objektit liittyvät tiettyyn sivuun.

## Viitteet ##

* [Johdatus Visio-tiedostomuotoon](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


