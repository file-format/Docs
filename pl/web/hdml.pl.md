{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik języka znaczników urządzenia przenośnego",
  "description":"Poznaj format plików HDML i interfejsy API, które mogą tworzyć i otwierać pliki HDML.",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## Co to jest plik HDML?

Plik z rozszerzeniem .hdml (Handheld Device Markup Language) to język znaczników do tworzenia stron internetowych dla przenośnych urządzeń elektronicznych, takich jak komputery podręczne, smartfony i urządzenia wyświetlające informacje. Mówi się, że HDML jest rozszerzeniem języka [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language). HDML jest podobny do HTML, ale dla urządzeń bezprzewodowych i przenośnych, które mają małe wyświetlacze, takie jak PDA, telefony komórkowe i tak dalej. Został zastąpiony przez WML, na który miał istotny wpływ.

## Format pliku HDML — więcej informacji

HDML to język znaczników dla urządzeń przenośnych, który jest oparty na znacznikach znaczników podobnych do HTML. HDML został przesłany do W3C w celu standaryzacji, ale nigdy nie stał się standardem. Specyfikacje formatu plików są jednak dostępne na [witrynie W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) w celach informacyjnych. [Składnia języka HDML](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) jest dostępna dla programistów i może być używana do tworzenia przykładowych aplikacji.

## Elementy HDML

Poniżej znajduje się lista elementów, które zapewniają środowisko wykonawcze dla HDML i jest określane jako agent użytkownika.

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

