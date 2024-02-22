{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Ismerje meg az ABCDDB fájlformátumot és az API-kat, amelyek ABCDDB fájlokat hozhatnak létre és nyithatnak meg.",
  "title" : "ABCDDB fájlformátum - Apple Address Book névjegylista adatbázis fájl",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-hu",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Mi az ABCDDB fájl?

A **.ABCDDB** kiterjesztésű fájl az Apple Address Book Contact List Database rövidítése. A **Címjegyzék** alkalmazáshoz tartozik, más néven **Kapcsolatok**. Ez egy beépített alkalmazás, amely iOS és macOS operációs rendszerekhez tartozik. A Névjegyek alkalmazás lehetővé teszi a felhasználók számára, hogy elmentsék és rendszerezzék a névjegyeikkel kapcsolatos információkat, beleértve az egyéneket, vállalkozásokat és szervezeteket. Ez az alkalmazás lehetővé teszi a felhasználók számára, hogy nyomon kövessék az olyan részleteket, mint a nevek, címek, telefonszámok és e-mail címek, valamint csoportokba sorolják névjegyeiket.

## Kapcsolat az SQLite-tal és a tipikus elérési úttal

Az Apple AddressBook (más néven Contacts) a kapcsolattartási adatokat vCard-ként tárolja a metaadat mappában. **Az _ABCDDB_ fájl valójában _SQLite 3 adatfájl_**.

Az SQLite egy népszerű adatbázis-kezelő rendszer, amelyet könnyűre és önállóra terveztek. Számos különböző típusú szoftverben és eszközben használják. Az SQLite az RDBMS egy típusa, ami azt jelenti, hogy olyan táblákban tárolja az adatokat, amelyek kulcsokon keresztül kapcsolódnak egymáshoz. Számos adattípust képes kezelni, beleértve az egész számokat, a lebegőpontos számokat, a karakterláncokat és a bináris adatokat. Ezenkívül az SQLite támogatja a tranzakciókat, amelyek lehetővé teszik a felhasználók számára, hogy több adatbázis-műveletet hajtsanak végre egyetlen munkaegységként.

Az ABCDDB kiterjesztésű fájl általában itt tárolódik

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## A sérült névjegyadatbázis javítása

Mielőtt ezt megkísérelné, készítsen biztonsági másolatot. Ezután navigáljon ide

`~/Könyvtár/Alkalmazástámogatás/Címjegyzék`

Ebben a könyvtárban három fájl található, köztük az .abcddb kiterjesztésű

- `címjegyzék-v22.abcddb`
- `címjegyzék-v22.abcddb-wal`
- `címjegyzék-v22.abcddb-shm`

Törölje az összes fájlt, és nyissa meg újra a Névjegyeket, és újra működni fog.

## Állítsa vissza a Címjegyzék adatbázist a biztonsági másolatból

Tételezzük fel, hogy a Címjegyzék adatbázis névjegyei az `addressbook-v22.abcddb' fájlban vannak tárolva.

- Először készítsen biztonsági másolatot a címjegyzék adatairól, és lépjen ki az összes alkalmazásból.
- Helyezze át adatbázisfájlját a `~/Library/Application Support/AddressBook` alkönyvtárba
- Indítsa el az **Address Book.app** alkalmazást.

## Az ABCDDB fájl adatainak exportálása a Microsoft Access szolgáltatásba

Mivel a fájl SQLite 3 adatfájl, az abcddb fájlon belüli adatokat exportálhatja a Microsoft Accessbe az ODBC-csatlakozó használatával.

Az SQLite ODBC-összekötő egy szoftverkönyvtár és -illesztőprogram, amely lehetővé teszi az ODBC-felületet támogató alkalmazások számára, hogy csatlakozzanak egy SQLite-adatbázishoz. Tartalmaz egy könyvtárat, amely meghatározza az ODBC felületet, és egy illesztőprogramot, amely ezt a felületet SQLite API hívásokká alakítja. Az SQLite ODBC-csatlakozó használatához először telepítenie kell, majd be kell állítania egy ODBC-adatforrást a számítógépén. A lépések végrehajtása után minden ODBC-támogatással rendelkező alkalmazás képes lesz csatlakozni az adatforráshoz, és adatokat kérni az SQLite adatbázisból.

## Hivatkozások
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Contact Database for Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Hogyan nyithatok meg vagy exportálhatok abcddb fájlt Windows 7 Excelben?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -windows-7-excel)

