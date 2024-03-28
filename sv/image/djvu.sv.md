{
  "date" : "2019-10-11",
  "keywords" :[ "djvu-fil", "djvu-filformat", "vad är en djvu-fil", "fil", "djvu-exempel", "djvu-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DJVU-filformat",
  "description":"Läs mer om DJVU-filformat och API:er som kan skapa och öppna DJVU-filer.",
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en DJVU fil?

DjVu, uttalas som "déjà vu", är ett grafikfilformat avsett för skannade dokument och böcker, särskilt de som innehåller en kombination av text, teckningar, bilder och fotografier. Det utvecklades av AT&T Labs. Den använder flera tekniker som bildlagerseparering av text och bakgrundsbilder, progressiv laddning, aritmetisk kodning och förlustkomprimering för bitonala bilder. Eftersom DJVU-filen kan innehålla komprimerade men ändå högkvalitativa färgbilder, fotografier, text och teckningar och kan sparas på mindre utrymme, används den på webben som e-böcker, manualer, tidningar, gamla dokument, etc.

DjVu kan klassas som ett överlägset alternativ till [PDF](/sv/pdf/). Filtillägg associerade med DjVu är .DJVU eller .DJV. DjVu kan uppnå komprimeringsförhållanden cirka 5–10 bättre än befintliga metoder som [JPEG](/sv/image/jpeg/) och [GIF](/sv/image/gif/) för färgdokument och 3–8 gånger bättre än [TIFF](/image/tiff/) i svartvita dokument. Skannade dokument med 300 DPI med fullfärg upp till 25 MB kan komprimeras ner till 30 till 100 KB. På samma sätt kan svartvita dokument komprimeras upp till 5 till 30 KB. Genomsnittlig HTML-sida kan vara upp till 50 KB, därför kan dessa dokument laddas upp på nätet utan problem.

## Kortfattad bakgrund ##

DjVu-tekniken utvecklades i AT&T-labb av [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner och Paul G från 1996 till 2001. DjVu-filformatet har gått igenom olika versioner, den senaste från 2005.


|Version|Utgivningsdatum|Anteckningar
---|---|---|
|1–19|1996–1999|Detta är utvecklingsversionerna.
|20|April 1999|En sida ändrades till flersidigt format.
|23|Juli 2002|CID-bit
|24|Februari 2003|LTAnno bit
|21|September 1999|Indirekt lagringsformat ersatt. Textsökningslager lades till.
|22|April 2001|Sidorientering, färg JB2
|25|Maj 2003|NAVM-bit. Stöd för DjVu-bokmärken har lagts till.
|26|April 2005|Text/radkommentarer

## DjVu-filformat ##

DjVu-dokument är IFF85-filer. Strukturen tillhandahåller en hierarki av behållare som innehåller information i en DjVu-fil. Dessa behållare kallas också "Chunks". Chunk-typ och Chunk-ID beskriver hur chunken används. Det finns en 4byte header följt av IFF-struktur. De första fyra byten i en DjVu-fil är 0x41 0x54 0x26 0x54. Det här avsnittet diskuterar de olika typerna av DjVu-dokument och de motsvarande bitar som de består av.


|Chunk ID|Användning
---|---|
|FORM|Den sammansatta biten har fyra första databytes av FORM-biten som är sekundär identifierare.
|FORM:DJVM|Ett DjVu-dokument med flera sidor. Kompositbit som innehåller DIRM-biten.
|FORM:DJVU|Ensidig DjVu-dokument. Sammansatt bit som innehåller de bitar som utgör en sida i ett djvu-dokument.
|FORM:DJVI|En “delad” DjVu-fil som ingår via INCL-biten. Delad anteckningar och formordbok.
|FORM:THUM|Kompositbit som innehåller TH44-bitarna som är de inbäddade miniatyrerna.
|DIRM|Sidnamnsinformation för flersidiga dokument.
|NAVM|Bokmärksinformation
|ANTa, ANTz|Annoteringar inklusive både initiala vyinställningar och överlagrade hyperlänkar, textrutor, etc.
|TXTA, TXTz|Unicode Text- och layoutinformation.
|Djbz|Delad formtabell.
|Sjbz|BZZ komprimerade JB2-bitonala data som används för att lagra mask.
|FG44|IW44-data som används för att lagra förgrunden
|BG44|IW44-data som används för att lagra bakgrund
|TH44|IW44-data som används för att lagra inbäddade miniatyrbilder
|WMRM|JB2-data krävs för att ta bort en vattenstämpel
|FGbz|Färg JB2-data. Ger en färg för varje (blit eller form?) i motsvarande Sjbz-bit.
|INFO|Information om a DjVu-sidan
|INCL|ID:t för en inkluderad FORM:DJVI-bit.
|BGjp|JPEG-kodad bakgrund
|FGjp|JPEG-kodad förgrund
|Smmr|G4-kodad mask

### DJVU-komprimering

En bild delas upp i många olika bilder och sedan komprimeras varje bild separat. För att skapa en DjVu-fil delas bilden först upp i tre bilder, en bakgrund, förgrund och en maskbild. Vanligtvis är bakgrunds- och förgrundsbilderna färgbilder med lägre upplösning; men maskbilden är en bild med högre upplösning och vanligtvis lagras texten där. Efter separationen komprimeras förgrunds- och bakgrundsbilderna genom en waveletbaserad komprimeringsalgoritm IW44, medan maskbilden komprimeras med en annan metod som kallas JB2.

JB2-kodningsmetoden eliminerar mycket av redundansen i textbilden genom att identifiera identiska former på sidan, till exempel flera förekomster av ett tecken i ett visst teckensnitt. JB2 kodar först bitmappen för varje unik form genom att dra fördel av redundansen mellan liknande former. Den kodar sedan de platser där varje form visas på sidan. Både JB2 och IW44 förlitar sig på en ny typ av adaptiv binär aritmetisk kodare som kallas ZP-kodaren som klämmer ut eventuell återstående redundans inom några procent av Shannon-gränsen. ZP-kodaren är adaptiv och snabbare än andra ungefärliga binära aritmetiska kodare.

## Referenser ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)
* [DjVu-filformat](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

