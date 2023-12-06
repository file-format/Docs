{
  "date" : "2023-06-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Dowiedz się o formacie pliku ABS i interfejsach API, które umożliwiają tworzenie i otwieranie plików ABS.",
  "title" :"Rozszerzenie pliku ABS - Format pliku absolutnej bazy danych Delphi",
  "linktitle" : "ABS",
  "menu" : {
    "docs" : {
      "identifier":"database-abs",
      "parent" : "database"
}
},
  "lastmod" : "2023-06-18"
}

## Czym jest plik ABS?

Plik z rozszerzeniem .abs to baza danych wygenerowana i używana przez bazę danych Absolute, która jest silnikiem bazy danych dla IDE do tworzenia oprogramowania Delphi. Zastąpił silnik bazy danych Borland (DBE) i jest bardziej kompaktowy, szybki, solidny i łatwy w użyciu. Baza danych ABS kompiluje się jako część pliku EXE aplikacji, dzięki czemu aplikacja jest szybsza i mniejsza. Dane są przechowywane w pliku ABS w ustrukturyzowanym formacie relacyjnym.

## Format pliku ABS — więcej informacji

Pliki ABS są przechowywane jako część [pliku EXE](/pl/executable/exe/) aplikacji, który jest zwykle przechowywany jako plik binarny. Plików binarnych nie można otworzyć w żadnym edytorze tekstu i zapewniają szybki dostęp do zawartości pliku bazy danych.

### Kluczowe cechy formatu pliku ABS

Pliki ABS są dość proste i można je osadzić w pliku wykonywalnym aplikacji. Posiada następujące funkcje:

* Brak BDE; żadnych bibliotek DLL
* Baza danych jednoplikowa
* Obsługa SQL'92 (DDL i DML).
* Kompatybilny ze standardowymi i zewnętrznymi kontrolami baz danych
* Tryb jednego użytkownika i wielu użytkowników (serwer plików)
* Działa świetnie na wszystkich wersjach systemu Windows - od 98 do najnowszych, nie wymaga żadnych aktualizacji ani dodatków Service Pack
* Ultraszybkie tabele w pamięci
* Niezrównana łatwość obsługi
* Silne szyfrowanie
* Kompresja BLOB
* Bezpłatnie do użytku osobistego
* Dostępny pełny kod źródłowy
* Dystrybucja bez tantiem

## Bibliografia

 * [Delphi Absolute Database File Format](https://www.componentace.com/bde_replacement_database_delphi_absolute_database.htm)
