{
  "date" : "2019-12-13",
  "keywords" :[ "WAV", "fil", "tillägg", "format", "ljudutbytesfilformat", "musik" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om WAV-filformat och API:er som kan skapa och öppna WAV-filer.",
  "title" :"WAV - Waveform Audio File Format",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## Vad är en WAV-fil?

WAV, känt för WAVE (Waveform Audio File Format), är en delmängd av Microsofts RIFF-specifikation (Resource Interchange File Format) för lagring av digitala ljudfiler. Formatet tillämpar ingen komprimering på bitströmmen och lagrar ljudinspelningarna med olika samplingshastigheter och bithastigheter. Det har varit och är ett av standardformaten för ljud-CD-skivor. Wave-filer är större i storlek jämfört med nya ljudfilformat som [MP3](/sv/audio/mp3/) som använder förlustkomprimering för att minska filstorleken med bibehållen ljudkvalitet. WAV-filer kan dock komprimeras med Audio Compression Manager (ACM) codecs. Det finns flera API:er och applikationer tillgängliga som kan konvertera WAV-filer till andra populära ljudfilformat.

**Visste du?**
Du kan bli en bidragsgivare på FileFormat.com för att hålla filformatgemenskapen uppdaterad med dina resultat. Om du måste dela något om WAV- eller ljudfilformat kan du lägga upp dina resultat i avsnittet [Audio File Format News](https://news.fileformat.com/t/audio) så att folk kan hålla sig uppdaterade.

## WAV-filformat ##

WAVE-filformatet, som är en delmängd av Microsofts RIFF-specifikation, börjar med ett filhuvud följt av en sekvens av databitar. En WAVE-fil har en enda "WAVE"-bit som består av två underklumpar:

* en "fmt"-bit - anger dataformatet
* en "data"-bit - innehåller den faktiska exempeldatan

### WAV-filhuvud ###

Rubriken på en WAV (RIFF) fil är 44 byte lång och har följande format:


|Positioner|Exempelvärde|Beskrivning
---|---|---|
|1 - 4|"RIFF"|Markerar filen som en rifffil. Tecken är var och en 1 byte lång.
|5 - 8|Filstorlek (heltal)|Storlek på den övergripande filen - 8 byte, i byte (32-bitars heltal). Vanligtvis skulle du fylla i detta efter att du skapat det.
|9 -12|"WAVE"|Filtypshuvud. För våra ändamål är det alltid lika med "WAVE".
|13-16|"fmt "|Formatera chunk markör. Inkluderar efterföljande null
|17-20|16|Längd på formatdata enligt listan ovan
|21-22|1|Typ av format (1 är PCM) - 2 byte heltal
|23-24|2|Antal kanaler - 2 byte heltal
|25-28|44100|Samplingshastighet - 32 byte heltal. Vanliga värden är 44100 (CD), 48000 (DAT). Samplingshastighet = Antal samplingar per sekund, eller Hertz.
|29-32|176400|(Samplingshastighet * BitsPerSample * Kanaler) / 8.
|33-34|4|(BitsPerSample * Kanaler) / 8.1 - 8 bitars mono2 - 8 bitars stereo/16 bitars mono4 - 16 bitars stereo
|35-36|16|Bitar per prov
|37-40|"data"|"data" chunk header. Markerar början av datasektionen.
|41-44|Filstorlek (data)|Storlek på datasektionen.
|Samplevärden ges ovan för en 16-bitars stereokälla.

## Referenser ##

* [WAV - av Wikipedia](https://en.wikipedia.org/wiki/WAV)

