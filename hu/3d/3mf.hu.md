{
  "date" : "2019-12-09",
  "keywords" :[ "3mf fájl", "3mf fájlformátum", "mi az a 3mf fájl", "fájl", "3mf példa", "3mf fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"Tudjon meg többet a 3MF fájlformátumról és az API-król, amelyek képesek megnyitni és létrehozni 3MF fájlokat.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## Mi az a 3MF fájl?

A 3MF, 3D gyártási formátumot az alkalmazások 3D objektummodellek megjelenítésére használják számos más alkalmazás, platform, szolgáltatás és nyomtató számára. Úgy készült, hogy elkerülje az egyéb 3D-s fájlformátumok, például az [STL](/hu/cad/stl/) korlátozásait és problémáit a 3D nyomtatók legújabb verzióival való munkavégzés során. A 3MF egy viszonylag új fájlformátum, amelyet a 3MF konzorcium fejlesztett ki és adott ki. Elég gazdag ahhoz, hogy teljes körűen leírjon egy modellt, megtartja a belső információkat, színeket és egyéb jellemzőket, ami bővíthetővé teszi a 3D nyomtatás új innovációinak támogatásához. A formátum bővíthető, széles körben alkalmazható, és mentes a többi széles körben használt fájlformátumot érintő problémáktól.

## A 3MF fájlformátum rövid története

A rendelkezésre álló modellleíró fájlformátumok, például az STL és mások létező korlátai arra késztetik a vezető márkákat, hogy összefogjanak, és kidolgozzanak egy bővíthetőbb fájlformátumot a 3D nyomtatáshoz. Fontos szempont volt, hogy az alkalmazások hogyan továbbítsák a modelladatokat a 3D nyomtatóknak. A 3MF konzorcium ezért egy új, 3MF nevű 3D fájlformátum támogatására jött létre azzal a céllal, hogy az elég bővíthető legyen a 3D nyomtatás igényeinek kielégítésére. Számos vállalat tagja volt ennek a konzorciumnak, köztük a Microsoft, az Autodesk, a Dassault Systems, a Netfabb, az SLM, a HP és mások. A Microsoft a 3D-s fájlformátum folyamatban lévő munkáját adományozta a 3MF Konzorcium közös, a specifikáció továbbfejlesztésének kiindulópontjaként.

## 3MF fájlformátum - További információ

A 3MF egy XML-alapú adatformátum – ember által olvasható tömörített XML –, amely tartalmazza a 3D gyártással kapcsolatos adatok definícióit, beleértve az egyéni adatok harmadik fél általi bővíthetőségét. A 3MF fájlformátumot úgy tervezték meg, hogy szem előtt tartva a többi 3D fájlformátum korlátait és problémáit. Ez a 3MF fájlformátum megfogalmazásához vezetett, amely a következő:

* **Teljes:** Az összes szükséges modell-, anyag- és tulajdonságinformációt egyetlen archívumban tartalmazza
* **Ember által olvasható:** Általános struktúrák, például OPC, [ZIP](/hu/compression/zip/) és XML használata a fejlesztés megkönnyítése érdekében
* **Egyszerű:** Rövid, világos specifikáció, amely megkönnyíti a fejlesztést és gyorsítja az érvényesítést
* **Bővíthető:** Az XML névterek kihasználása lehetővé teszi mind a nyilvános, mind a privát bővítményeket, miközben megőrzi a kompatibilitást
* **Egyértelmű:** Az egyértelmű nyelvi és megfelelőségi tesztek biztosítják, hogy a fájl mindig konzisztens legyen a digitálistól a fizikaiig
* **Ingyenes:** A 3MF specifikációhoz való hozzáférés és annak megvalósítása jogdíjaktól, szabadalmaktól és licencektől mentes és mindig is mentes lesz

A 3MF fájlformátum specifikációi a [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) oldalon találhatók a nyilvános hozzáférés és a folyamatos frissítés érdekében. A jelenlegi közzétett verzió az 1.2.3, amely leírja az XML és más széles körben elérhető technológiák használatára vonatkozó konvenciókat egy vagy több 3D modell tartalmának és megjelenésének leírására. Azok a fejlesztők, akik 3MF fájlformátumok feldolgozására szeretnének rendszereket építeni, ezekre a specifikációkra hivatkozhatnak megvalósítási célból.

## 3MF fájlformátum specifikációi

A 3MF fájlformátum az Open Packaging specifikációit használja ZIP archívum formájában fizikai modelljéhez. Jól meghatározott részek és kapcsolatok készletét tartalmazza, amelyek a dokumentumban meghatározott célt teljesítik. Emiatt a formátum követi a csomag funkcióját, beleértve a digitális aláírásokat és bélyegképeket.

### A 3MF dokumentum – Áttekintés

Egy tipikus 3MF dokumentum a következőképpen néz ki:

![3MF Document Structure](https://raw.githubusercontent.com/3MFConsortium/spec_core/master/images/figure_2-1.png "3MF Document Structure")

A hasznos teher tartalmazza a 3D modell alkatrész feldolgozásához szükséges teljes alkatrészkészletet. A 3D hasznos adatban leírt objektumok gyártásához felhasználandó összes tartalomnak szerepelnie KELL a 3MF dokumentumban. Az egyes dokumentumrészek leírása a szükséges állapotukkal vagy opciókkal együtt a következő táblázatban található.


|**Név**|**Leírás**|**Kapcsolatforrás**|**Kötelező/Nem kötelező**
--- | --- | --- | ---
|3D modell|Egy vagy több gyártáshoz szükséges 3D objektum leírását tartalmazza.|Csomag|KÖTELEZŐ
|Core Properties|Az OPC rész, amely különféle dokumentumtulajdonságokat tartalmaz.|Csomag|OPCIONÁLIS
|Digitális aláírás eredete|Az OPC rész, amely a csomagban lévő digitális aláírások gyökere.|Csomag|OPCIONÁLIS
|Digitális aláírás|OPC-részek, amelyek mindegyike tartalmaz digitális aláírást.|Digitális aláírás eredete|OPCIONÁLIS
|Digitális aláírási tanúsítvány|OPC-részek, amelyek digitális aláírási tanúsítványt tartalmaznak.|Digitális aláírás|OPCIONÁLIS
|PrintTicket|A 3D-s modellrészben lévő 3D objektum(ok) kiadásához használandó beállításokat adja meg.|3D-modell|OPCIONÁLIS
|Miniatűr|Kis JPEG vagy PNG képet tartalmaz, amely a csomagban lévő 3D objektumokat vagy a csomag egészét ábrázolja.|Csomag|OPCIONÁLIS
|3D textúra| Olyan textúrát tartalmaz, amely a 3D-s modellrészben található 3D objektumok színének alkalmazására szolgál (kiterjesztésekhez elérhető)|3D modell|OPCIONÁLIS
|Egyéni alkatrészek|OPC-alkatrészek, amelyek metaadatokhoz vannak társítva|Csomag|OPCIONÁLIS

A [Parts and Relationships](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D modellek](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Object Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [Material Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) és a [Csomagszolgáltatások](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) szakaszai dokumentum részletes információkat ad a 3MF dokumentumról.

## Hivatkozások ##

* [3MF fájlformátum specifikációi](https://github.com/3MFConsortium/spec_core)
* [3MF – a Wikipedia által](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

