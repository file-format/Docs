{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMV-bestandsindeling",
  "description":"Meer informatie over WMV-bestandsindeling en API's die WMV-bestanden kunnen maken en openen.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## Wat is een WMV-bestand?

Het Advanced Systems Format (ASF) is een digitale multimediacontainer die voornamelijk is ontworpen voor het opslaan en verzenden van mediastreams. Microsoft Windows Media Video (WMV) is het gecomprimeerde videoformaat en Microsoft Windows Media Audio (WMA) is het gecomprimeerde audioformaat samen met extra metadata in de ASF-container die door Microsoft is ontwikkeld. Zodra de WMV- of WMA-bestanden zijn gecodeerd met Windows Media Video- en Windows Media Audio-codecs, worden ze weergegeven met de extensie .asf. WMV comprimeert grote bestanden voor een betere overdrachtssnelheid via een netwerk met behoud van de kwaliteit van de video. WMV is speciaal ontworpen om op alle Windows-apparaten te draaien. Na de standaardisatie door de Society of Motion Picture and Television Engineers (SMPTE), wordt WMV nu beschouwd als een open standaardformaat.

## Geschiedenis ##

Met behulp van eigen codecs van Microsoft werd in 1999 een nieuw gecomprimeerd videoformaat ontwikkeld, bekend als WMV7, dat was gebaseerd op MPEG-4 Part 2. Verbeteringen werden toegevoegd in nog twee versies, namelijk WMV8 en 9. Microsoft diende een 9^^th^^ versie in van WMV naar SMPTE voor standaardisatie in 2003, die uiteindelijk in 2006 werd gestandaardiseerd als SMPTE 421M, ook bekend als VC-1. Het idee achter de WMV was om een mediaformaat te ontwikkelen dat door alle door Microsoft ondersteunde hardware en software zou kunnen worden ondersteund. Verder was een ander belangrijk doel om videostreams in een optimaal scenario over het internet te verzenden. Na de standaardisatie van SMPTE werd WMV ook een videoformaat voor Blu-ray discs.

## Specificaties bestandsindeling

### Container

Over het algemeen wordt WMV verpakt in een ASF-container, maar daarnaast kunnen Matroska- of AVI-containers het ook ondersteunen met extensies van respectievelijk .mkv en .avi.

### Windows Media Video 9

Hoewel er verschillende audio- en videocodecs beschikbaar zijn in de Windows Media Video 9-serie voor het schrijven en afspelen van digitale media, is de WMV-9-codec de nieuwste en beste videocodec omdat deze de optimale compressie kan bereiken vanaf zeer lage bitsnelheden, namelijk 160 x 120 bij 10 Kbps tot 1920 x 1080 bij 4-8 Mbps voor een verscheidenheid aan HD-video's.

### Structuur van Codec

WMV-9 heeft een 8 bit 4:2:0 intern kleurformaat. Net als alle andere populaire videocompressiestandaarden MPEG-1 en H.261, gebruikt WMV-9 een op blokken gebaseerd bewegingscompensatie- en ruimtelijke transformatieschema. Over het algemeen kunnen we zeggen dat deze standaarden blok-voor-blok bewegingscompensatie uitvoeren van het vorige gereconstrueerde frame met behulp van een 2D-grootheid die de bewegingsvector (MV) wordt genoemd om ruimtelijke verplaatsing te signaleren. Het huidige blok wordt gevormd met behulp van het voorspellen van de waarden van het vorige gereconstrueerde frame van dezelfde grootte dat door de bewegingsvector van de huidige positie wordt verplaatst. Uiteindelijk wordt de restfout berekend als het verschil tussen het bewegingsgecompenseerde voorspelde blok en het werkelijke blok. Deze restfout wordt getransformeerd met behulp van een lineaire energiecompacterende transformatie en vervolgens gekwantiseerd en entropiegecodeerd.

Gekwantiseerde transformatiecoëfficiënten worden entropiegedecodeerd, gedekwantiseerd en invers getransformeerd om een benadering van de restfout aan de decoderzijde te produceren, die vervolgens wordt toegevoegd aan de bewegingsgecompenseerde voorspelling om de reconstructie te genereren. De beschrijving op hoog niveau van de codec wordt weergegeven in de volgende afbeelding.

De rest van de sectie zal de nieuwe verbeteringen in WMV-9 bespreken die het onderscheiden van de rest van de videocoderingsoplossingen zoals MPEG-standaarden. WMV-9 heeft intra (I), voorspelde (P) en bidirectioneel voorspelde (B) frames. Intraframes zijn frames die onafhankelijk gecodeerd zijn en niet afhankelijk zijn van andere frames. Voorspelde frames zijn frames die afhankelijk zijn van één frame in het verleden. Decodering van een voorspeld frame kan alleen plaatsvinden nadat alle referentieframes voorafgaand aan het huidige frame, beginnend bij het meest recente (I) frame, zijn gedecodeerd. B-frames zijn frames die twee referenties hebben: één in het tijdelijke verleden en één in de tijdelijke toekomst. B-frames worden verzonden na hun referenties, wat betekent dat B-frames in de verkeerde volgorde worden verzonden om ervoor te zorgen dat hun referenties beschikbaar zijn op het moment van decodering. B-frames in WMV-9 worden niet gebruikt als referentie voor volgende frames. Dit plaatst B-frames buiten de decoderingslus, waardoor snelkoppelingen kunnen worden genomen tijdens het decoderen van B-frames zonder drift of langdurige visuele artefacten. De bovenstaande definitie van I-, P- en B-frames geldt voor zowel progressieve als geïnterlinieerde sequenties.

De prestaties van videocodecs worden vergeleken met hun snelheidsvervormingsplot (RD). Het is een 2D-curve die de vervorming weergeeft die wordt geproduceerd door de compressie bij een bepaalde bitsnelheid.

WMV-9 heeft dit probleem aangepakt met de introductie van een aantal onderstaande technieken:

1. Transformatie van adaptieve blokgrootte

2. Beperkte precisietransformatieset

3. Bewegingscompensatie

4. Kwantisering en dekwantisering

5. Geavanceerde entropiecodering

6. Lusfiltering

7. Geavanceerde B-framecodering

8. Interlace-codering

9. Overlapping vloeiend maken

10. Hulpprogramma's met een laag tarief

11. Fading compensatie

## Referenties ##

* [https://bytescout.com/blog/2014/10/windows-media-video-format.html](https://bytescout.com/blog/2014/10/windows-media-video-format.html )
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)
* [http://citeseerx.ist.psu.edu/viewdoc/download?doi#10.1.1.101.488&rep#rep1&type#pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi#10.1 .1.101.488&rep#rep1&type#pdf)

