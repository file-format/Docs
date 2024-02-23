{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ZST-fil - Zstandard komprimerat filformat",
  "description":"Lär dig om ZST-filformat och API:er som kan skapa och öppna ZST-filer.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-sv",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Vad är ZST fil?

En ZST-fil är en komprimerad fil som genereras med Zstandard (zstd) komprimeringsalgoritm. Det är en komprimerad fil som skapas med förlustfri komprimering av algoritmen. ZST-filer kan användas för att komprimera olika typer av filer som databaser, filsystem, nätverk och spel. Zstandarden styrs av [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878) som beskriver den övergripande komprimeringsmekanismen, mediatypen och innehållskodningen.

## ZST filformat

ZST-filer lagras i komprimerat filformat på skiva. Kompressionsmekanismen är enligt beskrivningen av RFC 8878 som föråldrar RFC 8478.

## ZST ramar

En ZST-fil består av en eller flera ramar. Varje ram kan vara antingen en Zstandard-ram eller en överhoppningsbar ram. En Zstandard-ram innehåller komprimerad data, medan en överhoppningsbar ram innehåller anpassad användarmetadata.

### Zstandard ram

En Zstandard-ram har följande struktur.

|Fält|Storlek i byte|
---|---|
|Magic_Number |4 byte|
|Frame_Header |2-14 byte|
|Data_Block |n byte|
|[Fler datablock] ||
|[Content_Checksum] |4 byte|

### Överhoppningsbar ram

En överhoppningsbar ram gör det möjligt att infoga användardefinierade metadata i ett flöde av sammanlänkade ramar. Strukturen för en överhoppningsbar ram är som följer.

|Magic_Number |Frame_Size |User_Data|
---|---|---|
|4 byte |4 byte |n byte|

## Referenser ##

* [RFC 8878 Zstandard Compression](https://www.rfc-editor.org/rfc/rfc8878)


