{
  "date" : "2022-02-22",
  "keywords" :["ETL", "rozszerzenie", "plik", "format", "system", "Sterownik", "Sterownik urządzenia Windows", "programy", "komputer", "aplikacja"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Pliki ETL - plik dziennika śledzenia zdarzeń firmy Microsoft",
  "description":"Poznaj format pliku ETL i interfejsy API, które mogą tworzyć i otwierać pliki ETL.",
  "linktitle" : "ETL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-02-22"
}

## Czym jest plik ETL?

Pliki ETL to pliki dziennika zawierające dzienniki zdarzeń generowane przez jądro systemu operacyjnego firmy Microsoft. Te pliki dziennika zawierają błędy na poziomie aplikacji i systemu, ostrzeżenia i inne dane o zdarzeniach. Pliki ETL są pomocne w analizowaniu i rozwiązywaniu problemów na poziomie systemu. Typowe problemy rejestrowane w plikach ETL obejmują problemy generowane przez dostęp do dysku i błędy strony. Microsoft udostępnia dwie aplikacje, Tracerpt i Event Viewer do odczytu i przeglądania zawartości plików ETL. Pliki ETL można konwertować do innych formatów plików, takich jak [TXT](/pl/processing/txt/) i [CSV](/pl/spreadsheet/csv/) za pomocą Tracerpt.

## Format pliku ETL

Pliki ETL są zapisywane na dysku w skompresowanym formacie binarnym, aby zmniejszyć miejsce na dysku.

## Otwórz pliki ETL za pomocą narzędzia Windows Performance Analyzer

Dane plików ETL można odczytywać i wizualizować w formacie tabelarycznym i graficznym za pomocą aplikacji Microsoft Windows Performance Analyzer (WPA). Przewodnik [Otwieranie i analizowanie plików ETL](https://learn.microsoft.com/en-us/windows-hardware/test/wpt/opening-and-analyzing-etl-files-in-wpa) zawiera informacje na temat pracy z plikami ETL.

## Bibliografia

* [Analizator wydajności systemu Windows](https://learn.microsoft.com/en-us/windows-hardware/test/wpt/getting-started--windows-performance-analyzer--wpa-)
* [Przewodnik szybkiego startu WPA](https://learn.microsoft.com/en-us/windows-hardware/test/wpt/wpa-quick-start-guide)

