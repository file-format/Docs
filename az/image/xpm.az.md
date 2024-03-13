{
  "date": "2019-10-11",
  "keywords": [
"xpm faylı",
"xpm fayl formatı",
"xpm faylı nədir",
"fayl",
"xpm nümunəsi",
"xpm fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XPM - X PixMap Fayl Format",
  "description": "XPM faylları yarada və aça bilən XPM fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "XPM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-xp-azm"
}
},
  "lastmod": "2019-09-10"
}

## XPM faylı nədir?

.xpm uzantısı olan fayl X Windows Sistemi tərəfindən istifadə edilən şəkil fayl formatıdır. Şəffaf pikselləri dəstəkləyir və adətən ikon piksel xəritələrinin yaradılmasını hədəfləyir. O, monoxrom, miqyaslı və rəngli pixmap məlumatlarını dəstəkləyir. Bunlar əl ilə redaktə olunmaq üçün nəzərdə tutulmuşdur və [C](/programming/c/) koduna daxil edilə bilər. Bu məqsədlə XPM faylları düz mətn faylı formatındadır və C proqramlaşdırma dili sintaksisinə əməl edir. XPM faylları müxtəlif şəkillərə baxmaq proqramları ilə açıla bilər
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView və Canvas X.

## XPM fayl formatı

XPM fayl formatı onların C və C++ proqramlarına inteqrasiyası üçün C sintaksisindən istifadə edir. Aşağıdakı altı müxtəlif bölmədən ibarətdir.

 * \<Values>
 * \<Colors>
 * \<Pixels>
 * \<Extensions>

Bölmələr əslində aşağıdakı kimi sətirlər massividir.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Aşağıda hər bölmənin təfərrüatları verilmişdir.

`<Values> ` - Bu bölmə 10-cu bazada olan və aşağıdakılara uyğun gələn dörd və ya altı tam ədəddən ibarət sətirdir:

 * pixmap eni və hündürlüyü
 * Rənglərin sayı
 * piksel başına simvolların sayı
 * isteğe bağlı hotspot koordinatları və XPMEXT etiketi

`<Colors> ` - Bu bölmədə rənglərin sayı qədər sətir var. Hər bir sətir aşağıdakı kimidir:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Bu bölmə ibarətdir<height> simlər və<width> \*<chars_per_pixel> personajlar. Hər<chars_per_pixel> uzunluq sətri əvvəlcədən müəyyən edilmiş qruplardan biri olmalıdır<Colors> bölmə.

`<Extension> ` - Genişləndirmə bölməsi boş deyilsə, etiketlənməlidir<Values> bölmə. Bir neçədən ibarət ola bilər<Extension> aşağıdakı iki növ ola bilən alt bölmələr:

 * bir tək sətir aşağıdakı kimi tərtib edilmişdir: XPMEXT<extension-name><extension-data>
 * və ya bir neçə sətirdən ibarət blok: XPMEXT<extension-name><related extension-data composed of several strings>

## İstinadlar

* [XPM - Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)

* [XPM Manual](http://www.xfree86.org/current/xpm.pdf)


