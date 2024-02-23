{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Dowiedz się o formacie pliku ABCDDB i interfejsach API, które umożliwiają tworzenie i otwieranie plików ABCDDB.",
  "title" : "Format pliku ABCDDB — plik bazy danych książki adresowej Apple z listą kontaktów",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-pl",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Co to jest plik ABCDDB?

Plik z rozszerzeniem **.ABCDDB** oznacza bazę danych listy kontaktów Apple Address Book. Należy do aplikacji **Książka Adresowa**, powszechnie znanej również jako **Kontakty**. Jest to aplikacja wbudowana i dołączona do systemów operacyjnych iOS i macOS. Aplikacja Kontakty umożliwia użytkownikom zapisywanie i organizowanie informacji związanych z ich kontaktami, w tym osobami, firmami i organizacjami. Ta aplikacja pozwala użytkownikom śledzić szczegóły, takie jak nazwiska, adresy, numery telefonów i adresy e-mail, a także kategoryzować kontakty w grupy.

## Relacja z SQLite i typowa ścieżka

Książka adresowa firmy Apple (znana również jako Kontakty) przechowuje informacje kontaktowe w postaci wizytówek vCard w folderze metadanych. **Plik _ABCDDB_ jest w rzeczywistości _plikiem danych SQLite 3_**.

SQLite to popularny system zarządzania bazami danych, który został zaprojektowany tak, aby był lekki i samodzielny. Jest używany w wielu różnych typach oprogramowania i urządzeń. SQLite jest rodzajem RDBMS, co oznacza, że przechowuje dane w tabelach, które są ze sobą powiązane za pomocą kluczy. Może obsługiwać szereg typów danych, w tym liczby całkowite, liczby zmiennoprzecinkowe, ciągi znaków i dane binarne. Dodatkowo SQLite obsługuje transakcje, które umożliwiają użytkownikom wykonywanie wielu operacji na bazach danych razem w ramach jednej jednostki pracy.

Zwykle w tym miejscu przechowywany jest plik z rozszerzeniem ABCDDB

`~/Biblioteka/Wsparcie aplikacji/Książka adresowa/Książka adresowa-v22.abcddb`

## Naprawianie uszkodzonej bazy danych kontaktów

Zanim spróbujesz to zrobić, najpierw wykonaj kopię zapasową. Następnie przejdź do

`~/Biblioteka/Wsparcie aplikacji/Książka adresowa`

W tym katalogu znajdziesz trzy pliki, w tym jeden z rozszerzeniem .abcddb

- `addressbook-v22.abcddb`
- `addressbook-v22.abcddb-wal`
- `addressbook-v22.abcddb-shm`

Usuń wszystkie te pliki i otwórz ponownie Kontakty, a zacznie działać ponownie.

## Przywróć bazę danych AddressBook z kopii zapasowej

Załóżmy, że kontakty w bazie danych AddressBook są przechowywane w `addressbook-v22.abcddb`

- Najpierw wykonaj kopię zapasową danych książki adresowej i zamknij wszystkie aplikacje.
- Przenieś plik bazy danych do podkatalogu `~/Library/Application Support/AddressBook`
- Uruchom **Książka adresowa.aplikacja**.

## Eksportuj dane pliku ABCDDB do programu Microsoft Access

Ponieważ plik jest plikiem danych SQLite 3, możesz wyeksportować dane z pliku abcddb do programu Microsoft Access za pomocą złącza ODBC.

Złącze SQLite ODBC to biblioteka oprogramowania i sterownik umożliwiający aplikacjom obsługującym interfejs ODBC łączenie się z bazą danych SQLite. Zawiera bibliotekę definiującą interfejs ODBC oraz sterownik, który tłumaczy ten interfejs na wywołania API SQLite. Aby wykorzystać złącze SQLite ODBC, należy je najpierw zainstalować, a następnie skonfigurować źródło danych ODBC na swoim komputerze. Po wykonaniu tych kroków dowolna aplikacja wyposażona w obsługę ODBC będzie mogła połączyć się ze źródłem danych i pobrać dane z bazy danych SQLite.

## Bibliografia
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Baza danych kontaktów dla komputerów Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Jak mogę otworzyć lub wyeksportować plik abcddb w programie Excel w systemie Windows 7?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -Windows-7-Excel)

