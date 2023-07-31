{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az ACCDT fájlformátumról és az API-król, amelyek ACCDT-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"ACCDT – Microsoft Access 2007 sablonadatbázis fájlformátum",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Mi az ACCDT fájl?

Az .accdt kiterjesztésű fájl egy Microsoft Access adatbázissablonfájl, amely előre meghatározott adatbáziselemeket tartalmaz. Ezek az elemek olyan struktúrák gyűjteményét alkotják, amelyek adatbázis-alkalmazásokat határoznak meg, mint például az adatok tárolására szolgáló adatbázissémák, az adatok nézeteinek elrendezési leírása és az adatbázist leíró metaadatok. Az ACCDT fájlok sablonfájlokként használhatók adatbázisok létrehozására az ezekben elérhető sablonbeállítások alapján. Az eredményül kapott adatbázisfájlokat a rendszer [ACCDB](/hu/database/accdb/) fájlként menti, és táblázatokban tölti fel adatokkal. A Microsoft Access 2007 és újabb verziói képesek megnyitni az ACCDT fájlokat.

## ACCDT fájlformátum

Az ACDT sablonfájlok az Office Open XML specifikációin alapulnak, és az összes adatot a ZIP-csomag tartalmazza. Az adatbázis szerkezeti és tartalmi információit az [XML](/hu/web/xml/) fájlok és szövegfájlok tartalmazzák, és kapcsolatokon keresztül kapcsolódnak egymáshoz. Átnevezhet egy ACCDT-fájlt [.zip](/hu/compression/zip/) kiterjesztésre, és bármilyen tömörítő szoftverrel kibonthatja a ZIP-archívum tartalmát.

### Fájlszerkezet

Az ACDT fájlok olyan csomagok, amelyek kapcsolódó részek gyűjteményét tartalmazzák. Mindegyik **rész** egy XML, szöveges és bináris formátumú adatbázis-alkalmazás tartalmáról tárol információkat, beleértve:

* Adatbázis objektumok
* Kapcsolódó metaadatok
* A csomag felépítése

#### Csomag

A csomag egy [ZIP](/hu/compression/zip/) archívum, amely több részből áll, és megfelel az [ISO/IEC-29500-2] dokumentumban (https://www.iso.org/standard/51459.html). Az ACDT-fájloknak tartalmazniuk kell legalább egy sablon metadaa részt, amely egy kapcsolat célpontja lehet. Ez a sablon metaadat az ACCDT fájl kezdő része.

#### Rész

A rész egy bájtfolyam, amelyhez társított típus tartozik a benne tárolt tartalom jellegének és típusának meghatározásához. Az alkatrészek felsorolása meghatározza az érvényes részeket, az érvényes tartalomtípusokat és a szükséges kapcsolatokat a csomag összes része között.

#### Kapcsolat

"Csomag kapcsolat" - ahol a cél egy rész, a forrás pedig a csomag mint egész.

"Part-to-Part Relationship" - ahol a cél egy része, a forrás pedig egy része a csomagban.

"Kifejezett kapcsolat" – ahol egy erőforrásra a forrásrész tartalmából hivatkoznak azáltal, hogy egy kapcsolatelemre hivatkoznak az azonosító attribútuma értékével.

„Közvetített kapcsolat” – olyan kapcsolat, amely nem explicit.

`Belső kapcsolat` – ahol a cél a csomag része.

"Külső kapcsolat" - ahol a cél egy külső erőforrás, amely nem szerepel a csomagban.

## Hivatkozások ##

* [Hozzáférési sablon fájlformátuma](https://learn.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

