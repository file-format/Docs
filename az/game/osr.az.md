{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"OSR fayl formatı və OSR faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title" : "OSR Faylı - osu! Fayl Formatını Təkrar Oynat",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-az",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## OSR faylı nədir?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**OSR Fayl Formatının MIME Növü:** x-osu-replay

## OSR fayl formatı

OSR faylları sabit, eləcə də dəyişən uzunluqlu məlumat sahələri ilə ikili fayllar kimi saxlanılır.

|Məlumat növü| Format|
---|---|
|Bayt |Təkrarın oyun rejimi (0 = osu! Standart, 1 = Taiko, 2 = Beat'i tut, 3 = osu!mania)|
|Tam |Təkrar yaradılan oyunun versiyası (məs. 20131216)|
|String |osu! beatmap MD5 hash|
|String| Oyunçunun adı|
|String| osu! replay MD5 hash (təkrarın müəyyən xüsusiyyətləri daxildir)|
|Qısa| 300-lərin sayı|
|Qısa| Standartda 100-lərin sayı, Taiko-da 150-lər, CTB-də 100-lər, maniyada 100-lər|
|Qısa| Standartda 50-lərin sayı, CTB-də kiçik meyvələr, maniyada 50-lər|
|Qısa| Standartda Gekis sayı, Maniada Maks 300s|
|Qısa| Standartda Katusların sayı, manidə 200s|
|Qısa| Buraxılanların sayı|
|tam| Hesab hesabatında göstərilən ümumi xal|
|Qısa| Hesab hesabatında göstərilən ən böyük kombin|
|bayt| Mükəmməl/tam kombinasiya (1 = buraxılış və sürüşmə fasilələri və erkən bitmiş sürgülər yoxdur)|
|tam| İstifadə olunan modlar. Mod dəyərlərinin siyahısı üçün aşağıya baxın.|
|String| Həyat zolağı qrafiki: vergüllə ayrılmış u/v cütləri, burada u mahnıya daxil olan millisaniyələrdə vaxtdır və v verilmiş vaxtda istifadə etdiyiniz ömrü əks etdirən 0-1 arasında dəyişən nöqtə dəyəridir (0 = həyat zolağı boş, 1= həyat çubuğu doludur)|
|Uzun| Vaxt möhürü (Windows işarələri)|
|tam| Sıxılmış təkrar məlumatların baytlarında uzunluq|
|Bayt |Masiv Sıxılmış təkrar oxunuş məlumatları|
|Uzun| Onlayn Hesab ID|
|İkiqat| Əlavə mod məlumatı. Yalnız Hədəf Təcrübəsi aktiv olduqda mövcuddur.|

## İstinadlar

* [OSU! Ritm Oyunu](https://osu.ppy.sh/home)

* [OSR Fayl Format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


