{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ZST Fayl - Zstandard Sıxılmış Fayl Format",
  "description":"ZST faylları yarada və aça bilən ZST fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-az",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## ZST faylı nədir?

ZST faylı Zstandard (zstd) sıxılma alqoritmi ilə yaradılan sıxılmış fayldır. Alqoritm tərəfindən itkisiz sıxılma ilə yaradılan sıxılmış fayldır. ZST faylları verilənlər bazası, fayl sistemləri, şəbəkələr və oyunlar kimi müxtəlif növ faylları sıxışdırmaq üçün istifadə edilə bilər. Zstandard ümumi sıxılma mexanizmini, media növünü və məzmun kodlamasını təsvir edən [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878) ilə idarə olunur.

## ZST fayl formatı

ZST faylları sıxılmış fayl formatında diskdə saxlanılır. Sıxılma mexanizmi RFC 8478-i köhnəlmiş RFC 8878 tərəfindən təsvir edildiyi kimidir.

## ZST Çərçivələri

ZST faylı bir və ya bir neçə çərçivədən ibarətdir. Hər bir çərçivə Zstandard çərçivə və ya atlana bilən çərçivə ola bilər. Zstandard çərçivəsi sıxılmış məlumatları ehtiva edir, atlana bilən çərçivə isə fərdi istifadəçi metadatasını ehtiva edir.

### Zstandart Çərçivə

Zstandard çərçivəsi aşağıdakı quruluşa malikdir.

|Sahə|Baytla Ölçü|
---|---|
|Sehrli_Nömrə |4 bayt|
|Frame_Header |2-14 bayt|
|Məlumat_Blok |n bayt|
|[Daha çox Data_Blokları] ||
|[Məzmun_Yoxlama məbləği] |4 bayt|

### Atlana bilən çərçivə

Atlana bilən çərçivə istifadəçi tərəfindən müəyyən edilmiş metadatanın birləşdirilən çərçivələr axınına daxil edilməsinə imkan verir. Atlana bilən çərçivənin quruluşu aşağıdakı kimidir.

|Sehrli_Nömrə |Çərçivə_Ölçüsü |İstifadəçi_Data|
---|---|---|
|4 bayt |4 bayt |n bayt|

## İstinadlar ##

* [RFC 8878 Zstandard Sıxılma](https://www.rfc-editor.org/rfc/rfc8878)


