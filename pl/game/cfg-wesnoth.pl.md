{
"data": "27.09.2023",
  "keywords": [
"cfg",
"plik cfg",
"cfg plik języka znaczników wesnoth",
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
"title": "Format pliku CFG - plik języka znaczników Wesnoth",
  "description":"Dowiedz się o formacie pliku CFG Wesnoth Markup Language File i interfejsach API, które umożliwiają tworzenie i otwieranie plików CFG.",
"linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
      "parent": "game"
}
},
"lastmod": "27.09.2023"
}

## Czym jest plik CFG?

Plik CFG jest również znany jako **"Wesnoth Markup Language" (WML)**. Jest to niestandardowy język znaczników używany głównie w grze "Battle for Wesnoth", która jest turową grą strategiczną. WML służy do definiowania i dostosowywania różnych aspektów gry, w tym scenariuszy, kampanii, jednostek i innych. Jest to sposób, w jaki modderzy i programiści mogą tworzyć zawartość do gry.

Jest napisany w formacie przypominającym połączenie XML i prostego skryptu. Oto przegląd niektórych typowych elementów i struktur, które można znaleźć w pliku WML:

1. **Tagi:** WML używa tagów do definiowania różnych elementów gry. Tagi są ujęte w nawiasy ostre. Na przykład:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **Atrybuty:** W tagach możesz zdefiniować atrybuty, aby określić właściwości lub wartości powiązane z elementem. W powyższym przykładzie atrybutami są "typ" i "punkty życia".
    










3. **Tablice i tablice tablic:** Możesz tworzyć tablice danych, a nawet tablice tablic, aby zdefiniować listy jednostek, typów terenu lub innych elementów gry.
    










4. **Instrukcje warunkowe:** WML obsługuje instrukcje warunkowe w celu kontrolowania przebiegu gry. Na przykład:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **Pętle:** Pętli można używać do przeglądania list elementów lub wielokrotnego wykonywania czynności.
    










6. **Zawiera:** Możesz dołączyć inne pliki WML do głównego pliku WML, aby uporządkować i zmodularyzować treść.
    










7. **Procedury obsługi zdarzeń:** Możesz zdefiniować procedury obsługi zdarzeń, które będą uruchamiały akcje, gdy w grze wystąpią określone zdarzenia.
    











Oto uproszczony przykład pliku WML, który definiuje jednostkę niestandardową:

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## Bitwa o Wesnoth

"The Battle for Wesnoth" to popularna turowa gra strategiczna typu open source. Jest dostępny na wiele platform, w tym Mac, Windows, Linux i nie tylko. Gra stworzona przez oddaną społeczność wolontariuszy, znana jest z głębokiej i wciągającej rozgrywki, a także bogatego świata fantasy.

Najważniejsze cechy "Bitwy o Wesnoth" to:

1. **Oprawa fantasy:** Akcja gry rozgrywa się w świecie fantasy, w którym żyją różne rasy, w tym ludzie, elfy, krasnoludy, orki i nie tylko. Fabuła i narracja gry stanowią integralną część jej atrakcyjności.
    










2. **Strategia turowa:** Rozgrywka jest turowa, a gracze poświęcają czas na planowanie i wykonywanie swoich ruchów na sześciokątnych siatkach. Łączy taktyczną walkę ze strategicznym podejmowaniem decyzji.
    










3. **Kampanie:** Gra oferuje szeroką gamę kampanii dla pojedynczego gracza, każda z własną fabułą, postaciami i wyzwaniami. Gracze mogą odkrywać różne narracje i scenariusze.
    










4. ** Tryb wieloosobowy:** "Wesnoth" obsługuje tryb wieloosobowy online, umożliwiając graczom rywalizację między sobą w strategicznych bitwach. Tryby wieloosobowe obejmują grę kooperacyjną i mecze konkurencyjne.

## Jak otworzyć plik CFG?

Pliki CFG, które są powszechnie kojarzone z językiem Wesnoth Markup Language (WML) używanym w grze "The Battle for Wesnoth", można łatwo edytować za pomocą dowolnego standardowego edytora tekstu. Pliki te zawierają czytelny dla człowieka kod napisany w języku WML, który definiuje różne aspekty gry, w tym scenariusze, jednostki i kampanie.

Chociaż do modyfikowania plików CFG można używać dowolnego edytora tekstu, niektóre zaawansowane edytory tekstu, takie jak Emacs i Vi, udostępniają wtyczki podświetlające składnię WML. Wtyczki te zapewniają przydatne kodowanie kolorami i formatowanie, aby ułatwić użytkownikom rozróżnianie różnych elementów i struktur w kodzie WML.

Programy, które otwierają pliki CFG lub odwołują się do nich, obejmują

- Bitwa o Wesnoth (bezpłatna) dla (Windows, MAC, Linux)
- Notatnik Microsoftu

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
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
