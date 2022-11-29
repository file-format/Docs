{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR2-filformat - Canon Raw 2-bildfil",
  "description":"Läs mer om CR2-filformat och API:er som kan skapa och öppna CR2-filer.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Vad är CR2 fil?

En CR2-fil (Camera RAW 2) är en RAW-bildfil som skapats av Canons digitalkameror. Den lagrar den ursprungliga obearbetade förlustfria bilddata som tagits av kameran. CR2-filformatet har utvecklats av Canon för sina digitalkameror och kan spela in bilder av hög kvalitet på upp till 14 bitars RGB. Detta ger bilder av hög kvalitet med tillräckligt med utrymme för efterbehandling. CR2-bildformat har använts av Canon i deras 350D, 20D och 1D kameramodeller. CR2-filer är RAW-filer och innehåller ytterligare metadatainformation som kamerainformation, objektivinformation, bracketinginformation, vitbalans och andra inställningar.

## CR2 filformat

CR2-filer lagras på kamerans minneskort som binära filer i Canons eget filformat. Filformatet CR2 ersatte det ursprungligen använda CRW-filformatet och ersattes senare av filformatet Canon RAW 3. CR2-filformatet är baserat på [TIFF](/sv/image/tiff/)-specifikationerna som har 4 bildfilskataloger (IFD).

|Offset |Innehåll |Kommentar|
---|---|---|
|0x0000 |Rubrik |innehåller byteordningen, versionen och offseten till RAW-bilden|
|beräknad |IFD#0 |den här delen innehåller Exif-sektionen, som innehåller Makernotes-sektionen.
Information om bild#0|
|beräknad |bild#0 |liten version av bilden (en fjärdedel av originalets storlek), komprimerad i Jpeg|
|beräknad |IFD#1 |Information om bild#1.|
|beräknad |bild#1 |liten version av bilden, komprimerad i Jpeg|
|beräknad |IFD#2 |Information om bild#2.|
|beräknad |bild#2 |liten version av bilden, inte komprimerad|
|i header| IFD#3| Information om bild#3, fulldimensionen RAW-bild|
|beräknad |bild#3 |RAW-bilddata, förlustfri komprimerad i Jpeg (inte RGB-data!)|

## Fördelen med CR2-filformat

Att lagra bilder i RAW-format möjliggör en hel del efterbearbetning av fotografiet, såsom justering av vitbalansen. Detta är mycket svårare och med en stor kvalitetsförlust med andra bildfilformat som [JPEG](/sv/image/jpeg/).

## Är CR2 bättre än JPEG?

CR2-filer är råfiler utan förlust av data och därmed ingen kvalitetsförlust. JPEG å andra sidan är ett bildfilformat med förlust eftersom det förlorar en del data för att minska filen. Således är CR2-filerna av hög kvalitet och mer lämpade för retuschering och förbättringar.

## Referenser

* [CR2-filformat](http://lclevy.free.fr/cr2/)

