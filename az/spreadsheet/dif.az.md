{
  "date": "2019-12-10",
  "keywords": [
"DIF",
"fayl",
"uzadılması",
"fayl formatı",
"Məlumat mübadiləsi faylı",
"Elektron cədvəl"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "DIF fayl uzantısının və DIF fayllarını yarada və aça bilən API-lərin nə olduğunu bilmək üçün fayl formatı bələdçisi.",
  "title": "DIF - Məlumat mübadiləsi fayl formatı",
  "linktitle": "DIF",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-di-azf"
}
},
  "lastmod": "2019-12-10"
}

## DIF faylı nədir?

DIF, müxtəlif proqramlar arasında elektron cədvəl məlumatlarını idxal/ixrac etmək üçün istifadə olunan Məlumat Mübadiləsi Formatının qısaltmasıdır. Bunlara Microsoft Excel, OpenOffice Calc, StarCalc və bir çox başqaları daxildir. O, bu fayl formatının yeganə məhdudiyyəti olan bir cədvəldə olan məlumatları saxlayır.

## DIF Fayl Formatının Qısa Tarixi ##

DIF fayl formatı 1980-ci illərin əvvəllərində Software Arts, Inc. tərəfindən hazırlanmışdır. DIF üçün fayl formatının spesifikasiyası fərdi kompüterlər üçün ilk elektron cədvəl proqramı olan VisiCalc-a daxil edilmişdir. Bu spesifikasiyalar 1981-ci ildə müəllif hüquqları ilə qorunur və Software Arts Products Corp.-un qeydə alınmış ticarət nişanı idi.

## DIF fayl formatı ##

DIF elektron cədvəl məzmununu ASCII mətn faylında saxlayır ki, bu da ona mətn redaktoru ilə baxmağa və redaktə etməyə imkan verir. Bu format məlumat mübadiləsi xüsusiyyətlərinə görə verilənlərin serializasiya formatları siyahısında öz yerini tutur. DIF faylı 2 bölmədən ibarətdir; başlıq və məlumatlar.

DIF-də hər şey 2 və ya 3 sətirli hissə ilə təmsil olunur. Başlıqlar 3 sətirli hissə əldə edir; məlumat, 2.

* Başlıq hissələri bütün böyük hərflərdən, yalnız əlifba simvollarından və 32 hərfdən az olan mətn identifikatoru ilə başlayır. Aşağıdakı sətir bir cüt rəqəm, üçüncü sətir isə sitat gətirilən sətir olmalıdır.

* Məlumat hissələri rəqəm cütü ilə başlayır və növbəti sətir sitat gətirilən sətir və ya açar sözdür.


### Dəyərlər ###

Dəyər iki sətir tutur, birincisi bir cüt ədəd, ikincisi isə sətir və ya açar sözdür. Cütlüyün ilk nömrəsi növü göstərir:

* −1 – directive type, the second number is ignored, the following line is one of these keywords:
** BOT – tuple başlanğıcı (sətrin başlanğıcı)
** EOD – məlumatın sonu
* 0 – numeric type, value is the second number, the following line is one of these keywords:
** V – etibarlıdır
** NA – mövcud deyil
** ERROR – xəta
** TRUE – həqiqi boolean dəyəri
** FALSE – yanlış boolean dəyəri
* 1 – sətir tipi, ikinci nömrə nəzərə alınmır, aşağıdakı sətir qoşa dırnaq içərisində olan sətirdir


### DIF başlıq parçası ###

DIF faylının başlıq hissəsi dəyərin iki sətirindən sonra identifikator xəttindən ibarətdir. Başlıq hissələrindəki rəqəmli dəyərlər etibarlılıq açar sözləri əvəzinə boş sətirdən istifadə edir. Bu başlıq hissələrinin təfərrüatları aşağıdakı kimidir.

* CƏDVƏL - versiyanın rəqəmsal dəyəri, istifadə olunmayan ikinci sətirdə generator şərhi var

* VEKTORLAR - rəqəmsal dəyər kimi sütunların sayı izlənilir

* TUPLES - cərgələrin sayı rəqəmsal dəyər kimi verilir

* MƏLUMAT - 0 rəqəmsal dəyərdən sonra, cədvəl üçün məlumatlar izlənilir, hər cərgə BOT dəyərindən əvvəl gəlir, bütün cədvəl EOD dəyəri ilə dayandırılır


### DIF nümunəsi ###

Aşağıdakı nümunə sadə iş vərəqinin məzmununu və onun ekvivalent DIF təmsilini göstərir.


|Ad|Yaş
---|---|
|Bob|34
|Vərəq|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## İstinadlar ##

* [ DIF - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Data_Interchange_Format)


