{
  "date" : "2019-10-11",
  "keywords" :[ "fișier ppsm", "format fișier ppsm", "ce este un fișier ppsm", "fișier", "exemplu ppsm", "extensie fișier ppsm", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPSM - Fișier de prezentare PowerPoint activat pentru macro",
  "description":"Aflați despre formatul de fișier PPSM și despre API-urile care pot crea și deschide fișiere PPSM.",
  "linktitle" : "PPSM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier PPSM?

Fișierele cu extensia PPSM reprezintă formatul de fișier de prezentare de diapozitive activat pentru macro creat cu Microsoft PowerPoint 2007 sau o versiune ulterioară. Un alt format de fișier similar este [PPTM](/ro/presentation/pptm/), care diferă în deschiderea cu Microsoft PowerPoint în format editabil în loc să ruleze ca prezentare de diapozitive. Când este rulat ca prezentare de diapozitive, fișierul PPSM arată diapozitivele de prezentare cu conținutul intact în prezentarea de diapozitive și este în mod implicit doar citire. Fișierele PPSM pot fi editate în continuare în Microsoft PowerPoint, deschizându-le în PowerPoint.

## Tipul fisierului ##

Formatul de fișier PPSM a fost introdus cu PowerPoint 2007 și se bazează pe formatul de fișier OpenXML care utilizează o combinație de XML și [ZIP](/ro/compression/zip/) pentru a-și stoca conținutul. Fișierele generate cu formatul de fișier Office Open XML sunt o colecție de fișiere XML împreună cu alte fișiere care oferă legături între toate fișierele constitutive. Această colecție este de fapt o arhivă comprimată care poate fi extrasă pentru a-și vizualiza conținutul. Pentru a face acest lucru, trebuie doar să redenumiți extensia fișierului PPSM cu zip și să o extrageți pentru a-i observa conținutul.

Următoarele secțiuni aruncă puțină lumină asupra fiecăruia dintre acestea.

### [Content_Types].xml ###

Acesta este singurul fișier care se găsește la nivelul de bază atunci când este extras zip-ul. Listează tipurile de conținut pentru părțile din pachet. Toate referințele la fișierele XML incluse în pachet sunt menționate în acest fișier XML. Următorul este un tip de conținut pentru o parte de diapozitiv:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Dacă trebuie adăugate noi părți la pachet, se poate face prin adăugarea noii părți și actualizarea oricăror relații din fișierele .rels. Trebuie reținut că pentru o astfel de modificare, Content_Types.xml trebuie de asemenea actualizat.

### \_rels (dosar) ###

Relațiile dintre celelalte părți și resursele din afara pachetului sunt menținute de partea de relații. Dosarul Relații conține un singur fișier XML care stochează relațiile la nivel de pachet. Legăturile către părțile cheie ale fișierelor de prezentare sunt conținute în acest fișier ca URI. Aceste URI-uri identifică tipul de relație a fiecărei părți cheie cu pachetul. Aceasta include relația cu documentul de birou principal situat ca ppt/presentation.xml și alte părți din docProps ca proprietăți de bază și extinse.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
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
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
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

* [Format fișier de prezentare OpenXML](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

