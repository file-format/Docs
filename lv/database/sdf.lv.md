{
  "date": "2021-05-03",
  "keywords": [
"SDF",
"sdf failu",
"kas ir sdf fails",
"kā atvērt sdf failu",
"pagarinājumu",
"failu",
"sdf faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Datu bāzes faili"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par SDF failu formātu un API, kas var izveidot un atvērt SDF failus.",
  "title": "SDF — SQL Server Compact Database File",
  "linktitle": "SDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sd-lvf"
}
},
  "lastmod": "2021-05-03"
}

## Kas ir SDF fails?
Fails ar paplašinājumu .sdf satur Microsoft SQL Server Compact (SQL CE) datu bāzi, kas pazīstama arī kā kompakta relāciju datu bāze; Microsoft ražojis lietojumprogrammām, kas paredzētas mobilajām ierīcēm un galddatoriem. Tā atbalsta gan 32, gan 64 bitu operētājsistēmu, un pilns datu bāzes saturs ir iekļauts vienā SDF failā un var aizņemt vairāk nekā 4 GB diska vietas. Drošības nolūkos .sdf failu var šifrēt ar 128 bitu šifrēšanu. SQL CE izpildlaiks nodrošina paralēlu vairāku lietotāju piekļuvi .sdf failam. SDF failu var kopēt, izmantojot **QuickOnce**, vai vienkārši to var kopēt uz galamērķi sistēmas izvietošanai.

## SDF faila formāts
SDF fails satur datu bāzi, ko parasti sauc par kompakto relāciju datu bāzi. SDF fails satur visu ar datu bāzi saistīto informāciju, un SQL Server Compact ir viegls un bezmaksas datu bāzes dzinējs, kas tiek izmantots .sdf failu pārvaldībai. .sdf faila lielums nedrīkst pārsniegt 4 GB lieluma ierobežojumu. SDF faili nesaglabā informāciju par saglabātajām procedūrām, aktivizētājiem vai skatiem. Lietojumprogrammām, kas izmanto SQL CE datu bāzi, nav jānorāda ceļš uz SDF failu ADO.NET savienojuma virknē, tā vietā to var minēt kā |DataDirectory|\database_name.sdf, kas nosaka datu direktoriju, kas tiek definēts lietojumprogrammas montāžas manifestā.
.sdf nosaukumu piešķiršanas metode nav obligāta, un faila saglabāšanai var izmantot jebkuru paplašinājumu. Paroles iestatīšana datu bāzes failam ir neobligāts solis. Lai saspiestu vai labotu datu bāzi, fails ir jāsaglabā, izmantojot opciju **saspiesta/labota datu bāze**.

## Atsauces

 * [SQL Server Compact — Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
 * [SQL Server Compact izmantošana ASP.NET tīmekļa lietojumprogrammām](https://learn.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


