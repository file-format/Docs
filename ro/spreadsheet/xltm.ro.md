{
  "date" : "2019-12-10",
  "keywords" :[ "XLTM", "fișier", "extensie", "format fișier", "Excel Open XML Macro", "Foaie de calcul" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ghidul dvs. de format de fișier pentru a afla ce este un fișier XLTM și API-urile care le pot crea și deschide.",
  "title" :"Ce este un fișier XLTM?",
  "linktitle" : "XLTM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Ce este un fișier XLTM?

Extensia de fișier XLTM reprezintă fișiere care sunt generate de Microsoft Excel ca fișiere șablon activate pentru Macro. Fișierele XLTM sunt similare cu [XLTX](/ro/spreadsheet/xltx/) în altă structură decât aceea că mai târziu nu acceptă crearea de fișiere șablon cu macrocomenzi. Astfel de fișiere șablon sunt folosite pentru a genera și a seta aspectul, formatarea și alte setări împreună cu macrocomenzi pentru a facilita crearea de fișiere XLSX similare.

## Scurt istoric ##

A fost la începutul anilor 2000 când Microsoft a decis să opteze pentru modificarea pentru a se adapta standardului pentru **Office Open XML**. Documentele, de diferite tipuri, conform acestui nou Standard au fost identificate prin adăugarea „X” în extensiile lor, unde „X” fiind pentru XML. Până în 2007, acest nou format de fișier a devenit parte a Office 2007 și este continuat și în noile versiuni ale Microsoft Office. Noul tip de fișier are avantaje adăugate de dimensiuni mici ale fișierelor, mai puține modificări ale corupției și reprezentarea imaginilor bine formatate.

## Specificații pentru formatul fișierului XLTM ##

Fișierele XLTM se bazează pe formatul de fișier Office OpenXML și folosesc XML și [ZIP](/ro/compression/zip/) pentru a reduce dimensiunea fișierului. Acestea pot fi deschise cu Microsoft Excel făcând dublu clic pe fișier. Organizarea fișierelor într-un format de fișier XLTM poate fi observată prin redenumirea fișierului în ZIP și apoi extragerea conținutului acestuia pe disc.

### [Content_Types].xml ###

Acesta este singurul fișier care se găsește la nivelul de bază atunci când este extras zip-ul. Listează tipurile de conținut pentru părțile din pachet. Toate referințele la fișierele XML incluse în pachet sunt menționate în acest fișier XML.

### \_rels (dosar) ###

Acesta este folderul Relații care conține un singur fișier XML care stochează relațiile la nivel de pachet. Legăturile către părțile cheie ale fișierelor Xltx sunt conținute în acest fișier ca URI. Aceste URI-uri identifică tipul de relație a fiecărei părți cheie cu pachetul. Aceasta include relația cu documentul de birou principal situat ca xl/workbook.xml și alte părți din docProps ca proprietăți de bază și extinse.

### docProps ###

Acest folder conține proprietățile generale ale documentului. Acestea includ un set de proprietăți de bază, un set de proprietăți extinse sau specifice aplicației și o previzualizare în miniatură a documentului. Un registru de lucru gol are două fișiere în acest folder și anume app.xml și core.xml. Core.xml conține informații precum autor, data creării și salvate și modificate. App.xml conține informații despre conținutul fișierului.

### xl (dosar) ###

Acesta este folderul principal care conține toate detaliile despre conținutul registrului de lucru. În mod implicit, are următoarele foldere:

* \_rels
*temă
* fișe de lucru

și următoarele fișiere xml:

* styles.xml
* workbook.xml

## Referințe ##

* [Format de fișier MS-XLSX](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

