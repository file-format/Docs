{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "fil", "tillägg", "format", "vad är en amr-fil", "musik", "amr-filformat", "amr-fil", "konvertera amr-fil till mp3", "spela amr-fil" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om AMR-filformat och API:er som kan skapa, konvertera och öppna AMR-filer.",
  "title" :"AMR - Adaptiv Multi-Rate Codec File",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## Vad är AMR fil?
Filen med tillägget .amr är ett ljuddataformat som är relevant för **Adaptive Multi-Rate** audiocodec; består av en multi-rate smalbandstal-codec som kodar smalbandssignaler med 4,75-12,2 kbit/s bithastighet med tullkvalitetstal som börjar vid 7,4 kbit/s; använder länkanpassning för att välja från en av åtta olika bithastigheter.

## AMR filformat
AMR-filformat använder många kodningstekniker, ACELP-algoritmen (Algebraic Code Excited Linear Prediction) är en av de bästa teknikerna; designad för att komprimera mänskligt talat ljud på ett mer effektivt sätt. AMR sattes som standard röst- eller tal-codec av 3GPP 1999. AMR-filformatet används också för att lagra det talade ljudet genom att använda **Adaptive Multi-Rate** audiocodec som används av många smarta telefoner för att lagra inspelade tal.

### Filformatstruktur
AMR( Adaptive Multi-Rate) är ett ljudformat; används ofta i olika mobila applikationer och enheter, vanligtvis i ljudspelare/inspelare eller i VoIP-applikationer. AMR kan vidare klassificeras som:

1. AMR-NB( NarrowBand )
2. AMR-WB( WideBand )

Vanligtvis hänvisar AMR till AMR-NB. AMR-filformatet har följande struktur:

Varje AMR-fil innehåller en 6-byte header som känner igen filen som ett AMR-ljud. Denna rubrik är alltid inställd på:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Detta är vanligtvis likt för alla AMR-NB-filer. Om rubriken följer en standard är det troligt att filen är skadad och inte bör användas. AMR-filen består av ett helt antal packade ramar av ljud. Dessa ramar komponerar var och en 20 ms ljud. Varje ram kan kodas med vilket som helst av de giltiga AMR-NB-lägena (0-7, 8 SID i DTX-läge). Eftersom ramarna kan kodas med olika bithastigheter kallas denna typiska metod Adaptive Multi-Rate (AMR).
#### AMR-lägen
Följande är de olika AMR-lägena och deras motsvarande bithastigheter:

|LÄGE| BIT PRISER|
---|---|
|0| AMR 4,75 - Kodar vid 4,75 kbit/s|
|1 | AMR 5.15 - Kodar vid 5.15kbit/s|
|2 | AMR 5.9 - Kodar vid 5,9 kbit/s|
|3 | AMR 6.7 - Kodar vid 6,7 kbit/s|
|4 | AMR 7.4 - Kodar vid 7,4 kbit/s|
|5 | AMR 7,95 - Kodar vid 7,95 kbit/s|
|6 | AMR 10.2 - Kodar vid 10,2 kbit/s|
|7 | AMR 12.2 - Kodar vid 12,2 kbit/s|

Ramstorlek för AMR-lägen i byte (inklusive rubrikbyte) ges nedan:

|CMR |LÄGE |RAMSTORLEK( i byte )|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7,95 |21|

## Referenser ##

* [Adaptive Multi-Rate audio codec - av Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [RTP nyttolastformat och fillagringsformat för AMR- och AMR-WB-ljudcodecs](https://tools.ietf.org/html/rfc4867#page-35)

