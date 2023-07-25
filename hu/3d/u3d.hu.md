{
  "date" : "2019-10-11",
  "keywords" :[ "u3d fájl", "u3d fájlformátum", "mi az u3d fájl", "fájl", "u3d példa", "u3d fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - univerzális 3D fájlformátum",
  "description":"További információ az U3D fájlformátumról és az API-król, amelyek U3D fájlokat nyithatnak meg és hozhatnak létre.",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az U3D fájl?

Az **U3D** (Universal 3D) egy tömörített fájlformátum és adatstruktúra a 3D számítógépes grafikákhoz. 3D modellinformációkat tartalmaz, például háromszöghálókat, világítást, árnyékolást, mozgásadatokat, vonalakat és pontokat színnel és szerkezettel. A formátumot 2005 augusztusában fogadták el [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) szabványként. A 3D [PDF](/hu/pdf/) dokumentumok támogatják az U3D-t objektumok beágyazása, és megtekinthető az Adobe Readerben (7-es és újabb verzió).

Az U3D formátumot azzal a céllal fejlesztették ki, hogy egy univerzális szabványt hozzanak létre a háromdimenziós adattároláshoz és adatcseréhez. A formátumot azonban elsősorban a 3D PDF kódolásában használják, nem pedig csereformátumként. Az Acrobat 3D a támogatott 3D fájltípusokat U3D-re vagy PRC-re konvertálja a PDF formátumba konvertáláskor.

## U3D fájlformátum

Az U3D fájlok bináris fájlformátumúak, amelyek az [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) referenciadokumentumban leírtak szerint négy kiadáson mentek keresztül, ami a specifikációk frissítését eredményezte. minden kiadással. Az ISO-32000 PDF fájlszabvány elfogadja az U3D-t engedélyezett annotációként és multimédiás típusként.

Az U3D első kiadása a 3D-s grafikai tulajdonságok kulcsfontosságú megjelenítésére összpontosított, mint például a geometria, a színek, a textúrák, a világítás, a csontok és a transzformációs alapú animáció. A második és harmadik kiadás javított néhány hibát az első kiadásban, a harmadik verzió volt a leggyakrabban használt típus az ipari szoftverekben. A negyedik kiadás definíciókat ad a magasabb rendű primitívekre (ívelt felületekre). Az [U3D specifikációk](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) online elérhetők felhasználói hivatkozásként az ECMA webhelyén.

### Adattípusok U3D-fájlokban

A bináris fájl a következő típusokat tartalmazza: U8, U16, U32, U64, I16, I32, F32, F64 és String.

* U8 : Előjel nélküli 8 bites egész szám
* U16 : Előjel nélküli 16 bites egész szám
* U32 : Előjel nélküli 32 bites egész szám
* U64 : Előjel nélküli 64 bites egész szám
* I16 : Előjeles 16 bites egész szám
* F32: Egyetlen precíziós IEEE úszó.
* F64: IEEE kettős pontosságú úszó.
* Karakterlánc: Az U3D fájlban lévő karakterláncok előjel nélküli 16 bites egész számmal kezdődnek, amely meghatározza a karakterláncban lévő karakterek teljes hosszát. A karakterláncok feldolgozása mindig kis- és nagybetűk között történik.

## U3D fájlszerkezet

Az U3D fájl blokkok sorozatát tartalmazza. Minden U3D fájlban 3 különböző típusú blokk található.

* Fájlfejléc blokk
* Nyilatkozat blokk
* Folytatás blokk

A betöltő meghatározza a blokk végét, ha az adott blokkban lévő adatokra nincs szükség, vagy ha az adott blokktípushoz nem érhető el dekódoló.

{{< figure src="../u3d.png" alt="U3D fájlformátum" >}}

### Fájlfejléc blokk
A fájlfejléc blokk olyan fájlinformációkat tartalmaz, amelyeket a betöltött a fájl olvasásának meghatározására használ fel.

### Nyilatkozat blokk

A deklarációs blokkok információkat tartalmaznak a fájlban lévő objektumokról. A deklarációs blokkban lévő objektumokat definiálni kell.

### Folytatás blokk

A Deklaráció blokkban deklarált objektumokra vonatkozó további információk a folytatásos blokkban találhatók. Minden folytatási blokkot hozzá kell rendelni egy deklarációs blokkhoz.


## Hivatkozások ##

* [U3D fájlformátum – Wikipédia](https://en.wikipedia.org/wiki/Universal_3D)
* [ECMA U3D fájlformátum specifikációi](https://www.ecma-international.org/publications/standards/Ecma-363.htm)

