{
  "date": "2022-04-07",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HAML fayl formatı - Haml mənbə kodu faylı",
  "description": "HAML fayl formatı və HAML faylını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "HAML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ham-azl"
}
},
  "lastmod": "2022-04-07"
}

## HAML faylı nədir?

HAML faylı [Haml](https://haml.info/) dilində yazılmış mənbə kodunu ehtiva edən HTML abstraksiya işarələmə dili faylıdır. O, ERB (Ruby şablon skriptləri) üçün əvəz kimi istifadə edilə bilər. HAML faylı veb sənədin HTML-ni yaratmaq üçün şablon mənbə kodunu ehtiva edir. ERB faylları sadəcə proqram/görüntülər qovluğundakı bu faylları faylın genişləndirilməsini dəyişdirərək Haml ilə əvəz etməklə əvəz edilə bilər. HAML faylları Microsoft Notepad, Notepad++, Apple TextEdit kimi istənilən mətn redaktoru ilə açıla bilər.

## HAML fayl formatı

HAML faylları düz mətn faylları kimi diskdə saxlanılan mənbə fayllardır. O, HAML sintaksisində yazılmış kodu ehtiva edir. HAML kodu daha sadə və asan etmək üçün **<>** teqlərini **%** işarəsi ilə əvəz edir. ERB faylları aşağıdakı sadə nümunədə göstərildiyi kimi HAML ilə əvəz edilə bilər.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML Nümunəsi

Aşağıda HAML nümunəsi Hello World nümunəsidir.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
aşağıdakı HTML çıxışını göstərir.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## İstinadlar

* [HAML - Github](https://github.com/haml/haml)


