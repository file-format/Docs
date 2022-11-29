{
  "date" : "2019-10-11",
  "keywords" :[ "psd-fil", "psd-filformat", "vad är en psd-fil", "fil", "psd-exempel", "psd-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD - Photoshop Image File Format",
  "description":"Läs mer om PSD-filformat och API:er som kan skapa och öppna PSD-filer.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en PSD-fil?

PSD, Photoshop Document, representerar Adobe Photoshops ursprungliga filformat som används för grafisk design och utveckling. PSD-filer kan innehålla bildlager, justeringslager, lagermasker, anteckningar, filinformation, nyckelord och andra Photoshop-specifika element. Photoshop-filer har standardtillägget .PSD och har en maximal höjd och bredd på 30 000 pixlar och en längdgräns på två gigabyte.

## PSD-filformatspecifikationer ##

Data i en PSD-fil lagras i big endian-byteordning. Detta innebär att man byter korta och långa heltal när man läser eller skriver på Windows-plattformen. Photoshop-filformatet är uppdelat i fem huvuddelar. Den har många längdmarkörer som kan användas för att flytta från en sektion till nästa. Längdmarkörerna är vanligtvis utfyllda med byte för att avrunda till närmaste 2 eller 4 byte intervall. De fem huvuddelarna är:

* Filhuvud
* Färglägesdata
* Bildresurser
* Information om lager och mask
* Bilddata

För överensstämmelse bör data skrivas till alla dessa fält i avsnittet, eftersom Photoshop kan försöka läsa hela avsnittet. Det innebär också att nollor skrivs till överhoppade fält när du skriver till en fil. Längdfältet i de längdavgränsade avsnitten ska användas för att bestämma när man ska sluta läsa. I de flesta fall anger längdfältet antalet byte, inte poster, som följer. Följande punkter måste komma ihåg när du läser en fil.

* Värdena i kolumnen "Längd" i alla tabeller är i byte.
* Alla värden som definieras som Unicode-sträng består av:
* Ett fält på 4 byte som representerar antalet tecken i strängen (inte byte).
* Strängen med Unicode-värden, två byte per tecken.

### Filhuvud ###

Filhuvudet innehåller bildens grundläggande egenskaper.

|Längd|Beskrivning
---|---|
|4|Signatur: alltid lika med '8BPS' . Försök inte läsa filen om signaturen inte matchar detta värde.
|2|Version: alltid lika med 1. Försök inte läsa filen om versionen inte matchar detta värde. (~*~*PSB~*~* version är 2.)
|6|Reserverad: måste vara noll.
|2|Antalet kanaler i bilden, inklusive eventuella alfakanaler. Området som stöds är 1 till 56.
|4|Höjden på bilden i pixlar. Området som stöds är 1 till 30 000.
|4|Bildens bredd i pixlar. Området som stöds är 1 till 30 000.
|2|Djup: antalet bitar per kanal. Värden som stöds är 1, 8, 16 och 32.
|2|Färgläget för filen. Värden som stöds är: Bitmap # 0; Gråskala # 1; Indexerad # 2; RGB # 3; CMYK # 4; Flerkanal #7; Duoton # 8; Lab # 9.

### Färgläge Data Sektion ###

Färglägesdatasektionen är strukturerad enligt följande:


|Längd|Beskrivning
---|---|
|4|Längden på följande färgdata
|variabel|Färgdata

Färglägesdata är endast tillgänglig för indexerad färg och duoton som definieras av lägesfältet i avsnittet Filrubrik. För alla andra lägen representeras detta avsnitt av 4-byte nollställda värden. För indexerade färgbilder är längden 768 och färgdatan innehåller färgtabellen för bilden, i icke-interfolierad ordning. För Duotone-bilder innehåller färgdata duotonspecifikationen (vars format inte är dokumenterat). Andra program som läser Photoshop-filer kan behandla en duotonebild som en grå bild och bara bevara innehållet i duotoninformationen när du läser och skriver filen.

### Bildresurser Sektion ###

Den tredje delen av filen innehåller bildresurser. Det börjar med ett längdfält, följt av en serie resursblock.


|Längd|Beskrivning
---|---|
|4|Längd på bildresurssektion. Längden kan vara noll.
|Variabel|Bildresurser (bildresursblock)

Bildresurser används för att lagra icke-pixeldata som är associerade med bilder, till exempel pennverktygsbanor. De kallas resursblock eftersom de innehåller data som lagrades i Macintoshs resurs i tidiga versioner av Photoshop. Den grundläggande strukturen för bildresursblock är som visas nedan:


|Längd|Beskrivning
---|---|
|4|Signatur: '8BIM'
|2|Unik identifierare för resursen. Bildresurs-ID:n innehåller en lista över resurs-ID:n som används av Photoshop.
|Variabel|Namn: Pascal-sträng, vadderad för att göra storleken jämn (ett nollnamn består av två byte med 0)
|4|Faktisk storlek på resursdata som följer
|Variabel|Resursdata, som beskrivs i avsnitten om de enskilda resurstyperna. Den är vadderad för att göra storleken jämn.

Bildresurser använder flera standard-ID-nummer.

### Lager- och maskinformation ###

Den fjärde delen av en Photoshop-fil innehåller information om lager och masker som antal lager, kanaler i lagren, blandningsintervall, nycklar för justeringslager, effektlager och maskparametrar. Om det inte finns några lager eller masker representeras detta avsnitt av ett nollställt 4-bytefält. Särskild uppmärksamhet måste ägnas åt längden på avsnitten när du läser detta avsnitt på grund av de nollställda värdena. Arrangemanget av Layer and Mask-sektionen är som följer:


|Längd|Beskrivning
---|---|
|4|Längden på sektionen med lager och maskinformation. (PSB-längden är 8 byte.)
|Variabel|Lagerinformation
|Variabel|Global lagermaskinformation
|Variabel|Serier av taggade block som innehåller olika typer av data.

#### Lagerinformation ####

Följande tabell visar högnivåorganisationen av lagerinformationen.


|Längd|Beskrivning
---|---|
|4|Längden på lagerinfosektionen, avrundad uppåt till en multipel av 2. (PSB-längden är 8 byte.)
|2|Antal lager. Om det är ett negativt tal är dess absoluta värde antalet lager och den första alfakanalen innehåller transparensdata för det sammanslagna resultatet.
|Variabel|Information om varje lager. Se Lagerposter beskriver strukturen för denna information för varje lager.
|Variabel|Kanalbilddata. Innehåller en eller flera bilddataposter för varje lager. Lagren är i samma ordning som i lagerinformationen

### Bilddata ###

Bildpixeldata finns i avsnittet Bilddata i filen. Arrangemanget av data i bilddatasektionen är i plan ordning, dvs först alla röda data, sedan alla gröna data, etc. Varje plan lagras i skanningslinjeordning, utan padbyte. Bilddatasektionen är arrangerad i ett format som visas i följande tabell.

|Längd|Beskrivning
---|---|
|2|Komprimeringsmetod: *0 = Rå bilddata * 1 = RLE komprimerad bilddatan börjar med byteantalet för alla skanningslinjer (rader * kanaler), med varje räkning lagrad som ett tvåbytevärde. RLE-komprimerade data följer, med varje skanningslinje komprimerad separat. RLE-komprimeringen är samma komprimeringsalgoritm som används av Macintosh ROM-rutinen PackBits och TIFF-standarden. *2 = ZIP utan förutsägelse *3 = ZIP med förutsägelse.
|Variabel|Bilddata. Planar order = RRR GGG BBB, etc.

## Referenser ##

* [PSD-filformatsspecifikationer - av Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Adobe Photoshop-filformat](https://en.wikipedia.org/wiki/Adobe_Photoshop#Filformat)

