{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik MDMP - format pliku Windows Minidump",
  "description":"Poznaj format pliku MDMP i interfejsy API, które mogą tworzyć i otwierać pliki MDMP.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Czym jest plik MDMP?

Plik MDMP to zrzut pamięci aplikacji w systemie Microsoft Windows, który jest tworzony, gdy aplikacja zamyka się nieprawidłowo lub ulega awarii. Zawiera informacje i zrzuty danych, których można użyć do debugowania przyczyny awarii. Pliki MDMP mają zastosowanie w aplikacjach tworzonych przez dowolną platformę, taką jak Java, C ++, .NET i inne. Oprócz MDMP,

Aplikacje, które mogą otwierać pliki MDMP, obejmują Microsoft Visual Studio Debugger.

## Format pliku MDMP

Pliki MDMP są zapisywane jako pliki binarne na dysku i można je otwierać za pomocą debugera Microsoft Visual Studio. Zawiera następujące informacje, które pomogą zidentyfikować przyczynę awarii.

* Szczegóły komunikatu Stop, jego parametry i inne dane
* Lista załadowanych sterowników
* Kontekst procesora (PRCB) dla procesora, który przestał działać
* Informacje o procesie i kontekst jądra (EPROCESS) dla procesu, który został zatrzymany
* Informacje o procesie i kontekst jądra (ETHREAD) dla zatrzymanego wątku
* Stos wywołań trybu jądra dla zatrzymanego wątku

Te informacje pomagają dowiedzieć się, co się stało, rozwiązać problem i zapobiec jego ponownemu wystąpieniu.

### Przeanalizuj minizrzut

System Windows wymaga pliku stronicowania na woluminie rozruchowym, aby utworzyć plik zrzutu pamięci. Plik stronicowania jest tworzony na woluminie rozruchowym i powinien mieć co najmniej 2 megabajty (MB). Plik zrzutu jest tworzony w przypadku awarii aplikacji. W przypadku drugiego problemu tworzony jest drugi mały plik zrzutu pamięci, podczas gdy poprzedni jest zachowywany. Nazwa pliku zrzutu jest odrębna, aby uniknąć nadpisania.

System Windows przechowuje listę wszystkich plików zrzutu pamięci w folderze %SystemRoot%\Minidump. Możesz analizować pliki MDMP, uruchamiając je w programie Visual Studio Debugger zgodnie z poniższymi krokami.

## Jak otworzyć plik MDMP w programie Visual Studio?

Aby otworzyć plik MDMP w programie Visual Studio, można wykonać następujące kroki.

* W Visual Studio z menu Plik wybierz Otwórz | Zrzut awaryjny .
* Przejdź do pliku zrzutu, który chcesz otworzyć.
* Wybierz Otwórz.

## Odniesienie

* [Jak odczytać mały plik zrzutu pamięci tworzony przez system Windows w przypadku awarii](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

