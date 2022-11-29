{
  "date" : "2021-06-09",
  "keywords" :[ "m4p", "mp3", "fil", "tillägg", "format", "vad är m4p filformat", "musik", "m4p filformat", "M4b vs MP3", "m4p filformatspecifikation "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Lär dig om M4P-filformat och API:er som kan skapa, konvertera och öppna M4P-filer.",
  "title" :"M4P - MPEG-4 ljudboksfilformat",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Vad är en M4P fil?
Filen med tillägget .m4p är en ljudfil som vanligtvis finns tillgänglig på Apple iTunes Store för nedladdning. Med andra ord kan vi säga att M4P är en AAC-fil men kopieringsskyddad genom att använda en Digital Rights Management (DRM). Det betyder att M4P-filer endast kan spelas på auktoriserade system eller enheter. Vanligtvis är M4P-filer specifika för Apples multimediaenheter. Så dessa filer kan bara spelas på Apple macbooks, podcasts, smarta telefoner som iPhone 6 eller iPhone 7.

## M4P filformat
M4P står för MPEG 4 Protected (audio), och den kodar ljudet med avancerad ljudkodek (AAC) och skyddar filen från obehörig användning av filen. Detta filformat betraktas vanligtvis som ljudfilformatet för en iTunes Music Store. Apple använder sitt FairPlay Digital Rights Management-system (DRM) för att skydda M4P-filer. FairPlay DRM är baserat på teknologi utvecklad av Veridisc. Dess skyddsmekanism fungerar genom att kryptera AAC-ljudströmmen med AES-krypteringen. Användaren får en huvudnyckel som tilldelas hans konto för dekryptering. Detta filformat introducerades som en ersättning för MP3-filformatet, eftersom MP3:n ursprungligen inte var tänkt som en ljudfil, utan som lager III i en MPEG 1 eller 2 videofil.


## M4P filformatspecifikationer

I likhet med [M4A](/sv/audio/m4a/), består M4P-filerna också av på varandra följande bitar. Varje bit har 8 byte header och uppdelad som:
- 4-byte bitstorlek (big-endian, hög byte först)
- 4-byte chunk typ - en av fördefinierade signaturer: "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "skip", "ftyp", "jP2", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT", "scpt ", "ctab", "ssrc".

I likhet med M4A kommer den första biten i M4P att vara av typen "ftype" och har en undertyp vid offset 8. M4P definieras av undertyp som måste vara "M4P_".

Itererar bitar, tills en bit av okänd typ upptäcks, kommer den att komponera M4P (MPEG-4 Audio) fil.

## Referenser ##

* [MPEG-4 del 14 - av Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format & Recovery Exempel](https://www.file-recovery.com/m4a-signature-format.htm)

