{
  "date" : "2019-10-11",
  "keywords" :["plik jp2", "format pliku jp2", "co to jest plik jp2", "plik", "przykład jp2", "rozszerzenie pliku jp2", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - Format pliku obrazu",
  "description":"Poznaj format pliku JP2 i interfejsy API, które mogą tworzyć i otwierać pliki JP2.",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## Czym jest plik JP2? ##

JPEG 2000 (**JP2**) to system kodowania obrazu i najnowocześniejszy standard kompresji obrazu. Wykorzystuje technologię falkową do kodowania bezstratnej treści w dowolnej jakości jednocześnie. Co więcej, bez znacznego uszczerbku na wydajności kodowania, JPEG 2000 ma możliwość skutecznego dostępu i dekodowania tej samej treści do wielu innych rozdzielczości i jakości. Strumienie kodu w formacie JPEG 2000 są w znacznym stopniu skalowalne i zawierają obszary zainteresowania, które zapewniają przestrzenny swobodny dostęp.

JPEG 2000 wyróżnia się jako jeden z najbardziej skalowalnych standardów. Różne części obrazu mogą być przechowywane przy użyciu różnych jakości. Godną uwagi eskalację wydajności można osiągnąć, porządkując strumień kodu na różne sposoby. Niemniej jednak JP2 wymaga złożonych i wymagających obliczeniowo koderów/dekoderów, co wynika z tej elastyczności. W porównaniu z JPEG, JPEG 2000 wytwarza tylko artefakty dzwonienia, które tworzą pierścienie w pobliżu krawędzi obrazu i mogą być rozmyte, podczas gdy JPEG wykorzystuje bloki artefaktów wizualnych 8 × 8, które mogą być zarówno artefaktami dzwonienia, jak i blokowania. Posiadający do 16384 różnych komponentów o wymiarach w terapikselach i precyzji, która może sięgać nawet 38 bitów/próbkę.

## Historia ##

W 2000 roku komitet Joint Photographic Experts Group zaprojektował JP2 w celu ulepszenia własnego standardu JPEG opartego na dyskretnej transformacji kosinusowej za pomocą tej nowej metody opartej na falkach. Komitet JPEG miał na celu udostępnienie swoich podstawowych metod bez opłat licencyjnych. W konkurencji o licencję JP2 wśród 20 firm wygrały one o włos. JPEG 2000 został ogłoszony standardem ISO, chociaż większość przeglądarek internetowych nie jest gotowa na przyjęcie JPEG 2000 od 2017 roku.

## Części systemu kodowania obrazu JPEG 2000 ##

Poniżej przedstawiono główne części, które składają się na pełny zestaw standardów dla JPEG 2000.


|Część|Tytuł|Opis|Numer
---|---|---|---|
|Część 1|Podstawowy system kodowania| Definiuje składnię strumienia kodu. Różne etapy dekodowania obrazów JPEG 2000. Wyjaśnia podstawowy format pliku JP2, metadane i prawa własności intelektualnej, które należy podać.|ISO/IEC 15444-1
|Część 2|Rozszerzenia|Definiuje rozszerzenia strumienia kodu formatu plików i umożliwia demonstracje próbek HDR, specyfikację przestrzeni kolorów, kadrowanie, transformacje geometryczne; różnorodne animacje, metadane i wiele strumieni kodu.|ISO/IEC 15444-2
|Część 3|Motion JPEG 2000 (MJ2 lub MJP2)|Wprowadzenie formatu pliku dla sekwencji ruchu, kodowanie obrazów w niezależnym strumieniu kodu.|ISO/IEC 15444-3
|Część 4|Zgodność|Określa techniki testowania kodowania i dekodowania oraz sprawdza pliki zarówno pod kątem strumieni kodu nagiego, jak i plików JP2.|ISO/IEC 15444-4
|Część 5|Oprogramowanie referencyjne|Składa się z dwóch pakietów kodu źródłowego (Java, C), które implementują system kodowania Core i są dostępne na licencji open source.|ISO/IEC 15444-5
|Część 6|Złożony format pliku obrazu|Definiuje format pliku JPM i umożliwia obrazowanie wielostronicowych dokumentów w aplikacjach podobnych do faksów. Obsługuje użycie JBIG2 i JPEG.|ISO/IEC 15444-6
|Część 8|JPEG 2000 Secured (JPSEC)|Zapewnia bezpieczeństwo transakcji, treści i technologii oraz umożliwia zabezpieczone strumienie bitów JPEG 2000.|ISO/IEC 15444-8
|Część 9|JPIP|Definiuje narzędzia w środowisku sieciowym umożliwiające dostęp do metadanych i obrazów oraz określa interaktywne i wydajne protokoły|ISO/IEC 15444-9
|Część 10|JP3D|Rozszerzenie objętościowe Części 1 i wprowadzenie wymiaru Z. Rozszerza koncepcję kafelków, bloków kodu, dzielnic i trójwymiarowych funkcji ułatwień dostępu w obszarach zainteresowania.|ISO/IEC 15444-10
|Część 11|JPWL|Dotyczy dobrze zorganizowanej transmisji w podatnej na błędy sieci bezprzewodowej. To rozszerzenie jest kompatybilne z dekoderami|ISO/IEC 15444-11
|Część 13|Enkoder poziomu podstawowego|Definiuje implementację kodera poziomu podstawowego systemu kodowania Core.|ISO/IEC 15444-13
|Część 14|JPXML|Reprezentacja w formacie XML i wyjaśnia segmenty znaczników oraz metody dostępu do wewnętrznych danych obrazów.|ISO/IEC 15444-14
|Część 15|HTJ2K (w fazie rozwoju)|Określa alternatywny algorytm kodowania blokowego. Algorytm oferuje dziesięciokrotnie większą przepustowość i bezstratne kodowanie/dekodowanie.|

## Format pliku JP2 ##

JPEG 2000 definiuje format pliku oraz strumień kodu w taki sam sposób jak JPEG-1. Chociaż próbki obrazu są opisane wyłącznie przez JPEG 2000, to jednak JPEG-1 zawiera inne dodatkowe informacje o przestrzeni kolorów i rozdzielczości niezbędne do zakodowania obrazu. Jeśli obraz jest zapisany jako plik JPEG 2000, jako rozszerzenie używany jest **.jp2**. Ten format pliku jest dodatkowo ulepszany przez rozszerzenie JPEG 2000 part-2, które definiuje mechanizmy animacji i konfigurację wielu strumieni kodu w jednym obrazie. Rozszerzenie **.jpx** jest używane, gdy obrazy są zapisywane przy użyciu tego rozszerzonego formatu pliku. Ponieważ dane strumienia kodu nie są uważane za zapisywane przede wszystkim w plikach, dlatego do tego celu nie zdefiniowano żadnego standardowego rozszerzenia. Chociaż do celów testowych często otrzymuje rozszerzenie **.jpc** lub **.j2k**. W przeciwieństwie do JPEG-1, JPEG 2000 wybiera inny sposób kodowania metadanych w formacie XML. Standard 12234-1.4 (opracowany przez komitet ISO TC42) jest używany jako odniesienie między znacznikami Exif a komponentami XML. JPEG 2000 może zawierać standard ISO, w tym XMP.

### Kawałki ###
Pliki JPEG 2000 składają się z następujących po sobie fragmentów. Każdy fragment ma 8-bajtowy nagłówek: 4-bajtowy rozmiar fragmentu (big-endian, najpierw wysoki bajt) oraz 4-bajtowy typ fragmentu - jeden z predefiniowanych podpisów: "jP" lub "jP2".

Druga porcja musi być typu „ftyp” i mieć podtyp o przesunięciu 8. JPEG 2000 zdefiniowany przez podtyp, który musi być jedną z wartości: „jp2” (typ pliku \*.JP2), „jp20” (plik typ \*.JPA), "jpm " (typ pliku \*.JPM), "jpx " (typ pliku \*.JPX).

Powtarzając fragmenty, aż do wykrycia nieznanego typu, tworzymy plik obrazu/wideo JPEG 2000.

### Transformacja kolorów ###

Początkowo wymagana jest transformacja obrazów z przestrzeni kolorów RGB na inną przestrzeń kolorów. W tym celu istnieją dwa sposoby: nieodwracalna transformacja koloru (ICT) i odwracalna transformacja koloru (RCT). Pierwsza wykorzystuje przestrzeń kolorów YC,,B,,C,,R, i musi być zaimplementowana w stałej/zmiennoprzecinkowej przestrzeni kolorów, podczas gdy później zmodyfikowana przestrzeń kolorów YUV i odwracalna natura.// //Nie ogranicza się do modelu RGB, JPEG Język 2000 wykorzystuje transformację wielu komponentów.

### Dekarstwo ###

Po zakończeniu transformacji kolorów obraz przekształca się w prostokątne obszary zwane kafelkami, które można oddzielnie przekształcać i kodować. Rozmiar wszystkich kafelków będzie taki sam lub cały obraz można uznać za jeden kafelek. Dekoder wykorzystuje kafelkowanie i zużywa mniej pamięci lub może częściowo zakodować niektóre kafelki. Chociaż ta technika ma wadę polegającą na degradacji jakości obrazu.

### Transformacja falkowa ###

Obraz po kafelkowaniu jest przekształcany falkowo, który może być nieodwracalny lub odwracalny i realizowany za pomocą schematu splotu lub podnoszenia.

### Stopień sprężania ###

W zależności od fizycznych właściwości obrazu uzyskuje się wzmocnienie kompresji na poziomie 20%. Przewidywanie nadmiarowości przestrzennej w formacie JPEG 2000 odgrywa istotną rolę w procesie kompresji, a obrazy o wysokiej rozdzielczości zwykle zyskują największą przewagę.

## Aplikacje obsługiwane przez standard ##

* Nagrywanie, edycja i przechowywanie filmów HD opartych na klatkach
* Obrazowanie medyczne i dane biometryczne
* zdjęcia satelitarne, teledetekcja i detekcja ruchu
* Komunikacja klient/serwer, dystrybucja sieciowa i przechowywanie.
* Kino cyfrowe, przekaz na żywo HDTV, cyfrowe materiały audiowizualne

## Bibliografia ##

* [Przegląd formatu JPEG 2000](https://jpeg.org/jpeg2000)
* [System kodowania obrazu JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)

