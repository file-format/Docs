{
  "date": "2021-12-09",
  "keywords": [
"kimi",
".kimi",
"fayl formatı",
"fayl növü",
".asa faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASA - ASP Konfiqurasiya Faylı",
  "description": "ASA faylı və ASA faylları yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "ASA",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-as-aza"
}
},
  "lastmod": "2021-12-09"
}

## ASA faylı nədir?

ASA faylı [ASP](/web/asp/)/ASP.NET layihələri üçün yaradılmış konfiqurasiya faylıdır. Tətbiqdə Qlobal səviyyədə əlçatan olması nəzərdə tutulan dəyişənlərin bəyannamələrini, ehtiva edən və funksiyaları ehtiva edir. Layihədəki bütün səhifələr bu dəyişənlərə və funksiyalara daxil ola bilər, beləliklə, onları yenidən yazmaq tələbindən qaçın. Belə nümunələrdən biri, digər ASP veb-sayt səhifələri tərəfindən əlçatan olmaq üçün kök kataloqda saxlanılan Global.asa səhifəsidir. Global.asa faylları isteğe bağlıdır, lakin istifadə olunarsa, hər bir proqramda yalnız bir Global.asa faylı ola bilər.

## ASA Fayl Format - Ətraflı Məlumat

ASA faylları aşağıdakı məlumatları ehtiva edən düz mətn fayllarıdır.

 * Tətbiq hadisələri
 * Sessiya hadisələri
 * \<object> bəyannamələr
 * TypeLibrary bəyannamələri
 * #include direktivi

## ASA fayl nümunəsi

Global.asa faylı bu kimi görünə bilər.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## İstinadlar

* [ASP Global.asa faylı - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)


