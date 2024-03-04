{
  "date": "2021-08-24",
  "keywords": [
"trc failą",
"trc failo formatas",
"kas yra trc failas",
"failą",
"trc pavyzdys",
"trc failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie TRC failo formatą ir API, kurios gali kurti ir atidaryti TRC failus.",
  "title": "TRC – SQL serverio sekimo failas",
  "linktitle": "TRC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-tr-ltc"
}
},
  "lastmod": "2021-08-24"
}

## Kas yra TRC failas?
Faile su plėtiniu .trc yra Miscrosoft SQL serverio duomenų bazės veiklos sekimo rezultatai. Šiuos failus sukuria programinė įranga SQL Server Profiler; paprastai supakuota su Microsoft SQL Server programine įranga. Duomenų bazės administratoriai gali analizuoti duomenų bazės teiginių seką ir peržiūrėti sekimo žurnalą, jei įtariama kokių nors klaidų ar įspėjimų. Šie failai paprastai yra tipiškame MSSQL aplanke LOG, esančiame Windows operacinės sistemos programos failų kataloge.

## TRC failo formatas
TRC failo formatą naudoja SQL Server Profiler, kad automatiškai sugeneruotų naują MS SQL serverio neseniai įvykdytų teiginių pėdsaką. SQL serverio profiliavimo priemonė bet kokiam naujam pėdsakui naudoja numatytąjį šabloną. Tačiau programinėje įrangoje yra keletas iš anksto nustatytų šablonų, skirtų tam tikrų tipų įvykiams stebėti. Taip pat SQL Server Profiler galima naudoti kuriant šablonus, kurie apibrėžia įvykių klases ir duomenų stulpelius, kuriuos reikia įtraukti į pėdsakus.

### Iš anksto nustatyti šablonai
Štai kai kurių iš anksto nustatytų šablonų, įtrauktų į SQL Server Profiler, sąrašas:
- **SP_Counts**: fiksuoja saugomų procedūrų vykdymo veiksmus laikui bėgant.
- **Standartinis**: bendras pėdsakų kūrimo pradžios taškas.
- **TSQL**: fiksuoja visus Transact-SQL teiginius, kuriuos klientai pateikia SQL Server, ir išleidimo laiką.
– **TSQL_Duration**: fiksuoja visus Transact-SQL teiginius, kuriuos klientai pateikia SQL Server, jų vykdymo laiką ir sugrupuoja juos pagal trukmę.
- **TSQL_Grouped**: naudokite konkretaus kliento ar vartotojo užklausoms tirti.
- **TSQL_Locks**: naudokite aklavietės trikčių šalinimui, užrakinimo skirtajam laikui ir eskalavimo įvykiams užrakinti.
- **TSQL_Replay**: naudokite kartotiniam derinimui, pvz., etaloniniam testavimui, atlikti.
- **TSQL_SP**: naudokite saugomų procedūrų komponentų žingsniams analizuoti.
- **Tunning**: naudokite sekimo išvesties generavimui, kurią Database Engine Tuning Advisor gali naudoti kaip darbo krūvį duomenų bazėms derinti.
### Susiekite pėdsaką su Windows Performance Log duomenimis
SQL Server Profiler galima naudoti norint atidaryti Microsoft Windows našumo žurnalą, pasirinkti skaitiklius, kurie susietų su sekimu, ir rodyti pasirinktus našumo skaitiklius kartu su pėdsakais MS SQL Server Profiler GUI. Norėdami nurodyti našumo žurnalo duomenis, susijusius su pasirinktu sekimo įvykiu, vertikali raudona juosta SQL serverio profiliavimo priemonės sistemos monitoriaus duomenų lango srityje.


## Nuorodos Nr.

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)


