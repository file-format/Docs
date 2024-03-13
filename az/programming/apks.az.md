
{
  "date": "2022-02-06",
  "keywords": [
".apks faylı",
"uzadılması",
"format",
"APK Set Arxivi",
"apks faylını necə açmaq olar",
"apks fayl formatı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APKS Faylı - APK Set Arxivi",
  "description": "APKS faylının nə olduğunu öyrənin?",
  "linktitle": "APKS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-apk-azs"
}
},
  "lastmod": "2022-02-06"
}

## APKS faylı nədir?

.apks uzantılı fayl Android paketi **APK** faylları toplusundan ibarət arxiv faylıdır. APKS faylındakı hər bir fərdi APK faylı cihazların müxtəlif aspektlərini nəzərə alaraq yaradılır. Bunlara memarlıq, dil, ekran sıxlığı və digər cihaz xüsusiyyətləri daxildir. APKS faylları **bundletool** tərəfindən yaradılıb. O, Android Tətbiq Paketini qurmaq və cihazlarda yerləşdirmək üçün proqram paketini müxtəlif APK-lara çevirmək üçün istifadə olunur.

## APKS Fayl Format - Ətraflı Məlumat

APKS faylları [ZIP](/compression/zip/) fayl formatından istifadə edərək sıxılmış fayllar kimi saxlanılır.

## APKS faylını necə yaratmaq olar?

Android Tətbiq Paketi (AAB) hazır olduqda, onun Google Play mağazasındakı davranışı cihazda yerləşdirilməsi üçün sınaqdan keçirilə bilər. APKS faylları bu məqsədlə AAB fayllarından yaradıla və Google Android [bundletool](https://developer.android.com/tools/bundletool) istifadə edərək sınaq cihazlarına quraşdırıla bilər. Aşağıdakı əmrdən istifadə edərək APK-lərdən APKS arxiv faylı yaratmaq üçün komanda xətti alətləri təqdim edir.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

APK-ları cihaza yerləşdirmək üçün APKS faylı aşağıdakı kimi cihaz imzalama məlumatı ilə imzalana bilər.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## İstinadlar

 * [bundletool - komanda xətti](https://developer.android.com/tools/bundletool)

