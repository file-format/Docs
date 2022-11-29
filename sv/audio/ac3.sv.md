{
  "date" : "2019-12-13",
  "keywords" :[ "AC3", "fil", "tillägg", "format", "Ljudkodning", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om AC3-filformat och API:er som kan skapa och öppna AC3-filer.",
  "title" :"AC3 - Audio Codec 3-fil",
  "linktitle" : "AC3",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## Vad är AC3 fil?

En fil med filtillägget .ac3 är en Audio Codec 3-fil, introducerad av Dolby Laboratories. Det är ett ljudformat som kan innehålla upp till sex kanaler med ljudutgång. Formatet hade ursprungligen använts för ljud men används nu även för andra applikationer som HDTV-sändningar, DVD-skivor, Blue-ray-skivor och spelkonsoler. Applikationer som kan öppna AC3-filer inkluderar Apple QuickTime-spelare, Microsoft Windows Media Player, Winamp, MPlayer och andra liknande.

## AC3 filformat

AC3-filer är binära till sin natur och baserade på Modified Discrete Cosine Transform (MDCT) som är en komprimeringsalgoritm med förlust. Dolby Laboratories använde MDCT-algoritmen tillsammans med perceptuella kodningsprinciper för att utveckla AC-3-ljudformatet. Detta ledde till lanseringen av AC-3-formatet som Dolby Digital-standarden 1991. Formatet stöder tillhandahållandet av fem kanaler för normalhögtalare (20 Hz - 20 000 Hz) och en kanal (20 Hz - 120 Hz) för de subwooferdrivna lågfrekventa effekterna. AC3 stöder samplingshastigheter upp till 48 kHz.

### Tekniska detaljer för AC3-filformat

Dolby Digital-tekniken använder ett mycket effektivt sätt att komprimera storleken på flerkanaliga ljudfiler utan att försämra ljudkvaliteten. Denna komprimering leder till mindre filstorlek vilket gör det enkelt att distribuera ljudfilerna. Med Dolby Digital är det möjligt att inkludera en fullständig 5.1-kanals ljudmix på en filmutskrift eller en DVD.

#### Specifikationer
Dolby Digital-specifikationerna är följande.

|Fält|Specifikation|
---|---|
|Kanaler |1.0 till 5.1, diskret|
|DVD-datahastighet, 5.1-kanals ljud| 384 eller 448 kbps|
|Blu-ray Disc-datahastighet, 5.1-kanals ljud|640 kbps|
|Stöder Dolby-metadata |Ja|
|Anslutningar |S/PDIF, HDMI®, IEEE 1394|
|Mixing/streamingfunktioner|Ja|

#### MetaData-parametrar

|Metadataparameter| Information|Kontroll|
---|---|---|
|Dialognivå| |Ja|
|Kanalläge| | Ja|
|LFE-kanal| | Ja|
|Bitströmsläge| Ja| Ja|
|Linjelägeskomprimering| | Ja|
|RF-lägeskomprimering| | Ja|
|RF övermodulationsskydd| | Ja|
|Centrera nedblandningsnivå| | Ja|
|Surround downmix nivå| | Ja|
|Dolby Surround-läge| |Ja|
|Ljudproduktionsinformation| Ja||
|Mixnivå| Ja||
|Rumstyp| Ja||
|Copyright bit| Ja||
|Original bitström| Ja||
|Föredraget stereodownmix| |Ja|
|Lt/Rt Center nedblandningsnivå||Ja|
|Lt/Rt Surround-downmixnivå||Ja|
|Lo/Ro Center downmix nivå||Ja|
|Lo/Ro Surround-downmixnivå||Ja|
|Dolby Digital Surround EX™-läge||Ja|
|A/D-omvandlartyp|Ja||
|DC-filter||Ja|
|Lågpassfilter||Ja|
|LFE lågpassfilter||Ja|
|Surround 3 dB dämpning||Ja|
|Surroundfasförskjutning||Ja|

## Referenser

* [AC3 - Av Wikiepedia](https://en.wikipedia.org/wiki/Dolby_Digital)
* [Dolby Digital 5.1](https://professional.dolby.com/tv/dolby-digital)

