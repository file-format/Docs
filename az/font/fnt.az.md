{
  "date": "2020-08-20",
  "keywords": [
"fnt faylı",
"fnt fayl formatı",
"fnt faylı nədir",
"fayl",
"fnt nümunəsi",
"fnt fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FNT - Windows şrift faylı",
  "description": "FNT fayl formatı və FNT fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "FNT",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-fn-azt"
}
},
  "lastmod": "2020-10-30"
}

## FNT faylı nədir?

.fnt uzantılı fayl Windows Əməliyyat sistemlərində ümumi şrift məlumatlarını saxlayan şrift faylıdır. FNT faylları əsasən TrueType (.TTF) və OpenType (.OTF) fayl formatları ilə əvəz edilmişdir və indi köhnəlmiş şrift fayl formatıdır. Bu fayllar tək qiymətləndirici və ya vektor şriftini saxlaya bilər. Bütün cihaz sürücüləri Windows 2.x şriftlərini dəstəkləyir. Bununla belə, bütün cihaz sürücüləri deyil
Windows 3.0 versiyasını dəstəkləyir.

## FNT fayl formatı

FNT faylları tək rastr və ya vektor şriftini saxlamağa qadirdir. Vektor formatları, hər nizamnamənin qlifinin kiçik bir bitmapdan istifadə edərək müəyyən edildiyi rastrla müqayisədə GDI tərəfindən daha tez-tez istifadə olunur. .fnt-nin .ttf və .otf ilə əvəz edilməsinin aşkar səbəbi onun rastr formatıdır.

### Şrift faylının başlığı
Həm rastr, həm də vektor şrift fayllarının başlanğıcı ümumidir, ondan sonra hər bir fayl növü üçün müxtəlif məlumatlar verilir. Windows 3.0 üçün şrift faylı başlığına aşağıdakı kimi altı yeni sahə daxildir ki, bunlar Windows-un gələcək versiyaları ilə uyğunluğu təmin etmək üçün sıfıra bərabərdir.

 * dBayraqlar
 * dfAspace
 * dfBspace
 * dfCspace
 * dfColorPointer
 * dfReserved1

Windows 3.0 və 2.0 üçün başlıqlar haqqında ətraflı məlumat üçün [Microsoft KnowledgeBase Archive](https://jeffpar.github.io/kbarchive/kb/065/Q65123/) saytına daxil olun.

## İstinadlar
 * [Şrift Faylı Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
 * [Windows-da şrifti necə quraşdırmaq və ya silmək olar](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8- 7613-c76f-88d043b334b8)

