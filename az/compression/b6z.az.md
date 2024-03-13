{
  "date": "2019-10-11",
  "keywords": [
"b6z faylı",
"b6z fayl formatı",
"b6z faylı nədir",
"fayl",
"b6z nümunəsi",
"b6z fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "B6Z - B6ZIP Arxiv Fayl Format",
  "description": "B6Z faylları yarada və aça bilən B6Z fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "B6Z",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-b6-azz"
}
},
  "lastmod": "2021-04-05"
}

## B6Z faylı nədir?

.b6z uzantısı olan fayl, faylları sıxmaq və açmaq üçün istifadə edilən macOS proqram proqramı [B6Zip](http://b6zip.com) yaradılmış sıxılmış arxiv faylıdır. Bu, daha yüksək sıxılma nisbətinə imkan verən nisbətən yeni arxiv formatıdır. B6Z açıq arxitekturaya malikdir və 900000 PB-ə qədər fayl ölçülərini dəstəkləyir. O, məlumatların sıxılmasını, səhvlərin bərpasını və faylların yayılmasını dəstəkləyir. B6Zip yardım proqramı, B6Z daxil olmaqla müxtəlif növ sıxılmış faylları açmaq üçün MacOS-da pulsuz olaraq mövcuddur.

## B6Z fayl formatı

B6Z fayl formatı açıq arxitekturaya əsaslanır və AES-256 şifrələmə alqoritmi ilə möhkəm sıxılma təmin edir. Standart sıxılma metodu kimi LZMA2-dən istifadə edir, eyni zamanda aşağıdakı kimi digər sıxılma üsullarını dəstəkləyir.

|Metod|Təsvir|
---|---|
|LZMA |LZ77 alqoritminin optimallaşdırılmış versiyası|
|LZMA2| LZMA|-nın təkmilləşdirilmiş versiyası
|Deflate| Adi LZ77 alqoritmi|
|BZip2| Standart BWT alqoritmi|
|PPMD| Dmitri Şkarinin PPMdH|

B6Zip yardım proqramı bütün bu sıxılma standartlarını dəstəkləyir və yüksək sürətlə nəticələnən yüksək optimallaşdırılmışdır. O, [ZIP](/compression/zip/), [TAR](/compression/tar/) və [RAR](/compression/rar/) fayl formatları ilə işləməyi dəstəkləyir. B6Z fayllarında MIME tipli proqram/x-b6z-sıxılmışdır.

## İstinadlar

* [B6Zip](http://b6zip.com)


