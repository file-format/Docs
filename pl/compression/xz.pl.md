{
  "date" : "2022-01-23",
  "keywords" :["plik xz", "format pliku", "co to jest plik xz", "plik", "przykład xz", "rozszerzenie pliku xz", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik XZ - skompresowane archiwum XZ",
  "description":"Poznaj format pliku XZ i interfejsy API, które mogą tworzyć i otwierać pliki XZ.",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## Czym jest plik XZ?

XZ to skompresowany format pliku, który wykorzystuje algorytm kompresji LZMA2. Został zaprojektowany jako zamiennik popularnych formatów gzip i bzip2 i oferuje szereg zalet w stosunku do tych starszych standardów. Pliki XZ są dobrze obsługiwane na wielu platformach i można je szybko i łatwo dekompresować. Chociaż nie są tak powszechne jak pliki [ZIP](/pl/compression/zip/) lub [RAR](/pl/compression/rar/), archiwa XZ mogą być używane do przechowywania dużych ilości danych bez utraty jakości kompresji. Jeśli potrzebujesz skompresować lub zdekompresować duże pliki, warto rozważyć rozszerzenie pliku XZ.

## Format pliku XZ

Plik XZ jest generowany i zapisywany jako pliki binarne na dysku. Wykorzystuje algorytm LZMA do kompresji danych i może osiągnąć współczynnik kompresji do 50%. Pliki XZ są zwykle używane do dystrybucji oprogramowania i archiwów kopii zapasowych. Można je zdekompresować za pomocą narzędzia XZ, które jest zawarte w większości dystrybucji Linuksa.

## Rozpakuj pliki XZ w systemie Linux/Unix

Aby rozpakować pliki XZ, najpierw zainstaluj pakiet `xz-utils`:
```
$ sudo apt-get install xz-utils
```

Użyj polecenia `unxz`, aby wyodrębnić pliki .xz:
```
$ unxz compressed_xz_file.xz
```

lub używając z opcją --decompress XZ:
```
$ xz --decompress compressed_xz_file.xz
```

## Bibliografia

* [Narzędzia XZ](https://en.wikipedia.org/wiki/XZ_Utils)

