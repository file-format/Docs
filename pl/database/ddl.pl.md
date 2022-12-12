{
  "date" : "2020-11-11",
  "keywords" :["DDL", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Pliki bazy danych" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku DDL i interfejsy API, które mogą tworzyć i otwierać pliki DDL.",
  "title" :"Format pliku DDL — plik języka definicji danych",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Czym jest plik DDL?

Plik z rozszerzeniem .ddl to plik języka definicji danych, który służy do definiowania schematu bazy danych. Zawiera instrukcje/polecenia do pracy ze strukturami baz danych, takimi jak tabele, kolumny, rekordy i inne pola. Polecenia w pliku DDL są napisane w [SQL](/pl/database/sql/) i mogą wykonywać operacje, takie jak tworzenie tabeli w bazie danych, upuszczanie i aktualizowanie. Schemat bazy danych jest własnością jego utworzonego i można na nim wykonywać wszystkie operacje CRUD. Popularne aplikacje, które mogą tworzyć i otwierać pliki DDL to Windows Text Editor, Jetbrains Intellij Idea i EclipseLink.

## polecenia DDL

Pojedynczy plik DDL może zawierać kilka poleceń, które dzięki poprawnej składni wykonają się po kolei i dokonują zmian w schemacie, takich jak tworzenie zestawów znaków i tabel, usuwanie tabel, zmiana nazwy i modyfikowanie tabel. Następujące polecenia DDL są często używane podczas pracy ze schematem bazy danych.

`CREATE` - Służy do tworzenia bazy danych lub jej obiektów (takich jak tabela, indeks, funkcja, widoki, procedura przechowywania i wyzwalacze).

`DROP` – Służy do usuwania obiektów z bazy danych.

`ALTER` - Służy do zmiany struktury bazy danych.

`TRUNCATE` – Służy do usuwania wszystkich rekordów z tabeli, w tym usuwane są wszystkie spacje przydzielone do rekordów.

`COMMENT` – Dodaje komentarze do słownika danych.

`RENAME` – Zmienia nazwę istniejącego obiektu w bazie danych.

## Przykład DDL

Poniższy przykład przedstawia instrukcję DDL dla polecenia CREATE, które tworzy tabelę i definiuje jej pola.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Bibliografia ##

* [DDL z Wikipedii](https://en.wikipedia.org/wiki/Data_definition_language)

