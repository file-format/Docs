{
  "date": "2019-12-09",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZIM Fayl Format - OpenZIM Arxiv Faylı",
  "description": "ZIM fayl formatı və ZIM faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "ZIM",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-zi-azm"
}
},
  "lastmod": "2019-12-09"
}

## ZIM faylı nədir? ##

.zim uzantılı fayllar Wiki məzmununu oflayn saxlamaq üçün yaradılmış arxivlərdir. Wikipedia-nı USB-də saxlamaq üçün ən uyğun açıq fayl formatı hesab olunur. Sayt məzmununu yığcam formatda saxlayır. Onun adı əvvəlki Zeno fayl formatı olan Zeno IMproved dən gəlir. ZIM, Wikimedia CH tərəfindən dəstəklənən və Wikimedia Fondu tərəfindən dəstəklənən [openZIM ](https://openzim.org/)layihəsi tərəfindən idarə olunur. ZIM faylları Kiwix və ZIMReader kimi proqramlar tərəfindən açıla bilər. OpenZIM layihəsi OpenSource icmasının töhfəsi üçün [Github](https://github.com/openzim) üzərində ZIM fayl formatının tətbiqinə ev sahibliyi etdi.

## ZIM Fayl Formatının Xüsusiyyətləri

ZIM fayl formatı [Zeno file format](https://openzim.org/wiki/Zeno_file_format) üzərində işlənib və geriyə uyğun deyil. ZIM fayl formatının format spesifikasiyası tərtibatçının istinadı üçün openZIM tərəfindən [available online](https://openzim.org/wiki/ZIM_file_format)-dir. OpenZIM, ZIM fayllarını oxumaq və yazmaq üçün C++ açıq mənbə tətbiqini, [LibZim](https://openzim.org/wiki/Zimlib) təmin etmişdir.

ZIM fayl formatı məzmunu yığcamlaşdırmaq üçün LZMA2 sıxılma istifadə edir.

{{< figure src="../ZIM_File_Format.jpeg" alt="ZIM fayl formatı" >}}


### ZIM Başlığı

A ZIM file starts with a header that is at offset 0. Bütün komponentlər kiçik endian əsasında qurulur və bütün tam ədədlər işarəsiz tam ədədlərdir, yəni uint_16, uint_32, uint_64.

|Sahənin Adı |Növü| Ofset| Uzunluq| Təsvir|
---|---|---|---|---|
|magicNumber| tam| 0| 4| Fayl formatını tanımaq üçün sehrli nömrə 72173914 (0x44D495A) olmalıdır|
|majorVersion| tam| 4| 2| ZIM fayl formatının əsas versiyası (5 və ya 6)|
|minorVersion| tam| 6| 2| ZIM fayl formatının kiçik versiyası|
|uuid| tam| 8| 16| bu zim faylının unikal identifikatoru|
|articleCount| tam| 24| 4| məqalələrin ümumi sayı|
|clusterCount| tam| 28| 4| klasterlərin ümumi sayı|
|urlPtrPos| tam| 32| 8| URL| ilə sıralanan kataloq göstəricilər siyahısının mövqeyi
|titlePtrPos| tam| 40| 8| Başlıq| ilə sıralanan kataloq göstəricilər siyahısının mövqeyi
|clusterPtrPos| tam| 48| 8| klaster göstəricisi siyahısının mövqeyi|
|mimeListPos| tam| 56| 8| MIME növü siyahısının mövqeyi (həmçinin başlıq ölçüsü)|
|əsas səhifə| tam| 64| 4| əsas səhifə və ya əsas səhifə yoxdursa 0xffffffff|
|layoutPage| tam| 68| 4| layout səhifəsi və ya layout səhifəsi yoxdursa 0xffffffffff|
|checksumPos| tam| 72| 8| yoxlama cəminin özü olmadan bu faylın md5checksumuna göstərici. Bu həmişə faylın sonuna 16 bayt qalmışa işarə edir.|

## İstinadlar ##

* [OpenZIM](https://openzim.org/)

* [C++ LibZim](https://openzim.org/wiki/Zimlib)


