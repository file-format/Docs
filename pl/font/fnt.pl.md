{
  "date" : "2020-08-20",
  "keywords" :[ "plik fnt", "format pliku fnt", "co to jest plik fnt", "plik", "przykład fnt", "rozszerzenie pliku fnt", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - plik czcionek systemu Windows",
  "description":"Poznaj format pliku FNT i interfejsy API, które mogą tworzyć i otwierać pliki FNT.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Czym jest plik FNT?

Plik z rozszerzeniem .fnt to plik czcionek, który przechowuje ogólne informacje o czcionkach w systemach operacyjnych Windows. Pliki FNT zostały w większości zastąpione formatami plików TrueType (.TTF) i OpenType (.OTF) i obecnie są przestarzałym formatem plików czcionek. Pliki te mogą przechowywać pojedynczą czcionkę oceniającą lub czcionkę wektorową. Wszystkie sterowniki urządzeń obsługują czcionki Windows 2.x. Jednak nie wszystkie sterowniki urządzeń
obsługuje wersję Windows 3.0.

## Format pliku FNT

Pliki FNT mogą przechowywać pojedynczą czcionkę rastrową lub wektorową. Formaty wektorowe są częściej używane przez GDI w porównaniu do rastra, w którym glif każdego czarteru jest definiowany za pomocą małej mapy bitowej. Oczywistym powodem zastąpienia .fnt przez .ttf i .otf jest jego format rastrowy.

### Nagłówek pliku czcionki
Początek plików czcionek rastrowych i wektorowych jest wspólny, a następnie różne informacje dla każdego typu pliku. Nagłówek pliku czcionki dla systemu Windows 3.0 zawiera sześć nowych pól, które są ustawione na zero, aby zapewnić kompatybilność z przyszłymi wersjami systemu Windows.

* dFlagi
* dfAprzestrzeń
* przestrzeń dfB
* dfCprzestrzeń
*dfColorPointer
* dfZarezerwowane1

Aby uzyskać szczegółowe informacje na temat nagłówków dla Windows 3.0 i 2.0, odwiedź [Archiwum Microsoft KnowledgeBase](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Bibliografia
* [Format pliku czcionki](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [Jak zainstalować lub usunąć czcionkę w systemie Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8 -7613-c76f-88d043b334b8)

