{
  "date" : "2021-06-09",
  "keywords" :[ "m4b", "mp3", "fájl", "kiterjesztés", "formátum", "mi az m4b fájlformátum", "zene", "m4b fájlformátum", "M4b vs MP3", "m4b fájlformátum specifikációja"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ismerje meg az M4B fájlformátumot és az API-kat, amelyek M4B fájlokat hozhatnak létre, konvertálhatnak és megnyithatnak.",
  "title" :"M4B - MPEG-4 hangoskönyv fájlformátum",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Mi az M4B fájl?

Az .m4b kiterjesztésű fájl egy hangoskönyv, amelyet általában az Apple Books és az iTunes használ. Az ebben a formátumban használt hangot MPEG-4 formátumban tárolják, és AAC kódolással tömörítik. Az M4B fájl nagyon hasonlít az M4A-hoz, de támogatja a hangoskönyvekkel kapcsolatos funkciókat, például a könyvjelzőket és a fejezettöréseket. Az M4B fájlok DRM-kompatibilis és DRM-mentes verziókban is elérhetők. A DRM-titkosított hangoskönyvek általában fizetős hangoskönyvek az iTunes Store-ból. Míg a DRM-mentesek könnyen megtalálhatók az interneten.

## M4B fájlformátum

A metaadatokat, képeket, könyvjelzőket és hiperhivatkozásokat tartalmazó hangoskönyv-fájlok .m4a kiterjesztéssel menthetők, de általában .m4b kiterjesztést használunk a mentés során, csak annak megadására, hogy a fájl hangoskönyv fájlformátumú-e. A Fairplay DRM-et (Digital Rights Management) használja az app az M4B-fájlok védelmére. Így az iTunes-ból letöltött fájlok csak engedélyezett eszközökön vagy számítógépeken játszhatók le.


## M4B vs M4A

Mind az M4B, mind az [MP3](/audio/mp3/) csak hangfájlformátum.

**M4B**: Minőségi szempontból nyer az MP3-mal összehasonlítva, ha mindkettőt azonos bitsebességgel kódolja. Az M4B egy hangoskönyv-fájl, amely AAC kódolással van tömörítve. Alapvetően az „MPEG-4 Audio Layer”-hez kapcsolódik, az .m4b kiterjesztésű fájlok az MPEG-4 filmek hangrétegét jelentik, de további hangoskönyvekkel kapcsolatos funkciókkal is rendelkezik. Célja, hogy megelőzze az MP3-at, és a hangtömörítés új szabványává váljon. Sok szempontból nagyon közel áll az MP3-hoz, de jobb minőségre fejlesztették ki azonos vagy még kisebb fájlméretben. Az M4B formátumot először az Apple vezette be. A formátumtípus Apple veszteségmentes kódolóként (ALE) is megvalósul.

Ezért az M4B jelenleg nem érheti el az MP3 mainstream sikerét, mivel az audio formátum még nem játszható le.

**Mp3**: Mindenki számára jól ismert digitális hangformátum. A legelső tömörítési formátum a színtéren, és nagyon híres lett a zenehallgatók körében. Mainstream sikere olyan gyors, hogy a fájltípus univerzálisan lejátszható, és szinte bármivel kompatibilis, legyen szó hardverről vagy szoftverről. Általánosságban elmondható, hogy az M4A jobb hangminőséget fog produkálni, de sokan azzal érvelnek, hogy akár igaz, akár nem, a hangkülönbség nem összehasonlítható, és időpocsékolás lenne MP3 fájlokat M4A fájlokká konvertálni. Végül az átalakítás csak elveszíti az eredeti hangminőséget.

## M4B fájlformátum specifikáció

Az [M4A]-hoz (/hu/audio/m4a/) hasonlóan az M4B fájlok is egymást követő darabokból állnak. Minden csonk 8 bájtos fejléccel rendelkezik, és a következőképpen van felosztva:
- 4 bájtos darabméret (big-endian, a magas bájt először)
- 4 bájtos csonktípus - az előre meghatározott aláírások egyike: "ftyp", "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "ctab", "skip", "jP2", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT" ", "scpt", "ssrc".

Az M4A-hoz hasonlóan az M4B első darabja "ftype" típusú lesz, és van egy altípusa a 8-as eltolásnál. Az M4B altípus által meghatározott, amelynek "M4B_"-nak kell lennie.

A darabok iterálása, amíg ismeretlen típusú darabot nem észlel, M4B (MPEG-4 Audio) fájlt készít.

## Hivatkozások

* [MPEG-4 14. rész – a Wikipedia által](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) formátum és helyreállítás példa](https://www.file-recovery.com/m4a-signature-format.htm)

