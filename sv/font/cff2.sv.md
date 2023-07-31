{
  "date" : "2020-08-20",
  "keywords" :[ "cff2 fil", "cff2 filformat", "vad är en cff2 fil", "fil", "cff2 exempel", "cff2 filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF2 - Compact Font File Format version 2",
  "description":"Läs mer om CFF2-filformat och API:er för att skapa och öppna CFF2-filer.",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Vad är en CFF2 fil?

CFF2-filformatet är version 2.0 av CFF-filformatet och möjliggör effektiv lagring av glyfkonturer och metadata som liknar CFF-filformatet. CFF2 skiljer sig från CFF genom att den är avsedd att användas i ett OpenType-teckensnitt som en 'sfnt'-tabell med taggen CFF2. Det kan inte användas som ett fristående program och beror på data i andra OpenType-tabeller.

## CFF2 filformat

[CFF2 filformatspecifikationer](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2) innehåller information om intern datalayout, datatyper, tabeller och annan intern information om filformatet. Det kan hänvisas till utvecklarens referens. Några av detaljerna om dessa är följande.

### Datalayout

Binära data i CFF2-filformatet är logiskt organiserade som ett antal separata datastrukturer. Layouten inom binära data är som visas i följande tabell.

|Entry |Kommentarer|
---|---|
|Rubrik |Fast plats|
|Topp DICT| Fast plats|
|Global Subr INDEX| Fast plats|
|Variation |Butik|
|FDSälj |Visas endast om det finns mer än en Font DICT i Font DICT INDEX.|
|Teckensnitt DICT INDEX ||
|Array of Font DICT| Ingår i Font DICT INDEX.|
|Privat DICT| En per typsnitt DICT.|

Endast de tre första strukturerna är baserade på fasta platser. Återstående nås via offset och deras beställning kan ändras.

### Datatyper

Filformatet CFF2 använder följande datatyper.

|Namn |Omfång |Beskrivning|
---|---|---|
|uint8 |0 till 255 |8-bitars osignerat nummer|
|uint16 |0 till 65535| 16-bitars osignerat nummer|
|uint32 |0 till 4294967295| 32-bitars osignerat nummer|
|Offset |varierar| 1, 2, 3 eller 4 byte förskjutningar (anges av OffSize-fältet i en indextabell)|
|OffSize |1 till 4| 1-byte osignerat nummer anger storleken på ett eller flera förskjutningsfält|

Den lagrar alla multi-byte numeriska data och offsetfält i big-endian byteordning. CFF2-formatet är fritt från utfyllnadsbytes eftersom det inte respekterar några inriktningsbegränsningar.

### DICT-data

CFF2-filer innehåller teckensnittslexikondata som nyckel-värdepar i ett kompakt tokeniserat format. Ordboksnycklar är kodade som 1 eller 2 byte-operatorer och ordboksvärden kodas som numeriska operander med variabel storlek. Det finns tre strukturer som använder DICT-dataformatet: `Top DICT`, `Font DICT` och `Private DICT`. Ett antal heltalsoperandtyper av varierande storlek definieras och kodas som visas i följande tabell (första byten av operanden är b0, den andra är b1 och så vidare).

|Storlek |b0-intervall |Värdeintervall |Värdeberäkning|
---|---|---|---|
|1 |32 till 246| -107 till +107 |b0 - 139|
|2 |247 till 250| +108 till +1131 |(b0 - 247) * 256 + b1 + 108|
|2 |251 till 254| -1131 till -108| -(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 till +32767| b1 << 8 | b2|
|5 |29| -(2^31) till +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Rubrik

Den binära datan börjar med en rubrik med formatet som visas i tabellen nedan.

|Typ |Namn |Beskrivning|
---|---|---|
|uint8| majorVersion| Formatera större version. Ställ in på 2.|
|uint8| minorVersion| Format mindre version. Ställ in på noll.|
|uint8| headerSize| Rubrikstorlek (byte).|
|uint16| topDictLength| Längd på Top DICT-struktur i byte.|

## Referenser

* [CFF2-filformat](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

