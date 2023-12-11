{
"data": "27.09.2023",
  "keywords": [
"cfg",
"plik cfg",
"plik konfiguracyjny cfg mugen",
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
"title": "Format pliku CFG - plik konfiguracyjny MUGEN",
  "description":"Dowiedz się więcej o formacie pliku konfiguracyjnego CFG MUGEN i interfejsach API, które umożliwiają tworzenie i otwieranie plików CFG.",
  "linktitle": "CFG M.U.G.E.N",
  "menu": {
    "docs": {
      "identifier": "game-cfg-mugen",
      "parent": "game"
}
},
"lastmod": "27.09.2023"
}

## Czym jest plik CFG?

Plik CFG w kontekście MUGEN odnosi się do "pliku konfiguracyjnego MUGEN". **MUGEN** to konfigurowalny silnik bijatyk 2D opracowany przez Elecbyte. Użytkownicy mogą tworzyć własne postacie, etapy, a nawet modyfikować zachowanie i zasady gry, edytując różne pliki konfiguracyjne, w tym pliki CFG.

Oto podstawowy przegląd tego, co możesz znaleźć w pliku MUGEN `.cfg`:

1. **Konfiguracja systemu**: Pliki CFG często zawierają ustawienia związane z ogólnym zachowaniem silnika gry. Obejmuje to takie kwestie, jak rozdzielczość ekranu, ustawienia dźwięku i konfiguracja wejść (mapowanie klawiatury, joysticka lub kontrolera).
    








2. **Domyślne ustawienia postaci i etapu**: Możesz zdefiniować domyślne ustawienia postaci i etapów. Na przykład możesz określić, które postacie i etapy będą ładowane po rozpoczęciu gry.
    








3. **Opcje rozgrywki**: Pliki MUGEN `.cfg` mogą również kontrolować różne opcje rozgrywki, takie jak limity czasu rundy, skalowanie obrażeń i inne.
    








4. **Debugowanie i rozwój**: Zaawansowani użytkownicy mogą używać plików `.cfg` do celów debugowania i programowania. Te ustawienia mogą kontrolować sposób wyświetlania informacji o debugowaniu na ekranie lub definiować inne zachowania związane z programowaniem.
    








5. **Konfiguracja pakietu zrzutów ekranu**: Pakiety zrzutów ekranu to motywy wizualne, które zmieniają wygląd i styl gry. Pliki `.cfg` mogą określać, który pakiet ekranu jest używany i konfigurować jego różne elementy.
    








6. **Zachowanie AI**: MUGEN pozwala zdefiniować, jak postacie sterowane komputerowo (AI) zachowują się w bitwach. Pliki `.cfg` mogą zawierać ustawienia związane z poziomem trudności i zachowaniem AI.

## Plik konfiguracyjny MUGEN

Plik MUGEN CFG (konfiguracyjny) jest kluczowym elementem dla twórców w świecie niestandardowych gier walki. Umożliwia im kształtowanie podstawowych zasad gry. Obejmuje to takie czynniki, jak czas trwania każdej rundy, poziom wyzwania stawiany przez sterowanych komputerowo przeciwników, tempo gry, stopień, w jakim kombinacje wpływają na obrażenia i wiele innych.

Ponadto plik CFG pozwala twórcom określić ustawienia wyświetlania gry, takie jak rozdzielczość ekranu i zdecydować, czy MUGEN powinien odtwarzać efekty dźwiękowe i muzykę podczas rozgrywki. Osobom dobrze zorientowanym w zawiłościach MUGENa ten plik oferuje możliwość dostosowania szeregu innych ustawień związanych z grą, aby zapewnić wyjątkowe wrażenia z gry.

Domyślnie główny plik CFG MUGEN, znany jako `mugen.cfg`, znajduje się w folderze danych programu. Chociaż możliwa jest bezpośrednia edycja ustawień gry w tym pliku, ogólnie zaleca się najpierw utworzenie kopii zapasowej. To zabezpieczenie gwarantuje, że w razie potrzeby możesz bez wysiłku przywrócić oryginalne ustawienia MUGEN, zapobiegając niezamierzonym zmianom zakłócającym wrażenia z gry.

## MUGEN – silnik gry

MUGEN to wszechstronny i wysoce konfigurowalny silnik bijatyk 2D opracowany przez Elecbyte. Nazwa "MUGEN" oznacza "Mugen Ultimate Game Engine". Pierwotnie została wydana w 1999 roku i od tego czasu zyskała oddaną społeczność użytkowników i twórców, którzy wykorzystują silnik do projektowania i rozwijania własnych bijatyk 2D.

Oto kilka kluczowych funkcji i aspektów MUGEN:

1. **Postacie z możliwością dostosowania:** MUGEN pozwala użytkownikom tworzyć i importować do gry własne postacie (znane jako "wojownicy" lub "duszki"). Twórcy mogą zaprojektować dla tych postaci unikalne zestawy ruchów, animacje i ataki specjalne, dzięki czemu możliwe jest włączenie praktycznie dowolnej postaci z różnych serii lub oryginalnych dzieł.
    








2. **Etapy:** Oprócz postaci użytkownicy mogą także tworzyć i dostosowywać etapy, na których toczą się bitwy. Etapy te mogą posiadać elementy interaktywne i unikalne tła.
      









3. **Pakiety ekranów:** Pakiety ekranów to motywy wizualne, które zmieniają ogólny wygląd gry, w tym menu, ekrany wyboru postaci i paski życia. Użytkownicy mogą tworzyć i udostępniać własne pakiety ekranów, aby nadać swoim grom niepowtarzalny wygląd i styl.
    








4. **Dźwięk i muzyka:** Twórcy mogą dodawać do swoich gier efekty dźwiękowe i muzykę w tle, poprawiając ogólne wrażenia z gry.
    








5. **Skrypty:** Zaawansowani użytkownicy mogą używać wbudowanego języka skryptowego do tworzenia złożonych zachowań postaci, unikalnej mechaniki gry i efektów specjalnych.

## Jak otworzyć plik CFG?

Pliki MUGEN CFG to zwykłe dokumenty tekstowe, dzięki czemu są dostępne w różnych edytorach tekstu. W systemie Windows można używać programu Microsoft Notatnik lub WordPad, natomiast użytkownicy systemu macOS mogą w tym celu skorzystać z programu Apple TextEdit. Te edytory umożliwiają użytkownikom łatwe przeglądanie i modyfikowanie ustawień konfiguracyjnych w plikach CFG.

Programy otwierające pliki CFG lub odwołujące się do nich

- Elektrobajt MUGEN
- Notatnik
-Edycja tekstu

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
* [Mugen (silnik gry)](https://en.wikipedia.org/wiki/Mugen_(game_engine))

