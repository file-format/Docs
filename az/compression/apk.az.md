{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APK - APK faylı nədir?",
  "description": "APK faylı və APK faylları yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "APK",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ap-azk"
}
},
  "lastmod": "2021-04-27"
}

## APK faylı nədir?

.apk uzantılı fayl Android cihazlarında proqramlar (tətbiqlər) quraşdırmaq üçün istifadə edilən Google Android proqram faylıdır. O, rəsmi IDE Google Android Studio proqramından istifadə edərək icra edilə bilən fayl kimi yaradılır və son istifadəçilər tərəfindən endirilməsi və quraşdırılması üçün Google Play mağazasına yüklənir. APK faylları yaradıla və əl ilə quraşdırma üçün, həmçinin Google Play mağazasında dərc olunmazdan əvvəl əlçatan edilə bilər. Bu, yaradılmış APK paket faylının funksionallığını və davranışını sınamağa kömək edir. Buna görə də, APK faylının etibarlı mənbədən olduğuna və heç bir zərərli proqram olmadığına əmin olmaq lazımdır.

## APK fayl formatı

APK faylları hər hansı ZIP faylı açma proqramı ilə açıla bilən [ZIP](/compression/zip/) fayl formatında sıxılmış şəkildə qablaşdırılır. Belə faylın .apk uzantısı .zip olaraq dəyişdirilə və faylı istənilən ZIP proqramında aça və ya məzmununu çıxara bilər.

## APK paket məzmunu

Tək bir APK faylı onun quraşdırılması və icrası üçün tələb olunan bütün lazımi faylları ehtiva edir. APK faylı ZIP tətbiqi ilə çıxarıldıqda aşağıdakı fayl və qovluqları ehtiva edir.

 * `META-INF/`: Manifest faylı, imza və arxivdəki resursların siyahısını ehtiva edən qovluq
 * `lib/`: armeabi-v7a, x86, arm64-v8a və s. kimi xüsusi platformalara aid tərtib edilmiş kodu ehtiva edən kataloq.
 * `res/`: Şəkillər kimi tərtib edilməmiş resursları ehtiva edən kataloq
 * `assets/`: AssetManager tərəfindən əldə edilə bilən tətbiq aktivlərini ehtiva edən kataloq.
 * `androidManifest.xml`: APK faylının adını, versiya məlumatını və məzmununu ehtiva edir
 * `classes.dex`: Bunlar Dalvik virtual maşınında və Android Runtime ilə işlədilə bilən tərtib edilmiş Java sinifləridir.
 * `resources.arsc`: Sətirlər kimi tərtib edilmiş resurslar faylı

## APK fayllarını necə açmaq olar

APK faylları Android cihazlarında quraşdırılmalıdır. Bundan əlavə, Windows 11, APK fayllarının quraşdırılması funksiyasını rəsmi olaraq dəstəkləyən Windows-un ilk versiyasıdır.

### APK faylını Android Cihazına necə quraşdırmaq olar

Android cihazlarınızda APK faylı quraşdırmaq üçün aşağıdakı addımlardan istifadə edilə bilər.

 1. Veb brauzerindən istifadə edərək APK yükləyin
 2. Ona toxunun – bundan sonra onun cihazınızın yuxarı çubuğunda endirilməsini görə bilməlisiniz
 3. Yükləndikdən sonra Yükləmələri açın, APK faylına toxunun və tələb olunduqda Bəli seçiminə toxunun.

Bu addımlardan sonra proqramın cihazınızda quraşdırılması başlayacaq.

### Windows-da APK faylını necə açmaq olar

APK faylını açmaq/girmək üçün Windows PC-də Android emulyatorundan istifadə edə bilərsiniz. BlueStacks, Windows-da Android emulyatorunu açmaq üçün istifadə edilə bilən belə bir Android emulyatorudur. Windows 11-dən istifadə edirsinizsə, şanslısınız, çünki Windows 11 rəsmi olaraq APK fayllarını quraşdırmaq qabiliyyətini dəstəkləyir.

### Mac-da APK faylını necə açmaq olar

Siz həmçinin macOS-da BlueStack-dən istifadə edə və APK fayllarını aça bilərsiniz. Bu, pulsuz bir Android emulyatorudur və onu yalnız Android tətbiqlərinə daxil olmaq üçün ən yaxşı üsul kimi istifadə etmək imkanı verir.

