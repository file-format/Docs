{
  "date": "2021-08-24",
  "keywords": [
"vbs",
"tiedosto",
"laajennus",
"tiedosto muoto",
"Visual Basic Script",
"Ohjelmointiopas",
"vbs esimerkki",
"Microsoft Visual Basic",
"VBScript"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "VBS - Visual Basic -skriptitiedosto",
  "description": "Opi VBS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata VBS-tiedostoja.",
  "linktitle": "VBS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vb-fis"
}
},
  "lastmod": "2021-08-24"
}

## Mikä on VBS-tiedosto?

VBS tai VBScript on yhdistetty Microsoft Visual Basicin komentosarjaversioon. Tietokoneympäristössä käyttäjällä on oikeus käyttää ja hallita monia sen ominaisuuksia. VBScript saa käyttää mallia nimeltä **Component Object Model** käyttääkseen ympäristön elementtejä ja työkaluja. Tämä ympäristö on määritetty VBScriptin käyttöä ja käyttöä varten.

Se toimii kuten Javascript, kun asiakas käyttää sitä Web-kehityksen alalla. Palvelimet käyttävät sitä myös web-sivujen käsittelyyn. Se voidaan ottaa huomioon joissakin muun tyyppisissä komentosarjatiedostoissa, kuten [HTML](/web/html/)-sovelluksissa.


## Lyhyt historia ##

Se lanseerattiin ensimmäisen kerran vuonna 1996 osana Microsoftin käyttämiä Windows-komentosarjoille määrittelemiä tekniikoita. Se kehitettiin alun perin erityisesti verkkokehittäjien avuksi. Samana vuonna julkaistiin Microsoft Windowsin Explorer Internet Explorer yhdessä Visual Basic Scriptin ominaisuuksien kanssa.

Tekniikan ja verkkokehityksen kehittyessä lanseerattiin useita VBScript-versioita sekä monia edistyneitä ominaisuuksia. Lisäksi tulevana vuonna tämä komentosarjakieli tulee olemaan osa Microsoft Windowsia uusilla ominaisuuksilla.

## Tekniset tiedot ##

Palvelinpuolen verkkosivuilla käytetään VBScriptin lisäksi työkaluja, kuten **Active Server Pages**. Tätä komentosarjakieltä voidaan käyttää myös Windowsin komentosarjakomponentissa. Tämän kielen tiedostot on tallennettu .vbs-tunnisteella Windowsissa.

Tämän kielen koodissa käytetään monia ohjausrakenteita, kuten silmukoita. Se sisältää myös argumentteja, jotka ovat komentoriviä ja voivat olla nimettyjä tai nimeämättömiä. Tämän kielen tiedostot voidaan tallentaa yksinkertaisesti Windows-käyttöjärjestelmän kansioihin tai työpöydälle. Vaikka VBScript-ohjelmille, kuten Microsoft Script Editor, ei ole erityistä integroitua kehitysympäristöä, tarjoavat mahdollisuuden tämän kielen kehittämiseen.

When VBScript is hosted by the Script host of Windows, it provides various features that are quite common to the languages of scripting but are not available in Visual Basic 6.0. Ominaisuuksiin, joihin liittyy helppo tai suora pääsy, kuuluvat verkkotulostimet, nimettömät ja nimetyt komentoriviargumentit, stdout ja stdin, verkkoosuudet, Windows Management Instrumentation, verkkojen käyttäjätiedot, kuten ryhmäjäsenyys, ja paljon muuta. 

## VBS-tiedostomuodon esimerkki ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## Viite ##

* [VBS - Wikipedia](https://en.wikipedia.org/wiki/VBScript)




