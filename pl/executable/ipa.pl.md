{
  "date" : "2021-08-30",
  "keywords" :["plik ipa", "format pliku ipa", "co to jest plik ipa", "plik", "przykład ipa", "rozszerzenie pliku ipa","rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format plików IPA i interfejsy API, które mogą tworzyć i otwierać pliki IPA.",
  "title" :"IPA - plik pakietu aplikacji iOS",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## Czym jest plik IPA?
Plik z rozszerzeniem .ipa należy do systemu iOS i jest znany jako plik pakietu aplikacji. Jest to plik archiwum (skompresowany przy użyciu kompresji [ZIP](/pl/compression/zip/)), który przechowuje aplikację iOS, ale tę aplikację można zainstalować tylko na urządzeniach z systemem MacOS opartych na systemie iOS lub ARM, takich jak iPad, iPhone lub iPoda Touch. Do instalowania plików IPA można używać głównie iTunes, Apple Configurator 2 lub oprogramowania innych firm.

## Format pliku IPA
Deweloperzy IOS, którzy opracowują aplikacje przy użyciu Apple Xcode, dobrze znają pliki IPA, ponieważ muszą pakować opracowane aplikacje jako pliki IPA w celu testowania wdrażania w sklepie z aplikacjami. Chociaż wiadomo, że pliki IPA są instalowane jako aplikacje na iOS, można je również rozpakować, aby wyświetlić zawarte dane aplikacji. Ponieważ plik IPA zawiera tylko jeden plik binarny dla architektury ARM telefonów komórkowych i nie zawiera pliku binarnego dla architektury x86, wielu plików .ipa nie można zainstalować w symulatorze iPhone'a.
### Struktura pliku .ipa
Poniższy przykład przedstawia strukturę IPA:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Powyżej przedstawiono wbudowaną strukturę rozpoznawaną przez iTunes i App Store. Zgodnie z tą strukturą:
- Katalog Payload zawiera wszystkie dane aplikacji.
- Plik iTunes Artwork to obraz PNG o wymiarach 512 x 512 pikseli, zawierający ikonę aplikacji do wyświetlania w iTunes i aplikacji App Store na iPadzie.
- Plik iTunesMetadata.plist zawiera różne informacje, począwszy od nazwy i identyfikatora programisty, informacji o prawach autorskich, identyfikatora pakietu, nazwy aplikacji, gatunku, daty wydania, daty zakupu itp.
- Folder META-INF zawiera tylko metadane dotyczące tego, jakiego programu użyto do utworzenia IPA.


## Bibliografia

* [.ipa – z Wikipedii](https://en.wikipedia.org/wiki/.ipa)


