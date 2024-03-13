{
  "date": "2022-02-16",
  "keywords": [
"obb faylı",
"obb fayl formatı",
"obb faylı nədir",
"fayl",
"obb nümunəsi",
"obb fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OBB Fayl Format - Android Opaque Binary Blob Faylı",
  "description": "OBB fayl formatı və OBB fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "OBB",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-ob-azb"
}
},
  "lastmod": "2022-02-16"
}

## OBB faylı nədir?

OBB faylı Android [APK](/compression/apk/) faylına əlavə olan əlavə məlumatları ehtiva edən genişləndirmə faylıdır. Google Play mağazası ölçüsü 100 MB-dan çox olan Android APK faylının olmasına icazə vermir. Lakin bəzi proqramlar APK fayllarına əlavə olaraq yüksək dəqiqlikli qrafika, media faylları və ya digər böyük aktivlərin yerləşdirilməsini tələb edə bilər. OBB fayl növləri burada daxil olur. Google Play bu genişləndirmə fayllarını APK faylına əlavə olaraq əlavə etməyə imkan verir.

## OBB fayl formatı

OBB faylları APK faylları ilə birlikdə ikili fayllar kimi saxlanılır. APK OBB faylları ilə birlikdə olduqda, Google Play genişləndirmə fayllarını öz serverində yerləşdirir və tərtibatçıdan əlavə xərc tələb olunmur. Proqram quraşdırma üçün endirilən zaman bu əlavə fayllar cihazın paylaşılan yaddaşında SD kartda və ya USB ilə quraşdırıla bilən bölmədə saxlanılır.

OBB faylları endirilir və yükləndikdən sonra quraşdırılır. Ancaq bəzi hallarda, proqram ilk dəfə işə salındıqda, bunlar quraşdırma üçün endirilir.

### OBB Maksimum Fayl Ölçüsü

Google Play Store sizə 2 GB-a qədər ölçülü OBB genişləndirmə faylları yükləməyinizə imkan verir. İnternet vasitəsilə səmərəli yükləmək üçün böyük ölçülü faylların sıxılmış [ZIP](/compression/zip/) fayl kimi yüklənməsi tövsiyə olunur.

Bu genişləndirmə faylları tətbiq tərəfindən tələb olunan əlavə resurslar üçün **əsas** əsas genişləndirmə faylı və ya əsas genişləndirmə faylına kiçik yeniləmələr üçün nəzərdə tutulmuş əlavə yamaq genişləndirmə faylı kimi yerləşdirilə bilər.

## İstinadlar

* [Android Tərtibatçıları - Genişlənmə Faylları](https://developer.android.com/google/play/expansion-files)


