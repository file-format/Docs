{
  "date": "2022-01-23",
  "keywords": [
"xz faylı",
"fayl formatı",
"xz faylı nədir",
"fayl",
"xz misal",
"xz fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XZ Faylı - XZ Sıxılmış Arxivi",
  "description": "XZ faylları yarada və aça bilən XZ fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "XZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-x-azz"
}
},
  "lastmod": "2022-01-23"
}

## XZ faylı nədir?

XZ, LZMA2 sıxılma alqoritmindən istifadə edən sıxılmış fayl formatıdır. O, məşhur gzip və bzip2 formatlarını əvəz etmək üçün hazırlanmışdır və bu köhnə standartlara nisbətən bir sıra üstünlüklər təklif edir. XZ faylları bir çox platformada yaxşı dəstəklənir və tez və asanlıqla açıla bilər. Onlar [ZIP](/compression/zip/) və ya [RAR](/compression/rar/) faylları qədər ümumi olmasalar da, XZ arxivləri sıxılma keyfiyyətini itirmədən böyük həcmdə məlumatların saxlanması üçün istifadə edilə bilər. Böyük faylları sıxmaq və ya açmaq lazımdırsa, XZ fayl uzantısını nəzərdən keçirməyə dəyər.

## XZ fayl formatı

XZ faylı yaradılır və ikili fayllar kimi diskdə saxlanılır. O, məlumatları sıxmaq üçün LZMA alqoritmindən istifadə edir və 50%-ə qədər sıxılma nisbətinə nail ola bilir. XZ faylları adətən proqram paylamaları və ehtiyat arxivləri üçün istifadə olunur. Əksər Linux paylamalarına daxil olan XZ yardım proqramından istifadə edərək onları açmaq olar.

## Linux/Unix-də XZ fayllarını açın

XZ fayllarını açmaq üçün əvvəlcə `xz-utils` paketini quraşdırın:
```
$ sudo apt-get install xz-utils
```

.xz fayllarını çıxarmaq üçün `unxz` əmrindən istifadə edin:
```
$ unxz compressed_xz_file.xz
```

və ya XZ-nin --decompress seçimi ilə istifadə edin:
```
$ xz --decompress compressed_xz_file.xz
```

## İstinadlar

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)


