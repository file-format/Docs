{
  "date" : "2021-06-09",
  "keywords" :[ "m4p", "mp3", "plik", "rozszerzenie", "format", "co to jest format pliku m4p", "muzyka", "format pliku m4p", "M4b vs MP3", "specyfikacja formatu pliku m4p "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Dowiedz się o formacie plików M4P i interfejsach API, które mogą tworzyć, konwertować i otwierać pliki M4P.",
  "title" :"M4P — format pliku audiobooka MPEG-4",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Czym jest plik M4P?
Plik z rozszerzeniem .m4p to plik audio, który jest zwykle dostępny do pobrania w sklepie Apple iTunes. Innymi słowy, możemy powiedzieć, że M4P jest plikiem AAC, ale chronionym przed kopiowaniem za pomocą zarządzania prawami cyfrowymi (DRM). Oznacza to, że pliki M4P mogą być odtwarzane tylko na autoryzowanych systemach lub urządzeniach. Zwykle pliki M4P są specyficzne dla urządzeń multimedialnych Apple. Tak więc te pliki można odtwarzać tylko na macbookach Apple, podcastach, smartfonach, takich jak iPhone 6 lub iPhone 7.

## Format pliku M4P
M4P oznacza MPEG 4 Protected (audio) i koduje dźwięk za pomocą zaawansowanego kodeka audio (AAC) i chroni plik przed nieautoryzowanym użyciem pliku. Ten format pliku jest zwykle uważany za format pliku audio iTunes Music Store. Apple używa swojego systemu FairPlay Digital Rights Management (DRM) do ochrony plików M4P. FairPlay DRM jest oparty na technologii opracowanej przez firmę Veridisc. Jego mechanizm ochrony polega na szyfrowaniu strumienia audio AAC za pomocą szyfrowania AES. Użytkownik otrzymuje klucz główny, który jest przypisany do jego konta w celu odszyfrowania. Ten format pliku został wprowadzony jako zamiennik formatu pliku MP3, ponieważ MP3 nie był pierwotnie przeznaczony jako plik audio, ale jako warstwa III w pliku wideo MPEG 1 lub 2.


## Specyfikacje formatu plików M4P

Podobnie jak [M4A](/pl/audio/m4a/), pliki M4P również składają się z następujących po sobie fragmentów. Każdy fragment ma 8-bajtowy nagłówek i jest podzielony jako:
- 4-bajtowy rozmiar porcji (big-endian, najpierw starszy bajt)
- typ chunk 4-bajtowy - jedna z predefiniowanych sygnatur: "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "skip", "ftyp", „jP2”, „szeroki”, „ładuj”, „imap”, „matt”, „chap”, „kmat”, „clip”, „crgn”, „sync”, „tmcd”, „PICT”, „scpt” ", "ctab", "ssrc".

Podobnie jak w przypadku M4A, pierwsza porcja w M4P będzie typu „ftype” i ma podtyp o przesunięciu 8. M4P zdefiniowany przez podtyp, który musi być „M4P_”.

Powtarzanie porcji, aż do wykrycia porcji nieznanego typu, utworzy plik M4P (MPEG-4 Audio).

## Bibliografia ##

* [MPEG-4 część 14 – z Wikipedii](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format i przykład odzyskiwania](https://www.file-recovery.com/m4a-signature-format.htm)

