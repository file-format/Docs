{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku CR2 — plik obrazu Canon Raw 2",
  "description":"Poznaj format pliku CR2 i interfejsy API, które mogą tworzyć i otwierać pliki CR2.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Czym jest plik CR2?

Plik CR2 (Camera RAW 2) to plik obrazu RAW utworzony przez aparaty cyfrowe firmy Canon. Przechowuje oryginalne nieprzetworzone bezstratne dane obrazu przechwycone przez aparat. Format pliku CR2 został opracowany przez firmę Canon dla jego aparatów cyfrowych i umożliwia rejestrowanie wysokiej jakości obrazów do 14 bitów RGB. Daje to wysokiej jakości obrazy z wystarczającą ilością miejsca na przetwarzanie końcowe. Format obrazu CR2 był używany przez firmę Canon w modelach aparatów 350D, 20D i 1D. Pliki CR2 są plikami RAW i zawierają dodatkowe informacje o metadanych, takie jak informacje o aparacie, informacje o obiektywie, informacje o braketingu, balans bieli i inne ustawienia.

## Format pliku CR2

Pliki CR2 są zapisywane na karcie pamięci aparatu jako pliki binarne w zastrzeżonym formacie plików firmy Canon. Format pliku CR2 zastąpił początkowo używany format pliku CRW, a później sam został zastąpiony formatem pliku Canon RAW 3. Format pliku CR2 jest oparty na specyfikacjach [TIFF](/pl/image/tiff/), które obejmują 4 katalogi plików obrazów (IFD).

|Przesunięcie |Zawartość |Komentarz|
---|---|---|
|0x0000 |Nagłówek |zawiera kolejność bajtów, wersję i przesunięcie do obrazu RAW|
|obliczone |IFD#0 |ta część zawiera sekcję Exif, która zawiera sekcję Makernotes.
Informacje o obrazku#0|
|obliczone |obrazek#0 |mała wersja obrazka (jedna czwarta rozmiaru oryginału), skompresowana w Jpeg|
|obliczone |IFD#1 |Informacje o obrazku#1.|
|obliczone |zdjęcie#1 |mała wersja obrazka, skompresowana w Jpeg|
|obliczone |IFD#2 |Informacje o obrazku#2.|
|obliczony |obrazek#2 |mała wersja obrazka, nieskompresowana|
|w nagłówku| IFD#3| Informacje o zdjęciu nr 3, pełnowymiarowym obrazie RAW|
|obliczone |zdjęcie#3 |Dane obrazu RAW, bezstratnie skompresowane w formacie Jpeg (nie dane RGB!)|

## Zaleta formatu pliku CR2

Przechowywanie zdjęć w formacie RAW pozwala na dużą obróbkę zdjęcia, np. dostosowanie balansu bieli. Jest to o wiele trudniejsze i wiąże się z dużą utratą jakości w przypadku innych formatów plików graficznych, takich jak [JPEG](/pl/image/jpeg/).

## Czy CR2 jest lepszy niż JPEG?

Pliki CR2 to surowe pliki bez utraty danych, a tym samym bez utraty jakości. Z drugiej strony JPEG to stratny format pliku obrazu, ponieważ traci niektóre dane w celu zmniejszenia pliku. Dzięki temu pliki CR2 są wysokiej jakości i lepiej nadają się do retuszu i ulepszeń.

## Bibliografia

* [Format pliku CR2](http://lclevy.free.fr/cr2/)

