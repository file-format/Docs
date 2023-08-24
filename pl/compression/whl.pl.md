{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku WHL - plik pakietu Python Wheel",
  "description":"Poznaj format pliku WHL i interfejsy API, które mogą tworzyć i otwierać pliki WHL.",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## Czym jest plik WHL?

Plik WHL (Wheel) to plik pakietu dystrybucyjnego zapisany w formacie koła Pythona. Jest to instalacja w standardowym formacie dystrybucji Pythona i zawiera wszystkie pliki i metadane wymagane do instalacji. Plik WHL zawiera również informacje o wersjach Pythona i platformach obsługiwanych przez ten plik koła. Podobnie jak plik instalacyjny [MSI](/pl/executable/msi/), format pliku WHL jest formatem gotowym do zainstalowania, który umożliwia uruchomienie pakietu instalacyjnego bez budowania dystrybucji źródłowej.

## Format pliku WHL

Format pliku WHL to archiwum [ZIP](/pl/compression/zip/) (.zip), które zawiera wszystkie pliki instalacyjne i metadane wymagane przez instalatorów do instalacji pakietu. Te pliki WHL można wyodrębnić za pomocą opcji rozpakowania lub standardowych aplikacji do dekompresji, takich jak WinZIP i WinRAR.

### Konwencja nazw plików WHL

Plik WHL jest nazywany zgodnie z następującą konwencją.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

Przykładowa nazwa pliku WHL jest następująca.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* `kryptografia` to nazwa pakietu.
* `2.9.2` to pakietowa wersja kryptografii. Wersja to ciąg zgodny z PEP 440, taki jak 2.9.2, 3.4 lub 3.9.0.a3.
* `cp35` to tag Pythona i oznacza implementację Pythona oraz wersję wymaganą przez koło.
* `abi3` to znacznik ABI. ABI oznacza binarny interfejs aplikacji.
* `macosx_10_9_x86_64` to tag platformy, który jest całkiem spory.

## Bibliografia

* [Czym są Python Wheels i dlaczego warto się tym przejmować?](https://realpython.com/python-wheels/)
* [Koło Pythona](https://pypi.org/project/wheel/)

