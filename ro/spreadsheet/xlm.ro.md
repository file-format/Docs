{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "fișier", "extensie", "format fișier", "Fișier Macro Microsoft Excel", "Foaie de calcul" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ghidul dvs. de format de fișier pentru a afla ce este un fișier XLM Macros și API-uri care pot crea și deschide fișiere XLM.",
  "title" :"Ce este un fișier XLM?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Ce este un fișier XLM?

XLM, pentru Excel Macro, este un tip de fișiere Spreadsheet care sunt folosite pentru a stoca macrocomenzi. Din punct de vedere al aplicației, o Macro este un set de instrucțiuni care sunt utilizate pentru automatizarea proceselor. O macrocomandă este utilizată pentru a înregistra pașii care sunt efectuati în mod repetat pentru formatul de fișier [XLS](/ro/spreadsheet/xls/) și facilitează efectuarea acțiunilor prin rularea din nou a macrocomenzii. Macro-urile sunt programate cu Visual Basic pentru aplicații (VBA) Microsoft din registrul de lucru Excel folosind Editorul Visual Basic și pot fi executate/depanate direct de acolo.

## Scurt istoric ##

Microsoft Excel a acceptat programarea macrocomenzilor încă de la prima lansare publică. Caracteristicile macrocomenzilor au rămas aceleași prin versiunile ulterioare ale Excel cu extensie conform noilor funcții. XLM a fost limba macro implicită pentru Excel prin Excel 4.0. Excel 5.0 a înregistrat macrocomenzi în VBA în mod implicit, dar cu versiunea 5.0 înregistrarea XLM era încă permisă ca opțiune. După versiunea 5.0, această opțiune a fost întreruptă. Toate versiunile de Excel, inclusiv Excel 2010, sunt capabile să ruleze o macrocomandă XLM, deși Microsoft descurajează utilizarea acestora.

## Înregistrarea unei macrocomenzi în XLM ##

Excel oferă pași ușor de utilizat pentru înregistrarea unei macrocomenzi. Este necesar să aveți instalate instrumente pentru dezvoltatori pentru a lucra cu macrocomenzi. Odată ce o înregistrare macro este în proces, aceasta înregistrează fiecare acțiune a utilizatorului pentru a fi redată mai târziu. Înregistrarea macro implică de fapt toți pașii pe care îi efectuează un utilizator după ce începe înregistrarea. Astfel, dacă faceți conținutul unei celule bold, italic și setați justificarea textului acesteia după ce a fost începută o înregistrare macro, toate aceste comenzi vor fi înregistrate. Fiecărei macrocomenzi înregistrate i se poate aloca o comandă rapidă, de asemenea, pentru o redare rapidă mai târziu. Înregistrarea macro generează cod VBA sub forma unei macrocomenzi care poate fi editată folosind Visual Basic Editor (VBE).

## Model obiect Excel ##

Macro-urile folosesc rutine VBA în spatele lor și urmează [Excel Object Model](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model) în acest scop. Acest model identifică obiectele unei foi de calcul pentru interacțiunea cu foaia de calcul prin bare de instrumente de comandă, bare de comandă sau casete de mesaje definite de utilizator. De exemplu, accesul la proprietățile registrului de lucru este acordat cu obiectul Workbook. În mod similar, în model există obiectul Foaie de lucru pentru a lucra cu foile de lucru ale registrului de lucru în mod programatic.

## Macrocomenzi și securitate ##

VBA permite accesul la toate domeniile de aplicație, precum și la sistemul de fișiere și poate fi, de asemenea, periculos. Acest lucru ridică îngrijorări atunci când partajați registrul de lucru cu cineva care poate rula fișierul la capătul său. Adică Microsoft Excel avertizează despre deschiderea unui astfel de fișier. Macro-urile pot fi certificate cu o semnătură digitală pentru ca alți utilizatori să verifice dacă acestea sunt de încredere. Astfel, macrocomenzile pot fi activate după verificarea sursei lor.

## Referințe ##

* [[MS-XLS] - Structura formatului fișierului binar Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Programare macro](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

