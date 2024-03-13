{
  "date": "2021-07-29",
  "keywords": [
"md5 faylı",
"md5 fayl formatı",
"md5 faylı nədir",
"fayl",
"md5 nümunəsi",
"md5 fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MD5 - MD5 Checksum faylı",
  "description": "MD5 faylları və MD5 fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "MD5",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-md-az5"
}
},
  "lastmod": "2021-07-29"
}

## MD5 faylı nədir?

MD5 faylı faylın bütövlüyünü yoxlamaq üçün istifadə edilən yoxlama faylıdır. O, əlaqəli fayl üçün barmaq izinə bənzəyir və fayldakı bitlərin sayından istifadə edən alqoritmdən istifadə edərək unikal şəkildə yaradılır. O, faylı [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html) kimi proqram təminatı ilə yoxlamaq üçün istifadə olunur. MD5 fayllarından istifadənin bir üstünlüyü endirilmiş faylların zədələnmədiyini yoxlamaqdır.

## MD5 Fayl Format - Ətraflı Məlumat

Adətən MD5 faylı orijinal fayl adı ilə eyni adla, lakin .md5 uzantısı ilə saxlanılır. Məsələn, əlaqəli fayl adı `abc_987_123456.grb` olarsa, müvafiq MD5 fayl adı `abc_987_123456.grb.md5` olacaq. MD5 faylları qəbul edilmiş və ya endirilmiş faylın zədələnmədiyini və ya zərərli məzmunun təsirinə məruz qalmadığını müəyyən etməyə kömək edir. Bir sözlə, MD5 faylları faylın tamlığına zəmanət verir.


## MD5 Checksumunu necə yoxlamaq olar?

Tək faylı aşağıdakı kimi [md5sum](https://en.wikipedia.org/wiki/Md5sum) alətindən istifadə etməklə MD5 üçün yoxlamaq/təsdiq etmək olar.

```
md5sum -c abc_987_123456.grb.md5
```

## İstinadlar

* [md5sum - Vikipediya](https://en.wikipedia.org/wiki/Md5sum)


