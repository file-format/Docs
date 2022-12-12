{
  "date" : "2019-10-11",
  "keywords" :[ "gif fájl", "gif fájl formátum", "mi az a gif fájl", "fájl", "gif példa", "gif fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GIF - Képfájl formátum",
  "description":"További információ a GIF fájlformátumról és az API-król, amelyek GIF-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "GIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a GIF fájl? ##

A GIF vagy grafikus csereformátum az erősen tömörített képek egyik fajtája. A Unisys tulajdonában lévő GIF az LZW tömörítési algoritmust használja, amely nem rontja a képminőséget. Minden képhez a GIF általában legfeljebb 8 bitet tesz lehetővé pixelenként, és legfeljebb 256 szín megengedett a képen. Ellentétben a [JPEG](/hu/image/jpeg/) képpel, amely akár 16 millió színt is képes megjeleníteni, és meglehetősen megérinti az emberi szem határait. Amikor az internet megjelent, a GIF-ek maradtak a legjobb választás, mivel alacsony sávszélességet igényeltek, és kompatibilisek voltak a szilárd színterületeket fogyasztó grafikákkal. Az animált GIF számos képet vagy képkockát egyesít egyetlen fájlba, és sorozatban jeleníti meg őket animált klip vagy rövid videó létrehozásához. A színkorlátozás kockánként legfeljebb 256 lehet, és valószínűleg a legkevésbé alkalmas más képek és fényképek színátmenetes reprodukálására.

## GIF fájl formátum ##

Elméletileg a GIF-fájlok fix méretű grafikus területtel rendelkeznek, amelyet nulla vagy több kép tölt ki. Egyes GIF-fájlok a rögzített méretű grafikus területet vagy blokkokat részképekre osztják, amelyek animált GIF esetén animált keretként is funkcionálhatnak. A GIF formátum 1-8 bites pixelmélységet használ a bittérképes adatok tárolására. A képek tárolására mindig az RGB színmodell- és palettaadatokat használják. A verziótól függően egy fix hosszúságú fejléc ("GIF87a" vagy "GIF89a") határozza meg egy tipikus GIF-fájl kezdetét.

Jelenleg a GIF két verziója érhető el: 87a és 89a. Az előbbi az eredeti GIF formátum, míg az utóbbi az új GIF formátum. Ebben a fájlformátumban a blokkok jellemzőit és a pixelméreteket egy rögzített hosszúságú logikai képernyőleíró említi. A globális színtáblázat létezését és méretét a képernyőleíró határozhatja meg, amely további részleteket követ, ha vannak. A trailer a fájl utolsó bájtja, amely egyetlen bájtot tartalmaz egy ASCII pontosvesszőből. Egy tipikus GIF87a fájlelrendezés a következő:

### Fejléc ###

A fejléc hat bájtot tartalmaz, és a fájl típusának megadására szolgál GIF-ként. Bár a Logikai Képernyő Leíró el van választva a tényleges fejléctől, néha a második fejlécnek tekintik. Ugyanaz a struktúra, amelyet a fejléc tárolására használunk, tárolhatja a logikai képernyő-leírót. Minden GIF-fájl 3 bájtos aláírással kezdődik, és a „GIF” karaktereket használja azonosítóként. A verzió szintén három bájt méretű, és deklarálja a GIF fájl verzióját.

### Logikai képernyőleíró ###

A rögzített hosszúságú képleíró megadja a GIF-kép létrehozásához szükséges képernyő- és színinformációkat. A Magasság és Szélesség mezők a képernyőfelbontás legkisebb értékét tartalmazzák, amely kötelező a képadatok megjelenítéséhez. Ha a megjelenítő eszköz nem képes megjeleníteni a megadott felbontást, akkor a kép megfelelő megjelenítéséhez méretezésre lesz szükség. A képernyő és a színtérkép információit az alábbi táblázat négy almezője jeleníti meg (míg a 0 bit a legkisebb jelentőségű bit):


|Bits|Részmezők
---|---|
|0-2|A globális színtábla mérete
|3|Színes táblázat rendezési zászló
|4-6|Színfelbontás
|7|Globális színes táblázat zászló

#### Globális színtábla ####

Az opcionális globális színtáblázat közvetlenül a Logikai képernyőleíró után kerül elhelyezésre. Ez a táblázat a képadatokon belüli pixelszínadatok indexelésére van leképezve. Globális színtábla hiányában a GIF-fájlban minden kép a saját helyi színét használja. Jobb, ha megad egy alapértelmezett színtáblázatot, ha a Globális és a Helyi színtáblázat is hiányzik. Három bájtos triplák sorozata alkotja a színtábla elemeit. Minden bájt egy RGB színértéket jellemez. A piros, zöld és kék színek az egyes színtáblázatelemek értékei. A globális színtáblázat bejegyzései legfeljebb 256 bejegyzést érnek el, és mindig kettő hatványában jelennek meg.

#### Képadatok ####

A képadatok egy bájt kódolatlan szimbólumot tárolnak, amelyet az al- linkek listája követ, valamint az LZW kódolású adatokat.

#### Filmelőzetes ####

A trailer egyetlen bájtnyi adatot képvisel, amely a fájl utolsó karaktere. Ennek a bájtnak az értéke állandóan 3Bh, és az adatfolyam végét határozza meg. Minden GIF-fájl utolsó részében szerepelnie kell az előzetesnek.

## Referenciák ##

* [GIF fájlformátum](https://en.wikipedia.org/wiki/GIF)

