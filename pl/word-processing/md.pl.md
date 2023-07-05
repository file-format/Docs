{
  "date" : "2019-10-11",
  "keywords" :["plik md", "format pliku md", "co to jest plik md", "plik", "przykład md", "rozszerzenie pliku md", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD - plik językowy MarkDown",
  "description":"Poznaj format plików MD i interfejsy API, które mogą tworzyć i otwierać pliki MD.",
  "linktitle" : "MD",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik MD?

Pliki tekstowe utworzone za pomocą dialektów języka Markdown są zapisywane z rozszerzeniem **.md** lub **.MARKDOWN**. Pliki MD są zapisywane w formacie zwykłego tekstu, który wykorzystuje język Markdown, który zawiera również wbudowane symbole tekstowe, określające sposób formatowania tekstu, taki jak wcięcia, formatowanie tabeli, czcionki i nagłówki. Pliki MD można konwertować do formatu HTML za pomocą programu o nazwie Markdown. Język Markdown został wydany przez Johna Grubera.

Pliki MD można również sklasyfikować jako pliki programistyczne, które są najczęściej używane przez Markdown, do konwersji plików tekstowych na wersje HTML, dzięki czemu użytkownicy mogą tworzyć pliki łatwe do odczytania i zapisania. Poniżej przedstawiono aplikacje, które mogą otworzyć plik .md:

* Notatnik Microsoftu
* Notatnik2
* Edycja tekstu Apple
* Microsoft WordPad

Uwaga: nie zmieniaj nazwy rozszerzenia plików .md. Jeśli tak, nie spowoduje to zmiany typu pliku, ponieważ dostępne są specjalne programy do konwersji umożliwiające zmianę typu pliku na inny. Jak omówiono powyżej, pliki .MD są rozszerzeniami plików tworzonych przez oprogramowanie języka Markdown. **Markdown** to [lekki język znaczników](https://en.wikipedia.org/wiki/Lightweight_markup_language) przeznaczony do jednego celu — do formatowania tekstu w internecie przy użyciu składni formatowania zwykłego tekstu. Niech będzie jasne, że Markdown nie zastępuje HTML, ponieważ jego składnia jest bardzo mała i zawiera bardzo mały podzbiór znaczników HTML. Powodem Markdown jest ułatwienie czytania, pisania i redagowania prozy. Innymi słowy, możemy powiedzieć, że HTML jest formatem publikowania, podczas gdy Markdown jest formatem pisania.

Markdown jest obecnie jednym z najpopularniejszych języków znaczników na świecie. Podczas korzystania z programu Microsoft Word formatowanie słów i fraz odbywa się poprzez klikanie przycisków, a zmiany są natychmiast widoczne. Ale Markdown taki nie jest. Podczas tworzenia pliku w formacie Markdown składnia Markdown jest dodawana do tekstu, aby wskazać, które słowa i frazy mogą wyglądać inaczej. Na przykład, aby pokazać nagłówek, przed nim dodawany jest znak z numerem (np. # Nagłówek jeden). Aby zdanie było pogrubione, przed i po nim dodaje się dwie gwiazdki (np. **ten tekst jest pogrubiony**). Składnię Markdown można zobaczyć po chwili w tekście.

## Krótka historia

John Gruber i Aaron Swartz w 2004 roku stworzyli język Markdown z ideą umożliwienia ludziom „pisania w łatwym do odczytania i zapisania formacie zwykłego tekstu z opcją konwersji do XHTML lub HTML. Celem jego projektu jest czytelność – język jest czytelny tak, jak jest, bez wyglądania, jakby został otagowany lub dodany z instrukcjami formatowania, jak ma to miejsce w językach znaczników, takich jak RTF lub HTML, gdzie znaczniki i instrukcje formatowania są oczywiste. Podstawową inspiracją jest wykorzystanie istniejących konwencji oznaczania zwykłego tekstu w wiadomościach e-mail.

Od tego czasu Markdown został ponownie zaimplementowany przez innych, jak również w [module] Perla (https://en.wikipedia.org/wiki/Modular_programming) dostępnym na [CPAN](https://en.wikipedia.org/ wiki/CPAN) oraz w różnych innych językach programowania. Jest rozpowszechniany na [licencji w stylu BSD](https://en.wikipedia.org/wiki/BSD_license) i jest dołączony lub dostępny jako wtyczka do kilku [systemów zarządzania treścią](https:// en.wikipedia.org/wiki/Content_management_system).

## Specyfikacja techniczna

Kiedy coś jest napisane w Markdown, tekst jest najpierw przechowywany w pliku tekstowym z rozszerzeniem .md lub .markdown, a następnie aplikacja do przeceny, taka jak Dillinger, jest używana do przetwarzania pliku Markdown w celu konwersji tekstu sformatowanego Markdown na HTML w celu wyświetlenia go w sieci przeglądarki. Aplikacje Markdown wykorzystują //procesor Markdown// (powszechnie nazywany „parserem” lub „implementacją”) do pobierania tekstu w formacie Markdown i wyprowadzania go do formatu HTML. Schemat przepływu procesu jest następujący:

W skrócie jest to czteroetapowy proces w następujący sposób:

1. Najpierw tworzenie plików Markdown za pomocą edytora tekstu lub aplikacji Markdown z rozszerzeniem .md lub .markdown.
1. Plik Markdown jest następnie otwierany w aplikacji Markdown.
1. Aplikacja Markdown służy do konwersji pliku Markdown na dokument HTML.
1. Plik HTML jest następnie przeglądany w przeglądarce internetowej lub aplikacja Markdown jest używana do konwertowania go na inny format pliku, np. PDF.

Markdown to szybkie i łatwe robienie notatek, pisanie treści na stronę internetową, tworzenie dokumentów gotowych do druku, publikowanie książek, generowanie prezentacji i tworzenie dokumentów.

Niektóre wersje w markdown miały tak duży wpływ na inne wersje, że często można je zobaczyć jako część innych wersji. Np. biblioteki wspominają o wsparciu dla CommonMark (GFM). Przyjrzyjmy się im pokrótce.

### GFM
Markdown jest tak popularny wśród programistów, ponieważ platforma udostępniania open source Github zaakceptowała i rozszerzyła język o wersję o nazwie Github Flavored Markup (GFM), która obejmuje chronione bloki kodu, łącza URL, przekreślenia, tabele i tworzenie zadań do wykonania.

### CommonMark
Twórcy Markdown próbowali ostatnio ujednolicić markdown, połączyli siły, aby stworzyć wersję, testy i dokumentację dla języka, który jest bardziej niezawodny i nazywa się CommonMark. Ten format jest nieco nowy i nie obsługuje wielu funkcji, ale wkrótce zostanie dodanych wiele funkcji MultiMarkdown.

### Wielokrotne przeceny
Multi-Markdown dodał do języka różne funkcje, które są obsługiwane przez inne wersje. Pierwotnie został napisany w Perlu, ale później został przeniesiony do C. Obsługuje ogrodzone bloki kodu, podświetlanie składni, tabele, metadane, fragmenty/odsyłacze, przypisy, przekreślenia, listy definicji, matematykę.

## Bibliografia

* [Mastering MarkDown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

