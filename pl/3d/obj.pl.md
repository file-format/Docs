{
  "date" : "2019-10-11",
  "keywords" :["plik obj", "format pliku obj", "co to jest plik obj", "plik", "przykład obiektu", "rozszerzenie pliku obj", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku OBJ",
  "description":"Poznaj format pliku OBJ i interfejsy API, które mogą otwierać i tworzyć pliki OBJ.",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik OBJ?

Pliki **OBJ** są używane przez aplikację Wavefront Advanced Visualizer do definiowania i przechowywania obiektów geometrycznych. Przesyłanie wstecz i do przodu danych geometrycznych jest możliwe dzięki plikom OBJ. Zarówno geometria wielokątna, jak punkty, linie, wierzchołki tekstur, ściany, jak i geometria swobodna (krzywe i powierzchnie) są obsługiwane przez format OBJ. Ten format nie obsługuje animacji ani informacji związanych ze światłem i pozycją scen.

Plik OBJ jest zwykle produktem końcowym procesu modelowania 3D generowanego przez CAD (projektowanie wspomagane komputerowo). Domyślna kolejność przechowywania wierzchołków jest przeciwna do ruchu wskazówek zegara, unikając jawnej deklaracji normalnych twarzy. Chociaż pliki OBJ deklarują informacje o skali w wierszu komentarza, nie zadeklarowano żadnych jednostek dla współrzędnych OBJ.

## Historia formatu 3D OBJ

Firma Wavefront Technologies stworzyła format pliku OBJ dla swojej aplikacji Advanced Visualizer do przechowywania obiektów geometrycznych i danych 3D. Jego wersja 2.11 została zastąpiona nowo udokumentowaną wersją 3. Format pliku jest otwarty i został zaimplementowany przez innych dostawców do ich aplikacji do grafiki 3D. Firma Wavefront Technologies zachowała ten format plików jako open source i neutralny.

## Format pliku OBJ

W obiektach 3D kodowanie geometrii powierzchni jest trudnym zadaniem, które format pliku OBJ wykonał bardzo dobrze. Ten format jest dość uniwersalny, ponieważ oferuje wiele możliwości kodowania geometrii powierzchni. Poniżej przedstawiono trzy dozwolone formaty, które mają swoje zalety i wady:

### Teselacja z wielobocznymi ścianami

Format pliku OBJ ułatwia użytkownikowi mozaikowanie powierzchni modelu 3D przy użyciu prostych lub złożonych kształtów geometrycznych. W przypadku kodowania geometrii powierzchni modelu plik przechowuje wierzchołki i normalną do każdego wielokąta. Chociaż teselacja zwiększa chropowatość modelu, konieczne jest znalezienie właściwej równowagi między rozmiarem pliku a jakością jego wydruku.

### Krzywa o swobodnym kształcie

Format pliku OBJ umożliwia zdefiniowane przez użytkownika dowolne krzywe powierzchni w celu określenia geometrii powierzchni modelu. Ponieważ krzywe o dowolnym kształcie są bardziej złożone niż ściany wielokątne, ponieważ przy niewielkiej liczbie parametrów matematycznych zakrzywione linie można najlepiej zdefiniować za pomocą krzywych o dowolnym kształcie. Dlatego przy mniejszej ilości danych w porównaniu z mozaikami wielokątnymi, krzywe o swobodnych kształtach używane do generowania wysokiej jakości kodowania dowolnego modelu 3D bez zwiększania rozmiaru pliku.

### Powierzchnie o dowolnym kształcie

Format pliku OBJ określa również kafelkowanie geometrii powierzchni z dowolnymi łatami powierzchni. Ten rodzaj łat powierzchni o dowolnym kształcie (NURBS) jest bardzo odpowiedni dla powierzchni bez sztywnych wymiarów promieniowych, takich jak nadwozie ciężarówki, skrzydła helikoptera lub kadłub łodzi. Korzystanie z powierzchni o dowolnym kształcie jest bardzo korzystne, ponieważ są one bardziej precyzyjne, aby zachować mniejsze rozmiary plików przy większej precyzji. Powierzchnie te są istotną częścią przemysłu lotniczego i samochodowego, gdzie niska precyzja jest bezlitosna.

Następujące słowa kluczowe są uporządkowane według typu danych w celu zdefiniowania geometrii powierzchni.


|Elementy|Dowolne formy krzywej/powierzchni ciała|Atrybuty swobodnej krzywej/powierzchni
---|---|---|
|p|Punkt|parametr|Wartości parametrów|stopnie|Stopnie
|l|Linia|przycinanie|Zewnętrzna pętla przycinania|bmat|Matryca bazowa
|f|Płaszcz|otwór|Wewnętrzna pętla przycinania|krok|Rozmiar kroku
|curv|Krzywa|scrv|Specjalna krzywa|cstype|Krzywa lub typ powierzchni
|curv2|Krzywa 2D|sp|Specjalny punkt|**Łączność i grupowanie powierzchni**
|surf|Powierzchnia|koniec|Instrukcja końcowa|con|connect
|**Atrybuty wyświetlania/renderowania**|g|Nazwa grupy
|bevel|Interpolacja skosu|shadow_obj|Rzucanie cienia|s|Grupa wygładzania
|lod|Poziom szczegółowości|trace_obj|Ray tracing|mg|Łączenie grup
|d_interp|Interpolacja rozpuszczania|ctech|Technika aproksymacji krzywych|o|Nazwa obiektu
|c_interp|Interpolacja kolorów|stech|Technika aproksymacji powierzchni|
|usemtl|Nazwa materiału|mtllib|Biblioteka materiałów|
|**Geometryczne wierzchołki**|
|v|wierzchołki geometryczne|vn|normalne wierzchołków|
|vt|wierzchołki tekstury|vp|wierzchołki przestrzeni parametrów|

### Kolor i tekstura

Plik OBJ umożliwia przechowywanie informacji o kolorze i teksturze w powiązanym formacie pliku o nazwie Material Template Library (MTL). Wielokolorowe modele geometryczne są renderowane przy użyciu tych dwóch plików razem. Pliki MTL są oparte na ASCII i ułatwiają renderowanie komputerowe, opisując właściwości powierzchni odbijającej światło za pomocą modelu odbicia Phonga. Standard został przyjęty przez wielu dostawców oprogramowania, którzy wykorzystują jego zalety do wymiany materiałów. Format MTL jest nieco przestarzały, ponieważ nie obsługuje najnowszych technologii, takich jak mapy lustrzane i paralaksy.

## Bibliografia

* [Plik Wavefront .obj](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

