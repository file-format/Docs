{
  "date": "2023-06-12",
  "keywords": [
"bak",
"bak fails",
"Microsoft SQL Server datu bāzes dublēšana",
"kas ir bak fails",
"kā atvērt bak failu",
"failu",
"bak faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "BAK faila formāts — Microsoft SQL Server datu bāzes dublējums",
  "description": "Uzziniet par BAK SQL Server dublēšanas formātu un API, kas var izveidot un atvērt BAK failus.",
  "linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver-lv",
      "parent": "database"
}
},
  "lastmod": "2023-06-12"
}

## Kas ir BAK fails?

.bak fails Microsoft SQL Server kontekstā ir dublējuma faila formāts, ko izmanto SQL Server datu bāzes kopiju glabāšanai. Šajos failos ir ietverts datu bāzes momentuzņēmums noteiktā brīdī, tostarp tās shēma, dati un cita saistīta informācija. Tie tiek ģenerēti, izmantojot SQL Server iebūvēto dublēšanas un atjaunošanas funkcionalitāti, un tie kalpo vairākiem būtiskiem mērķiem:

1. **Datu atkopšana:** .bak faili nodrošina datu bāzes atkopšanas līdzekli datu zuduma, bojājuma vai citu problēmu gadījumā. Atjaunojot datubāzi no .bak faila, varat atjaunot to iepriekšējā stāvoklī, samazinot dīkstāves laiku un datu zudumu.

2. **Migrācija un klonēšana:** dublējuma faili bieži tiek izmantoti, lai migrētu datu bāzes starp serveriem vai izveidotu datu bāzu kopijas testēšanas, izstrādes vai pārskatu sniegšanas nolūkos. Tie piedāvā konsekventu un efektīvu veidu, kā pārvietot datu bāzes starp vidēm.

3. **Atkopšana laikā:** SQL Server ļauj veikt tūlītēju atkopšanu, izmantojot .bak failus. Tas nozīmē, ka varat atjaunot datu bāzi noteiktā laika posmā, kas var būt ļoti svarīgi, lai nodrošinātu atbilstību normatīvajiem aktiem vai datu auditu.

4. **Atkopšana pēc katastrofas:** .bak faili ir būtiska avārijas atkopšanas plānošanas daļa. Tie nodrošina, ka jūsu dati ir drošībā un tos var ātri atjaunot aparatūras kļūmju, dabas katastrofu vai citu katastrofālu notikumu gadījumā.

## Izveidojiet .BAK failu programmā SQL Server

Lai SQL Server izveidotu .bak failu, parasti tiek izmantotas SQL Server Management Studio (SSMS) vai Transact-SQL (T-SQL) komandas, piemēram, BACKUP DATABASE vai BACKUP LOG. Šeit ir vienkāršots piemērs tam, kā varat izveidot datu bāzes dublējumu, izmantojot T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Atjaunojiet .BAK failu programmā SQL Server

Lai atjaunotu datu bāzi no .bak faila, varat izmantot komandu RESTORE DATABASE:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Kā atvērt BAK failu SQL serverī?

Lai atvērtu .bak failā saglabātos datus un piekļūtu tiem, tie parasti ir jāatjauno Microsoft SQL Server instancē. Tālāk ir norādītas vispārīgas darbības, lai atvērtu .bak failu, izmantojot SQL Server Management Studio (SSMS).

1. **Palaidiet SQL Server Management Studio**: atveriet SSMS savā datorā. Parasti to var atrast izvēlnē Sākt vai meklējot SQL Server Management Studio”.

2. **Savienojuma izveide ar SQL Server instanci**: SSMS sistēmā izveidojiet savienojumu ar SQL Server gadījumu, kurā vēlaties atjaunot datu bāzi. Lai veiktu šo darbību, jums būs nepieciešamas nepieciešamās atļaujas.

3. **Atjaunot datu bāzi**:

a. Objekta pārlūka rūtī kreisajā pusē izvērsiet SQL Server gadījumu.

b. Izvērsiet mezglu Datubāzes.

c. Ar peles labo pogu noklikšķiniet uz Datubāzes un atlasiet Atjaunot datu bāzi.

4. **Norādiet avotu un galamērķi**:

a. Dialoglodziņa Datu bāzes atjaunošana lapas Vispārīgi laukā Uz datu bāzi ievadiet jaunās datu bāzes nosaukumu. Tas būs atjaunotās datu bāzes nosaukums.

b. Sadaļā Avots” kā dublējuma datu nesēja veidu izvēlieties Ierīce”.

c. Noklikšķiniet uz pogas ... blakus laukam Ierīce, lai meklētu .bak failu, kuru vēlaties atjaunot.

d. Atlasiet .bak failu, kuru vēlaties atvērt, un noklikšķiniet uz OK.

5. **Atjaunošanas opcijas**: pārskatiet un konfigurējiet atjaunošanas opcijas pēc vajadzības. Varat norādīt, vai pārrakstīt esošu datu bāzi, iestatīt atkopšanas opcijas un veikt citas darbības. Noteikti iestatiet šīs opcijas atbilstoši savām prasībām.

6. **Sāciet atjaunošanu**: kad esat konfigurējis atjaunošanas opcijas, dialoglodziņā Atjaunot datu bāzi noklikšķiniet uz pogas Labi. SQL Server sāks atjaunošanas procesu.

7. **Piekļuve atjaunotajai datu bāzei**: pēc veiksmīgas atjaunošanas varat piekļūt atjaunotajai datu bāzei programmā SQL Server Management Studio tāpat kā jebkurai citai datu bāzei. Varat palaist vaicājumus, skatīt tabulas un strādāt ar datiem datu bāzē.

## Citi BAK faili

Šeit ir citi failu tipi, kas izmanto faila paplašinājumu **.bak**.

**Datu bāze**
- [BAK - Database Backup File](/database/bak/)
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)

**Spēle**
- [BAK - Terraria World or Player Backup](/game/bak-terraria/)

**Dažādi**
- [BAK - Backup File](/misc/bak-backup/)
- [BAK - Chromium Bookmarks Backup](/misc/bak-chromium/)
- [BAK - Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK - MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/misc/bak-vegas/)

**Iestatījumi**
- [BAK - Holo Launcher Backup](/settings/bak-holo/)

## Atsauces
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
