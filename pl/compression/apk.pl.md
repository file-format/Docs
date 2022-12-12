{
  "date" : "2019-10-11",
  "keywords" :[ "plik apk", "format pliku apk", "co to jest plik apk", "plik", "przykład apk", "rozszerzenie pliku apk", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK - Co to jest plik APK?",
  "description":"Dowiedz się, co to jest plik APK i interfejsy API, które mogą tworzyć i otwierać pliki APK.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## Co to jest plik APK?

Plik z rozszerzeniem .apk to plik aplikacji Google na Androida, który służy do instalowania aplikacji (aplikacji) na urządzeniach z Androidem. Jest tworzony jako plik wykonywalny przy użyciu oficjalnego środowiska IDE Google Android Studio i jest przesyłany do sklepu Google Play w celu pobrania i zainstalowania przez użytkowników końcowych. Pliki APK można generować i udostępniać do ręcznej instalacji, a także przed opublikowaniem w sklepie Google Play. Pomaga to w testowaniu funkcjonalności i zachowania wygenerowanego pliku pakietu APK. Dlatego należy mieć pewność, że plik APK pochodzi z zaufanego źródła i nie zawiera złośliwego oprogramowania.

## Format pliku APK

Pliki APK są spakowane jako skompresowane w formacie pliku [ZIP](/pl/compression/zip/), który można otworzyć za pomocą dowolnego oprogramowania do otwierania plików ZIP. Rozszerzenie .apk takiego pliku można zmienić na .zip i otworzyć plik w dowolnej aplikacji ZIP lub rozpakować jego zawartość.

## Zawartość pakietu APK

Pojedynczy plik APK zawiera wszystkie niezbędne pliki, które są wymagane do jego instalacji i wykonania. Plik APK rozpakowany za pomocą aplikacji ZIP zawiera następujące pliki i foldery.

* `META-INF/`: Katalog zawierający plik manifestu, sygnaturę i listę zasobów w archiwum
* `lib/`: Katalog zawierający skompilowany kod związany z określonymi platformami, takimi jak armeabi-v7a, x86, arm64-v8a itp.
* `res/`: Katalog zawierający nieskompilowane zasoby, takie jak obrazy
* `assets/`: Katalog zawierający zasoby aplikacji, które mogą być pobierane przez AssetManager.
* `androidManifest.xml`: zawiera nazwę, informacje o wersji i zawartość pliku APK
* `classes.dex`: Są to skompilowane klasy Java, które mogą być uruchamiane na maszynie wirtualnej Dalvik i przez Android Runtime
* `resources.arsc`: Skompilowany plik zasobów, taki jak ciągi znaków

## Jak zainstalować plik APK na urządzeniu z Androidem?

Aby zainstalować plik APK na urządzeniach z Androidem, można wykonać następujące czynności.

1. Pobierz APK za pomocą przeglądarki internetowej
2. Stuknij go – powinieneś zobaczyć, jak się pobiera na górnym pasku urządzenia
3. Po pobraniu otwórz Pobieranie, dotknij pliku APK i dotknij Tak po wyświetleniu monitu.

Wykonanie tych kroków rozpocznie instalację aplikacji na Twoim urządzeniu.

## Bibliografia

* [Format pliku APK](https://en.wikipedia.org/wiki/Android_application_package)

