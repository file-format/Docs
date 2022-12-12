{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "plik", "rozszerzenie", "format", "co to jest format pliku m4a", "muzyka", "format pliku m4a", "M4A vs MP3", "specyfikacja formatu pliku m4a "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku M4A i interfejsy API, które mogą tworzyć, konwertować i otwierać pliki M4A.",
  "title" :"M4A - Plik dźwiękowy MPEG-4",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Czym jest plik M4A?

**Format pliku M4A** to plik audio utworzony przy użyciu algorytmu AAC (Advanced Audio Coding), znanego jako kompresja stratna. Słowo M4A w skrócie MPEG 4 Audio. Te pliki audio mają zazwyczaj rozszerzenie .m4a. Dotyczy to zwłaszcza treści niechronionych. Może przechowywać różne rodzaje treści audio, takie jak audiobooki, piosenki i podcasty. M4A jest zwykle realizowany jako bardziej zaawansowany format niż MP3, który nie był zwykle przeznaczony wyłącznie do odtwarzania dźwięku. To tylko warstwa audio w plikach wideo MPEG 1 lub 2.

Format M4A jest szyfrowany przez FairPlay Digital Rights Management, podobnie jak w przypadku sprzedaży w sklepie iTunes Store z rozszerzeniem .m4p. IPhone'y Apple używają dźwięku MPEG-4 do swoich dzwonków, ale te pliki audio używają rozszerzenia .m4r.


## M4A kontra MP3

Zarówno M4A, jak i [MP3](https://docs.fileformat.com/audio/mp3/) to formaty plików wyłącznie audio.

**M4A**: Lepszy niż MP3 pod względem jakości i rozmiarów, gdy jest zakodowany z tą samą przepływnością. Rozszerzenie pliku .m4a jest tak powszechne, ponieważ były używane przez firmę Apple do użytku w iTunes Music Store. M4A to plik audio skompresowany przy użyciu technologii MPEG-4; algorytm kompresji stratnej. Zasadniczo jest kojarzony z „MPEG-4 Audio Layer”, pliki z rozszerzeniem .m4a są warstwą dźwiękową filmów MPEG-4. Ma on wyprzedzić MP3 i stać się nowym standardem kompresji dźwięku. Pod wieloma względami jest bardzo zbliżony do MP3, ale został wprowadzony, aby mieć lepszą jakość w tym samym lub nawet mniejszym rozmiarze pliku. Format M4A został po raz pierwszy wprowadzony przez firmę Apple. Typ formatu jest również realizowany jako bezstratny koder Apple (ALE).

Dlatego obecnie M4A nie może odnieść głównego nurtu sukcesu MP3, ponieważ format audio nie jest jeszcze generalnie odtwarzalny. Jest to w jakiś sposób ograniczone tylko do MacOS, iPoda i innych produktów Apple.

**Mp3**: Najbardziej znany cyfrowy format audio. Był to również jeden z pierwszych formatów kompresji na scenie i stał się bardzo popularny wśród melomanów. Jego główny nurt jest tak szybki, że ten typ pliku może być odtwarzany uniwersalnie i na prawie wszystkim, zarówno sprzętowym, jak i programowym. Ogólnie rzecz biorąc, M4A zapewni lepszą jakość dźwięku, ale wielu twierdzi, że niezależnie od tego, czy to prawda, czy nie, różnica w dźwięku jest nie do odróżnienia, a próba konwersji plików MP3 do plików M4A byłaby stratą czasu. W końcu konwersja spowoduje utratę oryginalnej jakości dźwięku.

## Specyfikacja formatu pliku M4A

Pliki M4A składają się z następujących po sobie fragmentów. Każdy fragment ma 8-bajtowy nagłówek i jest podzielony jako:
- 4-bajtowy rozmiar porcji (big-endian, najpierw starszy bajt)
- 4-bajtowy typ chunk - jedna z predefiniowanych sygnatur: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", „jP2”, „szeroki”, „ładuj”, „ctab”, „imap”, „matt”, „kmat”, „clip”, „crgn”, „sync”, „chap”, „tmcd”, „scpt” ", "ssrc", "PICT".

Pierwsza porcja będzie typu „ftype” i ma podtyp z przesunięciem 8. M4A zdefiniowany przez podtyp, który musi być „M4A_”, dla podtypu M4B musi być „M4B_”, a dla podtypu M4P musi być „M4P_”.

Powtarzanie porcji, aż do wykrycia porcji nieznanego typu, utworzy plik M4A (MPEG-4 Audio).

## Bibliografia ##

* [MPEG-4 część 14 – z Wikipedii](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format i przykład odzyskiwania](https://www.file-recovery.com/m4a-signature-format.htm)

