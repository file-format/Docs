{
  "date": "2019-10-11",
  "keywords": [
"dhtml",
"dhtml faylı",
"dhtml fayl formatı",
"dhtml fayl növü",
"fayl",
"növü",
"dhtml faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DHTML - Dinamik HTML Fayl Format",
  "description": "DHTML fayl formatı və DHTML faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "DHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-dhtm-azl"
}
},
  "lastmod": "2019-09-10"
}

## DHTML faylı nədir?

.dhtml uzantısı olan fayl veb səhifənin dinamik məzmununu yaratmaq üçün istifadə edilən dinamik [HTML](/web/html/) fayldır. DHTML-də yaradılmış veb element hadisə ilə idarə olunur və səhifənin yenidən yüklənməsini tələb etmir. Əksər hallarda DHTML faylı veb-səhifənin açılan menyular, üzən təbəqələr, sürüşmə düymələri və digər dinamik məzmunlar kimi dinamik məzmununu yaratmaq üçün istifadə olunur. Siz demək olar ki, hər gün həyatınızda siçanı bir menyu elementinin üzərinə gətirdiyiniz zaman digər alt menyu seçimlərini açdığınız zaman dinamik html elementlərinə rast gəlirsiniz. DHTML elementlərin dinamik davranışına nail olmaq üçün [HTML](/web/html/), [Javascript](/web/js/), HTML DOM, HTML Hadisələri və [CSS](/web/css/) kimi veb texnologiyalarından istifadə edir.

## DHTML fayl formatı

DHTML faylları veb elementlərinin dinamik davranışını həyata keçirmək üçün DHTML kodunu ehtiva edən düz mətn fayllarıdır.


### DHTML DOM

DHTML Sənədi Obyekt Modeli (DOM) aşağıdakı şəkildə göstərildiyi kimi elementləri, atributları və mətni olan ağac strukturu olan HTML DOM-a əsaslanır.

{{< figure src="../dhtml.png" alt="HTML DOM" >}}

`Sənəd` qovşağı müxtəlif funksiyaları həyata keçirmək üçün bir neçə funksiyaya zəng etmək üçün istifadə edilə bilər. Aşağıdakı nümunə sadəcə olaraq DHTML-də JavaScript-in document.write() metodundan istifadə edir.

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

Bu kod brauzerdə çıxış etmək üçün Salam Dünya mətnini yazır.

### DHTML Hadisələri

|S.No.|Hadisə|Baş vermə|
---|---|---|
|1|onabort|İstifadəçi səhifənin və ya media faylının yüklənməsini dayandırdıqda baş verir.|
|2|onblur|İstifadəçi HTML obyektini tərk etdikdə baş verir.|
|3|onchange|İstifadəçi obyektin dəyərini dəyişdikdə və ya yenilədikdə baş verir.|
|4|onclick|Hər hansı bir istifadəçi HTML elementinə klik etdikdə baş verir və ya tetikler.|
|5|ondblclick|İstifadəçi HTML elementinə iki dəfə birlikdə kliklədikdə baş verir.|
|6|onfocus|İstifadəçi diqqətini HTML elementinə cəmlədikdə baş verir. Bu hadisə idarəedicisi onblur.|-un əksinə işləyir
|7|onkeydown|İstifadəçi klaviatura cihazında düyməni basdıqda işə salınır. Bu hadisə idarəedicisi bütün açarlar üçün işləyir.|
|8|onkeypress|İstifadəçilər klaviaturada düyməni basdıqda işə salınır. Bu hadisə idarəedicisi bütün açarlar üçün işə salınmayıb.|
|9|onkeyup|İstifadəçi obyekt və ya elementə basdıqdan sonra klaviaturadan düyməni buraxdıqda baş verir.|
|10|yükləmə|Obyekt tam yükləndikdə baş verir.|
|11|onmousedown|İstifadəçi HTML elementi üzərində siçan düyməsini sıxdıqda baş verir.|
|12|onmousemove|İstifadəçi kursoru HTML obyekti üzərində hərəkət etdirdikdə baş verir.|
|13|onmouseover|İstifadəçi kursoru HTML obyekti üzərində hərəkət etdirdikdə baş verir.|
|14|onmouseout|Siçan göstəricisi HTML elementindən kənara köçürüldükdə baş verir və ya tetikler.|
|15|onmouseup|Siçan düyməsini HTML elementi üzərində buraxdıqda baş verir və ya tetikler.|
|16|onreset|Formanı sıfırlamaq üçün istifadəçi tərəfindən istifadə olunur.|
|17|onselect|Bu, veb-səhifədə məzmun və ya mətn seçildikdən sonra baş verir.|
|18|onsubmit|İstifadəçi formanı təqdim etdikdən sonra düyməni kliklədikdə işə salınır.|
|19|onun yüklənməsi|İstifadəçi veb səhifəni bağlayan zaman işə salınır.|

## İstinadlar

* [Dinamik HTML - Vikipediya](https://en.wikipedia.org/wiki/Dynamic_HTML)


