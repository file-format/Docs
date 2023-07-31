{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - Wat is een MSIX-bestand?",
  "description":"Meer informatie over MSIX-bestanden en API's die MSIX-bestanden kunnen maken en openen.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Wat is een MSIX-bestand?

Een MSIX-bestand is een Windows-app-verpakkingsformaat dat wordt gebruikt voor het maken en distribueren van applicaties in Windows 10. Dit is het moderne pakketbestandsformaat in vergelijking met de [APPX](/nl/programming/appx/) en MSI die uiteindelijk zullen worden uitgefaseerd naar dit nieuwe bestandsformaat. Het kan worden gebruikt voor de implementatie van Win32-, WPF- en Windows Forms-apps. MSIX-bestanden zijn betrouwbaar en richten zich op optimalisatie van netwerk- en schijfruimte. Ontwikkelaars gebruiken deze om programma's te distribueren naar eindgebruikers via de Microsoft Store (voorheen bekend als Windows Store).

## MSIX-bestandsindeling - Meer informatie

MSIX-bestanden zijn [ZIP](/nl/compression/zip/)-gecomprimeerd, met alle bestanden in het verpakte bestand. Naast de app-gerelateerde bestanden bevat het MSIX-bestand [.xml](/nl/web/xml/) configuratiebestanden die informatie bevatten over de app-installatie.

## Wat zit er in een MSIX-pakket?

Een MSIX-pakket bestaat uit de volgende bestanden.

* `AppxBlockMap.xml` - Bekend als het pakketblokkaartbestand, het is een XML-document dat een lijst met app-bestanden bevat met indexen en cryptografische hashes voor elk gegevensblok dat in het pakket is opgeslagen.
* `AppxManifest.xml` - Een XML-document dat de informatie bevat die nodig is voor de implementatie, weergave en update van een MSIX-app. Deze informatie omvat pakketidentiteit, pakketafhankelijkheden, vereiste mogelijkheden, visuele elementen en uitbreidbaarheidspunten.
* `AppxSignature.p7x` - Een bestand dat wordt gegenereerd wanneer het pakket wordt ondertekend. Alle MSIX-pakketten moeten worden ondertekend voordat ze worden geïnstalleerd. Met de AppxBlockmap.xml kan het platform het pakket installeren en valideren.

## Referenties

* [MSIX-overzicht](https://learn.microsoft.com/en-us/windows/msix/overview)
* [Maak APPX-bestanden met Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

