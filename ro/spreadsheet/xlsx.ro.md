{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "fișier", "extensie", "format fișier", "Excel", "Foaie de calcul"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre ce este un fișier XLSX și API-urile care pot crea și deschide fișiere XLSX.",
  "title" :"Format de fișier XLSX - Ce este un fișier XLSX?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Ce este un fișier XLSX?

**XLSX** este un format bine-cunoscut pentru documentele Microsoft Excel care a fost introdus de Microsoft odată cu lansarea Microsoft Office 2007. Bazat pe structura organizată conform convențiilor de ambalare deschisă, așa cum este prezentat în [Partea 2](https://www. .ecma-international.org/publications/standards/Ecma-376.htm) din standardul OOXML ECMA-376, noul format este un pachet zip care conține o serie de fișiere XML. Structura de bază și fișierele pot fi examinate prin simpla dezarhivare a fișierului .xlsx.

## Scurt istoric al formatului de fișier XLSX

Formatul de fișier XLSX a fost introdus în 2007 și folosește standardul Open XML adaptat de Microsoft încă din 2000. Înainte de XLSX, formatul de fișier obișnuit folosit era [XLS](/ro/spreadsheet/xls/), care era format de fișier binar pur. Noul tip de fișier a adăugat avantaje de dimensiuni mici ale fișierelor, mai puține modificări ale corupției și reprezentarea imaginilor bine formatate. A fost la începutul anilor 2000 când Microsoft a decis să opteze pentru modificarea pentru a se adapta standardului pentru **Office Open XML**. Până în 2007, acest nou format de fișier a devenit parte a Office 2007 și este continuat și în noile versiuni ale Microsoft Office.

## Specificații de format de fișier XLSX

[Specificațiile oficiale de format de fișier XLSX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) sunt disponibile online de la Microsoft. Pentru a vedea ce este în interiorul fișierului XLSX, trebuie doar să-l redenumiți în fișierul [ZIP](/ro/compression/zip/) schimbându-i extensia și apoi extrageți-l pentru a vizualiza fișierele constitutive ale acestui registru de lucru Excel. Un registru de lucru gol, atunci când este extras în fișierele sale, are următoarele fișiere și foldere constitutive.

### [Content_Types].xml ###

Acesta este singurul fișier care se găsește la nivelul de bază atunci când este extras zip-ul. Listează tipurile de conținut pentru părțile din pachet. Toate referințele la fișierele XML incluse în pachet sunt menționate în acest fișier XML.

### \_rels (dosar) ###

Acesta este folderul Relații care conține un singur fișier XML care stochează relațiile la nivel de pachet. Legăturile către părțile cheie ale fișierelor Xlsx sunt conținute în acest fișier ca URI. Aceste URI-uri identifică tipul de relație a fiecărei părți cheie cu pachetul. Aceasta include relația cu documentul de birou principal situat ca xl/workbook.xml și alte părți din docProps ca proprietăți de bază și extinse.

### docProps ###

Acest folder conține proprietățile generale ale documentului. Acestea includ un set de proprietăți de bază, un set de proprietăți extinse sau specifice aplicației și o previzualizare în miniatură a documentului. Un registru de lucru gol are două fișiere în acest folder și anume app.xml și core.xml. Core.xml conține informații precum autorul, data creării și salvate și modificate. App.xml conține informații despre conținutul fișierului.

### xl (dosar) ###

Acesta este folderul principal care conține toate detaliile despre conținutul registrului de lucru. În mod implicit, are următoarele foldere:

* \_rels
*temă
* fișe de lucru

și următoarele fișiere xml:

* styles.xml
* workbook.xml

## Exemplu de format XLSX ##


Pentru fiecare foaie de lucru Excel conținută într-un registru de lucru, există un fișier XML. Puteți găsi aceste fișiere XML în folderul xl/worksheets. Toate informațiile conținute într-o fișă de lucru sunt organizate în diferite secțiuni în fișierul XML. Să examinăm un exemplu de foaie de lucru dintr-un registru de lucru care este prezentat în imaginea următoare.

{{< figure src="../XLSX file format.png" alt="Format de fișier XLSX" >}}

După cum se poate vedea, această foaie de lucru conține conținut în celulele de la A1 la B2 și o imagine. În plus, celula G13 este în prezent celula activă din foaia de lucru. Acum, să examinăm fișierul xl/worksheets/sheet1.xml pentru a vedea cum sunt reprezentate aceste informații în fișierul XML. Conținutul acestui fișier XML este prezentat mai jos.

{{< figure src="../XLSX File Format Details.png" alt="Format de fișier XPS" >}}

1. Fila are culoarea temei aplicată. Este menționat în fișierul XML cu etichetă<tabColor> urmând id-ul temei.
1. Valoarea tabSelected este setată la 1, ceea ce arată că aceasta este foaia selectată
1. După cum se poate vedea în prima imagine de mai sus, celula G13 din foaia de lucru este o celulă activă, care este menționată și în fișierul XML.
1. Fila sheetData reprezintă datele conținute în foaia de lucru. Cu toate acestea, puteți vedea că conținutul original al foii de lucru nu se află nicăieri în această secțiune. Acest lucru se datorează faptului că textul este referit indirect din foaia XML „sharedStrings”. Această legătură asigură că fiecare text este salvat o singură dată și poate fi referit din nou pentru a economisi spațiu.
1. Imaginea, așa cum se poate vedea, este referită prin id-ul de referință „rId2”

## A contribui

Trebuie să împărtășiți ceva despre formatele de fișiere XLSX sau Spreadsheet? Vă puteți posta constatările în secțiunea [Spreadsheet File Format News](https://news.fileformat.com/t/Spreadsheet).

## Referințe

* [[MS-XLSX] - Format de fișier XLSX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

