{
  "date" : "2021-07-08",
  "keywords" :["SYS", "rozszerzenie", "plik", "format", "system", "Sterownik", "Plik systemowy", "programy", "komputer", "aplikacja"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SYS - Format pliku systemowego",
  "description":"Poznaj format plików SYS i interfejsy API, które mogą tworzyć i otwierać pliki SYS.",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Czym jest plik SYS? ##

Pliki SYS to „pliki systemowe” używane w aplikacjach systemu operacyjnego Windows i MS-DOS. Plików tych nie można otworzyć bezpośrednio i składają się one ze sterownika i konfiguracji urządzenia. Pliki SYS są odpowiedzialne za przechowywanie plików podstawowych funkcji systemu operacyjnego. Są to krytyczne pliki sterownika urządzenia i mogą być również używane, gdy ma zostać rozwiązany jakikolwiek problem z kierowcą wyścigowym. Odpowiadają one za prawidłowe funkcjonowanie systemu komputerowego, a pliki .sys muszą być poprawne i kompletne.


## Specyfikacja techniczna ##

Pliki .sys są w rzeczywistości podzbiorem formatu [BMP](/pl/image/bmp), ponieważ zezwalają tylko na określone kombinacje. Typowy format tych plików to LOGOS.SYS, LOGOW.SYS i LOGO.SYS. Żadne inne pliki nie mają tego formatu.

Te pliki są najczęściej używane w katalogu *C* systemu Windows w czasie instalacji. Większość problemów związanych ze sterownikami urządzeń można rozwiązać, aktualizując system operacyjny Windows. Szczegóły i informacje o tych plikach można przeglądać za pomocą wbudowanych programów systemu operacyjnego Windows. Obejmują one również odniesienia do różnych modułów w systemie operacyjnym.
Niektóre przykłady plików systemowych to:

* IO.SYS (przechowują sterowniki urządzeń systemu operacyjnego dysku)
* MSDOS.SYS (zawierają jądro lub podstawowy kod systemu operacyjnego)
* CONFIG.SYS (zawierają różne opcje konfiguracji)
* KEYBOARD.SYS (zawiera informacje związane z układem klawiatury)
* COUNTRY.SYS (Te informacje zawierają informacje dotyczące kraju i strony kodowej)

## Format pliku SYS ##

Microsoft opracował pliki z rozszerzeniem .sys. Zmienne i funkcje są zawarte w plikach SYS. Są one najczęściej używane przez system operacyjny Microsoft. Pliki te znajdują się głównie w katalogu głównym dysku:

* C:\Windows\system32\drivers
* C:\Windows\WinSxS

Niektóre typowe ostrzeżenia dotyczące plików SYS są następujące:

* Nazwy tych plików nie powinny być zmieniane, ponieważ pliki te odpowiadają za podstawowe funkcje i zmienne systemu operacyjnego
* Tych plików nie należy usuwać, ponieważ ich brak może spowodować błędy
* Pliki .sys nie powinny być pobierane z Internetu, dopóki nie masz pewności co do legalności źródła
* Nie należy zadzierać z tymi plikami, ponieważ ich zmiana lub manipulowanie powoduje poważne błędy systemowe
* Jeśli te pliki zostaną uszkodzone przez wirusa lub złośliwe oprogramowanie, należy je ponownie zainstalować

## SYS Przykład ##

Poniżej znajduje się przykład prostego pliku konfiguracyjnego systemu SYS:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
