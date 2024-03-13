{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MASTER Fayl - ASP.NET Master Səhifə Fayl Format",
  "description" : "MASTER faylları yaratmaq və açmaq üçün MASTER Fayl Format və API-lər haqqında məlumat əldə edin.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master-az",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## MASTER faylı nədir?

MASTER faylı ASP.NET ilə yaradılmış əsas veb səhifə şablon faylıdır. O, MASTER faylı ilə eyni tərtibata və parametrlərə malik olan çoxsaylı səhifələr yaratmaq üçün başlanğıc nöqtəsi kimi istifadə olunur. Şablon MASTER faylına başlıq, naviqasiya menyuları, altbilgi, şrift və üslub məlumatı üçün parametrlər daxildir. MASTER faylından istifadə tez bir zamanda birdən çox veb səhifə yaratmağa kömək edir.

MASTER faylı Microsoft Visual Studio 2022 və yuxarı versiyalardan istifadə edərək aça bilərsiniz.

## MASTER Fayl Format - Ətraflı Məlumat

MASTER faylı HTML fayl formatında yaradılır və saxlanılır və hər hansı digər veb səhifə faylına bənzəyir. O, redaktə edilə bilən və redaktə olunmayan bölmələrə bölünür. Redaktə edilə bilən bölmələr istifadəçi tələblərinə uyğun olaraq dəyişdirilə bilən bölmələrdir. MASTER faylı Microsoft Visual Studio-da açıldıqda redaktə olunmayan bölmələr boz rəngdədir.

Master Səhifələr iki hissədən, yəni əsas səhifənin özü və bir və ya daha çox məzmun səhifəsindən ibarətdir.

### MASTER Səhifə

Əsas səhifə .master genişlənməsinə malikdir və ASP.NET-də hazırlanmışdır. Statik mətn, HTML etiketləri və server tərəfi nəzarətlərindən ibarət əvvəlcədən təyin edilmiş tərtibata malikdir. Adi .aspx səhifələrində @ Page direktivindən istifadə olunur. .master faylları olduqda, bu @ Master direktivi ilə əvəz olunur.

### Məzmun Səhifələri

Məzmun səhifəsi əsas səhifənin yertutan idarələri üçün məzmunu təmsil edir. Bunlar əslində master səhifənin arxasındakı kod olan .aspx səhifələridir. Məzmun səhifələri @ Page direktivindən istifadə edərək, aşağıda göstərildiyi kimi istifadə ediləcək master səhifəyə işarə edən MasterPageFile atributunu daxil etməklə bağlanır.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## İstinadlar

* [ASP.NET Master Səhifələrinə Baxış](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))


