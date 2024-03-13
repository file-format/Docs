{
  "date": "2021-04-08",
  "keywords": [
"lz faylı",
"lz fayl formatı",
"lz faylı nədir",
"fayl",
"lz misal",
"lz fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZ - Lzip sıxılmış fayl formatı",
  "description": "LZ faylları yarada və aça bilən LZ fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "LZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-l-azz"
}
},
  "lastmod": "2021-04-19"
}

## LZ faylı nədir?

.lz uzantısı olan fayl sıxılma üçün pulsuz əmr xətti aləti olan Lzip ilə yaradılmış sıxılmış arxiv faylıdır. Dəstək fayllarını sıxışdırmaq üçün birləşməni dəstəkləyir. LZ faylları media tipli proqram/lzip-ə malikdir və [BZ2](/compression/bz2/) ilə müqayisədə daha yüksək sıxılma nisbətlərini dəstəkləyir. LZ LZMA (Lempel-Ziv-Markov zənciri) alqoritminə əsaslanır və faylın bütövlüyünü yoxlamaq üçün 32 bitlik CRC yoxlama cəmi və identifikator baytları ehtiva edir.

## LZMA Sıxılmış Format

LZMA sıxılmış formatı adaptiv ikili diapazon kodlayıcısı ilə kodlanan sıxılmış bit axınından ibarətdir. Axın paketlərə bölünür. Hər bir paket ya tək baytı, ya da LZ77 ardıcıllığını təsvir edir. Hər bir paketin uzunluğu və məsafəsi gizli və ya açıq şəkildə kodlanır.

Yeddi növ paket aşağıdakı kimidir ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Packed code (bit sequence)	|Packet name	|Packet description|
---|---|---|
|0 + baytkod| LIT| Adaptiv ikili diapazon kodlayıcısından istifadə edərək kodlaşdırılmış tək bayt.|
|1+0 + len + dist| MATCH| Ardıcıllığın uzunluğunu və məsafəsini təsvir edən tipik LZ77 ardıcıllığı.|
|1+1+0+0| QISA | Bir baytlıq LZ77 ardıcıllığı. Məsafə son istifadə olunan LZ77 məsafəsinə bərabərdir.|
|1+1+0+1 + len| LONGREP[0]| LZ77 ardıcıllığı. Məsafə son istifadə olunan LZ77 məsafəsinə bərabərdir.|
|1+1+1+0 + len| LONGREP[1]| LZ77 ardıcıllığı. Məsafə ikinci sonuncu istifadə edilən LZ77 məsafəsinə bərabərdir.|
|1+1+1+1+0 + len| LONGREP[2]| LZ77 ardıcıllığı. Məsafə üçüncü sonuncu istifadə edilən LZ77 məsafəsinə bərabərdir.|
|1+1+1+1+1 + len| LONGREP[3]| LZ77 ardıcıllığı. Məsafə dördüncü sonuncu istifadə edilən LZ77 məsafəsinə bərabərdir.|


## İstinadlar

* [LZMA - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Sıxılmış_format_baxış)

* [Lzip](https://en.wikipedia.org/wiki/Lzip)


