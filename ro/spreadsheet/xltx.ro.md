{
  "date" : "2019-12-10",
  "keywords" :[ "XLTX", "fișier", "extensie", "format fișier", "Excel Open XML", "Foaie de calcul"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ghidul dvs. de format de fișier pentru a ști ce este un fișier XLTX și API-urile care le pot crea și deschide.",
  "title" :"Ce este un fișier XLTX?",
  "linktitle" : "XLTX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Ce este un fișier XLTX?

Fișierele cu extensia .xltx reprezintă fișiere șablon Microsoft Excel care se bazează pe specificațiile de format de fișier Office OpenXML. Este folosit pentru a crea un fișier șablon standard care poate fi utilizat pentru a genera fișiere [XLSX](/ro/spreadsheet/xlsx/) care prezintă aceleași setări ca cele specificate în fișierul XLTX.

## Scurt istoric

A fost la începutul anilor 2000 când Microsoft a decis să opteze pentru modificarea pentru a se adapta standardului pentru **Office Open XML**. Documentele, de diferite tipuri, conform acestui nou Standard au fost identificate prin adăugarea „X” în extensiile lor, unde „X” fiind pentru XML. Până în 2007, acest nou format de fișier a devenit parte a Office 2007 și este continuat și în noile versiuni ale Microsoft Office. Noul tip de fișier are avantaje adăugate de dimensiuni mici ale fișierelor, mai puține modificări ale corupției și reprezentarea imaginilor bine formatate.

## Specificații pentru formatul fișierului XLTX

Fișierele XLTX se bazează pe formatul de fișier Office OpenXML și folosesc XML și [ZIP](/ro/compression/zip/) pentru a reduce dimensiunea fișierului. A fost creat odată cu lansarea Microsoft Office 2007 pentru a înlocui formatul de fișier binar XLT. Similar cu XLTX, formatul de fișier XLT poate fi folosit pentru a crea fișiere [XLS](/ro/spreadsheet/xls/) folosind Microsoft Excel 2003 și 2007. Acestea pot fi deschise cu Microsoft Excel făcând dublu clic pe fișier. Organizarea fișierelor într-un format de fișier XLTX poate fi observată prin redenumirea fișierului în ZIP și apoi extragerea conținutului acestuia pe disc.

### [Content_Types].xml ###

Acesta este singurul fișier care se găsește la nivelul de bază atunci când este extras zip-ul. Listează tipurile de conținut pentru părțile din pachet. Toate referințele la fișierele XML incluse în pachet sunt menționate în acest fișier XML.

### \_rels (dosar) ###

Acesta este folderul Relații care conține un singur fișier XML care stochează relațiile la nivel de pachet. Legăturile către părțile cheie ale fișierelor Xltx sunt conținute în acest fișier ca URI. Aceste URI-uri identifică tipul de relație a fiecărei părți cheie cu pachetul. Aceasta include relația cu documentul de birou principal situat ca xl/workbook.xml și alte părți din docProps ca proprietăți de bază și extinse.

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

## Referințe ##

* [[MS-XLSX] - Format de fișier .Xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

