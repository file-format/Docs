{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Microsoft OneNote-filformat",
  "description":"Läs mer om ONETOC2-filformat och API:er som kan skapa och öppna ONETOC2-filer.",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är ONETOC2? ##

De som har arbetat med applikationen [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) kan ha märkt närvaron av .onetoc2-filer i anteckningsbokens mapp. Microsoft OneNote skapar en binär .onetoc2-fil som innehållsförteckning för att hålla ett index över ordningen av olika anteckningsavsnitt i en anteckningsbok. En anteckningsbok är en samling avsnittsfiler som är lagrade i samma katalog. .onetoc2-filen använder en samling egenskaper för att ange inställningar som ordning på sektioner i anteckningsboken och färgen på anteckningsboken.

När du skapar en anteckningsbok i OneNote 2016, sparas den automatiskt i det nya 2010-2016 filformatet. Du behöver det här formatet om du vill att alla funktioner i OneNote 2016, som matematiska ekvationer och länkade anteckningar, ska fungera korrekt.

## ONETOC2 filformat ##

Filformatet .onetoc2 representeras som OneNote Revision Store File Format och är en samling strukturer som specificerar ett revisionsarkiv organiserat i korsreferensobjekt, innehållande objekt med egenskapsuppsättningar och som innehåller en transaktionslogg för att säkerställa filintegritet över asynkron skriver. Fullständiga specifikationer för filformatet .onetoc2 finns tillgängliga [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) och kan hänvisas till för utveckling av applikationer .

### Filstruktur ###

En revisionsarkiv MÅSTE börja med en **Rubrik**-struktur. Resten av filen är uppdelad i block av byte, där storleken och strukturen för varje block specificeras av fältet som refererar till det. Ett block är tillgängligt om det refereras av strukturen **Rubrik**, eller om det refereras av ett fält i ett annat nåbart block. Data utanför strukturen **Rubrik** och eventuella block som kan nås MÅSTE ignoreras.

Alla strukturer är justerade på 1-byte gränser. Alla heltal är signerade om inte annat anges. Alla fält är [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) om inget annat anges.

#### Rubrik ####

Rubriken för .ONE-filen består av bitar som innehåller olika unika ID och fält för representation av filinformation enligt följande:

`guidFileType (16 byte):` En GUID som anger typen av revisionsarkivet. MÅSTE vara ett av värdena från följande tabell.

|Filformat|Värde
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bytes):` En GUID som specificerar identiteten för denna versionsarkivfil. BÖR vara globalt unik.

`guidLegacyFileVersion (16 byte):` MÅSTE vara "{00000000-0000-0000-0000-0000000000000}" och MÅSTE ignoreras.

`guidFileFormat (16 bytes):` En GUID som anger att filen är en versionsarkivfil. MÅSTE vara "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}".

`ffvLastCodeThatWroteToThisFile (4 byte):` Ett heltal utan tecken. MÅSTE vara ett av värdena i följande tabell, beroende på filtyp.

|Filformat|Värde
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldest CodeThatHasWrittenToThisFile (4 byte):` Ett osignerat heltal. MÅSTE vara ett av värdena i följande tabell, beroende på filformatet för denna fil.


|Filformat|Värde
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewest CodeThatHasWrittenToThisFile (4 byte):` Ett heltal utan tecken. MÅSTE vara ett av värdena i följande tabell, beroende på filformatet för denna fil.
:


|Filformat|Värde
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 byte):` Ett heltal utan tecken. MÅSTE vara ett av värdena i följande tabell, beroende på filformatet för denna fil.


|Filformat|Värde
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## Referenser ##

* [[MS-ONESTORE] - OneNote-filformat](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

