{
  "date": "2023-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LAZ - Sıxılmış LIDAR Məlumat Mübadilə Faylı",
  "description": "LAZ fayl formatı və LAZ fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "LAZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-la-azz"
}
},
  "lastmod": "2023-07-18"
}

## LAZ faylı nədir?

LAZ fayl formatı LAS (Lidar LASer) fayl formatının sıxılmış versiyasıdır və xüsusi olaraq lidar nöqtəsi bulud məlumatlarını saxlamaq üçün nəzərdə tutulmuşdur. LAZ faylları LAS faylları ilə eyni məlumat və strukturu saxlayır, lakin orijinal məlumatların etibarlılığını qoruyarkən fayl ölçüsünü azaltmaq üçün itkisiz sıxılma üsullarından istifadə edir.

## LAZ Fayl Format - Qısa Tarix

TTLAZ fayl formatı böyük lidar məlumat dəstlərinin səmərəli saxlanması və ötürülməsinə artan tələbatı ödəmək üçün hazırlanmışdır. LAS fayllarını sıxaraq, LAZ faylları onların ölçüsünü əhəmiyyətli dərəcədə azaldır ki, bu da onları idarə etməyi və köçürməyi asanlaşdırır. Sıxılma, lidar nöqtəsi atributlarını daha yığcam formada təmsil etmək üçün entropiya kodlaşdırması və dəyişən uzunluqlu kodlaşdırma kimi müxtəlif alqoritmlərin birləşməsindən istifadə etməklə əldə edilir.

## LAZ fayl formatı

Sıxılmaya baxmayaraq, LAZ faylları heç bir məlumat itkisi olmadan orijinal LAS məlumatlarını tam bərpa etmək qabiliyyətini saxlayır. Bu o deməkdir ki, LAZ faylı açıldıqdan sonra onu sıxılmamış LAS faylı kimi emal etmək və təhlil etmək olar. Sıxılma və dekompressiya prosesi adətən LAZ formatını dəstəkləyən xüsusi proqram təminatı və ya kitabxanalardan istifadə etməklə həyata keçirilir.

LAZ fayl formatı LAS faylları ilə uyğunluğu saxlayır, lidar proqram təminatı və emal alətləri arasında qarşılıqlı əlaqəni təmin edir. Bu o deməkdir ki, LAS fayllarını oxuya və emal edə bilən proqramlar adətən LAZ fayllarını heç bir dəyişiklik etmədən idarə edə bilər. Bundan əlavə, LAZ faylları hələ də LAS faylları ilə eyni strukturu saxlayaraq fayl başlığını, dəyişən uzunluqlu qeydləri (VLR) və nöqtə məlumat qeydlərini ehtiva edir.

## LAZ Fayl Formatının üstünlükləri

**Azaldılmış Fayl Ölçüsü:** LAZ sıxılması lidar məlumat dəstlərinin fayl ölçüsünü əhəmiyyətli dərəcədə azaldır, onları daha idarəolunan və saxlanması və ötürülməsini asanlaşdırır.

**Data Integrity:** LAZ sıxılması itkisizdir, yəni sıxılmış məlumat orijinal LAS məlumatlarının dəqiq surətidir və heç bir məlumat və ya dəqiqlik itkisini təmin etmir.

**Birlikdə işləmə qabiliyyəti:** LAZ faylları LAS faylları ilə uyğun gəlir, mövcud lidar proqramı və iş axınları ilə qüsursuz inteqrasiyaya imkan verir.

**Effektiv emal:** Kiçik ölçüləri sayəsində LAZ faylları daha tez yüklənə və işlənə bilər, ümumi emal və təhlil vaxtlarını yaxşılaşdırır.

LAZ fayl formatı sıxılmış lidar məlumatlarının saxlanması və mübadiləsi üçün standart kimi lidar cəmiyyətində geniş şəkildə qəbul edilmişdir. O, ilkin məlumatların dəqiqliyini və keyfiyyətini qoruyarkən böyük lidar məlumat dəstlərinin daha asan idarə edilməsinə imkan yaradan məlumatların səmərəli sıxılması və məlumatların bütövlüyü arasında balans təklif edir.

## İstinadlar

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
