{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ZST-fil - Zstandard komprimeret filformat",
  "description":"Lær om ZST filformat og API'er, der kan oprette og åbne ZST filer.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-da",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Hvad er en ZST fil?

En ZST-fil er en komprimeret fil, der er genereret med Zstandard (zstd) komprimeringsalgoritmen. Det er en komprimeret fil, der er oprettet med tabsfri komprimering af algoritmen. ZST-filer kan bruges til at komprimere forskellige typer filer, såsom databaser, filsystemer, netværk og spil. Z-standarden er styret af [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878), der beskriver den overordnede komprimeringsmekanisme, medietype og indholdskodning.

## ZST filformat

ZST-filer gemmes i komprimeret filformat på disk. Kompressionsmekanismen er som beskrevet af RFC 8878, der forælder RFC 8478.

## ZST rammer

En ZST-fil består af en eller flere rammer. Hver ramme kan enten være en Zstandard-ramme eller en ramme, der kan springes over. En Zstandard-ramme indeholder komprimerede data, mens en ramme, der kan springes over, indeholder brugerdefinerede metadata.

### Zstandard ramme

En Zstandard ramme har følgende struktur.

|Felt|Størrelse i bytes|
---|---|
|Magic_Number |4 bytes|
|Frame_Header |2-14 bytes|
|Data_Blok |n bytes|
|[Flere datablokke] ||
|[Content_Checksum] |4 bytes|

### Ramme, der kan springes over

En ramme, der kan springes over, gør det muligt at indsætte brugerdefinerede metadata i et flow af sammenkædede rammer. Strukturen af en ramme, der kan springes over, er som følger.

|Magic_Number |Frame_Size |User_Data|
---|---|---|
|4 bytes |4 bytes |n bytes|

## Referencer ##

* [RFC 8878 Zstandard Compression](https://www.rfc-editor.org/rfc/rfc8878)


