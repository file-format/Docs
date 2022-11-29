{
  "date" : "2022-07-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om WEBA-filformat och API:er som kan skapa och öppna WEBA-filer.",
  "title" :"WEBA - Vad är en WebA-fil?",
  "linktitle" : "WEBA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2022-07-13"
}

## Vad är WEBA fil?

En WEBA är ett ljudfilformat som bara innehåller ljudet som extraherats från [WEBM](/sv/video/webm/) videofiler. Den komprimeras med OGG Vorbis-komprimeringscodec, vilket resulterar i en minskad filstorlek. Detta gör överföring av WEBA-filer enklare över internet. Användningen av [OGG](https://en.wikipedia.org/wiki/Ogg) Vorbis-komprimering gör att WEBA-filer kan stödjas i de flesta mediespelare.

**Visste du?**
Du kan bli en bidragsgivare på FileFormat.com för att hålla filformatgemenskapen uppdaterad med dina resultat. Om du måste dela något om WAV- eller ljudfilformat kan du lägga upp dina resultat i avsnittet [Audio File Format News](https://news.fileformat.com/t/audio) så att folk kan hålla sig uppdaterade.

## WEBA-filformat - Mer information

WEBA-filer komprimeras med OGG Vorbis-komprimering och sparas på skiva som binära filer. OGG är ett gratis containerfilformat med öppen källkod och ger effektiv streaming och hantering av högkvalitativ digital multimedia. Eftersom den kan multiplexera ett antal oberoende ljud-, video-, text- och metadataströmmar, ger den det idealiska sättet att lagra ljud som extraherats från WEBM-filer.

WEBA-filformatet ligger i avsnittet Endast ljud i WEBM-filformatspecifikationerna som visas nedan.

|Fält|Beskrivning|
---|---|
|MIME-typ |video/webm|
|Enbart ljud av MIME-typ |audio/webm|
|Uniform Type Identifier| org.webmproject.webm|
|Video Codec Namn| VP8 eller VP9|
|Ljud Codec Namn| Vorbis eller Opus|

## Hur konverterar man WEBA-fil till SubRip SRT-fil?

WEBA är en ljudfil, så den kan inte konverteras till en undertextfil. Det finns dock fria tal-till-text-konverterare som kan ta WEBA-filen som indata och konvertera den till SubRip SRT-fil. Ett sådant verktyg är det AI-baserade verktyget Sonix som kan konvertera WEBA-filer till SRT online.

## Hur konverterar man WEBA till andra ljudformat?

WEBA-filer kan konverteras till andra ljudfilformat. Eftersom det är baserat på OGG-containerfilformatet med öppen källkod, många API:er och applikationer som kan läsa och konvertera WEBA till andra filformat som [MP3](/sv/audio/mp3/), [MP4](/sv/audio/ mp4/), [FLAC](/sv/audio/flac/) och många andra. FFmpeg är en sådan programvara som kan konvertera WEBA till en MP3-fil.

## Referenser

* [OGG-filformat](https://en.wikipedia.org/wiki/Ogg)

