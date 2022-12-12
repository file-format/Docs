{
  "date" : "2021-09-13", 
  "keywords" :["ici", "plik", "rozszerzenie", "format pliku", "Implementacja ICI", "Przewodnik programowania", "przykład ici", "język programowania ICI", "moduły ICI", "model danych ICI ", "dokumentacja ICI", "język ICI" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI - Plik Języka Programowania",
  "description":"Poznaj format pliku ICI i interfejsy API, które mogą tworzyć i otwierać pliki ICI.",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## Czym jest plik ICI?

Język programowania ogólnego przeznaczenia, który jest interpretowany i zawiera kilka funkcji, takich jak dynamiczne pisanie wraz z elastycznymi typami danych, jest znany jako język programowania ICI (nie akronim). Uważa się, że jest podobny do języka [Perl](/pl/programming/pl/). Ten język ICI zawiera konstrukcje kontroli przepływu, a także zawiera niektóre operatory języka C. Nie jest to język zorientowany obiektowo, ale niektóre cechy OOP można osiągnąć za pomocą określonej metody dziedziczenia znanej jako nadbudowy. Podobnie jak [C](/pl/programming/c), ten język programowania ICI ma ten sam interfejs systemowy i standardową bibliotekę dla wbudowanych funkcji.


## Krótka historia ##

Pod koniec lat 80. został opracowany przez Tima Longa jako interpretowany język programowania ogólnego przeznaczenia. Większość cech tego języka jest podobna do języka C, a niektóre z tych cech można osiągnąć, stosując specjalne metody. Ten język jest własnością publiczną i jest dostępny jako język do odsprzedaży i nikt nie jest zobowiązany do wspominania, skąd wziął kod źródłowy. Dokumentacja ICI jest chroniona prawami autorskimi firmy Canon Information System Research Australia.

## Specyfikacja techniczna ##

W tym języku używane są dwa różne typy danych. Te dwa typy danych to prymitywny i zagregowany. Oba obejmują różne wyrażenia zgodnie z ich z góry określonym składem w języku. Ten język obsługuje różne moduły, takie jak zagnieżdżone i podprogramy. Ponieważ niektóre jego właściwości są podobne do Perla, ma on ścisłą integrację z wyrażeniami regularnymi.

Zestawy są ograniczone do heterogeniczności i zagnieżdżenia. Zestawy te zapewniają wsparcie dla powszechnie używanych operacji na zestawach, takich jak Union i Intersection itp. Jest używany głównie jako język ze względu na podstawową implementację aplikacji należących do organizacji międzynarodowych.

W tym języku można pisać prawie wszystkie rodzaje programów, aw języku programowania ICI pisane są głównie specyficzne programy, które zawierają złożone struktury danych. Aplikacje mogą obejmować implementację ICI w taki sposób, że powinny być w niej napisane. Funkcjonalne części aplikacji mogą być realizowane przez moduły ICI. Język ICI przypomina nieco język C, ale model danych ICI jest na wyższym poziomie i różni się typami, takimi jak słowniki (struct), zestawy, tablice dynamiczne, wyrażenia regularne i (rzeczywiste) ciągi znaków.


## Przykład formatu pliku ICI ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Odniesienie ##

* [Język programowania ICI](http://atrn.org/ici/doc/ici.html)



