{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4S-fil - Vad är en M4S-fil?",
  "description":"Läs mer om M4S-filformat och API:er som kan skapa och öppna M4S-filer.",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## Vad är en M4S fil?

En M4S-fil är ett litet segment av en video som strömmas över internet med **MPEG-DASH** strömningstekniken. Den innehåller ett videosegment i form av binära data. Den mottagande applikationen (vanligtvis en webbläsare eller mediaspelare) spelar upp dessa segment i den ordning de tas emot. Det första M4S-segmentet identifieras av initialiseringsdata som det innehåller. I **sammanfattning** är M4S-filer små individuella mediesegment av en komplett fil.

## M4S filformat

M4S-filer är baserade på formatet [ISO Base Media File (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Dessa små segment av en stor fil kan laddas ner oberoende av varandra via HTTP. Således, om du har en stor [MP4](/sv/video/mp4/) filmfil, kan den streamas med MPEG-DASH (Dynamic Adaptive Streaming over HTTP)-tekniken genom att segmentera den som M4S-segmentfiler. Om den här stora filmfilen laddas ner till skivan som M4S, laddas flera M4S-filer ned. Om alla dessa .m4s-segment är sammanlänkade skapas en komplett spelbar fil. Mediaspelarna kan inte spela upp filen om inte det första initialiseringssegmentet också är tillgängligt med filen.

## Om MPEG-DASH-strömning

MPEG-DASH använder adaptiv bitrate streaming-teknik som gör det möjligt att streama högkvalitativt medieinnehåll över internet. Detta görs genom att dela upp innehållet i en sekvens av små segment som streamas över HTTP. Stora mediefiler som film, poddsändningar eller livesändningar av ett sportevenemang kan streamas på detta sätt. Dessa segment kodas med olika bithastigheter. Den MPEG-DASH-aktiverade mediaspelaren väljer automatiskt segmentet med den högsta bithastigheten med hjälp av en bithastighetsanpassningsalgoritm. Detta undviker att stoppa eller återbuffra händelser i uppspelningen.

### Open-Source API för M4S-filer

Det finns API:er med öppen källkod tillgängliga som kan användas för att läsa och konvertera M4S-filer.

* [libdash](https://github.com/bitmovin/libdash) - .NET API för M4S-filer
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - Javascript-klient för M4S-fil
* [Go Library för att skapa Dash-filer](https://github.com/zencoder/go-dash)

### Open-Source API för att konvertera M4S till MP4

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Referenser ###

* [ISO Base Media File (ISOBMFF) format](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [Dynamic Adaptive Streaming over HTTP - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

