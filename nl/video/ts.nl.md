{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TS-bestandsindeling - Videotransportstreambestand",
  "keywords" :[ "ts", "flie", "extensie", "extensie", ".ts", "format" ],
  "description":"Meer informatie over wat een TS-bestand is en API's die TS-bestanden kunnen maken en openen.",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## Wat is een TS-bestand?

Een bestand met de extensie .ts is een videostream waarin de gegevens op dvd's worden opgeslagen. Het maakt gebruik van MPEG-2 ([.mpeg](/nl/video/mpg/)) compressie-algoritme om maximale efficiëntie en compatibiliteit te bereiken tussen verschillende mediatypes, zoals internetstreaming en uitzendingen. Het TS-bestandsformaat is gemaakt zodat het kan worden afgespeeld op apparaten met slechte internetverbindingen, zoals smart TV.

## TS-bestandsindeling - Meer informatie

Gegevens in een TS-bestand lijken op het [MP4](/nl/video/mp4/)-bestand, maar zijn opgedeeld in kleine stukjes. Elk stuk bestaat uit een klein stukje video, gevolgd door een stukje audio en een optioneel bijschrift. Een enkel TS-bestand bestaat uit veel van dergelijke brokken. Naast video, audio en ondertiteling, bevat elk stuk ook enkele aanvullende gegevens voor het detecteren van fouten in het stuk. Hierdoor zijn TS-bestanden wat groter van formaat.

### Waarom het TS-bestandsformaat gebruiken?

Dus, als TS-bestanden nogal groot zijn, welk voordeel biedt het dan om ze te gebruiken in plaats van andere bestandsformaten? Welnu, bij uitzendingen kunnen de kleine stukjes video en audio in realtime via de communicatiemedia (bedraad of radio) worden verzonden. De extra data in de chunks wordt door de ontvanger gebruikt om de foutgevoelige chunks over te slaan.

Bovendien worden TS-bestanden gebruikt omdat het omroepsysteem niet de hele stream nodig heeft om deze af te spelen. De transmissie kan worden opgehaald en in realtime worden gebruikt door audio en video samen te stellen.

## Hoe TS-bestanden afspelen?

Welnu, TS-bestanden kunnen worden geopend en afgespeeld in de populaire [VideoLAN VLC-mediaspeler](https://www.videolan.org/vlc/features.html), die gratis kan worden gedownload.

## Referenties ##

* [MPEG-transportstroom - Wikipedia](https://en.wikipedia.org/wiki/MPEG_transport_stream)

