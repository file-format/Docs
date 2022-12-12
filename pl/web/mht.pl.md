{
  "date" : "2019-10-11",
  "keywords" :[ "mht", "plik mht", "format pliku mht", "typ pliku mht", "plik", "typ", "co to jest plik mht"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHT - format pliku MIME HTML",
  "description" :"Dowiedz się o formacie plików MHT i interfejsach API do tworzenia i otwierania plików MHT.",
  "linktitle" : "MHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Czym jest plik MTH?

Plik z rozszerzeniem .mht to format pliku archiwizacji obsługujący MIME, który zawiera różne typy danych w jednym pliku. Może przechowywać dane, takie jak tekst, obrazy, styl strony w postaci plików [CSS](/pl/web/css/), JavaScript i inne zasoby jako osadzone w nim zasoby. Pliki MHT, mające komunikat typu MIME/rfc822, zawierają całą zawartość pliku HTML jako pojedynczy plik archiwum do przechowywania podczas archiwizacji na urządzeniach pamięci masowej. Aplikacje, takie jak Microsoft Word, umożliwiają konwersję dokumentów WORD do formatu MHT poprzez eksport do pliku MHT. Pliki MHT można otwierać za pomocą popularnych przeglądarek, takich jak Microsoft Internet Explorer i Google Chrome.

## Format pliku MHT

Podobnie jak [MHTML](/pl/web/mhtml/), MHT jest również hermetyzacją MIME zagregowanych dokumentów HTML. Zawartość dokumentu w dokumencie MHT, taka jak obrazy w wierszu, arkusze stylów, aplety itp., jest zakodowana w formacie MIME, jeśli jest połączona z zasobem głównym za pośrednictwem identyfikatorów URI. Klienci poczty e-mail, tacy jak Microsoft Outlook, przechowują wiadomości e-mail (zwykle [EML](/pl/email/eml/)) w formacie pliku MHT. Pełne specyfikacje formatu plików MHT są dostępne w dokumencie [RFC 822](https://tools.ietf.org/html/rfc822) i można się do nich odnieść w celu opracowania oprogramowania, które może przetwarzać pliki MHT.

## Różnica między MHT i MHTML

Podczas zapisywania strony internetowej użytkownik jest proszony o ustalenie rodzaju formatu pliku, w jakim strona internetowa ma zostać zapisana w systemie natywnym. Najczęściej użytkownik jest zdezorientowany między językiem znaczników a formatami plików MHTML. Zauważają, że kłopotliwe jest zobaczenie, że format pliku jest zdrowszy między nimi.

Gdy użytkownik zdecyduje się uniknąć marnowania strony internetowej jako języka znaczników, wówczas tworzony jest folder, który zawiera wiele plików dla różnej zawartości strony, tj. zupełnie inną jednostkę obszaru plików tworzoną dla tekstu, grafiki, apletów itp. strony online, ponieważ MHTML tworzy jeden plik dla całej strony online. Wszystkie elementy strony wraz z grafiką, linkami i plikami alternatywnymi stanowią jednostkę powierzchni osadzone w jednym pliku.

Oczywiście obsługa plików MHT lub MHTML jest prosta, ponieważ plik ten można chronić i udostępniać po prostu za pośrednictwem poczty e-mail. Jednak jednostka obszaru plików języka znaczników poniżej szansy na utratę informacji, ponieważ utrata lub usunięcie nawet jednego pliku może sprawić, że cały folder języka znaczników stanie się bezużyteczny dla użytkownika.

## Bibliografia

* [MHTML - Wikipedia](https://en.wikipedia.org/wiki/MHTML)
* [MHT RFC](https://tools.ietf.org/html/rfc822)

