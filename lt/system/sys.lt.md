{
  "date": "2021-07-08",
  "keywords": [
"SYS",
"pratęsimas",
"failą",
"formatu",
"sistema",
"Vairuotojas",
"Sistemos failas",
"programas",
"kompiuteris",
"taikymas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "SYS – sistemos failo formatas",
  "description": "Sužinokite apie SYS failo formatą ir API, kurios gali kurti ir atidaryti SYS failus.",
  "linktitle": "SYS",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-sy-lts"
}
},
  "lastmod": "2021-07-08"
}

## Kas yra SYS failas? ##

SYS failai yra sistemos failai, naudojami Windows OS ir MS-DOS programose. Šių failų negalima atidaryti tiesiogiai, juos sudaro įrenginio tvarkyklė ir konfigūracija. SYS failai yra atsakingi už pagrindinių operacinės sistemos funkcijų failų saugojimą. Tai laikomi svarbiais įrenginio tvarkyklės failais ir taip pat gali būti naudojami, kai reikia išspręsti bet kokią lenktynininko problemą. Jie yra atsakingi už tinkamą kompiuterinės sistemos veikimą, o .sys failai turi būti teisingi ir išsamūs.


## Techninė specifikacija Nr.

.sys failai iš tikrųjų yra [BMP](/image/bmp/) formato poaibis, nes leidžia naudoti tik tam tikrus derinius. Įprastas šių failų formatas yra LOGOS.SYS, LOGOW.SYS ir LOGO.SYS. Kiti failai neturi šio formato.

Diegimo metu šie failai dažniausiai naudojami Windows *C* kataloge. Dauguma problemų, susijusių su įrenginių tvarkyklėmis, išsprendžiamos atnaujinus Windows OS. Išsamią šių failų informaciją ir informaciją galima peržiūrėti naudojant Windows OS integruotas programas. Tai taip pat apima nuorodas į skirtingus operacinės sistemos modulius.
Kai kurie sistemos failų pavyzdžiai yra:

* IO.SYS (saugo disko operacinės sistemos įrenginių tvarkykles)

* MSDOS.SYS (Juose yra branduolys arba pagrindinis operacinės sistemos kodas)

* CONFIG.SYS (Juose yra įvairių konfigūravimo parinkčių)

* KEYBOARD.SYS (Juose yra su klaviatūros išdėstymu susijusi informacija) 

* COUNTRY.SYS (ši informacija yra susijusi su šalimi ir kodu)


## SYS failo formatas ##

Microsoft sukūrė failus su .sys plėtiniais. Kintamieji ir funkcijos yra įtraukti į SYS failus. Jas dažniausiai naudoja Microsoft operacinė sistema. Šie failai daugiausia yra disko šakniniame kataloge:

* C:\Windows\system32\tvarkyklės

* C:\Windows\WinSxS


Kai kurie įprasti įspėjimai apie SYS failus yra šie:

* Šių failų pavadinimai neturėtų būti keičiami, nes šie failai yra atsakingi už pagrindines operacinės sistemos funkcijas ir kintamuosius.
* Šie failai neturėtų būti ištrinti, nes jų nebuvimas gali sukelti klaidų
* .sys failai neturėtų būti atsisiunčiami iš interneto, kol nesate tikri dėl šaltinio teisėtumo
* Nereikėtų maišytis su šiais failais, nes jų pakeitimas ar trikdymas sukelia rimtų sistemos klaidų
* Jei šiuos failus sugadino koks nors virusas ar kenkėjiška programa, juos reikia įdiegti iš naujo

## SYS pavyzdys Nr.

Toliau pateikiamas paprasto SYS sistemos konfigūracijos failo pavyzdys:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
