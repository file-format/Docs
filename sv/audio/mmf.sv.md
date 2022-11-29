{
  "date" : "2021-08-09",
  "keywords" :[ "mmf", "fil", "tillägg", "format", "ljud", "smaf", "mmf förlängning", "mmf filer", "mobil musikfil", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om MMF-filformat och API:er som kan skapa och öppna MMF-filer.",
  "title" :"MMF - Mobile Music File Format",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## Vad är en MMF fil?

MMF är ett filtillägg som är associerat med en SMAF-fil. MMF står för Mobile Music File medan SMAF står för syntetisk musik Mobile Application Format. MMF-filerna i en smartphone innehåller systemringsignaler, ljud och kan även innehålla grafik och textvisning. MMF innehåller vidare tre typer av instrumentparametrar inklusive FM, PCM och Stream PCM. Dessa filformat är kompatibla med Windows systemplattform. MMF-filerna kategoriseras som datafiler. Vanligtvis stöder Microsoft Mail MMF-filer. Filen med MMF-suffix kan kopieras till vilken mobil enhet eller systemplattform som helst.

Dessutom är dessa filer mycket mindre i storlek jämfört med vanliga MIDI-formatfiler. [WAV](/sv/audio/wav/)- och [MID](/sv/audio/mid/)-filer kan konverteras till MMF-format som sedan kan delas och distribueras som ljudinnehåll. Dessa filer kan tas emot via e-post direkt till telefoner och PC.


## Kort historik över MMF-filformat

Yamaha utvecklade SMAF-verktyg som ljudfiler så att smartphones kan lagra ett större antal unika ringsignaler. Yamaha introducerade SMAF med produktionen av deras MA-1, MA-2, MA-3, MA-5 och MA-7 LSI-ljudchips. Alla dessa format blev ganska välbekanta bland mobiltelefoner på den östasiatiska marknaden under början av 2000.

På internationell nivå godkändes MMF-formatet av Samsung. Med hjälp av MMF-formatet kunde Samsung designa ett brett utbud av polyfoniska ringsignaler som skulle användas i Samsungs smartphones.

Yamaha ville göra formatet ännu mer populärt och så vidare de officiella Yamaha SMAF-filerna publicerade det fler verktyg som var kompatibla med detta format. Med detta kan användare nu enkelt spela MMF-filer på sina datorer.


## MMF filformatspecifikationer ##

MMF-filer är kategoriserade i datasektioner. En prefixstruktur runt en 8-byte används för att beskriva varje segment.
4-byte-etiketten inkluderar CNTI, OPDA, MSTR, MTR och ATR. Datastorlek plus 8 byte är chunkstorleken; hela filstorleken beräknas genom att summera alla bitstorlekar. Om en fil inte har skadats ska den summerade filstorleken vara densamma som en primär huvudstorlek.

### Rubrik ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Här är ett exempel på MMF-fil:

![](../mmf.png)

## Referenser

* [MMF - av Wikipedia](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)

