{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QT fájlformátum - gyors filmfájl",
  "keywords" :[ "QT", "QuickTime videó", "qt formátum", "qt fájlok lejátszása", "Quick Movie File", "QTFF", "video", "Apple" ],
  "description":"További információ a QT fájlformátumról és az API-król, amelyek QT fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Mi az a QT fájl?

A .qt kiterjesztésű fájl egy multimédiás tárolófájl, amelyet a QuickTime keretrendszer használ a multimédiás fájl tartalmának tárolására. Az Apple Inc. által kifejlesztett QuickTime File Format (QTFF) egy multimédiás tárolófájl, amely hangot, videót vagy szöveget tartalmaz a későbbi lejátszáshoz. Ez a választott formátum a digitális média eszközök, alkalmazások és operációs rendszerek közötti cseréjéhez. A QT-fájlokat [MOV](/hu/video/mov/) formátumban is menti a rendszer, amelyet szintén az Apple Inc. fejlesztett ki. A QT-fájlokat megnyitni képes alkalmazások közé tartozik az Apple QuickTime Player, a VLC médialejátszó és a Media Player Classic with K- Lite Codec Pack.

## QT fájlformátum

A QTFF objektumorientált, amely rugalmas objektumok gyűjteményét teszi lehetővé az elemzés és a bővítés megkönnyítése érdekében. A QT-fájl minden egyes műsorszáma tartalmaz egy digitálisan kódolt médiafolyamot vagy egy másik fájlban található médiafolyamra mutató adatreferenciát. Az atomoknak nevezett objektumokból álló hierarchikus adatstruktúra nyomkövető konténerként működik. A [QT-fájlformátum](https://developer.apple.com/documentation/quicktime-file-format) fájlformátum-specifikációi hivatalosan elérhetők az Apple Inc.-től a fejlesztői referenciaként.

### Médialeírás

A QuickTime fájl médialeírása a médiaadatoktól elkülönítve tárolódik. Az olyan információk, mint a műsorszámok száma, a videó tömörítési formátuma és az időzítési információk a médialeírásban tárolódnak (más néven filmforrás, filmatom vagy egyszerűen film). A médiaadatokra ebben a médiastruktúrában egy index hivatkozik. A médiaadatok a filmben használt tényleges mintaadatok, például videokockák és hangminták.

### Atomok

Az Atom a QuickTime fájl alapegysége. Bármely atomban két fő mező található a többi mező előtt: a Méret és a Típus mező. A méret mező az atom méretét mutatja, míg a típus mező az atomban tárolt adatok típusát. Az atomok természetüknél fogva hierarchikusak, ami azt jelenti, hogy egy atom tartalmazhat más atomokat, amelyek továbbra is tartalmazhatnak másokat. A mintaatom elrendezése a következő képen látható.

Minden atomnak két része van, fejléc és adat. A fejléc a méret és típus mezőket tartalmazza, az adatrész pedig a tényleges adatokat. Továbbá az alábbiakban az egyes mezőket ismertetjük:

#### Atomméret

Az atom fejlécét és tartalmát egy 32 bites egész szám jelzi, amelyet az atom méretének nevezünk. A méret mező tartalmazza az atom méretét bájtban, 32 bites előjel nélküli egész számban kifejezve.

#### Atom típusa

Az atom típusát egy 32 bites egész szám is mutatja, amelyet többnyire négykarakteres mezőként kezelnek knemonikus értékkel, például „moov” (0x6D6F6F76) filmatom esetén, vagy „trak” (0x7472616B) egy nyomatom. Ha az atom típusa ismert, lehetővé teszi az adatok értelmezését.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Fájlszerkezet ##

A QT/MOV fájlok egymást követő darabokból állnak. Minden csonknak van egy 8 bájtos fejléce: 4 bájtos csonkméret (big-endian, magas bájt először) és 4 bájtos csonktípus - az előre meghatározott aláírások egyike: "ftyp", "mdat", "moov", "pnot" ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". Az első darab "ftype" típusú, és van egy altípusa a 8-as eltolásnál. A MOV-t altípus határozza meg, amelynek "qt"-nek kell lennie. A MOV-fájl összeállításához ismételni kell a darabokat, amíg ismeretlen típust észlel.

Íme egy példa: Egy minta MOV fájl bináris adatainak vizsgálatakor nyilvánvaló, hogy az **ftyp** (hex: 66 74 79 70) aláírással kezdődik a 4. eltolásnál, amely meghatározza a QuickTime tárolófájl típusát. A fájl altípusa **qt~_~_** (hex: 71 74 20 20), amely a MOV fájltípusra mutat. Az első blokk mérete 32 (hexa: 00 00 00 20, big-endian, magas bájt először), a mérete 0 eltolásnál található. írja be az **mdat** (hex: 6D 64 61 74).

A következő darab a 32+8#40 eltolásnál (hex: 28) található, mérete 3 263 028 (hex: 00 31 CA 34), típusa pedig **mdat** (hex: 6D 64 61 74) a 44-es eltolásnál (hex) : 2C). A következő darab a 40 + 3 263 028#3 263 068 eltolásnál található (hex: 00 31 CA 5C), mérete 21 189 (hex: 00 00 52 C5), és típusa **moov** (hex: 6D 6F) at 6F 1 836 019 574 (hex: 00 31 CA 60). Ez az utolsó darab, tehát a teljes fájlméret 3 263 068+21 189#3 284 257 bájt.

## Referenciák ##

* [QT fájlformátum – Apple Inc.](https://developer.apple.com/documentation/quicktime-file-format)
* [QuickTime fájlformátum – Wikipédia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

