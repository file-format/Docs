{
  "date" : "2021-08-11",
  "keywords" :[ "wim file", "wim file format", "wat is een wim file", "file", "wim example", "wim file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Meer informatie over WIM-bestandsindeling en API's die WIM-bestanden kunnen maken en openen.",
  "title" :"WIM - Windows Imaging Format-bestand",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Wat is een WIM-bestand?
De bestanden met de extensie .wim werden voor het eerst gezien in Windows Vista. De WIM behoort tot een op bestanden gebaseerd beeldformaat dat typisch werd geïntroduceerd in Microsoft Windows Vista. Hiermee kan een enkele schijfkopie worden geïmplementeerd op verschillende computerplatforms. WIM-bestanden worden gebruikt om bestanden zoals updates, stuurprogramma's en componenten te beheren zonder de image van het besturingssysteem opnieuw op te starten. AQ WIM-bestand bevat een set bestanden en bijbehorende metadata die erg lijkt op andere schijfbestandsindelingen.

## WIM-bestandsindelingen
Het WIM-bestandsformaat is niet zoals sectorgebaseerde formaten zoals VHD of IS, in feite is het een op bestanden gebaseerd wat betekent dat de fundamentele informatie-eenheid in een WIM een bestand is. Het basisvoordeel van bestandsgebaseerd is dat een enkelvoudige opslag van een bestand waarnaar meerdere keren wordt verwezen in de bestandssysteemstructuur en hardware-onafhankelijkheid. Het vermindert de overhead van het afzonderlijk openen en sluiten van verschillende bestanden, omdat de bestanden worden opgeslagen in een enkele WIM het dossier. WIM-bestanden kunnen meerdere schijfkopieën opslaan, waarnaar wordt verwezen door hun unieke naam of door hun numerieke index.
### Ondersteuning voor compressie-algoritmen
WIM ondersteunt de volgende families van compressie-algoritmen in aflopende snelheid en oplopende verhouding:
- XPRESS
-LZX
- LZMS
- Solide compressie.
De eerste drie families zijn gebaseerd op LZ77, terwijl Solid-compressie samen met LZMS werd geïntroduceerd in WIMGAPI Windows 8 en DISM Windows 8.1.
### Tools voor WIM-bestandsindeling
De volgende tools ondersteunen meestal het WIM-bestandsformaat:

- **ImageX**: een opdrachtregelprogramma dat wordt gebruikt voor het bewerken, maken en implementeren van Windows-schijfkopieën in de Windows Imaging Format. Samen met de relevante WIMGAPI wordt het gedistribueerd als onderdeel van de gratis Windows Automated Installation Kit. Vanaf Windows Vista gebruikt Windows Setup de WAIK API om Windows te installeren.
- **DISM**: een tool die is geïntroduceerd in Windows 7 en Windows Server 2008 R2 en die servicegerelateerde taken kan uitvoeren op een Windows-installatiekopie, of het nu een online-image is of een offline-image in een map of WIM-bestand. deze tool was in staat om afbeeldingen te koppelen en te ontkoppelen, een apparaatstuurprogramma toe te voegen aan een offline afbeelding en geïnstalleerde apparaatstuurprogramma's op te vragen in een offline afbeelding.
 




## Referenties


* [Windows Imaging Format - door Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


