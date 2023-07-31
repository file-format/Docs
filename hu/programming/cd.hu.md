{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd", "mi az a cd fájl", "hogyan kell megnyitni a cd fájlt", "kiterjesztés", "fájl", "cd fájl", "cd fájl formátum", "cd fájl kiterjesztése" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - Visual Studio osztálydiagram fájl",
  "description":"További információ a CD-fájlformátumról és az API-król, amelyek CD-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## Mi az a CD-fájl?

A .cd kiterjesztésű fájl egy Visual Studio osztálydiagram-fájlja, amely információkat nyújt a jelenlegi megoldás összes osztályának szerkezetéről és kapcsolatáról. A Visual Studio-megoldás (amelyet a [.sln](/hu/programming/sln/) jelképez) tartalmazhat egy vagy több projektet, amelyek mindegyikének több különböző osztálya van. Az osztálydiagram fájl a projektre jobb gombbal kattintva, és az osztálydiagram opció kiválasztásával hozható létre.

## Osztálydiagram (.cd) fájlformátum - További információ

Az osztálydiagram-fájl szabványos XML-fájlformátumban kerül mentésre, amely XML-csomópontként jeleníti meg a projekt osztályait. Ha a Visual Studio nem érhető el, ezek az osztálydiagram-fájlok bármely olyan alkalmazásban megnyithatók, amely támogatja az XML-fájlok megnyitását.

### Osztálydiagramok hozzáadása a Visual Studio Projecthez

A Visual Studióban nyissa meg azt a megoldást/projektet, amelyhez hozzá szeretné adni az osztálydiagramot. Ezután kattintson a jobb gombbal a projektcsomópontra, majd válassza a Hozzáadás > Új elem parancsot. Vagy nyomja meg a Ctrl+Shift+A billentyűket.

* Megnyílik az Új elem hozzáadása párbeszédpanel.

* Bontsa ki a Common Items > General elemet, majd válassza az Osztálydiagram lehetőséget a sablonlistából. Visual C++ projektek esetén a Segédprogram kategóriában keresse meg az Osztálydiagram sablont.

### Osztálydiagramok (CD) exportálása képekbe

A Visual Studio lehetővé teszi az osztálydiagramok konvertálását/exportálását olyan képekké, mint a [PNG](/hu/image/png/), [JPEG](/hu/image/jpeg/) és [BMP](/hu/image/bmp/). Ezek az exportált osztálydiagram-fájlok dokumentációs és műszaki adatcsomag (TDP) nyilvántartási célokra használhatók. Az osztálydiagram képpé konvertálásához a következő lépéseket lehet végrehajtani a Microsoft Visual Studio alkalmazásból.

1. Nyissa meg az osztálydiagram (.cd) fájlt.
1. Az Osztálydiagram menüből vagy a diagramfelület helyi menüjéből válassza a Diagram exportálása képként lehetőséget.
1. Válasszon ki egy diagramot.
1. Válassza ki a kívánt formátumot.
1. Az exportálás befejezéséhez válassza az Exportálás lehetőséget.

## Hivatkozások

* [Tervezési osztályok a Visual Studioban](https://learn.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)

