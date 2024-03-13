{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"CSD Steam Game Data Backup Fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title" : "CSD Fayl Format - Buxar Oyunu Məlumat Yedəkləmə Faylı",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd-az",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## CSD faylı nədir?

CSD faylı istifadəçilərə **Valve** oyunlarını endirməyə və idarə etməyə imkan verən **Steam** oyun xidməti tərəfindən yaradılan oyunun ehtiyat faylıdır. O, silinmiş oyunu bərpa etmək üçün istifadə oluna bilən oyunlarla bağlı ehtiyat məlumatları ehtiva edir. Steam oyunu CSD faylından yalnız oyun Steam vasitəsilə endirilib, quraşdırılıb və yamaqlaşdırılıbsa bərpa edə bilər. Oyunu CSD faylından bərpa etmək üçün Steam → Backup and Restore Gamesteam seçimindən istifadə edin və faylı seçin.

## CSD Fayl Format - Ətraflı Məlumat

CSD fayl formatının daxili strukturu ictimaiyyətə açıq deyil və onun fayl formatının spesifikasiyası tərtibatçının arayışı üçün mövcud deyil. CSD faylları Steam oyun fayl formatları olan CSM və ISS faylları ilə müşayiət olunur.

### Buxar Yedək Fayllarını Harada Tapmaq olar?

Bütün Steam ehtiyat faylları aşağıdakı yerlərdə tapıla bilər:

 * C:\Proqram Faylları (x86)\Steam\steamapps\common\<game name> \ :
 * \cfg\ - Xüsusi konfiqurasiyalar və konfiqurasiya skriptləri
 * \downloads\ - Çox oyunçulu oyunlar üçün fərdi məzmun
 * \maps\ - Çox oyunçulu oyunlar zamanı quraşdırılmış və ya endirilmiş xüsusi xəritələr
 * \materiallar\ - Xüsusi teksturalar və dərilər
 * \SAVE\ - Tək oyunçu ilə yadda saxlanılan oyunlar

Bununla belə, üçüncü tərəfin yaratdığı oyunların yeri fərqli ola bilər və oyunun tərtibatçısı tərəfindən müəyyən edilir.

### CSD Yedək faylından bərpa edilir

Steam-i quraşdırın və düzgün Steam hesabına daxil olun (əlavə təlimatlar üçün Steam-in quraşdırılmasına baxın)
 * Steam-i işə salın
 * Steam tətbiqinin yuxarı sol küncündə Steam düyməsini basın
 * Oyunların ehtiyat nüsxəsini çıxarın və bərpa edin... seçin.
 * Əvvəlki ehtiyat nüsxəsini bərpa et seçin
 * Oyunun ehtiyat fayllarının yerləşdiyi yerə baxın
 * Lazımi oyunları quraşdırmaq üçün Steam pəncərələrində davam edin.

## İstinadlar

 * [Buxar Yedəkləmə Xüsusiyyətindən İstifadə](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

