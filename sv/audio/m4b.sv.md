{
  "date" : "2021-06-09",
  "keywords" :[ "m4b", "mp3", "fil", "tillägg", "format", "vad är m4b filformat", "musik", "m4b filformat", "M4b vs MP3", "m4b filformatspecifikation "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om M4B-filformat och API:er som kan skapa, konvertera och öppna M4B-filer.",
  "title" :"M4B - MPEG-4 ljudboksfilformat",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Vad är en M4B fil?

Filen med tillägget .m4b är en ljudbok som vanligtvis används av Apple Books och iTunes. Ljudet som används i detta format lagras i MPEG-4 och komprimeras med AAC-kodning. En M4B-fil är mycket lik M4A men har stöd för ljudboksrelaterade funktioner, såsom bokmärken och kapitelbrytningar. M4B-filerna finns tillgängliga i både DRM-aktiverade och DRM-fria versioner. DRM-krypterade ljudböcker är vanligtvis betalda ljudböcker från iTunes Store. Medan DRM-fri kan lätt hittas över internet.

## M4B filformat

Ljudboksfilerna som innehåller metadata, bilder, bokmärken och hyperlänkar kan sparas med .m4a-tillägget men vanligtvis används .m4b-tillägget när du sparar, bara för att ange att filen har ett ljudboksfilformat. Fairplay DRM (Digital Rights Management) används av application för att skydda sina M4B-filer. Så filerna som laddas ner från iTunes kan endast spelas på auktoriserade enheter eller datorer.


## M4B vs M4A

Både M4B och [MP3](/audio/mp3/) är filformat endast för ljud.

**M4B**: Vinner jämfört med MP3 vad gäller kvalitet om båda kodas med samma bithastighet. M4B är en ljudboksfil som är komprimerad med AAC-kodning. Det är i princip förknippat med "MPEG-4 Audio Layer", filer med .m4b-tillägget är ljudlagret för MPEG-4-filmer men med extra ljudboksrelaterade funktioner. Dess mål är att gå om MP3 och bli den nya standarden inom ljudkomprimering. Den är väldigt nära MP3 på många sätt men utvecklad för att ha bättre kvalitet i samma eller ännu mindre filstorlek. M4B-formatet introducerades först av Apple. Formattypen realiseras också som Apple Lossless Encoder (ALE).

Därför kunde M4B för närvarande inte få MP3:s mainstream-framgång eftersom ljudformatet inte är vanligt spelbart ännu.

**Mp3**: Ett digitalt ljudformat som är välbekant för alla. Ett allra första komprimeringsformat på scenen och blev mycket känt bland musiklyssnare. Dess vanliga framgång är så snabb att filtypen kan spelas universellt och kompatibel med nästan vad som helst, hårdvara eller mjukvara. I en allmän mening kommer M4A att producera bättre ljudkvalitet, men många skulle hävda att, oavsett om det är sant eller inte, är ljudskillnaden inte jämförbar, och det skulle vara ett slöseri med tid att försöka konvertera MP3-filer till M4A-filer. Slutligen kommer konverteringen bara att få dig att förlora den ursprungliga ljudkvaliteten.

## M4B filformatspecifikation

I likhet med [M4A](/sv/audio/m4a/), består M4B-filerna också av på varandra följande bitar. Varje bit har 8 byte header och uppdelad som:
- 4-byte bitstorlek (big-endian, hög byte först)
- 4-byte chunk typ - en av fördefinierade signaturer: "ftyp", "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "ctab", "hoppa", "jP2", "wide", "load", "imap", "matt", "chap", "kmat", "klipp", "crgn", "sync", "tmcd", "PICT ", "scpt", "ssrc".

I likhet med M4A kommer den första biten i M4B att vara av typen "ftype" och har en undertyp vid offset 8. M4B definieras av undertyp som måste vara "M4B_".

Itererar bitar, tills en bit av okänd typ upptäcks, kommer den att komponera M4B (MPEG-4 Audio) fil.

## Referenser

* [MPEG-4 del 14 - av Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format & Recovery Exempel](https://www.file-recovery.com/m4a-signature-format.htm)

