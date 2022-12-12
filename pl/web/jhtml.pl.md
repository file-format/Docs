{
  "date" : "2019-10-11",
  "keywords" :[ "jhtml","plik jhtml", "format pliku jhtml", "typ pliku jhtml", "plik", "typ", "co to jest plik jhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JHTML - Plik Java HTML",
  "description":"Poznaj format pliku JHTML i interfejsy API, które mogą tworzyć i otwierać pliki JHTML.",
  "linktitle" : "JHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-09"
}

## Co to jest plik JHTML?

Plik z rozszerzeniem .jhtml to plik [HTML](/pl/web/html/) z kodem [Java](/pl/programming/java/), który jest wykonywany na serwerze, gdy klient żąda tej strony w przeglądarce. Serwer przetwarza żądania, wykonuje funkcje Java zawarte w funkcji i zwraca stronę do przeglądarki klienta. Obiekty Java osadzone na stronach JHTML są uruchamiane na serwerze w celu obsługi żądań stron tego typu. Pliki JHTML mogą również uzyskiwać dostęp do informacji z bazy danych za pomocą połączenia JDBC (Java [Database](/pl/database/) Connectivity). Pliki JHTML można otwierać w dowolnym edytorze tekstu i przeglądać w przeglądarkach internetowych, takich jak Google Chrome, Firefox i Safari.

## Format pliku JHTML

JHTML jest zastrzeżoną technologią firmy ATG i można ją tworzyć za pomocą edytora dokumentów Dynamo ATG (Art Technology Group). Pliki JHTML są zapisywane w formacie zwykłego pliku tekstowego przy użyciu standardowego kodu HTML i Java. Zawierają one standardowe tagi HTML oprócz zastrzeżonych tagów, które odwołują się do obiektów Java. Gdy użytkownik zażąda takiej strony, serwer HTTP przekazuje żądanie do serwera aplikacji Java. Strona JHTML jest najpierw konwertowana do pliku .java i kompilowana w celu wygenerowania pliku [.class](/pl/programming/class/), który jest wykonywany jako serwlet. Generuje to strumień standardowych danych HTTP i HTML, które są zwracane z powrotem do żądającej przeglądarki w celu wyświetlenia użytkownikowi. Jest to pomocne przy uruchamianiu zapytań związanych z bazą danych na serwerze i zwracaniu sfinalizowanego skumulowanego wyniku do przeglądarki klienta.

## Bibliografia

* [Globalna struktura dokumentu HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

