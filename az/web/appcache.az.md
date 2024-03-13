{
  "date": "2022-08-05",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APPCACHE Faylı - HTML5 Keş Manifest Fayl Formatı",
  "description": "APPCACHE faylı və APPCACHE fayllarını yarada və aça bilən API-lərin nə olduğu haqqında öyrənin.",
  "linktitle": "APPCACHE",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-appcach-aze"
}
},
  "lastmod": "2022-08-05"
}

## APPCACHE faylı nədir?

APPCACHE faylı veb proqramlara oflayn daxil olmaq üçün brauzerlər tərəfindən keşləniləcək resursların siyahısını ehtiva edən mətn faylıdır. Bu, internet bağlantısı olmadıqda faydalıdır. Bu vəziyyətdə brauzer veb məzmununa girişi təmin etmək üçün oflayn keş resurslarından istifadə edir. APPCACHE faylında şəkillər (məsələn, **[PNG](/image/png/)**, **[WEBP](/image/webp/)** və s.), üslub cədvəlləri **([CSS])(/web/css/) kimi veb resursları var. )** və skript faylları (məsələn, Javascript **[JS](/web/js/)** faylları).

**APPCACHE fayllarını** aça bilən proqramlara Google Chrome, Safari və Firefox kimi veb brauzerlər daxildir.

## APPCACHE Fayl Format - Ətraflı Məlumat

APPCACHE faylları internet bağlantısı olmadan işləmək üçün veb səhifələrə oflayn çıxışı təmin edən sadə mətn fayllarıdır. APPCACHE-nin mövcudluğu səhifəni oflayn olaraq əlçatan kimi təyin edir.

### APPCACHE faylına necə istinad etmək olar?

HTML səhifənizdə APPCACHE faylına aşağıdakı kimi istinad edilir.

```
<html manifest="example.appcache">
  ...
</html>
```

## APPCACHE Manifest faylının strukturu

Sadə APPCACHE manifest faylı aşağıdakı kimi görünür.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Bu ən sadə nümunədir və daha mürəkkəb strukturlar da ola bilər.

## APPCACHE Manifestinin üstünlükləri

Keş interfeysindən istifadə veb proqramlara aşağıdakı üstünlükləri verir.

 1. Oflayn Baxış - Keş interfeysi son istifadəçilərə oflayn olduqda tam saytınıza baxmaq imkanı verir
 1. Sürət - keş birbaşa diskdən oflayn məzmuna yüksək sürətli giriş imkanı verir
 1. Hər zaman əlçatanlıq - Saytınız bağlandığı halda, istifadəçilər hələ də veb məzmuna daxil olacaq və oflayn təcrübə əldə edə biləcəklər

## İstinadlar

 * [AppCache Manifest üçün Başlanğıc Bələdçisi](https://web.dev/appcache-beginner/)

