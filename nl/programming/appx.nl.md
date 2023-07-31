{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - Wat is een APPX-bestand?",
  "description":"Meer informatie over APPX-bestandsindelingen en API's die APPX-bestanden kunnen maken en openen.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Wat is een APPX-bestand?

Een APPX-bestand is een distribueerbaar pakketbestandsformaat dat wordt gebruikt voor distributie en installatie van een applicatie. Het werd geïntroduceerd met Windows 8 om te worden gepubliceerd in de Microsoft Windows Store. Het bevat alle bestanden die nodig zijn om een Windows-toepassing te installeren. Deze omvatten metagegevens, bestanden en inloggegevens. Een moderner verpakkingsbestandsformaat is MSIX dat momenteel vaker wordt gebruikt in vergelijking met APPX.

## APPX-bestandsindeling - Meer informatie

APPX-bestanden worden opgeslagen als gecomprimeerde bestanden in de bestandsindeling [ZIP](/nl/compression/zip/). Dit maakt het hele pakket als een archiefbestand met verkleinde bestandsgrootte dat gemakkelijk kan worden geüpload naar de Microsoft Store.

## Hoe bestanden in een APPX-bestand te bekijken?

Om de inhoud of bestanden in een APPX-bestand te bekijken, moeten de volgende stappen worden gevolgd.

1. Aangezien APPX-bestanden worden opgeslagen als gecomprimeerde ZIP-bestanden, hernoemt u het bestand naar de extensie .zip
1. Gebruik een decompressietool zoals 7-Zip, WinZip of WinRAR om de bestanden in het APPX-bestand uit te pakken

## Hoe maak je een APPX-bestand aan?

Er zijn twee methoden die kunnen worden gebruikt om APPX-bestanden te maken.

1. MakeApp.exe gebruiken - [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) wordt gebruikt om beide te maken app-pakketten (.msix of .appx) en app-pakketbundelbestanden .msixbundle of .appxbundle). Bovendien kan het bestanden uit een app-pakket extraheren. MakeApp.exe is beschikbaar met Windows 10 SDK en kan worden gebruikt vanaf de opdrachtprompt.
1. Microsoft Visual Studio gebruiken - Ontwikkelaars [maken gewoonlijk APPX-bestanden](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) met Microsoft Visual Studio. Zodra de applicatie-ontwikkeling is voltooid en de app klaar is om te worden gepubliceerd, kan het APPX-pakketbestand worden gemaakt door het vanuit Visual Studio te publiceren.

## Referenties

* [Maak een MSIX-pakket of bundel met MakeAppx.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Maak APPX-bestanden met Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

