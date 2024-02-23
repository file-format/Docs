{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Dowiedz się o formacie pliku DSN i interfejsach API, które umożliwiają tworzenie i otwieranie plików DSN.",
  "title" : "Format pliku DSN — plik nazwy źródła bazy danych",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-pl",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Czym jest plik DSN?

DSN oznacza nazwę źródła danych” i jest to format pliku używany do przechowywania informacji o połączeniu z bazą danych. Pliki DSN są zwykle używane w połączeniu z ODBC (Open Database Connectivity) i umożliwiają łatwy dostęp do określonej bazy danych, dostarczając niezbędnych informacji do połączenia się z nią, takich jak nazwa serwera, nazwa użytkownika i hasło. Plik ma zwykle postać zwykłego tekstu i można go tworzyć i edytować za pomocą edytora tekstu. Można go używać w różnych systemach operacyjnych, takich jak Windows, Linux i Mac.

## Jak utworzyć plik DSN?

Metoda tworzenia pliku DSN może się różnić w zależności od systemu operacyjnego i dostępnych narzędzi. Poniższe kroki stanowią ogólny przegląd procesu tworzenia pliku DSN w systemie Windows.

1. Otwórz Administratora źródeł danych ODBC, wyszukując Źródła danych ODBC” w menu Start.
2. Wybierz zakładkę Systemowe DSN” i kliknij przycisk Dodaj”.
3. Wybierz odpowiedni sterownik dla bazy danych, z którą chcesz się połączyć, i kliknij Zakończ”.
4. Wprowadź informacje niezbędne do połączenia z bazą danych, takie jak nazwa serwera, nazwa użytkownika i hasło.
5. Kliknij OK”, aby zapisać plik DSN.

Alternatywnie możesz utworzyć plik DSN ręcznie, tworząc zwykły plik tekstowy z rozszerzeniem .dsn i wprowadzając niezbędne informacje o połączeniu w formacie:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Następnie możesz użyć ścieżki tego pliku jako DSN w swoim kodzie/skrypcie, aby połączyć się z bazą danych.

## Programy otwierające plik DSN

Plik DSN to zwykły plik tekstowy, w którym przechowywane są informacje używane do łączenia się z bazą danych, takie jak nazwa serwera, nazwa użytkownika i hasło. Zwykle jest używany w połączeniu z ODBC (Open Database Connectivity), aby zapewnić łatwy dostęp do określonej bazy danych.

Aby otworzyć i wyświetlić zawartość pliku DSN, możesz użyć dowolnego edytora tekstu, takiego jak Notatnik, Sublime Text, Atom itp. Programy te pozwolą Ci otworzyć plik DSN i wyświetlić zapisane w nim informacje o połączeniu.

Aby jednak użyć pliku DSN do połączenia się z bazą danych i wykonania operacji takich jak SELECT, INSERT, UPDATE, DELETE itp., potrzebny jest program z obsługą ODBC, taki jak język programowania, taki jak Python, Java, C# lub narzędzie do zarządzania bazami danych, takie jak Microsoft Access , wymagane jest SQL Server Management Studio. Programy te mogą wykorzystywać informacje zawarte w pliku DSN do łączenia się z bazą danych i wykonywania żądanych operacji.

## Bibliografia

* [Co to jest DSN (nazwa źródła danych)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



