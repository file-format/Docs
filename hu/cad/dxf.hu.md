{
  "date" : "2020-03-16",
  "keywords" :[ "DXF fájl", "Fájlformátum", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a DXF fájlformátumról és az API-król, amelyek DXF fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"DXF fájlformátum",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a DXF fájl?

A DXF, Drawing Interchange Format vagy Drawing Exchange Format az AutoCAD rajzfájl címkézett adatábrázolása. A fájl minden eleméhez tartozik egy egész szám előtag, amelyet csoportkódnak neveznek. Ez a csoportkód valójában az azt követő elemet képviseli, és egy adatelem jelentését jelzi egy adott objektumtípushoz. A DXF lehetővé teszi szinte az összes felhasználó által megadott információ megjelenítését egy rajzfájlban.

A DXF fájlformátumot az Autodesk fejlesztette ki CAD adatfájl formátumként az AutoCAD és más alkalmazások közötti adat-interoperabilitás érdekében. Így az adatok más formátumokból importálhatók DXF-be az AutoCAD-be, a DXF fájlformátum együttműködési specifikációi szerint.

## Rövid története ##


A DXF fájlformátum története 1982-ig nyúlik vissza, amikor az AutoCAD 1.0 részeként bemutatták. Az AutoCAD kezdeti verziói csak a DXF ASCII fájlformátumát támogatják. Az AutoCAD (és újabb) 1988-as kiadásával az ASCII és a bináris DXF fájlformátumok támogatása is megjelent az AutoCAD-ben. A korábbi szakaszokban az Autodesk nem osztott meg semmilyen fájlformátum-specifikációt, ezért a DXF-fájlok helyes importálása nem volt egyszerű. Az Autodesk azonban most közzéteszi a DXF specifikációit, és elérhető a nagyközönség számára.

## Fájlformátum specifikációi ##

A DXF fájlformátum a csoportkód- és értékpárokat használja a tartalom szakaszokba rendezéséhez. Minden szakasz rekordokból áll, ahol minden rekord egy csoportkódból és egy adatelemből áll. Minden csoportkód és érték a saját sorában található a DXF fájlban. Minden szakasz egy 0 csoportkóddal kezdődik, amelyet a SECTION karakterlánc követ. Ezt követi egy 2-es csoportkód és egy karakterlánc, amely a szakasz nevét jelzi (például SECTION1). Minden szakasz csoportkódokból és értékekből áll, amelyek meghatározzák az elemeit. A szakasz 0-ra, majd az ENDSEC karakterláncra végződik.

A DXF fájlformátum az entitásoktól eltérő objektumokat veszi figyelembe. Az objektumoknak itt nincs grafikus ábrázolása, de az entitásoknak igen. Így a DXF bejegyzéseit grafikus objektumoknak nevezzük, míg az objektumobjektumokat nem grafikus objektumoknak nevezzük. A DXF fájl BLOCK és ENTITIES szakaszai entitásokat tartalmaznak, és a csoportkódok használata ebben a két részben azonos. Egy entitás végét a következő 0 csoport jelzi, amely a következő entitást kezdi, vagy a szakasz végét jelzi.

### Fájlszerkezet ###

A DXF fájl szakaszai a következő sorrendben vannak elrendezve:

|Szakasz|Alapleírás
---|---|
|Header|Ez a szakasz általános információkat tartalmaz a rajzról. Ez olyan, mint a telefon Beállítások funkciója, amely a rajzhoz és a hozzá tartozó értékekhez tartozó különböző változókat tartalmazza. Például a Fejléc szakasz meghatározza, hogy a DXF fájl melyik AutoCAD verziót használja (a $ACADVER változó), vagy a fájl szögeinek mérésére használt mértékegységet (a $AUNITS változó)
|Osztályok|Az OSZTÁLYOK szakasz az alkalmazás által definiált osztályok információit tartalmazza, amelyek példányai az adatbázis BLOCKS, ENTITIES és OBJECTS szakaszaiban jelennek meg.
|Táblázatok|Ez a szakasz több különböző táblázat definícióit tartalmazza, amelyek mindegyike számos különböző szimbólumbejegyzést tartalmaz. Például a [sortípus](https://help.autodesk.com/view/ACD/2016/ENU/?guid=GUID-20B4D4B3-1220-426A-847B-5BBE36EC6FDF) táblázat (LTYPE) meghatározza a kötőjelek, pontok, szövegek és szimbólumok mintáját a DXF fájlban, valamint azok méretezését. Íme az ebben a részben található táblázatok teljes listája:<ul><li> Alkalmazásazonosító (APPID) táblázat</li><li> Block Record (BLOCK_RECORD) tábla</li><li> Méretstílus (DIMSTYPE) táblázat</li><li> Réteg (LAYER) táblázat</li><li> Vonaltípus (LTYPE) táblázat</li><li> Szövegstílus (STYLE) táblázat</li><li> Felhasználói koordinátarendszer (UCS) táblázat</li><li> Táblázat megtekintése (VIEW).</li><li> Viewport konfigurációs (VPORT) táblázat</li></ul>
|Blocks|Ez a szakasz azokat a grafikus objektumokat és rajzi entitásokat tartalmazza, amelyek a rajzban minden blokkreferenciát alkotnak.
|Entitások|Ez a szakasz a rajz tényleges objektumait és grafikus entitásait tartalmazza. Ez tartalmazhat nyers adatokat – például egy kör entitást a vastagsága, a középpontja, a sugara és a kihúzási iránya határoz meg.
|Objektumok|Itt a rajz nem grafikus részeit találja. Például az AutoCAD szótárak vannak itt tárolva.

## Hivatkozások ##

* [DXF-fájlspecifikációk](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF by Wikipedia](https://en.wikipedia.org/wiki/AutoCAD_DXF)

