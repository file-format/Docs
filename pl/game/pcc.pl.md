{
  "date" : "2021-09-08",
  "keywords" :["plik pcc", "format pliku pcc", "co to jest plik pcc", "plik", "przykład pcc", "rozszerzenie pliku pcc", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Dowiedz się o formacie plików PCC Mass Effect i interfejsach API, które mogą tworzyć i otwierać pliki PCC.",
  "title" :"PCC - plik pakietu Mass Effect",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Czym jest plik PCC?

Plik z rozszerzeniem .pcc to plik [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3), który zawiera dane gry umożliwiające modyfikację zawartości gry, takiej jak modele, tekstury i pokoje. Mass Effect 2 i 3 to pierwsze strzelanki oparte na silniku gier Unreal Engine 3. Gra została początkowo opracowana przez firmę [Bioware](https://www.bioware.com/about/), która zachowała większość zasobów gry w swoim zastrzeżonym formacie plików PCC. Bioware zostało przejęte przez Electronic Arts, wiodącego światowego wydawcę interaktywnej rozrywki.

## Format pliku PCC — więcej informacji

Pliki PCC zawierają skompresowane i / lub nieskompresowane struktury, które przyczyniają się do ogólnej organizacji plików.

### Skompresowana struktura PCC

Skompresowany plik PCC składa się z tabel i danych podzielonych na fragmenty. Każda porcja zawiera zmienną liczbę skompresowanych bloków.

* `Chunks Header` - 16-bajtowy wspólny nagłówek zawierający informacje o porcjach.
* `Chunk Header` - 16-bajtowy nagłówek zawierający informacje o nieprzetworzonych skompresowanych danych zawartych w postaci bloku.

### Nieskompresowana struktura PCC

Nieskompresowane pliki PCC są podzielone na pięć następujących części.

* `Nagłówek` - zawiera podstawowe informacje o strukturze pliku PCC.
* `Tabela nazw` - zawiera nazwę znalezioną wewnątrz pakietu, w tym klasy importu, eksporty i właściwości eksportu.
* `Import Table` - zawiera wszystkie klasy i obiekty zaimportowane przez PCC.
* `Export Table` - zawiera wszystkie obiekty zapisane w paczce. Każdy eksport może różnić się wielkością.

## Bibliografia

* [Me3Explorer - format pliku PCC](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [Gra Mass Effect](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)

