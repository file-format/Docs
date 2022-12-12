{
  "date" : "2021-02-15",
  "keywords" :["plik asf", "format pliku asf", "co to jest plik asf", "plik", "przykład asf", "rozszerzenie pliku asf","rozszerzenie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF — format plików zaawansowanych systemów",
  "description":"Poznaj format pliku ASF i interfejsy API, które mogą tworzyć i otwierać pliki ASF.",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Czym jest plik ASF?

Plik z rozszerzeniem .asf to format pliku multimedialnego do przechowywania i odtwarzania strumieni multimediów cyfrowych przez sieć. Jest to format pliku kontenera, który może zawierać zarówno treści wideo, jak i audio do przesyłania strumieniowego online. Rzadko można znaleźć pliki ASF, częściej można spotkać pliki Windows Media Audio ([WMA](/pl/audio/wma/)) i Windows Media Video ([WMV](/pl/video/wmv/)), które określają pliki ASF posiadanie treści zakodowanej za pomocą odpowiednich kodeków. Pliki multimedialne systemu Windows można tworzyć i odczytywać za pomocą zestawu Windows Media Format SDK.

## Format pliku ASF

Plik ASF może zawierać wiele niezależnych lub zależnych strumieni. Może to obejmować wiele strumieni audio dla wielokanałowego dźwięku lub wiele strumieni wideo o szybkości transmisji bitów. Wiele przepływności sprawia, że strumienie nadają się do transmisji na różnych szerokościach pasma. Ponadto strumienie w pliku ASF mogą być w formacie skompresowanym lub nieskompresowanym. Najlepszą kompresję zapewniają kodeki Microsoft Windows Media Audio i Video z serii 9. Pełna specyfikacja formatu pliku ASF jest dostępna w [witrynie Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### Struktura plików najwyższego poziomu ASF

Pliki ASF logicznie zawierają trzy typy obiektów najwyższego poziomu:

* `Obiekt nagłówka` - obowiązkowy i musi być umieszczony na początku każdego pliku ASF
* `Obiekt danych` - obowiązkowy i musi następować po obiekcie nagłówka
* `Obiekty indeksu` - opcjonalne, ale przydatne w zapewnianiu losowego dostępu do plików ASF w oparciu o czas

Poniższy obraz przedstawia strukturę plików najwyższego poziomu plików ASF.

![ASF File Structure](../asf.png "ASF File Structure")

#### Obiekt nagłówka najwyższego poziomu ASF

Obiekt Header zapewnia dobrze znaną sekwencję bajtów na początku plików ASF i opcjonalnie może zawierać metadane, takie jak informacje bibliograficzne. Zawiera wszystkie informacje wymagane do prawidłowej interpretacji informacji zawartych w obiekcie danych. Obiekt nagłówka może zawierać kilka standardowych obiektów, w tym między innymi:

* Obiekt właściwości pliku — zawiera globalne atrybuty pliku.
* Obiekt właściwości strumienia — definiuje strumień multimediów cyfrowych i jego charakterystykę.
* Obiekt rozszerzenia nagłówka — umożliwia dodanie dodatkowych funkcji do pliku ASF przy zachowaniu kompatybilności wstecznej.
* Treść Opis Obiekt — zawiera informacje bibliograficzne.
* Obiekt polecenia skryptu — zawiera polecenia, które można wykonać na osi czasu odtwarzania.
* Obiekt znacznika — zawiera nazwane punkty przeskoku w pliku.

Obiekt nagłówka jest reprezentowany za pomocą następującej struktury:

|Nazwa pola |Typ pola |Rozmiar (bity)|
---|---|---|
|Identyfikator obiektu| GUID| 128|
|Rozmiar obiektu| SŁOWO| 64|
|Liczba obiektów nagłówka| DWORD| 32|
|Zarezerwowane1| BAJT| 8|
|Zarezerwowane2| BAJT| 8|

#### Obiekt danych najwyższego poziomu ASF

Wszystkie dane mediów cyfrowych dla pliku ASF są zawarte w obiekcie danych i są przechowywane w postaci pakietów danych ASF. Każdy pakiet danych ma stałą długość i zawiera dane dla jednego lub większej liczby strumieni mediów cyfrowych.

#### Obiekty indeksu najwyższego poziomu ASF

Obiekty indeksu najwyższego poziomu ASF mają następujące dwa typy:

* `Prosty obiekt indeksu` — zawiera oparty na czasie indeks danych wideo w pliku ASF. Odstęp czasu między wpisami indeksu jest stały i jest przechowywany w prostym obiekcie indeksu.
* `Obiekt indeksu` — odnosi się do obiektu indeksu, obiektu indeksu obiektu medialnego i obiektu indeksu kodu czasowego, których formaty są podobne. Podobnie jak obiekt prostego indeksu, obiekt indeksu indeksuje według czasu w ustalonych odstępach czasu, ale nie ogranicza się do strumieni wideo.

## Bibliografia

* [Format pliku ASF — Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [Format pliku QuickTime – Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

