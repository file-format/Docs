{
  "date" : "2021-06-21",
  "keywords" :["UDL", "rozszerzenie", "plik udl", "format pliku udl", "Typ pliku bazy danych", "Format pliku bazy danych", "co to jest plik udl" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku UDL i interfejsy API, które mogą tworzyć i otwierać pliki UDL.",
  "title" :"UDL — uniwersalny plik łącza danych firmy Microsoft",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## Czym jest plik UDL?
Plik z rozszerzeniem .udl nazywa się plikiem Microsoft Universal Data Link; określanie atrybutów połączenia; używany przez aplikacje systemu Windows do nawiązywania połączenia z bazą danych. Plik UDL zawiera parametry połączenia dla źródła danych OLE DB; z nazwą użytkownika i hasłem oraz podstawowymi właściwościami parametrów połączenia. Aby uniknąć bezpośredniego ręcznego określania właściwości w parametrach połączenia, można zamiast tego użyć okna dialogowego Właściwości łącza danych do zapisania informacji o połączeniu w pliku .udl.

## Format pliku UDL
Zasadniczo plik UDL (Universal Data Link) to prosty plik tekstowy, który składa się z parametrów połączenia z bazą danych z określonymi atrybutami lub właściwościami. Po utworzeniu pliku UDL można go przetestować za pomocą programu SQL Server Management Studio w celu zweryfikowania łączności.

### Właściwości parametrów połączenia
Następujące właściwości można ustawić w UDL, aby zapewnić odpowiednią łączność:

- **Nazwa serwera**: lokalizacja serwera, na którym znajduje się baza danych, do której chcesz uzyskać dostęp.
- **Opcje uwierzytelniania**
- **Uwierzytelnianie Windows**: Uwierzytelnianie do SQL Server przy użyciu poświadczeń konta Windows aktualnie zalogowanego użytkownika.
- **Uwierzytelnianie serwera SQL**: Uwierzytelnianie przy użyciu identyfikatora logowania i hasła.
- **Active Directory — zintegrowane**: zintegrowane uwierzytelnianie z tożsamością usługi Azure Active Directory; może być również używany do uwierzytelniania systemu Windows w SQL Server.
- **Active Directory — hasło**: Uwierzytelnianie identyfikatora użytkownika i hasła za pomocą tożsamości usługi Azure Active Directory.
- **Active Directory — uniwersalna z obsługą usługi MFA**: interaktywne uwierzytelnianie z tożsamością usługi Azure Active Directory.
- **Active Directory — jednostka usługi**: uwierzytelnianie za pomocą nazwy głównej usługi Azure Active Directory.
- **Server SPN**: Jeśli korzystasz z zaufanego połączenia, możesz określić główną nazwę usługi (SPN) dla serwera.
- **Nazwa użytkownika**: wpisz identyfikator użytkownika, który ma być używany do uwierzytelniania podczas logowania się do źródła danych.
- **Hasło**: Wpisz hasło używane do uwierzytelniania podczas logowania się do źródła danych.
- **Puste hasło**: gdy jest zaznaczone, umożliwia określonemu dostawcy użycie pustego hasła w parametrach połączenia.
- **Zezwalaj na zapisywanie hasła**: umożliwia zapisanie hasła wraz z parametrami połączenia.
- **Użyj silnego szyfrowania danych**: dane przesyłane przez połączenie będą szyfrowane.
- **Zaufany certyfikat serwera**: Certyfikat serwera zostanie zweryfikowany.
- **Baza danych**: nazwa bazy danych, do której chcesz uzyskać dostęp.
- **Dołącz plik bazy danych jako nazwę bazy danych**: Określa nazwę podstawowego pliku dołączanej bazy danych.

## Bibliografia ##

* [Składniki dostępu do danych firmy Microsoft](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [Konfiguracja uniwersalnego łącza danych (UDL)](https://docs.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

