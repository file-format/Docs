{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ghidul dvs. de format de fișier pentru a afla ce este un fișier _XLSX și API-uri care pot crea și deschide fișiere _XLSX.",
  "title" :"Ce este un fișier _XLSX?",
  "linktitle" : "_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## Ce este un fișier _XLSX?

Un fișier cu extensia .\_xlsx este de fapt un fișier [XLSX](/ro/spreadsheet/xlsx/) care este redenumit de altă aplicație. Acest lucru se poate întâmpla în anumite cazuri când numele fișierului conține un . la sfârșitul numelui fișierului. Fișierele \_XLSX pot fi deschise în Microsoft Excel similar fișierelor XLSX prin redenumirea acestora în extensia .xlsx.

## _XLSX File Format - Mai multe informații

Fișierele _XLSX nu diferă de fișierele XLSX și utilizează standardul Open XML adoptat de Microsoft încă din 2000. Înainte de XLSX, [XLS](/ro/spreadsheet/xls/) era formatul de fișier principal utilizat pentru lucrul cu foile de calcul Excel pentru a salva documente. în format binar. Acest nou format de fișier bazat pe XML a venit cu avantaje precum dimensiunile mici ale fișierelor, rezistența la coruperea fișierelor și reprezentarea imaginilor bine formatate. Acest nou format de fișier bazat pe XML a devenit parte a Office 2007 și este realizat și în noile versiuni ale Microsoft.

## \_XLSX Specificații de format de fișier

Deoarece un fișier \_XLSX este un fișier XLSX redenumit, are aceleași specificații ca fișierul original. Este doar un fișier de arhivă care se bazează pe formatul de fișier de arhivă [ZIP](/ro/compression/zip/). Dacă doriți să vedeți conținutul acestei arhive, trebuie doar să redenumiți fișierul în extensia .zip și să îl extrageți pentru a vedea fișierele constitutive ale acestui registru de lucru Excel. Un registru de lucru gol, atunci când este extras în fișierele sale, are următoarele fișiere și foldere constitutive.

### [Content_Types].xml

Acesta este singurul fișier care se găsește la nivelul de bază atunci când este extras zip-ul. Listează tipurile de conținut pentru părțile din pachet. Toate referințele la fișierele XML incluse în pachet sunt menționate în acest fișier XML.

### \_rels (dosar)

Acesta este folderul Relații care conține un singur fișier XML care stochează relațiile la nivel de pachet. Legăturile către părțile cheie ale fișierelor Xlsx sunt conținute în acest fișier ca URI. Aceste URI-uri identifică tipul de relație a fiecărei părți cheie cu pachetul. Aceasta include relația cu documentul de birou principal situat ca xl/workbook.xml și alte părți din docProps ca proprietăți de bază și extinse.

### docProps

Acest folder conține proprietățile generale ale documentului. Acestea includ un set de proprietăți de bază, un set de proprietăți extinse sau specifice aplicației și o previzualizare în miniatură a documentului. Un registru de lucru gol are două fișiere în acest folder și anume app.xml și core.xml. Core.xml conține informații precum autorul, data creării și salvate și modificate. App.xml conține informații despre conținutul fișierului.

### xl (dosar)

Acesta este folderul principal care conține toate detaliile despre conținutul registrului de lucru. În mod implicit, are următoarele foldere:

* \_rels
*temă
* fișe de lucru

și următoarele fișiere xml:

* styles.xml
* workbook.xml

## Referințe

* [MS-XLSX - Format de fișier .xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

