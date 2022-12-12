{
  "date" : "2021-02-15",
  "keywords" :["plik vp6", "format pliku vp6", "co to jest plik vp6", "plik", "przykład vp6", "rozszerzenie pliku vp6","rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 — plik wideo TrueMotion",
  "description":"Poznaj format plików VP6 i interfejsy API, które mogą tworzyć i otwierać pliki VP6.",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Czym jest plik VP6?

VP6 to format wideo z kompresją stratną, który został wprowadzony przez technologie On2 w maju 2003 roku. Jest częścią serii kodeków wideo opracowanych przez TrueMotion, w tym V3, V4 i V5. Format był krótko używany w dziedzinie nadawania, na przykład w raportach BBC i oprogramowaniu QuickLink. VP6 został zastąpiony przez VP7 Codec w styczniu 2005 roku z lepszą kompatybilnością kompresji.

## Format pliku VP6

Pełne specyfikacje plików V6 nie są dostępne publicznie. On2 początkowo upublicznił specyfikacje, ale wkrótce stały się one niedostępne dla zwykłych użytkowników. Nieoficjalna dokumentacja formatu pliku VP6 jest dostępna na [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6), do której można się odnieść w celach informacyjnych dla programistów.

### Makrobloki (MB)

Podobnie jak MPEG-2, MPEG-4 części 2 i 10, każda klatka wideo pliku VP6 składa się z tablicy makrobloków (MB) o wymiarach 16x16. Każdy MB może pracować w jednym z następujących trybów:

* Wewnątrz MB
* Inter MB, null MV, poprzednie odniesienie do ramki
* Inter MB, różnicowy MV, odniesienie do poprzedniej ramki
* Inter MB, cztery MV, odniesienie do poprzedniej klatki
* Inter MB, MV 1, odniesienie do poprzedniej klatki
* Inter MB, MV 2, odniesienie do poprzedniej klatki
* Inter MB, null MV, odniesienie do ramki z zakładkami
* Inter MB, różnicowy MV, odniesienie ramki z zakładkami
* Inter MB, MV 1, odnośnik do ramki z zakładkami
* Inter MB, MV 2, odnośnik do ramki z zakładkami

### Nagłówek ramki

Nagłówek ramki VP6 jest pokazany poniżej, zgodnie z pakowaniem bitów typu big-endian.

|Składnia|Liczba bitów|Typ|Symantecs|
---|---|---|---|
|tryb_klatki|1|Enum|0x0 oznacza wewnątrzramkę|
|qp |6 |Bez znaku |Dopuszczalny zakres parametrów kwantyzacji 0..63|
|znacznik| 1| stała| 0=VP61/62, 1=VP60|
|if (tryb_klatki == 0) { | 0 | |równa się INTRA_FRAME|
|wersja |5| stała| 6=VP60/61, 7=VP60 (sztuka elektroniczna), 8=VP62|
|wersja2 |2| Stała |0=VP60, 3=VP61/62|
|przeplot |1| Boolean |true (1) oznacza, że zostanie użyty przeplot|
|if (znacznik==1 lub wersja2==0) {||||
|przesunięcie |16 |Bez znaku| przesunięcie bufora wtórnego (bajty względem początku bufora)|
|}||||
|dim_y |8| Niepodpisany| Wysokość makrobloku wideo|
|wymiar_x |8| Niepodpisany| Szerokość makrobloku wideo|
|render_y |8 |Bez znaku |Wyświetl wysokość wideo|
|render_x |8 |Bez znaku |Wyświetl szerokość wideo|
|}inaczej{||||
|if (znacznik==1 lub wersja2==0) {||||
|przesunięcie |16 |Bez znaku |Przesunięcie bufora pomocniczego (bajty względem początku bufora)|
|}||||
|}||||

## Bibliografia

* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)

