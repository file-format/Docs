{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik HDM - plik języka znaczników urządzenia przenośnego",
  "description":"Poznaj format pliku HDM i interfejsy API, które mogą tworzyć i otwierać pliki HDM.",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## Czym jest plik HDM?

Plik HDM to plik strony internetowej języka znaczników, który jest tworzony w języku Handheld Device Markup Language (HDML). Zawiera znaczniki znaczników podobne do języka [HTML](/pl/web/html/), ale jest przeznaczony dla przenośnych urządzeń elektronicznych, takich jak smartfony i urządzenia PDA. [Specyfikacja formatu plików HDML](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) została przesłana do W3C w celu standaryzacji, ale nie mogła stać się standardem. HDM opiera się na specyfikacjach formatu plików [HDML](/pl/web/hdml/) dostępnych na stronie internetowej W3.

## Format pliku HDM — więcej informacji

Plik HDM składa się ze znaczników znaczników, które są renderowane na wizualnie zaprojektowanej stronie internetowej na urządzeniach przenośnych. Pliki HDM są kopiowane na urządzenia przy użyciu protokołu HDTP (Handheld Device Transport Protocol) zamiast protokołu HTTP, który jest używany do stron HTML.

## Elementy plików HDML

Poniżej znajduje się lista elementów, które zapewniają środowisko wykonawcze dla HDML i jest określany jako agent użytkownika.

|Element|Opis|
---|---|
|Karty|Jest to podstawowy element budulcowy HDML, który wyświetla i umożliwia użytkownikowi interakcję z kartami informacyjnymi. |
|Talie|Karty HDML są pogrupowane w talie. Talia HDML jest podobna do strony HTML, ponieważ jest identyfikowana przez adres URL [RFC1738] i jest jednostką treści żądaną z serwera i przechowywaną w pamięci podręcznej przez agenta użytkownika.|
|Akcje|Akcje mogą być typu PREV, SOFT1-SOFT8 i HELP. Są one abstrakcyjne i obsługiwane w interfejsie użytkownika w sposób specyficzny dla agenta użytkownika.|
|Czynności|Aktywność jest jak grupa powiązanych ze sobą kart, które pełnią jedną funkcję logiczną. Mogą one obejmować jeden lub więcej pokładów. Model nawigacji i stanu HDML jest zorganizowany wokół działań.|
|Nawigacja oparta na historii|Agent użytkownika przechowuje historię kart wyświetlanych użytkownikowi. Każda karta, do której uzyskano dostęp, jest dodawana do historii kart. Agent użytkownika pozwala użytkownikowi łatwo wrócić do poprzedniej karty w historii.|

## Bibliografia

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [Specyfikacje HDML – W3 Schools](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

