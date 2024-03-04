{
  "date": "2023-06-12",
  "keywords": [
"bak",
"bak failas",
"Microsoft SQL Server duomenų bazės atsarginė kopija",
"kas yra bak failas",
"kaip atidaryti bak failą",
"failą",
"bak failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "BAK failo formatas – „Microsoft SQL Server“ duomenų bazės atsarginė kopija",
  "description": "Sužinokite apie BAK SQL Server atsarginės kopijos formatą ir API, kurios gali kurti ir atidaryti BAK failus.",
  "linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver-lt",
      "parent": "database"
}
},
  "lastmod": "2023-06-12"
}

## Kas yra BAK failas?

.bak failas Microsoft SQL Server kontekste yra atsarginės kopijos failo formatas, naudojamas SQL serverio duomenų bazės kopijoms saugoti. Šiuose failuose yra momentinė duomenų bazės nuotrauka konkrečiu momentu, įskaitant jos schemą, duomenis ir kitą susijusią informaciją. Jie generuojami naudojant integruotą SQL serverio atsarginių kopijų kūrimo ir atkūrimo funkciją ir atlieka keletą svarbių tikslų:

1. **Duomenų atkūrimas:** .bak failai suteikia galimybę atkurti duomenų bazę duomenų praradimo, sugadinimo ar kitų problemų atveju. Atkurdami duomenų bazę iš .bak failo, galite grąžinti jos ankstesnę būseną, sumažindami prastovos laiką ir duomenų praradimą.

2. **Perkėlimas ir klonavimas:** Atsarginės kopijos failai dažnai naudojami duomenų bazėms perkelti iš vieno serverio į kitą arba kuriant duomenų bazių kopijas testavimo, kūrimo ar ataskaitų teikimo tikslais. Jie siūlo nuoseklų ir efektyvų būdą perkelti duomenų bazes iš vienos aplinkos į kitą.

3. **Atkūrimas laiku:** SQL serveris leidžia atlikti atkūrimą tam tikru laiku naudojant .bak failus. Tai reiškia, kad galite atkurti duomenų bazę tam tikru momentu, o tai gali būti labai svarbu siekiant atitikties teisės aktams arba atliekant duomenų auditą.

4. **Atkūrimas nelaimės atveju:** .bak failai yra svarbi atkūrimo planavimo dalis. Jie užtikrina, kad jūsų duomenys būtų saugūs ir gali būti greitai atkurti aparatinės įrangos gedimų, stichinių nelaimių ar kitų katastrofiškų įvykių atveju.

## Sukurkite .BAK failą SQL serveryje

Norėdami sukurti .bak failą SQL serveryje, paprastai naudojate SQL Server Management Studio (SSMS) arba Transact-SQL (T-SQL) komandas, pvz., BACKUP DATABASE arba BACKUP LOG. Čia yra supaprastintas pavyzdys, kaip galite sukurti duomenų bazės atsarginę kopiją naudodami T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Atkurkite .BAK failą SQL serveryje

Norėdami atkurti duomenų bazę iš .bak failo, galite naudoti komandą RESTORE DATABASE:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Kaip atidaryti BAK failą SQL serveryje?

Norėdami atidaryti ir pasiekti .bak faile saugomus duomenis, paprastai turite atkurti juos Microsoft SQL Server egzemplioriuje. Toliau pateikiami bendrieji .bak failo atidarymo veiksmai naudojant SQL Server Management Studio (SSMS):

1. **Paleiskite SQL Server Management Studio**: kompiuteryje atidarykite SSMS. Paprastai jį galite rasti meniu Pradėti arba ieškodami SQL Server Management Studio.

2. **Prisijungti prie SQL serverio egzemplioriaus**: naudodami SSMS, prisijunkite prie SQL serverio egzemplioriaus, kuriame norite atkurti duomenų bazę. Norėdami atlikti šią operaciją, jums reikės reikiamų leidimų.

3. **Atkurti duomenų bazę**:

a. Kairėje pusėje esančioje srityje Object Explorer išplėskite SQL serverio egzempliorių.

b. Išplėskite mazgą Duomenų bazės.

c. Dešiniuoju pelės mygtuku spustelėkite Duomenų bazės ir pasirinkite Atkurti duomenų bazę.

4. **Nurodykite šaltinį ir paskirties vietą**:

a. Dialogo lango Atkurti duomenų bazę puslapyje Bendra įveskite naujos duomenų bazės pavadinimą lauke Į duomenų bazę. Tai bus atkurtos duomenų bazės pavadinimas.

b. Skiltyje Šaltinis kaip atsarginės kopijos laikmenos tipą pasirinkite Įrenginys.

c. Spustelėkite mygtuką ..., esantį šalia lauko Įrenginys, kad rastumėte .bak failą, kurį norite atkurti.

d. Pasirinkite .bak failą, kurį norite atidaryti, ir spustelėkite Gerai.

5. **Atkūrimo parinktys**: jei reikia, peržiūrėkite ir sukonfigūruokite atkūrimo parinktis. Galite nurodyti, ar perrašyti esamą duomenų bazę, nustatyti atkūrimo parinktis ir kt. Būtinai nustatykite šias parinktis pagal savo poreikius.

6. **Pradėkite atkūrimą**: sukonfigūravę atkūrimo parinktis, dialogo lange Atkurti duomenų bazę spustelėkite mygtuką Gerai. SQL serveris pradės atkūrimo procesą.

7. **Prieiga prie atkurtos duomenų bazės**: sėkmingai atkūrus, galite pasiekti atkurtą duomenų bazę SQL Server Management Studio, kaip ir bet kurią kitą duomenų bazę. Galite vykdyti užklausas, peržiūrėti lenteles ir dirbti su duomenų bazės duomenimis.

## Kiti BAK failai

Štai kiti failų tipai, kuriuose naudojamas **.bak** failo plėtinys.

**Duomenų bazė**
- [BAK - Database Backup File](/database/bak/)
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)

**Žaidimas**
- [BAK - Terraria World or Player Backup](/game/bak-terraria/)

**Įvairūs**
- [BAK - Backup File](/misc/bak-backup/)
- [BAK - Chromium Bookmarks Backup](/misc/bak-chromium/)
- [BAK - Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK - MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/misc/bak-vegas/)

**Nustatymai**
- [BAK - Holo Launcher Backup](/settings/bak-holo/)

## Nuorodos
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
