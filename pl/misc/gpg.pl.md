{
  "date" : "2022-02-17",
  "keywords" :["plik gpg", "format pliku gpg", "co to jest plik gpg", "plik", "przykład gpg", "rozszerzenie pliku gpg", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik GPG - Publiczny plik kluczy GNU Privacy Guard",
  "description":"Dowiedz się o plikach GPG i interfejsach API, które mogą tworzyć i otwierać pliki GPG.",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## Czym jest plik GPG?

Plik GPG to plik klucza szyfrowania/deszyfrowania używany przez program szyfrujący GNU Privacy Guard (GnuPG). Sam program GnuPC jest oparty na standardzie OpenPGP zgodnie z definicją RFC4880 i jest również znany jako PGP. Kluczem do pomyślnego wykorzystania GPG w nowoczesnym systemie operacyjnym jest jego wszechstronny system zarządzania kluczami. Narzędzie wiersza poleceń GPG umożliwia łatwą integrację z innymi aplikacjami.

## Format pliku GPG

Pliki GPG są zapisywane jako zaszyfrowane pliki binarne i oczywiście nie są czytelne dla człowieka. Aby odszyfrować zaszyfrowany plik GPG, musisz użyć tego samego bezpiecznego klucza. I dlatego wewnętrzny format plików tych plików nie jest znany.

## Szyfruj i odszyfruj pliki za pomocą GPG w systemie Linux

Narzędzie wiersza poleceń GPG może służyć do szyfrowania i odszyfrowywania plików w systemie Linux.

### Szyfrowanie pliku

Plik można zaszyfrować za pomocą polecenia gpg z opcją -c (tworzenie), jak pokazano poniżej.

```
gpg -c file1.txt
```
Uruchomienie tego polecenia wymaga podania frazy kluczowej, za pomocą której ma zostać zaszyfrowana zawartość oryginalnego pliku `file1.txt`. Powoduje to utworzenie zaszyfrowanego pliku file1.txt.gpg.

### Odszyfrowywanie i wyodrębnianie pliku

Aby odszyfrować i wyodrębnić zaszyfrowany plik, można użyć następującego polecenia.

```
gpg cfile.txt.gpg
```

## Bibliografia

* [GNUPG](https://gnupg.org/)
* [HDF – Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

