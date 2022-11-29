{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX","fil", "format", "filtyp", "tillägg","vad är en DOCX-fil?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"Läs mer om DOCX-filformat och API:er som kan skapa och öppna DOCX-filer.",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Vad är en DOCX fil? ##

DOCX är ett välkänt format för Microsoft Word-dokument. Introducerad från 2007 med lanseringen av Microsoft Office 2007, ändrades strukturen för detta nya dokumentformat från vanligt binärt till en kombination av XML och binära filer. Docx-filer kan öppnas med Word 2007 och laterala versioner men inte med de tidigare versionerna av MS Word som stöder DOC-filtillägg.

## Kortfattad bakgrund ##

Efter att Microsoft öppnade specifikationerna för DOC-filformatet var det lätt för sina konkurrenter att omvända formatet och ge samma stöd i sina egna applikationer. Dessutom tvingade konkurrensen från Open Office i form av dess Open Document Format, Microsoft att anta mer öppna och breda standarder. Det var i början av 2000 när Microsoft bestämde sig för att gå för förändringen för att tillgodose standarden för **Office Open XML**. Dokument under denna nya standard fick [.docx-tillägg](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), "X" vara för XML. År 2007 blev detta nya filformat en del av Office 2007 och används även i de nya versionerna av Microsoft Office. Den nya filtypen har lagt till fördelarna med små filstorlekar, färre ändringar av korruption och välformaterad bildrepresentation.

## DOCX filformatspecifikationer - Mer information

En Docx-fil består av en samling XML-filer som finns i ett ZIP-arkiv. Innehållet i ett nytt Word-dokument kan ses genom att packa upp dess innehåll. Samlingen innehåller en lista över XML-filer som är kategoriserade som:

* MetaData Files - innehåller information om andra filer som finns tillgängliga i arkivet
* Dokument - innehåller det faktiska innehållet i dokumentet

### Metadatafiler ###

Microsoft Word använder dessa filer för att hitta förhållandet mellan filer och för att hitta dokumentinnehållet. När ett Word-dokumentarkiv extraheras innehåller det ett antal sådana filer som beskrivs nedan.

#### Relationer - \_rels/.rels ####

Den här filen innehåller information som talar om för MS Word var man ska leta efter dokumentinnehållet och andra referenser. Varje relation identifieras av ett unikt relations-id och anger den refererade XML-filen som mål. Ett exempel på relationsfil visas som följer:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Innehållstyper ####

Ett dokument kan innehålla flera mediatyper inuti som bilder, teman, ordkonst, etc. [Content_Types].xml innehåller information om sådana mediatyper som finns i dokumentet. Innehållet i en sådan XML-fil visas som följer:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Referenser till resurser - \_rels/document.xml.rels ####

Information om resurser, såsom bilder inbäddade i dokumentet, hänvisas till i denna XML-fil.

#### Huvuddokumentets innehåll ####

Detta hänvisar till den huvudsakliga XML-filen i arkivet som innehåller dokumentets textinnehåll. Detta innehåll representeras av olika noder enligt OpenOffice XML-specifikationerna. Mestadels består innehållet i den här filen av stycken och tabeller, även om de också kan vara andra noder.

### Filformatnoder ###

Huvudfilen document.xml är en samling noder för representation av det övergripande innehållet i en fil. Varje nod har en start och ett slut som kapslar in antingen ytterligare noder eller innehållet. Ett förenklat exempel på en sådan xml-fil är följande:

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

Följande är informationen om några av noderna som finns i en DOCX-fil för representation av innehåll.

`<w:document> ` - Representerar rotelementet i filens huvudinnehåll.

`<w:body> ` - Representerar dokumentets brödtext som kan bestå av många andra elementnoder som stycken, tabeller och sektioner.

#### Stycken ####

Ett stycke är huvudinnehållsinnehavaren i ett dokument. Det representeras av **<w:p> ** element i ett dokument. Ett stycke består vidare av en eller flera körningar **<w:r> ** som innehåller själva texten i stycket. Förutom körningar kan stycken även innehålla andra dokumentelement som hyperlänkar, kommentarer etc. Ett exempel på styckestruktur är som visas nedan:

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

## Referenser ##

* [MS - DOCX-filformat](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML](http://officeopenxml.com/)

