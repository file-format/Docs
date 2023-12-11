{
"data": "27.09.2023",
  "keywords": [
"cfg",
"plik cfg",
"plik konfiguracyjny cfg mame",
"co to jest plik cfg",
"jak otworzyć plik cfg",
"plik",
"rozszerzenie pliku cfg",
"rozszerzenie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format pliku CFG - plik konfiguracyjny MAME",
  "description":"Dowiedz się o formacie pliku konfiguracyjnego CFG MAME i interfejsach API, które umożliwiają tworzenie i otwieranie plików CFG.",
  "linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame",
      "parent": "settings"
}
},
"lastmod": "27.09.2023"
}

## Czym jest plik CFG?

Plik CFG to plik konfiguracyjny klawiatury XML używany przez emulatory gier wideo MAME. Jest to kluczowy element pozwalający dostosować sterowanie klawiaturą i klawisze skrótu do preferencji gracza. Pliki te przechowują mapowania i ustawienia określające sposób interakcji klawiatury z emulatorem podczas grania w grę. Edytując ten plik, użytkownicy mogą dostosować swoje wrażenia z gry, przypisując określone klawisze klawiatury do działań w grze, takich jak wkładanie monety, uruchamianie, poruszanie się i różne inne funkcje.

## Plik konfiguracyjny MAME

MAME, czyli **Multiple Arcade Machine Emulator**, to aplikacja umożliwiająca emulację i granie w gry zręcznościowe na komputerze. MAME korzysta z plików konfiguracyjnych, aby dostosować swoje zachowanie i ustawienia. Te pliki konfiguracyjne zazwyczaj znajdują się w folderze `cfg` w katalogu MAME.

Oto główne pliki konfiguracyjne, które możesz napotkać podczas instalowania i konfigurowania MAME:

1. **mame.ini:** To jest główny plik konfiguracyjny MAME. Zawiera ustawienia globalne, które mają zastosowanie do wszystkich gier. Możesz znaleźć ten plik w katalogu głównym instalacji MAME.

1. **default.cfg:** Ten plik przechowuje domyślne ustawienia dla wszystkich gier, które nie mają własnych plików konfiguracyjnych. Jest używany jako rezerwowy dla ustawień specyficznych dla gry.

1. **game-specific.cfg:** Pliki te służą do przechowywania ustawień poszczególnych gier. Ich nazwy zwykle pochodzą od pliku ROM gry, której odpowiadają. Na przykład, jeśli masz grę o nazwie "pacman.zip", jej plikiem konfiguracyjnym będzie "pacman.cfg".

Oto kilka typowych ustawień, które można znaleźć w pliku konfiguracyjnym MAME.

1. **rompath:** Określa katalog, w którym znajdują się ROM-y z grami zręcznościowymi.

1. **katalog_cfg:** Określa katalog, w którym przechowywane są pliki konfiguracyjne specyficzne dla gry.

1. **katalog_nvram:** Określa katalog, w którym przechowywane są pliki nieulotnej pamięci RAM (NVRAM). NVRAM przechowuje najlepsze wyniki i inne dane specyficzne dla gry.

1. **katalog_grafiki:** Określa katalog, w którym przechowywane są pliki graficzne (takie jak ramki, markizy i ulotki).

1. **samplepath:** Określa katalog, w którym znajdują się przykładowe pliki dźwiękowe.

1. **cheatpath:** Określa katalog, w którym znajdują się pliki z cheatami.

Możesz także skonfigurować różne inne ustawienia, takie jak opcje wideo i audio, elementy sterujące i urządzenia wejściowe. Aby zmodyfikować te ustawienia, możesz otworzyć plik konfiguracyjny w edytorze tekstu i wprowadzić niezbędne zmiany.

## MAMA

MAME, co oznacza **"Multiple Arcade Machine Emulator",** to aplikacja przeznaczona do emulacji i replikacji sprzętu starych automatów do gier i konsol do gier. Pozwala użytkownikom grać w ogromną bibliotekę klasycznych gier zręcznościowych na nowoczesnych komputerach i innych kompatybilnych urządzeniach. MAME to projekt typu open source, który stał się popularnym emulatorem pozwalającym zachować i cieszyć się bogatą historią gier arkadowych.

1. **Emulacja:** głównym celem MAME jest dokładna emulacja sprzętu automatów do gier, w tym ich jednostek centralnych (CPU), układów dźwiękowych, układów graficznych i urządzeń wejściowych. Ten poziom dokładności gwarantuje, że gry zachowują się jak najbliżej oryginalnych gier arkadowych.

1. **Kompatybilność:** MAME obsługuje szeroką gamę ROM-ów z grami arkadowymi, co czyni go jednym z najbardziej wszechstronnych dostępnych emulatorów arkadowych. Może uruchamiać gry z różnych platform arkadowych, w tym klasyczne gry z lat 70., 80., 90., a nawet niektóre nowsze tytuły arkadowe.

1. **Ochrona:** Jedną z głównych misji MAME jest zachowanie historii gier arkadowych. Dzięki dokładnej emulacji sprzętu do gier arcade, MAME pomaga zapobiegać utracie klasycznych gier i zapewnia, że przyszłe pokolenia będą mogły grać w nie zgodnie z pierwotnym zamierzeniem.

1. **Fronty:** Wielu użytkowników korzysta z aplikacji front-end, które zapewniają interfejs graficzny do zarządzania grami i ich uruchamiania poprzez MAME. Te interfejsy ułatwiają nawigację po obszernej bibliotece gier MAME.

## Jak otworzyć plik CFG?

Programy otwierające pliki CFG lub odwołujące się do nich

- MAME (bezpłatny) (Windows)
- ExtraMAME (wersja próbna)
-MacMAME (MAC)

## Inne pliki CFG

Oto inne typy plików, które mają rozszerzenie **.cfg**.

**Ustawienia**
- [CFG - plik konfiguracyjny Celestii](/pl/settings/cfg-celestia/)
- [CFG - plik połączenia serwera Citrix](/pl/settings/cfg-citrix/)
- [CFG - plik konfiguracyjny MAME](/pl/settings/cfg-mame/)
- [CFG – plik konfiguracyjny LightWave](/pl/settings/cfg-lightwave/)

**Gra**
- [CFG - plik języka znaczników Wesnoth](/pl/game/cfg-wesnoth/)
- [CFG - plik konfiguracyjny MUGEN](/pl/game/cfg-mugen/)
- [CFG - plik konfiguracyjny silnika źródłowego](/pl/game/cfg-sourceengine/)

**System i różne**
- [CFG - plik CFG](/pl/system/cfg/)
- [CFG - plik konfiguracyjny modelu Cal3D](/pl/misc/cfg-cal3d/)

## Bibliografia
* [MAME](https://en.wikipedia.org/wiki/MAME)

