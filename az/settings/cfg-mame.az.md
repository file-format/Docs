{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg faylı",
"cfg mame konfiqurasiya faylı",
"cfg faylı nədir",
"cfg faylını necə açmaq olar",
"fayl",
"cfg fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CFG Fayl Format - MAME Konfiqurasiya Faylı",
  "description": "CFG MAME Konfiqurasiya Faylı formatı və CFG fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame-az",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## CFG faylı nədir?

CFG faylı MAME arcade video oyun emulyatorları tərəfindən istifadə edilən XML klaviatura konfiqurasiya faylıdır. O, klaviatura idarəetmələrini və isti düymələri oyunçunun seçimlərinə uyğunlaşdırmaq üçün vacib komponentdir. Bu fayllar oyun oynayarkən klaviaturanın emulyatorla necə qarşılıqlı əlaqədə olduğunu müəyyən edən xəritələr və parametrləri saxlayır. Bu faylı redaktə etməklə, istifadəçilər sikkə daxil etmək, işə salmaq, hərəkət etdirmək və digər müxtəlif funksiyalar kimi oyun daxilində fəaliyyətlərə xüsusi klaviatura düymələri təyin etməklə oyun təcrübəsini uyğunlaşdıra bilərlər.

## MAME Konfiqurasiya Faylı

**Multiple Arcade Machine Emulator** mənasını verən MAME, kompüterinizdə arcade oyunlarını təqlid etməyə və oynamağa imkan verən proqram proqramıdır. MAME davranışını və parametrlərini fərdiləşdirmək üçün konfiqurasiya fayllarından istifadə edir. Bu konfiqurasiya faylları adətən MAME kataloqunuzdakı `cfg` qovluğunda yerləşir.

MAME-ni qurarkən və konfiqurasiya edərkən qarşılaşa biləcəyiniz əsas konfiqurasiya faylları bunlardır:

1. **mame.ini:** Bu MAME üçün əsas konfiqurasiya faylıdır. O, bütün oyunlara aid olan qlobal parametrləri ehtiva edir. Bu faylı MAME quraşdırmanızın kök kataloqunda tapa bilərsiniz.

1. **default.cfg:** Bu fayl öz konfiqurasiya faylları olmayan bütün oyunlar üçün standart parametrləri saxlayır. O, oyuna xas parametrlər üçün ehtiyat kimi istifadə olunur.

1. **game-specific.cfg:** Bu fayllar fərdi oyunlar üçün parametrləri saxlamaq üçün istifadə olunur. Onlar adətən uyğun olduqları oyun üçün ROM faylının adını daşıyırlar. Məsələn, pacman.zip adlı oyununuz varsa, onun konfiqurasiya faylı pacman.cfg olacaqdır.

MAME konfiqurasiya faylında tapa biləcəyiniz bəzi ümumi parametrlər bunlardır.

1. **rompath:** Arcade oyun ROM-larınızın yerləşdiyi kataloqu müəyyənləşdirir.

1. **cfg_directory:** Oyuna aid konfiqurasiya fayllarının saxlandığı qovluğu müəyyən edir.

1. **nvram_directory:** Qeyri-uçucu RAM (NVRAM) fayllarının saxlandığı qovluğu müəyyən edir. NVRAM yüksək balları və digər oyuna aid məlumatları saxlayır.

1. **artwork_directory:** İncəsənət fayllarının (məsələn, çərçivələr, marquees və flayerlər) saxlandığı qovluğu müəyyən edir.

1. **samplepath:** Nümunə səs fayllarının yerləşdiyi kataloqu müəyyən edir.

1. **cheatpath:** Fırıldaqçı faylların yerləşdiyi kataloqu müəyyənləşdirir.

Siz həmçinin video və audio seçimləri, idarəetmə elementləri və daxiletmə cihazları kimi müxtəlif digər parametrləri konfiqurasiya edə bilərsiniz. Bu parametrləri dəyişdirmək üçün mətn redaktorunda konfiqurasiya faylını aça və lazımi dəyişikliklər edə bilərsiniz.

## MAME

**Çoxlu Arkada Maşın Emulatoru** mənasını verən MAME, köhnə arcade maşınlarının və arcade oyun konsollarının avadanlığını təqlid etmək və təkrarlamaq üçün nəzərdə tutulmuş proqram təminatıdır. O, istifadəçilərə müasir kompüterlərdə və digər uyğun cihazlarda klassik arcade oyunlarının geniş kitabxanasını oynamağa imkan verir. MAME açıq mənbəli layihədir və arcade oyunlarının zəngin tarixini qorumaq və ondan həzz almaq üçün əsas emulyatora çevrilmişdir.

1. **Emulyasiya:** MAME-nin əsas məqsədi arcade maşınlarının aparatlarını, o cümlədən onların mərkəzi prosessorları (CPU), səs çipləri, qrafik çipləri və daxiletmə qurğularını dəqiq şəkildə təqlid etməkdir. Bu dəqiqlik səviyyəsi oyunların orijinal arcade təcrübəsinə mümkün qədər yaxın davranmasını təmin edir.

1. **Compatibility:** MAME supports wide range of arcade game ROMs, making it one of most comprehensive arcade emulators available. It can run games from various arcade platforms including classic games from '70s, '80s, '90s, and even some more recent arcade titles.

1. **Mühafizə:** MAME-nin əsas missiyalarından biri arcade oyunlarının tarixini qorumaqdır. Arcade aparatını dəqiq şəkildə təqlid edərək, MAME klassik oyunların itirilməsinin qarşısını alır və gələcək nəsillərin onları ilkin nəzərdə tutulduğu kimi yaşamasını təmin edir.

1. **Front-Ends:** Bir çox istifadəçi MAME vasitəsilə oyunları idarə etmək və işə salmaq üçün qrafik interfeysi təmin edən qabaqcıl proqramlardan istifadə edir. Bu ön hissələr MAME-nin geniş oyun kitabxanasında naviqasiyanı asanlaşdırır.

## CFG faylını necə açmaq olar?

CFG fayllarını açan və ya onlara istinad edən proqramlar

- MAME (Pulsuz) (Windows)
- ExtraMAME (Sınaq)
- MacMAME (MAC)

## Digər CFG faylları

**.cfg** fayl uzantısından istifadə edən digər fayl növləri bunlardır.

**Parametrlər**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Oyun**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**Sistem və Müxtəlif**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## İstinadlar
* [MAME](https://en.wikipedia.org/wiki/MAME)


