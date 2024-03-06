{
  "date": "2019-12-13",
  "keywords": [
"WAV",
"failu",
"pagarinājumu",
"formātā",
"audio apmaiņas faila formāts",
"mūzika"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par WAV failu formātu un API, kas var izveidot un atvērt WAV failus.",
  "title": "WAV — viļņu formas audio faila formāts",
  "linktitle": "WAV",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wa-lvv"
}
},
  "lastmod": "2019-12-13"
}

## Kas ir WAV fails?

WAV, kas pazīstams kā WAVE (viļņu formāta audio faila formāts), ir Microsoft Resource Interchange File Format (RIFF) specifikācijas apakškopa digitālo audio failu glabāšanai. Formāts nepiemēro bitu straumes saspiešanu un saglabā audio ierakstus ar atšķirīgu iztveršanas ātrumu un bitu pārraides ātrumu. Tas ir bijis un ir viens no audio kompaktdisku standarta formātiem. Wave faili ir lielāki, salīdzinot ar jauniem audio failu formātiem, piemēram, [MP3](/audio/mp3/), kas izmanto zudumu saspiešanu, lai samazinātu faila lielumu, vienlaikus saglabājot to pašu audio kvalitāti. Tomēr WAV failus var saspiest, izmantojot Audio Compression Manager (ACM) kodekus. Ir pieejamas vairākas API un lietojumprogrammas, kas var konvertēt WAV failus citos populāros audio failu formātos.

**Vai tu zināji?**
You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about WAV or Audio file formats, you can post your findings in [Audio File Format News](https://news.fileformat.com/t/audio) section for people to remain up to date.

## WAV faila formāts ##

WAVE faila formāts, kas ir Microsoft RIFF specifikācijas apakškopa, sākas ar faila galveni, kam seko datu gabalu secība. WAVE failam ir viens WAVE gabals, kas sastāv no diviem apakšgabaliem:

* "fmt" gabals — norāda datu formātu

* "datu" gabals — satur faktiskos paraugdatus


### WAV faila galvene ###

WAV (RIFF) faila galvene ir 44 baitus gara, un tai ir šāds formāts:


|Pozīcijas|Vērtības paraugs|Apraksts
---|---|---|
|1 - 4|RIFF|Atzīmē failu kā riff failu. Katras rakstzīmes garums ir 1 baits.
|5 - 8|Faila lielums (vesels skaitlis)|Kopējā faila lielums - 8 baiti, baitos (32 bitu vesels skaitlis). Parasti tas ir jāaizpilda pēc izveides.
|9 -12|WAVE|Faila tipa galvene. Mūsu vajadzībām tas vienmēr ir vienāds ar VILNI.
|13-16|fmt |Formatēt gabala marķieri. Ietver beigu nulli
|17-20|16|Formāta datu garums, kā norādīts iepriekš
|21-22|1|Formāta veids (1 ir PCM) — 2 baitu vesels skaitlis
|23-24|2|Kanālu skaits — 2 baitu vesels skaitlis
|25-28|44100|Iztveršanas ātrums — 32 baiti vesels skaitlis. Kopējās vērtības ir 44100 (CD), 48000 (DAT). Sample Rate = paraugu skaits sekundē vai herci.
|29-32|176400|(Sample Rate * BitsPerSample * Kanāli) / 8.
|33-34|4|(BitsPerSample * Kanāli) / 8.1 - 8 bitu mono2 - 8 bitu stereo/16 bitu mono4 - 16 bitu stereo
|35-36|16|Biti paraugā
|37-40|data|datu daļas galvene. Atzīmē datu sadaļas sākumu.
|41-44|Faila lielums (dati)|Datu sadaļas lielums.
|Iepriekš ir norādītas 16 bitu stereo avota paraugvērtības.

## Atsauces Nr.

* [WAV — Wikipedia](https://en.wikipedia.org/wiki/WAV)


