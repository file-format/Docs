{
  "date" : "2021-03-12",
  "keywords" :[ "VP9", "Fil", "Tillägg", "Filformat", "Videoformat", "TrueMotion Video", "VPX", "On2 Technologies"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 - TrueMotion Video File",
  "description":"Läs mer om VP9-filformat och API:er som kan skapa och öppna VP9-filer.",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## Vad är VP9 fil?

Google har utvecklat VP9-codec som en royaltyfri, öppen källkodsstandard för videokodning som efterföljare till VP8. Det designades ursprungligen för att komprimera ultra HD-innehållet på YouTube eftersom det utökar och förbättrar kodningseffektiviteten hos sin föregångare. Om vi pratar om de ursprungliga VPX-codecna så kom de från On2 Technologies, som assimilerades av Google 2010. Google skapade senare codec med öppen källkod. VP8 och VP9 båda formaten är tillgängliga under en gratis BSD-licens som tillåter operatörer att organisera kodnings- eller avkodningsfärdigheter i både exklusiv programvara och öppen källkod utan att avslöja sin källkod.

## Tekniska egenskaper hos VP9

* VP9 tillhandahåller en maximal upplösning på 8192x4352 vid upp till 120 fps och flera färgrymder, med Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 och sRGB
* Hela utbudet av webb- och mobilanvändningsfall från komprimering med låg bithastighet till högkvalitativ ultra-HD, med ytterligare stöd för 10/12-bitars kodning och HDR stöds fullt ut av detta format
* Det kan minska videobithastigheter med så mycket som 50 % i jämförelse med andra
* Den är rustad för adaptiv streaming och används av YouTube och andra välkända webbvideoleverantörer
* Chrome-, Opera-, Edge-, Firefox- och Android-enheter, samt miljontals smarta TV-apparater, stöder avkodningen av denna codec
* Videoupplösningar över 1080p modifieras genom VP9 och tillåter förlustfri komprimering
* Olika färgrymder som Rec. 601, Rec. 709, Rec. 2020, SMPTE-170, SMPTE-240 och sRGB stöds av VP9
* HDR-video med Hybrid Log-Gamma och Perceptual Quantizer kan också stödjas av VP9


## Kortfattad bakgrund

* Utvecklingen av VP9-videocodec började 2011 och dess avkodare lades till i Chromium-webbläsaren i december 2012
* Den första versionen av webbläsaren Google Chrome släpptes i februari 2013 och släpptes avkodning vid den tiden
* Google släppte Chrome 29.0.1547 med slutgiltigt VP9-stöd i augusti 2013
* I oktober 2013 lades en instinktiv VP9-avkodare till FFmpeg
* Mozilla har lagt till VP9 näring till Firefox i december 2013 i version 2 som sedan släpptes den 18 mars 2014
 

## Fungerar av VP9

Vanligtvis ökar 4K-videon bildkvaliteten genom att göra specifika pixlar mindre, VP9-codec och HEVC gör dem större för att minska bithastigheten och filstorleken. Även om detta kan verka motsägelsefullt, tar kodningsmotorn de större pixlarna och ändrar dem till bättre upplösningsproduktivitet. Källvideo, som innefattar videoramar, kodas eller komprimeras för att skapa en komprimerad videobitström. Varje separat bildruta delas först in i block med pixlar. Blocken granskas sedan för tredimensionella avskedanden och sekventiella kopplingar mellan ramar utvärderas för att dra fördel av områden som inte kan ändras. Dessa kodas via rörelsevektorer som säkerställer egenskaperna hos det givna blocket på nästa bildruta. Restinformationen kodas med hjälp av en effektiv binär komprimering.

## Referenser

* [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9#:~:text=VP9%20is%20an%20open%20and,on%20Googles%20video%20platform%20YouTube)
* [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
* [Coconut](https://www.coconut.co/)

