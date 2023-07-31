{
  "date" : "2020-08-20",
  "keywords" :[ "plik cff", "format pliku cff", "co to jest plik cff", "plik", "przykład cff", "rozszerzenie pliku cff", "rozszerzenie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF – kompaktowy format pliku czcionki",
  "description":"Poznaj format pliku CFF i interfejsy API do tworzenia i otwierania plików CFF.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Czym jest plik CFF?

Plik z rozszerzeniem .cff to Compact Font Format i jest również znany jako PostScript Type 1 lub CIDFont. CFF działa jak kontener do przechowywania wielu czcionek razem w jednej jednostce znanej jako FontSet. Projekt czcionek CFF umożliwia osadzenie kodu języka PostScript, co zapewnia dodatkową elastyczność i rozszerzalność formatu do użytku w środowiskach drukarek. Pliki czcionek CFF można otwierać i konwertować za pomocą interfejsów API, takich jak [Aspose.Font](https://products.aspose.com/font).

## Format pliku CFF

Pliki CFF to pliki binarne, które zawierają uporządkowany układ danych, mają zdefiniowane typy danych, nagłówek, organizację glifów i słowniki tabel. Więcej informacji na ten temat można znaleźć w [specyfikacjach kompaktowego formatu czcionek](https://learn.microsoft.com/en-us/typography/opentype/spec/cff).

### Układ danych
Układ danych w formacie pliku CFF pokazano poniżej.

|Wpis|Komentarze|
---|---|
|Nagłówek|–|
|NazwaINDEX|–|
|Top DICT INDEX|–|
|ŁAŃCUCH INDEKS|–|
|Globalny indeks Subr|–|
|Kodowania–Zestawy znaków|–|
|FDSelect|Tylko CIDFonts|
|CharStrings INDEX|na czcionkę|
|Czcionka DICT INDEX|dla czcionki, tylko CIDFonts|
|Prywatny DICT|na czcionkę|
|Lokalny Subr INDEX|dla czcionki lub dla Prywatnego DICT dla CIDFonts|
|Informacje o prawach autorskich i znakach towarowych|–|

### Typy danych

Typy danych CFF są takie, jak pokazano w poniższej tabeli.

|Nazwa|Zakres|Opis|
---|---|---|
|Karta8|0 –255|1-bajtowa liczba bez znaku|
|Karta16|0 – 65535|2-bajtowa liczba bez znaku|
|Przesunięcie|różne|przesunięcie o 1, 2, 3 lub 4 bajty (określone przez pole OffSize)|
|OffSize|1–4|1-bajtowa liczba bez znaku określa rozmiar pola lub pól przesunięcia|
|SID|0 – 64999|2-bajtowy identyfikator łańcucha|

### Nagłówek

Dane binarne rozpoczynają się nagłówkiem o formacie pokazanym w poniższej tabeli.

|Typ|Nazwa|Opis|
---|---|---|
|Karta8|główna|Formatuj wersję główną (zaczynając od 1)|
|Karta8|podrzędna|Sformatuj podrzędną wersję (zaczynając od 0)|
|Karta8|hdrRozmiar| Rozmiar nagłówka (bajty)|
|OffSize|offSize|Rozmiar bezwzględnego przesunięcia (0)|

## Bibliografia

* [Tabela kompaktowych formatów czcionek](https://learn.microsoft.com/en-us/typography/opentype/spec/cff)
* [Format pliku CFF](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [Zestaw wykresów CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

