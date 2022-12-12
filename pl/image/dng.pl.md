{
  "date" : "2019-10-11",
  "keywords" :[ "plik dng", "format pliku dng", "co to jest plik dng", "plik", "przykład dng", "rozszerzenie pliku dng", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DNG — format pliku obrazu z aparatu cyfrowego",
  "description":"Poznaj format plików DNG i interfejsy API, które mogą tworzyć i otwierać pliki DNG.",
  "linktitle" : "DNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik DNG?

DNG to format obrazu z aparatu cyfrowego używany do przechowywania plików RAW. Został opracowany przez firmę Adobe we wrześniu 2004 roku. Zasadniczo został opracowany dla fotografii cyfrowej. DNG jest rozszerzeniem standardowego formatu [TIFF](/pl/image/tiff/)/EP i znacząco wykorzystuje metadane. Aby manipulować nieprzetworzonymi danymi z aparatów cyfrowych z łatwością elastyczności i artystycznej kontroli, fotografowie wybierają pliki camera raw. Formaty JPEG i TIFF przechowują obrazy przetworzone przez aparat, dlatego w takich formatach nie ma zbyt wiele miejsca na zmiany.

## Historia i wersje formatu pliku DNG

Do tej pory powstało 5 wersji specyfikacji DNG. Wersja 1.0.0.0 została uruchomiona we wrześniu 2004 roku wraz z wydaniem „2.3” (ACR i DNG Converter). W lutym 2005 została opublikowana wersja 1.1.0.0. W maju 2008 została wydana wersja 1.2.0.0, która została wykorzystana w „4.4”. Wersja 1.3.0.0 została opublikowana w czerwcu 2009 roku. Wersja 1.4.0.0 pojawiła się w 2012 roku.

## Format pliku DNG

Natomiast pliki camera raw przechwytują nieprzetworzone lub słabo przetworzone dane bezpośrednio z czujnika. Ponieważ są one podobne do negatywów filmowych, formaty camera raw są również znane jako „cyfrowe negatywy”. Zaletą surowych formatów jest zwiększona kontrola artystyczna dla użytkownika końcowego. Użytkownik może dostosować różne zakresy parametrów zgodnie z wymaganiami, takimi jak balans bieli, mapowanie tonalne, redukcja szumów, wyostrzanie i tak dalej. Z drugiej strony plik camera raw musi zostać przetworzony do dowolnego użytku za pomocą dowolnego oprogramowania lub konwertera.

Ponieważ nie było dostępnego standardowego formatu dla plików camera raw, stwarzało to wiele problemów dla użytkownika końcowego. Firma Adobe rozwiązała te problemy i zdefiniowała niezastrzeżony format plików camera raw. Format jest znany jako Digital Negative lub DNG. DNG może być używany przez szeroką gamę sprzętu i oprogramowania do przetwarzania plików RAW. Ponadto DNG może być również używany jako format pośredni do przechowywania obrazów, które zostały pierwotnie przechwycone przez aparaty posiadające własne, zastrzeżone formaty RAW.

### Specyfikacje formatu plików DNG

W tej sekcji opiszemy format DNG jako rozszerzenie TIFF 6.0.

* **Rozszerzenia plików**: DNG wykorzystuje rozszerzenia „.DNG” lub „.TIF”.
* **Drzewa SubIFD**: DNG nie obsługuje łańcuchów SubIFD, zamiast tego DNG zaleca korzystanie z drzew SubIFD, jak wspomniano w specyfikacjach TIFF-EP. Najwyższa jakość i rozdzielczość mogą używać NewSubFileType o wartości 0, podczas gdy miniatury o obniżonej jakości powinny używać wartości NewSubFileType równej 1. Zaleca się również, choć nie jest to wymagane, aby pierwszy IFD miał miniaturę o niskiej jakości lub rozdzielczości.
* **Kolejność bajtów**: Kolejność bajtów musi być obsługiwana przez czytniki DNG, także dla plików z określonego modelu aparatu.
* **Zamaskowane piksele**: większość czujników aparatu oblicza w pełni zamaskowane piksele na krawędzi czujnika za pomocą kodowania czerni. Te piksele można dołączyć lub przyciąć przed zapisaniem obrazu w formacie DNG. Jeśli zamaskowane piksele nie są przycięte, to obszar tych pikseli musi być podany w znaczniku ActiveArea. Informacje zebrane z tych pikseli o poziomie kodowania czerni powinny być wykorzystane albo przed zapisaniem surowych danych, albo mogą być zawarte w pliku DNG określającym poziom czerni.
* **Uszkodzone piksele**: przed zapisaniem nieprzetworzonych danych w formacie DNG należy wykluczyć wadliwe piksele.
* **Metadane**: Metadane mogą być zawarte w DNG w jeden z następujących sposobów:
** Przy użyciu tagów metadanych TIFF-EP lub EXIF
** Poprzez tag metadanych IPTC (33723)
** Korzystanie ze znacznika metadanych XMP (700)
* **Dane zastrzeżone**: Zwykle dostawcy dołączają dane zastrzeżone w nieprzetworzonych plikach do wykorzystania przez ich własne konwertery. DNG przechowuje swoje zastrzeżone dane w prywatnych tagach, prywatnych IFD oraz w prywatnej MakerNote. Dostawcy muszą używać tagów DNGPrivateData i MakerNoteSafety, aby mieć pewność, że aplikacje, które edytują pliki DNG, zachowują te zastrzeżone dane.

Poniżej przedstawiono kilka ważnych ograniczeń i rozszerzeń tagów TIFF.

**Bity na próbkę**

Obsługiwane są od 8 do 32 bitów na próbkę. Każda próbka musi mieć taką samą głębokość, gdy parametr SamplePerPixel nie jest równy 1. Ale jeśli parametr BitsPerSample nie jest równy 8, 16 lub 32, bity muszą być spakowane w bajty przy użyciu domyślnego ustawienia FillOrder TIFF równego 1 (big-endian).

**Kompresja**

Obsługiwane są dwie wartości tagów kompresji:

* Wartość nr 1: Dane nieskompresowane.
* Wartość # 7: Skompresowane dane JPEG, albo podstawowy format DCT JPEG, albo bezstratna kompresja JPEG.

**Interpretacja fotometryczna**

Następujące wartości są obsługiwane tylko w przypadku IFD miniatur i podglądu:

* 1 = CzarnyIsZero. Zakłada się, że jest w przestrzeni kolorów gamma 2.2.
* 2 = RGB. Zakłada się, że jest w przestrzeni kolorów sRGB.
* 6 = YCbCr. Używany do podglądu obrazów zakodowanych w formacie JPEG.

Następujące wartości są obsługiwane dla surowego IFD i zakłada się, że są to natywna przestrzeń kolorów kamery:

* 32803 # CFA (macierz filtrów kolorów).
* 34892 # Liniowy surowy.

**Orientacja**

Znacznik orientacji jest używany w przeglądarkach plików, aby mogły wykonywać bezstratne obracanie plików DNG. Czytniki DNG muszą obsługiwać wszystkie możliwe orientacje, w tym orientacje lustrzane.

## Funkcje w najnowszej wersji DNG

Wersja DNG 1.4 z października 2012 r. zawiera następujące zaawansowane funkcje.

* Domyślne przycinanie użytkownika
* Przejrzystość
* Zmiennoprzecinkowy (HDR)
* Kompresja stratna
* Pełnomocnicy

## Bibliografia ##

* [Specyfikacje DNG — firma Adobe](https://www.kronometric.org/phot/processing/DNG/dng_spec_1.4.0.0.pdf)
* [Cyfrowy negatyw – Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG — publiczny format archiwalny nieprzetworzonych danych z aparatu cyfrowego](https://helpx.adobe.com/photoshop/digital-negative.html)

