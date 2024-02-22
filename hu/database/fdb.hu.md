{
  "date" : "2023-01-18",
  "keywords" : [ "FDB", "what is a FDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Ismerje meg az FDB fájlformátumot és az API-kat, amelyek FDB fájlokat hozhatnak létre és nyithatnak meg.",
  "title" : "FDB fájlformátum - Microsoft Dynamics NAV adatbázisfájl",
  "linktitle" : "FDB",
  "menu" : {
    "docs" : {
      "identifier":"database-fdb-hu",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-18"
}

## Mi az FDB fájl?

Az .fdb fájl a Microsoft Dynamics NAV adatbázisfájljaihoz használt fájlkiterjesztés. Az .fdb fájlkiterjesztés a Firebird Database File” rövidítése, és ez a Firebird Database Management System által használt fájlformátum, amely a Microsoft Dynamics NAV által használt adatbázis-motor. Az .fdb fájl tartalmazza a NAV rendszer összes adatát, tábláját, struktúráját, beleértve a pénzügyi adatokat, a készletadatokat, az ügyfelek adatait stb. Fontos, hogy biztonsági másolatot készítsen az .fdb fájlról, hogy biztosítsa az adatok sértetlenségét, és bármilyen probléma esetén helyre tudja állítani az adatokat. Az .fdb fájl exportálható, importálható és replikációban is használható.

## Kapcsolat a Microsoft Dynamics NAV-val

Az FDB-fájlok adatbázis-fájlok a Microsoft Dynamics NAV-ban. A Microsoft Dynamics NAV a Microsoft által fejlesztett vállalati erőforrás-tervező (ERP) szoftver. Kis- és középvállalkozások számára készült, és az üzleti menedzsment funkciók széles skáláját kínálja, beleértve a pénzügyi menedzsmentet, az ellátási lánc menedzsmentet, a gyártást, a projektmenedzsmentet és még sok mást. A Microsoft Dynamics platformra épül, és teljes mértékben integrálva van más Microsoft-termékekkel, mint például az Office és az Outlook. A Dynamics NAV webes kliensen, valamint Windows kliensen keresztül érhető el, valamint saját C/AL nevű fejlesztőkörnyezet segítségével testre szabható és integrálható más rendszerekkel. Általában a gyártó, a nagykereskedelmi forgalmazás és a szolgáltató iparágakban működő vállalatok használják.

## .fdb fájl - Mivel nyitható meg egy .fdb fájl?

Az FDB fájlt általában a Microsoft Dynamics NAV fejlesztői környezet vagy a Microsoft Dynamics NAV kliens segítségével nyitják meg és kezelik.

Az alábbi lépésekkel nyithat meg egy .fdb fájlt a Microsoft Dynamics NAV-ban:

1. Nyissa meg a Microsoft Dynamics NAV fejlesztői környezetet.
2. Kattintson a Fájl menüre, és válassza a Megnyitás lehetőséget, vagy nyomja meg a Ctrl+O gombot.
3. Keresse meg az .fdb fájl mentési helyét.
4. Válassza ki az .fdb fájlt, és kattintson a Megnyitás gombra.

Az .fdb fájlt úgy is megnyithatja, hogy a NAV kliens segítségével csatlakozik az adatbázishoz.

1. Nyissa meg a NAV klienst.
2. Kattintson a Fájl menüre, és válassza a Csatlakozás lehetőséget.
3. A Szerver mezőbe írja be annak a szervernek a nevét vagy IP-címét, ahol az .fdb fájl található.
4. Adja meg a megfelelő Adatbázis neve és Hitelesítő adatok
5. Kattintson a Csatlakozás gombra.

Lehetőség van .fdb fájlok megnyitására a Firebird adatbázis-kezelő rendszerkezelő szoftverrel is, mivel ez a Microsoft Dynamics NAV által használt adatbázis-motor.

## Hivatkozások
* [Microsoft Dynamics NAV](https://dynamics.microsoft.com/en-us/nav-erp/)

* [Új adatbázisfájlok hozzáadása a Dynamics NAV-ban](https://learn.microsoft.com/en-us/dynamics-nav/how-to--add-new-database-files)


