{
  "date": "2021-06-29",
  "keywords": [
"CUR",
"uzadılması",
"fayl",
"format",
"şəkil",
"Cihazdan Müstəqil Bitmap",
"Kursor fayl formatı",
"Kursor",
"Windows",
"tətbiq"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CUR - Kursor Fayl Formatı",
  "description": "CUR faylları yarada və aça bilən CUR fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "CUR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-cu-azr"
}
},
  "lastmod": "2021-06-29"
}

## CUR faylı nədir? ##

CUR faylı statik Microsoft Windows kursor fayl formatıdır. Əsasən, onlar uzantıdan başqa hər cəhətdən ICO (ikon) faylları ilə eyni olan stasionar şəkillərdir. Həm CUR, həm də [ICO](/image/ico/) Cihazdan Müstəqil Bitmap [DIB](/image/dib/) (Cihazdan Müstəqil Bitmap) spesifikasiyası əsasında qurulub. Defolt, həmçinin Windows əməliyyat sistemi üçün Windows siçan göstəricisi kimi xüsusi kursor CUR fayllarında saxlanılır. Bu, normal istifadə üçün ox, gözləmə müddətlərini göstərmək üçün fırlanan qum saatı və ya mətnin redaktəsi üçün I-bar ola bilər. CUR faylları, Windows kursorunun fərdi masa üstü mövzusuna uyğun olmasını təmin etmək üçün xüsusi masa üstü mövzularının quraşdırma paketi ilə birlikdə gəlir.

## Texniki Spesifikasiya ##

CUR faylları Microsoft Windows əməliyyat sistemində işləyən cihazlarda tapıla bilən ikili sistem fayllarıdır. CUR göstərici şəkilləri 16×16, 32×32 və s. kimi müxtəlif standart ölçülərdə olur. CUR faylları ICO fayllarına çox oxşardır; onların hər ikisi kiçik stasionar təsvirlərdən ibarətdir. Yalnız CUR və ICO fayllarının genişləndirilməsi fərqlidir. Bundan əlavə, CUR faylının başlığında qaynar nöqtənin izahı ICO faylından fərqlidir. Qaynar nöqtə yuxarı sol küncdən siçanı göstərdiyiniz yerə qədər piksel ofsetini şərh edir. Windows sistemləri hələ də CUR fayllarından istifadə edir, lakin indi cizgi kursorları adətən CUR əvəzinə ANI fayl uzantısına malikdir.

## Qısa tarix ##

CUR faylı ICO faylından hazırlanır. İlk CUR fayl formatı kommersiya istifadəsini asanlaşdırmaq üçün 1981-ci ildə Microsoft-un Windows 1.0 əməliyyat sisteminə daxil edilmişdir. Tezliklə istifadəçilərə əvvəlcədən quraşdırılmış seçimlərdən kursor seçimlərini dəyişdirməyə imkan verən daha çox interaktiv kursorlar təqdim edildi. Bununla belə, kifayət qədər texniki məlumatınız olmasa belə, CUR faylını təkbaşına redaktə etmək asandır.


## CUR Nümunəsi ##

CUR faylları *C:\Windows\Cursors* ünvanında tapıla bilər:

{{< figure src="../cur.png" alt="CUR fayl formatı" >}}

