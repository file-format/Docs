{
  "date": "2019-10-11",
  "keywords": [
"ico faylı",
"ico fayl formatı",
"ico faylı nədir",
"fayl",
"ico misal",
"ico fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ICO - Şəkil fayl formatı",
  "description": "ICO faylları yarada və aça bilən ICO fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "ICO",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ic-azo"
}
},
  "lastmod": "2019-09-10"
}

## ICO faylı nədir?

ICO uzantısı olan fayllar [Microsoft Windows](https://www.microsoft.com/en-us/windows) üzərindəki tətbiqin təsviri üçün ikona kimi istifadə edilən şəkil fayl növləridir. Bunlar displeyin tələblərinə uyğun olaraq müxtəlif ölçüdə, rəng dəstəyi və qətnamə ilə gəlir. Microsoft Windows-da başqa oxşar şəkil faylı formatı kursor təmsili üçün [CUR](/image/cur/)-dir və şəkil başlığında qaynar nöqtəni təyin edir. MacOS-da ICNS fayl formatları ICO faylları ilə eyni məqsədə xidmət edir. Bir sıra onlayn veb-saytlar, eləcə də proqramlar bu cür faylların yaradılması və [BMP](/image/bmp/), [PNG](/image/png/) və s. kimi digər şəkil formatlarını ikon fayl formatına çevirmək funksiyasını təmin edir. ICO faylları üçün rəsmi IANA qeydiyyatdan keçmiş İnternet media növü image/vnd.microsoft.icon-dur.

## Qısa tarix ##

Icons were introduced with the launch of Microsoft Windows 1.0. Bunlar 32x32 ölçüdə və monoxrom idi. Win32-nin gəlişi ilə, ölçüsü 256x256 pikselə qədər olan həqiqi rəngli ikon şəkillərinə dəstək təqdim edildi. Windows XP ilk olaraq 32-bit rəngli ikona şəkillərini dəstəkləməklə, kölgələr, anti-aliasing və şüşə kimi effektlər kimi yarı şəffaf sahələrin simvola əlavə edilməsinə imkan yaradıb. Microsoft yalnız Windows XP üçün 48×48 pikselə qədər işarə ölçülərini tövsiyə etmişdir. Windows Vista Windows Explorer-ə 256×256 piksel ikona görünüşünü əlavə etdi, həmçinin sıxılmış [PNG](/image/png/) formatını dəstəklədi. Daha yüksək qətnamə və yüksək DPI rejimlərindən istifadə edən istifadəçilərlə daha böyük ikon formatları (məsələn, 256×256) tövsiyə olunur.

## ICO Fayl Format ##

Tək ICO faylı birdən çox ölçülü və rəng dərinliyi olan bir və ya birdən çox kiçik təsvirdən ibarətdir. Çox ölçülü şəkillərin olması müxtəlif ekran qətnamələrində müvafiq miqyaslama üçündür. ICO/CUR fayllarında bütün dəyərlər [little-endian](https://en.wikipedia.org/wiki/Little-endian) bayt sırası ilə təmsil olunur.

ICO faylı Icon başlığından, Icon Directory,

|Sahə|Təsvir
---|---|
|Icon Header|ICO faylı haqqında ümumi məlumatı saxlayır.
|Directory[1..n]|Fayldakı hər bir şəkil haqqında ümumi məlumatı saxlayır.
|Icon #1|Köhnə AND/XOR DIB formatında və ya daha yeni PNG-də ilk şəkil üçün faktiki məlumat
|...|
|Icon #n|Sonuncu ikon şəkli üçün məlumatlar

### Başlıq ###

|Ofset|Ölçü (baytla)|Məqsəd
---|---|---|
|0|2|Ehtiyatdadır. Həmişə 0 olmalıdır.
|2|2|Şəkil növünü müəyyən edir: ikon (.ICO) şəkli üçün 1, kursor (.CUR) şəkli üçün 2. Digər dəyərlər etibarsızdır.
|4|2|Fayldakı şəkillərin sayını müəyyən edir.

### Kataloq ###

ICONDIR strukturu kimi təqdim olunan ICO faylında olan kataloq fayldakı hər bir şəkil üçün ICONDIRECTORY strukturunu ehtiva edir. Eyni şəkildə bütün təsvir bitmap məlumatlarının bitişik bloku izlənilir. Bu, aşağıda göstərildiyi kimidir.

|Ofset|Ölçü|Təsvir
---|---|---|
|0 (0)|1|256 piksel olarsa, eni 0 olmalıdır
|1 (1)|1|Hündürlük, 256 piksel olarsa, 0 olmalıdır
|2 (2)|1|Rəng sayı, 256 rəngdən çox olduqda 0 olmalıdır
|3 (3)|1|Ehtiyatdadır, 0 olmalıdır
|4 (4)|2|.ICO formatında olduqda rəng müstəviləri 0 və ya 1, yaxud .CUR formatında olduqda X qaynar nöqtə olmalıdır
|6 (6)|2|.ICO formatında olduqda piksel başına bit və ya .CUR formatında olduqda Y hotspot
|8 (8)|4|Bitmap məlumatının baytlarla ölçüsü.
|12 (C)|4|Faylda ofset.

## İstinadlar ##

* [ICO - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/ICO_(file_format))

* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)


