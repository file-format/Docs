{
  "date": "2019-12-13",
  "keywords": [
"WAV",
"fil",
"udvidelse",
"format",
"lydudvekslingsfilformat",
"musik"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om WAV-filformat og API'er, der kan oprette og åbne WAV-filer.",
  "title": "WAV - Waveform Audio File Format",
  "linktitle": "WAV",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wa-dav"
}
},
  "lastmod": "2019-12-13"
}

## Hvad er en WAV fil?

WAV, kendt for WAVE (Waveform Audio File Format), er en undergruppe af Microsofts RIFF-specifikation (Resource Interchange File Format) til lagring af digitale lydfiler. Formatet anvender ingen komprimering til bitstrømmen og gemmer lydoptagelserne med forskellige samplingshastigheder og bithastigheder. Det har været og er et af standardformaterne for lyd-cd'er. Wave-filer er større i størrelse sammenlignet med nye lydfilformater som f.eks. [MP3](/audio/mp3/), som bruger tabskomprimering til at reducere filstørrelsen og samtidig bevare den samme lydkvalitet. WAV-filer kan dog komprimeres ved hjælp af Audio Compression Manager (ACM) codecs. Der er flere tilgængelige API'er og applikationer, der kan konvertere WAV-filer til andre populære lydfilformater.

**Vidste du?**
You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about WAV or Audio file formats, you can post your findings in [Audio File Format News](https://news.fileformat.com/t/audio) section for people to remain up to date.

## WAV-filformat ##

WAVE-filformatet, der er en delmængde af Microsofts RIFF-specifikation, starter med en filoverskrift efterfulgt af en sekvens af datastykker. En WAVE-fil har en enkelt WAVE-chunk, som består af to under-chunks:

* en "fmt" chunk - angiver dataformatet

* en "data" chunk - indeholder de faktiske eksempeldata


### WAV-filoverskrift ###

Overskriften på en WAV (RIFF) fil er 44 bytes lang og har følgende format:


|Positioner|Eksempelværdi|Beskrivelse
---|---|---|
|1 - 4|RIFF|Markerer filen som en riff-fil. Tegn er hver 1 byte lange.
|5 - 8|Filstørrelse (heltal)|Størrelse af den samlede fil - 8 bytes, i bytes (32-bit heltal). Typisk vil du udfylde dette efter oprettelsen.
|9 -12|WAVE|Filtypeoverskrift. Til vores formål er det altid lig med WAVE.
|13-16|fmt |Formater chunk markør. Inkluderer efterfølgende nul
|17-20|16|Længde af formatdata som angivet ovenfor
|21-22|1|Formattype (1 er PCM) - 2 byte heltal
|23-24|2|Antal kanaler - 2 byte heltal
|25-28|44100|Samplehastighed - 32 byte heltal. Fælles værdier er 44100 (CD), 48000 (DAT). Sample Rate = Antal prøver pr. sekund, eller Hertz.
|29-32|176400|(Sample Rate * BitsPerSample * Kanaler) / 8.
|33-34|4|(BitsPerSample * kanaler) / 8.1 - 8 bit mono2 - 8 bit stereo/16 bit mono4 - 16 bit stereo
|35-36|16|Bits pr. prøve
|37-40|data|data chunk header. Markerer begyndelsen af dataafsnittet.
|41-44|Filstørrelse (data)|Størrelse på datasektionen.
|Eksempelværdier er givet ovenfor for en 16-bit stereokilde.

## Referencer ##

* [WAV - af Wikipedia](https://en.wikipedia.org/wiki/WAV)


