{
  "date" : "2019-12-13",
  "keywords" :[ "fișier pptx", "format fișier pptx", "ce este un fișier pptx", "fișier", "exemplu pptx", "extensie fișier pptx", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier PPTX și despre API-urile care pot crea și deschide fișiere PPTX.",
  "title" :"PPTX - Format de fișier de prezentare PowerPoint",
  "linktitle" : "PPTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier PPTX?

Fișierele cu extensia PPTX sunt fișiere de prezentare create cu aplicația populară Microsoft PowerPoint. Spre deosebire de versiunea anterioară a formatului de fișier de prezentare PPT, care era binar, formatul PPTX se bazează pe formatul de fișier de prezentare XML deschis Microsoft PowerPoint. Un fișier de prezentare este o colecție de diapozitive în care fiecare diapozitiv poate cuprinde text, imagini, formatare, animații și alte medii. Aceste diapozitive sunt prezentate publicului sub formă de prezentări de diapozitive cu setări de prezentare personalizate.

## Scurt istoric

Formatul de fișier PPTX a fost introdus în 2007 și folosește standardul Open XML adaptat de Microsoft încă din 2000. Înainte de PPTX, formatul de fișier comun folosit era PPT, care era format de fișier binar pur. Noul tip de fișier are avantaje adăugate de dimensiuni mici ale fișierelor, mai puține modificări ale corupției și reprezentarea imaginilor bine formatate. A fost la începutul anilor 2000 când Microsoft a decis să opteze pentru modificarea pentru a se adapta standardului pentru **Office Open XML**. Până în 2007, acest nou format de fișier a devenit parte a Office 2007 și este continuat și în noile versiuni ale Microsoft Office.

## Specificații de format de fișier PPTX

Fișierele generate cu formatul de fișier Office Open XML sunt o colecție de fișiere XML împreună cu alte fișiere care oferă legături între toate fișierele constitutive. Această colecție este de fapt o arhivă comprimată care poate fi extrasă pentru a-și vizualiza conținutul. Pentru a face acest lucru, trebuie doar să redenumiți extensia de fișier PPTX cu zip și să o extrageți pentru a-i observa conținutul (consultați [Specificațiile formatului fișierului PPTX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-pptx/) efd8bb2d-d888-4e2e-af25-cad476730c9f) de la Microsoft).

Următoarele secțiuni aruncă puțină lumină asupra fiecăruia dintre acestea.

### [Content_Types].xml

Acesta este singurul fișier care se găsește la nivelul de bază atunci când este extras zip-ul. Listează tipurile de conținut pentru părțile din pachet. Toate referințele la fișierele XML incluse în pachet sunt menționate în acest fișier XML. Următorul este un tip de conținut pentru o parte de diapozitiv:

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

Dacă trebuie adăugate noi părți la pachet, se poate face prin adăugarea noii părți și actualizarea oricăror relații din fișierele .rels. Trebuie reținut că pentru o astfel de modificare, Content_Types.xml trebuie de asemenea actualizat.

### \_rels (dosar) ###

Relațiile dintre celelalte părți și resursele din afara pachetului sunt menținute de partea de relații. Dosarul Relații conține un singur fișier XML care stochează relațiile la nivel de pachet. Legăturile către părțile cheie ale fișierelor PPTX sunt conținute în acest fișier ca URI. Aceste URI-uri identifică tipul de relație a fiecărei părți cheie cu pachetul. Aceasta include relația cu documentul de birou principal situat ca ppt/presentation.xml și alte părți din docProps ca proprietăți de bază și extinse.

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```

Fiecare parte a documentului care este sursa uneia sau mai multor relații va avea propria sa parte de relații în care fiecare astfel de parte a relației se găsește într-un subdosar \_rels al părții și este denumită prin adăugarea „.rels” la numele părții. parte. Partea principală de conținut (presentation.xml) are propria sa parte de relații (presentation.xml.rels). Conține relații cu alte părți ale conținutului, cum ar fi slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, precum și URI-urile pentru link-uri externe.

#### Relație explicită ####

Pentru o relație explicită, o resursă este referită folosind atributul Id al lui a<Relationship> element. Adică, ID-ul din sursă se mapează direct la un ID al unui element de relație, cu o referință explicită la țintă.

De exemplu, un diapozitiv poate conține un hyperlink ca acesta:

```
<a:hlinkClick r:id#"rId2">
```

r:id#"rId2" face referire la următoarea relație din partea de relații pentru diapozitiv (slide1.xml.rels).

```
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
```

#### Relație implicită ####

Pentru o relație implicită, nu există o astfel de referință directă la un `<Relationship> Id`. În schimb, referința este înțeleasă.

### ppt Folder ###

Acesta este folderul principal care conține toate detaliile despre conținutul Prezentării. În mod implicit, are următoarele foldere:

* \_rels
*temă
* diapozitive
* slideLayouts
* slideMasters

și următoarele fișiere xml:

* prezentare.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## Referințe ##

* [[MS-PPTX] - Format fișier PPTX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

