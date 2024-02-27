{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TS File Format - Video Transport Stream File",
  "keywords" : [ "ts", "flie", "extension", "extension", ".ts", "format" ],
  "description":"Lær om, hvad en TS-fil og API'er er, der kan oprette og åbne TS-filer.",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts-da",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## Hvad er TS fil?

En fil med filtypenavnet .ts er en videostream, der gemmer dataene på dvd'er. Den bruger MPEG-2 ([.mpeg](/video/mpg/)) komprimeringsalgoritme for at opnå maksimal effektivitet og kompatibilitet på tværs af forskellige medietyper såsom internetstreaming og broadcasting. TS-filformatet blev oprettet, så det kan afspilles på enheder med dårlige internetforbindelser, såsom smart-tv.

## TS-filformat - flere oplysninger

Data i en TS-fil ligner [MP4](/video/mp4/)-fil, men den er opdelt i små bidder. Hver del består af et lille stykke video, efterfulgt af en smule lyd og en valgfri billedtekst. En enkelt TS-fil består af mange sådanne bidder. Ud over video, lyd og billedtekst, består hver chunk også af nogle ekstra data til at opdage fejl i chunken. På grund af dette er TS-filer noget større i størrelse.

### Hvorfor bruge TS-filformat?

Så hvis TS-filer er lidt store i størrelse, hvilken fordel giver det så at bruge dem i stedet for andre filformater? Tja, i broadcasting kan de små bidder af video og lyd sendes over kommunikationsmediet (kablet eller radio) i realtid. De ekstra data i bidderne bruges af modtageren til at springe de fejltilbøjelige bidder over.

Derudover bruges TS-filer, fordi udsendelsessystemet ikke behøver hele streamen for at afspille det. Transmissionen kan opfanges og kan bruges i realtid ved at samle lyd og video.

## Hvordan afspiller man TS-filer?

Nå, TS-filer kan åbnes og afspilles i populære [VideoLAN VLC media player](https://www.videolan.org/vlc/features.html), som er frit tilgængelig til download.

## Referencer ##

* [MPEG Transport Stream - Wikipedia](https://en.wikipedia.org/wiki/MPEG_transport_stream)


