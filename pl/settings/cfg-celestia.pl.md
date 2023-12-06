{
"data": "27.09.2023",
  "keywords": [
"cfg",
"plik cfg",
"cfg plik konfiguracyjny Celestii",
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
"title": "Format pliku CFG - plik konfiguracyjny Celestii",
  "description":"Dowiedz się o formacie pliku konfiguracyjnego CFG Celestia i interfejsach API, które umożliwiają tworzenie i otwieranie plików CFG.",
"linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
      "parent": "settings"
}
},
"lastmod": "27.09.2023"
}

## Czym jest plik CFG?

Plik konfiguracyjny Celestii to zwykły plik tekstowy używany przez Celestia, program do symulacji wszechświata 3D. Pliki te są niezbędne do dostosowania zachowania Celestii, wyświetlanych obiektów niebieskich i wyglądu programu. Edycja tych plików wymaga jednak szczególnej uwagi, ponieważ niewłaściwe zmiany mogą zakłócić proces ładowania Celestii, uniemożliwiając jej prawidłowe działanie.

## Celestia

Celestia to bezpłatne oprogramowanie do symulacji astronomii 3D o otwartym kodzie źródłowym, które umożliwia użytkownikom eksplorację i wizualizację wszechświata w wysoce realistyczny i interaktywny sposób. Został opracowany przez Chrisa Laurela i został wydany po raz pierwszy na początku XXI wieku. Celestia jest dostępna dla systemów operacyjnych Windows, macOS i Linux.

Kluczowe cechy i aspekty Celestii obejmują:

- **Realistyczna wizualizacja 3D:** Celestia zapewnia szczegółowe i dokładne odwzorowanie naszego Układu Słonecznego, a także gwiazd, galaktyk i innych ciał niebieskich. Wykorzystuje wysokiej jakości modele i tekstury 3D, aby stworzyć wciągające wizualnie wrażenia.

- **Rozbudowana baza danych o obiektach niebieskich:** Oprogramowanie zawiera obszerną wbudowaną bazę danych znanych obiektów niebieskich, w tym gwiazd, planet, księżyców, asteroid, komet i statków kosmicznych. Użytkownicy mogą łatwo lokalizować i eksplorować te obiekty.

- **Dokładność naukowa:** Chociaż Celestia jest narzędziem do wizualizacji, jego celem jest możliwie najdokładniejsze przedstawienie obiektów i zjawisk niebieskich w oparciu o dostępne dane naukowe.

## Formaty plików używane przez Celestię

Celestia wykorzystuje różne formaty plików do różnych aspektów swojej trójwymiarowej symulacji astronomicznej. Oto niektóre z kluczowych formatów plików używanych przez Celestię:

1. **Pliki konfiguracyjne (.cel)**
- *Opis*: Zwykłe pliki tekstowe, które pozwalają użytkownikom dostosować zachowanie, wygląd i zawartość Celestii.
- *Cel*: Dostosowywanie ustawień, definiowanie lokalizacji i określanie obiektów niebieskich.

2. **Modele 3D i siatki**
- *Formaty*: [.3ds](/pl/3d/3ds/), [.obj](/pl/3d/obj/), [.dae](/pl/3d/dae/), .ac
- *Opis*: Obsługiwane formaty plików modeli 3D używanych do renderowania ciał niebieskich i statków kosmicznych.
- *Cel*: Wyświetlanie obiektów 3D w Celestii.

3. **Pliki tekstur**
- *Formaty*: [.jpg](/pl/image/jpeg/), [.png](/pl/image/png/), [.dds](/pl/image/dds/)
- *Opis*: Te pliki zawierają tekstury powierzchni ciał niebieskich.
- *Cel*: Mapowanie tekstur na modele 3D w celu uzyskania realistycznego wyglądu.

4. **Katalogi gwiazd i pliki danych**
- *Formaty*: Formaty niestandardowe, [.csv](/pl/spreadsheet/csv/), [.tsv](/pl/spreadsheet/tsv/)
- *Opis*: Pliki danych używane do reprezentowania gwiazd i innych ciał niebieskich, zapewniające dokładną symulację.
- *Cel*: Dokładne przedstawienie obiektów niebieskich.

5. **Mapy kostek tekstur**
- *Opis*: Mapy kostkowe służą do symulacji wyglądu odległych obiektów niebieskich, takich jak galaktyki.
- *Cel*: Renderowanie odległych obiektów z realistycznymi teksturami.

6. **Pliki skryptów**
- *Opis*: Te pliki zawierają niestandardowe skrypty napisane w języku skryptowym Celestii.
- *Cel*: Umożliwienie użytkownikom tworzenia dynamicznych wydarzeń i animacji we wszechświecie Celestii.

## Plik konfiguracyjny Celestii

Oto podstawowy przegląd możliwości pliku konfiguracyjnego Celestii:

1. **Ustawianie swojej lokalizacji**: Możesz określić swoją lokalizację na Ziemi za pomocą parametrów szerokości, długości i wysokości geograficznej. Dzięki temu Celestia może dokładnie wyświetlać nocne niebo z Twojej pozycji.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Dostosowywanie opcji wyświetlania:** Możesz dostosować różne opcje wyświetlania, takie jak pole widzenia, ustawienia czasu i preferencje renderowania.

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **Ładowanie obiektów niebieskich:** Do swojej symulacji możesz dodawać obiekty niebieskie, takie jak gwiazdy, planety, asteroidy, statki kosmiczne i inne. Każdy obiekt jest zdefiniowany w pliku konfiguracyjnym wraz z jego właściwościami.

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **Definiowanie statków kosmicznych:** Możesz stworzyć swój własny fikcyjny statek kosmiczny lub użyć prawdziwych, określając ich parametry, takie jak położenie, orientacja i modele 3D.

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **Tworzenie skryptów:** Możesz pisać skrypty w niestandardowym języku skryptowym Celestii, aby tworzyć dynamiczne wydarzenia i animacje.

## Jak otworzyć plik CFG?

Programy otwierające pliki CFG lub odwołujące się do nich

- Celestia (bezpłatna) dla (Windows, Mac, Linux)

## Inne pliki CFG

Oto inne typy plików, które mają rozszerzenie **.cfg**.

**Ustawienia**
- [CFG - Plik konfiguracyjny Celestii](/pl/settings/cfg-celestia/)
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
* [Celestia](https://en.wikipedia.org/wiki/Celestia)

