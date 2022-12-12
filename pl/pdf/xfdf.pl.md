{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku XFDF - Co to jest plik XFDF?",
  "description":"Dowiedz się o plikach XFDF i interfejsach API, które mogą tworzyć i otwierać pliki XFDF.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik XFDF?

Plik z rozszerzeniem .xfdf to format danych formularzy XML, który jest generowany za pomocą oprogramowania Adobe Acrobat. Podobnie jak [FDF](/pl/pdf/fdf/), XFDF zawiera opis elementów formularza i ich wartości w formacie XML. Może to obejmować nazwy i wartości pól tekstowych w formularzu PDF. XFDF są zapisywane w formacie czytelnym dla człowieka i mogą być odczytywane programowo przy użyciu języków programowania, takich jak C#.

## Format pliku XFDF — więcej informacji

Pliki XFDF są zapisywane w formacie pliku XML, który jest uniwersalnym formatem używanym do importu i eksportu danych. Struktura pliku XFDF składa się z nagłówka, po którym następują wartości pól i dane elementów, jak pokazano poniżej.

|Element|Atrybut|Zawartość|
---|---|---|
|\<XFDF> ||Najwyższy element|
|\<fields> ||Wszystkie wartości pól dla tego szablonu|
|<field (T)> |nazwa |Nazwa pola|
|<value (V)> |wartość |Wartość pola|

## Bibliografia

* [Obsługa formatu FDF przez program Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)
* [Zasoby Adobe dla programistów](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

