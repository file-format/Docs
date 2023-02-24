{
  "date" : "2021-04-16",
  "keywords" :[ "XML", "P6XML", "File", "Extension", "File Format", "Project", "Management", "Primavera", "P6"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P6XML – Primavera P6 Project",
  "description":"További információ a P6XML fájlformátumról és az API-król, amelyek P6XML fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "P6XML",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## Mi az a P6XML fájl? ##

A P6XML fájlkiterjesztés kiváló olvashatósággal, alkalmazkodóképességgel és széleskörű felhasználási lehetőséggel rendelkezik, ami ideális formátummá teszi. A Primavera P6 Professional rendelkezik a [XER](/hu/project-management/xer/) és az XML fájlok exportálására és importálására is. Az XML az **Extensible Markup Language** rövidítése. Ez az általános formátum lehetővé teszi a felhasználók számára a projektinformációk megosztását a Primavera P6 adatbázisok között. A projekt adatai könnyen tárolhatók szöveges fájlban az XML fájlon keresztül; ez számos szoftver számára egyszerűbbé teszi az adatcserét. Az ilyen adatokat a Primavera P6 felhasználó könnyen megoszthatja és kezelheti.

## A P6XML fájlformátum előnyei ##

* A Primavera felhasználók könnyen meghatározhatják, hogy mely alapvonalakat exportálja és importálja az XML fájl segítségével
* Az XML export tartalmazhatja az összes projekt részletes cselekvési tervet
* A Primavera 6-ot használó olyan felhasználók, akik nem tudnak szerkeszteni, hozzáadni vagy törölni bizonyos globális adatelemeket, például tevékenységkódokat, naptárakat és erőforrásokat, nem tudják azokat importálni.
* A Primavera által használt általános és projektbiztonsági profil beállításain túlmenően az adatbázisban lévő adatokat befolyásoló vagy módosító adatelemek nem kerülnek importálásra

## XML-fájl exportálása a Primavera P6-ból ##

A P6 Professional projektek és projektadatok P6XML-fájlba exportálásához használja az Oracle Primavera Cloud szolgáltatást. A fájl létrehozása közben letöltheti a P6 Professional asztali alkalmazásból, és importálhatja a Primavera Cloudba. Az exportálási folyamat megszakítás nélküli működtetése előtt szabályoznia kell, hogy P6 Professional adatbázishoz vagy P6 EPPM-hez van-e kapcsolva. Az exportálási folyamat egyes funkciói az adatbázistól függően eltérőek lehetnek. A P6 Specialized beállításokkal és egy P6 Proficient adatbázissal az exportálási folyamat helyileg működik a rendszeren. A P6 Professional adatbázissal könnyedén exportálhatja és megnyithatja a P6 XML fájlt a rendszer beállításaiból.

Íme néhány lépés az exportálási folyamat leírásához:

* Nyitott vágyak Primavera P6 projekt
* Ezután válassza az Exportálás lehetőséget a Fájl lapon
* Válassza a „Primavera P6 – (XML)” lehetőséget. Ezt követően kattintson a Tovább gombra
* Kattintson duplán az exportálni kívánt projektre
* Válassza ki annak az elérési útnak a csonkolásait, ahová az exportált fájlt el szeretné helyezni, majd válassza a „Befejezés” lehetőséget.
* Válassza ki a fájl mentési módját
* Ha az exportfájlban nincs szükség projektszintű elrendezésekre, feltétlenül törölje az "Összes projektszintű elrendezés exportálása" beállítást.
* Válassza a Befejezést, és akkor kap egy visszaigazolást az XML exportálásról

### Fontos tippek ###

* Amikor csatlakozik egy P6 EPPM adatbázishoz, az adminisztrátornak át kell adnia a tartalomforrás URL-jét a P6 alkalmazásbeállítások általános oldalán lévő P6 URL mezőbe.
* Kényelmes több projekt exportálása egyetlen XML-fájlba
* A projekthez hozzárendelt globális adatok exportálásra kerülnek
* Kényelmes XML-fájlok exportálása anélkül, hogy minden erőforráshoz hozzáférne

## Problémái vannak a P6XML fájl megnyitásakor? ##

A következő néhány gyakori probléma, amely a P6XML formátum hibás működését okozhatja:

* A támogató szoftver hiánya
* Sérült fájl
* Fertőzött fájl vírus miatt
* A P6XML leírás véletlenül törölve a Windows rendszerleíró adatbázisból
* Nincs hozzáférési jog a rendszerben a fájlok megnyitásához
* Elavult meghajtó a rendszerben
* A fájl kiterjesztése átnevezve

## Referenciák ##

* [Oracle – P6 XML](https://docs.oracle.com/cd/E80480_01/English/admin/p6_import_guide/index.html)
