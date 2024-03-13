{
  "date": "2021-04-08",
  "keywords": [
"lzma faylı",
"lzma fayl formatı",
"lzma faylı nədir",
"fayl",
"lzma misal",
"lzma fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZMA - LZMA sıxılmış fayl formatı",
  "description": "LZMA faylı və LZMA fayllarını yarada və aça bilən API nədir.",
  "linktitle": "LZMA",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lzm-aza"
}
},
  "lastmod": "2021-04-18"
}

## LZMA faylı nədir?

.lzma uzantısı olan fayl LZMA (Lempel-Ziv-Markov zəncir alqoritmi) sıxılma metodu ilə yaradılmış sıxılmış arxiv faylıdır. Bunlar əsasən Unix əməliyyat sistemində tapılır/istifadə olunur və fayl ölçüsünü minimuma endirmək üçün [ZIP](/compression/zip/) kimi digər sıxılma alqoritmlərinə bənzəyir. LZMA köhnə fayl formatıdır və .xz formatı ilə əvəz olunur. .lzma formatının MIME növü \`application/x-lzma'dır. Bu fayl formatı LZMA SDK-da istifadə üçün İqor Pavlov tərəfindən hazırlanmışdır.

## LZMA fayl formatı

LZMA faylı iki əsas hissədən ibarətdir:

 1. Başlıq
 1. Sıxılmış Məlumat


### LZMA Başlığı

LZMA fayllarının 13 baytlıq başlığı var, ondan sonra LZMA sıxılmış məlumatı var. LZMA başlığı aşağıdakılardan ibarətdir:

 * Xüsusiyyətlər
 * Lüğət ölçüsü
 * Sıxılmamış Ölçü

#### LZMA Başlıq Xüsusiyyətləri

Xüsusiyyətlər sahəsi üç xüsusiyyətdən ibarətdir. Mötərizədə abbreviatura verilir, ondan sonra əmlakın dəyər diapazonu verilir. Sahəsi ibarətdir

1) hərfi kontekst bitlərinin sayı (lc, [0, 8]);
2) hərfi mövqe bitlərinin sayı (lp, [0, 4]); və
3) mövqe bitlərinin sayı (pb, [0, 4]).

#### LZMA Lüğət Ölçüsü

Bu, 2^n və 2^n + 2^(n-1) arasında dəyişən qiymətlərlə işarəsiz 32-bitlik kiçik endian tam ədəd kimi saxlanılır. LZMA Utils istənilən lüğət ölçüsü ilə faylları aça bilər.

#### Sıxılmamış Ölçü
Sıxılmamış Ölçü işarəsiz 64 bitlik kiçik endian tam ədədi kimi saxlanılır. 0xFFFF_FFFF_FFFF_FFFF xüsusi dəyəri Sıxılmamış Ölçünün naməlum olduğunu göstərir. Sıxılmamış Ölçü naməlum olduqda dəyər Yük Yükün Sonu Markeri (\*) ilə təmsil olunur.

## İstinadlar

* [Lempel–Ziv–Markov chain algorithm](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)
