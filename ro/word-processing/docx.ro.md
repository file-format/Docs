{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX","fișier", "format", "tip fișier", "extensie","ce este un fișier DOCX?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"Aflați despre formatul de fișier DOCX și despre API-urile care pot crea și deschide fișiere DOCX.",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Ce este un fișier DOCX? ##

DOCX este un format binecunoscut pentru documentele Microsoft Word. Introdusă din 2007 odată cu lansarea Microsoft Office 2007, structura acestui nou format de document a fost schimbată de la binar simplu la o combinație de fișiere XML și binare. Fișierele Docx pot fi deschise cu Word 2007 și versiunile laterale, dar nu și cu versiunile anterioare de MS Word care acceptă extensii de fișiere DOC.

## Scurt istoric ##

După ce Microsoft a deschis specificațiile pentru formatul de fișier DOC, a fost ușor pentru concurenții săi să facă inginerie inversă a formatului și să ofere același suport în propriile aplicații. În plus, concurența de la Open Office sub forma sa Open Document Format, a obligat Microsoft să adopte standarde mai deschise și mai ample. A fost la începutul anului 2000 când Microsoft a decis să opteze pentru modificarea pentru a se adapta standardului pentru **Office Open XML**. Documentele conform acestui nou standard au primit [extensia .docx](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), „X” fiind pentru XML. Până în 2007, acest nou format de fișier a devenit parte a Office 2007 și este continuat și în noile versiuni ale Microsoft Office. Noul tip de fișier a adăugat avantaje de dimensiuni mici ale fișierelor, mai puține modificări ale corupției și reprezentarea imaginilor bine formatate.

## Specificații format fișier DOCX - Mai multe informații

Un fișier Docx constă dintr-o colecție de fișiere XML care sunt conținute într-o arhivă ZIP. Conținutul unui document Word nou poate fi vizualizat prin dezarhivarea conținutului acestuia. Colecția conține o listă de fișiere XML care sunt clasificate astfel:

* Fișiere metadate - conține informații despre alte fișiere disponibile în arhivă
* Document - conține conținutul real al documentului

### Fișiere de metadate ###

Microsoft Word utilizează aceste fișiere pentru a găsi relația dintre fișiere și pentru a localiza conținutul documentului. Când o arhivă de documente Word este extrasă, aceasta conține un număr de astfel de fișiere, așa cum este detaliat mai jos.

#### Relații - \_rels/.rels ####

Acest fișier conține informații care îi indică lui MS Word unde să caute conținutul documentului și alte referințe. Fiecare relație este identificată printr-un ID unic de relație și specifică fișierul XML referit ca țintă. Un exemplu de fișier de relații este afișat după cum urmează:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Tipuri de conținut ####

Un document poate conține mai multe tipuri de media în interior, cum ar fi imagini, teme, word art etc. [Content_Types].xml conține informații despre astfel de tipuri de media prezente în document. Conținutul unui astfel de fișier XML este afișat după cum urmează:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Referințe la resurse - \_rels/document.xml.rels ####

Informațiile despre resurse, cum ar fi imaginile încorporate în document, sunt menționate în acest fișier XML.

#### Conținutul documentului principal ####

Aceasta se referă la fișierul XML principal al arhivei care conține conținutul text al documentului. Acest conținut este reprezentat de o varietate de noduri conform specificațiilor OpenOffice XML. În cea mai mare parte, conținutul acestui fișier este format din Paragrafe și Tabele, deși acestea pot fi și alte noduri.

### Noduri de format de fișier ###

Fișierul principal document.xml este o colecție de noduri pentru reprezentarea conținutului general al unui fișier. Fiecare nod are un început și un sfârșit care încapsulează fie noduri suplimentare, fie conținutul. Un exemplu simplificat al unui astfel de fișier xml este următorul:

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

Următoarele sunt informații despre unele dintre nodurile conținute într-un fișier DOCX pentru reprezentarea conținutului.

`<w:document> ` - Reprezintă elementul rădăcină al conținutului principal al fișierului.

`<w:body> ` - Reprezintă corpul documentului care poate cuprinde multe alte noduri de elemente, cum ar fi paragrafe, tabele și secțiuni.

#### Paragrafe ####

Un paragraf este principalul deținător de conținut al unui document. Este reprezentat de **<w:p> ** element dintr-un document. Un paragraf mai constă din una sau mai multe runde **<w:r> ** care conține textul propriu-zis al paragrafului. Pe lângă rulări, paragrafele pot conține și alte elemente ale documentului, cum ar fi hyperlinkuri, comentarii etc. Un exemplu de structură de paragraf este prezentat mai jos:

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## Referințe ##

* [MS - Format de fișier DOCX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML](http://officeopenxml.com/)

