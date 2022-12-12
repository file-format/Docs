{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR3 fájlformátum - Canon Raw 3 képfájl",
  "description":"További információ a CR3 fájlformátumról és az API-król, amelyek CR3 fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Mi az a CR3 fájl?

A CR3 fájl egy Canon RAW képfájl formátum, amelyet bizonyos Canon digitális fényképezőgépek hoznak létre. A Canon a CR2 fájlformátum helyettesítésére vezette be, és néhány Canon digitális eszköz használja. A CR3 fájlok a fényképezőgép által rögzített eredeti, nem feldolgozott veszteségmentes képadatokat tárolják. Ezeknek a nyers képeknek a használata kiváló minőségű képeket biztosít, és rengeteg szerkesztési lehetőséget biztosít a fotósok számára. A fő képadatokon kívül a CR3 fájlok a kép metaadatait is tárolják.

## CR3 fájlformátum

A CR3 fájlok bináris fájlként kerülnek a lemezre az ISO Base Media File Format (ISO/IEC 14496-12) szerint, és egyéni [Canon-címkéket] is tartalmaznak (https://exiftool.org/TagNames/Canon.html#uuid). Tartalmazza továbbá a [Canon „crx” kodeket] (https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp), amely a JPEG-LS (Rice-Golomb + RLE) keveréke kódolás) és JPEG-2000 (LeGall 5/3 DWT + kvantifikáció).

## CR3 egyéni címkék

A CR3 fájlok különböző célokra egyedi címkéket tartalmaznak. E címkék közül néhány a következő.

|Címkeazonosító| Címke neve| Írható |Értékek / Megjegyzések|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP címkék|
|'CMT1' |IFD0| - |--> EXIF-címkék|
|'CMT2' |ExifIFD| - |--> EXIF-címkék|
|'CMT3' |MakerNoteCanon| - |--> Canon Címkék|
|'CMT4' |GPSIinfo| - |--> GPS-címkék|
|'CNCV' |CompressorVersion| nem| |
|'CNOP' |CanonCNOP| - |--> Canon CNOP címkék|
|'CNTH' |CanonCNTH| - |--> Canon CNTH címkék|
|'THMB' |ThumbnailImage| nem| |

## Hivatkozások

* [CR2 fájlformátum] (http://lclevy.free.fr/cr2/)
* [Canon-címkék](https://exiftool.org/TagNames/Canon.html#uuid)

