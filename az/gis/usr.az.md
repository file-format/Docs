{
  "date": "2023-08-03",
  "keywords": [
"usr",
"usr faylı",
"usr faylı nədir",
"usr faylını necə açmaq olar",
"fayl",
"usr fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "USR Fayl Format - Lowrance GPS Məlumat Faylı",
  "description": "USR faylları yarada və aça bilən USR formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr-az",
      "parent": "gis"
}
},
  "lastmod": "2023-08-03"
}

## USR faylı nədir?

.usr fayl uzantısı da Lowrance GPS cihazları ilə bağlıdır. Xüsusilə, GPS məlumatlarını Lowrance GPS cihazları tərəfindən istifadə olunan İstifadəçi Məlumat Formatı (USR formatı) kimi tanınan formatda saxlamaq üçün istifadə olunur.

Lowrance GPS qurğusundan istifadə edərkən siz yol nöqtələrinizi, yollarınızı və marşrutlarınızı .usr faylları kimi saxlaya bilərsiniz. Bu fayllar adətən enlik, uzunluq, hündürlük, vaxt damğası və GPS fəaliyyətlərinizlə bağlı digər məlumatlar kimi məlumatları ehtiva edir.

Aşağıda Lowrance GPS cihazları ilə .usr fayllarının bəzi ümumi istifadələri verilmişdir:

- **Yol nöqtələri:** İstiqamət nöqtələri GPS-də işarələnmiş xüsusi yerlərdir, məsələn, orientirlər, sevimli balıqçılıq yerləri və ya maraq nöqtələri. Siz bu yerləri .usr faylları kimi saxlaya bilərsiniz və onlar idxal edilə, ixrac edilə və ya digər Lowrance GPS istifadəçiləri ilə paylaşıla bilər.

- ** Tracks:** Tracks GPS hərəkətlərinizin qeydə alınmış yolunu təmsil edir. Siz trek qeydlərinizi .usr faylları kimi saxlaya bilərsiniz ki, bu da sizə marşrutlarınızı daha sonra nəzərdən keçirməyə və təhlil etməyə və ya başqaları ilə paylaşmağa imkan verir.

- **Marşrutlar:** Marşrutlar GPS cihazınızda yarada və saxlaya biləcəyiniz əvvəlcədən müəyyən edilmiş yollardır. Bu marşrutlar həmçinin gələcək istifadə və ya paylaşmaq üçün .usr faylları kimi yadda saxlanıla bilər.

Lowrance GPS cihazınızda .usr fayllarını idarə etmək üçün siz adətən GPS məlumatlarınızı idxal etmək, ixrac etmək və manipulyasiya etmək üçün Lowrance-in Insight Planner və ya Lowrance GPS Utility kimi proqram təminatından istifadə edirsiniz.

## USR Fayl Format - Ətraflı Məlumat

Lowrance iFinder GPS cihazlarında .usr faylları yaradılır və cihaza daxil edilmiş MultiMediaCard (MMC) yaddaş kartında saxlanılır. Bu fayllar yol nöqtələri, yollar və marşrutlar kimi istifadəçi məlumatlarını ehtiva edir.

.usr fayllarını MMC-dən kompüterə köçürmək üçün bu addımları yerinə yetirə bilərsiniz:

- **MMC-ni çıxarın:** MultiMediaCard-ı (MMC) Lowrance iFinder GPS cihazından ehtiyatla çıxarın.

- **Kompüterə MMC daxil edin:** Yaddaş kartını kompüterinizin kart oxuyucusu yuvasına daxil etmək üçün müvafiq MMC kart oxuyucudan istifadə edin.

- **.usr fayllarını tapın:** MMC kompüteriniz tərəfindən tanındıqdan sonra siz onun üzərində saxlanan fayllara daxil ola bilməlisiniz. GPS məlumatlarınızı ehtiva edən .usr fayllarını axtarın.

- **GPSBabel ilə konvertasiya:** .usr fayllarını başqa GPS formatına çevirmək üçün siz müxtəlif GPS fayl formatları ilə işləmək üçün pulsuz və açıq mənbəli alət olan GPSBabel-dən istifadə edə bilərsiniz. GPSBabel sizə .usr fayllarını digər GPS proqram təminatı və ya cihazları ilə uyğun gələn formatlara çevirməyə imkan verən geniş çeşidli giriş və çıxış formatlarını dəstəkləyir.

Siz GPSBabel-i rəsmi internet saytından (http://www.gpsbabel.org/) yükləyə və kompüterinizə quraşdıra bilərsiniz. Quraşdırıldıqdan sonra çevrilməni həyata keçirmək üçün proqram təminatının komanda xətti interfeysindən və ya qrafik istifadəçi interfeysindən (əgər varsa) istifadə edə bilərsiniz.

Məsələn, .usr fayllarını GPX formatına çevirmək istəyirsinizsə, belə bir əmrdən istifadə edə bilərsiniz:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

Yuxarıdakı əmr GPSBabel-ə Lowrance USR formatında input.usr daxiletmə faylını oxumağı və output.gpx çıxış faylını GPX formatında yazmağı tapşırır.

- **Çevrilmiş Faylların İdxal edilməsi/İstifadəsi:** Konversiyadan sonra siz GPS məlumatlarınızı bu formatı dəstəkləyən digər GPS proqram təminatı və ya cihazlarla istifadə edə biləcəyiniz yeni formatda (məsələn, GPX) əldə edəcəksiniz.

## USR faylını necə açmaq olar?

USR fayllarını açan və ya istinad edən proqramlar daxildir

- GPSBabel (Windows)
- GPSBabel (Mac)
- GPSBabel (Linux)

## İstinadlar
* [Lowrance Electronics](https://en.wikipedia.org/wiki/Lowrance_Electronics)


