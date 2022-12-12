{
  "date" : "2021-01-22",
  "keywords" :[ "ASE", "plik", "format", "typ pliku", "rozszerzenie", "co to jest plik ASE?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku ASE i interfejsy API, które mogą otwierać i tworzyć pliki ASE.",
  "title" :"ASE — plik eksportu sceny Autodesk ASCII",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## Czym jest plik ASE?

Plik z rozszerzeniem .ase to format pliku Autodesk ASCII Scene Export, który jest reprezentacją sceny w formacie ASCII, zawierającą informacje 2D lub 3D podczas eksportowania danych sceny przy użyciu programu Autodesk. Firma Autodesk udostępnia opcje dołączania komponentów sceny podczas eksportowania danych sceny. Możesz dołączyć definicję siatki wraz z informacjami o wierzchołkach i powierzchniach, opis materiału, transformację danych animacji dla obiektów, pełną definicję siatki co n klatek, dane animacji dla kamer i świateł oraz ustawienia połączeń IK.

## Format pliku ASE — więcej informacji

Pliki ASE to pliki tekstowe przechowywane w formacie ASCII, które można otworzyć w dowolnym edytorze tekstu. Plik ASE może zawierać następujące typy informacji dostarczanych przez firmę Autodesk.

### Opcje wyjścia

* `Definicja siatki` - Eksportuje definicję każdej siatki, w tym informacje o wierzchołkach i powierzchniach obiektów geometrycznych. Ponadto włączenie tej opcji powoduje włączenie elementów w polu grupy Opcje siatki, opisanych poniżej.
* `Materiały` — zawiera opis materiału. Jeśli materiał nie jest przypisany do obiektu, eksportowany jest jego kolor modelu szkieletowego. Uwzględniono wszystkie poziomy drzewa materiałów, więc może to spowodować powstanie dużej ilości tekstu.
* `Transform Animation Keys` - Zawiera dane animacji transformacji dla obiektów. Jeśli obiekt jest docelową kamerą lub reflektorem, będzie to obejmować dane animacji celu.
* `Animowana siatka` - Eksportuje pełną definicję siatki co n klatek. Częstotliwość jest określana za pomocą pokrętła wyjścia kontrolera, opisanego poniżej. Każdy blok zawiera te same informacje, które zostały określone w polu grupy Opcje siatki, opisanym poniżej. Włączenie tej opcji może skutkować powstaniem ogromnego pliku, nawet w przypadku małych scen.
* `Animowane ustawienia kamery/światła` - Eksportuje dane animacji dla kamer i świateł, takie jak kolor, intensywność, spadek, odchylenie mapy i tak dalej. Generuje blok co n klatek, zgodnie z pokrętłem Controller Output.
* `Inverse Kinematic Joints` - Eksportuje ustawienia połączeń IK w gałęzi Hierarchia.

### Typy obiektów

Pozycje tutaj pozwalają określić, którą kategorię obiektów chcesz uwzględnić w danych wyjściowych. Możesz dołączyć obiekty geometryczne, kształty, kamery, światła i obiekty pomocnicze.

* Geometryczne
* Kształty
* Kamery
* Światła
* Pomocnicy

### Opcje siatki

* `Normalne siatki` - Eksportuje normalne twarzy i wierzchołków. Normalna ściany jest wymieniona jako pierwsza, a następnie normalne trzech wierzchołków podtrzymujących ścianę. Włączenie tej opcji powoduje utworzenie znacznie większego pliku.
* `Mapping Coordinates` - Eksportuje listę wierzchołków i powierzchni mapowania, zgodnie ze strukturami TVert i TVFace opisanymi w 3ds Max Software Development Kit. Jeśli obiekt używa mapowania twarzy, eksportowana jest lista map twarzy zawierająca współrzędne UVW dla każdej twarzy.
* `Kolory wierzchołków` - Eksportuje kolory wierzchołków.

### Wyjście kontrolera

* `Użyj kluczy` - Eksportuje kluczowe wartości. Jeśli kontroler nie używa klawiszy, wówczas używana jest metoda Force Sample. W przypadku kontrolerów transformacji opcja Użyj klawiszy działa tylko wtedy, gdy wszystkie kontrolery transformacji są albo liniowe/TCB, albo Beziera. Jeśli jedna ze ścieżek transformacji wykorzystuje inny typ kontrolera, wówczas dla wszystkich ścieżek transformacji stosowana jest metoda Force Sample.
* `Wymuś pobieranie próbek` - Próbkuje wartości kontrolera na podstawie częstotliwości określonej w Ramkach na kontroler próbki.

## Bibliografia

* [Autodesk — eksportowanie do ASCII](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2020/ENU/3DSMax-Data-Exchange/files/GUID-98B2388D -A3A7-4096-8E81-888A3F9D6069-htm.html)

