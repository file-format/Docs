{
  "date": "2021-03-12",
  "keywords": [
"VP9",
"Fil",
"Udvidelse",
"Filformat",
"Videoformat",
"TrueMotion video",
"VPX",
"On2 teknologier"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "VP9 - TrueMotion videofil",
  "description": "Lær om VP9-filformat og API'er, der kan oprette og åbne VP9-filer.",
  "linktitle": "VP9",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-vp-da9"
}
},
  "lastmod": "2021-03-27"
}

## Hvad er en VP9 fil?

Google has developed the VP9 codec as a royalty-free, open-source video coding standard as the successor to VP8. Det blev oprindeligt designet til at komprimere ultra HD-indholdet på YouTube, fordi det udvider og forbedrer kodningseffektiviteten af sin forgænger. Hvis vi taler om de originale VPX-codecs, kom de fra On2 Technologies, som blev assimileret af Google i 2010. Google åbnede senere codec'et. VP8 og VP9 begge formater er tilgængelige under en gratis BSD-licens, der tillader operatører at organisere indkodning eller afkode færdigheder i både eksklusiv software og open source-software uden at afsløre deres kildekode.

## Tekniske funktioner i VP9

* VP9 giver en maksimal opløsning på 8192x4352 ved op til 120 fps og flere farverum med Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 og sRGB
* Hele udvalget af web- og mobilbrugssager fra komprimering med lav bithastighed til højkvalitets ultra-HD med yderligere understøttelse af 10/12-bit-kodning og HDR understøttes fuldt ud af dette format
* Det kan reducere video bithastigheder med så meget som 50% i sammenligning med andre
* Den er rustet til adaptiv streaming og bruges af YouTube og andre velkendte webvideoudbydere
* Chrome-, Opera-, Edge-, Firefox- og Android-enheder samt millioner af smart-tv'er understøtter afkodningen af denne codec
* Videoopløsninger større end 1080p modificeres gennem VP9 og tillader tabsfri komprimering
* Forskellige farverum som Rec. 601, Rec. 709, Rec. 2020, SMPTE-170, SMPTE-240 og sRGB understøttes af VP9
* HDR-video ved hjælp af Hybrid Log-Gamma og Perceptual Quantizer kan også understøttes af VP9


## Kort historie

 *  Udviklingen af VP9-videocodec startede i 2011, og dens dekoder blev tilføjet Chromium-webbrowseren i december 2012
 *  Dens første Google Chrome-webbrowserversion blev udgivet i februar 2013 og udgav afkodning på det tidspunkt
 *  Google udgav Chrome 29.0.1547 med VP9 endelig support i august 2013
 *  I oktober 2013 blev en instinktiv VP9-dekoder tilføjet til FFmpeg
 *  Mozilla har føjet VP9-underhold til Firefox i december 2013 i version 2, der derefter blev udgivet den 18. marts 2014
 
## Arbejder med VP9

Normalt øger 4K-videoen billedkvaliteten ved at gøre specifikke pixels mindre, VP9-codec og HEVC gør dem større for at nedskalere bithastigheden og filstørrelsen. Selvom dette kan virke modstridende, tager kodningsmotoren de større pixels og ændrer dem til bedre opløsningsproduktivitet. Kildevideo, der omfatter videorammer, kodes eller komprimeres for at lave en komprimeret videobitstream. Hver separat ramme er først opdelt i blokke af pixels. Blokkene bliver derefter undersøgt for tredimensionelle afskedigelser, og sekventielle forbindelser mellem frames evalueres for at drage fordel af områder, der ikke kan ændres. Disse er kodet via bevægelsesvektorer, der sikrer kvaliteterne af den givne blok på den næste frame. Den resterende information kodes ved hjælp af en effektiv binær komprimering.

## Referencer

 * [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9)
 * [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
 * [Kokosnød](https://www.coconut.co/)

