{
  "date": "2021-08-17",
  "keywords": [
"udf faylı",
"udf fayl formatı",
"udf faylı nədir",
"fayl",
"udf nümunəsi",
"udf fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "UDF fayl formatı və UDF faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "UDF - Universal Disk Format Faylı",
  "linktitle": "UDF",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-ud-azf"
}
},
  "lastmod": "2021-08-17"
}

## UDF faylı nədir?
.udf uzantılı fayl adətən faylları optik mediada saxlamaq üçün istifadə olunan disk təsvir formatıdır; DVD, CD və digər optik mediaları yazmaq üçün istifadə edilə bilər; UDF standartında müəyyən edilmiş kataloq strukturundan istifadə edərək fayllar toplusunu saxlayır; fayllar yazıldıqdan sonra da hədəf diskdə silinməyə və dəyişdirilməyə imkan verir. Optik Saxlama Texnologiyaları Assosiasiyası, yenidən yazıla bilən optik media və yalnız oxuna bilən media kimi bütün optik media üçün ümumi fayl sistemi yaratmaq üçün UDF fayl sistemini standart olaraq təyin etdi.

## UDF fayl formatı 
UDF fayl formatı geniş çeşidli media üçün kompüter məlumatlarının saxlanması üçün açıq satıcı-neytral fayl sistemidir. O, adətən DVD-lər və daha yeni optik disk formatları üçün istifadə olunur. Adətən, proqram toplu prosesdə UDF fayl sistemini mənimsəyir və onu bir keçiddə optik mediaya yazır. Bununla belə, paketləri yenidən yazıla bilən mediaya yazdıqda, UDF faylların diskdə yaradılmasına, silinməsinə və dəyişdirilməsinə imkan verir.
### UDF Spesifikasiyaları
UDF standartı aşağıdakı üç fayl sistemi variantını müəyyən edir:

- **Plain Build**: Bu, bütün UDF versiyalarında dəstəklənən orijinal formatdır. O, standartın ilk versiyasında təqdim edilib, bu format DVD+RW, sərt disklər və DVD-RAM mediası kimi təsadüfi oxumaq və ya yazmaq imkanı verən istənilən disk tipində istifadə oluna bilər.
- **VAT build**: Used specifically for writing to write-once media. The VAT is an additional structure on the disc that allows packet writing; that is, remapping physical blocks when files or other data on the disc are modified or deleted. For write-once media, the entire disc is virtualized, making the write-once nature transparent for the user; the disc can be treated the same way one would treat a rewritable disc.
- **Spared (RW) build**: Xüsusilə yenidən yazıla bilən mediaya yazmaq üçün istifadə olunur. O, diskin dəfələrlə yenidən yazılmış hissələrində nəticədə baş verəcək nasazlıqları idarə etmək üçün əlavə Ehtiyatlı Cədvəl əlavə edir. Bu cədvəl köhnəlmiş sektorların izlərini saxlayır və onları işləyən sektorlara uyğunlaşdırır. UDF-nin qüsurların idarə edilməsi, optik disklər üçün Mount Rainier (MRW) və ya sabit disk üçün disk nəzarətçisi kimi qüsurların idarə edilməsinin başqa formasını artıq tətbiq edən sistemlərə şamil edilmir.
 



## İstinadlar 

* [Windows Imaging Format - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Windows_Imaging_Format)



