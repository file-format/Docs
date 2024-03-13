{
  "date": "2021-08-24",
  "keywords": [
"vbs",
"fayl",
"uzadılması",
"fayl formatı",
"Visual Basic Skripti",
"Proqramlaşdırma bələdçisi",
"vbs nümunəsi",
"Microsoft Visual Basic",
"VBScript"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "VBS - Visual Basic Skript Faylı",
  "description": "VBS fayl formatı və VBS fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "VBS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vb-azs"
}
},
  "lastmod": "2021-08-24"
}

## VBS faylı nədir?

VBS və ya VBScript Microsoft Visual Basic-in skript nəşri ilə bağlıdır. Hesablama mühitində istifadəçiyə onun bir çox aspektlərinə daxil olmaq və nəzarət etmək icazəsi verilir. VBScript-ə ətraf mühitin elementləri və alətlərindən istifadə etmək üçün **Komponent Obyekt Modeli** adlı modeldən istifadə etməyə icazə verilir. Bu mühit VBScript-in işləməsi və işləməsi üçün nəzərdə tutulub.

Veb inkişafı sahəsində müştəri tərəfindən daxil olduqda Javascript-ə bənzəyir. O, həmçinin veb səhifələrin emalı üçün serverlər tərəfindən istifadə olunur. Bu, [HTML](/web/html/) tətbiqləri kimi bəzi digər skript fayllarında nəzərə alına bilər.


## Qısa tarix ##

İlk dəfə 1996-cı ildə Microsoft tərəfindən Windows Skriptləri üçün nəzərdə tutulmuş texnologiyaların bir hissəsi kimi istifadəyə verilmişdir. Əvvəlcə veb tərtibatçılarının köməyi üçün xüsusi olaraq hazırlanmışdır. Elə həmin il Microsoft Windows-un Internet Explorer adlı tədqiqatçısı Visual Basic Script-in xüsusiyyətləri ilə birlikdə buraxıldı.

Texnologiya və veb inkişafındakı tərəqqi ilə VBScript-in bir çox versiyaları və bir çox qabaqcıl funksiyalar istifadəyə verildi. Üstəlik, gələn il bu skript dili yeni funksiyalarla Microsoft Windows-un bir hissəsi olacaq.

## Texniki Spesifikasiya ##

Server tərəfindəki veb səhifələr üçün VBScript ilə birlikdə **Aktiv Server Səhifələri** kimi alətlərdən istifadə olunur. Bu skript dili Windows-un skript komponentində də istifadə edilə bilər. Bu dildə olan fayllar Windows-da .vbs genişlənməsi ilə saxlanılır.

Bu dilin kodunda istifadə olunan döngələr kimi bir çox idarəetmə strukturları var. O, həmçinin əmr satırı olan və adlandırıla bilən və ya adlandırılmayan arqumentləri ehtiva edir. Bu dildə olan fayllar sadəcə Windows əməliyyat sisteminin qovluqlarında və ya iş masasında saxlanıla bilər. Microsoft Script Editor kimi VBScript proqramları üçün xüsusi inteqrasiya olunmuş inkişaf mühiti olmasa da, bu dilin inkişafı üçün şərait yaradır.

When VBScript is hosted by the Script host of Windows, it provides various features that are quite common to the languages of scripting but are not available in Visual Basic 6.0. Asan və ya birbaşa çıxışı əhatə edən xüsusiyyətlərə Şəbəkə Printerləri, adsız və adlandırılmış komanda xətti arqumentləri, stdout və stdin, Şəbəkə Paylaşımları, Windows İdarəetmə Alətləri, qrup üzvlüyü kimi şəbəkələrin istifadəçi məlumatı və daha çox şey daxildir. 

## VBS fayl formatı nümunəsi ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## İstinad ##

* [VBS - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/VBScript)




