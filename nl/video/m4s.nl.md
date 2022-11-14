{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4S-bestand - Wat is een M4S-bestand?",
  "description":"Meer informatie over M4S-bestandsindeling en API's die M4S-bestanden kunnen maken en openen.",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## Wat is een M4S-bestand?

Een M4S-bestand is een klein segment van een video die via internet wordt gestreamd met behulp van de **MPEG-DASH**-streamingtechniek. Het bevat een videosegment in de vorm van binaire gegevens. De ontvangende applicatie (meestal een webbrowser of mediaspelers) speelt deze segmenten af in de volgorde waarin ze zijn ontvangen. Het eerste M4S-segment wordt geïdentificeerd door de initialisatiegegevens die het bevat. In **samenvatting** zijn M4S-bestanden kleine afzonderlijke mediasegmenten van een compleet bestand.

## M4S-bestandsindeling

M4S-bestanden zijn gebaseerd op het [ISO Base Media File (ISOBMFF)-formaat](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Deze kleine segmenten van een groot bestand kunnen onafhankelijk worden gedownload via HTTP. Als u dus een groot [MP4](/nl/video/mp4/) filmbestand heeft, kan het worden gestreamd met behulp van de MPEG-DASH-techniek (Dynamic Adaptive Streaming over HTTP) door het te segmenteren als M4S-segmentbestanden. Als dit grote filmbestand als M4S naar schijf wordt gedownload, worden meerdere M4S-bestanden gedownload. Als al deze .m4s-segmenten aaneengeschakeld zijn, wordt een volledig afspeelbaar bestand geproduceerd. De mediaspelers kunnen het bestand niet afspelen tenzij het eerste initialisatiesegment ook beschikbaar is bij het bestand.

## Over MPEG-DASH-streaming

MPEG-DASH maakt gebruik van adaptieve bitrate-streamingtechniek die het mogelijk maakt om media-inhoud van hoge kwaliteit via internet te streamen. Dit wordt gedaan door de inhoud op te splitsen in een reeks kleine segmenten die via HTTP worden gestreamd. Grote mediabestanden zoals film, podcasts of live-uitzendingen van een sportevenement kunnen op deze manier worden gestreamd. Deze segmenten worden gecodeerd met verschillende bitsnelheden. De MPEG-DASH-compatibele mediaspelers selecteren automatisch het segment met de hoogste bitsnelheid met behulp van een algoritme voor bitsnelheidsaanpassing. Dit voorkomt het vastlopen of opnieuw bufferen van gebeurtenissen in het afspelen.

### Open Source API voor M4S-bestanden

Er zijn open source API's beschikbaar die kunnen worden gebruikt om M4S-bestanden te lezen en te converteren.

* [libdash](https://github.com/bitmovin/libdash) - .NET API voor M4S-bestanden
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - Javascript-client voor M4S-bestand
* [Go Library voor het maken van Dash-bestanden](https://github.com/zencoder/go-dash)

### Open Source API om M4S naar MP4 te converteren

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Referenties ###

* [ISO Base Media File (ISOBMFF)-indeling](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [Dynamisch adaptief streamen via HTTP - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

