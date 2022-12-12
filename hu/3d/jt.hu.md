{
  "date" : "2019-12-12",
  "keywords" :[ "JT", "fájl", "kiterjesztés", "formátum", "3D fbx", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a JT fájlformátumról és az API-król, amelyek JT fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"JT – Jupiter Tessellation File Format",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a JT fájl?

A **JT** (Jupiter Tessellation) a Siemens PLM Software által kifejlesztett, hatékony, iparág-központú és rugalmas, ISO-szabványos 3D adatformátum. Az Aerospace, az autóipar és a Heavy Equipment mechanikus CAD-tartományai a JT-t használják legvezetőbb 3D-s megjelenítési formátumként.

A JT formátum egy jelenetgrafikon, amely támogatja a CAD-specifikus attribútumokat és csomópontokat. Kifinomult tömörítési technikákat használnak a facet adatok (háromszögek) tárolására. Ez a formátum úgy van kialakítva, hogy támogassa a vizuális attribútumokat, a termék- és gyártási információkat (PMI), valamint a metaadatokat. Jó támogatást nyújt a tartalom aszinkron streamingje. A nehézgépiparban a szakemberek JT-fájlt használnak CAD-megoldásaikban és termékéletciklus-menedzsment (PLM) szoftverprogramjaikban a bonyolult áruk geometriájának vizsgálatára.

Mivel a JT szinte az összes fontos 3D CAD formátumot támogatja, összeállítása számos kombinációt képes kezelni, amelyeket "multi-CAD" néven ismerünk. Ez a több CAD összeállítás mindig jól kezelt és naprakész, mivel a natív CAD termékleíró fájlok és a hozzájuk tartozó JT fájlok közötti szinkronizálás automatikusan megtörténik. A JT fájlok eredetileg könnyűek, ezért alkalmasak internetes együttműködésekre. A vállalatok a 3D-s vizualizációk médián keresztül történő elküldésével sokkal könnyebben működnek együtt, mint a „nehéz” eredeti CAD-fájlokkal. Ezenkívül a JT-fájlok számos biztonsági funkciót biztosítanak, amelyek biztonságosabbá teszik a szellemi tulajdon megosztását.

## A JT fájlformátum rövid története

Az Engineering Animation, Inc. és a Hewlett Packard voltak a JT eredeti tervezői, akik ezt a formátumot Direct Model eszközkészletként fejlesztették ki. Miután az UGS Corp. felvásárolta az EAI-t, a JT az UGS csomagjának részévé vált. 2007 elején az UGS bejelentette a JT-t, mint a fő 3D formátumot. Ugyanebben az évben a Siemens AG megvásárolta az UGS-t, és kiderült, hogy a Siemens PLM Software. A Siemens a JT-t használja közös interoperabilitási formátumként és adatarchiválási formátumként. 2009-ben az ISO elfogadta a JT specifikációt közzétételre, mint ISO nyilvánosan elérhető specifikációt (PAS). 2010 közepén a ProSTEP iViP bejelentette, hogy ipari szinten a JT és a STEP AP 242 XML együtt használható a maximális adatelőny elérése érdekében. forgatókönyvek cseréje. 2012-ben a JT-t hivatalosan ISO szabványos (ISO 14306:2012 (ISO JT V1)) 3D vizualizációs formátumnak nyilvánították.

## JT fájlformátum ##

Minden JT formátumú objektumot egy objektumazonosító ábrázol, és az objektumok közötti hivatkozásokat a hivatkozott objektum azonosítója kezeli. Ezen objektumhivatkozások integritása a mutatók feloldásával/swizzlingével tartható fenn.

A JT fájl blokkok sorozataként van elrendezve, és a fejléc blokk mindig az első adatblokk a fájlban. Egy sor adatszegmens és egy TOC szegmens közvetlenül követi a fejléc blokkot. Az egyetlen adatszegmens (6 LSG szegmens) mindig létezik referencia-kompatibilis JT-fájllal. A TOC szegmens az adott fájl összes többi adatszegmensének helyinformációit tartalmazza.

{{< figure src="../JT-1.png" alt="JT fájlformátum" >}}

### Fájlfejléc ###

A fájlfejléc az első blokk a JT fájl adathierarchiájában. A verziószám és a tartalomjegyzék helyére vonatkozó információ a fejlécben található, ami megkönnyíti a betöltőket a fájlolvasás során. A fájlfejléc tartalma a következőképpen van elrendezve.

### TOC szegmens ###

A TOC szegmensnek léteznie kell egy fájlban, és tartalmaznia kell az összes többi adatszegmens azonosítási és helyinformációit. A TOC szegmens tényleges helyét a fájl fejlécének TOC Offset mezője határozza meg. Minden egyes egyedileg címezhető adatszegmens egy TOC-szegmensben található TOC-bejegyzéssel jelenik meg.

### Adatszegmens ###

A JT fájl meghatározza az összes tárolt adatot egy adatszegmensen belül. Egyes adatszegmensek tömöríthetik a szegmensben maradt információ összes adatbájtját. Az adatszegmensek a következő szerkezettel rendelkeznek:

![alt text](../JT-2.png "JT Data Segment")

Az alábbi táblázat a különböző típusú adatszegmenseket írja le:

|Név|Leírás
---|---|
|LSG szegmens|Objektumok gyűjteményét tartalmazza, amelyek irányított hivatkozásokon keresztül LSG-t (irányított aciklikus gráfstruktúra) alkotnak
|Alakzat LOD szegmens|tartalmazza a geometriai alakzatok meghatározó adatait (pl. csúcsok, normálok, sokszögek stb.)
|JT B-Rep szegmens|JT B-Rep formátumú egyedi rész pontos geometriai határait ábrázoló adatelemekkel.
|XT B-Rep szegmens|Az adatokhoz olyan elem tartozik, amely egy adott rész pontos geometriai határvonalát ábrázolja határábrázolási formátumban
|Drótváz szegmens|Az adatok pontos 3D drótvázat jelenítenek meg egy adott részhez, amelyet egy ebben a szegmensben található elem határoz meg.
|Meta adatszegmens|Lehetővé teszi a metaadatok tárolását külön címezhető szegmensekben.
|JT ULP szegmens|JT ULP formátumú egyedi rész félig pontos geometriai határvonalát ábrázoló adatelemekkel.
|JT LWPA szegmens|Elemet tartalmaz, amely meghatározza egy adott alkatrész analitikai adatait. Az LWPA az analitikai felületek gyűjteményét az alkatrész b-rep definíciójába foglalja.

## Tömörítés ##

A 3D modellek átviteli és tárolási követelményei szigorúbbak, így a JT fájlok kihasználhatják a tömörítés előnyeit. A JT adatmodell különböző fájlokból állhat különböző tömörítési technikával, de a tömörítési folyamat átlátható a JT adatfelhasználó számára.

Eddig a JT Open Toolkit (szabványként) és a fejlett tömörítés a JT fájlok által használt két tömörítési technika. A JT Open Toolkit egy egyszerű, veszteségmentes tömörítési algoritmust alkalmaz, míg a fejlett tömörítés egy kifinomultabb, tartományspecifikus tömörítési technikát alkalmaz, amely veszteséges geometriatömörítéshez vezet. Az ügyfélalkalmazások inkább a fejlett tömörítést részesítik előnyben, mint a szabványos tömörítést, mivel a fejlett tömörítés meglehetősen magas tömörítési arányt eredményez. A normál JT fájlmegjelenítő alkalmazásokkal való visszamenőleges kompatibilitást a szabványos tömörítés biztosítja. A tömörítési űrlapnak kompatibilisnek kell lennie a JT fájlformátum verziójával, amely akkor látható, amikor egy JT fájl szövegszerkesztővel megnyílik, és az ASCII fejléc információi közé kell zárni.

## Hivatkozások ##

* [JT fájlformátum referencia](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (vizualizációs formátum)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)