## APK faylını necə yaratmaq olar

APK faylının yaradılması xüsusi alətlərin və inkişaf mühitlərinin istifadəsini tələb edir. Android tərtibatçıları ilk növbədə Android proqramlarının hazırlanması üçün rəsmi inteqrasiya olunmuş inkişaf mühiti (IDE) olan Android Studio-dan istifadə edirlər. APK faylının yaradılması ilə bağlı addımların ümumi icmalı buradadır:

 1. **İnkişaf mühitini qurun:** Android Studio proqramını kompüterinizdə quraşdırın və qurun. Android Studio Android proqramlarının hazırlanması, sınaqdan keçirilməsi və qablaşdırılması üçün hərtərəfli alətlər dəsti təqdim edir.
 1. **Tətbiqinizi inkişaf etdirin:** Android proqramınızın kodunu yazmaq üçün Java və ya Kotlin proqramlaşdırma dillərindən istifadə edin. Android Studio proqramınızı yaratmağınıza kömək etmək üçün kod redaktorları, emulyatorlar və sazlama alətləri daxil olmaqla zəngin xüsusiyyətlər və resurslar dəsti təqdim edir.
 1. **Tətbiqi yaradın:** Kodu yazmağı və istifadəçi interfeysinin dizaynını tamamladıqdan sonra tətbiqinizi tərtib etmək və paketləmək üçün Android Studio-nun qurma alətlərindən istifadə edin. Bu proses APK faylı üçün tələb olunan lazımi faylları və resursları yaradır.
 1. ** APK faylını imzalayın:** Tətbiqinizi yaymazdan əvvəl APK faylını imzalamaq vacibdir. Tətbiqin imzalanması proqramın bütövlüyünü və həqiqiliyini təmin edir. Android Studio sizə imza açarı yaratmağa və bu açardan istifadə edərək APK faylınızı imzalamağa imkan verir.
 1. **APK faylını paylayın:** APK faylınızı imzaladıqdan sonra onu müxtəlif kanallar vasitəsilə yaya bilərsiniz. Siz onu geniş auditoriyaya paylamaq üçün Google Play Store-a yükləyə və ya e-poçt, yükləmə linkləri və ya digər paylama platformaları vasitəsilə birbaşa istifadəçilərlə paylaşa bilərsiniz.

Qeyd etmək lazımdır ki, Android Studio-dan yaradılan APK faylı adətən istehsalda istifadə üçün optimallaşdırılıb. İnkişaf prosesi zamanı siz həmçinin test və sazlama məqsədləri üçün faydalı olan, lakin paylanma üçün nəzərdə tutulmayan debaq APK faylları yarada bilərsiniz.

## Tez-tez verilən suallar

 * ** APK faylları cihazıma zərər verə bilərmi?** APK faylları cihazlar üçün təhlükə yarada bilər. Bu, onlarda zərərli proqramların olma ehtimalı ilə bağlıdır. Buna görə, quraşdırmaya davam etməzdən əvvəl APK fayllarını onlayn virus taramasına məruz qoymaq məsləhətdir. Bundan əlavə, bir Android antivirus tətbiqindən istifadə etmək ehtiyatlı bir tədbirdir. Cihazınızın aldadıcı proqramın qurbanı olmaq riskini azaltmaq üçün yaxşı tanış olduğunuz və etibar etdiyiniz etibarlı mənbələrdən yükləmək yaxşıdır.

 * ** APK faylları qanunidirmi?** APK fayllarının endirilməsi və onlardan Google Play Store-dan başqa mənbələrdən tətbiq quraşdırmaları üçün istifadə edilməsi tamamilə qanun çərçivəsindədir. EXE və ya ZIP kimi formatlara bənzər APK fayl formatıdır. Google bu formata öncülük etsə də, APK faylları yaratmaq və istifadə etmək hər kəs üçün açıqdır.

 * **Android cihazımda APK fayllarını necə tapa bilərəm?** APK faylları istifadəçilərdən gizli qalır, çünki Android proqram quraşdırmalarını Google Play və ya digər proqram paylama platforması vasitəsilə fonda idarə edir. Bununla belə, digər mənbələrdən endirilmiş APK faylları Android fayl meneceri ilə tapıla bilər.

## İstinadlar

* [APK Fayl Formatı](https://en.wikipedia.org/wiki/Android_application_package)


