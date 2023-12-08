{
"datum":"2023-10-18",
   "keywords":[
"kö",
"cue-fil",
"cue cdrwin cue sheet-fil",
"hur man öppnar en cue-fil",
"fil",
"cue filtillägg",
"förlängning",
"fil"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"utkast":"falskt",
"toc":true,
"title":"CUE-filformat - CDRWIN Cue Sheet",
   "description":"Läs mer om CUE CDRWIN Cue Sheet-filformat och API:er som kan skapa och öppna CUE-filer.",
   "linktitle":"CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin",
         "parent":"disc-and-media"
}
},
"lastmod":"2023-10-18"
}

## Vad är en CUE fil?

En **.CUE**-fil, även känd som **CDRWIN Cue Sheet**, är en vanlig textfil som innehåller information om spår och layout för en ljud-CD eller skivbild, vanligtvis i BIN- eller ISO-format. Dessa filer används ofta för att beskriva skivans struktur och innehåll, vilket gör att programvara för CD-bränning eller programvara för virtuella enheter kan återge originalskivan korrekt.

## Exempel på CUE-fil

Här är ett exempel på hur ".cue"-filen kan se ut:

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## CDRWIN Cue Sheet

CDRWIN Cue Sheet är en specifik variant av filformatet ".cue" som används av CDRWIN-programvaran. CDRWIN är programvara för att bränna och skapa CD/DVD och dess ".cue"-ark är designade för användning med denna programvara. Dessa ".cue"-ark innehåller information som behövs för att CDRWIN ska kunna skapa eller bränna CD eller DVD på ett korrekt sätt.

Här är några viktiga detaljer som är specifika för CDRWIN Cue Sheets:

1. **Unikt för CDRWIN**: CDRWINs ".cue"-ark är proprietära format som är specifikt för CDRWIN-programvara. Även om de delar likheter med vanliga ".cue"-filer, är de skräddarsydda för att fungera med CDRWINs funktioner och inställningar.
    






2. **Användarvänligt gränssnitt**: CDRWIN tillhandahåller ett lättanvänt gränssnitt för att skapa och redigera sina ".cue"-ark. Användare kan lägga till eller ändra information om spår, index, luckor och andra parametrar på ett användarvänligt sätt.
    






3. **Kompatibla skivtyper**: CDRWIN Cue Sheets används främst för att skapa olika typer av CD- och DVD-skivor, inklusive dataskivor, ljud-CD-skivor, mixed-mode-skivor och mer. Formatet tillåter användare att ange typ och innehåll på skivan de vill skapa.
    






4. **Control Over Disc Layout**: CDRWIN Cue Sheets ger detaljerad kontroll över skivans layout och struktur, inklusive spårordning, paus/gap-inställningar och andra specifika preferenser som användaren kan ha.
    






5. **ISO- och BIN-stöd**: CDRWIN kan fungera med både ISO- och BIN-skivbildsformat. ".cue"-arket anger vilken bildfil som används för skivan, vilket säkerställer korrekt synkronisering mellan ledtrådar och bild.
    






6. **Bränning och rippning**: Dessa ".cue"-ark är avgörande när du bränner skivor eller ripper spår från skivor med CDRWIN. De hjälper till att säkerställa att slutprodukten matchar avsedd layout och innehåll.
    






7. **Säkerhetskopiering och återställning**: CDRWIN-användare skapar ofta ".cue"-ark när de gör säkerhetskopior av sina CD- eller DVD-skivor. Dessa ark kan senare användas för att återställa skivans innehåll, inklusive spårlayout och timing.

## Hur öppnar man filen CUE?

CDRWIN Cue Sheets är speciellt utformade för CDRWIN-programvara, så de är vanligtvis avsedda att öppnas och användas inom CDRWIN.

Program som öppnar eller refererar till CUE-filer

- CDRWIN
- Smarta projekt IsoBuster
- EZB Systems UltraISO

## Andra CUE-filer

Här är andra filtyper som använder filtillägget **.cue**.

**Disk och media**
- [CUE - Cue Sheet File](/sv/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/sv/disc-and-media/cue-cdrwin/)

## Referenser
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)

