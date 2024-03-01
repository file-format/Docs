{
  "date": "2019-10-11",
  "keywords": [
"asmx",
"asmx tiedosto",
"asmx tiedostomuoto",
"asmx tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on asmx-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASMX - ASP.NET-verkkopalvelutiedosto",
  "description": "Opi ASMX-tiedostosta ja API:ista, jotka voivat luoda ja avata ASMX-tiedostoja.",
  "linktitle": "ASMX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asm-fix"
}
},
  "lastmod": "2021-06-10"
}

## Mikä on ASMX-tiedosto?

.asmx-päätteinen tiedosto on ASP.NET-verkkopalvelutiedosto, joka tarjoaa tiedonsiirron kahden objektin välillä Internetin kautta käyttämällä SOAP (Simple Object Access Protocol) -protokollaa. Se otetaan käyttöön palveluna Windows-pohjaisessa Web-palvelimessa saapuvien pyyntöjen käsittelemiseksi ja vastauksen palauttamiseksi. Toisin kuin [ASPX](/web/aspx/)-tiedostot, jotka sisältävät koodin ASP.NET-verkkosivujen visuaalista näyttämistä varten, ASMX-tiedostot toimivat palvelimella taustalla ja suorittavat erilaisia tehtäviä, kuten yhteyden muodostamisen tietokantaan, tietojen hakemisen ja niiden palauttamisen muodossa, jossa pyyntö tehtiin. Näitä käytetään erityisesti XML-verkkopalveluihin.

## ASMX tiedostomuoto

ASMX-tiedostot ovat pelkkää tekstiä, ja niitä voidaan avata tai muokata sovelluksissa, kuten Microsoft Visual Studiossa tai tekstieditoreissa. Se on Microsoftin patentoima tiedostomuoto ja sillä on hyvin määritelty syntaksi verkkopalveluiden luomista varten. ASMX-tiedoston vastauksessa SOAP XML:n muodossa on seuraavat elementit.

 * Envelop - Juurielementti, joka tunnistaa XML-dokumentin SOAP-viestiksi.
 * Otsikko – valinnainen elementti, joka sisältää sovelluskohtaisia tietoja, kuten todennustietoja. Jos Header-elementti on läsnä, sen on oltava Envelope-elementin ensimmäinen lapsielementti.
 * Body - Sisältää vastaanottajalle tarkoitetun SOAP-viestin.
 * Fault - valinnainen elementti, jota käytetään osoittamaan virheilmoitukset. Jos Vika-elementti on olemassa, sen on oltava Body-elementin lapsielementti.

ASMX-tiedostoja voidaan kirjoittaa .NET-kielillä, kuten [C#](/programming/cs/), [Visual Basic](/programming/vb/) tai JScript.

## Miten ASMX eroaa ASPX:stä ja ASCX:stä?

ASMX-tiedostot eroavat ASPX- ja ASCX-tiedostoista.

 * ASPX, Active Server Pages, tiedostot ovat ohjelmointitiedostoja, jotka luodaan käyttämällä Microsoft ASP.NET -kehystä, joka toimii web-palvelimilla. Nämä hahmonnetaan asiakkaan verkkoselaimessa, kun käyttäjä pyytää pääsyä tällaiselle sivulle.
 * ASCX, Active Server User Control, määrittää käyttäjäohjaimet, joita käytetään uudelleenkäytettävien ohjausobjektien määrittämiseen ASP.NET-verkkosivuilla tai koko verkkosivustolla.

## Viitteet

 * [ASMX-palvelun käyttäminen](https://learn.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
 * [ASCX User Control](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

