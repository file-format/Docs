{
  "date" : "2021-12-09",
  "keywords" :[ "aro", "plik .aro", "format pliku aro", "typ pliku", "plik", "typ", "co to jest plik .aro" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku ARO - plik aplikacji internetowej SteelArrow",
  "description" :"Dowiedz się, czym jest plik ARO i interfejsy API, które mogą tworzyć i otwierać pliki ARO.",
  "linktitle" : "ARO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Czym jest plik ARO?

Plik ARO to plik strony internetowej po stronie serwera, który jest generowany za pomocą aplikacji internetowej SteelArrow. Zawiera znaczniki i skrypty [HTML](/pl/web/html/) i SteelArrow. Są one wykonywane na serwerze w celu wygenerowania kompletnej strony odpowiedzi przed wysłaniem ich do przeglądarki użytkownika. Pliki ARO zawierają prawie 95% treści HTML, podczas gdy pozostała część składa się z kodu SteelArrow. Aby pliki ARO działały dla Ciebie, serwer SteelArrow Web Applications powinien być zainstalowany i uruchomiony na komputerze serwera WWW.

## Format pliku ARO

Pliki ARO są zapisywane w pliku języka znaczników HTML z osadzonym kodem JavaScript i apletami Java. [Tagi SteelArrow](http://www.steelarrow.com/docs/basics1.aro) to podstawowe elementy składowe do tworzenia stron internetowych. Chociaż nie zmieniają one sposobu wyświetlania strony, służą do wypełniania strony danymi. Ponadto mogą być również używane do sterowania wyjściem za pomocą instrukcji warunkowych.

### Przykład znacznika ARO

The<SAOUTPUT> Znacznik ARO umożliwia programistom wyprowadzanie wartości danych w dowolnym miejscu skryptu. Na przykład można go użyć do uzyskania danych wyjściowych tabeli PARAM za pomocą<SAOUTPUT VALUE=PARAM[]> które mogą być wyświetlane w kodzie HTML<BODY> etykietka.

## Bibliografia

* [Tagi SteelArrow](http://www.steelarrow.com/docs/basics.aro)

