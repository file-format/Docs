{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "Fájlformátum", "CAD", "Megnyitás", "Létrehozás" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tudjon meg többet a DWG fájlformátumról és az API-król, amelyekkel DWG fájlokat hozhat létre és nyithat meg.",
  "title" :"DWG fájlformátum",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a DWG fájl?

A DWG kiterjesztésű fájlok a 2D és 3D tervezési adatok tárolására használt, védett bináris fájlok. A DXF-hez hasonlóan, amelyek ASCII fájlok, a DWG a CAD (számítógéppel segített tervezés) rajzok bináris fájlformátumát képviseli. Vektoros képet és metaadatokat tartalmaz a CAD-fájlok tartalmának megjelenítéséhez. Ingyenes megjelenítők állnak rendelkezésre a DWG fájlok megtekintésére Windows operációs rendszeren, például az Autodesk ingyenes DWG TrueView. Vannak más harmadik féltől származó alkalmazások is, amelyek támogatják a DWG-fájlok elérését. A DWG fájlok felhasználó által létrehozott információkat tartalmaznak, és a következőket tartalmazzák:

* Tervek
* Geometriai adatok
* Térképek és fényképek

Ezt a formátumot széles körben használják építészek, mérnökök és tervezők különféle tervezési célokra.

## Rövid története ##

A DWG fájlformátum az 1982-es hivatalos bevezetése óta eltelt idővel fejlődött. A múltbeli események rövid áttekintése a történelem szemszögéből a következő.

**1982:** Az Autodesk az AutoCAD alapjaként engedélyezte a Mike Riddle által 1970-ben kifejlesztett DWG fájlformátumot.

**1998:** Az AutoCAD R14.01 kiadásával az Autodesk hozzáadta a fájlellenőrzést a DWGCHECK nevű funkción keresztül, amely egy titkosított ellenőrző összeget és termékkódot, az Autodesk WaterMark néven nevezett be a program által létrehozott DWG-fájlokba.

**2006:** Az Autodesk módosította az AutoCAD 2007-et, és belefoglalta a "TrustedDWG technológiát" az "Autodesk DWG. Ez a fájl egy megbízható DWG, amelyet utoljára egy Autodesk-alkalmazás vagy az Autodesk-licencelt alkalmazás" mentett a DWG-fájlokba. Ennek az volt a célja, hogy segítse az Autodesk szoftver felhasználóit abban, hogy ezeket a fájlokat Autodesk vagy RealDWG alkalmazás hozza létre, ami mindenképpen segít csökkenteni az összeférhetetlenség kockázatát.

## Fájlszerkezet ##

A DWG az egyik legszélesebb körben használt fájlformátum volt számos alkalmazásban, és robusztus fájlszerkezettel rendelkezik. Mivel a DWG egy bináris fájlformátum, ember által nem olvasható, mint a sima ASCII [DXF](/hu/cad/dxf/) fájlformátum. A DWG-fájlok általában információkat tartalmaznak a kép koordinátáiról és a hozzájuk kapcsolódó metaadatokról. A DWG fájlformátum teljes [specifikációja](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) letölthető az OpenDesign által. A DWG fájlformátum fájlszerkezetét az alábbiakban foglaljuk össze.

**Fejléc**: A fájlfejléc DWG fejlécváltozókból és a hibaészlelésre használt ciklikus redundancia-ellenőrzés (CRC) információiból áll. Mindegyik alszakasz egy speciális vektor, ahol különböző hosszúságú biteket használnak a különböző címkék ábrázolására. Például a DWG fejléc változó első 6 bitje a verzió karakterláncot jelöli.

**Osztálydefiníciók:** Egy DWG-fájl számos osztályt tartalmazhat az adott .dwg fájl céljától függően. Az olyan információk, mint az osztály metaadatainak mérete az osztály adatterületén, az osztály száma és az ellenőrző összeg a többi mellett.

**Sablon**: Ez opcionális, és az R15 és R15 verziók esetében ez a rész az Object Free Space rész alatt található.

**Padding**: A metaadatok meghatározott számú bájttal utó- és utótaggal vannak rögzítve, így a régebbi AutoCAD szoftververziók továbbítási kompatibilisek lesznek az új DWG fájlformátummal.

**Képadatok**: A szakasz metaadatai az adott .dwg típustól függenek. Az R14 és R15 felhasználók számára ez a szakasz nem kötelező.

**Objektumadatok**: Az objektumadatok a meglévő objektumok listájának megfelelő tábla entitások, szótárbejegyzések stb. teljes listájából állnak.

**Objektumtérkép**: Az egyes objektumok helye a fájlban a fájl ezen szakaszában van megadva. Az ebben a szakaszban található metaadatok többsége fájlleíró, amely szerepet játszik az objektum azonosításában és újbóli megjelenítésében.

**Object Free Space**: Ez a rész nem kötelező minden felhasználó számára

**Második fejléc**: A fájl fejléc szakaszának másolata a DWG fájl vége felé

## Referenciák ##

* [DWG fájlformátum specifikációi](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [A DWG fájl specifikációja](https://www.scan2cad.com/dwg/file-spec/)
* [DWG – a Wikipédia által](https://en.wikipedia.org/wiki/.dwg)

