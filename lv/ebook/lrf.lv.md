{
  "date": "2019-12-12",
  "keywords": [
"LRF",
"failu",
"pagarinājumu",
"formātā",
"e-grāmata",
"Digitālā grāmata"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par LRF failu formātu un API, kas var izveidot un atvērt LRF failus.",
  "title": "LRF faila formāts — Sony portatīvā lasītāja fails",
  "linktitle": "LRF",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-lr-lvf"
}
},
  "lastmod": "2019-12-12"
}

## Kas ir LRF fails?

Fails ar paplašinājumu .lrf ir platjoslas e-grāmatas (BBeB) fails, kas satur datus par Sony BBeB, tostarp tekstu, attēlus un lappušu datus. Fails tiek saglabāts saspiestā binārā formātā, kas satur galveni, noteiktu objektu skaitu un objekta indeksu. LRF un LRX faili ietver divus pieejamos BBeB grāmatu formātus. LRF faili nav šifrēti, un tos var apkopot no [LRX](/ebook/lrf/) failiem. LRF failus var konvertēt no vairākiem citiem failu tipiem, tostarp PDF un HTML. Ja jūsu dators nevar atvērt LRF failu, iespējams, jums nav instalēta programmatūra, lai atvērtu vai rediģētu LRF failus. Programmas, ar kurām var atvērt LRF failus, ir Caliber, BookDesigner, Makelrf un Canon Book Creator operētājsistēmai Windows, Caliber operētājsistēmai Linux, Caliber un Sony Reader operētājsistēmai Macintosh.

## Īsa vēsture

LRF faila tips vispirms ir saistīts ar Line Rider, ko izveidoja [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). Line Rider ir interneta fizikas rotaļlieta, un to 2006. gada septembrī izgudroja slovēņu universitātes students Boštjans Čadežs. Sony zīmola e-grāmatu lasītāji (piemēram, Sony PRS-500 lasītāji un Sony Librie) saviem dokumentiem un tekstiem izmanto LRF faila paplašinājumu. Šis patentētais faila veids tagad ir novecojis, kā arī saistītie LRS un LRX faili. Šie trīs failu tipi veidoja platjoslas e-grāmatu (BBeB), kas tika pārtraukta 2010. gadā, kad Sony sāka pārdot savas e-grāmatas EPUB formātā.

## LRF faila formāts

Detalizētas LRF faila formāta specifikācijas ir pieejamas vietnē [web archive](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). LRF fails sastāv no:
* galvene

* vairāki objekti

* objekta indekss.


Visas šīs vērtības ir norādītas Intel (LSB vispirms) secībā.

### LRF galvene

|Nobīde (hex) |Izmērs (baiti) |Nosaukums/nozīme| Piemēra vērtība|
---|---|---|---|
|0 |8| LRF paraksts| 4C 00 52 00 46 00 00 00 = LRF Unicode|
|8 |2| versija?| 999 lielākajā daļā failu|
|A |2| Psuedo-Encryption |atslēgas baits 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| Objektu skaits |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| nezināms| 0|
|24 |1| Karogi| (16 - no aizmugures uz priekšu, 1 = no priekšpuses uz aizmuguri) 16|
|25 |1| nezināms |(polsterējums?) 0|
|26 |2| nezināms| 1600|
|28 |2| nezināms| (polsterējums?) 0|
|2A |2| Augstums?| 600|
|2C |2| Platums?| 800|
|2E |1| nezināms| 24|
|2F |1| nezināms |(polsterējums?) 0|
|30 |0x14| nezināms| nulles|
|44 |4| Objekta ID tikai PlaneStream (0x1E) objektam| 0x0042|
|48 |4| nezināms |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Atsauces

* [LRF faila formāts](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)

* [BBeB — Wikipedia](https://en.wikipedia.org/wiki/BBeB)


