{
  "date" : "2021-04-08",
  "keywords" :["plik dar", "format pliku dar", "co to jest plik dar", "plik", "przykład dar", "rozszerzenie pliku dar", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - Format pliku archiwizatora dysku",
  "description":"Poznaj format pliku DAR i interfejsy API, które mogą tworzyć i otwierać pliki DAR.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Czym jest plik DAR?

Plik z rozszerzeniem .dar to skompresowane archiwum utworzone przy użyciu archiwum DAR Disk. Może tworzyć kopie zapasowe/archiwum dla całego dysku lub grupy plików. Został stworzony w celu zastąpienia formatu plików [TAR](/pl/compression/tar/) w systemie operacyjnym UNIX i może być tworzony jako podzielone pliki archiwów dla dużej liczby plików. Archiwum DAR obsługuje opcję usuwania z systemu plików powiązanych z głównymi plikami w archiwum. Jego możliwości tworzenia różnicowych, przyrostowych i dekrementalnych kopii zapasowych sprawiają, że jest lepszy niż pliki TAR.

## Format pliku DAR

Pliki DAR to skompresowane archiwa, które mogą wykorzystywać dowolną kompresję poszczególnych plików, taką jak [gzip](/pl/compression/gz/), [bzip2](/pl/compression/bz2/), lzo, xz lub lzma. Dokładny format pliku DAR zależy od rodzaju formatowania używanego do kompresji zawartości archiwum. Umożliwia również opcjonalne szyfrowanie Blowfish, Twofish, AES, Serpent, Camellia oraz szyfrowanie i podpis klucza publicznego (OpenPGP).

### Funkcje DAR

Niektóre funkcje formatu pliku DAR są następujące.

* Dba o każdy typ i-węzła (katalog, zwykłe pliki, dowiązania symboliczne, urządzenia specjalne, nazwane potoki, gniazda, drzwi, ...)
* Dba o twarde i-węzły (zwykłe pliki z twardymi linkami, urządzenia char, urządzenia blokowe, dowiązania symboliczne z twardymi linkami)
* Dba o rzadkie pliki
* Dba o plik Linux Extended Attributes,
* Dba o plik Linux ACL
* Dba o rozwidlenia plików Mac OS X
* Dba o niektóre atrybuty specyficzne dla systemu plików, takie jak data urodzenia systemu plików HFS+ i niezmienne, rejestrowanie danych, bezpieczne usuwanie, nieusuwalne, nieusuwalne atrybuty systemu plików ext2/3/4.
* Kompresja poszczególnych plików za pomocą gzip, bzip2, lzo, xz lub lzma (w przeciwieństwie do kompresji całego archiwum). Osoba fizyczna może zrezygnować z kompresji już skompresowanych plików na podstawie sufiksu nazwy pliku.
* Szybkie rozpakowywanie plików z dowolnego miejsca w archiwum
* Szybkie zestawienie zawartości archiwum poprzez zapisanie katalogu plików w archiwum
* Kopia zapasowa systemu plików na żywo: wykrywa, kiedy plik został zmodyfikowany podczas odczytu w celu wykonania kopii zapasowej i może ponowić próbę zapisywania go do określonej maksymalnej liczby ponownych prób
* Plik skrótu (MD5, SHA1 lub SHA-512) generowany w locie dla każdego wycinka, wynikowy plik jest zgodny z md5sum lub sha1sum, aby móc szybko sprawdzić integralność każdego wycinka
* Niezależny od systemu plików: może być użyty do przywrócenia systemu na partycję o innym rozmiarze i/lub na partycję z innym systemem plików[5]

## Bibliografia

* [DAR](http://dar.linux.free.fr/)
* [Archiwizator dysku DAR](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

