{
  "date" : "2021-02-25",
  "keywords" :["plik bdf", "format pliku bdf", "co to jest plik bdf", "plik", "przykład bdf", "rozszerzenie pliku bdf","rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - format dystrybucji mapy bitowej glifów",
  "description":"Poznaj format pliku BDF i interfejsy API, które mogą tworzyć i otwierać pliki BDF.",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Czym jest plik BDF?
Pliki BDF mają formę czytelną dla człowieka i są zwykle dystrybuowane w kodowaniu ASCII. Plik zaczyna się od globalnych informacji odnoszących się do całej czcionki, po których następują informacje i mapy bitowe dla poszczególnych glifów. Zawarte w nim dane dotyczą czcionki dla orientacji o jednym rozmiarze. Metryki do wykorzystania w więcej niż jednym kierunku mogą być zawarte w jednym pliku. W pliku BDF każdy element jest zawarty w osobnym wierszu tekstu w pliku. Spacje służą do oddzielania elementów w wierszu.

## Format pliku BDF
Skróty BDF dla formatu dystrybucji Glyph Bitmap; własnością firmy Adobe to format pliku do zapisywania czcionek typu bitmapa. Treść ma postać pliku tekstowego, który ma być zarówno czytelny dla komputera, jak i dla człowieka. BDF jest szczególnie używany w środowiskach Unix X Window. Został on szeroko zastąpiony formatem czcionek PCF, który ma być bardziej wydajny, oraz czcionkami OpenType i TrueType.
### Struktura plików BDF
Plik czcionki BDF składa się z trzech sekcji:

- globalna sekcja, która dotyczy wszystkich glifów w czcionce.
- sekcja z osobnym wpisem dla każdego glifu.
- instrukcja ENDFONT.

## Przykład
Oto przykładowa czcionka zawierająca jeden glif dla dużej litery „A” w kodzie ASCII. Jego globalne deklaracje zaczynają się linią „STARTFONT” i kończą linią „CHARS”.
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## Bibliografia
* [Format dystrybucji map bitowych glifów](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [Specyfikacja formatu dystrybucji map bitowych glifów (BDF)](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

