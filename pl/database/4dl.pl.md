{
  "date" : "2023-06-14",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Dowiedz się o formacie pliku 4DL i interfejsach API, które umożliwiają tworzenie i otwieranie plików 4DL.",
  "title" :"4DL - plik dziennika bazy danych czwartego wymiaru",
  "linktitle" : "4DL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-06-14"
}

## Co to jest plik 4DL?

Plik dziennika 4DL służy do rejestrowania modyfikacji wprowadzonych w pliku bazy danych 4D (.4DD). Plik ten jest przechowywany wraz z plikiem bazy danych i ma podobną nazwę. Jego celem jest dokładne śledzenie i utrzymywanie kompleksowego rejestru aktualizacji wprowadzonych w bazie danych. [Plik 4DD](/pl/database/4dd/), w porównaniu do pliku 4DL, jest kojarzony głównie z 4th Dimensions firmy 4D Inc.

## Format pliku 4DL — więcej informacji

Zazwyczaj wiele plików 4DL jest przechowywanych razem z plikiem 4DD. Zatem pierwsza wersja pliku dziennika może mieć nazwę 0001.4dl, ale wersje boczne plików dziennika zostaną zapisane jako 0002.4dl, 0003.4dl i tak dalej. Teraz, jeśli sam plik dziennika zostanie poddany 3 kolejnym zapisom, zostanie oznaczony jako "db1[0005-0003].4dl".

## Bibliografia

* [4DD - Wikipedia](https://en.m.wikipedia.org/wiki/4th_Dimension_(software))
