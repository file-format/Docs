{
  "date": "2019-10-11",
  "keywords": [
"mhtml",
"mhtml faylı",
"mhtml fayl formatı",
"mhtml fayl növü",
"fayl",
"növü",
"mhtml faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MHTML - MIME HTML faylı",
  "description": "MHTML fayl formatı və MHTML faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "MHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mhtm-azl"
}
},
  "lastmod": "2019-09-10"
}

## MHTML faylı nədir?

MHTML uzantılı fayllar bir sıra müxtəlif proqramlar tərəfindən yaradıla bilən veb səhifə arxiv formatını təmsil edir. Bu format arxiv formatı kimi tanınır, çünki o, veb **[HTML](/web/html/)** kodunu və əlaqəli resursları bir faylda saxlayır. Bu resurslara veb-səhifə ilə əlaqəli hər şey daxildir, məsələn, şəkillər, appletlər, animasiyalar, audio fayllar və s. MHTML faylları Internet Explorer və Microsoft Word kimi müxtəlif proqramlarda açıla bilər. Microsoft Windows, Windows-da problem yaradan hər hansı proqramdan istifadə zamanı müşahidə olunan problemlərin ssenarilərini qeyd etmək üçün MHTML fayl formatından istifadə edir. MHTML fayl formatı, mesaj/rfc822-də müəyyən edilmiş spesifikasiyalara oxşar səhifə məzmununu kodlaşdırır ki, bu da düz mətn e-poçtu ilə əlaqəli spesifikasiyalardır. Formatın faktiki spesifikasiyalar [RFC 2557](https://tools.ietf.org/html/rfc2557) tərəfindən təfərrüatlandırıldığı kimidir.

## MHTML fayl formatı

MHTML eyni zamanda HTML veb səhifələrini öz resursları ilə birlikdə vahid veb arxivə kodlaşdırmaq qabiliyyətinə görə Ümumi HTML sənədlərinin MIME Encapsulation kimi tanınır. RFC 2557 spesifikasiyasına uyğun olaraq, məcmu sənəd kök resursu (obyekt) və URI-lər vasitəsilə onunla əlaqəli digər resursları ehtiva edən MIME kodlu mesajdır. Bu cür digər resurslar daxili şəkillərin, üslub cədvəllərinin, appletlərin və s.-nin təqdimatı ola bilər. Bundan əlavə, bunlar digər multimedia sənədlərinin kökü ola bilər. MHTML fayl formatı üçün tam sənəd spesifikasiyası [RFC 2557](https://tools.ietf.org/html/rfc2557)-də təfərrüatlı şəkildə verilmişdir və bu fayl formatının oxunması/yazılması üçün hər cür proqram inkişafı üçün istinad edilməlidir. Standart müəyyən edir ki, istinad ediləcək bədən hissələri ya Content-ID, ya da Məzmun Yeri ilə müəyyən edilə bilər.

### MIME Məzmun Başlıqları

MIME məzmun başlığı, Məzmun-Yer, digər bədən hissələrindəki resurslara URI istinadlarını həll etmək üçün müəyyən edilmişdir. Bu başlıq istənilən mesaj və ya məzmun başlığında baş verə bilər.

### Məzmun-Məkan Başlığı

Məzmun-Məkan, yerləşdirildiyi bədən hissəsinin məzmununu etiketləyən URI-nin təsviridir. Onun dəyəri mütləq və ya nisbi URI ola bilər. O, mesajın bəzi və ya bütün alıcıları tərəfindən alına bilməyən resursu etiketləmək üçün istifadə edilə bilər. Tək mesajın yalnız bir Məzmun-Məkan başlığına malik olmasına icazə verilir. Həm Məzmun-Məkan, həm də Məzmun-ID etiketləri ilə bədən hissələrini ehtiva edən çoxhissəli/əlaqəli strukturun nümunəsi:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### MHTML Aqreqatlarının URI-ləri

MHTML aqreqatının URI-si kök URI-dən fərqlidir. Məzmun-Məkan başlığı sahəsi çoxhissəli/əlaqəli başlığın başlığında istifadə olunarsa, bütün məcmuəyə şamil edilməlidir. Eynilə, əldə edilən resurslar dəsti, MHTML məcmuuna istinad edən URI bu məcmuu əldə etmək üçün istifadə edildikdə, onun hissələrinin Məzmun-Məkanlarından istifadə etməklə əldə edilən resurslar dəstindən fərqli ola bilər. Məsələn, MHTML aqreqatını əldə etmək köhnə versiyanı qaytara bilər, kök URI-ni və onun daxili əlaqəli obyektlərini əldə etmək daha yeni versiyanı qaytara bilər.

## İstinadlar

* [Məcmu Sənədlərin MIME Encapsulation - RFC 2557](https://tools.ietf.org/html/rfc2557)

* [MHTML Fayl Format - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/MHTML)


