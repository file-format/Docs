{
  "date" : "2021-08-24",
  "keywords" :["plik wdb", "format pliku wdb", "co to jest plik wdb", "plik", "przykład wdb", "rozszerzenie pliku wdb","rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku WDB i interfejsy API, które mogą tworzyć i otwierać pliki WDB.",
  "title" :"WDB - plik śledzenia serwera SQL",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Czym jest plik WDB?
Plik z rozszerzeniem .wdb jest w rzeczywistości plikiem bazy danych utworzonym przez Microsoft Works, który był używany do wykonywania funkcji, takich jak system zarządzania bazą danych. Plik WDB jest podobny do pliku Access Database ([MDB](/pl/database/mdb/)), ale jest mniej wydajny i ma większe ograniczenia. Plików WDB nie można otworzyć za pomocą programu Microsoft Access. Możesz jednak otworzyć plik WDB w Microsoft Works, a następnie wyeksportować go do pliku MDB, aby otworzyć plik WDB w MS Access.

## Format pliku WDB
Microsoft Works Database to natywny format bazy danych pakietu biurowego Microsoft Works. Ze względu na zastrzeżony charakter formatu i pewne ograniczenia. Plików WDB nie można otwierać w żadnym innym oprogramowaniu niż Microsoft Works. W formacie pliku powtarzający się, 10-bajtowy nagłówek można znaleźć przed każdym z ciągów tekstowych ASCII reprezentujących wartości pól, które zostały zakończone wartością NULL. Nagłówek zazwyczaj zaczyna się bajtem **\x0f** i NULL, po którym następują 4 bajty danych na przemian z NULL.

### Struktura plików

Struktura pliku WDB jest podana poniżej:
- **1. nagłówek**: od początku pliku, kończąc na \x25\x00\xf2 i 244 bajtach NULL
- **Drugi nagłówek**: zaczynający się od \xffT - tj. \xff\x54 i rozciągający się na 4096 bajtów, który zawiera nazwy kolumn/pól i inne rzeczy, i wydaje się zaczynać od pozycji bajtu 6144.
- **Pole**: wartość ma 10-bajtowy nagłówek o następującym formacie: {bajt typu} {bajt typu, część 2} {bajt danych 1} \x00 {db 2} \x00 {db 3} {db 3 , część 2} {db 4} \x00. bajt danych 2 to numer pola, bajt danych 3 to numer rekordu (dodanie bajtu danych 3, część 2, gdy przekracza 256 rekordów).


## Bibliografia ##

* [Użytkownik:JesseW/format wdb](https://en.wikipedia.org/wiki/Użytkownik:JesseW/wdb_format)

