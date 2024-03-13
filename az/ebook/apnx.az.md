{
  "date": "2021-03-11",
  "keywords": [
"APNX",
"Amazon Səhifə Nömrəsi İndeksi",
"uzadılması",
"fayl",
"format",
"elektron kitab",
"Amazon Kindle"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Amazon APNX fayl formatı və APNX fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "APNX - Amazon Səhifə Nömrəsi İndeksi",
  "linktitle": "APNX",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-apn-azx"
}
},
  "lastmod": "2021-05-28"
}

## APNX faylı nədir? ##

.apnx uzantısından istifadə edən Amazon Səhifə Nömrəsi İndeksi faylı e-kitab fayl növüdür; Amazon Kindle tərəfindən istifadə olunur. Bu fayllar əslində Kindle cihazları tərəfindən istifadə edilən səhifələşdirmə faylları kimi tanınır. Beləliklə, APNX faylları adətən Kindle elektron kitablarının səhifələrini qeyd etmək üçün yaradılır. Səhifələndirmə funksiyası Amazon Kindle cihazlarında 3.1 proqram təminatından bəri işə salınıb. O, səhifə indeksləri üçün APNX faylına baxır və sonra onu orijinal çap kitabındakı səhifə nömrələri ilə əlaqələndirir. Bu fayllar Amazon eBooks faylları ilə birlikdə Kindle cihazlarında saxlanılır. Siz APNX fayllarını aça və ya redaktə edə bilməzsiniz.

## APNX Fayl Formatının Xüsusiyyətləri ##

### Layout

|bayt| məzmun| şərhlər|
---|---|---|
|4 |00010001 | Format identifikatoru. 65537 az-endian dəyəri.|
|4 |növbəti | başlanğıcı Birinci başlığın bitdiyi yerdən sonra ofset. Başlıq məlumatının yeni ardıcıllığını başlayır|
|4 |uzunluq| İlk başlığın uzunluğu|
|N |ilk başlıq | Məzmun başlığını ehtiva edən sətir. Növbəti ardıcıllıqla başlayır|
|2 |naməlum | Həmişə 1|
|2 |uzunluğu | İkinci başlığın uzunluğu|
|2 |səhifələrin sayı | Səhifələri təmsil edən ikinci başlıqdan sonra ümumi bayt sayı. Bu ümumiyə pageMap.| tərəfindən nəzərə alınmayan baytlar daxildir
|2 |naməlum | Həmişə 32|
|N |ikinci başlıq | Səhifənin xəritələşdirilməsi başlığını ehtiva edən sətir|
|4*N |doldurma | Səhifənin xəritələşdirilməsi başlığında verilən ilk rəqəm 0 baytın sayını göstərir.|
|4*N |səhifə siyahısı ||

### Məzmun Başlığı

Məzmun başlığı açar, dəyər cütlərini ehtiva edən {} sətirinə daxil edilmiş sətirdən ibarətdir:

|məzmun| şərhlər|
---|---|
|contentGuid| Bələdçi.|
|asin | Kitabın Kindle versiyası üçün Amazon identifikatoru.|
|cdeType | MOBI cdeType. Elektron kitablar üçün həmişə EBOK olmalıdır.|
|fileRevisionId | Bu faylın yenidən nəzərdən keçirilməsi.|

#### Nümunə
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Səhifə Xəritəçəkmə Başlığı
Səhifənin xəritələşdirilməsi başlığı açar, dəyər cütlərini ehtiva edən {} sətrinə daxil edilmiş sətirdən ibarətdir.

|məzmun | şərhlər|
---|---|
|asin | Səhifələr uyğun gələn kağız kitab üçün ISBN 10|
|pageMap| Üç dəyər dəsti. Belə görünür: (N, N, N)\
1) Səhifə nömrələmə ardıcıllığını başlayan başlıqdan sonra baytların sayı\
2) naməlum\
3) naməlum\|
#### Nümunə
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Səhifə siyahısı

Səhifə siyahısı xam HTML-də ofsetlər ardıcıllığıdır. Hər biri
dəyər yeni səhifənin başlanğıcıdır. Hər giriş 4 bayt böyük endiandır
int.



## İstinadlar

* [Amazon APNX fayl formatı](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)

* [APNX - MobileRead Wiki tərəfindən](https://wiki.mobileread.com/wiki/APNX)


