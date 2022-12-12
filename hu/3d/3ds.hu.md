{
  "date" : "2019-10-11",
  "keywords" :[ "3DS", "fájl", "formátum", "fájl típusa", "kiterjesztés", "mi az a 3DS fájl?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tudjon meg többet a 3DS fájlformátumról és az API-król, amelyek képesek megnyitni és létrehozni 3DS fájlokat.",
  "title" :"3DS fájlformátum",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a 3DS fájl?

A .3ds kiterjesztésű fájl az Autodesk 3D Studio által használt 3D Sudio (DOS) mesh fájlformátumot képviseli. Az Autodesk 3D Studio a 3D-s fájlformátumok piacán az 1990-es évek óta működik, és mára 3D Studio MAX-má fejlődött a 3D modellezés, animáció és renderelés terén. A 3DS-fájlok a jelenetek és képek 3D-s megjelenítéséhez szükséges adatokat tartalmazzák, és a 3D-s adatok importálására és exportálására szolgáló egyik legnépszerűbb fájlformátum. Figyelembe veszi az olyan információkat, mint a kamera helye, hálóadatok, világítási információk, nézetablak konfigurációk, simító csoportadatok, bittérképes hivatkozások és attribútumok csúcsok és sokszögek létrehozásához egy jelenet rendereléséhez.

## 3DS fájlformátum – További információ
Alapjában véve a 3DS egy bináris fájlformátum, és előre meghatározott struktúrát követ az adatok tárolására és visszakeresésére. A bináris fájlformátum lehetővé teszi, hogy a 3DS fájlformátum gyorsabban kisebb legyen a szövegalapú fájlformátumokhoz képest. A 3DS-fájlban lévő adatok darabok formájában tárolódnak.

### 3DS darab

A 3DS-fájlban minden egyes adatblokk egy azonosítót, a következő blokk helyére vonatkozó blokk hosszát és magát az adatot tartalmazza. A csonkazonosító lehetővé teszi a 3DS fájlformátum-olvasók számára, hogy kihagyják azokat a blokkokat, amelyeket nem ismernek fel. Ez is segít a formátum bővíthetőségében. Mindegyik darab a formákkal, a világítással és a megtekintéssel kapcsolatos információkat tárol, amelyek együttesen jelenítik meg a jelenetet. A darabok hierarchikus struktúrában vannak elrendezve egy 3DS-fájlban, és az XML-dokumentumobjektum-fához hasonlítanak.

**Csonkazonosító:** A csonk első két bájtja egy darabazonosítót jelent, amely lehetővé teszi a fájlolvasó számára, hogy eldöntse, hogy figyelembe veszi-e az olvasást, vagy kihagyja.

**A csonk hossza:** A csonk azonosítóját egy 4 bájtos egész szám követi (little-endianban), amely a csonk hosszát jelenti. Ez a hossz tartalmazza az adatok hosszát, alblokkjainak hosszát és a 6 bájtos fejlécet is.

**Hasznos terhelés:** A darab hosszát a darab tényleges adatbájtjai követik, majd az alcsonkok követik ugyanabban a hierarchikus struktúrában, amely több szintre kiterjeszthető.

### Egy darab szerkezete

Egy egyszerű darab hierarchikus felépítése a következő:

**Egy darab**

|kezdet|vége|méret|név
--- | --- | --- | ---
|0|1|2|Részletazonosító
|2|5|4|Következő darab

A darabokra egy hierarchia van érvényben, amelyet az azonosítója azonosít. A 3ds fájl elsődleges darabazonosítója 4D4Dh. Mindig ez a fájl első része. Az elsődleges darabban vannak a fő darabok.

**Fő darabok**

|id|Leírás
--- | ---
|3D3D|Az objektumháló adatok kezdete.
|B000|A kulcsképkocka adatainak kezdete.

Az ID blokk utáni Következő darab mutató a következő fődarabra mutat.
Közvetlenül egy fődarab után van egy másik darab. Ez lehet bármilyen más típusú csonk, amely a fő darabok hatókörén belül megengedett.
A Mesh leíráshoz (3D3D) ezek tetszőleges többszörösei lehetnek.

**A 3D3D részegységei – Mesh Block**


|id|Leírás
--- | ---
|1100|ismeretlen
|1200|Háttérszín.
|1201|ismeretlen
|1300|ismeretlen
|1400|ismeretlen
|1420|ismeretlen
|1450|ismeretlen
|1500|ismeretlen
|2100|Ambient Color Block
|2200|köd?
|2201|köd?
|2210|köd?
|2300|ismeretlen
|3000|ismeretlen
|4000|Objektumblokk
|7001|ismeretlen
|AFFF|ismeretlen

**4000-es részegységek – Objektumleíró blokk**
A Subchunk 4000 első eleme az objektumok nevének ASCIIZ-karakterlánca.
Ne feledje, hogy egy tárgy lehet háló, lámpa vagy kamera.

|id|Leírás
--- | ---
|4010|ismeretlen
|4012|árnyék?
|4100|Háromszög alakú sokszög objektum
|4600|Fény
|4700|Fényképezőgép

## Hivatkozások

* [Geometriai fájlformátumok – Autodesk](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2015/ENU/3DSMax/files/GUID-566E59EE-8221-4AC6 -824B-5062C5AE0B32-htm.html)
* [3DS – Wikipedia](https://en.wikipedia.org/wiki/.3ds)

