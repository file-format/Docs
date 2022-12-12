{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "file", "extension", "file format", "Microsoft Excel Macro File", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"A fájlformátum útmutatója, hogy megtudja, mi az XLM Makró fájl és API-k, amelyek XLM fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"What is an XLM file?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Mi az XLM fájl?

Az XLM az Excel makróhoz a makrók tárolására használt táblázatkezelő fájlok egy típusa. Alkalmazási szempontból a makró a folyamatok automatizálására használt utasítások halmaza. A makró rögzíti az [XLS](/hu/spreadsheet/xls/) fájlformátum esetén ismételten végrehajtott lépéseket, és megkönnyíti a műveletek végrehajtását a makró újbóli futtatásával. A makrók a Microsoft Visual Basic for Applications (VBA) programmal programozhatók az Excel-munkafüzetből a Visual Basic Editor segítségével, és onnan közvetlenül futtathatók/hibakereshetők.

## Rövid története ##

A Microsoft Excel az első nyilvános bevezetése óta támogatja a makrók programozását. A makrók jellemzői változatlanok maradtak az Excel későbbi verzióiban, az új funkcióknak megfelelő kiterjesztéssel. Az XLM volt az Excel alapértelmezett makrónyelve az Excel 4.0-n keresztül. Az Excel 5.0 alapértelmezés szerint VBA-ban rögzítette a makrókat, de az 5.0-s verzióban az XLM-rögzítés továbbra is engedélyezett volt. Az 5.0-s verzió után ez a lehetőség megszűnt. Az Excel összes verziója, beleértve az Excel 2010-et is, képes XLM-makró futtatására, bár a Microsoft nem támogatja ezek használatát.

## Makró rögzítése XLM-ben ##

Az Excel könnyen használható lépéseket kínál a makró rögzítéséhez. A makrók használatához telepített fejlesztői eszközök szükségesek. Amint egy makrórögzítés folyamatban van, minden felhasználói műveletet rögzít a későbbi lejátszáshoz. A makrórögzítés valójában magában foglalja az összes lépést, amelyet a felhasználó a rögzítés megkezdése után végrehajt. Így, ha egy cella tartalmát félkövérre, dőltre szedi, és a szöveg igazítását a makrórögzítés elindítása után állítja be, akkor az összes parancs rögzítésre kerül. Minden rögzített makróhoz hozzá lehet rendelni egy parancsikont is a későbbi gyors lejátszáshoz. A makrórögzítés VBA-kódot generál makró formájában, amely a Visual Basic Editor (VBE) segítségével szerkeszthető.

## Excel objektummodell ##

A makrók hátul VBA-rutinokat használnak, és ehhez az [Excel-objektummodellt] (https://docs.microsoft.com/en-us/office/vba/api/overview/excel/object-model) követik. Ez a modell azonosítja a táblázat objektumait a táblázattal való interakcióhoz a felhasználó által definiált parancseszköztárak, parancssorok vagy üzenetmezők segítségével. Például a munkafüzet tulajdonságaihoz a munkafüzet objektum hozzáférést biztosít. Ehhez hasonlóan a modellben található egy Munkalap objektum, amely programozottan dolgozik a munkafüzet munkalapjaival.

## Makrók és biztonság ##

A VBA hozzáférést biztosít minden alkalmazási területhez, valamint a fájlrendszerhez, és veszélyes is lehet. Ez aggályokat vet fel, amikor a munkafüzetet megosztja valakivel, aki a végén futtatni tudja a fájlt. Vagyis a Microsoft Excel figyelmeztet egy ilyen fájl megnyitására. A makrók hitelesíthetők digitális aláírással annak érdekében, hogy a többi felhasználó ellenőrizhesse azok megbízhatóságát. Így a makrók a forrásuk ellenőrzése után engedélyezhetők.

## Referenciák ##

* [[MS-XLS] – Excel bináris fájlformátum-struktúra](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Makróprogramozás](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

