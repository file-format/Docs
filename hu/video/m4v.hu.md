{
  "date" : "2019-10-11",
  "keywords" :[ "M4V", "fájl", "kiterjesztés", "formátum", "MPEG-4", "Digitális jogkezelés", "DRM", "Apple", "videó"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"További információ az M4V fájlformátumról és az API-król, amelyek M4V fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## Mi az M4V fájl?

Az Apple által kifejlesztett **M4V** fájlformátum egy videotároló, amelyet opcionálisan digitális jogkezelés (DRM) másolásvédelemmel védenek a magánélet vagy a másolás védelme érdekében. A videókat és hangsávokat konténerfájlok veszik körül a lejátszási adatfolyamok indexeléséhez és rendezéséhez. Ezenkívül a konténerek a DVD-khez hasonló fejezetek funkcióját is biztosítják. Az Apple M4V-t használ a videók kódolására az iTunes Store-ban. Az Apple FairPlay másolásvédelmével védi a jogosulatlan reprodukálást azáltal, hogy lehetővé teszi az M4V fájlok lejátszását csak olyan engedélyezett számítógépeken, amelyek rendelkeznek a videó megvásárlásához használt fiókkal. Ha azonban eltávolítják a DRM-védelmet az M4V-fájlokról, ezek a fájlok más videolejátszókban is lejátszhatók, ha a kiterjesztést .m4v-ről .mp4-re módosítják, ezért az M4V-fájlok MPEG-4-hez vannak társítva. Az M4V H.264-et használ a videóhoz és **[AAC](/hu/audio/aac/)** és Dolby Digitalt a hangkódoláshoz és dekódoláshoz.

## M4V fájlstruktúra ##

Az M4V fájlok folyamatos darabokat tartalmaznak 8 bájtos fejléccel, 4 bájtos darabmérettel és 4 bájtos csonktípussal minden csonkban. Az első darab „ftype”, és van egy altípusa a 8-as eltolásnál. Az M4V altípus határozza meg, amelynek „M4V_”-nak kell lennie. A további darabtípusok előre meghatározott aláírások: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "ingyenes", "kihagyás", "jP2", "széles" , "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", " KÉP". A darabokat iterálva, amíg ismeretlen típust nem észlelünk, M4V fájlt készítünk.

Íme egy minta vizsgálata: Egy minta m4v fájl bináris adatait a Hex Viewer ellenőrzi, és megfigyelhető, hogy az **ftyp** (hex: 66 74 79 70) aláírással kezdődik a 4-es eltolásnál, amely meghatározza a QuickTime-ot. Tárolófájl típusa. A fájl altípusa **M4V_** (hex: 4D 34 56 20), amely M4V (MPEG-4) fájltípusra mutat. Az első blokk mérete 32 (hexa: 00 00 00 20, big-endian, a magas bájt az első), a méret 0 eltolásnál található. A 32-es eltolásnál (hex: 20) található a második darab, amelynek mérete 30 322 (hexa) : 00 00 76 72, big-endian, alsó bájt először) és írja be a **moov** (hex: 6D 6F 6F 76) parancsot. A következő darab a 32+30,322#30,354 eltolásnál található (hex: 00 00 76 92), mérete 8 (hexa: 00 00 00 08) és **ingyenes** (hexa: 66 72 65 65).
### Az M4V-ben használt kodekek ###

#### Videokodek H.264 ####

A H.264 egy videotömörítési szabvány, amely a digitális videót olyan formátummá alakítja, amely átvitel vagy tárolás esetén kevesebb helyet igényel. Az M4V H.264-et használ a videotömörítéshez. Alkalmazása a DVD-től, a TV-től, a videokonferenciától és az interneten keresztüli videó streamingtől terjed. A H.264 két fő részből áll: Encoder – amely tömöríti a videót, Decoder – amely visszatömöríti a tömörített videót. Az alábbi ábrán a kódolási és dekódolási folyamatok kiemeltek, a többi folyamatra pedig a H.264 szabvány vonatkozik.

##### Videókódolási és dekódolási folyamat a H.264-ben #####

A tömörített H.264 bitfolyam esetében a videokódoló végzi az előrejelzési, átalakítási és kódolási folyamatot. Ugyanakkor a dekódoló végrehajtja a dekódolás, az inverz transzformáció és a rekonstrukció fordított folyamatát a videofájl visszaállításához. A H.264 feleakkora, mint az MPEG.

#### Audiokodek ####

Az Advanced Audio Coding (AAC) egy audiokodek a veszteséges digitális hangtömörítéshez, és M4V tárolóban használatos. Az AAC az [MP3](/hu/audio/mp3/) formátum utódja, és jobb minőséget ér el, mint az MP3 azonos bitsebességgel. Az AAC formátum néhány információt kidob a tömörítési folyamat során, ami kevésbé fontos. Az AAC egy változó bitsebességű (VBR) blokkalapú kodek, ahol minden blokk 1024 időtartomány-mintára dekódol.

### Referenciák ###

* [Wikipédia – M4V](https://en.wikipedia.org/wiki/M4V)
* [Wikipédia – MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)

