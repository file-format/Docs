{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MKS-bestandsindeling",
  "keywords" :[ "mks", "matroska video", "mkv-formaat", "bestand", "formaat", "video"],
  "description":"Meer informatie over MKS-bestandsindelingen voor ondertitels die alleen door Matroska zijn gemaakt en API's die MKS-bestanden kunnen maken en openen.",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## Wat is een MKS-bestand?

De MKS-bestanden zijn algemeen bekend als Matroska-bestanden die alleen ondertitels bevatten. Hoewel de Matroska een algemene bestandscontainer is, wordt voorkomen dat de informatie van specifieke formaten wordt bewaard. Aangezien ondertitels worden gebruikt in sommige audio- of videocontainers, besteedt Matroska aandacht aan het opslaan van enkele veelgebruikte ondertitelformaten. Het helpt Matroska om consistent te zijn met de groeisnelheid. U moet de onderstaande punten volgen om de ondertitels in Matroska op te slaan:

- De ".mks". de extensie wordt gebruikt door het Matroska-bestand (dat alleen ondertitels bevat).
- **CodecPrivate** wordt gebruikt om alle codec-gerelateerde informatie op te slaan die globaal is voor een hele stream.
- Verwijder de start- en stop-tijdstempels die worden gebruikt in een tijdstempel-native opslagformaat. Gebruik in plaats daarvan de Blokken tijdstempel en Duur.
- Je kunt alles gebruiken met een transparante laag, inclusief een video.

## Algemene ondertitelformaten

Hier zijn enkele korte opmerkingen over meer algemene ondertitelformaten die zijn opgeslagen in Matroska:

### Afbeeldingen Ondertitels
Het ondertitelformaat VobSub is het eerste ondertitelingsformaat voor afbeeldingen dat in Matroska wordt geïmporteerd. Dit formaat wordt gegenereerd door de ondertitels van een dvd te exporteren. De tracks moeten worden gescheiden tijdens het opslaan in Matroska als de VobSub uit een set van meerdere streams bestaat.

### SRT-ondertitels
De SRT is de meest eenvoudige en meest basale van alle ondertitelformaten. Het bestaat uit vier delen, zoals hieronder weergegeven:
 



1. Een getal dat de volgorde van de ondertitel aangeeft.
2. De verschijnende en verdwijnende tijd van de ondertitel op het scherm.
3. De ondertitel zelf.
4. Een lege regel om het begin van de volgende ondertitel aan te geven.
 



### SSA/ASS-ondertitels
Sub Station Alpha (SSA) is een bestandsindeling die wordt gebruikt door de populaire ondertiteleditor SubStation Alpha. De SSA-ondertitels worden veel gebruikt door fansubbers. Het heeft de mogelijkheid om moderne functies weer te geven, zoals karaoke, positionering, styling, enz.
 



### WebVTT-ondertitels
Het World Wide Web Consortium (W3C) heeft de WebVTT ontwikkeld, die wordt afgekort als "Web Video Text Tracks Format". Dit formaat wordt gebruikt om externe teksttrackbronnen te markeren in verband met het HTML-element.

### HDMV presentatie graphics ondertitels
Het HDMV presentatie graphics ondertitelformaat (HDMV PGS) is een serie bitmaps en we kunnen het helemaal niet zeggen als tekst. Met andere woorden, je kunt zeggen dat het slechts een getimede reeks grafische afbeeldingen is. Om de informatie te extraheren, is het converteren van PGS naar SRT een noodzakelijk proces.

### HDMV tekst ondertitels
De HDMV-tekst staat bekend als het tekstuele ondertitelingsformaat dat op Blu-rays wordt gebruikt. Matroska staat alleen UTF-8-tekenset toe wanneer de TextST-ondertitels worden opgeslagen.

### Digital Video Broadcasting (DVB) ondertitels
Het DVB-ondertitelingsformaat werd geïntroduceerd voor het reguleren van de transmissie en weergave van verschillende ondertitelingstalen op tv-signalen. Een typisch ondertitelingsformaat zou elke kijker ook in staat stellen om DVB-ondertitelde uitzendingen te bekijken, ongeacht de fabrikant van de transmissiesystemen.


## Referenties ##

- [Matroska-ondertitels](https://www.matroska.org/technical/subtitles.html)

