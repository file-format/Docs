{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "keywords" :[ "SWF", "plik", "rozszerzenie", "format", "format wideo", "Co to jest plik SWF", "format pliku SWF", "odtwarzacz plików SWF", "jak otworzyć plik SWF"] ,
  "title" :"Plik SWF — format pliku Flash Shockwave Flash",
  "description":"Dowiedz się, co to jest plik SWF i interfejsy API, które mogą tworzyć, i pokaż, jak otworzyć plik SWF.",
  "linktitle" : "SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik SWF?

Plik SWF to plik animacji utworzony za pomocą programu Adobe Flash. Może zawierać różnego rodzaju elementy, takie jak tekst, obrazy wektorowe, obrazy rastrowe, skrypty akcji, obiekty, takie jak koła, linie, kwadraty i prostokąty, aby utworzyć animację. Pliki SWF porządkują te elementy multimedialne w klatkach, które mogą być odtwarzane z różną liczbą klatek na sekundę (fps). SWF oznacza krótki plik internetowy, ale znany jest również z formatu Shockwave.

Aplikacje, które mogły *otwierać pliki SWF**, obejmowały Adobe Flash Player (obecnie wycofany) i Eltima Elmedia Player.

## Format pliku SWF — więcej informacji

Pliki SWF były używane do przechowywania jako pliki binarne na dysku. Format pliku SWF został wykorzystany do opracowania animacji i gier, które można osadzać na stronach internetowych i odtwarzać niezależnie. Obsługuje również filmy i dźwięki, które dają programistom wiele możliwości tworzenia interaktywnych aplikacji multimedialnych. Pliki SWF można odtwarzać w przeglądarkach internetowych z zainstalowanym programem Adobe Shockwave. Adobe Flash został wycofany w grudniu 2020 r. Ze względu na niedociągnięcia i problemy z bezpieczeństwem.

## Krótka historia formatu pliku SWF

Format pliku SWF został pierwotnie zaprojektowany przez FutureWave Software, aby wyświetlać animacje z zamiarem uruchomienia na oprogramowaniu odtwarzacza w dowolnym systemie z wolniejszymi połączeniami sieciowymi, przy jednoczesnym zachowaniu małego rozmiaru pliku. W grudniu 1996 roku firma Macromedia była właścicielem FutureWave i przeszła na Macromedia Flash 1.0.

W 2005 roku firma Macromedia została przejęta przez firmę Adobe, która w 2008 roku ogłosiła SWF jako część swojego projektu open source. W tym samym roku firma Adobe udostępniła kod do popularnych na świecie silników internetowych, aby umożliwić im przeszukiwanie i indeksowanie plików SWF. Ponieważ jednak wydaje się, że pliki SWF stają się standardowym formatem do publikowania treści Flash w Internecie, SWF został zmieniony tak, aby oznaczał mały format internetowy.

## Struktura pliku SWF

Ścieżka to podstawowy element graficzny SWF, który jest ciągiem segmentów podstawowych elementów, począwszy od prostych linii, a skończywszy na krzywych Beziera. Te proste elementy pomagają również tworzyć inne dodatkowe prymitywy, takie jak kostki, elipsy, a nawet teksty. Prymitywy graficzne w pliku SWF są podobne do elementów graficznych innych formatów, takich jak SVG i MPEG-4 BIFS.

Wyświetlanie list i ponowne użycie/zmiana nazwy już zdefiniowanych elementów są również dozwolone przez format. Format strumienia binarnego SWF można porównać do atomów QuickTime, które są podobne pod względem znacznika, rozmiaru i ładunku. Format strumienia binarnego pozwala starszym graczom pominąć nieobsługiwane treści. Chociaż oryginalne wersje SWF były ograniczone do grafiki wektorowej i obrazów, dlatego nowe wersje umożliwiają również zawartość audio i wideo.

Nowy interfejs API 3D niskiego poziomu Flash Playera o nazwie „Stage3D” został wprowadzony w wersji 11. Ten interfejs API miał być odpowiednikiem OpenGL lub Direct3D. Stage3D definiuje kolory w języku niskiego poziomu o nazwie Adobe Graphics Assembly Language (AGAL). Poniżej przedstawiono kilka podstawowych typów danych formatu plików SWF.

### Współrzędne

Współrzędne XY w formacie pliku SWF są zapisywane jako liczby całkowite i mierzone w jednostce zwanej twipem. Twip składa się z 1/20 piksela logicznego. Piksel logiczny i piksel ekranowy są takie same, gdy plik jest odtwarzany bez skalowania w 100%.

### Typy całkowite i kolejność bajtów

Typy liczb całkowitych ze znakiem i bez znaku 8, 16, 32 i 64 bity są dozwolone w formacie pliku SWF. Little-endian kolejność bajtów jest używana do przechowywania wartości całkowitych. Chociaż w bajtach kolejność bitów jest przechowywana w big-endian. Wszystkie wartości całkowite powinny być wyrównane do bajtów. Liczby całkowite ze znakiem są reprezentowane przy użyciu tradycyjnych wzorców bitowych dopełnienia do dwóch.

### Liczby stałoprzecinkowe

Format pliku SWF obsługuje dwa typy liczb stałoprzecinkowych, tj. 32- i 16-bitowe.

### Liczb zmiennoprzecinkowych

SWF 8 i nowsze wersje używają trzech typów liczb zmiennoprzecinkowych (FLOAT, FLOAT 16, DOUBLE), które są zgodne ze standardem IEEE 754 dotyczącym typów zmiennoprzecinkowych.

### Zakodowane liczby całkowite

Jeden typ zakodowanej liczby całkowitej jest obsługiwany przez SWF 9 i nowsze ze zmienną liczbą bajtów.

## Bibliografia

* [Format pliku SWF](https://en.wikipedia.org/wiki/Swf)

