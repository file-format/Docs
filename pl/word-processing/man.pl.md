{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Podręcznik systemu Unix",
  "description":"Poznaj format plików FODT i interfejsy API, które mogą tworzyć i otwierać pliki MAN.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## Czym jest plik MAN?

Plik z rozszerzeniem .man oznacza stronę man, która jest podręcznikiem użytkownika programowania w systemie Unix w formie dokumentacji oprogramowania. Jest używany przez narzędzie `Man` zawarte w systemie Unix, które służy do przeglądania dokumentacji. Dokumentacja oprogramowania zawiera informacje w sekcjach i na stronach, które można pobrać za pomocą narzędzia Man z terminala poleceń, wydając polecenia. Będąc dostępnym w komputerze jako miękka kopia dokumentacji, nie wymaga żadnej drukowanej kopii ani połączenia z Internetem, aby uzyskać do niej dostęp.

## Unix Manual Man File Format — więcej informacji

Strony podręcznika są przechowywane w formacie zwykłego tekstu i można je tworzyć i otwierać w dowolnym edytorze tekstu w celu przeglądania lub edytowania. W systemie UNIX informacje ze stron podręcznika są pobierane przez wydawanie poleceń z terminala, które zawierają odniesienia do numerów sekcji i stron podręcznika.

### Sekcje i strony

Unix man to podręcznik systemu, w którym każdy argument strony polecenia odnosi się do nazwy programu, narzędzia lub funkcji. polecenie, jeśli podano informacje o sekcji, wyszuka stronę w tej konkretnej sekcji. Jednak domyślnym zachowaniem jest wyszukiwanie strony we wszystkich sekcjach i wyświetlanie pierwszej strony, niezależnie od tego, czy istnieje ona w wielu sekcjach.

### Numery sekcji

Poniżej podano informacje o numerach rozdziałów instrukcji, a następnie o typach zawartych w nich stron.

|Numer sekcji|Rodzaj stron|
---|---|
|1|Programy wykonywalne lub polecenia powłoki|
|2|Wywołania systemowe (funkcje dostarczane przez jądro)|
|3|Wywołania biblioteczne (funkcje w bibliotekach programów)|
|4|Pliki specjalne (zwykle znajdują się w /dev)|
|5|Formaty plików i konwencje, np. /etc/passwd|
|6|Gry|
|7|Różne (w tym pakiety makr i konwencje), np. man(7), groff(7)|
|8|Polecenia do administrowania systemem (zwykle tylko dla roota)|
|9|Procedury jądra [niestandardowe]|

## Przykład - Jak czytać strony MAN?

Oto przykład, jak pobrać informacje o poleceniu MkDir za pomocą polecenia Man.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## Bibliografia

* [Specyfikacje techniczne OpenDocument – z Wikipedii](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — strona podręcznika systemu Linux](https://man7.org/linux/man-pages/man1/man.1.html)

