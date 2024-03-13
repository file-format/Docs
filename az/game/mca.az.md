{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "MCA fayl formatı və MCA faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "MCA - Minecraft Anvil Region Fayl Formatı",
  "linktitle": "MCA",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-aza"
}
},
  "lastmod": "2022-12-13"
}

## MCA faylı nədir?

Minecraft Anvil region fayl formatı məşhur **Minecraft** video oyununda Minecraft Dünyasının ərazi hissələrini saxlamaq üçün istifadə edilən məlumat saxlama formatıdır. Minecraft dünyası hər bölgənin hissələrə bölündüyü bölgələrdən ibarətdir. MCA fayl formatı oyun dünyasının müəyyən bir hissəsində blokların və obyektlərin yeri kimi böyük miqdarda oyun məlumatlarının səmərəli saxlanmasına imkan verir. Bütün dünya yaratmaq üçün MCA faylları digər MCA faylları ilə birləşdirilməlidir.

Oyun məlumatlarının saxlanması ilə yanaşı, Anvil region fayl formatı oyunçu məlumatları və metadata kimi müxtəlif digər məlumat növləri üçün də dəstəyi ehtiva edir. Bu, blokların, obyektlərin və digər oyun obyektlərinin yeri də daxil olmaqla, oyun dünyasının müəyyən bir hissəsini tam şəkildə yenidən yaratmaq üçün lazım olan bütün məlumatların səmərəli saxlanmasına imkan verir.

## MCA Fayl Format - Ətraflı Məlumat

Anvil region fayl formatı ikili faylda məlumatların saxlanması üçün iyerarxik ağaca bənzər struktur olan NBT (Named Binary Tag) formatının bir variantıdır. Bu, mürəkkəb məlumat strukturlarının yığcam və asanlıqla oxuna bilən formatda səmərəli saxlanmasına imkan verir.

### MCA faylında parçalar

Minecraft-da yığın, yaddaşa yüklənən və oyunçunun ekranında göstərilən oyun dünyasının 16x16x16 blok sahəsidir. Anvil bölgəsi fayl formatı müəyyən bir parça üçün bütün məlumatları bir faylda saxlayır, sonra lazım olduqda tez yaddaşa yüklənə bilər. Bu, hamar və qüsursuz oyun təcrübəsini təmin etmək üçün vacib olan oyun məlumatlarına səmərəli saxlama və sürətli çıxış imkanı verir.

### Kiçik MCA Fayl Ölçüsü

Anvil bölgəsi fayl formatının əsas xüsusiyyətlərindən biri onun sıxılma istifadəsidir. Bu, verilənlərin keyfiyyətini və ya əldə olunma sürətini itirmədən, böyük həcmdə məlumatların səmərəli saxlanmasına imkan verir. Bu, gzip sıxılması və yığın məlumatların sıxılması kimi müxtəlif üsullardan istifadə etməklə həyata keçirilir.

MCA fayllarının sıxılmış fayl formatı onu oyunun məlumatların saxlanması və idarəetmə sisteminin mühüm hissəsinə çevirir. Onun sıxılmadan səmərəli istifadəsi və müxtəlif məlumat növləri üçün dəstəyi səmərəli saxlamağa və oyun məlumatlarına tez daxil olmağa imkan verir, oyunçular üçün hamar və qüsursuz oyun təcrübəsini təmin edir.

## MCA Fayl Format Strukturu

MCA fayllarının daxili fayl formatı strukturu aşağıdakılardan ibarətdir:
 * Başlıq və a
 * Faydalı yük

### MCA Başlığı

MCA region faylının başlığı iki 4KiB cədvələ bölünmüş 8KiB başlığı ilə başlayır. Birinci cədvəl region faylının özündə olan hissələrin ofsetlərini ehtiva edir, ikinci cədvəl isə bu parçaların son yeniləmələri üçün vaxt ştamplarını təqdim edir.

### MCA yükü

MCA faydalı yükü hər bir yığın məlumatının dörd bayt uzunluğunda (böyük endian) sahəsi ilə başladığı hissələrdən ibarətdir. Bu sahə baytlarda qalan yığın məlumatlarının dəqiq uzunluğunu göstərir. Son hissənin məlumatları uzunluğu 4096B-dən çox olacaq şəkildə doldurulur. Son hissənin doldurulmadığı fayllar Minecraft tərəfindən qəbul edilmir.

## MCA fayllarını necə açmaq olar

Minecraft üçün pulsuz, açıq mənbəli redaktor olan MCEdit proqramından istifadə edərək MCA fayllarını aça və redaktə edə bilərsiniz. Rəsmi vebsaytdan [download MCEdit](https://www.mcedit.net/) edə və Anvil region faylınızın məzmununu açmaq və baxmaq üçün ondan istifadə edə bilərsiniz.

MCEdit quraşdırdıqdan sonra bu addımları yerinə yetirərək Anvil region faylınızı aça bilərsiniz:

 1. MCEdit proqramını işə salın və pəncərənin yuxarı sol küncündəki Açıq düyməsini sıxın.

 1. Açıq Dünya informasiya qutusunda Anvil region faylınızın yerinə gedin və onu seçin.

 1. Faylı MCEdit-də açmaq üçün Açıq düyməsini klikləyin.

 1. MCEdit faylı yükləyəcək və məzmununu əsas pəncərədə göstərəcək. Daha sonra Anvil region faylından verilənlərə baxmaq, redaktə etmək və çıxarmaq üçün MCEdit-dəki alətlər və funksiyalardan istifadə edə bilərsiniz.

## İstinadlar

* [Minecraft üçün Dünya Redaktoru](https://www.mcedit.net/)

* [Minecraft haqqında](https://www.minecraft.net/)

* [Region Fayl Formatı](https://minecraft.fandom.com/wiki/Region_file_format)


