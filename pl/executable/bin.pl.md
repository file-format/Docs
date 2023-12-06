{
"data":"2023-07-20",
   "keywords":[
"KOSZ",
"Plik BIN",
"plik",
"rozszerzenie pliku BIN",
"rozszerzenie",
"plik"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"Format pliku BIN - plik wykonywalny Unix",
   "description":"Dowiedz się o formacie BIN i interfejsach API, które umożliwiają tworzenie i otwieranie plików BIN.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
         "parent":"executable"
}
},
"lastmod":"2023-07-20"
}

## Czym jest plik BIN?

Plik BIN to plik wykonywalny w systemach operacyjnych opartych na systemie Unix, takich jak Linux lub FreeBSD. Zawiera skompilowany program złożony z kodu binarnego pochodzącego z kodu źródłowego, dzięki czemu jest kompatybilny z podstawową architekturą systemu. Pliki wykonywalne BIN systemu Unix można porównać do plików .EXE systemu Windows i plików .APP systemu macOS pod względem ich roli jako formatów wykonywalnych.

W dziedzinie tworzenia oprogramowania dla systemów Unix pliki BIN są powszechnie wykorzystywane przez programistów do pakowania i dystrybucji programów. Oferują wygodny sposób dostarczania oprogramowania użytkownikom, umożliwiając łatwą instalację i wykonanie. Oprócz plików BIN istnieją inne typy plików wykonywalnych Uniksa, w tym [.ELF](/pl/executable/elf/), .X86, [.RUN](/pl/executable/run/) i .X86_64, każdy dostosowany do określonego sprzętu lub wymagania systemowe.

Jeśli chodzi o wewnętrzną strukturę pliku BIN, składa się on z zakodowanych danych, które system operacyjny Unix wykorzystuje do identyfikacji, odczytu i wykonania dołączonego programu. System opiera się na określonych sygnaturach lub nagłówkach plików w celu rozpoznania pliku BIN jako pliku wykonywalnego, a następnie interpretacji i wykonania zawartych w nim instrukcji binarnych.

Do plików BIN często dołączony jest plik **INSTALL.TXT**, który zawiera szczegółowe instrukcje dotyczące prawidłowej instalacji i konfiguracji programu. Niniejsza dokumentacja gwarantuje, że użytkownicy będą mogli pomyślnie przejść proces instalacji i rozpocząć korzystanie z oprogramowania bez komplikacji.

## Jak otworzyć plik BIN?

Pliki BIN nie są przeznaczone do bezpośredniego otwierania i przeglądania. Można jednak uruchamiać programy lub wyodrębniać zawarte w nich dane. Aby uzyskać dostęp do zawartości pliku BIN, wykonaj poniższe kroki w wierszu poleceń, zakładając, że nazwa pliku BIN to "sample.bin":

1. **Zapewnij uprawnienia do wykonywania:**

Przed uruchomieniem pliku BIN upewnij się, że ma on niezbędne uprawnienia do uruchomienia jako plik wykonywalny. Użyj polecenia:

```
$ chmod +x sample.bin
```

To polecenie przyznaje uprawnienia do pliku wykonywalnego.

2. **Wykonaj plik BIN:**

Po ustawieniu uprawnień do pliku wykonywalnego możesz uruchomić plik BIN wpisując następującą komendę:

```
$ ./sample.bin
```

**Ostrzeżenie**

_Zachowaj ostrożność podczas postępowania z pobranymi lub przesłanymi pocztą elektroniczną plikami BIN, ponieważ mogą one potencjalnie zostać wykorzystane przez cyberprzestępców do dystrybucji złośliwego oprogramowania. Uruchamiaj pliki BIN wyłącznie z zaufanych źródeł, aby zmniejszyć ryzyko złośliwych ataków wykonywalnych._

## Inne pliki BIN

Oto inne typy plików, które korzystają z rozszerzenia **.bin**.

- [BIN – plik zakodowany w systemie MacBinary](/pl/kompresja/bin/)
- [BIN – Binarny plik obrazu dysku](/pl/disc-and-media/bin/)
- [BIN – plik zasad IT BlackBerry](/pl/settings/bin/)
- [BIN - ROM gry Sega Genesis](/pl/game/bin/)
- [BIN - Obraz BIOS-u PSX PlayStation](/pl/game/bin-pcsx/)

## Bibliografia

* [Jak uruchamiać pliki binarne w systemie Linux](https://linuxhint.com/execute-binary-files-in-linux/)


