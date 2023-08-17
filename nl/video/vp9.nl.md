{
  "date" : "2021-03-12",
  "keywords" :[ "VP9", "Bestand", "Extensie", "Bestandsindeling", "Videoindeling", "TrueMotion Video", "VPX", "On2 Technologies"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 - TrueMotion-videobestand",
  "description":"Meer informatie over VP9-bestandsindeling en API's die VP9-bestanden kunnen maken en openen.",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## Wat is een VP9-bestand?

Google heeft de VP9-codec ontwikkeld als een royaltyvrije, open-source videocoderingsstandaard als opvolger van VP8. Het was oorspronkelijk ontworpen om de ultra HD-inhoud op YouTube te comprimeren, omdat het de coderingsefficiëntie van zijn voorganger uitbreidt en verbetert. Als we het hebben over de originele VPX-codecs, ze kwamen van On2 Technologies, dat in 2010 door Google werd geassimileerd. Google heeft de codec later open source gemaakt. Beide formaten VP8 en VP9 zijn beschikbaar onder een gratis BSD-licentie die operators in staat stelt om vaardigheid in coderen of decoderen in zowel exclusieve software als open-source software te organiseren zonder hun broncode te onthullen.

## Technische kenmerken van VP9

* VP9 biedt een maximale resolutie van 8192x4352 bij maximaal 120 fps en meerdere kleurruimten, met Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 en sRGB
* Het volledige scala aan web- en mobiele toepassingen, van compressie met lage bitrate tot ultra-HD van hoge kwaliteit, met extra ondersteuning voor 10/12-bits codering en HDR, wordt volledig ondersteund door dit formaat
* Het kan de videobitsnelheden met maar liefst 50% verlagen in vergelijking met andere
* Het is voorbereid op adaptieve streaming en wordt gebruikt door YouTube en andere bekende webvideoproviders
* Chrome-, Opera-, Edge-, Firefox- en Android-apparaten, evenals miljoenen smart-tv's, ondersteunen de decodering van deze codec
* De videoresoluties groter dan 1080p worden gewijzigd via VP9 en maken verliesvrije compressie mogelijk
* Verschillende kleurruimten zoals Rec. 601, rec. 709, rec. 2020, SMPTE-170, SMPTE-240 en sRGB worden ondersteund door VP9
* HDR-video met Hybrid Log-Gamma en Perceptual Quantizer kan ook worden ondersteund door VP9


## Korte geschiedenis

* De ontwikkeling van de VP9-videocodec is in 2011 begonnen en de decoder is in december 2012 aan de Chromium-webbrowser toegevoegd
* De eerste versie van de Google Chrome-webbrowser werd uitgebracht in februari 2013 en werd destijds gedecodeerd
* Google heeft in augustus 2013 Chrome 29.0.1547 uitgebracht met definitieve ondersteuning voor VP9
* In oktober 2013 werd een instinctieve VP9-decoder toegevoegd aan FFmpeg
* Mozilla heeft in december 2013 VP9-ondersteuning aan Firefox toegevoegd in versie 2 die toen op 18 maart 2014 werd uitgebracht
 

## Werking van VP9

Gewoonlijk verhoogt de 4K-video de beeldkwaliteit door specifieke pixels kleiner te maken, de VP9-codec en HEVC maken ze groter om de bitrate en bestandsgrootte terug te schalen. Hoewel dit tegenstrijdig lijkt, neemt de coderingsengine de grotere pixels en verandert deze in een hogere resolutieproductiviteit. Bronvideo, bestaande uit videoframes, wordt gecodeerd of gecomprimeerd om een gecomprimeerde videobitstream te maken. Elk afzonderlijk frame wordt eerst verdeeld in blokken pixels. De blokken worden vervolgens onderzocht op driedimensionale ontslagen en opeenvolgende verbindingen tussen frames worden geëvalueerd om te profiteren van gebieden die niet kunnen worden gewijzigd. Deze worden gecodeerd via bewegingsvectoren die de kwaliteiten van het gegeven blok op het volgende frame waarborgen. De resterende informatie wordt gecodeerd met behulp van een effectieve binaire compressie.

## Referenties

* [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9)
* [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
* [Kokosnoot](https://www.coconut.co/)

