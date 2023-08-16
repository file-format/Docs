{
  "date" : "2020-08-20",
  "keywords" :[ "fnt fájl", "fnt fájl formátum", "mi az fnt fájl", "fájl", "fnt példa", "fnt fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - Windows Font File",
  "description":"További információ az FNT fájlformátumról és az FNT-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Mi az FNT fájl?

Az .fnt kiterjesztésű fájl olyan betűtípusfájl, amely általános betűtípus-információkat tárol a Windows operációs rendszereken. Az FNT fájlokat többnyire a TrueType (.TTF) és az OpenType (.OTF) fájlformátumok váltották fel, és máig elavult betűtípus-fájlformátum. Ezek a fájlok egyetlen értékelő vagy vektoros betűtípust tárolhatnak. Minden eszközillesztő támogatja a Windows 2.x betűtípusokat. Azonban nem minden eszközillesztő
támogatja a Windows 3.0 verziót.

## FNT fájlformátum

Az FNT fájlok egyetlen raszteres vagy vektoros betűtípus tárolására képesek. A vektoros formátumokat a GDI gyakrabban használja, mint a raszteres, ahol minden egyes charta karakterjelét egy kis bittérkép segítségével határozzák meg. Az .fnt .ttf-re és .otf-re cserélésének nyilvánvaló oka a raszteres formátum.

### Betűtípusfájl fejléce
Mind a raszteres, mind a vektoros betűtípus-fájlok eleje gyakori, amit az egyes fájltípusokhoz más-más információ követ. A Windows 3.0 font-fájl fejléce hat új mezőt tartalmaz az alábbiak szerint, amelyek nullára vannak állítva, hogy biztosítsák a kompatibilitást a Windows jövőbeli verzióival.

* dFlags
* dfAspace
* dfBspace
* dfCspace
* dfColorPointer
* dfReserved1

A Windows 3.0 és 2.0 fejléceivel kapcsolatos részletes információkért keresse fel a [Microsoft KnowledgeBase Archívumot](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Hivatkozások
* [Font fájlformátum](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [A betűtípus telepítése vagy eltávolítása Windows rendszerben](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8-7613-c76f-88d043b334b8)

