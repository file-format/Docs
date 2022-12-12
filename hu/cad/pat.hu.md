{
  "date" : "2020-03-16",
  "keywords" :[ "PAT File", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a PAT fájlformátumról és az API-król, amelyek PAT fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"PAT fájlformátum",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## Mi az a PAT fájl?

A .pat kiterjesztésű fájl egy CAD-fájl, amelyet az AutoCAD szoftver használ. Azok az alkalmazások, amelyek képesek megnyitni a PAT fájlokat, az ezekben a fájlokban tárolt sraffozási mintákat használják, információkat kapnak egy terület textúrájáról/kitöltéséről. A benne található minták információt adnak az anyag megjelenéséről a rajzolt tárgyakon. A PAT fájlok megnyithatók olyan alkalmazásokban, mint az Autodesk AutoCAD, a CorelDRAW Graphics Suite és a Ketron Software. A PAT fájlok különböző képformátumokká konvertálhatók, például JPG, PNG, BMP stb.

## PAT fájlformátum

A PAT fájlok egyszerű szöveges formátumban készülnek, és bármely szövegszerkesztőben megnyithatók. Ezekben a fájlokban a sraffozási minták vektoralapúak, és az AutoCAD dokumentációjában felvázolt szintaxist követik.

Minden minta a 0,0 ponttól kezdődik, a minta úgy van kiszámítva, hogy lefedje a sraffozási határt.

### Mintadefiníció

Minden mintadefiníció a következő mezőket tartalmazza:
* Egy kezdő "\*"
* Név – A név nem tartalmazhat szóközt, írásjelet, zárójelet vagy perjelet.
* Egy leírás

A sraffozási minták szabványos formátuma a `<\*><name> <, leírás>`. A név és a leírás vesszővel van elválasztva, és a leírások nem haladhatják meg a nyolcvan karakteres sor hosszúságát. A sraffozási minták ezen információk után kerülnek meghatározásra.

### Sraffozási minta példák
Az alábbiakban egy négyzet alakú minta látható
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Egy másik példa a paralelogramma mintázatára a következő.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Referenciák ##

* [Hash Patterns by Autodesk](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/AutoCAD-LT/files/GUID-A6F2E6FF-1717- 44B6-A476-0CA817ADD77E-htm.html)

