{
  "date" : "2020-08-20",
  "keywords" :[ "eot fil", "eot filformat", "vad är en eot fil", "fil", "eot exempel", "eot filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - TrueType Font File Format",
  "description":"Läs mer om EOT-filformat och API:er för att skapa och öppna EOT-filer.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Vad är en EOT fil?

En fil med filtillägget .eot är ett OpenType-teckensnitt som är inbäddat i ett dokument. Dessa används mest i webbfiler såsom en webbsida. Den skapades av Microsoft och stöds av Microsoft-produkter inklusive PowerPoint-presentationsfilen [.pps](/sv/presentation/pps). Filen är inte av primär användning och är ett slags medföljande dokument med huvuddokumentet eller webbsidan. I likhet med OTF-teckensnitt stöder EOT både Postscript- och TrueType-konturer för glyferna. EOT-filer är mindre i storlek av den anledningen att de komprimeras med LZ-komprimering. EOT använder ett Microsoft-verktyg för att skapa ett typsnitt från befintliga TTF/OTF-teckensnitt.

## Kortfattad bakgrund

EOT-teckensnittet skickades till W3C 2007 som en del av CSS3 men på grund av dess krav på att vara permanent installerat på fjärrsystem blev det anledningen till att det avvisades. Den skickades in igen i mars 2008, men W3C valde till slut [Web Font Format](/sv/font/woff/) (WOFF) som då standardiserades.

## EOT filformat

Detaljer för EOT-filformat finns på [W3-inlämningssidan](https://www.w3.org/Submission/EOT/#FileFormat) och utvecklar strukturen som används av detta teckensnittsformat. EOT består av en enda EMBEDDEDFONT-struktur som ger tillräckligt med grundläggande information om teckensnittsnamnet och tecken som stöds. Packningen av denna information gör att användaragenter kan undvika att packa upp, dekomprimera eller installera teckensnittet om det redan finns på maskinen.

### EMBEDDED FONT Struktur
EMBEDDEDFONT-strukturen har genomgått tre revisioner, med tillägg av ytterligare data i slutet av strukturen med varje revision. Den senaste revideringen av EMBEDDEDFONT-strukturen är som avbildas nedan.

|Datatyp|Inmatningsnamn|Beskrivning|
---|---|---|
|unsigned long|EOTSize|Total strukturlängd i byte (inklusive sträng- och teckensnittsdata)|
|unsigned long|FontDataSize|Längden på OpenType-teckensnittet (FontData) i byte|
|unsigned long|Version|Versionsnummer för detta format - 0x00020002|
|unsigned long|Flaggor|Bearbetar flaggor|
|byte[10]|FontPANOSE|PANOSE-värdet för detta teckensnitt - Se http://www.microsoft.com/typography/otspec/os2.htm#pan|
|byte|Charset|I Windows härleds detta från TEXTMETRIC.tmCharSet. Detta värde anger teckenuppsättningen för teckensnittet. DEFAULT_CHARSET (0x01) indikerar ingen preferens. - Se https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|Om biten för ITALIC är inställd i OS/2.fsSelection blir värdet 0x01 - Se http://www.microsoft.com/typography/otspec/os2.htm#fss|
|unsigned long|Weight|Viktvärdet för detta teckensnitt - Se http://www.microsoft.com/typography/otspec/os2.htm#wtc|
|unsigned short|fsType|Typ flaggor som ger information om inbäddningsbehörigheter - Se http://www.microsoft.com/typography/otspec/os2.htm#fst|
|osignerad kort|MagicNumber|Magiskt nummer för EOT-fil - 0x504C. Används för att söka efter datakorruption.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bitar 0-31) - Se http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bitar 32-63) - Se http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bitar 64-95) - Se http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bitar 96-127) - Se http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bitar 0-31) - Se http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bitar 32-63) - Se http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - Se http://www.microsoft.com/typography/otspec/head.htm|
|unsigned long|Reserved1|Reserved - måste vara 0|
|unsigned long|Reserved2|Reserved - måste vara 0|
|unsigned long|Reserved3|Reserved - måste vara 0|
|unsigned long|Reserved4|Reserved - måste vara 0|
|unsigned short|Padding1|Utfyllning för att bibehålla lång inriktning. Utfyllnadsvärdet måste alltid vara inställt på 0x0000.|
|unsigned short|FamilyNameSize|Antal byte som används av FamilyName-matrisen|
|byte|FamilyName[FamilyNameSize]|Array av UTF-16-tecken längden på FamilyNameSize-byte. Detta är den engelska teckensnittssträngen som finns i teckensnittets namntabell (namn-ID = 1) - Se http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding2|Utfyllningsvärde måste alltid sättas till 0x0000.|
|unsigned short|StyleNameSize|Antal byte som används av StyleName|
|byte|StyleName[StyleNameSize]|Array av UTF-16-tecken längden på StyleNameSize-byte. Detta är den engelska teckensnittssträngen som finns i namntabellen för teckensnittet (namn-ID = 2) - Se http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding3|Utfyllningsvärde måste alltid sättas till 0x0000.|
|unsigned short|VersionNameSize|Antal byte som används av VersionName|
|bytes|Versionsnamn[VersionNameSize]|Array av UTF-16-tecken längden på VersionNameSize-byte. Detta är den engelska versionssträngen som finns i namntabellen för teckensnittet (namn-ID = 5) - Se http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding4|Utfyllningsvärdet måste alltid sättas till 0x0000.|
|unsigned short|FullNameSize|Antal byte som används av FullName|
|byte|Fullnamn[FullnamnStorlek]|Array av UTF-16-tecken längden på FullNameSize-byte. Detta är den engelska fullständiga namnsträngen som finns i namntabellen för teckensnittet (namn-ID = 4) - Se http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding5|Utfyllningsvärde måste alltid sättas till 0x0000.|
|unsigned short|RootStringSize|Antal byte som används av RootString-matrisen|
|byte|RootString[RootStringSize]|Array av UTF-16-tecken längden på RootStringSize-bytes.|
|unsigned long|RootStringCheckSum|RootString CheckSum-värde. Se algoritm för att bearbeta RootStringChecksum nedan.|
|unsigned long|EUDCCodePage|Codepage-värde behövs för stöd för EUDC-teckensnitt.|
|unsigned short|Padding6|Utfyllningsvärde måste alltid sättas till 0x0000.|
|unsigned short|SignatureSize|Antal byte som används av signaturmatrisen. För närvarande reserverad och bör ställas in på 0x0000.|
|byte|Signatur[SignatureSize]|För närvarande reserverad. Om SignatureSize är 0x0000 finns det ingen längd på denna array.|
|unsigned long|EUDCFlags|Bearbetar flaggor för EUDC-teckensnittet. Typiska värden kan vara TTEMBED_XORENCRYPTDATA och TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Antal byte som används av signaturarrayen.|
|byte|EUDCFontData[EUDCFontSize]|Antal byte som används för EUDC-teckensnittsdata. Om EUDCFontSize är 0x00000000 finns det ingen längd på denna array.|
|byte|FontData[FontDataSize]|Teckensnittsdata för denna EOT-fil. Data kan komprimeras eller XOR-krypteras såsom indikeras av bearbetningsflaggorna.|

## Referenser

* [EOT-filformat](https://www.w3.org/Submission/EOT/)
* [Embedded OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Teckensnittsinbäddning](https://en.wikipedia.org/wiki/Font_embedding)

