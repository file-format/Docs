{
"dátum": "2023-06-12",
  "keywords": [
"bak",
"bak fájl",
"Microsoft SQL Server Database Backup",
"mi az a bak fájl",
"hogyan kell megnyitni a bak fájlt",
"fájl",
"bak fájl kiterjesztése",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "BAK fájlformátum - Microsoft SQL Server adatbázis biztonsági mentése",
  "description":"További információ a BAK SQL Server Backup formátumáról és az API-król, amelyek BAK-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
      "parent": "database"
}
},
"lastmod": "2023-06-12"
}

## Mi az a BAK fájl?

A ".bak" fájl a Microsoft SQL Server kontextusában egy biztonsági mentési fájlformátum, amelyet az SQL Server-adatbázis másolatainak tárolására használnak. Ezek a fájlok az adatbázis pillanatképét tartalmazzák egy adott időpontban, beleértve annak sémáját, adatait és egyéb kapcsolódó információkat. Az SQL Server beépített biztonsági mentési és visszaállítási funkciójával készülnek, és számos kulcsfontosságú célt szolgálnak:

1. **Adat-helyreállítás:** A .bak fájlok lehetőséget nyújtanak az adatbázis helyreállítására adatvesztés, adatsérülés vagy egyéb problémák esetén. Ha visszaállít egy adatbázist egy .bak fájlból, akkor visszaállíthatja azt egy korábbi állapotába, minimalizálva az állásidőt és az adatvesztést.

2. **Áttelepítés és klónozás:** A biztonsági mentési fájlokat gyakran használják adatbázisok kiszolgálók közötti áttelepítésére vagy adatbázis-másolatok létrehozására tesztelési, fejlesztési vagy jelentéskészítési célokra. Konzisztens és hatékony módot kínálnak az adatbázisok környezetek közötti mozgatására.

3. **Point-in-Time Recovery:** Az SQL Server lehetővé teszi a pont-időben történő helyreállítást .bak fájlok használatával. Ez azt jelenti, hogy egy adott időpontra visszaállíthatja az adatbázist, ami kulcsfontosságú lehet a szabályozási megfelelés vagy az adatok auditálása szempontjából.

4. **Katasztrófa-helyreállítás:** A .bak fájlok a katasztrófa utáni helyreállítás tervezésének kritikus részét képezik. Biztosítják, hogy adatai biztonságban legyenek, és hardverhiba, természeti katasztrófa vagy egyéb katasztrófa esetén gyorsan visszaállíthatók legyenek.

## Hozzon létre egy .BAK fájlt az SQL Serverben

Ha .bak fájlt szeretne létrehozni az SQL Serverben, általában az SQL Server Management Studio (SSMS) vagy a Transact-SQL (T-SQL) parancsokat használja, például a BACKUP DATABASE vagy a BACKUP LOG parancsot. Íme egy egyszerűsített példa arra, hogyan hozhat létre adatbázis-mentést T-SQL használatával:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Állítson vissza egy .BAK fájlt az SQL Serverben

Adatbázis .bak fájlból történő visszaállításához használja a RESTORE DATABASE parancsot:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Hogyan lehet megnyitni a BAK fájlt az SQL Serverben?

A ".bak" fájlban tárolt adatok megnyitásához és eléréséhez általában vissza kell állítania azokat egy Microsoft SQL Server-példányba. Íme a „.bak” fájl SQL Server Management Studio (SSMS) használatával történő megnyitásának általános lépései:

1. **Indítsa el az SQL Server Management Studio programot**: Nyissa meg az SSMS-t a számítógépén. Általában megtalálja a Start menüben vagy az „SQL Server Management Studio” kifejezésre keresve.

2. **Csatlakozás egy SQL Server-példányhoz**: SSMS-ben csatlakozzon ahhoz az SQL Server-példányhoz, ahol vissza szeretné állítani az adatbázist. A művelet végrehajtásához szüksége lesz a szükséges engedélyekre.

3. **Adatbázis visszaállítása**:

a. A bal oldali Object Explorer panelen bontsa ki az SQL Server példányt.

b. Bontsa ki az „Adatbázisok” csomópontot.

c. Kattintson a jobb gombbal az "Adatbázisok" elemre, és válassza az "Adatbázis visszaállítása" lehetőséget.

4. **Adja meg a forrást és a célt**:

a. Az "Adatbázis visszaállítása" párbeszédpanel "Általános" oldalán adja meg az új adatbázis nevét az "Adatbázishoz" mezőben. Ez lesz a visszaállított adatbázis neve.

b. A „Forrás” részben válassza az „Eszköz” lehetőséget biztonsági mentési adathordozó típusaként.

c. Kattintson a "..." gombra az "Eszköz" mező mellett, hogy megkeresse a visszaállítani kívánt ".bak" fájlt.

d. Válassza ki a megnyitni kívánt ".bak" fájlt, majd kattintson az "OK" gombra.

5. **Visszaállítási beállítások**: Tekintse át és szükség szerint konfigurálja a visszaállítási beállításokat. Megadhatja, hogy felül kell-e írni egy meglévő adatbázist, megadhatja a helyreállítási beállításokat stb. Ügyeljen arra, hogy ezeket a beállításokat igényeinek megfelelően állítsa be.

6. **A visszaállítás kezdeményezése**: Miután konfigurálta a visszaállítási beállításokat, kattintson az "OK" gombra az "Adatbázis visszaállítása" párbeszédpanelen. Az SQL Server megkezdi a visszaállítási folyamatot.

7. **Hozzáférés a visszaállított adatbázishoz**: Sikeres visszaállítás után a visszaállított adatbázishoz ugyanúgy hozzáférhet az SQL Server Management Studio alkalmazásban, mint bármely más adatbázishoz. Lekérdezéseket futtathat, táblákat tekinthet meg, és dolgozhat az adatbázison belüli adatokkal.

## Egyéb BAK fájlok

Íme más fájltípusok, amelyek a **.bak** fájlkiterjesztést használják.

**Adatbázis**
- [BAK - Adatbázis biztonsági mentési fájl](/hu/database/bak/)
- [BAK - Swiftpage Act! Adatbázis biztonsági mentése](/hu/database/bak-act/)

**Játszma, meccs**
- [BAK - Terraria World vagy Player Backup](/hu/game/bak-terraria/)

**Egyéb**
- [BAK - Backup File](/hu/misc/bak-backup/)
- [BAK - Chromium Bookmarks Backup](/hu/misc/bak-chromium/)
- [BAK - Finale 2012 Score Backup](/hu/misc/bak-finale/)
- [BAK - MobileTrans Backup](/hu/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/hu/misc/bak-vegas/)

**Beállítások**
- [BAK - Holo Launcher Backup](/hu/settings/bak-holo/)

## Hivatkozások
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
