{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TS File Format - Video Transport Stream File",
  "keywords" :[ "ts", "fluga", "tillägg", "tillägg", ".ts", "format" ],
  "description":"Läs mer om vad en TS-fil och API:er är som kan skapa och öppna TS-filer.",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## Vad är TS fil?

En fil med tillägget .ts är en videoström som lagrar data på DVD-skivor. Den använder MPEG-2 ([.mpeg](/sv/video/mpg/)) komprimeringsalgoritm för att uppnå maximal effektivitet och kompatibilitet mellan olika medietyper såsom internetströmning och sändning. TS-filformatet skapades så att det kan spelas upp på enheter med dåliga internetanslutningar, till exempel smart-TV.

## TS-filformat - Mer information

Data i en TS-fil liknar [MP4](/sv/video/mp4/)-fil, men den är uppdelad i små bitar. Varje bit består av en liten bit av video, följt av lite ljud och en valfri bildtext. En enda TS-fil består av många sådana bitar. Förutom video, ljud och bildtext, består varje bit också av ytterligare data för att upptäcka fel i biten. På grund av detta är TS-filer något större i storlek.

### Varför använda TS-filformat?

Så, om TS-filer är något stora i storlek, vilken fördel erbjuder det att använda dem istället för andra filformat? Tja, i sändningar kan de små bitarna av video och ljud skickas över kommunikationsmedia (kabel eller radio) i realtid. Den extra datan i bitarna används av mottagaren för att hoppa över de felbenägna bitarna.

Dessutom används TS-filer eftersom sändningssystemet inte behöver hela strömmen för att spela upp den. Sändningen kan plockas upp och kan användas i realtid genom att montera ljud och bild.

## Hur spelar man TS-filer?

Tja, TS-filer kan öppnas och spelas upp i populära [VideoLAN VLC media player](https://www.videolan.org/vlc/features.html) som är gratis tillgänglig för nedladdning.

## Referenser ##

* [MPEG Transport Stream - Wikipedia](https://en.wikipedia.org/wiki/MPEG_transport_stream)

