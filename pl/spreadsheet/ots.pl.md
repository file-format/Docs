{
  "date" : "2019-12-16",
  "keywords" :["OTS", "plik", "rozszerzenie", "format pliku", "Excel", "Arkusz kalkulacyjny" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format plików OTS i interfejsy API, które mogą tworzyć i otwierać pliki OTS.",
  "title" :"OTS — format pliku szablonu arkusza kalkulacyjnego OpenDocument",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## Czym jest plik OTS?

Plik z rozszerzeniem .ots to plik szablonu arkusza kalkulacyjnego OpenDocument, który jest tworzony za pomocą aplikacji Calc zawartej w Apache OpenOffice. Oprogramowanie Calc jest podobne do programu Excel dostępnego w pakiecie Microsoft Office. Format pliku OTS służy do tworzenia szablonów zawierających wstępnie zdefiniowane ustawienia związane ze stylami, czcionką, danymi, układem arkusza kalkulacyjnego i formatowaniem. Pliki OTF mają `mime-type application/vnd.oasis.opendocument.spreadsheet-template`. Te pliki szablonów mogą służyć jako punkt wyjścia do generowania i zapisywania rzeczywistych plików danych, które są zapisywane w [formacie pliku ODS](/pl/spreadsheet/ods/). Pliki OTS mogą być używane z aplikacjami takimi jak OpenOffice i LibreOffice.

## Format pliku OTS

Pliki OTS są zapisywane w formacie pliku OASIS OpenDocument opartym na XML, który składa się z kolekcji kilku dokumentów podrzędnych z pakietem jako archiwum [ZIP](/pl/compression/zip/). Każde archiwum zip przechowuje część całego dokumentu, a każdy dokument podrzędny przechowuje określony aspekt dokumentu. Na przykład jeden dokument podrzędny zawiera informacje o stylu, a inny dokument podrzędny zawiera treść dokumentu. Typowy dokument ODF składa się z następujących elementów:

### Treść OTS.xml

Plik content.xml zawiera rzeczywistą treść dokumentu. Nie obejmuje to jednak danych binarnych, takich jak obrazy.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml formatu pliku OTS

Plik styles.xml zawiera informacje o stylu i jest często używany do formatowania i układu. Typy stylów obejmują:

* Style akapitowe
* Style strony
* Style postaci
* Style ramek
* Lista stylów

### Meta.xml

Plik meta.xml zawiera informacje o metadanych pliku, takie jak autor, data ostatniej modyfikacji itp.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Ustawienia.xml

Plik `settings.xml` zawiera ustawienia na poziomie dokumentu, takie jak współczynnik powiększenia i pozycja kursora.

## Bibliografia ##

* [Specyfikacja OpenDocument 1.2](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument – z Wikipedii](https://en.wikipedia.org/wiki/OpenDocument)

