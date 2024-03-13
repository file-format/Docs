{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"KIT fayl formatı və KIT faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title" : "KIT fayl formatı - CodeKit faylı",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit-az",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## KIT faylı nədir?

.kit uzantılı fayl [CodeKit](https://codekitapp.com/) proqramlaşdırma dili tətbiqi ilə yaradılmış HTML faylıdır. O, mövcud [HTML](/web/html/) fayllarına əlavə olaraq `import` və `dəyişənlər` ehtiva edir və bu, onu statik saytlar üçün ideal edir. CodeKit, asanlıqla statik veb-sayt faylları kimi istifadə oluna bilən KIT fayllarını HTML-yə tərtib edir.

## KIT fayl formatı

KIT faylları əlavə olaraq idxal və dəyişənləri ehtiva edən HTML fayllarıdır. Bunlar düz mətn faylları kimi saxlanılır və istənilən mətn redaktoru və ya veb fayl redaktorları ilə açıla bilər.

### KIT fayl idxalı

Demək olar ki, hər hansı bir fayl növü Kit faylına idxal edilə bilər. Aşağıda faylları .kit faylına idxal etmək üçün istifadə edilən idxal sintaksisi verilmişdir.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

KIT faylına idxal əlavə edildikdə və yadda saxlanıldıqda, idxal edilən faylın mətni ilə əvəz olunur. Siz həmçinin @import əvəzinə @include istifadə edə bilərsiniz.

### KIT faylında çoxlu idxal

Siz həmçinin vergüllə ayrılmış siyahıdan istifadə etməklə eyni anda birdən çox faylı idxal edə bilərsiniz:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## İstinadlar

* [Kit nədir?](https://codekitapp.com/help/kit/)


