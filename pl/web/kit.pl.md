{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku KIT i interfejsy API, które mogą tworzyć i otwierać pliki KIT.",
  "title" :"Format pliku KIT - Plik CodeKit",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Czym jest plik KIT?

Plik z rozszerzeniem .kit to plik HTML utworzony za pomocą aplikacji języka programowania [CodeKit](https://codekitapp.com/). Zawiera `importy` i `zmienne` oprócz istniejących plików [HTML](/pl/web/html/), dzięki czemu idealnie nadaje się do statycznych witryn. CodeKit kompiluje pliki KIT do formatu HTML, które można łatwo wykorzystać jako statyczne pliki stron internetowych.

## Format pliku KIT

Pliki KIT to pliki HTML, które dodatkowo zawierają importy i zmienne. Są one przechowywane jako zwykłe pliki tekstowe i można je otwierać za pomocą dowolnego edytora tekstu lub internetowych edytorów plików.

### Import plików KIT

Do pliku Kit można zaimportować prawie każdy typ pliku. Poniżej przedstawiono składnię importu używaną do importowania plików do pliku .kit.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Kiedy import jest dodawany do pliku KIT i zapisywany, jest zastępowany tekstem importowanego pliku. Możesz także użyć @include zamiast @import.

### Wiele importów w pliku KIT

Możesz także zaimportować więcej niż jeden plik na raz, używając listy oddzielonej przecinkami:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Bibliografia

* [Co to jest zestaw?](https://codekitapp.com/help/kit/)

