{
  "date" : "2019-10-11",
  "keywords" :[ "CGM", "Metaplik grafiki komputerowej", "Plik", "Rozszerzenie", "Format pliku", "Grafika wektorowa", "Deskryptor metapliku"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku CGM",
  "description":"Poznaj format plików CGM i interfejsy API, które mogą tworzyć i otwierać pliki CGM.",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Czym jest plik CGM? ##

Computer Graphics Metafile (CGM) to darmowy, niezależny od platformy, międzynarodowy standardowy format metaplików do przechowywania i wymiany grafiki wektorowej (2D), grafiki rastrowej i tekstu. CGM wykorzystuje podejście obiektowe i wiele funkcji do tworzenia obrazów. CGM wykorzystuje te zorientowane obiektowo cechy do przekształcania elementów graficznych w celu renderowania obrazu. Metaplik zawiera niezbędne informacje definiujące inne pliki. W CGM tekstowy plik źródłowy zawiera wszystkie elementy graficzne, które można później skompilować do pliku binarnego. Zasadniczo CGM to sposób na ułatwienie wymiany danych graficznych 2D, niezależnie od konkretnej platformy lub urządzenia.

Format CGM zapewnia różne elementy do wykonywania funkcji i oznaczania obiektów w celu dostosowania prymitywów geometrycznych i informacji graficznych. Chociaż CGM został zastąpiony przez inne formaty do wyświetlania grafiki na stronach internetowych, ponieważ nie jest dobrze obsługiwany przez strony internetowe, nadal jest bardzo popularny wśród zastosowań przemysłowych, lotniczych i innych technicznych. Chociaż konsorcjum World Wide Web opracowało WebCGM, alternatywne podejście do korzystania z CGM w sieci. Podstawowa implementacja CGM była ilustracją sekwencji podstawowych operacji Graficznego Systemu Jądra (GKS). Nie został zbytnio przyjęty w profesjonalnych projektach, ale został w dużej mierze wyparty przez inne formaty, takie jak DXF i SVG.

## Historia ##

CGM okazał się standardem międzynarodowym w 1987 r. (ISO 8632-1987), a także został przyjęty jako standard krajowy w Wielkiej Brytanii przez BSI iw USA przez ANSI. Po wielu poprawkach w 1991 r., w 1992 r. opublikowano poprawiony standard CGM (ISO 8632:1992). W 2001 roku World Wide Web Consortium opracowało WebCGM z ulepszonymi możliwościami używania ze stronami internetowymi. W 2007 roku została wydana druga wersja WebCGM, a trzecia wersja została wydana w 2010 roku z rozszerzonymi możliwościami.

## Format pliku CGM ##

Metapliki grafiki komputerowej są zasadniczo bazami danych informacji graficznych i zapewniają środki do przechwytywania, przechowywania i przesyłania danych graficznych. W związku z tym musi istnieć graficzny komponent systemu do tworzenia bazy danych równolegle z wykonywaniem aplikacji w formacie metapliku. W większości przypadków tym komponentem jest generator metaplików. Oprócz tego potrzebny jest inny komponent, który może pobierać, interpretować i renderować dane graficzne w metapliku. Potrzebę tę zaspokaja obecność interpretera metaplików. Poniższy rysunek przedstawia graficzne środowisko pracy z metaplikami.

Relacje CGM z innymi komponentami typowego systemu graficznego ilustruje powyższy rysunek. Z rysunku wynika również, że funkcjonalność metapliku nie jest zależna od wyjścia końcowego urządzenia.

Zasadniczo istnieją dwie kategorie metaplików: **przechwytywanie sekcji** i **przechwytywanie obrazu**. Podstawową funkcją metapliku przechwytywania obrazu jest przechwytywanie niezależnych od urządzenia, wielu definicji obrazu. Podczas gdy metapliki przechwytywania sesji używają interfejsu systemowego do przechwytywania wyjściowego dialogu w systemie graficznym. CGM należy do kategorii metaplików przechwytywania obrazów statycznych. CGM zapewnia dobrze zorganizowany układ komponentów o dwupoziomowej strukturze.

1. Deskryptor metapliku
1. Pula logicznie niezależnych obrazów

Każdy obraz jest zbiorem deskryptorów obrazu i treści obrazu, w tym definicji obrazu. deskryptor metapliku definiuje informacje opisowe, które w równym stopniu odnoszą się do wszystkich obrazów tego metapliku. Te informacje pomagają tłumaczowi poprawnie przeanalizować metaplik i rozpoznać zasoby wymagane do poprawnego renderowania obrazu. Chociaż deskryptor obrazu zawiera również informacje opisowe, może on jednak rozpoznać tylko obraz, w którym znajduje się deskryptor. W tym formacie pliku każda definicja obrazu jest samodzielna i logicznie niezależna. Są niezależne od wszystkich innych definicji obrazów w pliku. Bezpośrednio po interpretacji metadeskryptora obrazy mogą być udostępniane i interpretowane w sposób losowy. Zmiana stanu poprzednich zdjęć nie ma wpływu na ich następców. Ta niezależność obrazu jest kolejną wyróżniającą cechą CGM.CGM składa się z przestrzeni współrzędnych, które są współrzędnymi kartezjańskimi 2D, zwanymi współrzędnymi urządzenia wirtualnego i mogą być reprezentowane przez liczbę lub precyzję reprezentującą zakres i ziarnistość. CGM określa zarówno bezpośredni wybór kolorów, jak i wybór oparty na indeksie. W pierwszym specyfikator koloru składa się z trójki RGB, podczas gdy później specyfikator koloru wskazuje indeks w tabeli kolorów.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
