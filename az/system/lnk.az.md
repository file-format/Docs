{
  "date": "2021-07-15",
  "keywords": [
"LNK",
"uzadılması",
"fayl",
"format",
"sistemi",
"LNK faylı",
"keçid",
"LNK faylları",
"LNK sənədləri",
"tətbiq",
"proqramlar"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "LNK - Link fayl formatı",
  "description": "LNK faylları yarada və aça bilən LNK fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "LNK",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-ln-azk"
}
},
  "lastmod": "2021-07-15"
}

## LNK faylı nədir? ##

Mac sistemindəki identifikasiyanın analoqu olan LNK faylı orijinal şəkil sənədi qovluğu və ya proqramı ilə əlaqə kimi xidmət edən Windows alternatividir və ya linkdir. O, qısayol təyinat yerinin növünü, mövqeyini və fayl adını, həmçinin hədəf sənədi açan proqram və əlavə qısayol düyməsini ehtiva edir.

Windows-da birbaşa faylı, qovluğu və ya icra olunan proqramı seçin və Qısayol yarat seçin. Fayl formatının yeri və Başlanğıc” kataloqu LNK fayllarının iki əsas xüsusiyyətidir. LNK fayllarının fayl formatı maskalanır və əyri ox onların qısa yol olduğunu göstərir.

## LNK Fayl Format ##

LNK fayl formatları adətən təyinat faylları ilə eyni işarəyə malikdir, lakin faylın başqa yerə işarə etdiyini göstərmək üçün bir az əyilmiş ox əlavə olunur. Qısayol iki dəfə kliklədikdə, istifadəçi faktiki faylı iki dəfə klikləmiş kimi davranır.

Tətbiq qısa yollarını ehtiva edən LNK faylları proqramın işləməsinə təsir edən xüsusiyyətlərə malik ola bilər. Atributları dəyişdirmək üçün qısayol faylına sağ klikləyin və **Xüsusiyyətlər**-i seçin, sonra Hədəf sahəsini dəyişdirin.

Fayl uzantıları olmaq əvəzinə, LNK faylları Windows Explorer genişləndirmələridir. Terminal uzantısı olaraq, .lnk sənədləri yalnız Windows Explorer-də faylı əvəz etmək üçün istifadə edilə bilər və onlar yerli sənədə qısa yol kimi xidmət etməklə yanaşı, Windows Explorer-də başqa məqsədlərə malikdir. Bu fayllar da L hərfi ilə başlayır.

Qısayollar yaradılan zaman xüsusi fayl və qovluqlara bağlansa da, hədəf başqa yerə dəyişdirilərsə, onlar işləməyə bilər. Explorer açılan zaman ölü hədəfə işarə edən qısayol qovluğunu təmir etməyə başlayacaq.


## Texniki Spesifikasiya ##

Yalnız Tanınmış fayl növləri üçün genişləndirmələri gizlət qovluğuna baxış parametri seçilmədikdə, Windows sənəd qısa yolları üçün .lnk sənəd uzantısını göstərmir. Tövsiyə olunmasa da, HKEY_CLASSES_ROOT\lnk faylının Windows reyestr elementindən NeverShowExt xassəsini silməklə fayl uzantısının göstərilməsini təmin edə bilərsiniz.

Bunu etmək üçün bu addımları yerinə yetirin:

* Tapşırıq çubuğunun axtarış sahəsinə Regedit daxil edərək və proqramı seçərək Qeydiyyat Redaktorunu açın
* Tətbiqdə Kompüter\HKEY HKEY_CLASSES_ROOT\lnkfayl məkanına keçin
* Elementin ehtiyat nüsxəsini yaradın, üzərinə sağ klikləyin və İxrac seçin
* NeverShowExt atributunu seçin və silin
* Windows yenidən başlamalıdır


## İstinad ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
