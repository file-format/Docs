{
  "date" : "2021-06-30",
  "keywords" :[ "exe fájl", "exe fájl formátum", "mi az exe fájl", "fájl", "exe példa", "exe fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Az .exe fájl egy Microsoft végrehajtható fájl, amely Windows operációs rendszeren fut. Tudjon meg többet az EXE fájlformátumról.",
  "title" :"What is an Executable EXE file?",
  "linktitle" : "EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Mi az EXE fájl?

Az EXE szó a **végrehajtás** rövidítése. Az .exe fájl egy olyan program, amely Microsoft Windows operációs rendszeren futtatható. Az alkalmazásfejlesztők a Windows operációs rendszerre szánt programjaikat többnyire futtatható formátumban teszik közzé exe fájlként. Ez a szabványos fájlformátum az alkalmazások Windows rendszeren történő futtatásához. A **Setup.exe**, **Install.exe** és **cmd.exe** az EXE-fájlok néhány gyakori és jól ismert neve.

## EXE fájl formátum

Az MS-DOS fordítókat a 64K memóriakorlátozással rendelkező memóriamodellekkel vezették be. Az általános koncepció az, hogy az x86 CPU-ban különböző szegmensregisztereket állítanak be (CS, DS, ES, SS), hogy a különböző vagy azonos szegmensekre mutassanak, ezáltal lehetővé téve a memória különböző fokú hozzáférését. Néhány speciális memóriamodell a következő volt:

- **Apró**: Minden memória-hozzáférés 16 bites (a szegmensregiszterek változatlanok). .COM fájlt hoz létre .EXE fájl helyett.
- **Kicsi**: Minden memória-hozzáférés 16 bites (a szegmensregiszterek változatlanok).
- **Kompakt**: Az adatcímek tartalmazzák a szegmenst és az eltolást is, újratöltve a DS vagy ES regisztereket hozzáféréskor, és akár 1 millió adatot is lehetővé tesznek. A kódelérések nem változtatják meg a CS-regisztert, 64K kódot tesznek lehetővé.
- **Közepes**: A kódcímek tartalmazzák a szegmens címét, a CS újratöltését hozzáféréskor és legfeljebb 1 millió kódot. Az adathozzáférések nem változtatják meg a DS és ES regisztereket, így 64 KB adatot tesz lehetővé.
- **Nagy**: Mind a kód-, mind az adatcímek (szegmens, eltolás) párok, mindig újratöltik a szegmenscímeket. A teljes 1M bájtos memóriaterület mind a kód, mind az adatok számára elérhető.
- **Huge**: Ugyanaz, mint a nagy modellnél, a fordító által generált további aritmetika lehetővé teszi a 64K-nál nagyobb tömbök elérését.

A fejlesztőknek kell eldönteniük, hogy melyik modellt válasszák az exe fájl létrehozásakor.

### Hordozható EXE fájlformátum

A hordozható végrehajtható fájlformátum (PE) számos információs fejlécet tartalmaz, a fejlécek listája a következő:

- **DOS fejléc**: Az MS-DOS fejléc biztosítja a visszafelé kompatibilitást vagy az új fájltípusok kecses visszaszorítását.
- **PE fejléc**: A DOS fejléc elejétől számított 60-as eltolásnál (0x3C) egy mutató a PE fájl fejlécére
- **COFF fejléc**: A COFF fejléc tartalmaz néhány olyan információt, amely egy végrehajtható fájl számára hasznos, és néhány olyan információ, amely hasznosabb egy objektumfájl számára.
- **PE opcionális fejléc**: A PE opcionális fejléc közvetlenül a COFF fejléc után jelenik meg, és egyes források a két fejlécet is ugyanannak a szerkezetnek a részeként jelenítik meg.
- **Section Table**: Közvetlenül a PE opcionális fejléc után találunk egy szakasztáblázatot. A szakasztábla IMAGE_SECTION_HEADER struktúrák tömbjéből áll.
- **Leképezhető szakaszok**: Helyet takaríthat meg a memóriában, ha egy könyvtár kódját egynél több folyamathoz rendeli hozzá.

## Futtathat EXE fájlt Mac-en?

Az exe fájlokat nem használják végrehajtható fájlokként Mac OS rendszeren. Ha azonban exe fájlt szeretne futtatni Mac OS rendszeren, a következő módszerek használhatók.

1. **Wine** – A Wine tökéletes megoldás azoknak, akik PC-s alkalmazásaikat Mac rendszeren szeretnék használni. Ez egy mozaikszó, ami a „Wine Is Not A Emulator” kifejezést jelenti. A Wine ugyanazt a könyvtárkörnyezetet hozza létre, mint amit a Microsoft használ, így futtathatja a Windows-alkalmazást.
2. **Virtuális gépek** – Hozzon létre egy Windows virtuális gépet a Parallel Desktop vagy a VM Virtual Box használatával, és futtassa az alkalmazást a virtuális gépen belül.
3. **Boot Camp** – A Windows Boot Camp telepítése és konfigurálása Mac OS rendszeren lehetővé teszi a Windows operációs rendszer futtatását Mac gépen.

## Hivatkozások

* [.exe- a Wikipewdia által](https://en.wikipedia.org/wiki/.exe)
* [x86 Disassembly/Windows végrehajtható fájlok](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

