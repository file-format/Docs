{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "fájl", "kiterjesztés", "formátum", "mi az m4a fájlformátum", "zene", "m4a fájlformátum", "M4A vs MP3", "m4a fájlformátum specifikációja"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ismerje meg az M4A fájlformátumot és az API-kat, amelyek M4A fájlokat hozhatnak létre, konvertálhatnak és megnyithatnak.",
  "title" :"M4A - MPEG-4 hangfájl",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Mi az M4A fájl?

Az **M4A fájlformátum** egy AAC (Advanced Audio Coding) használatával létrehozott hangfájl, amely veszteséges tömörítésként ismert. Az M4A szó rövidítése MPEG 4 Audio. Ezek a hangfájlok általában .m4a kiterjesztéssel rendelkeznek. Ez különösen igaz a nem védett tartalomra. Különféle hangtartalmakat tárolhat, például hangoskönyveket, dalokat és podcastokat. Az M4A rendszerint fejlettebb formátum, mint az MP3, amelyet általában nem csak hanghoz terveztek. Ez csak egy audio réteg az MPEG 1 vagy 2 videofájlokban.

Az M4A formátumot a FairPlay Digital Rights Management titkosítja, mivel az iTunes Store-on keresztül értékesítették az .m4p kiterjesztést. Az Apple iPhone-ok MPEG-4 hangot használnak csengőhangjukhoz, de ezek az audiofájlok az .m4r kiterjesztést használják.


## M4A vs MP3

Mind az M4A, mind az [MP3](https://docs.fileformat.com/audio/mp3/) csak hangfájlformátum.

**M4A**: Minőségben és méretben jobb, mint az MP3, azonos bitsebességgel kódolva. Az .m4a fájlkiterjesztés annyira elterjedt, mert az Apple az iTunes Music Store-ban való használatra használta őket. Az M4A egy MPEG-4 technológiával tömörített hangfájl; egy algoritmus a veszteséges tömörítéshez. Alapvetően az „MPEG-4 Audio Layer”-hez kapcsolódik, az .m4a kiterjesztésű fájlok az MPEG-4 filmek hangrétegét jelentik. Célja, hogy megelőzze az MP3-at, és a hangtömörítés új szabványává váljon. Sok szempontból nagyon közel áll az MP3-hoz, de azért vezették be, hogy jobb minőségű legyen azonos vagy még kisebb fájlméretben. Az M4A formátumot először az Apple vezette be. A formátumtípus Apple veszteségmentes kódolóként (ALE) is megvalósul.

Ezért az M4A jelenleg nem érheti el az MP3 mainstream sikerét, mivel az audio formátum még nem játszható le. Valahogy csak a MacOS, az iPod és más Apple termékekre korlátozódik.

**Mp3**: A leghíresebb digitális hangformátum. Ez volt az egyik első tömörítési formátum a színtéren, és nagyon népszerűvé vált a zene szerelmesei körében. A mainstream siker olyan gyors, hogy a fájltípus univerzálisan és szinte bármivel lejátszható, legyen az hardver vagy szoftver. Általánosságban elmondható, hogy az M4A jobb hangminőséget fog produkálni, de sokan azzal érvelnek, hogy akár igaz, akár nem, a hangkülönbség nem megkülönböztethető, és időpocsékolás lenne megpróbálni MP3 fájlokat M4A fájlokká konvertálni. Végül az átalakítás csak az eredeti hangminőség elvesztését okozza.

## M4A fájlformátum specifikáció

Az M4A fájlok egymást követő darabokból állnak. Minden csonk 8 bájtos fejléccel rendelkezik, és a következőképpen van felosztva:
- 4 bájtos darabméret (big-endian, a magas bájt először)
- 4 bájtos csonktípus - az előre meghatározott aláírások egyike: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt" ", "ssrc", "PICT".

Az első darab "ftype" típusú lesz, és egy altípusa van a 8-as eltolásnál. Az altípus által meghatározott M4A, amelynek "M4A_"-nak kell lennie, az M4B altípushoz "M4B_", az M4P altípushoz pedig legyen "M4P_".

A darabok iterálása, amíg ismeretlen típusú darabot nem észlel, M4A (MPEG-4 Audio) fájlt készít.

## Hivatkozások ##

* [MPEG-4 14. rész – a Wikipedia által](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) formátum és helyreállítás példa](https://www.file-recovery.com/m4a-signature-format.htm)

