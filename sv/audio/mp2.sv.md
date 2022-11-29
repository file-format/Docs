{
  "date" : "2021-06-11",
  "keywords" :[ "mp2", "mp2-fil", "tillägg", "format", "vad är en mp2-fil", "musik", "mp2-filformat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om MP2-filformat och API:er som kan skapa, konvertera och öppna MP2-filer.",
  "title" :"MP2 - MPEG Layer 2 Audio File Format",
  "linktitle" : "MP2",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Vad är en MP2-fil?

En MP2-fil som också kallas MPA-fil är en ljudfil komprimerad med Layer II av MPEG-1 eller MPEG-2; ett förlustformat för ljudkomprimering definierat av ISO/IEC 11172-3 tillsammans med MPEG-1 Audio Layer I och MPEG-1 Audio Layer III ([MP3](/sv/audio/mp3/)), för att minska storleken på ljudfilen. Medan MP3 är mer populärt än MP2 på grund av dess mindre storlek och tillgänglighet över internet. Därför är MP2 fortfarande en viktig standard för ljudsändningar.

## MP2 filformat

MPEG Audio Layer II (MP2) är kärnalgoritmen i MP3-standarderna. MPEG-1 Audio Layer 2-kodning erhölls från MUSICAM audio codec. Det började som Digital Audio Broadcast (DAB)-projektet i Tyskland som en del av EUREKA-forskningsprogrammet. Eureka 147 innehöll tre huvudelement: Transmission Coding & Multiplexing, COFDM Modulation och MUSICAM Audio Coding (Masking pattern Universal Sub-band Integrated Coding And Multiplexing). MUSICAM var en av få kodningar som kunde uppnå hög ljudkvalitet vid bithastigheter i intervallet 64 till 192 kbit/s per monofonisk kanal. Målet var att tillhandahålla låg fördröjning, låg komplexitet, felrobusthet, korta accessenheter och uppfylla de tekniska kraven för sändning, telekommunikation och inspelning på digitala lagringsmedier.

MP2 är en subbandsljudkodare, som kan komprimeras i tidsdomänen med en lågfördröjningsfilterbank som genererar 32 frekvensdomänkomponenter. Som jämförelse är MP3 en transform ljudkodare med hybridfilterbank, vilket innebär att komprimering tillämpas i frekvensdomänen efter en hybridtransformation från tidsdomänen. MP2-kodaren kan utnyttja interkanalredundanser genom att använda valfri "gemensam stereo" intensitetskodning.

### MP2-filformatspecifikationer

MP2-filformatet är baserat på successiva digitala bildrutor med 1152 samplingsintervall med fyra möjliga format:

- monoformat
- stereoformat
- intensitetskodat gemensamt stereoformat (stereo irrelevans)
- format med dubbla kanaler (okorrelerat).
Några viktiga tekniska specifikationer för MP2 ges i tabellen nedan:

|Specifikation| Beskrivning|
---|---|
|**Samplingsfrekvens**| 32, 44,1 och 48 kHz|
|**Bithastigheter**|32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 och 384 kbit/s|
|**Ytterligare samplingsfrekvens**|16, 22,05 och 24 kHz|
|**Ytterligare bithastigheter**|8, 16, 24, 40 och 144 kbit/s|
|**Stöd för flera kanaler**|Upp till 5 ljudkanaler med full spektrum och en LFE-kanal (Low Frequency Enhancement-kanal)|

## Referenser ##

* [MPEG-1 Audio Layer II - Av Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

