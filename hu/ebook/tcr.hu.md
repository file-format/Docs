{
  "date" : "2021-03-09",
  "keywords" :[ "TCR", "Psion", "extension", "format", "eBook" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a Psion 3 sorozat TCR fájlformátumáról és az API-król, amelyek tcr fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"TCR - Psion Series 3 eBook File",
  "linktitle" : "TCR",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-09"
}

## Mi az a TCR fájl?

A 90-es évek elején a TCR fájlformátumot vezették be az ősi **Psion Series 3** tenyérgépekhez. A vállalat a platform-specifikus tömörítést használta, és ez a formátum nagyon korlátozott mértékben támogatja a szövegformázást. Ez egy ZVR alapú fájlformátum, és viszonylag jobb tömörítési arányt biztosít, mint a PalmDOC. A FontMachine-nal is nagyon jól működik. Bár a TCR fájlformátum egy megszűnt eszközhöz tartozik, ez a fájlformátum mégis olvasható néhány e-olvasóval. Ez a fájlformátum asztalon is megtekinthető a Sumatra PDF-ben és a Caliber alkalmazással Windows és Linux rendszeren.

## Műszaki információk

Mivel a TCR fájlformátum egy ZVR tömörítőn alapul, amely képes sok fájlt az eredeti méretük körülbelül 50%-ával csökkenteni. Az over által használt tömörítési séma egy kicsit régi. A tömörített fájl a 256 lehetséges szimbólum szótárával kezdődik, amelyek megjelenhetnek a tömörített fájlban. A szótár minden egyes szimbólumhoz tartalmaz egy rögzített alternatív karakterláncot. A kicsomagolás még OPL-ben is nagyon gyors lett, és a tömörített fájl bármely pontján megkezdődhet.

## Problémák a TCR fájl megnyitásakor ##

Ha nem tudja megnyitni és futtatni a TCR fájlt; ez nem jelenti azt, hogy nincs megfelelő szoftver telepítve a készülékére. Más problémák is akadályozhatják a fájl megfelelő működését. A lehetséges problémák a következők lehetnek:

- A TCR fájl megsérülése.
- Hibás hivatkozások a TCR fájlra a rendszerleíró bejegyzésekben.
- A TCR leírása törölve a Windows rendszerleíró adatbázisából
- A TCR formátumot támogató alkalmazás hibás telepítése
- Egy fertőzött TCR-fájl nemkívánatos kártevőkkel.
- A számítógép nem rendelkezik elegendő hardvererőforrással a TCR fájl működtetéséhez.
- A számítógép által a TCR fájl megnyitásához használt illesztőprogramok elavultak.




## Hivatkozások

* [TCR – MobileRead](https://wiki.mobileread.com/wiki/TCR)
* [ZVR tömörített szövegfájl-olvasó](https://iay.org.uk/zvr/)

