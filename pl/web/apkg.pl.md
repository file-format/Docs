{
  "date" : "2019-10-11",
   "keywords" :[ "apkg", "plik apkg", "format pliku apkg", "typ pliku apkg", "plik", "typ", "Co to jest plik APKG"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Anki Format Pliku Talii Fiszek",
  "description" :"Dowiedz się, co to jest plik APKG i interfejsy API, które mogą je tworzyć i otwierać.",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## Co to jest plik APKG?

Plik z rozszerzeniem .apkg to zestaw fiszek wygenerowanych do użycia w aplikacji [Anki](https://ankiweb.net/about), która jest programem do nauki opartym na fiszkach. Zawiera tekst [HTML](/pl/web/html/) do załadowania i wyświetlenia w aplikacji Anki, a dodatkowo może zawierać obrazy i dźwięki do nauki wizualnej i dźwiękowej. Anki pozwala użytkownikom tworzyć własne talie fiszek Anki, a także importować talie fiszek innych użytkowników.

## Format pliku APKG

Talie kart Anki są tworzone z szablonów napisanych w HTML, znanym i popularnym języku do tworzenia stron internetowych. Stylizacja kart talii odbywa się za pomocą CSS, który jest językiem używanym do stylizacji stron internetowych. Stylizacja obejmuje modyfikacje:

* rodzina czcionek — nazwa czcionki, która ma być użyta na karcie.
* font-size - Rozmiar czcionki w pikselach.
* text-align — określa, czy tekst ma być wyrównany do środka, do lewej czy do prawej.
* kolor — określa kolor tekstu, którym mogą być proste nazwy kolorów, takie jak „niebieski”, „czerwony” itp. lub kody kolorów HTML.
* kolor tła - Określa kolor tła karty

Informacje o stylu są wspólne dla wszystkich kart, wpływając na wszystkie karty po wprowadzeniu zmiany. Poniższy przykład użyje żółtego tła na wszystkich kartach z wyjątkiem pierwszej:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Zmiana rozmiaru obrazów na karcie Anki może być kontrolowana w następujący sposób.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Osadzanie Javascript w kartach Anki

Możliwe jest osadzenie [Javascript](/pl/web/js/) w karcie Anki przy użyciu szablonów kart. Jednak ze względu na zaawansowany poziom JavaScript, jego obsługa nie jest zapewniona. Ponadto urządzenia renderujące mogą w różny sposób pokazywać wpływ implementacji Javascript na karcie, co powoduje konieczność przetestowania implementacji na wszystkich urządzeniach. Niektóre funkcje JavaScript, takie jak window.alert, utrudniające debugowanie napisanego kodu JavaScript.

## Bibliografia ##

* [Dokumentacja Anki](https://docs.ankiweb.net/intro.html)

