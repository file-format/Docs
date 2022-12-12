{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku MPG",
  "keywords" :[ "MPG", "plik", "rozszerzenie", "format", "format wideo", "co to jest format pliku mpg", "format pliku mpg", "odtwarzacz plików mpg", "kompresja mpeg", "wideo ", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"Poznaj format pliku MPG i interfejsy API, które mogą tworzyć i pokaż, jak otwierać pliki MPG.",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-26"
}

## Co to jest format pliku MPG? ##

Plik z rozszerzeniem .mpg należy do grupy rozszerzeń plików służących do kompresji audio i wideo MPEG-1 lub MPEG-2. Wideo MPEG-1 Part 2 nie jest łatwo dostępne, a to rozszerzenie (format pliku MPG) zwykle wskazuje na strumień programu MPEG, który jest zdefiniowany w MPEG-1 i MPEG-2, lub strumień transportowy MPEG, który jest zdefiniowany w MPEG-2 . Istnieją również inne rozszerzenia, takie jak .m2ts, określające dokładny kontener, w tym przypadku MPEG-2 TS, ale ma to niewielkie znaczenie dla nośników MPEG-1. [.mp3](https://docs.fileformat.com/audio/mp3/) to najpopularniejsze rozszerzenie plików zawierających dźwięk w formacie MP3. Plik MP3 to typowy strumień surowego dźwięku; Tradycyjny sposób oznaczania plików MP3 polega na zapisywaniu danych strumienia w „śmieciowych” segmentach każdej klatki, które zapisują informacje o multimediach, ale są odrzucane przez **odtwarzacz plików mpg**. Jest to podobna technika używana do oznaczania plików AAC, ale obecnie jest mniej obsługiwana.

## Kompresja MPEG ##

Nazwa MPEG oznacza Moving Pictures Experts Group. MPEG to narzędzie do kompresji wideo, które obejmuje kompresję obrazu i dźwięku, a także synchronizację tych dwóch elementów.
Obecnie istnieje kilka standardów MPEG.

- MPEG-1 proponuje się dla pośrednich szybkości transmisji danych, rzędu 1,5 Mbit/s.
- MPEG-2 jest proponowany dla dużych szybkości transmisji danych, co najmniej 10 Mbit/s.
- MPEG-3 został zaproponowany do kompresji HDTV, ale okazał się zbędny i został połączony z MPEG-2.
- MPEG-4 jest proponowany dla bardzo niskich szybkości przesyłania danych poniżej 64 Kbit/s.


## Strumień programu w formacie pliku MPG ##

Strumień programu jest kontenerem służącym do multipleksowania cyfrowego dźwięku, obrazu i nie tylko. Format Program Stream jest określony w pierwszej części MPEG-1 (ISO/IEC 11172-1) i pierwszej części MPEG-2, Systems (norma ISO/IEC 13818-1/ITU-T H.222.0). Strumień programu MPEG-2 jest analogowy i podobny do warstwy systemowej ISO/IEC 11172 i kompatybilny w przód.

### Szczegóły kodowania ###

Oto szczegóły kodowania częściowego formatu nagłówka pakietu MPEG-2 Program Stream:

| Imię | Liczba bitów | Opis |
---|---|---|
| synchronizuj bajty | 32 | 0x000001BA |
| bity znacznikowe | 2 | 01b dla wersji MPEG-2. Bity znacznikowe dla wersji MPEG-1 to 4 bity o wartości 0010b. |
| Zegar systemowy [32..30] | 3 | Bity odniesienia zegara systemowego (SCR) od 32 do 30 |
| bit znacznika | 1 | 1 Bit zawsze ustawiony. |
| Zegar systemowy [29..15] | 15 | Bity zegara systemowego od 29 do 15 |
| bit znacznika | 1 | 1 Bit zawsze ustawiony. |
| Zegar systemowy [14..0] | 15 | Bity zegara systemowego od 14 do 0 |
| bit znacznika | 1 | 1 Bit zawsze ustawiony. |
| rozszerzenie SCR | 9 | |
| bit znacznika | 1 | 1 Bit zawsze ustawiony. |
| szybkość transmisji | 22 | W jednostkach 50 bajtów na sekundę. |
| bity znacznikowe | 2 | 11 Bity zawsze ustawione. |
| zarezerwowane | 5 | zarezerwowane do wykorzystania w przyszłości |
| długość farszu | 3 | |
| wypychanie bajtów | 8*długość nadzienia | |
| nagłówek systemowy (opcjonalnie) | 0 lub więcej | jeśli kod startowy nagłówka systemowego jest następujący: 0x000001BB |

Poniższa tabela przedstawia częściowy format nagłówka systemu:

| Imię | Liczba bajtów | Opis |
---|---|---|
| synchronizuj bajty | 4 | 0x000001BB |
| długość nagłówka | 2 | |
| bity związane z szybkością i znaczniki | 3 | |
| oprawa audio i flagi | 1 | |
| flagi, bit znacznika i powiązanie wideo | 1 | |
| Ograniczenie szybkości pakietów i zarezerwowany bajt | 1 | |


## Bibliografia ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



