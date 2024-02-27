{
  "date": "2023-01-29",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VDISCO-fil - DISCO Dynamic Discovery-dokumentfilformat",
  "description": "Lær om, hvad en VDISCO fil er?",
  "linktitle": "VDISCO",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-vdisc-dao"
}
},
  "lastmod": "2023-01-29"
}

## Hvad er en VDISCO fil?

En VDISCO-fil er en opdagelsesfil, der bruges af Microsoft Visual Studio i dets webtjenester. Det giver oplysninger om de tilgængelige webtjenester, såsom deres URL'er, navnerum og metoder. VDISCO-filen ligner filformatet [DISCO](/web/disco/), men genereres under kørsel. Den er gemt i webtjenesteapplikationen og bruges af Visual Studio til dynamisk at opdage og bruge webtjenester i et projekt. VDISCO-filer bruges i kombination med [.asmx](/web/asmx/)-filen, der indeholder den faktiske webtjenestekode.

Du kan åbne VDISCO-filen i enhver teksteditor, såsom Microsoft Notepad, Github Atom og Apple TextEdit. Det kan også åbnes med Microsoft Visual Studio 2012 og senere for at arbejde med det.

## VDISCO filformat

En VDISCO-fil gemmes og hostes i filformatet [XML](/web/xml/), som er et universelt format til sammensætning og publicering af data. Det indeholder tjenestens URL, navneområder og metoder i standard XML-tags, hvor hvert tag indeholder respektive værdi af dens information.

## Referencer

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)

* [Web Services Discovery](https://en.wikipedia.org/wiki/Web_Services_Discovery)

* [C# Example of DiscoveryClient Class](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

