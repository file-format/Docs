{
  "date" : "2019-10-11",
  "keywords" :[ "asmx","asmx-bestand", "asmx-bestandsformaat", "asmx-bestandstype", "bestand", "type", "wat is een asmx-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - ASP.NET-webservicebestand",
  "description" :"Meer informatie over wat een ASMX-bestand is en API's die ASMX-bestanden kunnen maken en openen.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Wat is een ASMX-bestand?

Een bestand met de extensie .asmx is een ASP.NET Web Service-bestand dat zorgt voor communicatie tussen twee objecten via internet met behulp van het Simple Object Access Protocol (SOAP). Het wordt ingezet als een service op de op Windows gebaseerde webserver om binnenkomende verzoeken te verwerken en het antwoord terug te sturen. In tegenstelling tot [ASPX](/nl/web/aspx/)-bestanden die de code bevatten voor visuele weergave van ASP.NET-webpagina's, draaien ASMX-bestanden op de server op de achtergrond en voeren ze verschillende taken uit, zoals verbinding maken met de database, gegevens ophalen en terugsturen in een formaat waarin het verzoek is gedaan. Deze worden specifiek gebruikt voor XML-webservices.

## ASMX-bestandsindeling

ASMX-bestanden zijn in platte tekstindeling en kunnen worden geopend of bewerkt in toepassingen zoals Microsoft Visual Studio of teksteditors. Het is een eigen bestandsindeling van Microsoft en heeft een goed gedefinieerde syntaxis voor het maken van webservices. Een reactie door een ASMX-bestand in de vorm van SOAP XML heeft de volgende elementen.

* `Envelop` - Een root-element dat het XML-document identificeert als een SOAP-bericht.
* `Header` - Een optioneel element dat toepassingsspecifieke informatie bevat, zoals authenticatiegegevens. Als het Header-element aanwezig is, moet dit het eerste onderliggende element van het Envelope-element zijn.
* `Body` - Bevat het SOAP-bericht bedoeld voor de ontvanger.
* `Fault` - Een optioneel element dat wordt gebruikt om foutmeldingen aan te geven. Als het Fault-element aanwezig is, moet het een onderliggend element van het Body-element zijn.

ASMX-bestanden kunnen worden geschreven in .NET-talen zoals [C#](/nl/programming/cs/), [Visual Basic](/nl/programming/vb/) of JScript.

## Waarin verschilt ASMX van ASPX en ASCX?

ASMX-bestanden zijn anders dan ASPX- en ASCX-bestanden.

* ASPX-, Active Server Pages-bestanden zijn programmeerbestanden die worden gegenereerd met behulp van het Microsoft ASP.NET-framework dat op webservers wordt uitgevoerd. Deze worden weergegeven in de webbrowser van de klant wanneer de gebruiker vraagt om toegang tot een dergelijke pagina.
* ASCX, Active Server User Control, definieert gebruikersbesturingselementen die worden gebruikt om herbruikbare besturingselementen in ASP.NET-webpagina's of de hele website te definiëren.

## Referenties

* [ASMX-service verbruiken](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [ASCX-gebruikersbediening](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

