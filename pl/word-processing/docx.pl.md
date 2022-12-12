{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX", "plik", "format", "typ pliku", "rozszerzenie", "co to jest plik DOCX?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"Poznaj format plików DOCX i interfejsy API, które mogą tworzyć i otwierać pliki DOCX.",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Czym jest plik DOCX? ##

DOCX to dobrze znany format dokumentów programu Microsoft Word. Wprowadzony od 2007 roku wraz z wydaniem pakietu Microsoft Office 2007, struktura tego nowego formatu dokumentu została zmieniona ze zwykłego pliku binarnego na kombinację plików XML i plików binarnych. Pliki Docx można otwierać w programie Word 2007 i wersjach nowszych, ale nie we wcześniejszych wersjach programu MS Word, które obsługują rozszerzenia plików DOC.

## Krótka historia ##

Po tym, jak Microsoft otworzył specyfikację formatu pliku DOC, jego konkurenci z łatwością mogli dokonać inżynierii wstecznej formatu i zapewnić taką samą obsługę we własnych aplikacjach. Ponadto konkurencja ze strony Open Office w postaci Open Document Format zmusiła Microsoft do przyjęcia bardziej otwartych i szerokich standardów. Na początku 2000 roku firma Microsoft zdecydowała się na zmianę w celu dostosowania do standardu **Office Open XML**. Dokumenty objęte tym nowym standardem otrzymały [rozszerzenie .docx](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), znak „X” jest dla XML. Do 2007 roku ten nowy format plików stał się częścią pakietu Office 2007 i jest również stosowany w nowych wersjach pakietu Microsoft Office. Nowy typ pliku ma dodatkowe zalety w postaci małych rozmiarów plików, mniejszej liczby zmian powodujących uszkodzenie i dobrze sformatowanej reprezentacji obrazów.

## Specyfikacje formatu plików DOCX — więcej informacji

Plik Docx składa się z kolekcji plików XML zawartych w archiwum ZIP. Zawartość nowego dokumentu programu Word można wyświetlić, rozpakowując jego zawartość. Kolekcja zawiera listę plików XML, które są sklasyfikowane jako:

* Pliki metadanych - zawiera informacje o innych plikach dostępnych w archiwum
* Dokument - zawiera rzeczywistą treść dokumentu

### Pliki metadanych ###

Program Microsoft Word używa tych plików do znajdowania relacji między plikami i lokalizowania zawartości dokumentu. Po rozpakowaniu archiwum dokumentów programu Word zawiera ono pewną liczbę takich plików, jak opisano poniżej.

#### Relacje - \_rels/.rels ####

Ten plik zawiera informacje, które mówią MS Word, gdzie szukać zawartości dokumentu i innych odniesień. Każda relacja jest identyfikowana przez unikalny identyfikator relacji i określa plik XML, do którego się odwołuje, jako cel. Przykładowy plik relacji jest pokazany w następujący sposób:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Typy treści ####

Dokument może zawierać kilka typów multimediów, takich jak obrazy, motywy, grafiki tekstowe itp. Plik [Content_Types].xml zawiera informacje o typach multimediów obecnych w dokumencie. Zawartość takiego pliku XML przedstawia się następująco:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Odwołania do zasobów — \_rels/document.xml.rels ####

Informacje o zasobach, takie jak obrazy osadzone w dokumencie, znajdują się w tym pliku XML.

#### Główna zawartość dokumentu ####

Odnosi się to do głównego pliku XML archiwum, który zawiera treść tekstową dokumentu. Ta zawartość jest reprezentowana przez różne węzły zgodnie ze specyfikacją OpenOffice XML. W większości zawartość tego pliku składa się z akapitów i tabel, chociaż mogą to być również inne węzły.

### Węzły formatu pliku ###

Główny plik document.xml to zbiór węzłów reprezentujących ogólną zawartość pliku. Każdy węzeł ma początek i koniec, który obejmuje dalsze węzły lub zawartość. Uproszczony przykład takiego pliku xml jest następujący:

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

Poniżej przedstawiono informacje o niektórych węzłach zawartych w pliku DOCX do reprezentacji zawartości.

`<w:document> ` — reprezentuje główny element głównej zawartości pliku.

`<w:body> ` — Reprezentuje treść dokumentu, która może składać się z wielu innych węzłów elementów, takich jak akapity, tabele i sekcje.

#### Akapity ####

Akapit jest głównym nośnikiem treści w dokumencie. Jest reprezentowany przez **<w:p> ** element w dokumencie. Akapit składa się ponadto z jednego lub więcej przebiegów **<w:r> ** który zawiera aktualny tekst akapitu. Oprócz przebiegów akapity mogą zawierać również inne elementy dokumentu, takie jak hiperłącza, komentarze itp. Przykładowa struktura akapitu jest pokazana poniżej:

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

## Bibliografia ##

* [Format pliku MS — DOCX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML](http://officeopenxml.com/)

