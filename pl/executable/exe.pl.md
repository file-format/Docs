{
  "date" : "2021-06-30",
  "keywords" :[ "plik exe", "format pliku exe", "co to jest plik exe", "plik", "przykład exe", "rozszerzenie pliku exe", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Plik .exe to plik Microsoft Executable, który jest uruchamiany w systemie operacyjnym Windows. Dowiedz się więcej o formacie pliku EXE.",
  "title" :"Co to jest plik wykonywalny EXE?",
  "linktitle" : "EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Czym jest plik EXE?

Słowo EXE jest skrótem od **plik wykonywalny**. Plik .exe to program, który można uruchomić w systemie operacyjnym Microsoft Windows. Twórcy aplikacji najczęściej publikują swoje programy dla systemu operacyjnego Windows w formacie wykonywalnym jako pliki exe. Jest to standardowy format pliku do uruchamiania aplikacji w systemie Windows. **Setup.exe**, **Install.exe** i **cmd.exe** to popularne i dobrze znane nazwy plików EXE.

## Format pliku EXE

Kompilatory MS-DOS zostały wprowadzone wraz z modelami pamięci mającymi ograniczenie pamięci do 64 KB. Ogólna koncepcja polega na ustawieniu różnych rejestrów segmentów w procesorze x86 (CS, DS, ES, SS), aby wskazywały różne lub te same segmenty, umożliwiając w ten sposób różne stopnie dostępu do pamięci. Niektóre konkretne modele pamięci to:

- **Tiny**: Wszystkie dostępy do pamięci są 16-bitowe (rejestry segmentowe niezmienione). Tworzy plik .COM zamiast pliku .EXE.
- **Mały**: Wszystkie dostępy do pamięci są 16-bitowe (rejestry segmentowe niezmienione).
- **Kompaktowy**: adresy danych obejmują zarówno segment, jak i przesunięcie, przeładowanie rejestrów DS lub ES przy dostępie i dopuszczanie do 1M danych. Dostęp do kodu nie zmienia rejestru CS, umożliwiając 64 KB kodu.
- **Średni**: adresy kodowe obejmują adres segmentu, ponowne ładowanie CS przy dostępie i dopuszczanie do 1 MB kodu. Dostęp do danych nie zmienia rejestrów DS i ES, pozwalając na 64K danych.
- **Duży**: zarówno kod, jak i adresy danych są parami (segment, przesunięcie), zawsze przeładowując adresy segmentów. Cały 1M bajtowy obszar pamięci jest dostępny zarówno dla kodu, jak i danych.
- **Ogromny**: taki sam jak duży model, z dodatkową arytmetyką generowaną przez kompilator, aby umożliwić dostęp do tablic większych niż 64 KB.

Programiści muszą zdecydować, który model wybrać podczas tworzenia pliku exe.

### Przenośny format pliku EXE

Przenośny format pliku wykonywalnego (PE) zawiera szereg nagłówków informacyjnych, poniżej znajduje się lista nagłówków:

- **Nagłówek DOS**: Nagłówek MS-DOS zapewnia kompatybilność wsteczną lub płynne odrzucanie nowych typów plików.
- **PE Header**: Przesunięcie 60 (0x3C) od początku nagłówka DOS jest wskaźnikiem do nagłówka pliku PE
- **Nagłówek COFF**: Nagłówek COFF zawiera pewne informacje, które są przydatne dla pliku wykonywalnego, oraz pewne informacje, które są bardziej przydatne dla pliku obiektowego.
- **Opcjonalny nagłówek PE**: Opcjonalny nagłówek PE występuje bezpośrednio po nagłówku COFF, a niektóre źródła podają nawet, że dwa nagłówki stanowią część tej samej struktury.
- **Tabela sekcji**: Bezpośrednio po opcjonalnym nagłówku PE znajdujemy tabelę sekcji. Tabela sekcji składa się z tablicy struktur IMAGE_SECTION_HEADER.
- **Możliwe do mapowania sekcje**: mogą zaoszczędzić miejsce w pamięci, mapując kod biblioteki na więcej niż jeden proces.

## Czy możesz uruchomić plik EXE na komputerze Mac?

Pliki exe nie są używane jako pliki wykonywalne w systemie Mac OS. Jeśli jednak chcesz uruchomić plik exe w systemie Mac OS, możesz użyć następujących metod.

1. **Wine** - Wine to idealne rozwiązanie dla osób, które chcą korzystać z aplikacji PC na systemach Mac. Jest to akronim oznaczający „Wine Is Not A Emulator”, czyli „Wine Is Not A Emulator”. Wine tworzy to samo środowisko katalogów, które jest używane przez firmę Microsoft, dzięki czemu można za jego pomocą uruchamiać aplikacje Windows.
2. **Maszyny wirtualne** — utwórz maszynę wirtualną z systemem Windows za pomocą pulpitu równoległego lub maszyny wirtualnej Virtual Box i uruchom aplikację na maszynie wirtualnej.
3. **Boot Camp** — instalacja i konfiguracja Windows Boot Camp w systemie Mac OS umożliwia uruchomienie systemu operacyjnego Windows na komputerze Mac.

## Bibliografia

* [.exe – autorstwa Wikipewdia](https://en.wikipedia.org/wiki/.exe)
* [Dezasemblacja x86/Pliki wykonywalne systemu Windows](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

