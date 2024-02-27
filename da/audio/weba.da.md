{
  "date": "2022-07-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om WEBA-filformat og API'er, der kan oprette og åbne WEBA-filer.",
  "title": "WEBA - Hvad er en WebA fil?",
  "linktitle": "WEBA",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-web-daa"
}
},
  "lastmod": "2022-07-13"
}

## Hvad er en WEBA fil?

En WEBA er et lydfilformat, der kun indeholder lyden udtrukket fra [WEBM](/video/webm/) videofiler. Det komprimeres ved hjælp af OGG Vorbis-komprimeringscodec, hvilket resulterer i en reduceret filstørrelse. Dette gør transmission af WEBA-filer nemmere over internettet. Brugen af [OGG](https://en.wikipedia.org/wiki/Ogg) Vorbis-komprimering gør det muligt at understøtte WEBA-filer i de fleste medieafspillere.

**Vidste du?**
You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about WAV or Audio file formats, you can post your findings in [Audio File Format News](https://news.fileformat.com/t/audio) section for people to remain up to date.

## WEBA-filformat - flere oplysninger

WEBA-filer komprimeres ved hjælp af OGG Vorbis-komprimering og gemmes på disk som binære filer. OGG er et gratis og open source-containerfilformat og giver effektiv streaming og styring af digitale multimedier af høj kvalitet. Da det kan multiplekse en række uafhængige lyd-, video-, tekst- og metadatastrømme, giver det det ideelle middel til at gemme lyd udvundet fra WEBM-filer.

WEBA-filformatet ligger i afsnittet Kun lyd i WEBM-filformatspecifikationerne som vist nedenfor.

|Felt|Beskrivelse|
---|---|
|MIME-type |video/webm|
|Lyd-kun MIME-type |audio/webm|
|Uniform Type Identifier| org.webmproject.webm|
|Video Codec Navn| VP8 eller VP9|
|Lyd Codec Navn| Vorbis eller Opus|

## Sådan konverteres WEBA fil til SubRip SRT fil?

WEBA er en lydfil, så den kan ikke konverteres til en undertekstfil. Der er dog fri tale-til-tekst-konvertering, der kan tage WEBA-filen som input og konvertere den til SubRip SRT-fil. Et sådant værktøj er det AI-baserede værktøj Sonix, der kan konvertere WEBA-filer til SRT online.

## Hvordan konverteres WEBA til andre lydformater?

WEBA-filer kan konverteres til andre lydfilformater. Da det er baseret på det gratis og open source OGG-containerfilformat, er der mange API'er og applikationer, der kan læse og konvertere WEBA til andre filformater såsom [MP3](/audio/mp3/), [MP4](/video/mp4/), [FLAC](/audio/flac/), og mange andre. FFmpeg er en sådan software, der kan konvertere WEBA til en MP3-fil.

## Referencer

* [OGG-filformat](https://en.wikipedia.org/wiki/Ogg)


