{
"data": "2023-04-20",
  "keywords": [
"plik ldb",
"co to jest plik ldb",
"jakie informacje zawiera ldb",
"jaki jest cel pliku ldb",
"rozszerzenie ldb",
"plik",
"rozszerzenie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format pliku LDB - plik blokady programu Microsoft Access",
  "description":"Dowiedz się o formacie LDB i jakie informacje zawiera.",
"tytuł łącza": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
      "parent": "misc"
}
},
"lastmod": "2023-04-20"
}

## Czym jest plik LDB?

Plik LDB to plik blokady używany przez program Microsoft Access w celu uniemożliwienia wielu użytkownikom jednoczesnego edytowania tej samej bazy danych. Gdy użytkownik otwiera bazę danych programu Access, program Access tworzy odpowiedni plik LDB w tym samym katalogu, co baza danych. Plik ten zawiera informacje o tym, kto aktualnie korzysta z bazy danych i jakie rekordy edytuje.

Plik LDB jest tworzony automatycznie przez program Microsoft Access po otwarciu bazy danych i usuwany po zamknięciu bazy danych. Należy pamiętać, że pliku LDB nigdy nie należy usuwać ręcznie, ponieważ może to spowodować problemy z bazą danych.

Jeśli napotkasz problemy z bazą danych Microsoft Access, jednym z potencjalnych rozwiązań jest próba usunięcia pliku LDB powiązanego z tą bazą danych. Spowoduje to zwolnienie wszelkich blokad, które mogą uniemożliwiać dostęp do bazy danych. Jednak przed podjęciem tej próby należy wykonać kopię zapasową bazy danych, ponieważ nieprawidłowe usunięcie pliku LDB może spowodować utratę lub uszkodzenie danych.

## Format pliku LDB — więcej informacji

Plik LDB w programie Microsoft Access zawiera informacje o użytkownikach, którzy aktualnie uzyskują dostęp do bazy danych, takie jak ich nazwa użytkownika, nazwa komputera i czas logowania. Plik LDB zawiera również informacje o wszelkich blokadach nałożonych na bazę danych, np. o tym, które rekordy są edytowane przez którego użytkownika.

Oto bardziej szczegółowa lista rodzajów informacji, które można znaleźć w pliku LDB:

- **Nazwa użytkownika** - nazwa użytkownika korzystającego aktualnie z bazy danych
- **Nazwa komputera** – nazwa komputera, z którego użytkownik uzyskuje dostęp do bazy danych
- **Czas logowania** – czas pierwszego otwarcia bazy danych przez użytkownika
- **Blokady rekordów** - informacja o tym, które rekordy są aktualnie edytowane przez jakiego użytkownika
- **Blokady obiektów** - informacja o tym, które obiekty bazy danych (takie jak tabele, formularze czy raporty) są aktualnie edytowane przez którego użytkownika
- **Informacje o połączeniu** - informacja o sposobie połączenia użytkownika z bazą danych (np. czy korzysta z połączenia lokalnego czy sieciowego)

Informacje zawarte w pliku LDB są używane przez program Microsoft Access w celu zapobiegania jednoczesnemu wprowadzaniu przez wielu użytkowników sprzecznych zmian w tej samej bazie danych. Gdy użytkownik spróbuje edytować rekord lub obiekt, który jest już zablokowany przez innego użytkownika, program Microsoft Access wyświetli komunikat wskazujący, że obiekt jest już używany. Plik LDB jest aktualizowany, gdy użytkownicy otwierają i zamykają bazę danych oraz wprowadzają zmiany w zablokowanych obiektach.

## Bibliografia
* [Co to jest plik LDB?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

