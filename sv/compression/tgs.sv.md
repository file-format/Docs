{
  "date" : "2019-10-11",
  "keywords" :[ "tgs fil", "tgs filformat", "vad är en tgs fil", "fil", "tgs exempel", "tgs filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - Telegram Animated Sticker File Format",
  "description":"Läs mer om TGS-filformat och API:er som kan skapa och öppna TGS-filer.",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Vad är TGS fil?

En fil med filtillägget .tgs är en animerad klistermärkefil som introducerades av den plattformsoberoende meddelandetjänsten [Telegram](https://core.telegram.org/stickers#animated-stickers). Animerade klistermärken används av användare av meddelandeappar för att skicka mer förbättrat och livligt innehåll i meddelanden till skillnad från den statiska grafiken som är stillbilder. Telegram använde ursprungligen filformatet [WEBP](/sv/image/webp/) för stillbildsetiketter. TGS-filformatet kan lagra animationsdata med högre upplösningar och mindre filstorlek jämfört med statiska WEBP-klistermärken. TGS-filer kan öppnas med applikationer som Telegram, 7-zip, Apple Archive Utility och Corel WinZip.

## TGS filformat

Telegram introducerade TGS-filformatet redan i juli 2019 baserat på Lottie-biblioteket. En TGS-fil består av [JSON](/sv/web/json/) text som exporteras från en animation i Adobe After Effects. Den exporterade JSON-texten komprimeras med gzip-komprimeringen som minskar filstorleken. JSON-informationen om textfilen lagras i en textfil som blir grunden för höga komprimeringshastigheter.

### TGS Stickers Specifikationer

TGS-filformatet sätter vissa begränsningar på skapandet av TGS animerade klistermärken. En TGS-animerad fil:

* Storleken på klistermärken/duken måste vara 512×512 pixlar.
* Dekalföremål får inte lämna duken.
* Animationens längd får inte överstiga 3 sekunder.
* Alla animationer måste vara loopade.
* Stickerstorlek får inte överstiga 64 KB efter rendering i Bodymovin.
* Alla animationer måste köras med 60 bilder per sekund.

### Exempel på TGS JSON-text

Ett exempel på animerad klistermärke, när den är uppackad, innehåller följande JSON-textinnehåll.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Referenser ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

