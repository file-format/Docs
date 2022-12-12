{
  "date" : "2021-02-15",
  "keywords" :["MJPEG", "plik", "rozszerzenie", "format", "Motion JPEG", "kompresja", "Obraz JPEG", "wideo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJPEG — format pliku Motion JPEG",
  "description":"Poznaj format plików MJPEG i interfejsy API, które mogą tworzyć i otwierać pliki MJPEG.",
  "linktitle" : "MJPEG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Czym jest plik MJPEG? ##

Plik z rozszerzeniem .mjpeg (Motion JPEG) to plik wideo utworzony przez kompresję pojedynczej klatki wideo jako obraz JPEG. Różni się od standardowych formatów plików MPEG-1 i MPEG-2, gdzie kompresja jest międzyklatkowa i jest ustalana na podstawie przewidywania zawartości w kolejnych klatkach. MJPEG jest obsługiwany przez szeroką gamę aplikacji, w tym przeglądarki internetowe, odtwarzacze multimedialne, aparaty cyfrowe, kamery internetowe, serwery strumieniowe. Wtyczki są dostępne dla aplikacji, które chcą korzystać z formatu plików MJPEG.

## Format pliku MJPEG ##

MJPEG jest oparty na dojrzałym standardzie kompresji, tj. [JPEG](/pl/image/jpeg/), który ma dobrze zdefiniowane biblioteki. Nie można go znormalizować podobnie do standardów takich jak MPEG-2 i nie ma dostępnej dokumentacji, którą można by określić jako pełną specyfikację dla „Motion JPEG”. W przypadku braku takiego standardu, wyjścia różnych producentów mogą powodować problemy ze zgodnością. Jednak firmy takie jak Microsoft i Apple udokumentowały, w jaki sposób pliki M-JPEG są przechowywane w ich natywnych formatach, takich jak [AVI](/pl/video/avi/) i [QT](/pl/video/qt/). Dokument [rfc2435](https://tools.ietf.org/html/rfc2435) opisuje format ładunku RTP dla wideo skompresowanego w formacie JPEG i można się z nim zapoznać jako materiał referencyjny.

## Bibliografia ##

- [RFC2435 — format ładunku RTP dla wideo skompresowanego w formacie JPEG](https://tools.ietf.org/html/rfc2435)
- [Motion JPEG - Wikipedia](https://en.wikipedia.org/wiki/Motion_JPEG)

