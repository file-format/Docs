{
  "date": "2022-07-21",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HDR Fayl Format - HDR şəkil faylı nədir?",
  "description": "HDR fayl formatı və HDR faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "HDR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-hd-azr"
}
},
  "lastmod": "2022-07-21"
}

## HDR faylı nədir?

HDR faylı rəqəmsal kamera fotoşəkillərini saxlamaq üçün Yüksək Dinamik Diapazonlu (HDR) rastr şəkil fayl formatıdır. O, foto redaktorlarına dinamik diapazonu məhdud olan rəqəmsal şəkillərin rəngini və parlaqlığını artırmağa imkan verir. Bu modifikasiya künclərin ətrafındakı parlaqlığı yaxşılaşdıra bilər, nəticədə təbii görüntüyə yaxındır. HDR faylları adətən 32 bitlik rastr şəkillər kimi saxlanılır. Adobe Photoshop HDR faylları yarada və aça bilər.

HDR faylları HDRI kimi də tanınır.

## HDR Fayl Format - Ətraflı Məlumat

HDR fayl formatı orijinal Radiance Picture (.pic) fayl formatına əsaslanır. HDR faylının piksel məlumatları adətən sıxılmamış şəkildə saxlanılır, lakin bəzi hallarda o, sadə işləmə uzunluğu kodlaşdırma sistemindən istifadə edərək sıxılır.

### HDR Fayl Strukturu

HDR şəkil faylı aşağıdakı üç hissədən ibarətdir:

 * **Başlıq:** HDR faylı şəkil faylındakı ilk baytlarla, yəni #?RADIANCE ilə müəyyən edilir.
 * **Qətiyyət sətri:** Başlıqdan sonra 4 dəyərdən ibarət tək ayırdetmə xətti gəlir; hər birinin ardınca ədədi tam dəyər olan X və Y etiketi. X və Y sırası fırlanmanı göstərir. X və Y-nin müsbət və mənfi qiymətlərlə birləşməsi bütün mümkün istiqamət və fırlanmaları əhatə edir.
 * **Piksel Məlumatı:** HDR faylının piksel datası ya sıxılmamış, ya da standart iş uzunluğu kodlaşdırmasından istifadə edərək sıxılmışdır.

## Açıq mənbəli HDR/HDRI API-ləri

 * **[imageinfo](https://github.com/xiaozhuai/imageinfo)** - Yükləmə/şifrəni açmadan şəkil ölçüsünü və formatını əldə etmək üçün çarpaz platforma super sürətli tək başlıq [C++](/programming/cpp/) kitabxanası.
 * **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - Yükləmə/şifrəni açmadan şəkil ölçüsünü və formatını əldə etmək üçün pas kitabxanası. Dəstəkləyir [.avif](/image/avif/), [.bmp](/image/bmp/), [.cur](/image/cur/), [.dds](/image/dds/), [ .gif](/image/gif/), hdr (şəkil), [heic (heif)](/image/heic/), [.icns](/image/icns/), [.ico](/image/ ico/), [.jp2](/image/jp2/), [jpeg (jpg)](/image/jpeg/), [jpx](/image/jpx/), ktx, [png](/image/ png/), [psd](/image/psd/), qoi, tga, tiff (tif) və webp.
 * **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - HdrHistogramın Java tətbiqi.

## İstinadlar

 * [Radiance HDR](http://paulbourke.net/dataformats/pic/)
 * [imageinfo](https://github.com/xiaozhuai/imageinfo)

