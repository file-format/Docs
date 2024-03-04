{
  "date": "2019-12-03",
  "keywords": [
"DOCX",
"failą",
"formatu",
"Failo tipas",
"pratęsimas",
"kas yra DOCX failas?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DOCX",
  "description": "Sužinokite apie DOCX failo formatą ir API, kurios gali kurti ir atidaryti DOCX failus.",
  "linktitle": "DOCX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-doc-ltx"
}
},
  "lastmod": "2019-12-03"
}

## Kas yra DOCX failas? ##

DOCX yra gerai žinomas Microsoft Word dokumentų formatas. Pradėtas naudoti nuo 2007 m., kai buvo išleista Microsoft Office 2007, šio naujojo dokumento formato struktūra buvo pakeista iš paprasto dvejetainio į XML ir dvejetainių failų derinį. Docx failus galima atidaryti naudojant Word 2007 ir šonines versijas, bet ne ankstesnes MS Word versijas, kurios palaiko DOC failų plėtinius.

## Trumpa istorija ##

After Microsoft opened the specifications for the DOC file format, it was easy for its competitors to reverse engineer the format and provide the same support in their own applications. In addition, the competition from Open Office in the form of its Open Document Format, compelled Microsoft to adopt more open and wide standards. It was in early 2000 when Microsoft decided to go for the change to accommodate the standard for **Office Open XML**. Documents under this new Standard were given [.docx extension](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), the "X" being for XML. By 2007, this new file format became part of Office 2007 and is carried on in the new versions of Microsoft Office as well. The new file type has added advantages of small file sizes, fewer changes of corruption and well-formatted images representation.

## DOCX failo formato specifikacijos – daugiau informacijos

Docx failą sudaro XML failų rinkinys, kuris yra ZIP archyve. Naujo Word dokumento turinį galima peržiūrėti išpakavus jo turinį. Kolekcijoje yra sąrašas XML failų, kurie skirstomi į:

* MetaData Files – yra informacijos apie kitus archyve esančius failus

* Dokumentas – pateikiamas tikrasis dokumento turinys


### Metaduomenų failai ###

Microsoft Word naudoja šiuos failus, kad surastų ryšį tarp failų ir rastų dokumento turinį. Kai ištraukiamas Word dokumentų archyvas, jame yra daug tokių failų, kaip aprašyta toliau.

#### Santykiai – \_rels/.rels ####

Šiame faile yra informacijos, kuri nurodo MS Word, kur ieškoti dokumento turinio ir kitų nuorodų. Kiekvienas ryšys identifikuojamas pagal unikalų ryšio ID ir nurodo nurodytą XML failą kaip tikslą. Ryšio failo pavyzdys rodomas taip:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Turinio tipai ####

Dokumente gali būti kelių tipų laikmenos, pvz., vaizdai, temos, Word Art ir kt. [Content_Types].xml yra informacijos apie tokius dokumente esančius medijos tipus. Tokio XML failo turinys rodomas taip:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Nuorodos į išteklius – \_rels/document.xml.rels ####

Informacija apie išteklius, pvz., į dokumentą įterptus vaizdus, pateikiama šiame XML faile.

#### Pagrindinio dokumento turinys ####

Tai reiškia pagrindinį archyvo XML failą, kuriame yra dokumento teksto turinys. Šis turinys pateikiamas įvairiais mazgais pagal OpenOffice XML specifikacijas. Dažniausiai šio failo turinį sudaro pastraipos ir lentelės, tačiau tai gali būti ir kiti mazgai.

### Failo formato mazgai ###

Pagrindinis document.xml failas yra mazgų rinkinys, skirtas bendram failo turiniui pateikti. Kiekvienas mazgas turi pradžią ir pabaigą, kurios apima arba kitus mazgus, arba turinį. Supaprastintas tokio xml failo pavyzdys yra toks:

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

Toliau pateikiama informacija apie kai kuriuos mazgus, esančius DOCX faile, skirtoje turiniui pateikti.

`<w:document> ` – žymi pagrindinio failo turinio šakninį elementą.

`<w:body> ` – atspindi dokumento turinį, kurį gali sudaryti daug kitų elementų mazgų, tokių kaip pastraipos, lentelės ir skyriai.

#### Pastraipos ####

Pastraipa yra pagrindinis dokumento turinio turėtojas. Jį atstovauja **<w:p> ** elementas dokumente. Be to, pastraipą sudaro vienas ar daugiau eilių**<w:r> **, kuriame yra tikrasis pastraipos tekstas. Be paleidimų, pastraipose taip pat gali būti kitų dokumento elementų, pvz., hipersaitų, komentarų ir kt. Pastraipos struktūros pavyzdys yra toks, kaip parodyta toliau:

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

## DOCX DUK

 * **Ar DOCX yra failo plėtinys?** – DOCX naudojamas kaip failo plėtinys, vaizduojantis Microsoft Word 2007 ir naujesnius failų formatus, naudojamus Word failams saugoti. Ji taip pat praneša jūsų OS, kad norint atidaryti šį DOCX failą ir parodyti jo piktogramą, reikia Microsoft Word 2007.
 * **Ar DOCX yra tas pats kaip Word** – DOCX yra failo formatas, naudojamas Microsoft Word dokumentams išsaugoti Open XML formatu. Kita vertus, Word yra Microsoft Office taikomoji programinė įranga, kuri taip pat palaiko kitus failų formatus, tokius kaip DOC, DOT, DOTM ir kt.
 * **Kuo skiriasi DOC ir DOCX** – DOC yra Word failas, išsaugotas Word 2007 ir ankstesniuose failų formatuose. DOCX yra pagrįstas Open XML failo formatu, kurį palaiko Microsoft 2007 ir naujesnės versijos. Norėdami gauti daugiau informacijos, žr. [DOC ir DOCX skirtumai](https://blog.fileformat.com/2022/08/11/doc-vs-docx/).

## Nuorodos Nr.

* [MS – DOCX failo formatas](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)

* [Office Open XML](http://officeopenxml.com/)


