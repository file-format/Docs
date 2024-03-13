{
  "date": "2019-10-11",
  "keywords": [
"bz2 faylı",
"bz2 fayl formatı",
"bz2 faylı nədir",
"fayl",
"bz2 nümunəsi",
"bz2 fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BZ2 - Sıxılmış Fayl Formatı",
  "description": "BZ2 faylının və BZ2 fayllarını yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "BZ2",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-bz-az2"
}
},
  "lastmod": "2020-09-05"
}

## BZ2 faylı nədir?

BZ2, əsasən UNIX və ya Linux sistemində [BZIP2](http://www.bzip.org/) açıq mənbə sıxılma metodu ilə yaradılan sıxılmış fayllardır. Bir faylın sıxılması üçün istifadə olunur və birdən çox faylın arxivləşdirilməsi üçün nəzərdə tutulmur. Bu, birdən çox faylı bir faylda arxivləşdirən, lakin sıxılmadan eyni platformalardakı TAR fayl formatından fərqlidir. BZ2 kimi sıxılmış fayllar [WinZip](https://www.winzip.com/win/en/) kimi proqramlarla açıla bilər. BZIP2 yüksək səviyyəli sıxılma əldə etmək üçün Run-Length Encoding (RLE) və ya [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) sıxılma alqoritmindən istifadə edir.

## BZ2 File Format

Bu fayl formatı üçün heç bir rəsmi spesifikasiya yoxdur. Bununla belə, qeyri-rəsmi [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) göstərir ki, .bz2 axını sıfır və ya daha çox sıxılmış blokdan sonra gələn 4 baytlıq başlıqdan ibarətdir. Bundan dərhal sonra işlənmiş düz mətn üçün 32 bitlik CRC-dən ibarət axın sonu markeri gəlir. Sıxılmış bloklar arasında heç bir doldurma yoxdur və bütün bloklar bit hizalanır.

## BZ2 faylını açın/çıxarın

Siz WinZip kimi proqram təminatından istifadə edərək Windows və Mac OS-də BZ2 faylını aça bilərsiniz. Linux-da terminalda aşağıdakı əmr.

```
bzip2 -d filename.bz2
```

## İstinadlar

* [BZIP2 Format Xüsusiyyətləri](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)


