{
  "date" : "2021-06-24",
  "keywords": [ "GADGET file", "what is a gadget file", "extension", "format", "what is a GADGET file", "archive" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"További információ a GADGET fájlformátumról és az API-król, amelyek GADGET fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"GADGET - Virtuális CD-fájl",
  "linktitle" : "GADGET",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-06-24"
}

## Mi az a GADGET fájl?

A GADGET-fájl egy kis szoftverprogramból áll, amely a Windows Vista vagy a Windows 7 oldalsávján fut. Több webalapú fájlt tömörít, és a fájlok tartalmazhatnak [.html](/hu/web/html/), [.css](/hu/web/css/) vagy [.js](/hu/web/js/) fájlokat, valamint egyéb webes fájlok. A GADGET-fájlok kis komponensekhez, például keresőeszközökhöz, hírfolyamokhoz, rendszer-segédprogramokhoz és kis játékokhoz használhatók. Bár a modulokat az oldalsáv tárolja, nem jellemzőek az oldalsáv területére; ezek leválaszthatók és tetszés szerint áthelyezhetők az asztalra.

## GADGET fájlformátum

A GADGET fájl egy átnevezett [ZIP](/hu/compression/zip/) archívum, amely HTML, XML, JScript és CSS (Cascading Style Sheets) fájlok gyűjteményét tartalmazza. A telepítés magában foglalja a .gadget fájl letöltését és a letöltési folyamat engedélyezését az összetevő telepítéséhez, vagy a .gadget fájl mentését a helyi rendszerbe, és a telepítési folyamat elindításához kattintson duplán.

Alapvetően egy GADGET két fájlt tartalmaz:

1. **Gadget.xml**: A jegyzék, egy XML-fájl, amely a gadget általános bemutatását és konfigurációs információit tartalmazza.
2. **name.html**: Egy HTML fájl, amelyben a név a<name> címkéje a társított gadget jegyzékben, amely megadja a modul felhasználói felületének burkolóját, és tartalmazza a gadget alapvető funkcióit.

Egy GADGET-fájl több példánya is futtatható egyidejűleg. Például, ha valaki tudni szeretné az időt a különböző időzónákban, akkor az óra modul több példányát is futtathatja úgy, hogy minden órát egy adott időzónára állít.

### A GADGET megszűnése

Mivel a Windows Sidebar platform a Windows 7 rendszerben komoly biztonsági réseket tartalmaz, a modulok már nem érhetők el a Microsoft hivatalos webhelyén. Később a Microsoft megszüntette ezt a funkciót a Windows újabb kiadásaiban. A GADGET bármikor kihasználható a számítógép fájljaihoz való hozzáférésre, a számítógép károsodására, a kifogásolható tartalom felfedésére vagy a viselkedés megváltoztatására.

## Hivatkozások

* [Windows oldalsáv – a Microsofttól](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-entry)
* [Gadget fejlesztése Windows oldalsávhoz, 1. rész](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-overview-gdo)

