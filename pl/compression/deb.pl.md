{
  "date" : "2021-04-08",
  "keywords" :["plik deb", "format pliku deb", "co to jest plik deb", "plik", "przykład deb", "rozszerzenie pliku deb", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - skompresowane archiwum tar Bzip",
  "description":"Poznaj format pliku DEB i interfejsy API, które mogą tworzyć i otwierać pliki DEB.",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Czym jest plik DEB?

Plik z rozszerzeniem .deb to format pliku pakietu binarnego Debiana dostępny do dystrybucji pakietów oprogramowania w systemie operacyjnym Linux. Składa się z dwóch plików archiwum [TAR](/pl/compression/tar/). DPKG zapewnia mechanizm odczytu i instalacji pakietów DEB. Pakiety DEB można instalować za pomocą interfejsu zarządzania pakietami oprogramowania APT. Pliki DEB mają Internet Media Type jako `application/vnd.debian.binary-package`.

## Format pliku DEB

Plik DEB składa się z dwóch plików archiwum [TAR](/pl/compression/tar/). Jedno archiwum zawiera informacje sterujące, a drugie zawiera dane do zainstalowania.

### Organizacja pakietu

Plik DEB to plik archiwum **ar**, który ma magiczną wartość `!<arch> `. Od Debiana 0.93 mechanizm archiwizacji plików DEB zawiera trzy pliki w określonej kolejności.

1. `Debian Binary` - Przeznaczeniem jest seria linii oddzielonych znakami nowej linii. Obecnie dostępna jest tylko jedna linia opisująca numer wersji. Bieżący numer wersji to 2.0.
1. `Archiwum kontrolne` — zawiera archiwum control.tar, które zawiera skrypty opiekuna i metainformacje o pakiecie, takie jak nazwa pakietu, wersja, zależności i opiekun.
1. `Archiwum danych` — jest to archiwum tar o nazwie data.tar i zawiera rzeczywiste instalowalne pliki multimedialne. Archiwum można skompresować za pomocą gz, bz2, lzma lub xz, a rozszerzenie pliku archiwum danych odpowiednio się zmienia.

### Archiwum kontrolne

Archiwum kontrolne może zawierać następującą zawartość.

* `control` - Zawiera krótki opis pakietu oraz inne informacje takie jak jego zależności.
* `md5sums` - Zawiera sumy kontrolne MD5 wszystkich plików w paczce w celu wykrycia uszkodzonych lub niekompletnych plików.
* `conffiles` - Wyświetla listę plików pakietu, które powinny być traktowane jako pliki konfiguracyjne. Pliki konfiguracyjne nie są zastępowane podczas aktualizacji, chyba że określono inaczej.
* `preinst`, postinst, prerm i postrm - Opcjonalne skrypty wykonywane przed lub po instalacji lub usunięciu pakietu
* `config` to opcjonalny skrypt obsługujący mechanizm konfiguracyjny debconf.
* `shlibs` - Jest to lista współdzielonych zależności bibliotek.

## Bibliografia

* [DEB - Wikipedia](https://en.wikipedia.org/wiki/Deb_(file_format))
* [Format pakietu binarnego Debiana](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

