{
  "date" : "2021-08-30",
  "keywords" :["ACCDW", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Pliki bazy danych" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Dowiedz się o formacie plików ACCDW i interfejsach API, które mogą tworzyć i otwierać pliki ACCDW.",
  "title" :"ACCDW - Plik łącza bazy danych programu Microsoft Access",
  "linktitle" : "ACCDW",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-30"
}

## Czym jest plik ACCDW?

Plik z rozszerzeniem .accdw jest plikiem łącza utworzonym za pomocą programu Microsoft Access i zawiera informacje o łączu do pobrania pliku bazy danych programu Access, tj. [ACCDB](/pl/database/accdb/) z serwera SharePoint. Pozwala to użytkownikom na udostępnianie plików bazy danych, które są hostowane zdalnie. Otwarcie pliku ACCDW powoduje pobranie połączonego pliku ACCDB jako lokalnej kopii na komputerze użytkownika. Pobrany plik jest zapisywany w domyślnej lokalizacji pobierania i można uzyskać do niego dostęp, przechodząc do niego. Zwykle pliki te są pobierane i przechowywane pod nazwą „SiteServer.accdb”, która odnosi się do baz danych klienta.

## Format pliku ACCDW — więcej informacji

Plik ACCDW to plik XML zawierający łącze do witryny programu SharePoint, w której hostowane są usługi programu Access. Jest to tylko skrót i wymaga połączenia z Internetem, aby je uruchomić. W przypadku trybu online SharePoint jest buforowany lokalnie, aby zapewnić możliwość późniejszego przełączenia go w tryb offline.

## Bibliografia

* [Specyfikacje programu Access 2016](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [Którego formatu pliku programu Access powinienem użyć?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)
