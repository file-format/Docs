{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku SY_ - Skompresowany plik SYS",
  "description":"Poznaj format pliku SY_ i interfejsy API, które mogą tworzyć i otwierać pliki SY_.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## Co to jest plik SY_?

Plik SY_ to skompresowany plik .sys używany przez instalatory oprogramowania do zmniejszania rozmiaru plików instalacyjnych spakowanych w instalatorze. Zmniejsza to całkowity rozmiar instalatora. Pliki SY_ można rozszerzyć za pomocą narzędzia wiersza polecenia Microsoft Expand, które rozszerza jeden lub więcej skompresowanych plików.

## Format pliku SY_ — więcej informacji

Pliki SY_ są zapisywane na dysku jako skompresowane pliki binarne. Jednak ich wewnętrzny format plików nie jest publicznie dostępny. Narzędzie wiersza polecenia Microsoft Expand może rozwinąć pliki SY_ przy użyciu jednego z następujących wierszy poleceń.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Po rozwinięciu pliki SY_ są konwertowane do pliku [SYS](/system/sys/).

Pliki SY_ są podobne do plików EX_ i DL_.

## Bibliografia

* [StuffIt – Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft rozwiń](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

