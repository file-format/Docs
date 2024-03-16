{
"datum": "2023-06-12",
  "keywords": [
"bak",
"soubor bak",
"Záloha databáze Microsoft SQL Server",
"co je soubor bak",
"jak otevřít soubor bak",
"soubor",
"přípona souboru bak",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru BAK - Záloha databáze Microsoft SQL Server",
  "description":"Další informace o formátu BAK SQL Server Backup a rozhraních API, která mohou vytvářet a otevírat soubory BAK.",
  "linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
      "parent": "database"
}
},
"lastmod": "2023-06-12"
}

## Co je soubor BAK?

Soubor ".bak" v kontextu Microsoft SQL Server je záložní formát souboru používaný k ukládání kopií databáze SQL Server. Tyto soubory obsahují snímek databáze v určitém okamžiku, včetně jejího schématu, dat a dalších souvisejících informací. Jsou generovány pomocí vestavěné funkce zálohování a obnovy SQL Serveru a slouží několika zásadním účelům:

1. **Obnova dat:** Soubory .bak poskytují prostředky k obnovení databáze v případě ztráty dat, poškození nebo jiných problémů. Obnovením databáze ze souboru .bak ji můžete vrátit do předchozího stavu, čímž se minimalizují prostoje a ztráta dat.

2. **Migrace a klonování:** Záložní soubory se často používají k migraci databází mezi servery nebo vytváření kopií databází pro účely testování, vývoje nebo vytváření sestav. Nabízejí konzistentní a efektivní způsob přesunu databází mezi prostředími.

3. **Obnova v okamžiku:** SQL Server umožňuje provádět obnovu v okamžiku pomocí souborů .bak. To znamená, že můžete obnovit databázi k určitému okamžiku v čase, což může být klíčové pro dodržování předpisů nebo audit dat.

4. **Disaster Recovery:** Soubory .bak jsou kritickou součástí plánování obnovy po havárii. Zajišťují, že vaše data jsou v bezpečí a lze je rychle obnovit v případě selhání hardwaru, přírodních katastrof nebo jiných katastrofických událostí.

## Vytvořte soubor .BAK v SQL Server

K vytvoření souboru .bak na serveru SQL Server obvykle používáte příkazy SQL Server Management Studio (SSMS) nebo Transact-SQL (T-SQL), jako je BACKUP DATABASE nebo BACKUP LOG. Zde je zjednodušený příklad toho, jak můžete vytvořit zálohu databáze pomocí T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Obnovení souboru .BAK v SQL Server

Chcete-li obnovit databázi ze souboru .bak, můžete použít příkaz RESTORE DATABASE:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Jak otevřít soubor BAK na serveru SQL?

Chcete-li otevřít a získat přístup k datům uloženým v souboru ".bak", obvykle je potřebujete obnovit do instance Microsoft SQL Server. Zde jsou obecné kroky k otevření souboru „.bak“ pomocí SQL Server Management Studio (SSMS):

1. **Spusťte SQL Server Management Studio**: Otevřete SSMS v počítači. Obvykle jej najdete v nabídce Start nebo vyhledáním výrazu „SQL Server Management Studio“.

2. **Připojení k instanci SQL Server**: V SSMS se připojte k instanci SQL Serveru, kde chcete obnovit databázi. K provedení této operace budete potřebovat potřebná oprávnění.

3. **Obnovení databáze**:

A. V podokně Object Explorer na levé straně rozbalte instanci SQL Server.

b. Rozbalte uzel "Databáze".

C. Klikněte pravým tlačítkem na "Databáze" a vyberte "Obnovit databázi".

4. **Uveďte zdroj a cíl**:

A. Na stránce "Obecné" v dialogovém okně "Obnovit databázi" zadejte do pole "Do databáze" název nové databáze. Toto bude název obnovené databáze.

b. V části „Zdroj“ vyberte jako typ záložního média „Zařízení“.

C. Kliknutím na tlačítko „...“ vedle pole „Zařízení“ vyhledejte soubor „.bak“, který chcete obnovit.

d. Vyberte soubor „.bak“, který chcete otevřít, a klikněte na „OK“.

5. **Možnosti obnovení**: Zkontrolujte a nakonfigurujte možnosti obnovení podle potřeby. Můžete určit, zda se má přepsat existující databáze, nastavit možnosti obnovy a další. Ujistěte se, že jste tyto možnosti nastavili podle svých požadavků.

6. **Spusťte obnovení**: Jakmile nakonfigurujete možnosti obnovení, klikněte v dialogovém okně „Obnovit databázi“ na tlačítko „OK“. SQL Server zahájí proces obnovení.

7. **Přístup k obnovené databázi**: Po úspěšné obnově můžete přistupovat k obnovené databázi v SQL Server Management Studio stejně jako k jakékoli jiné databázi. Můžete spouštět dotazy, prohlížet tabulky a pracovat s daty v databázi.

## Další soubory BAK

Zde jsou další typy souborů, které používají příponu **.bak**.

**Databáze**
- [BAK - Soubor zálohy databáze](/cs/database/bak/)
- [BAK - Swiftpage Act! Záloha databáze](/cs/database/bak-act/)

**Hra**
- [BAK - Terraria World or Player Backup](/cs/game/bak-terraria/)

**Různé**
- [BAK - Backup File](/cs/misc/bak-backup/)
- [BAK - Záloha záložek Chromium](/cs/misc/bak-chromium/)
- [BAK - Záloha skóre finále 2012](/cs/misc/bak-finale/)
- [BAK - MobileTrans Backup](/cs/misc/bak-mobiletrans/)
- [BAK - Záloha video projektu VEGAS](/cs/misc/bak-vegas/)

**Nastavení**
- [BAK - Holo Launcher Backup](/cs/settings/bak-holo/)

## Reference
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
