{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "bestand", "extensie", "format", "wat is een amr-bestand", "muziek", "amr-bestandsformaat", "amr-bestand","converteer amr-bestand naar mp3", "amr-bestand afspelen"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over AMR-bestandsindeling en API's die AMR-bestanden kunnen maken, converteren en openen.",
  "title" :"AMR - Adaptief Multi-Rate Codec-bestand",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## Wat is een AMR-bestand?
Het bestand met de extensie .amr is een audiogegevensformaat dat relevant is voor de **Adaptive Multi-Rate** audiocodec; bestaat uit een smalbandige spraakcodec met meerdere snelheden die smalbandsignalen codeert met een bitsnelheid van 4,75-12,2 kbit/s en spraak met tolkwaliteit vanaf 7,4 kbit/s; gebruikt koppelingsaanpassing om uit een van de acht verschillende bitsnelheden te kiezen.

## AMR-bestandsindeling
Het AMR-bestandsformaat maakt gebruik van veel coderingstechnieken, het ACELP-algoritme (Algebraic Code Excited Linear Prediction) is een van de beste technieken; ontworpen om menselijke gesproken audio op een efficiëntere manier te comprimeren. De AMR is in 1999 door 3GPP ingesteld als de standaard spraak- of spraakcodec. Het AMR-bestandsformaat wordt ook gebruikt om de gesproken audio op te slaan met behulp van **Adaptive Multi-Rate** audiocodec die door veel smartphones wordt gebruikt om opgenomen toespraken.

### Structuur van bestandsindeling
De AMR (Adaptive Multi-Rate) is een audioformaat; veel gebruikt in verschillende mobiele toepassingen en apparaten, meestal in audiospeler/recorder of in VoIP-achtige toepassingen. AMR kan verder worden geclassificeerd als:

1. AMR-NB (Smalband)
2. AMR-WB (breedband)

Meestal verwijst AMR naar AMR-NB. Het AMR-bestandsformaat heeft de volgende structuur:

Elk AMR-bestand bevat een 6-byte header die het bestand herkent als een AMR-audio. Deze header is altijd ingesteld op:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Dit is meestal hetzelfde voor alle AMR-NB-bestanden. Als de header een standaard volgt, is het bestand waarschijnlijk beschadigd en mag het niet worden gebruikt. het AMR-bestand bestaat uit een geheel aantal ingepakte audioframes. Deze frames vormen elk 20 ms audio. Elk frame kan worden gecodeerd met behulp van een van de geldige AMR-NB-modi (0-7, 8 SID in DTX-modus). Aangezien de frames met verschillende bitsnelheden kunnen worden gecodeerd, wordt deze typische methode Adaptive Multi-Rate (AMR) genoemd.
#### AMR-modi
Hieronder volgen de verschillende AMR-modi en de bijbehorende bitrates:

|MODUS| BIT-TARIEVEN|
---|---|
|0| AMR 4.75 - Codeert met 4.75kbit/s|
|1 | AMR 5.15 - Codeert met 5.15kbit/s|
|2 | AMR 5.9 - Codeert met 5,9 kbit/s|
|3 | AMR 6.7 - Codeert met 6.7kbit/s|
|4 | AMR 7.4 - Codeert met 7.4kbit/s|
|5 | AMR 7.95 - Codeert met 7.95kbit/s|
|6 | AMR 10.2 - Codeert met 10,2kbit/s|
|7 | AMR 12.2 - Codeert met 12.2kbit/s|

Framegrootte van AMR-modi in bytes (inclusief de header-byte) worden hieronder gegeven:

|CMR |MODE |FRAME SIZE( in bytes )|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7,95 |21|

## Referenties ##

* [Adaptive Multi-Rate audiocodec - Door Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [RTP Payload-indeling en bestandsopslagindeling voor AMR- en AMR-WB Audio-codecs](https://tools.ietf.org/html/rfc4867#page-35)

