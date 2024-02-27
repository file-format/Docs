{
  "date": "2020-08-20",
  "keywords": [
"eot fil",
"eot filformat",
"hvad er en eot fil",
"fil",
"eot eksempel",
"eot filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EOT - TrueType Font File Format",
  "description": "Lær om EOT-filformat og API'er til at oprette og åbne EOT-filer.",
  "linktitle": "EOT",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-eo-dat"
}
},
  "lastmod": "2020-10-21"
}

## Hvad er en EOT fil?

En fil med filtypenavnet .eot er en OpenType-skrifttype, der er indlejret i et dokument. Disse bruges mest i webfiler såsom en webside. Den blev oprettet af Microsoft og understøttes af Microsoft-produkter, herunder PowerPoint-præsentationsfilen [.pps](/presentation/pps/). Filen er ikke til primær brug og er en slags ledsagedokument med hoveddokumentet eller websiden. I lighed med OTF-skrifttyper understøtter EOT både Postscript- og TrueType-konturer for glyfferne. EOT-filer er mindre i størrelse af den grund, at de er komprimeret ved hjælp af LZ-komprimering. EOT bruger et Microsoft-værktøj til at oprette en skrifttype ud fra eksisterende TTF/OTF-skrifttyper.

## Kort historie

EOT-skrifttypen blev indsendt til W3C i 2007 som en del af CSS3, men på grund af dens krav om at blive permanent installeret på fjernsystemet blev det årsagen til dens afvisning. Det blev genindsendt i marts 2008, men W3C valgte i sidste ende [Web Font Format](/font/woff/) (WOFF), som blev standardiseret dengang.

## EOT filformat

EOT-filformatdetaljer kan findes på [W3 submission page](https://www.w3.org/Submission/EOT/#FileFormat) og uddyber den struktur, der bruges af dette skrifttypeformat. EOT består af en enkelt EMBEDDEDFONT-struktur, der giver tilstrækkelig grundlæggende information om skrifttypenavnet og understøttede tegn. Pakningen af disse oplysninger gør det muligt for brugeragenter at undgå at pakke ud, dekomprimere eller installere skrifttypen, hvis den allerede findes på maskinen.

### EMBEDDEDFONT-struktur
EMBEDDEDFONT-strukturen har gennemgået tre revisioner, med tilføjelse af yderligere data i slutningen af strukturen med hver revision. Den sidste revision af EMBEDDEDFONT-strukturen er som vist nedenfor.

|Datatype|Indtastningsnavn|Beskrivelse|
---|---|---|
|unsigned long|EOTSize|Samlet strukturlængde i bytes (inklusive streng- og skrifttypedata)|
|unsigned long|FontDataSize|Længde af OpenType-skrifttypen (FontData) i bytes|
|unsigned long|Version|Versionsnummer for dette format - 0x00020002|
|unsigned long|Flag|Behandler flag|
|byte[10]|FontPANOSE|PANOSE-værdien for denne skrifttype - Se https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|byte|Charset|I Windows er dette afledt fra TEXTMETRIC.tmCharSet. Denne værdi angiver skrifttypens tegnsæt. DEFAULT_CHARSET (0x01) angiver ingen præference. - Se https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|Hvis bit for ITALIC er indstillet i OS/2.fsSelection, vil værdien være 0x01 - Se https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss|
|unsigned long|Vægt|Vægtværdien for denne skrifttype - Se https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc|
|unsigned short|fsType|Typeflag, der giver oplysninger om indlejringstilladelser - Se https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst|
|unsigned short|MagicNumber|Magisk nummer til EOT-fil - 0x504C. Bruges til at kontrollere for datakorruption.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bits 0-31) - Se https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bits 32-63) - Se https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bits 64-95) - Se https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bits 96-127) - Se https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bits 0-31) - Se https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bits 32-63) - Se https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - Se https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|unsigned long|Reserved1|Reserved - skal være 0|
|unsigned long|Reserved2|Reserved - skal være 0|
|unsigned long|Reserved3|Reserved - skal være 0|
|unsigned long|Reserved4|Reserved - skal være 0|
|unsigned short|Padding1|Padding for at opretholde lang justering. Udfyldningsværdi skal altid sættes til 0x0000.|
|unsigned short|FamilyNameSize|Antal bytes brugt af FamilyName-arrayet|
|byte|FamilyName[FamilyNameSize]|Array af UTF-16-tegn længden af FamilyNameSize-bytes. Dette er den engelsksprogede Font Family-streng, der findes i skrifttypens navnetabell (navn-id = 1) - Se https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|Padding-værdi skal altid sættes til 0x0000.|
|unsigned short|StyleNameSize|Antal bytes brugt af StyleName|
|byte|StyleName[StyleNameSize]|Array af UTF-16-tegn længden af StyleNameSize-bytes. Dette er den engelsksprogede Font Subfamily-streng, der findes i skrifttypens navnetabell (navn-ID = 2) - Se https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|Padding-værdi skal altid sættes til 0x0000.|
|unsigned short|VersionNameSize|Antal bytes brugt af VersionName|
|bytes|Versionsnavn[VersionNameSize]|Array af UTF-16-tegn længden af VersionNameSize-bytes. Dette er den engelsksprogede versionsstreng, der findes i navnetabellen for skrifttypen (navn-ID = 5) - Se https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|Padding-værdi skal altid sættes til 0x0000.|
|unsigned short|FullNameSize|Antal bytes brugt af FullName|
|byte|Fuldnavn[FuldnavnStørrelse]|Array af UTF-16-tegn længden af FullNameSize-bytes. Dette er den engelsksprogede fulde navnestreng, der findes i navnetabellen for skrifttypen (navn ID = 4) - Se https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|Padding-værdi skal altid sættes til 0x0000.|
|unsigned short|RootStringSize|Antal bytes brugt af RootString-arrayet|
|byte|RootString[RootStringSize]|Array af UTF-16-tegn længden af RootStringSize-bytes.|
|unsigned long|RootStringCheckSum|RootString CheckSum værdi. Se algoritmen til at behandle RootStringChecksum nedenfor.|
|unsigned long|EUDCCodePage|Tidstabelværdi er nødvendig for EUDC-skrifttypeunderstøttelse.|
|unsigned short|Padding6|Padding-værdi skal altid sættes til 0x0000.|
|unsigned short|SignatureSize|Antal bytes brugt af signaturarrayet. I øjeblikket reserveret og bør indstilles til 0x0000.|
|byte|Signatur[SignatureSize]|I øjeblikket reserveret. Hvis SignatureSize er 0x0000, er der ingen længde på dette array.|
|unsigned long|EUDCFlags|Behandler flag for EUDC-skrifttypen. Typiske værdier kan være TTEMBED_XORENCRYPTDATA og TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Antal bytes brugt af signaturarrayet.|
|byte|EUDCFontData[EUDCFontSize]|Antal bytes brugt til EUDC-skrifttypedata. Hvis EUDCFontSize er 0x00000000, er der ingen længde på denne matrix.|
|byte|FontData[FontDataSize]|Skriftdataene for denne EOT-fil. Dataene kan være komprimeret eller XOR-krypteret som angivet af behandlingsflag.|

## Referencer

 * [EOT-filformat](https://www.w3.org/Submission/EOT/)
 * [Embedded OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
 * [Skriftindlejring](https://en.wikipedia.org/wiki/Font_embedding)

