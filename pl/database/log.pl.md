{
  "date" : "2021-06-14",
  "keywords" :["LOG", "rozszerzenie", "plik dziennika", "format pliku dziennika", "Typ pliku bazy danych", "Format pliku bazy danych", "co to jest plik dziennika"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Dowiedz się o formacie pliku LOG i interfejsach API, które mogą tworzyć i otwierać pliki LOG.",
  "title" :"LOG - Format pliku dziennika",
  "linktitle" : "LOG",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Czym jest plik LOG?
Plik z rozszerzeniem .log zawiera listę zwykłego tekstu ze znacznikiem czasu. Zwykle niektóre szczegóły aktywności są rejestrowane przez oprogramowanie lub systemy operacyjne, aby pomóc programistom lub użytkownikom śledzić, co działo się w określonym czasie. Użytkownicy mogą bardzo łatwo edytować te pliki za pomocą dowolnego edytora tekstu. Zwykle raporty o błędach lub działania związane z logowaniem są rejestrowane przez systemy operacyjne, ale inne oprogramowanie lub serwery internetowe również generują pliki dziennika w celu śledzenia odwiedzających i monitorowania wykorzystania przepustowości.

## Format pliku dziennika
Format pliku LOG rejestruje typowe zdarzenia występujące w systemie operacyjnym, komunikaty między różnymi użytkownikami oprogramowania komunikacyjnego lub inne uruchomione oprogramowanie. Po prostu możemy powiedzieć, że pewne wiadomości w określonych znacznikach czasu są rejestrowane w pliku LOG. Niektóre powszechnie używane terminy dotyczące rejestrowania to:
### Dzienniki zdarzeń
Rejestruje zdarzenia występujące podczas wykonywania systemu w celu śledzenia i zrozumienia działania systemu oraz diagnozowania problemów. Są one ważne, aby identyfikować działania złożonych systemów, zwykle w przypadku aplikacji z bardzo małą interakcją użytkownika.
### Dzienniki transakcji
Prawie wszystkie systemy baz danych przechowują dziennik transakcji, który zwykle nie jest pomyślany jako ścieżka audytu do późniejszej analizy i nie jest czytelny dla człowieka. Te dzienniki przechowują tylko zapis zmian w istniejących danych, aby umożliwić przywrócenie bazy danych po awariach lub innych błędach danych i zachować spójność danych. Dlatego systemy baz danych mają zwykle zarówno ogólne dzienniki zdarzeń, jak i dzienniki transakcyjne.
### Dzienniki komunikatów
Komunikacja tekstowa zapisana przez Internet Relay Chat (IRC), programy do obsługi wiadomości błyskawicznych (IM), klienty wymiany plików peer-to-peer z funkcjami czatu oraz gry wieloosobowe (zwłaszcza gry MMORPG) są nazywane dziennikami wiadomości. Te dzienniki są zazwyczaj zapisywane w zwykłych plikach tekstowych, ale klienci IM i VoIP (np. Skype) mogą zapisywać je w plikach HTML, aby ułatwić odczyt lub umożliwić szyfrowanie.
### Dzienniki serwera
Dziennik serwera jest w rzeczywistości plikiem dziennika zawierającym listę działań wykonanych i utworzonych lub utrzymywanych automatycznie przez sam serwer. Zwykle pliki te nie są dostępne dla zwykłych użytkowników Internetu, a jedynie dla webmastera lub innej osoby administracyjnej serwisu internetowego.



## Bibliografia ##

* [Plik dziennika – Wikipedia](https://en.wikipedia.org/wiki/Log_file)

