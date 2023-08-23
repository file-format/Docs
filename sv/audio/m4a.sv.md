{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "fil", "tillägg", "format", "vad är m4a filformat", "musik", "m4a filformat", "M4A vs MP3", "m4a filformatspecifikation "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om M4A-filformat och API:er som kan skapa, konvertera och öppna M4A-filer.",
  "title" :"M4A - MPEG-4 ljudfil",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Vad är en M4A fil?

**M4A-filformatet** är en ljudfil skapad med hjälp av AAC (Advanced Audio Coding) som är känd som en förlustkomprimering. Ordet M4A förkortas till MPEG 4 Audio. Dessa ljudfiler har vanligtvis filtillägget .m4a. Detta gäller särskilt oskyddat innehåll. Den kan lagra olika typer av ljudinnehåll, såsom ljudböcker, sånger och podcaster. M4A är vanligtvis realiserat som mer avancerat format än MP3, som vanligtvis inte hade utformats för enbart ljud. Det är bara ett ljudlager i MPEG 1 eller 2 videofiler.

M4A-formatet är krypterat av FairPlay Digital Rights Management som såldes via iTunes Store med tillägget .m4p. Apple iPhones använder MPEG-4-ljud för sina ringsignaler, men de ljudfilerna använder tillägget .m4r.


## M4A vs MP3

Både M4A och [MP3](/audio/mp3/) är filformat endast för ljud.

**M4A**: Bättre än MP3 vad gäller kvalitet och storlekar när den kodas med samma bithastighet. Filtillägget .m4a är så vanligt eftersom de har använts av Apple för användning i iTunes Music Store. M4A är en ljudfil som är komprimerad med MPEG-4-teknik; en algoritm för komprimering med förlust. Det är i princip associerat med "MPEG-4 Audio Layer", filer med .m4a-tillägget är ljudlagret för MPEG-4-filmer. Det är tänkt att gå om MP3 och bli den nya standarden inom ljudkomprimering. Det är mycket nära MP3 på många sätt men introducerat för att ha en bättre kvalitet i samma eller ännu mindre filstorlek. M4A-formatet introducerades först av Apple. Formattypen realiseras också som Apple Lossless Encoder (ALE).

Därför kunde M4A för närvarande inte få MP3:s mainstream-framgång eftersom ljudformatet i allmänhet inte är spelbart ännu. Det är på något sätt endast begränsat till MacOS, iPod och andra Apple-produkter.

**Mp3**: Det mest kända digitala ljudformatet. Det var också ett av de första komprimeringsformaten på scenen och blev mycket populärt bland musikälskare. Dess vanliga framgång är så snabb att filtypen kan spelas universellt och med nästan vad som helst, hårdvara eller mjukvara. Generellt sett kommer M4A att producera bättre ljudkvalitet, men många skulle hävda att, oavsett om det är sant eller inte, är ljudskillnaden inte urskiljbar, och det skulle vara ett slöseri med tid att försöka konvertera MP3-filer till M4A-filer. Så småningom kommer konverteringen bara att få dig att förlora den ursprungliga ljudkvaliteten.

## M4A filformatspecifikation

M4A-filerna består av på varandra följande bitar. Varje bit har 8 byte header och uppdelad som:
- 4-byte bitstorlek (big-endian, hög byte först)
- 4-byte chunk typ - en av fördefinierade signaturer: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt ", "ssrc", "PICT".

Den första delen kommer att vara av typen "ftype" och har en undertyp vid offset 8. M4A definierad av undertyp som måste vara "M4A_", för M4B måste undertyp vara "M4B_" och för M4P måste undertyp vara "M4P_".

Itererar bitar, tills en bit av okänd typ upptäcks, kommer den att komponera M4A (MPEG-4 Audio) fil.

## Referenser ##

* [MPEG-4 del 14 - av Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format & Recovery Exempel](https://www.file-recovery.com/m4a-signature-format.htm)

