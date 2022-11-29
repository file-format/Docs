{
  "date" : "2021-04-26",
  "keywords" :[ "aiff", "fil", "tillägg", "format", "audio utbyte filformat", "musik", "aiff filformat", "aiff till mp3", "aiff vs wav", "konvertera aiff till mp3" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om AIFF-filformat och API:er som kan skapa, konvertera och öppna AIFF-filer.",
  "title" :"AIFF - Audio Interchange File Format",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Vad är en AIFF-fil?
AIFF (Audio Interchange File Format) är ett okomprimerat ljudfilformat utvecklat av Apple 1998, men är baserat på **EA IFF 85** (Standard for Interchange Format Files utvecklad av Electronic Arts), ett omslagsformat som används på Amiga-system . Detta filformat kommer med en standard för lagring av samplade ljud. Formatet är tillräckligt bra i flexibilitet och möjliggör lagring av mono- eller flerkanalssamplade ljud med olika samplingshastigheter och samplingsbredder. Eftersom AIFF-filerna är okomprimerade gör detta att de blir större än andra förlustformat som [MP3](https://docs.fileformat.com/audio/mp3/).

AIFF-filer består av 2 kanaler okomprimerat stereoljud med 16 bitars samplingsstorlek, inspelad vid 44,1 khz. På grund av hög ljudkvalitet kan ett 5 minuters ljud ta upp till 50 MB diskutrymme, vilket liknar filformatet [WAV](https://docs.fileformat.com/audio/wav/).

## AIFF vs WAV

AIFF och WAV är nästan samma när det gäller kvalitet. Båda använder samma PCM-kodning (pulskodmodulering), vilket gör dem större i storlek jämfört med andra förlustformat, såsom [MP3](https://docs.fileformat.com/audio/mp3/), [M4A](). Några av de allmänna skillnaderna är skrivna i tabellen nedan:

|AIFF|WAV|
---|---|
|Används mest för MAC|Används mest för PC|
|Tillåter metadeta| Tillåter inte metadeta|

## AIFF-filstruktur

**EA IFF 85** anger en övergripande struktur för lagring av data i filer. En **EA IFF 85**-fil består av ett antal databitar. En bit är byggande block av AIFF-filen består av viss rubrikinformation följt av data:
{{< figure src="../chunk.png" alt="AIFF-bit" >}}

En AIFF-fil är en samling av ett antal olika typer av bitar. Det finns två generella typer av bitar som är viktiga för att bilda en AIFF-filbit:
- **Common Chunk**: Innehåller viktiga parametrar som beskriver det samplade ljudet, såsom dess längd och samplingshastighet.
- **Sound Data Chunk**: Innehåller de faktiska ljudproverna.
Det finns många andra valfria bitar som listar instrumentparametrar, definierar markörer, lagrar applikationsspecifik information, etc.

### Lokala bittyper

Bittyperna för att bilda AIFF anges i tabellen nedan:

|Chunk Type| Beskrivning|
---|---|
|Common Chunk|Common Chunk beskriver grundläggande parametrar för det samplade ljudet|
|Ljuddataklump|Ljuddataklumpen innehåller de faktiska exempelramarna|
|Marker Chunk|Marker Chunk innehåller markörer som pekar på positioner i ljuddata|
|Instrument Chunk|Instrument Chunk definierar grundläggande parametrar som ett instrument, såsom en sampler, kan använda för att spela upp ljuddata|
|MIDI Data Chunk|MIDI Data Chunk kan användas för att lagra MIDI-data|
|Audio Recording Chunk|Ljudinspelningsdelen innehåller information som är relevant för ljudinspelningsenheter|
|Application Specific Chunk|Den Application Specific Chunk kan användas för alla ändamål av tillverkare av applikationer|
|Comments Chunk|The Comments Chunk används för att lagra kommentarer i FORM AIFF|
|Textbitar - Namn, författare, upphovsrätt, anteckning| Alla är textbitar|

## Referenser ##

* [Audio Interchange File Format - Av Wikipedia](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)

