{
  "date": "2020-11-11",
  "keywords": [
"BAK",
"pratęsimas",
"failą",
"Dokumento formatas",
"BAK failo tipas",
"BAK failo plėtinys",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"Duomenų bazės failai"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie BAK failo formatą ir API, kurios gali kurti ir atidaryti BAK failus.",
  "title": "BAK failo formatas – duomenų bazės atsarginės kopijos failas",
  "linktitle": "BAK",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ba-ltk"
}
},
  "lastmod": "2020-12-04"
}

## Kas yra BAK failas?

Failas su plėtiniu .bak paprastai yra atsarginės kopijos failas, naudojamas skirtingų programinės įrangos įrankių atsarginėms duomenų kopijoms saugoti. Duomenų bazės požiūriu BAK failas naudojamas Microsoft SQL Server duomenų bazės turiniui saugoti. Visi duomenys ir failai, susiję su duomenų baze, yra saugomi šiuo failo formatu, kad būtų galima juos gauti, jei duomenų bazė dėl kokių nors priežasčių gali būti sugadinta arba negaliojanti. Saugumo sumetimais atsarginės kopijos gali būti saugomos ir indeksuojamos kituose serveriuose. Kelios programos gali sukurti BAK failus, pvz., SQL Server Management Studio, Transact-SQL ir Windows PowerShell.

## BAK failo formatas

Vidinė BAK failo informacija nėra žinoma, tačiau plačiai manoma, kad jis pagrįstas Microsoft Tape Format (MTF). MTF specifikacijos yra prieinamos ir jas galima nurodyti norint suprasti failo struktūrą. Dokumente pateikiama išsami informacija apie MTF saugyklą visiems, kurie turi bendrų žinių apie saugyklos valdymo operacijas, juostinius įrenginius ir failų sistemas.

### Duomenų rinkiniai

Duomenų rinkinys yra objektų, įrašytų į laikmeną (juostą, optinį diską ir kt.) duomenų atsarginės kopijos arba atkūrimo metu, rinkinys. Duomenų rinkinius sudaro kelios laikmenos esant dideliam duomenų kiekiui.

### Pagrindiniai DPS elementai

MTF failą sudaro keli pagrindiniai elementai, sudarantys jo sudedamąsias dalis. Šie elementai yra:

#### Deskriptorių blokai

Deskriptorių blokai (DBLK) naudojami formato valdymui ir yra pagrindiniai MTF failo pagrindai. Vienas MTF failas apibrėžia kelis DBLK kiekvienam unikaliam vaidmeniui. Kiekvienas DBLK yra kintamo ilgio duomenų blokas, padalintas į šias keturias dalis:

 * Bendra bloko antraštė – fiksuoto ilgio struktūra, bendra visiems DBLK. Tai yra vienintelė reikalinga bloko antraštė.
 * DBLK tipo informacija – fiksuoto ilgio blokas, būdingas apibrėžiamo DBLK tipui
 * Operacinės sistemos duomenys – konkretūs duomenys, apibrėžti pagal DBLK tipą ir operacines sistemas
 * DBLK informacija – kintamo ilgio DBLK specifinė informacija, kurios negalima išsaugoti naudojant fiksuoto ilgio DBLK informaciją.

{{< figure src=../bak.png alt=Microsoft SQL atsarginės kopijos failo formatas >}}

#### Duomenų srautas

Duomenų srautai MTF faile naudojami duomenų inkapsuliavimui ir lygiavimui. Jį sudaro srauto antraštė, po kurios eina srauto duomenys. Srauto antraštė gali apimti tik vieno tipo srauto duomenis.

{{< figure src="../bak_datastream.png" alt="Microsoft SQL atsarginės kopijos failo formatas" >}}

#### FileMarks

Failo žymeklis naudojamas loginiam atskyrimui ir greitai prieigai prie laikmenos. Failų žymes emuliuoja įrenginio tvarkyklė arba Soft Filemark Descriptor blokas, jei naudojamas įrenginys nepateikia failų ženklų.

## Kiti BAK failai

Štai kiti failų tipai, kuriuose naudojamas **.bak** failo plėtinys.

**Duomenų bazė**
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)
- [BAK - Microsoft SQL Server Database Backup](/database/bak-sqlserver/)

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

## Nuorodos Nr.

* [[MS-BCP]: masinio kopijavimo formatas](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)


