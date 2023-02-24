{
  "date" : "2021-04-16",
  "keywords" :[ "XML", "P6XML", "Plik", "Rozszerzenie", "Format pliku", "Projekt", "Zarządzanie", "Primavera", "P6"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P6XML - Projekt Primavera P6",
  "description":"Poznaj format plików P6XML i interfejsy API, które mogą tworzyć i otwierać pliki P6XML.",
  "linktitle" : "P6XML",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## Co to jest plik P6XML? ##

Rozszerzenie pliku P6XML ma doskonałą czytelność, możliwość dostosowania i szerokie zastosowanie, co czyni go idealnym formatem. Primavera P6 Professional posiada funkcję eksportu i importu zarówno plików [XER](/pl/project-management/xer/), jak i plików XML. XML oznacza **Extensible Markup Language**. Ten ogólny format umożliwia użytkownikom udostępnianie informacji o projekcie między bazami danych Primavera P6. Dane projektu można łatwo zapisać w pliku tekstowym za pośrednictwem pliku XML; Ułatwia to wielu programom wymianę danych. Takie dane mogą być łatwo udostępniane i zarządzane przez użytkownika Primavera P6.

## Zalety formatu pliku P6XML ##

* Użytkownicy Primavery mogą łatwo określić, które linie bazowe mają być eksportowane i importowane za pomocą pliku XML
* Eksport XML może zawierać szczegółowe plany działania wszystkich projektów
* Każdy użytkownik korzystający z Primavera 6, który nie może edytować, dodawać ani usuwać pewnych elementów danych globalnych, takich jak kody aktywności, kalendarze i zasoby, nie będzie mógł ich importować
* Oprócz ustawień profilu ogólnego i profilu bezpieczeństwa projektu używanych przez Primavera, elementy danych, które wpłyną na dane w bazie danych lub je zmienią, nie zostaną zaimportowane

## Eksportowanie pliku XML z Primavera P6 ##

Do eksportowania projektów P6 Professional i danych projektu do pliku P6XML użyj Oracle Primavera Cloud. Możesz pobrać plik podczas jego tworzenia z aplikacji komputerowej P6 Professional i zaimportować go do Primavera Cloud. Zanim nieprzerwanie obsłużysz proces eksportu, powinieneś uregulować, czy jesteś połączony z bazą danych P6 Professional lub P6 EPPM. Niektóre funkcje procesu eksportu mogą się różnić w zależności od bazy danych. Mając ustawienia P6 Specialized z bazą danych P6 Proficient, proces eksportu odbywa się lokalnie w twoim systemie. Mając bazę danych P6 Professional, możesz łatwo eksportować i otwierać plik XML P6 z ustawienia w swoim systemie.

Oto kilka kroków opisujących proces eksportu:

* Otwarte pragnienia projektu Primavera P6
* Następnie wybierz Eksportuj na karcie Plik
* Wybierz „Primavera P6 – (XML)”. Następnie kliknij Dalej
* Kliknij dwukrotnie projekt, który chcesz wyeksportować
* Wybierz obcięcia dla ścieżki, w której chcesz umieścić wyeksportowany plik i wybierz „Zakończ”.
* Wybierz opcję, w jaki sposób chcesz zapisać plik
* Jeśli w pliku eksportu nie są potrzebne układy na poziomie projektu, konieczne jest usunięcie zaznaczenia opcji „Eksportuj wszystkie układy na poziomie projektu”.
* Wybierz zakończenie, a następnie otrzymasz potwierdzenie eksportu XML

### Ważne wskazówki ###

* Za każdym razem, gdy łączysz się z bazą danych P6 EPPM, administrator musi podać adres URL źródła treści w polu adresu URL P6 na stronie Ogólne ustawień aplikacji w P6
* Wygodnie jest eksportować wiele projektów do jednego pliku XML
* Eksportowane są dane globalne, które są przypisane do projektu
* Wygodnie jest eksportować pliki XML bez dostępu do wszystkich zasobów



## Problemy z otwarciem pliku P6XML? ##

Niektóre typowe problemy, które mogą się pojawić i powodować nieprawidłowe działanie formatu P6XML, są następujące:

* Brak oprogramowania pomocniczego
* Uszkodzony plik
* Zainfekowany plik z powodu wirusa
* Opis P6XML przypadkowo usunięty z rejestru systemu Windows
* Brak prawa dostępu w systemie do otwierania plików
* Przestarzały dysk w twoim systemie
* Zmieniono nazwę rozszerzenia pliku


## Bibliografia ##

* [Oracle — P6 XML](https://docs.oracle.com/cd/E80480_01/English/admin/p6_import_guide/index.html)
