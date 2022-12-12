{
  "date" : "2021-04-22",
  "keywords": [ "aps file", "visual studio aps file", "extension", "format","aps file visual studio","aps file extension","how to open aps file","APS file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APS - Visual C++ Resource File",
  "description":"Tudjon meg többet az APS fájlformátumról az APS példával és az API-kkal, amelyek APS fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "APS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Mi az APS fájlformátum?
Az APS fájlt a Visual C++, a Microsoft szoftverfejlesztő alkalmazása hozza létre. Elmenti a projektbe beépített erőforrás bináris ábrázolását, és lehetővé teszi az alkalmazás számára az erőforrások gyorsabb betöltését. Könnyen megtalálhatja ezeket a fájlokat .aps kiterjesztéssel. Valójában az erőforrás-szerkesztők nem olvassák be közvetlenül a resource.h fájlokat, ezért az erőforrás-fordító .aps fájlokká fordítja azokat, amelyeket az erőforrás-szerkesztők használnak fel.

## APS fájlformátum
Az APS fájlformátum csak egy fordítási lépés, és csak szimbolikus adatokat tárol. A nem szimbolikus információkat, például a megjegyzéseket, a rendszer elveti a fordítási folyamat során. Például a Mentés során az erőforrás-szerkesztő felülírja az erőforrás-parancsfájlt és a resource.h fájlt. Az erőforrások minden módosítása az erőforrás-parancsfájlban marad, de a megjegyzések mindig elvesznek, ha az erőforrás-parancsfájlt felülírják.


## Hivatkozások

* [Resource Files (C++)](https://docs.microsoft.com/en-us/cpp/windows/resource-files-visual-studio?view=msvc-160)
 


