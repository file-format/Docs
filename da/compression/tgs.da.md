{
  "date": "2019-10-11",
  "keywords": [
"tgs fil",
"tgs filformat",
"hvad er en tgs fil",
"fil",
"tgs eksempel",
"tgs filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TGS - Telegram Animated Sticker File Format",
  "description": "Lær om TGS filformat og API'er, der kan oprette og åbne TGS filer.",
  "linktitle": "TGS",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tg-das"
}
},
  "lastmod": "2021-04-02"
}

## Hvad er TGS fil?

En fil med filtypenavnet .tgs er en animeret klistermærkefil, der blev introduceret af meddelelsestjenesten på tværs af platforme, [Telegram](https://core.telegram.org/stickers#animated-stickers). Animerede klistermærker bruges af brugere af beskedapps til at sende mere forbedret og livligt indhold i beskeder i modsætning til den statiske grafik, der er stillbilleder. Telegram brugte oprindeligt filformatet [WEBP](/image/webp/) til stillbilledklistermærker. TGS-filformatet kan gemme animationsdata i højere opløsninger og mindre filstørrelse sammenlignet med de statiske WEBP-klistermærker. TGS-filer kan åbnes ved hjælp af programmer som Telegram, 7-zip, Apple Archive Utility og Corel WinZip.

## TGS filformat

Telegram introducerede TGS-filformatet tilbage i juli 2019 baseret på Lottie-biblioteket. En TGS-fil består af [JSON](/web/json/)-tekst, der eksporteres fra en animation i Adobe After Effects. Den eksporterede JSON-tekst komprimeres ved hjælp af gzip-komprimeringen, som reducerer filstørrelsen. JSON-oplysningerne om tekstfilen gemmes i en tekstfil, der bliver grundlaget for høje komprimeringsrater.

### TGS Stickers Specifikationer

TGS-filformatet pålægger visse begrænsninger for oprettelsen af TGS animerede klistermærker. En TGS animeret fil:

 * Sticker/lærredsstørrelse skal være 512×512 pixels.
 * Klistermærkegenstande må ikke forlade lærredet.
 * Animationens længde må ikke overstige 3 sekunder.
 * Alle animationer skal loopes.
 * Stickerstørrelse må ikke overstige 64 KB efter gengivelse i Bodymovin.
 * Alle animationer skal køre med 60 billeder pr. sekund.

### Eksempel på TGS JSON-tekst

Et eksempel på animeret klistermærke, når det er pakket ud, indeholder følgende JSON-tekstindhold.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Referencer ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)


