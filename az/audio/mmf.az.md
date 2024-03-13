{
  "date": "2021-08-09",
  "keywords": [
"mmf",
"fayl",
"uzadılması",
"format",
"audio",
"smaf",
"mmf uzantısı",
"mmf faylları",
"Mobil musiqi faylı",
"yamaha"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "MMF fayl formatı və MMF fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "MMF - Mobil Musiqi Fayl Formatı",
  "linktitle": "MMF",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-mm-azf"
}
},
  "lastmod": "2021-08-09"
}

## MMF faylı nədir?

MMF SMAF faylı ilə əlaqəli fayl uzantısıdır. MMF Mobil Musiqi Faylı, SMAF isə sintetik musiqi Mobil Tətbiq Formatını ifadə edir. Smartfondakı MMF faylları sistem zəng melodiyalarını, səsləri ehtiva edir və həmçinin qrafika və mətn displeyini ehtiva edə bilər. MMF əlavə olaraq FM, PCM və Stream PCM daxil olmaqla üç növ alət parametrlərini ehtiva edir. Bu fayl formatları Windows sistem platforması ilə uyğun gəlir. MMF faylları məlumat faylları kimi təsnif edilir. Adətən Microsoft Mail MMF fayllarını dəstəkləyir. MMF şəkilçisi olan fayl istənilən mobil cihaza və ya sistem platformasına kopyalana bilər.

Üstəlik, bu fayllar standart MIDI format faylları ilə müqayisədə ölçü baxımından çox kiçikdir. [WAV](/audio/wav/) və [MID](/audio/mid/) faylları MMF formatına çevrilə və sonra audio məzmun kimi paylaşıla və paylana bilər. Bu fayllar e-poçt vasitəsilə birbaşa telefonlara və kompüterə qəbul edilə bilər.


## MMF Fayl Formatının Qısa Tarixi

Yamaha SMAF alətlərini səs faylları kimi işləyib hazırlayıb ki, smartfonlar daha çox sayda unikal zəng melodiyasını saxlaya bilsin. Yamaha SMAF-ı MA-1, MA-2, MA-3, MA-5 və MA-7 LSI səs çiplərinin istehsalı ilə təqdim etdi. Bütün bu formatlar 2000-ci ilin əvvəllərində Şərqi Asiya Bazarında mobil telefonlar arasında kifayət qədər tanış oldu.

Beynəlxalq səviyyədə MMF formatına Samsung tərəfindən icazə verilmişdir. MMF formatının köməyi ilə Samsung, Samsung smartfonlarında istifadə olunmaq üçün geniş çeşiddə polifonik zəng melodiyalarını dizayn edə bildi.

Yamaha rəsmi Yamaha SMAF fayllarında formatı daha da populyarlaşdırmaq istədi və bu formata uyğun daha çox alət nəşr etdi. Bununla istifadəçilər MMF fayllarını kompüterlərində asanlıqla oynaya bilərlər.


## MMF Fayl Formatının Xüsusiyyətləri ##

MMF faylları məlumat bölmələrinə təsnif edilir. Hər bir seqmenti təsvir etmək üçün 8 bayt ətrafında prefiksli struktur istifadə olunur.
4 baytlıq etiketə CNTI, OPDA, MSTR, MTR və ATR daxildir. Məlumat ölçüsü plus 8 bayt yığın ölçüsüdür; bütün fayl ölçüsü bütün yığın ölçülərinin cəmlənməsi ilə hesablanır. Əgər fayl zədələnməyibsə, cəmlənmiş fayl ölçüsü əsas başlıq ölçüsü ilə eyni olmalıdır.

### Başlıq ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

MMF faylının bir nümunəsidir:

![](../mmf.png)

## İstinadlar

* [MMF - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)


