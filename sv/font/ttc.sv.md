{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - TrueType Collection File Format",
  "description":"En TrueType Collection-fil (TTC) kombinerar flera teckensnitt till en enda fil. Både Apple och Microsoft använde TTF på Mac- och Windows-operativsystem.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Vad är TTC fil?
TTC förkortas som TrueType Collection är en förlängning av True Type-formatet. En TTC-fil kan kombinera flera teckensnittsfiler till den. Dessa filer är fördelaktiga för att kombinera flera teckensnitt som delar många glyfer gemensamma. Före Windows 2000 användes TTC-filerna i kinesiska, japanska och koreanska versioner av Windows, men senare var stödet tillgängligt för alla regioner.


## Strukturen för teckensnittssamlingsfil
En TTC-fil består av en TTC Header-tabell, Tabellkataloger och flera OpenType-tabeller. TTC-huvudet måste hittas i början av filen. En komplett tabellkatalog för varje typsnitt måste finnas. TableDirectory-formatet bör likna det som fanns i en icke-samlingsfil. Tabellantalet i alla kataloger i en TTC-fil beräknas från början av en TTC-fil.
Tabellerna i en TTC-fil refereras genom tabellkatalogen för sina respektive typsnitt. Några av OpenType-tabellerna måste visas flera gånger, en gång för varje teckensnitt som läggs till i TTC. Medan de andra tabellerna kan delas av flera typsnitt i TTC-filen.

### TTC Header
Två versioner av TTC Header-tabellen är tillgängliga hittills:
- Version 1.0 används för TTC-filer utan digitala signaturer.
- Version 2.0 kan användas för TTC-filer med eller utan digitala signaturer.
Här är TTC Header-tabellerna för båda versionerna:

**TTC Header version 1.0:**

|Typ|Namn|Beskrivning|
---|---|---|
|TAG|ttcTag|Teckensnittssamlings-ID-sträng: 'ttcf' (används för teckensnitt med CFF- eller CFF2-konturer samt TrueType-konturer)|
|uint16|majorVersion|Större version av TTC-huvudet, = 1.|
|uint16|minorVersion|Mindre version av TTC-huvudet, = 0.|
|uint32|numFonts|Antal teckensnitt i TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Array av offsets till TableDirectory för varje typsnitt från början av filen|

**TTC Header version 2.0:**

|Typ|Namn|Beskrivning|
---|---|---|
|TAG|ttcTag |Teckensnittssamlings-ID-sträng: 'ttcf'|
|uint16| majorVersion |Större version av TTC-huvudet, = 2.|
|uint16| minorVersion |Minorversion av TTC-huvudet, = 0.|
|uint32| numFonts |Antal teckensnitt i TTC|
|Offset32| tableDirectoryOffsets[numFonts] |Array av offset till TableDirectory för varje typsnitt från början av filen|
|uint32| dsigTag |Tagg som indikerar att det finns en DSIG-tabell, 0x44534947 ('DSIG') (null om ingen signatur)|
|uint32| dsigLength |Längden (i byte) av DSIG-tabellen (null om ingen signatur)|
|uint32| dsigOffset |Offset (i byte) för DSIG-tabellen från början av TTC-filen (null om ingen signatur)|

## Referenser
* [OpenType Font File](https://learn.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

