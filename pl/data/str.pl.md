{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Plik STR - Plik obiektu listy struktur dBASE - Co to jest plik .str i jak go otworzyć?",
  "description" : "Dowiedz się o pliku obiektu listy struktur STR dBASE i o tym, jak go otworzyć.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-pl",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## .STR opcja № 1

Format pliku STR jest powszechnie kojarzony z dBASE, systemem zarządzania bazami danych. W dBASE plik .str zazwyczaj reprezentuje plik obiektu listy struktur. Plik ten zawiera strukturę tabeli bazy danych, zawierającą informacje o polach (kolumnach) i ich właściwościach.

Plik obiektu listy struktur (.str) zawiera metadane, takie jak nazwy pól, typy danych, długości pól i wszelkie inne właściwości powiązane z każdym polem w tabeli bazy danych. Służy do definiowania struktury tabeli bazy danych bez uwzględniania rzeczywistych rekordów danych.

Programy takie jak dBASE lub inne narzędzia do zarządzania bazami danych mogą wykorzystywać ten plik do zrozumienia układu tabeli bazy danych i wykonywania operacji, takich jak wysyłanie zapytań, aktualizowanie lub tworzenie nowych rekordów w oparciu o tę strukturę.

Oto podstawowy przykład tego, co może zawierać plik STR:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

W tym przykładzie opisano tabelę zawierającą cztery pola: ID, Name, Age i DOB, wraz z odpowiadającymi im typami danych i długościami.

## Jak otworzyć plik STR?

Podstawowym sposobem otwierania plików .str jest użycie samego dBASE, szczególnie w systemach operacyjnych Windows. dBASE potrafi czytać i interpretować zawartość tych plików, umożliwiając użytkownikom przeglądanie i pracę ze strukturą bazy danych.

Ponieważ pliki .str są zasadniczo zwykłymi plikami tekstowymi, które zawierają informacje o strukturze bazy danych, można je również otworzyć za pomocą edytora tekstu. Przykłady edytorów tekstu obejmują Microsoft Notatnik w systemie Windows i Apple TextEdit na komputerze Mac. Po otwarciu w edytorze tekstu będzie można zobaczyć zawartość pliku, w tym nazwy pól, typy danych i inne informacje strukturalne, w formacie czytelnym dla człowieka.

## Bibliografia
* [dBase](https://en.wikipedia.org/wiki/DBase)


