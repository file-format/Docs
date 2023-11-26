{
  "date" : "2023-01-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDISCO-bestand - DISCO dynamisch detectiedocumentbestandsformaat",
  "description":"Meer informatie over wat een VDISCO-bestand is?",
  "linktitle" : "VDISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-01-29"
}

## Wat is een VDISCO-bestand?

Een VDISCO-bestand is een detectiebestand dat door Microsoft Visual Studio wordt gebruikt in zijn webservices. Het biedt informatie over de beschikbare webservices, zoals hun URL's, naamruimten en methoden. Het VDISCO-bestand is vergelijkbaar met het bestandsformaat [DISCO](/nl/web/disco/), maar wordt tijdens runtime gegenereerd. Het wordt opgeslagen in de webservicetoepassing en wordt door Visual Studio gebruikt om webservices dynamisch in een project te ontdekken en te gebruiken. VDISCO-bestanden worden gebruikt in combinatie met het [.asmx](/nl/web/asmx/) bestand dat de daadwerkelijke webservicecode bevat.

U kunt het VDISCO-bestand openen in elke teksteditor zoals Microsoft Notepad, Github Atom en Apple TextEdit. Het kan ook worden geopend met Microsoft Visual Studio 2012 en later om ermee te werken.

## VDISCO-bestandsindeling

Een VDISCO-bestand wordt opgeslagen en gehost in de bestandsindeling [XML](/nl/web/xml/), een universeel formaat voor het samenstellen en publiceren van gegevens. Het bevat de service-URL, naamruimten en methoden in standaard XML-tags, waarbij elke tag de respectieve waarde van zijn informatie bevat.

## Referenties

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Ontdekking van webservices](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [C#-voorbeeld van DiscoveryClient-klasse](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

