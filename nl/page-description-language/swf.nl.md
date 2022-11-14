{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "keywords" :[ "SWF", "bestand", "extensie", "formaat", "videoformaat", "Wat is een SWF-bestand", "swf-bestandsformaat", "swf-bestandsspeler", "hoe een swf-bestand te openen"] ,
  "title" :"SWF-bestand - Shockwave Flash-filmbestandsindeling",
  "description":"Meer informatie over wat een SWF-bestand is en API's die kunnen maken en laten zien hoe u het SWF-bestand opent.",
  "linktitle" : "SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een SWF-bestand?

Een SWF-bestand is een animatiebestand dat is gemaakt met Adobe Flash. Het kan verschillende soorten elementen bevatten, zoals tekst, vectorafbeeldingen, rasterafbeeldingen, actionscripts, objecten zoals cirkels, lijnen, vierkanten en rechthoeken om de animatie te maken. SWF-bestanden rangschikken deze multimedia-items in frames die kunnen worden afgespeeld op verschillende frames per seconde (fps). SWF betekent Short Web File maar staat ook bekend als Shockwave Format.

Toepassingen die *SWF-bestanden konden openen** waren onder meer Adobe Flash Player (nu niet meer leverbaar) en Eltima Elmedia Player.

## SWF-bestandsindeling - Meer informatie

SWF-bestanden werden vroeger als binaire bestanden op schijf opgeslagen. Het SWF-bestandsformaat werd gebruikt om animaties en games te ontwikkelen die in websites konden worden ingesloten en ook onafhankelijk konden worden gespeeld. Het ondersteunde ook video's en geluiden die ontwikkelaars veel keuzes gaven om interactieve multimediatoepassingen te maken. SWF-bestanden kunnen worden afgespeeld in webbrowsers waarop Adobe Shockwave is geïnstalleerd. Adobe Flash is in december 2020 stopgezet vanwege tekortkomingen en beveiligingsproblemen.

## Korte geschiedenis van SWF-bestandsindeling

Het SWF-bestandsformaat is oorspronkelijk ontworpen door FutureWave Software om animaties weer te geven met de bedoeling om op een spelersoftware te draaien op elk systeem met langzamere netwerkverbindingen, terwijl de bestandsgrootte klein blijft. In december 1996 bezat Macromedia FutureWave en werd het omgezet naar Macromedia Flash 1.0.

In 2005 werd Macromedia overgenomen door Adobe, die de SWF in 2008 aankondigde als onderdeel van zijn open source-project. In datzelfde jaar bracht Adobe code uit aan 's werelds populaire web-engines om hen in staat te stellen SWF-bestanden te crawlen en te indexeren. Aangezien SWF-bestanden echter een standaardindeling lijken te worden voor het publiceren van Flash-inhoud op internet, is de SWF gewijzigd in Small Web Format.

## SWF-bestandsstructuur

Pad is het grafische basiselement in SWF, een reeks segmenten van basiselementen, variërend van eenvoudige lijnen tot Bezier-curven. Deze eenvoudige elementen helpen ook om andere extra primitieven te maken, zoals kubussen, ellipsen en zelfs teksten. De grafische primitieven in SWF hebben gelijkenis met de grafische elementen van andere formaten zoals SVG en MPEG-4 BIFS.

Lijsten weergeven en het hergebruiken/hernoemen van reeds gedefinieerde elementen zijn ook toegestaan door het formaat. Het binaire streamformaat van SWF kan worden vergeleken met QuickTime-atomen, wat qua tag, grootte en payload vergelijkbaar is. Met het binaire streamformaat kunnen oudere spelers niet-ondersteunde inhoud overslaan. Hoewel originele versies van SWF beperkt waren tot het aanbieden van vectorafbeeldingen en afbeeldingen, maken nieuwe versies daarom ook audio- en video-inhoud mogelijk.

Een nieuwe, low-level 3D API van de Flash Player genaamd "Stage3D" werd geïntroduceerd in versie 11. Deze API was bedoeld als tegenhanger van OpenGL of Direct3D. Stage3D definieert kleuren in een taal op laag niveau, Adobe Graphics Assembly Language (AGAL) genaamd. Hieronder volgen enkele basisgegevenstypen van het SWF-bestandsformaat.

### Coördinaten

XY-coördinaten in SWF-bestandsindeling worden opgeslagen als gehele getallen en gemeten in een eenheid die een twip wordt genoemd. Een twip bestaat uit 1/20e van een logische pixel. De logische pixel en de schermpixel zijn hetzelfde wanneer het bestand wordt afgespeeld zonder schaling op 100%.

### Gehele typen en bytevolgorde

De ondertekende en niet-ondertekende integer-typen van 8, 16, 32 en 64 bits zijn toegestaan in SWF-bestandsindeling. De bytevolgorde van Little-endian wordt gebruikt om gehele waarden op te slaan. Hoewel binnen bytes, wordt de bitvolgorde opgeslagen in big-endian. Alle integer-waarden moeten byte-uitgelijnd zijn. Getekende gehele getallen worden weergegeven door gebruik te maken van traditionele 2-complement bitpatronen.

### Vaste-kommagetallen

Twee soorten vaste-kommagetallen worden ondersteund door het SWF-bestandsformaat, namelijk 32 en 16 bit.

### Drijvende-kommagetallen

SWF 8 en latere versies gebruiken drie typen getallen met drijvende komma (FLOAT, FLOAT 16, DOUBLE) die compatibel zijn met de IEEE-standaard 754 van typen met drijvende komma.

### Gecodeerde gehele getallen

Eén type gecodeerd geheel getal wordt ondersteund door SWF 9 en hoger met een variabel aantal bytes.

## Referenties

* [SWF-bestandsformaat](https://en.wikipedia.org/wiki/Swf)

