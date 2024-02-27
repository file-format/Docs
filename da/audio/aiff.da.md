{
  "date": "2021-04-26",
  "keywords": [
"aiff",
"fil",
"udvidelse",
"format",
"lydudvekslingsfilformat",
"musik",
"aiff filformat",
"aiff til mp3",
"aiff vs wav",
"konverter aiff til mp3"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om AIFF-filformat og API'er, der kan oprette, konvertere og åbne AIFF-filer.",
  "title": "AIFF - Audio Interchange File Format",
  "linktitle": "AIFF",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-aif-daf"
}
},
  "lastmod": "2021-04-26"
}

## Hvad er en AIFF fil?
AIFF (Audio Interchange File Format) er et ukomprimeret lydfilformat udviklet af Apple i 1998, men er baseret på **EA IFF 85** (Standard for Interchange Format Files udviklet af Electronic Arts), et indpakningsformat, der bruges på Amiga-systemer . Dette filformat kommer med en standard til lagring af samplede lyde. Formatet er godt nok i fleksibilitet og muliggør lagring af mono- eller flerkanals samplede lyde ved forskellige samplehastigheder og samplebredder. Da AIFF-filerne er ukomprimerede, gør dette dem større i størrelse end andre tabsgivende formater såsom [MP3](/audio/mp3/).

AIFF-filer består af 2 kanaler ukomprimeret stereolyd med 16 bits samplestørrelse, optaget ved 44,1 khz. På grund af høj lydkvalitet kan en 5 minutters lyd tage op til 50 MB diskplads, hvilket svarer til filformatet [WAV](/audio/wav/).

## AIFF vs WAV

AIFF og WAV er næsten det samme med hensyn til kvalitet. Begge bruger samme PCM (pulse-code modulation)-kodning, hvilket gør dem større i størrelse sammenlignet med andre tabsgivende formater, såsom [MP3](/audio/mp3/), [M4A](/audio/m4a/). Nogle af de generelle forskelle er skrevet i tabellen nedenfor:

|AIFF|WAV|
---|---|
|Bruges mest til MAC|Benyttes mest til pc'er|
|Tillader metadeta| Tillader ikke metadeta|

## AIFF-filstruktur

**EA IFF 85** opstiller en overordnet struktur for lagring af data i filer. En **EA IFF 85**-fil består af et antal bidder af data. En del er byggeblok af AIFF-filen består af nogle headeroplysninger efterfulgt af data:
{{< figure src="../chunk.png" alt="AIFF Chunk" >}}

En AIFF-fil er en samling af en række forskellige typer bidder. Der er to generelle typer bidder, som er vigtige for at danne en AIFF-filklump:
- **Common Chunk**: Indeholder vigtige parametre, der beskriver den samplede lyd, såsom dens længde og samplehastighed.
- **Sound Data Chunk**: Indeholder de faktiske lydeksempler.
Der er mange andre valgfrie bidder, der viser instrumentparametre, definerer markører, gemmer applikationsspecifik information osv.

### Lokale chunktyper

Klumptyperne til at danne AIFF er angivet i tabellen nedenfor:

|Chunk Type| Beskrivelse|
---|---|
|Common Chunk|Common Chunk beskriver grundlæggende parametre for den samplede lyd|
|Sound Data Chunk|Lyd Data Chunk indeholder de faktiske sample frames|
|Marker Chunk|Marker Chunk indeholder markører, der peger på positioner i lyddataene|
|Instrument Chunk|Instrument Chunk definerer grundlæggende parametre, som et instrument, såsom en sampler, kan bruge til at afspille lyddata|
|MIDI Data Chunk|MIDI Data Chunk kan bruges til at gemme MIDI data|
|Audio Recording Chunk|Lyd Recording Chunk indeholder oplysninger, der er relevante for lydoptagelsesenheder|
|Application Specific Chunk|Den Application Specific Chunk kan bruges til ethvert formål af producenter af applikationer|
|Comments Chunk|Comments Chunk bruges til at gemme kommentarer i FORM AIFF|
|Tekstbidder - Navn, Forfatter, Ophavsret, Annotering| Alle er tekststykker|

## Referencer ##

* [Audio Interchange File Format - Af Wikipedia](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)


