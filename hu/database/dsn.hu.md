{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Ismerje meg a DSN fájlformátumot és az API-kat, amelyekkel DSN fájlokat hozhat létre és nyithat meg.",
  "title" : "DSN-fájlformátum – Adatbázis-forrásnévfájl",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-hu",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Mi az a DSN fájl?

A DSN az adatforrás neve” rövidítése, és ez egy fájlformátum, amelyet az adatbázis-kapcsolati információk tárolására használnak. A DSN-fájlokat általában az ODBC-vel (Open Database Connectivity) együtt használják, és egyszerű hozzáférést tesznek lehetővé egy adott adatbázishoz azáltal, hogy megadják a csatlakozáshoz szükséges információkat, például a kiszolgáló nevét, felhasználónevét és jelszavát. A fájl általában egyszerű szöveges, és szövegszerkesztővel hozható létre és szerkeszthető. Különféle operációs rendszereken használható, például Windows, Linux és Mac.

## Hogyan készítsünk DSN fájlt?

A DSN-fájlok létrehozásának módja az operációs rendszertől és a rendelkezésre álló eszközöktől függően változhat. A következő lépések általános áttekintést nyújtanak a DSN-fájl Windows rendszeren történő létrehozásának folyamatáról.

1. Nyissa meg az ODBC adatforrás adminisztrátort az ODBC Data Sources” kifejezésre keresve a start menüben.
2. Válassza a System DSN lapot, és kattintson a Hozzáadás gombra.
3. Válassza ki a megfelelő illesztőprogramot az adatbázishoz, amelyhez csatlakozni kíván, és kattintson a Befejezés gombra.
4. Töltse ki az adatbázishoz való csatlakozáshoz szükséges információkat, például a kiszolgáló nevét, felhasználónevét és jelszavát.
5. Kattintson az OK gombra a DSN-fájl mentéséhez.

Alternatív megoldásként létrehozhat egy DSN-fájlt manuálisan is úgy, hogy létrehoz egy egyszerű szöveges fájlt .dsn kiterjesztéssel, és megadja a szükséges csatlakozási információkat a következő formátumban:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Ezután ennek a fájlnak az elérési útját használhatja DSN-ként a kódban/szkriptben az adatbázishoz való csatlakozáshoz.

## Programok, amelyek megnyitják a DSN fájlt

A DSN-fájl egy egyszerű szöveges fájl, amely az adatbázishoz való csatlakozáshoz használt információkat tárolja, például a kiszolgáló nevét, felhasználónevét és jelszavát. Általában az ODBC-vel (Open Database Connectivity) együtt használatos, hogy egyszerű hozzáférést biztosítson egy adott adatbázishoz.

A DSN-fájlok tartalmának megnyitásához és megtekintéséhez használhat bármilyen szövegszerkesztőt, például Jegyzettömböt, Sublime Text-et, Atomot stb. Ezek a programok lehetővé teszik a DSN-fájl megnyitását és a benne tárolt kapcsolódási információk megtekintését.

Ha azonban a DSN-fájlt adatbázishoz való csatlakozáshoz és olyan műveletek végrehajtásához szeretné használni, mint a SELECT, INSERT, UPDATE, DELETE stb., ODBC-támogatással rendelkező programok, például programozási nyelvek, például Python, Java, C# vagy adatbázis-kezelő eszköz, mint a Microsoft Access , SQL Server Management Studio szükséges. Ezek a programok a DSN-fájlban található információk segítségével csatlakozhatnak az adatbázishoz, és végrehajthatják a kívánt műveletet.

## Hivatkozások

* [Mi az a DSN (adatforrás neve)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



