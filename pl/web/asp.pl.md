{
  "date" : "2019-10-11",
  "keywords" :["asp","plik asp", "format pliku asp", "typ pliku asp", "plik", "typ", "co to jest plik asp" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP — format pliku stron aktywnego serwera",
  "description" :"Dowiedz się, co to jest plik ASP i interfejsy API, które mogą je tworzyć i otwierać.",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik ASP?

ASP to skrót od Active Server Pages, który jest platformą programistyczną do tworzenia stron internetowych. Umożliwia wykonanie kodu komputerowego przez wewnętrzny serwer w celu obsługi żądań sieciowych. Gdy żądanie pliku ASP jest generowane przez przeglądarkę internetową, serwer odczytuje plik i wykonuje znajdujący się w nim kod/skrypt w celu wygenerowania wyniku **[HTML](/pl/web/html/)**, który jest zwracany do przeglądarka do wyświetlania.

W przeciwieństwie do stron HTML, które są statycznymi stronami obsługiwanymi przez serwer, pliki ASP generują dynamiczną zawartość w czasie wykonywania, która może obejmować żądania danych z bazy danych. Strony ASP zazwyczaj używają rozszerzenia .asp zamiast .html. Ponieważ kod/skrypt w pliku ASP jest wykonywany po stronie serwera, przeglądarka żądająca nie widzi kodu użytego do zbudowania obsługiwanej strony. Wszystkie nowoczesne przeglądarki są w stanie wyświetlać strony wygenerowane w wyniku. Zbudowane w oparciu o technologię firmy Microsoft strony zbudowane za pomocą ASP są hostowane na serwerach Microsoft Internet Information Services (IIS).

## Krótka historia formatu pliku ASP
ASP przeszedł zaledwie kilka zmian, zanim został zastąpiony przez ASP.NET, który jest nowocześniejszym i wydajniejszym sposobem tworzenia i zarządzania stronami po stronie serwera. Obsługa ASP jest domyślnie dołączana wraz z Internetowymi usługami informacyjnymi (IIS). ASP została opublikowana w trzech różnych wersjach z ulepszeniami w każdej z nich.

* ASP 1.0 został wydany w grudniu 1996 roku jako część usług IIS 3.0
* ASP 2.0 został wydany we wrześniu 1997 jako część IIS 4.0
* ASP 3.0 został wydany w listopadzie 2000 jako część IIS 5.0

## Obiekty funkcjonalne ASP

Pliki ASP używają obiektów po stronie serwera do przetwarzania żądań użytkowników i generowania stron wyjściowych, które mają być udostępniane użytkownikom. Każdy obiekt ma zestaw kolekcji, właściwości i metod przetwarzania żądań i odpowiedzi. Obiekty te obejmują:

### Żądaj obiektu

Gdy przeglądarka prosi o stronę z serwera, nazywa się to żądaniem. Obiekt Request służy do uzyskiwania informacji od odwiedzającego.

### Obiekt odpowiedzi

Obiekt ASP Response służy do wysyłania danych wyjściowych do użytkownika z serwera.

### Obiekt serwera

Obiekt serwera ASP służy do uzyskiwania dostępu do właściwości i metod na serwerze. Umożliwia połączenia z bazami danych (ADO), systemem plików oraz korzystanie z komponentów zainstalowanych na serwerze.

### Obiekt sesji

Obiekt sesji jest jak łącze między przeglądarką użytkownika żądającą strony z serwera a samym serwerem. Odbywa się to za pomocą pliku cookie tworzonego przez ASP i wysyłanego do komputera użytkownika. Obiekt Session przechowuje informacje lub zmiany ustawień sesji użytkownika. Informacje przechowywane w obiekcie Session są udostępniane na wszystkich stronach aplikacji. Typowe informacje przechowywane w zmiennych sesji to nazwa, identyfikator i preferencje. Serwer tworzy nowy obiekt Session dla każdego nowego użytkownika i niszczy obiekt Session po wygaśnięciu sesji.

### Obiekt aplikacji

Obiekt Application zawiera informacje, które będą używane przez wiele stron w aplikacji (np. informacje o połączeniu z bazą danych). Dostęp do informacji można uzyskać z dowolnej strony. Informacje można również zmienić w jednym miejscu, a zmiany zostaną automatycznie odzwierciedlone na wszystkich stronach. Obiekt Application służy do przechowywania i uzyskiwania dostępu do zmiennych z dowolnej strony, podobnie jak obiekt Session.

### Obiekt ASPError

Obiekt ASPError został zaimplementowany w ASP 3.0 i jest dostępny w usługach IIS5 i nowszych. Obiekt ASPError służy do wyświetlania szczegółowych informacji o wszelkich błędach występujących w skryptach na stronie ASP.

**Uwaga:** Obiekt ASPError jest tworzony podczas wywoływania metody Server.GetLastError, dlatego dostęp do informacji o błędzie można uzyskać tylko za pomocą metody Server.GetLastError.

## Bibliografia

* [ASP – przez W3C](https://www.w3schools.com/asp/default.asp)
* [Tworzenie prostych stron ASP](https://docs.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))

