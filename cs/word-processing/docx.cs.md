{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX","soubor", "formát", "typ souboru", "přípona","co je soubor DOCX?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"Další informace o formátu souborů DOCX a rozhraních API, která mohou vytvářet a otevírat soubory DOCX.",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Co je soubor DOCX? ##

DOCX je dobře známý formát pro dokumenty Microsoft Word. Zaváděný od roku 2007 s vydáním Microsoft Office 2007, struktura tohoto nového formátu dokumentu byla změněna z prostého binárního na kombinaci XML a binárních souborů. Soubory Docx lze otevřít pomocí aplikace Word 2007 a laterálních verzí, ale nikoli pomocí dřívějších verzí MS Word, které podporují přípony souborů DOC.

## Stručná historie ##

Poté, co Microsoft otevřel specifikace pro formát souboru DOC, bylo pro jeho konkurenty snadné zpětně analyzovat formát a poskytovat stejnou podporu ve svých vlastních aplikacích. Konkurence Open Office v podobě formátu Open Document Format navíc přinutila Microsoft přijmout otevřenější a širší standardy. Bylo to počátkem roku 2000, kdy se Microsoft rozhodl přistoupit ke změně, aby vyhovoval standardu pro **Office Open XML**. Dokumentům podle tohoto nového standardu byla přidělena [přípona .docx](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), „X“ být pro XML. V roce 2007 se tento nový formát souborů stal součástí sady Office 2007 a je používán i v nových verzích sady Microsoft Office. Nový typ souboru přidal výhody malých velikostí souborů, méně změn poškození a dobře formátované reprezentace obrázků.

## Specifikace formátu souboru DOCX – Další informace

Soubor Docx se skládá z kolekce souborů XML, které jsou obsaženy v archivu ZIP. Obsah nového dokumentu aplikace Word lze zobrazit rozbalením jeho obsahu. Kolekce obsahuje seznam souborů XML, které jsou kategorizovány jako:

* Soubory metadat – obsahuje informace o dalších souborech dostupných v archivu
* Dokument – obsahuje skutečný obsah dokumentu

### Soubory metadat ###

Aplikace Microsoft Word používá tyto soubory k nalezení vztahu mezi soubory a k vyhledání obsahu dokumentu. Když je archiv dokumentu Word extrahován, obsahuje řadu takových souborů, jak je popsáno níže.

#### Vztahy - \_rels/.rels ####

Tento soubor obsahuje informace, které říkají MS Word, kde hledat obsah dokumentu a další odkazy. Každý vztah je identifikován jedinečným ID vztahu a určuje odkazovaný soubor XML jako cíl. Vzorový soubor vztahu je zobrazen následovně:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Typy obsahu ####

Dokument může uvnitř obsahovat několik typů médií, jako jsou obrázky, témata, word art atd. Soubor [Content_Types].xml obsahuje informace o takových typech médií přítomných v dokumentu. Obsah takového souboru XML je zobrazen následovně:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Odkazy na zdroje - \_rels/document.xml.rels ####

V tomto souboru XML se odkazuje na informace o zdrojích, jako jsou obrázky vložené do dokumentu.

#### Obsah hlavního dokumentu ####

To se týká hlavního souboru XML archivu, který obsahuje textový obsah dokumentu. Tento obsah je reprezentován řadou uzlů podle specifikací OpenOffice XML. Obsah tohoto souboru se většinou skládá z odstavců a tabulek, i když to mohou být i jiné uzly.

### Uzly formátu souboru ###

Hlavní soubor document.xml je kolekce uzlů pro reprezentaci celkového obsahu souboru. Každý uzel má začátek a konec, který zapouzdřuje buď další uzly, nebo obsah. Zjednodušený příklad takového souboru xml je následující:

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

Následují informace o některých uzlech obsažených v souboru DOCX pro reprezentaci obsahu.

`<w:document> ` - Představuje kořenový prvek hlavního obsahu souboru.

`<w:body> ` - Představuje tělo dokumentu, které může obsahovat mnoho dalších uzlů prvků, jako jsou odstavce, tabulky a oddíly.

#### Odstavce ####

Odstavec je hlavním držitelem obsahu v dokumentu. Je reprezentován **<w:p> ** prvek v dokumentu. Odstavec se dále skládá z jednoho nebo více běhů **<w:r> ** který obsahuje skutečný text odstavce. Kromě běhů mohou odstavce obsahovat také další prvky dokumentu, jako jsou hypertextové odkazy, komentáře atd. Příklad struktury odstavce je uveden níže:

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

## Reference ##

* [formát souboru MS – DOCX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML] (http://officeopenxml.com/)

