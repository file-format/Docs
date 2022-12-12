{
  "date" : "2021-01-21",
  "keywords" :[ "plik otp", "format pliku otp", "co to jest plik otp", "plik", "przykład otp", "rozszerzenie pliku otp", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTP - szablon prezentacji OpenDocument",
  "description":"Dowiedz się o formacie pliku OTP i interfejsach API, które mogą tworzyć i otwierać pliki OTP.",
  "linktitle" : "OTP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2021-01-21"
}

## Czym jest plik OTP?

Pliki z rozszerzeniem .otp reprezentują pliki szablonów prezentacji utworzone przez aplikacje w standardowym formacie OASIS OpenDocument. Zawartość takiego pliku zawiera informacje o prezentacji w postaci slajdów z tekstem, obrazami, kształtami, treściami multimedialnymi, efektami przejść i innymi elementami slajdów. Te pliki szablonów służą do szybkiego tworzenia nowych prezentacji na podstawie informacji o stylach przechowywanych w samym szablonie. Pliki OTP można tworzyć i zapisywać za pomocą kilku różnych aplikacji, takich jak Impress dostarczany z pakietem OpenOffice i Microsoft PowerPoint. Format pliku OTP jest podobny do plików szablonów Microsoft PowerPoint [.pot](/pl/presentation/pot/) i [.potx](/pl/presentation/potx/).

## Format pliku OTP

Format pliku OTP jest oparty na standardzie OpenDocument, który obsługuje reprezentację dokumentu jako pojedynczy dokument XML, a także zbiór kilku dokumentów podrzędnych w jednym spakowanym pakiecie w formacie [ZIP](/pl/compression/zip/). Zawartość pliku jest dystrybuowana w wielu plikach xml spakowanych razem. Te liczne pliki [XML](/pl/web/xml/) zawierają informacje o stylu, zawartości, metainformacjach i ustawieniach dokumentu, jak wspomniano poniżej.

* `content.xml` – Treść dokumentu i automatyczne style użyte w treści.
* `styles.xml` – Style używane w treści dokumentu i style automatyczne używane w samych stylach.
* `meta.xml` – metadane dokumentu, takie jak autor lub czas ostatniej akcji zapisu.
* `settings.xml` – Ustawienia specyficzne dla aplikacji, takie jak rozmiar okna lub informacje o drukarce.

## Bibliografia

* [OpenDocument – z Wikipedii](https://en.wikipedia.org/wiki/OpenDocument)

