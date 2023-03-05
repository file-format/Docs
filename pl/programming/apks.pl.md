
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik APKS - Archiwum zestawu APK",
  "description":"Dowiedz się, co to jest plik APKS?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Co to jest plik APKS?

Plik z rozszerzeniem .apks to plik archiwum będący zbiorem plików pakietu Android **APK**. Każdy pojedynczy plik APK w pliku APKS jest generowany z uwzględnieniem różnych aspektów urządzeń. Obejmują one architekturę, język, gęstość ekranu i inne funkcje urządzenia. Pliki APKS są generowane przez **bundletool**. Służy do tworzenia pakietu aplikacji na Androida i konwertowania pakietu aplikacji na różne pliki APK do wdrożenia na urządzeniach.

## Format pliku APKS — więcej informacji

Pliki APKS są zapisywane jako pliki skompresowane przy użyciu formatu pliku [ZIP](/pl/compression/zip/).

## Jak wygenerować plik APKS?

Gdy pakiet Android App Bundle (AAB) jest gotowy, jego zachowanie w sklepie Google Play można przetestować pod kątem wdrożenia na urządzeniu. Pliki APKS można w tym celu generować z plików AAB i instalować na urządzeniach testowych za pomocą Google Android [bundletool](https://developer.android.com/studio/command-line/bundletool). Zapewnia narzędzia wiersza poleceń do tworzenia pliku archiwum APKS z plików APK za pomocą następującego polecenia.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Aby wdrożyć pliki APK na urządzeniu, plik APKS można podpisać za pomocą informacji o podpisaniu urządzenia w następujący sposób.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Bibliografia

* [bundletool - wiersz poleceń](https://developer.android.com/studio/command-line/bundletool)

