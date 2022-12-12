{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX - Plik skrzynki poczty e-mail",
  "description":"Poznaj format pliku MBOX i interfejsy API, które mogą tworzyć i otwierać pliki MBOX.",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik MBOX?

Format pliku MBox to ogólny termin reprezentujący kontener do zbierania wiadomości poczty elektronicznej. Wiadomości są przechowywane w kontenerze wraz z załącznikami. Wiadomości z całego folderu są zapisywane w pojedynczym pliku bazy danych, a nowe wiadomości są dołączane na końcu pliku. Liczne aplikacje i API zapewniają obsługę formatu plików MBox, takich jak Apple Mail i Mozilla Thunderbird.

## Format pliku MBOX ##

Format pliku MBox pozostawał nieznormalizowany przez dość długi czas, aż do 2005 r., kiedy aplikacja/mbox została ustandaryzowana jako [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Wiadomości w formacie RFC 2822 , są łączone jeden po drugim w formacie pliku MBox. Każda wiadomość zaczyna się od linii oddzielającej, która identyfikuje nadawcę wiadomości, a także datę i godzinę odebrania wiadomości przez odbiorcę końcowego (albo system ostatniego przeskoku na ścieżce transferu, albo system, który służy jako sklep pocztowy). Każda wiadomość jest zwykle zakończona pustą linią. Koniec bazy danych jest zwykle rozpoznawany przez brak jakichkolwiek dodatkowych danych lub obecność wyraźnego znacznika końca pliku.

## Czytanie wiadomości z pliku MBox ##

Czytnik skanuje plik mbox w poszukiwaniu linii From_. Każda linia From_ oznacza początek wiadomości. Czytelnik nie powinien próbować wykorzystywać faktu, że każda linia From_ (poza początkiem pliku) jest pusta. Gdy czytnik znajdzie wiadomość, wyodrębnia (prawdopodobnie uszkodzoną) kopertę z nadawcą i datą dostarczenia z wiersza From_. Następnie czyta do następnej linii From_ lub końca pliku, w zależności od tego, co nastąpi wcześniej. Usuwa ostatnią pustą linię i usuwa cytowanie wierszy >From_ i >>From_ i tak dalej. Wynikiem jest komunikat RFC 822.

## Uwagi dotyczące kodowania ##

Zawartość pliku MBox może zostać nieodwracalnie wymieszana, gdy otrzymana wiadomość e-mail zawiera plik Mbox jako załącznik i jest zapisywana w innym pliku Mbox. Aby tego uniknąć, systemy przesyłania wiadomości muszą kodować bazę danych mbox za pomocą nieprzejrzystego kodowania transferu (takiego jak BASE64 lub Quoted-Printable) za każdym razem, gdy taki obiekt jest przesyłany za pośrednictwem protokołów przesyłania wiadomości. Implementatorzy powinni być również przygotowani na lokalne kodowanie danych mbox w przypadku otrzymania niezgodnych danych.

## Bibliografia ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)

