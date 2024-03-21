{
  "date" : "2019-10-11",
  "keywords" :[ "djvu fájl", "djvu fájl formátum", "mi az a djvu fájl", "fájl", "djvu példa", "djvu fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DJVU fájlformátum",
  "description":"További információ a DJVU fájlformátumról és az API-król, amelyek DJVU fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a DJVU fájl?

A DjVu, ejtsd: „déjà vu”, egy grafikus fájlformátum, amelyet beolvasott dokumentumokhoz és könyvekhez, különösen azokhoz, amelyek szövegek, rajzok, képek és fényképek kombinációját tartalmazzák. Az AT&T Labs fejlesztette ki. Többféle technikát használ, mint például a szöveg és a háttérkép képréteg-elválasztása, progresszív betöltés, aritmetikai kódolás és veszteséges tömörítés a bitonális képekhez. Mivel a DJVU fájl tömörített, de jó minőségű színes képeket, fényképeket, szöveget és rajzokat tartalmazhat, és így kevesebb helyen menthető, a weben e-könyvként, kézikönyvként, újságként, régi dokumentumként stb.

A DjVu a [PDF](/hu/pdf/) kiváló alternatívájaként értékelhető. A DjVu-hoz társított fájlkiterjesztések .DJVU vagy .DJV. A DjVu körülbelül 5-10-szer jobb tömörítési arányt tud elérni, mint a jelenlegi módszerek, például a [JPEG](/hu/image/jpeg/) és [GIF](/hu/image/gif/) színes dokumentumok esetén, és 3-8-szor jobb, mint a [TIFF](/image/tiff/) fekete-fehér dokumentumokban. A 300 DPI-vel szkennelt, színes dokumentumok akár 25 MB-ig 30-100 KB-ig tömöríthetők. Hasonlóképpen a fekete-fehér dokumentumok 5-30 KB-ig tömöríthetők. Egy átlagos HTML oldal akár 50 KB méretű is lehet, így ezek a dokumentumok gond nélkül feltölthetők a netre.

## Rövid története ##

A DjVu technológiát az AT&T laborokban fejlesztette ki [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner és Paul G 1996-tól 2001-ig. A DjVu fájlformátum különböző felülvizsgálatokon ment keresztül, a legutóbbi 2005-ből származik.


|Verzió|Kiadás dátuma|Megjegyzések
---|---|---|
|1–19|1996–1999|Ezek a fejlesztő verziók.
|20|1999. április|Az egyoldalas formátum többoldalas formátumra módosult.
|23|2002. július|CID-darab
|24|2003. február|LTAnno darab
|21|1999. szeptember|A közvetett tárolási formátum lecserélve. Szövegkereső réteg hozzáadva.
|22|2001. április|Oldaltájolás, szín JB2
|25|2003. május|NAVM-darab. A DjVu könyvjelzők támogatása hozzáadásra került.
|26|2005. április|Szöveges/soros megjegyzések

## DjVu fájlformátum ##

A DjVu dokumentumok IFF85 fájlok. A struktúra a konténerek hierarchiáját biztosítja, amely információkat tartalmaz egy DjVu fájlban. Ezeket a tartályokat „daraboknak” is nevezik. A csonk típusa és a darabazonosító leírja a csonk használatát. Van egy 4 bájtos fejléc, amelyet az IFF szerkezet követ. A DjVu fájl első négy bájtja 0x41 0x54 0x26 0x54. Ez a rész a különféle DjVu-dokumentumokat és az ezekből álló megfelelő részeket tárgyalja.


|Chunk ID|Használat
---|---|
|FORM|Az összetett csonk, amely tartalmazza a FORM csonk első négy adatbájtját, amelyek másodlagos azonosítók.
|FORM:DJVM|Egy többoldalas DjVu dokumentum. Összetett darab, amely tartalmazza a DIRM-darabot.
|FORM:DJVU|Egyoldalas DjVu dokumentum. Összetett darab, amely tartalmazza a djvu-dokumentum oldalát alkotó darabokat.
|FORM:DJVI|Egy „megosztott” DjVu-fájl, amelyet az INCL-darabon keresztül tartalmaznak. Megosztott megjegyzések és alakszótár.
|FORM:THUM|Összetett darab, amely tartalmazza a TH44 darabokat, amelyek a beágyazott bélyegképek.
|DIRM|Többoldalas dokumentumok oldalnév-információi.
|NAVM|Könyvjelző információk
|ANTa, ANTz|Annotációk, beleértve a kezdeti nézetbeállításokat és az átfedő hiperhivatkozásokat, szövegdobozokat stb.
|TXTa, TXTz|Unicode Szöveg- és elrendezési információk.
|Djbz|Megosztott alakzattábla.
|Sjbz|BZZ tömörített JB2 bitonális adatok a maszk tárolására.
|FG44|IW44 adatok az előtér tárolására
|BG44|IW44 adatok a háttér tárolására
|TH44|IW44 adatok a beágyazott miniatűrök tárolására
|WMRM|JB2 adatok szükségesek a vízjel eltávolításához
|FGbz|Színes JB2 adatok. Színt ad a megfelelő Sjbz-darab mindegyikéhez (blit vagy alakzat?).
|INFO|Információ a DjVu oldalról
|INCL|Egy mellékelt FORM:DJVI darab azonosítója.
|BGjp|JPEG kódolású háttér
|FGjp|JPEG kódolású előtér
|Smmr|G4 kódolású maszk

### DJVU tömörítés

Az egyetlen kép több különböző képre van felosztva, majd minden képet külön-külön tömörít. A DjVu fájl létrehozásához a képet először három képre, egy háttérre, előtérre és egy maszkképre osztják fel. A háttér- és előtérképek általában alacsonyabb felbontású színes képek; de a maszk kép egy nagyobb felbontású kép és jellemzően a szöveget ott tárolják. A szétválasztás után az előtér- és a háttérképet egy wavelet alapú IW44 tömörítési algoritmussal, míg a maszkképet egy másik módszerrel, a JB2-vel tömörítik.

A JB2 kódolási módszer kiküszöböli a szövegkép redundanciájának nagy részét azáltal, hogy azonos alakzatokat azonosít az oldalon, például egy karakter többszöri előfordulását egy adott betűtípusban. A JB2 először kódolja az egyes egyedi alakzatok bittérképét, kihasználva a hasonló alakzatok közötti redundanciát. Ezután kódolja azokat a helyeket, ahol az egyes alakzatok megjelennek az oldalon. Mind a JB2, mind az IW44 egy új típusú adaptív bináris aritmetikai kódolóra támaszkodik, az úgynevezett ZP-kódolóra, amely a Shannon-határ néhány százalékán belül kiszorítja a maradék redundanciát. A ZP-kódoló adaptív, és gyorsabb, mint a többi közelítő bináris aritmetikai kódoló.

## Hivatkozások ##

* [DjVu – Wikipédia](https://en.wikipedia.org/wiki/DjVu)
* [DjVu fájlformátum](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

