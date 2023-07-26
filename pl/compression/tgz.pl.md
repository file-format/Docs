{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik TGZ - spakowany plik tar",
  "description":"Poznaj format pliku TGZ i interfejsy API, które mogą tworzyć i otwierać pliki TGZ.",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-02"
}

## Czym jest plik TGZ?

Plik z rozszerzeniem .tgz to plik archiwum TAR, składający się z wielu plików i folderów, który został skompresowany przy użyciu oprogramowania do kompresji Gnu Zip (gzip). Plik [TAR](/pl/compression/tar/) zwykle łączy wiele plików w jeden plik do tworzenia kopii zapasowych lub dystrybucji przez Internet. Jest to plik rozpakowywany, dopóki nie zostanie skompresowany za pomocą oprogramowania gzip, po czym staje się plikiem TGZ. Pliki TGZ, jako pliki skompresowane, zajmują mniej miejsca na dysku i można je łatwo przenosić za pośrednictwem Internetu za pośrednictwem poczty e-mail. Niektóre aplikacje, które mogą otwierać pliki TGZ, to WinZip, Apple Archive Utility, 7-Zip i WinRAR. Pliki TGZ są najczęściej używane w systemach UNIX i Linux.

## Format pliku TGZ

Pliki TGZ są zapisywane jako skompresowane pliki binarne przy użyciu algorytmu kompresji [GZ](/pl/compression/gz/).

## Jak rozpakować plik .tgz w systemie Linux

W systemie operacyjnym Linux/Unix do rozpakowania plików TGZ z wiersza poleceń można użyć następującego polecenia.

```
tar zxvf tgzCompressedFile.tgz
```

Powyższe polecenie dekompresuje skompresowany plik TGZ i rozpakowuje jego pliki z archiwum TAR na dysk.
## Bibliografia ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

