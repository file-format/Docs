{
  "date" : "2021-06-09",
  "keywords" :[ "m4p", "mp3", "fájl", "kiterjesztés", "formátum", "mi az m4p fájlformátum", "zene", "m4p fájlformátum", "M4b vs MP3", "m4p fájlformátum specifikációja"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tudjon meg többet az M4P fájlformátumról és az API-król, amelyek M4P fájlokat hozhatnak létre, konvertálhatnak és megnyithatnak.",
  "title" :"M4P - MPEG-4 hangoskönyv fájlformátum",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Mi az M4P fájl?
Az .m4p kiterjesztésű fájl egy hangfájl, amely általában letölthető az Apple iTunes áruházból. Más szóval azt mondhatjuk, hogy az M4P egy AAC fájl, de másolásvédett egy Digital Rights Management (DRM) segítségével. Ez azt jelenti, hogy az M4P fájlok csak engedélyezett rendszereken vagy eszközökön játszhatók le. Az M4P fájlok általában az Apple multimédiás eszközökre vonatkoznak. Így ezeket a fájlokat csak Apple Macbookokon, podcastokon és okostelefonokon, például iPhone 6-on vagy iPhone 7-en lehet lejátszani.

## M4P fájlformátum
Az M4P az MPEG 4 Protected (audio) rövidítése, és a hangot fejlett audiokodekkel (AAC) kódolja, és megvédi a fájlt a fájl jogosulatlan használatától. Ezt a fájlformátumot általában az iTunes Music Store hangfájlformátumának tekintik. Az Apple a FairPlay Digital Rights Management (DRM) rendszerét használja az M4P-fájlok védelmére. A FairPlay DRM a Veridisc által kifejlesztett technológián alapul. Védelmi mechanizmusa úgy működik, hogy az AAC hangfolyamot AES titkosítással titkosítja. A felhasználó kap egy mesterkulcsot, amelyet a fiókjához rendelnek a visszafejtéshez. Ezt a fájlformátumot az MP3 fájlformátum felváltásaként vezették be, mivel az MP3 eredetileg nem hangfájlnak készült, hanem egy MPEG 1 vagy 2 videofájl III. rétegének.


## M4P fájlformátum specifikációi

Az [M4A]-hoz (/hu/audio/m4a/) hasonlóan az M4P fájlok is egymást követő darabokból állnak. Minden csonk 8 bájtos fejléccel rendelkezik, és a következőképpen van felosztva:
- 4 bájtos darabméret (big-endian, a magas bájt először)
- 4 bájtos darabtípus - az előre meghatározott aláírások egyike: "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "skip", "ftyp", "jP2 ", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT", "scpt" ", "ctab", "ssrc".

Az M4A-hoz hasonlóan az M4P első darabja "ftype" típusú lesz, és van egy altípusa a 8-as eltolásnál. Az M4P-t altípus határozza meg, amelynek "M4P_"-nak kell lennie.

A darabok iterálása, amíg ismeretlen típusú darabot nem észlel, M4P (MPEG-4 Audio) fájlt készít.

## Hivatkozások ##

* [MPEG-4 14. rész – a Wikipedia által](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) formátum és helyreállítás példa](https://www.file-recovery.com/m4a-signature-format.htm)

