{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "fil", "tillägg", "format", "eBook", "Digital bok" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om LRF-filformat och API:er som kan skapa och öppna LRF-filer.",
  "title" :"LRF File Format - En Sony Portable Reader File",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Vad är LRF fil?

En fil med filtillägget .lrf är en bredbands-eBook-fil (BBeB) som innehåller data för en Sony BBeB, inklusive text, bilder och sidnumreringsdata. Filen sparas i ett komprimerat binärt format som innehåller en rubrik, ett specificerat antal objekt och ett objektindex. LRF- och LRX-filer omsluter de två tillgängliga BBeB-bokformaten. LRF-filerna är inte krypterade och kan kompileras från [LRX](/sv/ebook/lrf/)-filer. LRF-filerna kan konverteras från flera andra filtyper inklusive PDF och HTML. Om din dator inte kan öppna LRF-filen har du förmodligen inte programvaran installerad för att öppna eller redigera LRF-filerna. Program som kan öppna LRF-filer är Caliber, BookDesigner, Makelrf och Canon Book Creator för Windows, Caliber för Linux, Caliber och Sony Reader för Macintosh.

## Kortfattad bakgrund

LRF-filtypen associeras först och främst med Line Rider av [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). Line Rider är en fysikleksak på internet och uppfanns i september 2006 av en slovensk universitetsstudent, Boštjan Čadež. Sonys eBook eReaders (som Sony PRS-500-läsare och Sony Librie) använder filtillägget LRF för sina dokument och texter. Denna proprietära filtyp är nu föråldrad, liksom de relaterade LRS- och LRX-filerna. Dessa tre filtyper utgjorde Bredbands-e-boken (BBeB) som avbröts 2010 när Sony började sälja sina e-böcker i EPUB-formatet.

## LRF filformat

Detaljerade specifikationer för LRF-filformat finns på [webarkiv](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). En LRF-fil består av:
* en rubrik
* ett antal föremål
* ett objektindex.

Alla dessa värden är i Intel (LSB första) ordning.

### LRF-huvud

|Offset (hex) |Storlek(byte) |Namn/betydelse| Exempelvärde|
---|---|---|---|
|0 |8| LRF Signatur| 4C 00 52 00 46 00 00 00 = "LRF" i Unicode|
|8 |2| version?| 999 i de flesta filer|
|A |2| "Psuedo-kryptering" |nyckelbyte 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| NumberOfObjects |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| okänd| 0|
|24 |1| Flaggor| (16 - bakifrån till fram, 1 = fram till bak) 16|
|25 |1| okänd |(utfyllnad?) 0|
|26 |2| okänd| 1600|
|28 |2| okänd| (stoppning?) 0|
|2A |2| Höjd?| 600|
|2C |2| Bredd?| 800|
|2E |1| okänd| 24|
|2F |1| okänd |(utfyllnad?) 0|
|30 |0x14| okänd| nollor|
|44 |4| Objekt-ID för endast PlaneStream (0x1E) objekt| 0x0042|
|48 |4| okänd |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Referenser

* [LRF-filformat](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - av Wikipedia](https://en.wikipedia.org/wiki/BBeB)

