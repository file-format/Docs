{
  "date": "2019-12-03",
  "keywords": [
"DOCX",
"fil",
"format",
"filtype",
"udvidelse",
"hvad er en DOCX fil?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DOCX",
  "description": "Lær om DOCX filformat og API'er, der kan oprette og åbne DOCX filer.",
  "linktitle": "DOCX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-doc-dax"
}
},
  "lastmod": "2019-12-03"
}

## Hvad er en DOCX fil? ##

DOCX er et velkendt format til Microsoft Word-dokumenter. Introduceret fra 2007 med udgivelsen af Microsoft Office 2007, blev strukturen af dette nye dokumentformat ændret fra almindelig binær til en kombination af XML og binære filer. Docx-filer kan åbnes med Word 2007 og laterale versioner, men ikke med de tidligere versioner af MS Word, som understøtter DOC-filudvidelser.

## Kort historie ##

After Microsoft opened the specifications for the DOC file format, it was easy for its competitors to reverse engineer the format and provide the same support in their own applications. In addition, the competition from Open Office in the form of its Open Document Format, compelled Microsoft to adopt more open and wide standards. It was in early 2000 when Microsoft decided to go for the change to accommodate the standard for **Office Open XML**. Documents under this new Standard were given [.docx extension](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), the "X" being for XML. By 2007, this new file format became part of Office 2007 and is carried on in the new versions of Microsoft Office as well. The new file type has added advantages of small file sizes, fewer changes of corruption and well-formatted images representation.

## DOCX filformatspecifikationer - flere oplysninger

En Docx-fil består af en samling XML-filer, der er indeholdt i et ZIP-arkiv. Indholdet af et nyt Word-dokument kan ses ved at pakke dets indhold ud. Samlingen indeholder en liste over XML-filer, der er kategoriseret som:

* MetaData-filer - indeholder oplysninger om andre filer, der er tilgængelige i arkivet

* Dokument - indeholder det faktiske indhold af dokumentet


### Metadatafiler ###

Microsoft Word bruger disse filer til at finde forholdet mellem filer og til at finde dokumentindholdet. Når et Word-dokumentarkiv udpakkes, indeholder det en række sådanne filer som beskrevet nedenfor.

#### Relationer - \_rels/.rels ####

Denne fil indeholder information, der fortæller MS Word, hvor man skal lede efter dokumentindholdet og andre referencer. Hver relation identificeres af et unikt relations-id og angiver den refererede XML-fil som mål. En eksempelrelationsfil vises som følger:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Indholdstyper ####

Et dokument kan indeholde flere medietyper indeni såsom billeder, temaer, ordkunst osv. [Content_Types].xml indeholder information om sådanne medietyper, der findes i dokumentet. Indholdet af en sådan XML-fil vises som følger:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Referencer til ressourcer - \_rels/document.xml.rels ####

Der henvises til oplysninger om ressourcer, såsom billeder, der er indlejret i dokumentet, i denne XML-fil.

#### Hoveddokumentets indhold ####

Dette refererer til arkivets XML-hovedfil, der indeholder dokumentets tekstindhold. Dette indhold er repræsenteret af forskellige noder i henhold til OpenOffice XML-specifikationerne. For det meste består indholdet af denne fil af afsnit og tabeller, selvom de også kan være andre noder.

### Filformat noder ###

Hovedfilen document.xml er en samling af noder til repræsentation af det overordnede indhold af en fil. Hver node har en start og en ende, der indkapsler enten yderligere noder eller indholdet. Et forenklet eksempel på en sådan xml-fil er som følger:

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

Følgende er oplysningerne om nogle af noderne indeholdt i en DOCX-fil til repræsentation af indhold.

`<w:document> ` - Repræsenterer rodelementet i filens hovedindhold.

`<w:body> ` - Repræsenterer dokumentets krop, som kan bestå af mange andre elementknudepunkter, såsom afsnit, tabeller og sektioner.

#### Afsnit ####

Et afsnit er hovedindholdsholderen i et dokument. Det er repræsenteret af **<w:p> ** element i et dokument. Et afsnit består yderligere af en eller flere kørsler **<w:r> ** der indeholder den faktiske tekst i afsnittet. Ud over kørsler kan afsnit også indeholde andre dokumentelementer såsom hyperlinks, kommentarer osv. Et eksempel på afsnitsstruktur er som vist nedenfor:

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

## DOCX ofte stillede spørgsmål

 * **Er DOCX en filudvidelse?** - DOCX bruges som filtypenavn til at repræsentere Microsoft Word 2007 og senere filformater, der bruges til at gemme Word-filer. Den fortæller også dit OS, at denne DOCX-fil kræver Microsoft Word 2007 for at åbne den og vise dens ikon.
 * **Er DOCX det samme som Word** - DOCX er et filformat, der bruges af Microsoft Word til at gemme dokumenter i Open XML-format. Word, på den anden side, er en applikationssoftware fra Microsoft Office, der også understøtter andre filformater såsom DOC, DOT, DOTM og andre.
 * **Hvad er forskellen DOC og DOCX** - DOC er en Word-fil, der er gemt i Word 2007 og tidligere filformat. DOCX er baseret på Open XML-filformat, der understøttes af Microsoft 2007 og senere versioner. Se [Forskelle mellem DOC og DOCX](https://blog.fileformat.com/2022/08/11/doc-vs-docx/) for flere detaljer.

## Referencer ##

* [MS - DOCX-filformat](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)

* [Office Open XML](http://officeopenxml.com/)


