{
  "date": "2022-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M4S fil - Hvad er en M4S fil?",
  "description": "Lær om M4S filformat og API'er, der kan oprette og åbne M4S filer.",
  "linktitle": "M4S",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-m4-das"
}
},
  "lastmod": "2022-07-18"
}

## Hvad er en M4S fil?

En M4S-fil er et lille segment af en video, der streames over internettet ved hjælp af **MPEG-DASH**-streamingteknikken. Den indeholder et videosegment i form af binære data. Den modtagende applikation (normalt en webbrowser eller medieafspillere) afspiller disse segmenter i den rækkefølge, de modtages. Det første M4S-segment identificeres af de initialiseringsdata, det indeholder. I **resumé** er M4S-filer små individuelle mediesegmenter af en komplet fil.

## M4S filformat

M4S-filer er baseret på [ISO Base Media File (ISOBMFF) format](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Disse små segmenter af en stor fil kan downloades uafhængigt via HTTP. Så hvis du har en stor [MP4](/video/mp4/) filmfil, kan den streames ved hjælp af MPEG-DASH (Dynamic Adaptive Streaming over HTTP) teknikken ved at segmentere den som M4S segmentfiler. Hvis denne store filmfil downloades til disken som M4S, downloades flere M4S-filer. Hvis alle disse .m4s-segmenter er sammenkædet, produceres en komplet fil, der kan afspilles. Medieafspillerne kan ikke afspille filen, medmindre det første initialiseringssegment også er tilgængeligt med filen.

## Om MPEG-DASH-streaming

MPEG-DASH bruger adaptiv bitrate streaming teknik, der gør det muligt at streame højkvalitets medieindhold over internettet. Dette gøres ved at opdele indholdet i en sekvens af små segmenter, der streames over HTTP. Store mediefiler såsom film, podcasts eller live-udsendelse af en sportsbegivenhed kan streames på denne måde. Disse segmenter er kodet ved forskellige bithastigheder. De MPEG-DASH-aktiverede medieafspillere vælger automatisk segmentet med den højeste bithastighed ved hjælp af en bithastighedstilpasningsalgoritme. Dette undgår at gå i stå eller genbuffere begivenheder i afspilningen.

### Open-Source API til M4S-filer

Der findes open source API'er, som kan bruges til at læse og konvertere M4S-filer.

 * [libdash](https://github.com/bitmovin/libdash) - .NET API til M4S-filer
 * [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - Javascript-klient til M4S-fil
 * [Go Library til oprettelse af Dash-filer](https://github.com/zencoder/go-dash)

### Open-Source API til at konvertere M4S til MP4

 * [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Referencer ###

* [ISO Base Media File (ISOBMFF) format](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)

* [Dynamic Adaptive Streaming over HTTP - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)


