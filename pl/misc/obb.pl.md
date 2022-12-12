{
  "date" : "2022-02-16",
  "keywords" :[ "plik obb", "format pliku obb", "co to jest plik obb", "plik", "przykład obb", "rozszerzenie pliku obb", "rozszerzenie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku OBB - nieprzezroczysty binarny plik typu Blob systemu Android",
  "description":"Poznaj format pliku OBB i interfejsy API, które mogą tworzyć i otwierać pliki OBB.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## Czym jest plik OBB?

Plik OBB to plik rozszerzenia, który zawiera dodatkowe dane oprócz pliku Android [APK](/pl/compression/apk/). Sklep Google Play nie zezwala na posiadanie pliku APK Androida o rozmiarze większym niż 100 MB. Jednak niektóre aplikacje mogą wymagać hostowania grafiki w wysokiej rozdzielczości, plików multimedialnych lub innych dużych zasobów oprócz plików APK. W tym miejscu pojawiają się typy plików OBB. Google Play pozwala dołączyć te pliki rozszerzeń jako uzupełnienie pliku APK.

## Format pliku OBB

Pliki OBB są zapisywane jako pliki binarne wraz z plikami APK. Gdy plik APK jest dołączony do plików OBB, Google Play przechowuje pliki rozszerzeń na swoim serwerze i programista nie jest obciążany żadnymi dodatkowymi kosztami. Te dodatkowe pliki są przechowywane we współdzielonej pamięci urządzenia na karcie SD lub partycji USB, gdy aplikacja jest pobierana do instalacji.

Pliki OBB są pobierane i instalowane podczas pobierania. Ale w niektórych przypadkach są one pobierane do instalacji, gdy aplikacja jest uruchamiana po raz pierwszy.

### Maksymalny rozmiar pliku OBB

Sklep Google Play umożliwia przesyłanie plików rozszerzeń OBB o rozmiarze do 2 GB. Zaleca się przesyłanie plików o dużych rozmiarach jako skompresowanych plików [ZIP](/pl/compression/zip/) w celu wydajnego przesyłania przez Internet.

Te pliki rozszerzeń mogą być hostowane jako **główny** podstawowy plik rozszerzenia dla dodatkowych zasobów wymaganych przez aplikację lub jako opcjonalny plik rozszerzenia poprawki przeznaczony do niewielkich aktualizacji głównego pliku rozszerzenia.

## Bibliografia

* [Programiści Androida - pliki rozszerzeń](https://developer.android.com/google/play/expansion-files)

