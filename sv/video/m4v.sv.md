{
  "date" : "2019-10-11",
  "keywords" :[ "M4V", "fil", "tillägg", "format", "MPEG-4", "Digital Rights Management", "DRM", "Apple", "video"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"Läs mer om M4V-filformat och API:er som kan skapa och öppna M4V-filer.",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## Vad är en M4V fil?

**M4V**-filformatet, utvecklat av Apple, är en videobehållare som eventuellt är skyddad med Digital Rights Management (DRM) kopieringsskydd för att skydda integritet eller kopiering. Videor och ljudspår lindas runt av containerfiler för att indexera och organisera uppspelningsströmmar. Dessutom ger behållare också funktioner för kapitel som liknar dem på DVD-skivor. Apple använder M4V för att koda videor i sin iTunes Store. Det skyddar obehörig reproduktion genom Apples FairPlay-kopieringsskydd genom att tillåta att M4V-filer spelas upp på endast auktoriserade datorer som har kontona som används för att köpa videon. Men om DRM-skydd tas bort från M4V-filer kan dessa filer spelas upp i andra videospelare genom att ändra filtillägget från .m4v till .mp4, vilket är anledningen till att M4V-filer associeras med MPEG-4. M4V använder H.264 för video och **[AAC](/sv/audio/aac/)** och Dolby Digital för ljudkodning och avkodning.

## M4V-filstruktur ##

M4V-filer har kontinuerliga bitar med 8 byte header, 4 byte chunk storlek och 4 byte chunk typ i varje chunk. Den första delen är "ftype" och har en undertyp vid offset 8. M4V definieras av undertyp som måste vara "M4V_". Ytterligare bittyper är fördefinierade signaturer: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide" , "ladda", "ctab", "imap", "matt", "kmat", "klipp", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", " BILD". Itererande bitar, tills okänd typ upptäcks, komponerar vi M4V-fil.

Här är en undersökning av ett prov: En provm4v-fils binära data inspekteras genom Hex Viewer och det kan observeras att den börjar med en signatur **ftyp** (hex: 66 74 79 70) vid offset 4, som definierar QuickTime Behållarfiltyp. Filens undertyp är **M4V_** (hex: 4D 34 56 20) vilket pekar på filtypen M4V (MPEG-4). Första blockstorleken är 32 (hex: 00 00 00 20, big-endian, hög byte först), storleken placerad vid offset 0. Vid offset 32 (hex: 20) finns den andra biten, som har en storlek på 30 322 (hexadecimal) : 00 00 76 72, big-endian, lägre byte först) och skriv **moov** (hex: 6D 6F 6F 76). Nästa bit är placerad vid offset 32+30,322#30,354 (hex: 00 00 76 92) och har en storlek 8 (hex: 00 00 00 08) och typ **fri** (hex: 66 72 65 65).
### Codecs som används i M4V ###

#### Video Codec H.264 ####

H.264 är en videokomprimeringsstandard som konverterar digital video till ett format som kräver mindre utrymme vid överföring eller lagring. M4V använder H.264 för videokomprimering. Dess applikation sträcker sig från DVD, TV, videokonferenser och videoströmning över internet. H.264 består av två huvuddelar: Encoder – Som komprimerar videon, Decoder – Som dekomprimerar tillbaka den komprimerade videon. I figuren nedan är kodnings- och avkodningsprocesser framhävda, och andra processer täcks av H.264-standarden.

##### Videokodnings- och avkodningsprocess i H.264 #####

För den komprimerade H.264-bitströmmen utför videokodaren förutsägelse-, transformations- och kodningsprocessen. Samtidigt utför avkodaren den omvända processen av avkodning, omvänd transformation och rekonstruktion för att producera tillbaka videofilen. H.264 tar hälften så stor som MPEG.

#### Audio Codec ####

Advanced Audio Coding (AAC) är en ljudkodek för digital ljudkomprimering med förlust och används i en M4V-behållare. AAC är efterföljaren till formatet [MP3](/sv/audio/mp3/) och uppnår bättre kvalitet än MP3 med samma bithastighet. AAC-format kastar bort en del information under komprimeringsprocessen, vilket är av mindre betydelse. AAC är en variabel bithastighet (VBR) blockbaserad codec där varje block avkodar till 1024 tidsdomänsampel.

### Referenser ###

* [Wikipedia - M4V](https://en.wikipedia.org/wiki/M4V)
* [Wikipedia - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)

