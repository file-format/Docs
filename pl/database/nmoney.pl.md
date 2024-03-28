{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Dowiedz się o formacie pliku NMONEY i interfejsach API, które umożliwiają tworzenie i otwieranie plików NMONEY.",
  "title" :"Plik NMONEY - Format pliku konta Denaro",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## Czym jest plik NMONEY?

Plik NMONEY to plik bazy danych do przechowywania danych finansowych, który zawiera historię transakcji finansowych. Został opracowany przez Nickvision i był używany w oprogramowaniu Nickvision Denaro, które jest osobistą aplikacją finansową. Dane przechowywane w pliku NOMONEY obejmują informacje o transakcjach kredytowych i debetowych na koncie.

Pliki NOMONEY można otworzyć za pomocą aplikacji [Github](https://github.com/NickvisionApps/Denaro).

## O oprogramowaniu Denaro

Denaro zostało pierwotnie opracowane przez [Nickvision](https://nickvision.org/) jako produkt, który później został przekonwertowany na aplikację typu open source hostowaną na [Github](https://github.com/NickvisionApps/Denaro) . Od tego czasu aplikacja była modyfikowana i aktualizowana wyłącznie na Githubie. Aplikacja została opracowana w języku C# w interfejsie użytkownika systemu Windows z pakietem Windows App SDK (obecnie WinUI 3).

### Funkcje oferowane przez Denaro

* Zarządzaj wieloma kontami jednocześnie za pomocą najpopularniejszego i znanego interfejsu zakładek
* Filtruj transakcje według typu, grupy lub daty
* Powtarzaj transakcje, takie jak rachunki, które występują co miesiąc
* Przelej pieniądze z jednego konta na drugie
* Eksportuj dane z konta jako plik CSV i importuj plik CSV, OFX lub QIF, aby dodać transakcje do konta

## Format pliku Denaro — więcej informacji

Pliki Denaro zapisywane są na płycie w formacie binarnym. Dane finansowe przechowywane są w postaci pliku bazy danych w formacie pliku **.SQLITE3**. SQLITE to lekki plik bazy danych SQL utworzony za pomocą oprogramowania SQLite. Zapewnia samodzielny silnik bazy danych, który jest w stanie zapewnić w pełni funkcjonalną i wysoce niezawodną bazę danych. Pliki bazy danych SQLite mogą być używane do udostępniania bogatej zawartości pomiędzy systemami poprzez prostą wymianę tych plików przez sieć. Istnieją powiązania SQLite dla języków programowania, takich jak C, [C#](/pl/programming/cs/), [C++](/pl/programming/cpp/), [Java](/pl/programming/java/), [PHP](/pl/programming/php/) i wiele innych.

## Bibliografia

* [Nickvision](https://nickvision.org/)
* [NICkVision – Github](https://github.com/NickvisionApps/Denaro)

