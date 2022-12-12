{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku FDF - Co to jest plik FDF?",
  "description":"Poznaj format pliku FDF i interfejsy API, które mogą tworzyć i otwierać pliki FDF.",
  "linktitle" : "FDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik FDF?

Plik FDF (**Forms Data Format**) to dokument tekstowy generowany przez eksport danych z pól formularza w pliku [PDF](/pl/pdf/). Zawiera tylko dane pól tekstowych wyodrębnione z pól formularza dostępnych w pliku PDF. Powoduje to stosunkowo mały plik danych, ponieważ eksportowane dane nie zawierają samego formularza. Program Adobe Acrobat udostępnia funkcję eksportowania danych pól formularzy za pomocą opcji „Eksportuj dane formularzy” z menu aplikacji.

## Format pliku FDF — więcej informacji

FDF jest formatem zwykłego tekstu i stanowi część [standardu ISO 32000](https://www.iso.org/standard/51502.html) formatu Portable Document Format. Został opracowany przez Adobe, aby umożliwić import i eksport danych z Acrobat Forms lub AcroForms.

Istnieją dwa rodzaje plików FDF:

• `Klasyczny FDF` – Dostarcza danych do wypełnienia istniejącego formularza statycznego.

• `Szablon FDF` – Konstruuje nowy plik PDF na podstawie szablonów z określonych plików PDF. Formularze wewnątrz nowego dokumentu są wypełniane poprzez podanie danych.

## Tworzenie FDF za pomocą Adobe Acrobat

[Zestaw narzędzi FDF](https://opensource.adobe.com/dc-acrobat-sdk-docs/) firmy Adobe umożliwia tworzenie plików FDF z danych tekstowych.

## Bibliografia ##

* [Obsługa formatu FDF przez program Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)
* [Zasoby Adobe dla programistów](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

