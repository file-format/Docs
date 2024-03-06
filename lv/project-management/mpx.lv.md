{
  "date": "2019-10-11",
  "keywords": [
"mpx fails",
"mpx faila formātā",
"kas ir mpx fails",
"failu",
"mpx piemērs",
"mpx faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MPX — Microsoft Project Exchange faila formāts",
  "description": "Uzziniet par MPX failu formātu un API, kas var izveidot un atvērt MPX failus.",
  "linktitle": "MPX",
  "menu": {
    "docs": {
      "parent": "project-management",
      "identifier": "project-management-mp-lvx"
}
},
  "lastmod": "2021-05-07"
}

## Kas ir MPX fails? ##

Fails ar paplašinājumu .mpx ir Microsoft Exchange faila formāts. Microsoft Project (MSP) izstrādāja MPX faila formātu, lai atvieglotu projekta informācijas apmaiņu starp MSP un citām lietojumprogrammām, kas atbalsta MPX faila formātu, tostarp Primavera Project Planner, Sciforma un Timerline Precision Estimating. Izmantojot MPX failus, varat pārsūtīt visu veidu informāciju no projekta uz citu sistēmu, piemēram, detalizētu informāciju par resursu piešķiršanu, kalendāra informāciju vai informāciju no dialoglodziņa Projekta informācija.

Microsoft Project 4.0 introduced support for creating and reading MPX file formats that continued to be used through Microsoft Project 98. Tomēr atbalsts MPX failu izveidei ir pārtraucis Microsoft Project 2000 izlaišanu, un versijas līdz Microsoft Project 2010 atbalsta tikai MPX lasīšanu. MPX faila formāts netiek atbalstīts versijās, kas jaunākas par MSP 2010.

## MPX faila formāts ##

Šajā sadaļā ir sniegts pārskats par MPX failu specifikācijām. Pilnīgas specifikācijas ir atrodamas šajā [Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) rakstā, un tās var skatīt sīkākai informācijai.

### Ieraksti ###

MPX faila ieraksts satur informāciju par projektu. Ir dažādi ierakstu veidi, kur katram ierakstam ir sava secība. Katrs ieraksta veids tiek identificēts pēc tā ieraksta numura. MPX failam ir nepieciešams faila izveides ieraksta veids. Cita veida ieraksti nav obligāti. Nākamajā tabulā ir parādīti visi ierakstu veidi, to ierakstu numuri un ierakstu skaits, ko katrs tips var ietvert MPX failā. Ieraksta iekļaušanai MPX failā ir jāatbilst tabulas secībai, jebkurā vietā ievietojot komentārus.

|Ieraksta nosaukums|Ieraksta numurs|Maksimālais ierakstu skaits
---|---|---|
|Faila izveide (obligāti)|nav|1
|Valūtas iestatījumi|10|1
|Noklusējuma iestatījumi|11|1
|Datuma un laika iestatījumi|12|1
|Bāzes kalendāra definīcija|20|250
|Pamata kalendāra Stundas|25| 7 par katru bāzes kalendāra definīcijas ierakstu
|Bāzes kalendāra izņēmums|26| 250 par katru bāzes kalendāra definīcijas ierakstu
|Projekta galvene|30|1
|Teksta resursu tabulas definīcija|140|1- (Vai arī varat izmantot ciparu resursu tabulas definīcijas ierakstu)
|Ciparu resursu tabulas definīcija|41|1
|Resurss|50|9999
|Resursu piezīmes|51| 1 katram resursa ierakstam
|Resursu kalendāra definīcija|55| 1 katram resursa ierakstam
|Resursu kalendārs Stundas|56| 7 katram resursu kalendāram
|Resursu kalendāra izņēmums| 57|250 par vienu resursu kalendāru
|Teksta uzdevumu tabulas definīcija|60|1 (vai arī varat izmantot skaitlisko uzdevumu tabulas definīcijas ierakstu)
|Ciparu uzdevumu tabulas definīcija|61|1
|Uzdevums|70|9
|Uzdevuma piezīmes|71| 1 katram uzdevuma ierakstam
|Atkārtots uzdevums|72| 1 katram uzdevuma ierakstam
|Resursu piešķiršana|75| 100 par vienu uzdevumu ierakstu
|Uzdevumu darba grupas lauki|76| 1 katram uzdevuma ierakstam
|Projektu nosaukumi|80|500
|DDE un OLE klientu saites|81|500
|Komentāri|0|neierobežots

### Faila struktūra ###

MPX fails sastāv no iepriekš minētajiem ierakstiem, kas failā ir sakārtoti iepriekš iestatītā veidā. Sīkāka informācija par šiem ierakstu veidiem tiek apspriesta šādi:

**Faila izveides ieraksts (FCR):** Šis ir obligāts ieraksts, kura mērķis ir identificēt:

* Faila formāts (MPX)

* Uzskaitiet failā izmantoto atdalītāju rakstzīmi

* Faila izveidei izmantotās programmas un versijas numurs

* Failā izmantotā MPX faila formāta versijas numurs

* Faila izveidošanai izmantotā koda lapa


Tam ir jābūt pirmajam ierakstam failā. Eksportējot no Microsoft Project, saraksta atdalīšanas rakstzīme ir norādīta Windows vadības paneļa vienumā Reģionālie iestatījumi. FCR ieraksts ietver šādus laukus:

* MPX, kam tūlīt seko saraksta atdalīšanas rakstzīme

* Programmas nosaukums/identifikators

* Faila versijas numurs

* Koda lapa (850, 437, MAC, ANSI)


Piemēram, ierakstā var būt informācija **MPX, Microsoft Project, 3.0**, kas norāda, ka šajā MPX failā kā saraksta atdalīšanas rakstzīme tiek izmantots komats. Failā izmantotā MPX formāta versija tiek eksportēta no Microsoft Project versijas 3.0.

**Valūtas iestatījumi** Šis ieraksts ar ieraksta numuru 10 norāda valūtas opciju iestatījumus dialoglodziņā Opcijas. Ja šis ieraksts nav iekļauts, tiek izmantoti pašreizējie iestatījumi dialoglodziņā Opcijas. Tūkstošiem un decimāldaļskaitļu atdalītāji ir norādīti Windows vadības paneļa vienumā Reģionālie iestatījumi.
Šajā ierakstā iekļautie lauki ir:

* Valūtas simbols

* Simbola pozīcija (0 # pēc, 1 # pirms, 2 # pēc ar atstarpi, 3 # pirms ar atstarpi)

* Valūtas cipari (0,1,2)

* Tūkstošiem atdalītājs

* Decimāldaļas atdalītājs


**Piemērs:** 10,$,1,2,,.
Šajā piemērā ir norādīts, ka valūtas vērtībām pirms tām ir iekļauta dolāra zīme ($), ka aiz komata ir iekļauti divi cipari, ka komats tiek izmantots, lai atdalītu tūkstošus, un punkts tiek izmantots kā decimālzīme. Tā kā saraksta atdalīšanas rakstzīme ir iekļauta laukā Tūkstošiem atdalītājs, lauks tiek ieskauts ar pēdiņām.

**Noklusējuma iestatījumi:** Šis ieraksts ar ieraksta numuru 11 norāda noklusējuma opciju iestatījumus dialoglodziņā Opcijas. Ja ilgums nav norādīts, lai pareizi veiktu ilguma vienības aprēķinus, ir jāiestata noklusējuma ilguma vienība. Ja šis ieraksts nav iekļauts, tiek izmantoti pašreizējie iestatījumi dialoglodziņā Opcijas.
Šajā ierakstā iekļautie lauki ir:

* Noklusējuma ilguma vienības (0 # minūtes, 1 # stunda, 2 # dienas, 3 # nedēļas)

* Noklusējuma ilguma veids (0 # nav fiksēts, 1 # fiksēts)

* Noklusējuma darba vienības (0 minūtes, 1 stunda, 2 dienas, 3 nedēļas)

* Noklusējuma stundas/diena

* Noklusējuma stundas/nedēļa

* Noklusējuma standarta likme

* Noklusējuma virsstundu likme

* Uzdevuma statusa atjaunināšana Resursa statusa atjaunināšana (0 # nē, 1 # jā)

* Sadalīti nepabeigtie uzdevumi (0 # nē, 1 # jā)


**Date and Time Settings:** This record, having record number 12, specify settings for the date and time options in the Options dialog box, and the Bar Text Date Format option in the Layout dialog box. If this record is not included, the current settings in the Options dialog box are used.
\\Šajā ierakstā iekļautie lauki ir:

* Pasūtījuma datums (0 # mēnesis/diena/gads, 1 # diena/mēnesis/gads, 2 # gads/mēnesis/diena)

* Laika formāts (0 # 12 stundas, 1 # 24 stundas)

* Noklusējuma laiks (minūšu skaits pēc pusnakts)

* Datuma atdalītājs

* Laika atdalītājs

* 0:00 līdz 11:59 Teksts

* 12:00 līdz 23:59 Teksts

* Datuma formāts (0–14)*

* Joslas teksta datuma formāts (0 -194)*


**Pamata kalendāra definīcija:** Šie ieraksti, kuru ieraksta numurs ir 20, nosaka bāzes kalendārus un to nedēļas darba un brīvdienas. Noklusētie iestatījumi tiek izmantoti, ja par dienu nav ieraksta. Noklusējuma iestatījumi ir no pirmdienas līdz piektdienai darba dienām un sestdienām un svētdienām brīvdienām. Šajā ierakstā ir jāaizpilda lauks Vārds. Katrai no dienām ieraksts 0 norāda, ka diena ir brīvdiena, bet ieraksts 1 norāda, ka diena ir darba diena.
Šajā ierakstā iekļautie lauki ir:

* Vārds

* Svētdiena

* pirmdiena

* Otrdiena

* Trešdiena

* ceturtdiena

* Piektdiena

* Sestdiena


**Kalendāra pamatstundas:** Šie ieraksti ar ieraksta numuru 25 norāda darba laiku nedēļas dienām, ja tie atšķiras no noklusējuma iestatījumiem. Noklusējuma darba laiks ir no 8:00 līdz 12:00 un 13:00 līdz 17:00 Katrs bāzes kalendāra stundu ieraksts attiecas uz iepriekšējo bāzes kalendāra definīcijas ierakstu. Katram Base Calendar Definition ierakstam var sekot līdz septiņiem no šiem ierakstiem.

* Nedēļas diena (no 1 līdz 7, kur 1 # svētdiena un 7 # sestdiena)

* No laika 1

* Līdz 1. laikam

* No laika 2

* Līdz 2. laikam

* No laika 3

* Līdz 3. laikam


**Bāzes kalendāra izņēmums:** Šie ieraksti ar ieraksta numuru 26 nosaka izņēmumus no dienām un stundām, kas norādītas iepriekšējos divos ierakstu tipos. Katram Base Calendar Definition ierakstam var sekot līdz 250 no šiem ierakstiem. Šie ieraksti ir jāuzskaita hronoloģiskā secībā. Ja izņēmums ir viena diena, varat atstāt lauku Līdz datums tukšu. Ja laiki nav norādīti, tiek izmantoti noklusējuma laiki no 8:00 līdz 12:00 un 13:00 līdz 17:00.
Šajā ierakstā iekļautie lauki ir:

* No datuma

* Līdz datumam

* Nestrādājošs/strādājošs (0 # nestrādā, 1 # strādā)

* No laika 1

* Līdz 1. laikam

* No laika 2

* Līdz 2. laikam

* No laika 3

* Līdz 3. laikam


**Project Header:** This record, having record value 30,  sets global project fields, such as the project start date and project finish date. The fields in this record correspond to the information in the Project Info and Statistics dialog boxes.
Šajā ierakstā iekļautie lauki un cilnes ir:

* Cilne Projekts

* Uzņēmums

* Pārvaldnieks

* Kalendārs (izmantots standarta gadījumā, ja nav ieraksta)

* Sākuma datums (importētajam failam tiek aprēķināts šis vai nākamais lauks atkarībā no iestatījuma Grafiks no)

* Beigu datums

* Grafiks no (0 # sākums, 1 # finišs)

* Šodienas datums*

* Komentāri

* Izmaksas

* Pamata izmaksas

*Faktiskās izmaksas

* Darbs

* Sākotnējais darbs

* Faktiskais darbs

* Darbs

* Ilgums*

* Sākotnējais ilgums*

* Faktiskais ilgums

* Pabeigts procents

* Sākotnējais sākums

* Pamatlīnijas apdare

* Faktiskais sākums

* Faktiskā apdare

* Sāciet novirzi

* Pabeigt dispersiju

* Priekšmets

* Autors

* Atslēgvārdi


**Teksta resursu tabulas definīcija**: šajā ierakstā ir norādīti resursu lauki, kas tiek importēti vai eksportēti. Importēto failu nosaukumiem ir jāatbilst lauku nosaukumiem, kas tiek izmantoti programmā Microsoft Project. Eksportētajiem failiem šis ieraksts tiek iegūts no resursu eksportēšanas tabulas. Jāizmanto vai nu šis ieraksts, vai ciparu resursu tabulas definīcijas ieraksts. Eksportējot no Microsoft Project, tiek iekļauti abi šie ieraksti.

**Ciparu resursu tabulas definīcija:** izmantojot skaitļus, nevis nosaukumus, šajā ierakstā ir norādīti resursu lauki, kas tiek importēti vai eksportēti. Šī ir alternatīva metode, lai identificētu katrā resursa ierakstā iekļautos resursu laukus, un tā ir noderīga, definējot MPX failu, kas izveidots ar svešvalodas produktu.

**Resurss:** šajos ierakstos ir informācija par katru importēto vai eksportējamo resursu. Katrs resursa ieraksts apraksta vienu resursu. Importējot informāciju, iekļautos laukus nosaka ieraksts Teksta resursu tabulas definīcija vai Skaitlisko resursu tabulas definīcijas ieraksts. Eksportējot informāciju, tiek iekļauti lauki, kas ir norādīti resursu eksportēšanas tabulā.

**Piezīmes par resursiem:** šajos ierakstos ir piezīmes par tieši iepriekšējo resursu ierakstu. Jaunai piezīmes rindai tiek izmantota ASCII rakstzīme 127. Ja piezīmē ir iekļauta saraksta atdalīšanas zīme, ievietojiet piezīmi pēdiņās.

**Resursu kalendāra definīcija:** Šie ieraksti nosaka darba dienas resursam, kas norādīts tieši iepriekšējā Resursu ierakstā. Importētajiem failiem, ja laukā Base Calendar Name nav ieraksta, tiek izmantots standarta. Ja konkrētajai dienai nav ieraksta, tas norāda, ka diena ir iestatīta uz noklusējuma vērtību (2). Ja nav Resursu kalendāra definīcijas ierakstu, standarta tiek izmantots kā resursa bāzes kalendārs, pēc noklusējuma tiek izmantots dienām. Katrai dienai ieraksts 0 norāda, ka diena ir brīvdiena, 1 norāda, ka diena ir darba diena, un 2 norāda, ka tiek izmantota noklusējuma diena.

**Resursu kalendāra stundas:** šie ieraksti nosaka resursa darba laiku, kas atšķiras no resursa izmantotā bāzes kalendāra. Šie ieraksti attiecas uz Resursu kalendāra definīcijas ierakstu tieši pirms šī ieraksta. Katram resursu kalendāra definīcijas ierakstam var sekot līdz septiņiem no šiem ierakstiem.

**Resursu kalendāra izņēmums:** šie ieraksti definē iepriekšējos divos ierakstu veidos norādīto dienu un stundu izņēmumus. Līdz 250 no šiem ierakstiem var sekot katram Resursu kalendāra definīcijas ierakstam. Šie ieraksti ir jāuzskaita hronoloģiskā secībā. Ja izņēmums ir tikai viena diena, varat atstāt lauku Līdz datums tukšu. Ja laiks nav norādīts, tiek izmantoti noklusējuma laiki no 8:00 līdz 12:00 un 13:00 līdz 17:00.

**Text Task Table Definition:** This record lists the task fields, in order, that are being imported or exported. For imported files, the names must match the field names used in Microsoft Project. If the file is being exported, this record comes from the task Export table. When exporting from Microsoft Project, both of these records are included. Fields that are calculated by Microsoft Project, such as Scheduled Start and Scheduled Finish, are ignored if imported. If you have task start or finish dates that are fixed, use the Constraint Type and Constraint Date fields.

**Ciparu uzdevumu tabulas definīcija:** izmantojot skaitļus, nevis nosaukumus, šajā ierakstā ir norādīti uzdevumu lauki, kas tiek importēti vai eksportēti. Šī ir alternatīva metode katrā uzdevuma ierakstā iekļauto uzdevumu lauku identificēšanai, un tā ir noderīga, definējot MPX failu, kas izveidots ar svešvalodas produktu.

**Uzdevums:** šajos ierakstos ir informācija par katru importēto vai eksportējamo uzdevumu. Katrs uzdevuma ieraksts apraksta vienu uzdevumu. Importējot informāciju, iekļautos laukus nosaka ieraksts Teksta uzdevumu tabulas definīcija vai Skaitliskās uzdevumu tabulas definīcijas ieraksts. Eksportējot informāciju, tiek iekļauti lauki, kas ir norādīti uzdevuma eksportēšanas tabulā.

**Uzdevuma piezīmes:** Šajos ierakstos ir piezīmes par tieši iepriekšējo uzdevumu ierakstu. Izmantojiet ASCII rakstzīmi 127, lai norādītu jaunu rindiņu piezīmē. Ja piezīmē ir iekļauta saraksta atdalīšanas zīme, ievietojiet piezīmi pēdiņās.

**Resursu piešķiršana**: šajos ierakstos ir norādīta informācija par resursiem, kas piešķirti uzdevumam, kas tika definēts iepriekšējā uzdevuma ierakstā. Ja apvienojat failus un vēlaties, lai informācija par resursu piešķiršanu tiktu saglabāta, šī informācija ir jāiekļauj MPX failā. Ja apvienosiet, visi esošie sapludināto uzdevumu uzdevumi tiks dzēsti. Ja apvienojat failus, pamatojoties uz unikālajiem ID, resursi tiek piešķirti, izmantojot resursu unikālos ID, nevis ID.

**Resource Assignment Workgroup Fields:** These records list the information that is stored with each assignment for the Workgroup features of Microsoft Project 4.0 and 4.1. Ja izmantojat Workgroup līdzekļus, šis ieraksts ir jāiekļauj, lai nodrošinātu, ka informācija netiek zaudēta.

**Projektu nosaukumi:** Šajos ierakstos ir uzskaitīti visi projektā saglabātie DDE saišu nosaukumi.

**DDE un OLE klientu saites:** šajos ierakstos ir uzskaitītas projekta DDE saites.

**Komentāri:** šos ierakstus var izmantot, lai failam pievienotu komentārus, un tie var parādīties jebkurā faila pozīcijā. Katram komentāru ierakstam jāsākas ar 0.

## Problēmas, atverot MPX failu ##

Šeit ir saraksts ar dažām izplatītām problēmām, kas var rasties un izraisīt MPX formāta nepareizu darbību:

 *   Atbalsta programmatūras trūkums
 *   Bojāts fails
 *   Inficēts fails vīrusa dēļ
 *   Sistēmā nav piekļuves tiesību, lai atvērtu failus
 *   Novecojis disks jūsu sistēmā
 *   Faila paplašinājums tiek pārdēvēts

## Atsauces Nr.

* [MPX — Microsoft zināšanu bāze](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)


