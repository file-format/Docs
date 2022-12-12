{
  "date" : "2019-10-11",
  "keywords" :[ "dcm fájl", "dcm fájlformátum", "mi az a dcm fájl", "fájl", "dcm példa", "dcm fájlkiterjesztés", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCM fájlformátum – digitális orvosi információs fájl",
  "description":"További információ a DCM-fájlformátumról és az API-król, amelyek DCM-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-07-03"
}

## Mi az a DCM fájl?

A .dcm kiterjesztésű fájlok olyan digitális képet képviselnek, amely a betegek orvosi adatait, például MRI-ket, CT-vizsgálatokat és ultrahangképeket tárolja. A DCM-fájlok [DICOM](/hu/image/dicom) (Digital Imaging and Communications in Medicine) képfájlformátumot használnak, és referenciaként tartalmazhatják a páciens adatait. A [National Electrical Manufacturers Association] (https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) fejlesztette ki, és célja az volt, hogy szabványosítsa a képalkotó fájlformátumot az orvosi képek terjesztéséhez és megtekintéséhez.

## DCM fájlformátum

A DCM fájlok DICOM képformátumban tárolják az információkat. Ezek a fájlok tárolják az adatkészletet, amely valós információ, amely egy DICOM IOD-hoz kapcsolódó SOP-példányt képvisel. A DICOM fájl metainformációi a fájlban tárolódnak, majd az aktuális adatkészlet bájtfolyama.

### DICOM fájl metainformáció ##

Minden DICOM-fájl tartalmaz egy azonosító információs fejlécet a beágyazott adatkészlethez, amely a következőkből áll:
* 128 bájtos fájl preambulum
* 4 bájtos DICOM előtag
* Fájl metaelemek

Ez a fejléc minden DICOM-fájlhoz kötelező.

### Fájl metaelemei ###
|Attribútum neve|Címke|Típus| Attribútum leírása
---|---|---|---|
|Fájl preambuluma|Nincsenek címke- vagy hosszmezők|1|Rögzített 128 bájtos mező érhető el az alkalmazásprofil vagy a megvalósítás által meghatározott felhasználáshoz. Ha nem egy alkalmazásprofil vagy egy adott megvalósítás használja, minden bájtot 00H-ra kell állítani. A fájlkészlet olvasói vagy frissítői nem hagyatkozhatnak a preambulum tartalmára annak megállapítása során, hogy ez a fájl DICOM-fájl-e vagy sem.
|DICOM előtag|Nincs címke vagy hosszmező|1|Négy bájt, amely tartalmazza a "DICM" karakterláncot. Ez az előtag annak felismerésére szolgál, hogy ez a fájl DICOM-fájl-e vagy sem.
|Fájl metainformációs csoport hossza|(0002,0000)|1|A fájl metaelemet követő bájtok száma (az Érték mező vége) a 2. csoport utolsó fájl metaeleméig, beleértve a 2. csoport fájl metainformációit
|File Meta Information Version|(0002,0001)|1|Ez egy két bájtos mező, ahol minden bit a fájl metainformáció fejlécének egy-egy verzióját azonosítja. Az 1-es verzióban az első bájt értéke 00H, a második bájtérték pedig 01H. Olyan megvalósítások, amelyek olyan metainformációt tartalmazó fájlokat olvasnak, amelyeknél ez az attribútum a második bájt 0-s bitje (lsb) 1-re van állítva, értelmezhetik a fájl metainformációit az ebben meghatározottak szerint. PS3.10 verzió. Az összes többi bitet nem kell ellenőrizni.
|Médiatár SOP osztály UID|(0002,0002)|1|Egyedileg azonosítja az adatkészlethez társított SOP osztályt. A médiatároláshoz engedélyezett SOP osztályú UID-ket a PS3.4 - Media Storage Application Profiles tartalmazza.
|Médiatár SOP-példány UID|(0002,0003)|1|Egyedileg azonosítja a fájlban elhelyezett adatkészlethez társított SOP-példányt, amely a fájl metainformációit követi.
|Transfer Syntax UID|(0002,0010)|1|Egyedileg azonosítja a következő adatkészlet kódolásához használt átviteli szintaxist. Ez az átviteli szintaxis nem vonatkozik a fájl metainformációira.
|Implementation Class UID|(0002,0012)|1|Egyedileg azonosítja az implementációt, amely ezt a fájlt írta, és annak tartalmát. Csereproblémák esetén egyértelműen azonosítja a fájlt legutóbb író implementáció típusát.
|Implementation Version Name|(0002,0013)|3|Az implementációs osztály UID (0002,0012) verzióját azonosítja a repertoár legfeljebb 16 karakteréből.
|Forrásalkalmazás-entitás címe|(0002,0016)|3|A DICOM-alkalmazás entitás (AE) címe, amely a fájl tartalmát írta (vagy legutóbb frissítette). Használata esetén médiacsere-problémák esetén lehetővé teszi a hibaforrás nyomon követését.
|Private Information Creator UID|(0002,0100)|3|A privát információ létrehozójának UID-je (0002,0102).
|Privát információ|(0002,0102)|1C|A Fájl metainformációiban elhelyezett személyes információkat tartalmaz. Az alkotót (0002,0100) kell azonosítani. Szükséges, ha a Private Information Creator UID (0002,0100) szerepel.

### Adatkészlet beágyazása ###

A DICOM-fájl egyetlen adatkészletet tartalmaz, amely egyetlen SOP-osztályhoz kapcsolódó egyetlen SOP-példányt képvisel. A DICOM fájl metainformációjának átviteli szintaxisának UID-je határozza meg az adatkészlet kódolásához használt átviteli szintaxist.

### Fájlkezelési információk támogatása ###

A Media Format Layer a következő fájlkezelési információkat nyújtja, ha szükséges egy adott DICOM alkalmazásprofilhoz.

* A fájltartalom tulajdonosának azonosítása

* Fájl-hozzáférési statisztikák (pl. a létrehozás dátuma és időpontja)

* Alkalmazásfájl hozzáférés-szabályozás

* Fizikai adathordozó-hozzáférés szabályozása (pl. írásvédelem)

## Hivatkozások ##
* [DICOM-szabvány](https://www.dicomstandard.org/current/)
* [DICOM fájlformátum] (http://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

