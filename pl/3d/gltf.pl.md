{
  "date" : "2019-12-12",
  "keywords" :["GLTF", "plik", "rozszerzenie", "format", "3D", "Khronos Group 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Dowiedz się o plikach GLTF i interfejsach API, które mogą tworzyć i otwierać pliki GLTF.",
  "title" :"GLTF - Format pliku transmisji GL",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik GLTF?

glTF (GL Transmission Format) to format pliku 3D, który przechowuje informacje o modelu 3D w formacie JSON. Użycie JSON minimalizuje zarówno rozmiar zasobów 3D, jak i przetwarzanie w czasie wykonywania potrzebne do rozpakowania i użycia tych zasobów. Został przystosowany do sprawnego przesyłania i ładowania scen i modeli 3D przez aplikacje. glTF został opracowany przez grupę roboczą Khronos Group 3D Formats i jest również opisywany jako [JPEG](/pl/image/jpeg/) 3D przez jego twórców.

Format pliku GLTF definiuje rozszerzalny, powszechny format publikowania dla narzędzi i usług treści 3D, który usprawnia procesy tworzenia treści i umożliwia interoperacyjne wykorzystanie treści w całej branży. Intencją stworzenia formatu plików glTF było zdefiniowanie rozszerzalnego, wspólnego formatu publikowania dla narzędzi i usług treści 3D, który powinien usprawnić procesy tworzenia treści i umożliwić interoperacyjne wykorzystanie treści w całej branży. Minimalizuje przetwarzanie w czasie wykonywania przez aplikacje korzystające z WebGL i innych interfejsów API.

## Krótka historia pliku GLTF

Pierwsze specyfikacje formatu pliku glTF 1.0 zostały ogłoszone w październiku 2015 r. Było to serią wysiłków rozpoczętych w marcu 2012 r. przez Khronos. Celem tych działań była ocena szans związanych z trakcją WebGL. W rezultacie pierwsze demo formatu glTF, oparte na formacie JSON, zostało zaprezentowane na spotkaniu WebGl w 2012 roku. Format ten był od czasu do czasu przyjmowany przez kilka firm, w tym Cesium, 3D Tiles, Oculus, Microsoft, Archilogic i inne.

glTF 2.0 został opublikowany 5 czerwca 2017 roku na konferencji Web3D 2017. Istnieje długa lista firm, które później przyjęły format pliku glTF.

## Format pliku GLTF

Specyfikacje formatu plików dla glTF 2.0 są dostępne [online](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0) w celach informacyjnych i należy się z nimi zapoznać w każdej implementacji związanej z odczytem/zapisem w celu wsparcia format pliku glTF.

glTF definiuje zasoby jako pliki JSON z obsługującymi danymi zewnętrznymi. Reprezentuje modele 3D za pomocą:

* Pełny opis sceny zawarty w pliku .glTF w formacie JSON, który zawiera informacje o hierarchii węzłów, materiałach, kamerach, a także informacje deskryptorowe dla siatek, animacji i innych konstrukcji
* Pliki binarne (.bin) zawierające dane geometrii i animacji oraz inne dane oparte na buforze
* Pliki graficzne ([.jpg](/pl/image/jpeg/), [.png](/pl/image/png/)) dla tekstur

Wszelkie zasoby zewnętrzne, takie jak obrazy, są przechowywane w zewnętrznych plikach, do których odwołuje się identyfikator URI. Te identyfikatory URI są przechowywane obok kontenera GLB lub osadzone bezpośrednio w JSON przy użyciu identyfikatorów URI danych. Każdy ważny glTF musi określać swoją wersję.

glTF został zaprojektowany tak, aby osiągnąć mały rozmiar pliku, szybkie ładowanie, pełną reprezentację sceny 3D i rozszerzalność. Te unikalne cele projektowe są głównymi przyczynami popularności formatu plików glTF w domenie 3D. Poniżej przedstawiono typy MIME obsługiwane przez format pliku glTF dla różnych typów plików:

* Pliki .gltf używają modelu/gltf+json
* Pliki .bin używają application/octet-stream
* Pliki tekstur używają oficjalnego typu obrazu/* w oparciu o określony format obrazu. W celu zapewnienia zgodności z nowoczesnymi przeglądarkami internetowymi obsługiwane są następujące formaty obrazów: image/jpeg, image/png.

### Kodowanie JSON

glTF nakłada następujące dodatkowe ograniczenia na format pliku JSON

Aby uprościć implementację po stronie klienta, glTF ma dodatkowe ograniczenia dotyczące formatu i kodowania JSON.

1. JSON musi używać kodowania UTF-8 bez BOM.
1. Wszystkie łańcuchy zdefiniowane w tej specyfikacji (nazwy właściwości, wyliczenia) używają tylko zestawu znaków ASCII i muszą być zapisane jako zwykły tekst, np. "bufor" zamiast `"\u0062\u0075\u0066\u0066\u0065\u0072"`.
1. Nazwy (klucze) w obiektach JSON muszą być unikalne, tzn. duplikaty kluczy są niedozwolone.

### URI

Zasoby buforów i obrazów są przywoływane za pośrednictwem identyfikatorów URI. Klienci muszą obsługiwać następujące dwa typy identyfikatorów URI.

**Dane URI:** Data URI są zdefiniowane w RFC 2397 i są używane przez glTF do osadzania zasobów w JSON.

**Ścieżki względnego identyfikatora URI:** lub path-noscheme zgodnie z definicją zawartą w dokumencie RFC 3986, [sekcja 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) — bez schematu, uprawnień ani parametrów. Zarezerwowane znaki muszą być zakodowane procentowo zgodnie z dokumentem RFC 3986, [sekcja 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2).

## Bibliografia ##

* [Specyfikacje glTF 2.0 - Khronos](https://github.com/KhronosGroup/glTF)
* [Format pliku glTF – według Wikipedii](https://en.wikipedia.org/wiki/GlTF)

