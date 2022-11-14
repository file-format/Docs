{
  "date" : "2022-03-21",
  "keywords" :[ "xpr-bestand", "xpr-bestandsindeling", "wat is een xpr-bestand", "bestand", "xpr-voorbeeld", "xpr-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPR-bestandsindeling - Microsoft Expression Design grafisch bestand",
  "description":"Meer informatie over XPR-bestandsindeling en API's die XPR-bestanden kunnen maken en openen.",
  "linktitle" : "XPR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-21"
}

## Wat is een XPR-bestand?

Een XPR-bestand is een vectorafbeeldingsbestand dat is gemaakt met de inmiddels stopgezette Microsoft Expression Graphics (EGD)-software. Het bevat grafische informatie die kan worden gebruikt als mockup voor de gebruikersinterface. XPR-bestanden werden later vervangen door .design-bestanden in Microsoft Expression Design. XPR-bestanden kunnen worden geopend met Microsoft Expression Studio, dat al geruime tijd niet meer leverbaar is.

## Kwetsbaarheid in XPR-bestandsindeling

XPR-bestanden werden geïdentificeerd om te profiteren van een kwetsbaarheid in Microsoft Expression Design, waardoor uitvoering van externe code mogelijk werd. In het gerapporteerde probleem, als een gebruiker een legitiem .xpr-bestand opende dat in de netwerkmap samen met het DLL-bestand (Dynamic Link Library) is opgenomen, zou Microsoft Expression Design kunnen proberen het DLL-bestand te laden en de code die het bevatte uit te voeren. Dit werd later door Microsoft opgelost in een beveiligingsupdate.

## Referenties

* [Kwetsbaarheid in expressieontwerp kan leiden tot uitvoering van externe code (2651018)](https://docs.microsoft.com/en-us/security-updates/securitybulletins/2012/ms12-022)

