{
  "date": "2019-10-11",
  "keywords": [
"mpx failą",
"mpx failo formatas",
"kas yra mpx failas",
"failą",
"mpx pavyzdys",
"mpx failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MPX – „Microsoft Project Exchange“ failo formatas",
  "description": "Sužinokite apie MPX failo formatą ir API, kurios gali kurti ir atidaryti MPX failus.",
  "linktitle": "MPX",
  "menu": {
    "docs": {
      "parent": "project-management",
      "identifier": "project-management-mp-ltx"
}
},
  "lastmod": "2021-05-07"
}

## Kas yra MPX failas? ##

Failas su plėtiniu .mpx yra Microsoft Exchange failo formatas. MPX failo formatą sukūrė Microsoft Project (MSP), kad būtų lengviau keistis projekto informacija tarp MSP ir kitų MPX failo formatą palaikančių programų, įskaitant Primavera Project Planner, Sciforma ir Timerline Precision Estimating. Naudodami MPX failus galite perkelti visų rūšių informaciją iš projekto į kitą sistemą, pvz., išsamią išteklių priskyrimo informaciją, kalendoriaus informaciją arba informaciją iš dialogo lango Projekto informacija.

Microsoft Project 4.0 introduced support for creating and reading MPX file formats that continued to be used through Microsoft Project 98. Tačiau MPX failų kūrimo palaikymas nutraukė Microsoft Project 2000 leidimą, o versijos iki Microsoft Project 2010 palaiko tik MPX skaitymą. MPX failo formatas nepalaikomas naujesnėse nei MSP 2010 versijose.

## MPX failo formatas ##

Šiame skyriuje pateikiama MPX failų specifikacijų apžvalga. Išsamias specifikacijas rasite šiame [Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) straipsnyje ir galite rasti išsamios informacijos.

### Įrašai ###

MPX failo įrašą sudaro projekto informacija. Yra įvairių tipų įrašų, kur kiekvienas įrašas turi savo tvarką. Kiekvienas įrašo tipas identifikuojamas pagal įrašo numerį. MPX faile būtina turėti failo kūrimo įrašo tipą. Kitų tipų įrašai nėra privalomi. Šioje lentelėje rodomi visi įrašų tipai, jų įrašų numeriai ir įrašų skaičius, kurį kiekvienas tipas gali turėti MPX faile. Įrašo įtraukimas į MPX failą turi atitikti lentelės tvarką, o komentarai įterpiami bet kur.

|Įrašo pavadinimas|Įrašo numeris|Maksimalus įrašų skaičius
---|---|---|
|Failo kūrimas (būtina)|nėra|1
|Valiutos nustatymai|10|1
|Numatytieji nustatymai|11|1
|Datos ir laiko nustatymai|12|1
|Pagrindinio kalendoriaus apibrėžimas|20|250
|Pagrindinio kalendoriaus valandos|25| 7 už bazinio kalendoriaus apibrėžimo įrašą
|Pagrindinio kalendoriaus išimtis|26| 250 už bazinio kalendoriaus apibrėžimo įrašą
|Projekto antraštė|30|1
|Teksto išteklių lentelės apibrėžimas|140|1- (Arba galite naudoti skaitmeninių išteklių lentelės apibrėžimo įrašą)
|Skaičių išteklių lentelės apibrėžimas|41|1
|Išteklius|50|9 999
|Išteklių pastabos|51| 1 vienam išteklių įrašui
|Išteklių kalendoriaus apibrėžimas|55| 1 vienam išteklių įrašui
|Išteklių kalendoriaus valandos|56| 7 už išteklių kalendorių
|Išteklių kalendoriaus išimtis| 57|250 už išteklių kalendorių
|Teksto užduočių lentelės apibrėžimas|60|1 (arba galite naudoti skaitmeninės užduočių lentelės apibrėžimo įrašą)
|Skaičių užduočių lentelės apibrėžimas|61|1
|Užduotis|70|9
|Užduoties pastabos|71| 1 už užduoties įrašą
|Pasikartojanti užduotis|72| 1 už užduoties įrašą
|Išteklių paskyrimas|75| 100 už kiekvieną užduoties įrašą
|Priskyrimo darbo grupės laukai|76| 1 kiekvienam priskyrimo įrašui
|Projektų pavadinimai|80|500
|DDE ir OLE klientų nuorodos|81|500
|Komentarai|0|neribotas

### Failo struktūra ###

MPX failą sudaro pirmiau minėti įrašai, kurie faile yra išdėstyti iš anksto nustatyta tvarka. Išsami informacija apie šiuos įrašų tipus aptariama taip:

**Failo kūrimo įrašas (FCR):** Tai yra privalomas įrašas, kurio tikslas yra identifikuoti:

* Failo formatas (MPX)

* Sąrašas faile naudojamas skyriklio simbolis

* Programos ir versijos numeris, naudojamas kuriant failą

* Faile naudojamo MPX failo formato versijos numeris

* Kodo puslapis, naudojamas kuriant failą


Tai turi būti pirmasis įrašas faile. Eksportuojant iš Microsoft Project, sąrašo skyriklio simbolis nurodomas Windows valdymo skydo elemente Regional Settings. FCR įrašas apima šiuos laukus:

* MPX, po kurio iškart eina sąrašo skyriklio simbolis

* Programos pavadinimas / identifikatorius

* Failo versijos numeris

* Kodo puslapis (850, 437, MAC, ANSI)


Pavyzdžiui, įraše gali būti informacijos **MPX, Microsoft Project, 3.0**, kuri nurodo, kad šiame MPX faile kaip sąrašo skyriklio simbolis naudojamas kablelis. Faile naudojama MPX formato versija eksportuojama iš Microsoft Project 3.0 versijos.

**Valiutos nustatymai** Šis įrašas, kurio įrašo numeris 10, nurodo valiutos parinkčių nustatymus dialogo lange Parinktys. Jei šis įrašas neįtrauktas, naudojami dabartiniai parametrai dialogo lange Parinktys. Tūkstančių ir dešimtainių skyrikliai nurodyti Windows valdymo skydo elemente Regioniniai nustatymai.
Į šį įrašą įtraukti laukai:

* Valiutos simbolis

* Simbolio padėtis (0 # po, 1 # prieš, 2 # po tarpo, 3 # prieš su tarpeliu)

* Valiutos skaitmenys (0,1,2)

* Tūkstantis skyriklis

* Dešimtainis skyriklis


**Pavyzdys:** 10,$,1,2,,.
Šiame pavyzdyje nurodoma, kad prieš valiutos reikšmes yra dolerio ženklas ($), kad po kablelio įrašomi du skaitmenys, kad tūkstančiai atskiriami kableliais ir kad taškas naudojamas kaip kablelis. Kadangi sąrašo skyriklio simbolis yra įtrauktas į lauką Tūkstantis skyriklis, laukas yra parašytas kabutėmis.

**Numatytieji nustatymai:** Šis įrašas, kurio įrašo numeris 11, nurodo numatytųjų parinkčių nustatymus dialogo lange Parinktys. Jei trukmė nenurodyta, norint teisingai apskaičiuoti trukmės vienetą, reikia nustatyti numatytąjį trukmės vienetą. Jei šis įrašas neįtrauktas, naudojami dabartiniai parametrai dialogo lange Parinktys.
Į šį įrašą įtraukti laukai:

* Numatytieji trukmės vienetai (0 # minučių, 1 # valandos, 2 # dienos, 3 # savaitės)

* Numatytasis trukmės tipas (0 # nepataisyta, 1 # nustatyta)

* Numatytieji darbo vienetai (0 # minučių, 1 # valandos, 2 # dienos, 3 # savaitės)

* Numatytosios valandos per dieną

* Numatytoji valandos per savaitę

* Numatytoji standartinė norma

* Numatytasis viršvalandžių tarifas

* Užduočių būsenos atnaujinimas Atnaujina išteklių būseną (0 # ne, 1 # taip)

* Padalintos vykdomos užduotys (0 # ne, 1 # taip)


**Date and Time Settings:** This record, having record number 12, specify settings for the date and time options in the Options dialog box, and the Bar Text Date Format option in the Layout dialog box. If this record is not included, the current settings in the Options dialog box are used.
\\Į šį įrašą įtraukti laukai:

* Datos užsakymas (0 # mėnuo/diena/metai, 1 # diena/mėnuo/metai, 2 # metai/mėnuo/diena)

* Laiko formatas (0 # 12 valandų, 1 # 24 valandos)

* Numatytasis laikas (minučių skaičius po vidurnakčio)

* Datos skyriklis

* Laiko skyriklis

* Nuo 0:00 iki 11:59 Tekstas

* Nuo 12:00 iki 23:59 Tekstas

* Datos formatas (0–14)*

* Juostos teksto datos formatas (0 -194)*


**Pagrindinio kalendoriaus apibrėžimas:** Šie įrašai, turintys įrašo numerį 20, apibrėžia bazinius kalendorius ir jų darbo bei nedarbo savaitės dienas. Jei nėra dienos įrašo, naudojami numatytieji nustatymai. Numatytieji nustatymai yra nuo pirmadienio iki penktadienio darbo dienomis, o šeštadienį ir sekmadienį – ne darbo dienomis. Šiame įraše būtinas Vardo laukelis. Kiekvienai dienai įrašas 0 rodo, kad diena yra ne darbo diena, o 1 – kad diena yra darbo diena.
Į šį įrašą įtraukti laukai:

* Vardas

* Sekmadienis

* Pirmadienis

* Antradienis

* Trečiadienis

* Ketvirtadienis

* Penktadienis

* Šeštadienis


**Pagrindinės kalendoriaus valandos:** Šie įrašai, turintys įrašo numerį 25, nurodo savaitės dienų darbo valandas, jei jos skiriasi nuo numatytųjų nustatymų. Numatytosios darbo valandos yra 8:00–12:00 ir 13:00–17:00 Kiekvienas bazinio kalendoriaus valandų įrašas nurodo ankstesnį Bazinio kalendoriaus apibrėžimo įrašą. Iki septynių šių įrašų galima sekti kiekvieną bazinio kalendoriaus apibrėžimo įrašą.

* Savaitės diena (1–7, kur 1 # sekmadienis ir 7 # šeštadienis)

* Nuo 1 laiko

* Iki 1 laiko

* Nuo 2 laiko

* Iki 2 laiko

* Nuo 3 laiko

* Iki 3 laiko


**Pagrindinė kalendoriaus išimtis:** Šie įrašai, turintys įrašo numerį 26, apibrėžia dienų ir valandų, nurodytų ankstesniuose dviejuose įrašų tipuose, išimtis. Iki 250 šių įrašų gali sekti kiekvieną bazinio kalendoriaus apibrėžimo įrašą. Šie įrašai turi būti išvardyti chronologine tvarka. Jei išimtis yra viena diena, lauką Iki datos galite palikti tuščią. Jei laikas nenurodytas, naudojami numatytieji laikai nuo 8:00 iki 12:00 ir nuo 13:00 iki 17:00.
Į šį įrašą įtraukti laukai:

* Nuo datos

* Iki šiol

* Nedirbantis/dirbantis (0 # nedirbantis, 1 # dirbantis)

* Nuo 1 laiko

* Iki 1 laiko

* Nuo 2 laiko

* Iki 2 laiko

* Nuo 3 laiko

* Iki 3 laiko


**Project Header:** This record, having record value 30,  sets global project fields, such as the project start date and project finish date. The fields in this record correspond to the information in the Project Info and Statistics dialog boxes.
Į šį įrašą įtraukti laukai ir skirtukai:

* Skirtukas Projektas

* Bendrovė

* Vadovas

* Kalendorius (naudojamas standartinis, jei nėra įrašo)

* Pradžios data (šis arba kitas laukas apskaičiuojamas importuotam failui, atsižvelgiant į nustatymą „Tvarkaraštis nuo“)

* Baigimo data

* Tvarkaraštis nuo (0 # pradžia, 1 # finišas)

* Dabartinė data*

* Komentarai

* Kaina

* Pradinė kaina

* Tikroji kaina

* Darbas

* Pradinis darbas

* Tikras darbas

* Darbas

* Trukmė*

* Pradinė trukmė*

* Faktinė trukmė

* Procentas baigtas

* Pradinė pradžia

* Bazinė apdaila

* Faktinė pradžia

* Tikra apdaila

* Pradėkite nuokrypį

* Apdailos dispersija

* Tema

* Autorius

* Raktažodžiai


**Teksto išteklių lentelės apibrėžimas**: šiame įraše iš eilės pateikiami importuojami arba eksportuojami išteklių laukai. Importuotų failų pavadinimai turi atitikti Microsoft Project naudojamus laukų pavadinimus. Eksportuotų failų atveju šis įrašas gaunamas iš išteklių eksportavimo lentelės. Turi būti naudojamas šis įrašas arba skaitmeninės išteklių lentelės apibrėžimo įrašas. Eksportuojant iš Microsoft Project, įtraukiami abu šie įrašai.

**Skaičių išteklių lentelės apibrėžimas:** naudojant skaičius, o ne pavadinimus, šiame įraše iš eilės pateikiami importuojami arba eksportuojami išteklių laukai. Tai yra alternatyvus būdas identifikuoti išteklių laukus, įtrauktus į kiekvieną išteklių įrašą, ir naudingas apibrėžiant MPX failą, sukurtą užsienio kalbos produktu.

**Išteklius:** šiuose įrašuose yra informacija apie kiekvieną importuojamą arba eksportuojamą išteklį. Kiekvienas išteklių įrašas aprašo vieną šaltinį. Kai importuojate informaciją, įtrauktus laukus apibrėžia teksto išteklių lentelės apibrėžimo įrašas arba skaitmeninių išteklių lentelės apibrėžimas. Kai eksportuojate informaciją, įtraukiami laukai, nurodyti išteklių eksportavimo lentelėje.

**Išteklių pastabos:** šiuose įrašuose yra pastabų apie prieš pat buvusį išteklių įrašą. Naujai pastabos eilutei naudojamas 127 ASCII simbolis. Jei pastaboje yra sąrašo skyriklio simbolis, pažymėkite pastabą kabutėse.

**Išteklių kalendoriaus apibrėžimas:** šie įrašai apibrėžia ištekliaus, nurodyto prieš pat buvusiame išteklių įraše, darbo dienas. Importuotiems failams, jei nėra lauko Bazinio kalendoriaus pavadinimo įrašo, naudojamas standartinis. Konkrečios dienos neįrašas rodo, kad diena nustatyta kaip numatytoji (2). Jei nėra išteklių kalendoriaus apibrėžimo įrašų, Standartinis naudojamas kaip pagrindinis išteklių kalendorius, o pagal numatytuosius nustatymus naudojamas dienoms. Kiekvienos dienos įrašas 0 rodo, kad diena yra ne darbo diena, 1 – kad diena yra darbo diena, o 2 nurodo, kad naudojama numatytoji diena.

**Išteklių kalendoriaus valandos:** šie įrašai apibrėžia ištekliaus darbo valandas, kurios skiriasi nuo pagrindinio šaltinio naudojamo kalendoriaus. Šie įrašai taikomi išteklių kalendoriaus apibrėžimo įrašui prieš pat šį įrašą. Iki septynių iš šių įrašų galima sekti kiekvieną išteklių kalendoriaus apibrėžimo įrašą.

**Išteklių kalendoriaus išimtis:** šie įrašai apibrėžia dienų ir valandų, nurodytų ankstesniuose dviejuose įrašų tipuose, išimtis. Iki 250 šių įrašų gali sekti kiekvieną išteklių kalendoriaus apibrėžimo įrašą. Šie įrašai turi būti išvardyti chronologine tvarka. Jei išimtis yra tik viena diena, lauką Iki datos galite palikti tuščią. Jei laikas nenurodytas, naudojami numatytieji laikai nuo 8:00 iki 12:00 ir nuo 13:00 iki 17:00.

**Text Task Table Definition:** This record lists the task fields, in order, that are being imported or exported. For imported files, the names must match the field names used in Microsoft Project. If the file is being exported, this record comes from the task Export table. When exporting from Microsoft Project, both of these records are included. Fields that are calculated by Microsoft Project, such as Scheduled Start and Scheduled Finish, are ignored if imported. If you have task start or finish dates that are fixed, use the Constraint Type and Constraint Date fields.

**Skaičių užduočių lentelės apibrėžimas:** naudojant skaičius, o ne pavadinimus, šiame įraše iš eilės pateikiami užduočių laukai, kurie yra importuojami arba eksportuojami. Tai yra alternatyvus būdas identifikuoti užduočių laukus, įtrauktus į kiekvieną užduoties įrašą, ir naudingas apibrėžiant MPX failą, sukurtą užsienio kalbos produktu.

**Užduotis:** šiuose įrašuose yra informacija apie kiekvieną importuojamą arba eksportuojamą užduotį. Kiekvienas užduoties įrašas aprašo vieną užduotį. Kai importuojate informaciją, įtraukti laukai apibrėžiami įrašu Teksto užduočių lentelės apibrėžimas arba skaitmeninės užduočių lentelės apibrėžimo įrašu. Kai eksportuojate informaciją, įtraukiami laukai, išvardyti užduočių eksportavimo lentelėje.

**Užduoties pastabos:** šiuose įrašuose yra pastabų apie prieš pat buvusį užduoties įrašą. Naudokite ASCII simbolį 127, kad nurodytumėte naują pastabos eilutę. Jei pastaboje yra sąrašo skyriklio simbolis, pažymėkite pastabą kabutėse.

**Išteklių priskyrimas**: šiuose įrašuose pateikiama informacija apie išteklius, priskirtus užduočiai, kuri buvo apibrėžta ankstesniame užduoties įraše. Jei sujungiate failus ir norite, kad išteklių priskyrimo informacija būtų išsaugota, turite įtraukti informaciją į MPX failą. Jei sujungsite, visos esamos sujungtų užduočių užduotys bus ištrintos. Jei sujungiate failus pagal unikalius ID, ištekliai priskiriami naudojant unikalius išteklių ID, o ne ID.

**Resource Assignment Workgroup Fields:** These records list the information that is stored with each assignment for the Workgroup features of Microsoft Project 4.0 and 4.1. Jei naudojate darbo grupės funkcijas, turite įtraukti šį įrašą, kad neprarastumėte jokios informacijos.

**Projektų pavadinimai:** šiuose įrašuose pateikiami visi projekte saugomi DDE nuorodų pavadinimai.

**DDE ir OLE klientų nuorodos:** šiuose įrašuose pateikiamos DDE nuorodos į projektą.

**Komentarai:** Šie įrašai gali būti naudojami norint pridėti komentarų prie failo ir gali būti rodomi bet kurioje failo vietoje. Kiekvienas komentarų įrašas turi prasidėti 0.

## Problemos atidarant MPX failą ##

Čia pateikiamas kai kurių dažniausiai pasitaikančių problemų, kurios gali kilti ir sukelti MPX formato netinkamą veikimą, sąrašas:

 *   Pagalbinės programinės įrangos nebuvimas
 *   Sugadintas failas
 *   Užkrėstas failas dėl viruso
 *   Sistemoje nėra prieigos teisės atidaryti failus
 *   Pasenęs diskas jūsų sistemoje
 *   Failo plėtinys pervardytas

## Nuorodos Nr.

* [MPX – „Microsoft“ žinių bazė](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)


