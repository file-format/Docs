{
  "date" : "2021-03-10",
  "keywords" :["ACSM", "Wiadomość Adobe Content Server", "rozszerzenie", "format", "eBook", "plik", "Adobe Digital Editions" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku ACSM firmy Adobe i interfejsy API, które mogą tworzyć i otwierać pliki ACSM.",
  "title" :"ACSM — format pliku wiadomości Adobe Content Server",
  "linktitle" : "ACSM",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## Czym jest plik ACSM?

Pliki z rozszerzeniem .acsm są nazywane plikami wiadomości Adobe Content Server. Te pliki są używane przez **Adobe Digital Editions** do aktywowania i pobierania treści chronionych przez Adobe DRM. W rzeczywistości plik ACSM nie jest plikiem eBook; nie można go otworzyć i czytać jak inne eBooki (np. PDF); Zawiera tylko dane do aktywacji i pobrania ebooka. Oznacza to, że plik ACSM zawiera tylko informacje, które komunikują się z serwerami Adobe. Użytkownicy Digital Editions mogą zobaczyć plik ACSM, jeśli chcą pobrać eBook, ale pobieranie zostałoby zatrzymane z jakiegokolwiek powodu. Użytkownicy mogą wznowić pobieranie, klikając dwukrotnie plik .acsm.

## Jak działa plik ACSM?

Ponieważ serwer Adobe Content Server jest odpowiedzialny za ochronę eBooków i innych materiałów cyfrowych. Po zakupie zawartość jest automatycznie łączona z identyfikatorem Adobe ID kupującego. Identyfikator jest prywatny i nie można go przekazać innym osobom. Użytkownik musi go skonfigurować przed zakupem jakiegokolwiek dokumentu z ochroną przed kopiowaniem firmy Adobe. Klienci nie mogą uzyskać dostępu do swoich dokumentów chronionych przed kopiowaniem bez przekazania swojego identyfikatora Adobe ID do aplikacji serwerowej Adobe działającej w tle.

Kiedy klienci dokonują zakupu, ACSM jest jedynym plikiem, który mogą najpierw pobrać. Klient musi mieć zainstalowane oprogramowanie Adobe Digital Editions w swoim systemie i powiązać je ze swoim identyfikatorem Adobe ID, aby otworzyć plik ACSM. Adobe Digital Editions zweryfikuje identyfikator autoryzacji do konwersji pliku ACSM. Po uwierzytelnieniu użytkownik może pobrać e-booka w formacie [EPUB](/pl/ebook/epub/) lub [PDF](/pl/pdf/). Adobe Digital Editions używa również pliku ACSM do rozpoznawania katalogu pobierania.

## Bibliografia

* [Adobe Content Server – Wikipedia](https://en.wikipedia.org/wiki/Adobe_Content_Server)


