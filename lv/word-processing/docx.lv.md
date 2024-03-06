{
  "date": "2019-12-03",
  "keywords": [
"DOCX",
"failu",
"formātā",
"faila tips",
"pagarinājumu",
"kas ir DOCX fails?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DOCX",
  "description": "Uzziniet par DOCX failu formātu un API, kas var izveidot un atvērt DOCX failus.",
  "linktitle": "DOCX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-doc-lvx"
}
},
  "lastmod": "2019-12-03"
}

## Kas ir DOCX fails? ##

DOCX ir plaši pazīstams Microsoft Word dokumentu formāts. Šī jaunā dokumenta formāta struktūra, kas tika ieviesta no 2007. gada, izlaižot Microsoft Office 2007, tika mainīta no vienkārša bināra uz XML un bināro failu kombināciju. Docx failus var atvērt ar Word 2007 un sānu versijām, bet ne ar iepriekšējām MS Word versijām, kas atbalsta DOC failu paplašinājumus.

## Īsa vēsture ##

After Microsoft opened the specifications for the DOC file format, it was easy for its competitors to reverse engineer the format and provide the same support in their own applications. In addition, the competition from Open Office in the form of its Open Document Format, compelled Microsoft to adopt more open and wide standards. It was in early 2000 when Microsoft decided to go for the change to accommodate the standard for **Office Open XML**. Documents under this new Standard were given [.docx extension](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), the "X" being for XML. By 2007, this new file format became part of Office 2007 and is carried on in the new versions of Microsoft Office as well. The new file type has added advantages of small file sizes, fewer changes of corruption and well-formatted images representation.

## DOCX faila formāta specifikācijas — vairāk informācijas

Docx fails sastāv no XML failu kolekcijas, kas atrodas ZIP arhīvā. Jauna Word dokumenta saturu var skatīt, atarhivējot tā saturu. Kolekcijā ir XML failu saraksts, kas ir klasificēti kā:

* MetaData faili – satur informāciju par citiem arhīvā pieejamajiem failiem

* Dokuments - satur faktisko dokumenta saturu


### Metadatu faili ###

Microsoft Word izmanto šos failus, lai atrastu attiecības starp failiem un dokumenta satura atrašanu. Kad tiek izvilkts Word dokumentu arhīvs, tajā ir vairāki šādi faili, kā norādīts tālāk.

#### Attiecības - \_rels/.rels ####

Šajā failā ir informācija, kas MS Word norāda, kur meklēt dokumenta saturu un citas atsauces. Katra relācija tiek identificēta ar unikālu relācijas ID, un tā norāda atsauces XML failu kā mērķi. Attiecību faila paraugs tiek parādīts šādi:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Satura veidi ####

Dokumentā var būt ietverti vairāki multivides veidi, piemēram, attēli, motīvi, teksta mākslas darbi utt. Fails [Content_Types].xml satur informāciju par šādiem dokumentā esošajiem multivides veidiem. Šāda XML faila saturs tiek parādīts šādi:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Atsauces uz resursiem - \_rels/document.xml.rels ####

Informācija par resursiem, piemēram, dokumentā iegultiem attēliem, ir norādīta šajā XML failā.

#### Galvenā dokumenta saturs ####

Tas attiecas uz arhīva galveno XML failu, kurā ir dokumenta teksta saturs. Šis saturs tiek attēlots ar dažādiem mezgliem atbilstoši OpenOffice XML specifikācijām. Lielākoties šī faila saturs sastāv no rindkopām un tabulām, lai gan tie var būt arī citi mezgli.

### Faila formāta mezgli ###

Galvenais document.xml fails ir mezglu kolekcija faila kopējā satura attēlošanai. Katram mezglam ir sākums un beigas, kas iekapsulē vai nu citus mezglus, vai saturu. Šāda xml faila vienkāršots piemērs ir šāds:

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

Tālāk ir sniegta informācija par dažiem mezgliem, kas ietverti DOCX failā satura attēlošanai.

`<w:document> ` — attēlo faila galvenā satura saknes elementu.

`<w:body> ` — attēlo dokumenta pamattekstu, kurā var būt daudz citu elementu mezglu, piemēram, rindkopas, tabulas un sadaļas.

#### Punkti ####

Rindkopa ir galvenais dokumenta satura turētājs. To pārstāv **<w:p> ** elements dokumentā. Tālāk rindkopa sastāv no viena vai vairākiem skrējieniem**<w:r> **, kas satur rindkopas faktisko tekstu. Papildus izpildei rindkopās var būt arī citi dokumenta elementi, piemēram, hipersaites, komentāri utt. Rindkopas struktūras piemērs ir parādīts tālāk:

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

## DOCX FAQ

 * **Vai DOCX ir faila paplašinājums?** — DOCX tiek izmantots kā faila paplašinājums, lai attēlotu Microsoft Word 2007 un jaunākus failu formātus, ko izmanto Word failu glabāšanai. Tas arī informē jūsu OS, ka šim DOCX failam ir nepieciešams Microsoft Word 2007, lai to atvērtu un parādītu tā ikonu.
 * **Vai DOCX ir tāds pats kā Word** — DOCX ir faila formāts, ko Microsoft Word izmanto, lai saglabātu dokumentus Open XML formātā. No otras puses, Word ir Microsoft Office lietojumprogrammatūra, kas atbalsta arī citus failu formātus, piemēram, DOC, DOT, DOTM un citus.
 * **Kāda ir atšķirība DOC un DOCX** - DOC ir Word fails, kas saglabāts Word 2007 un agrākā faila formātā. DOCX pamatā ir Open XML faila formāts, ko atbalsta Microsoft 2007 un jaunākas versijas. Plašāku informāciju skatiet sadaļā [Atšķirības starp DOC un DOCX] (https://blog.fileformat.com/2022/08/11/doc-vs-docx/).

## Atsauces Nr.

* [MS — DOCX faila formāts](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)

* [Office Open XML](http://officeopenxml.com/)


