{
  "date": "2022-04-01",
  "keywords": [
"nkit faylı",
"nkit fayl formatı",
"nkit faylı nədir",
"fayl",
"nkit nümunəsi",
"nkit fayl uzantısı",
"uzadılması",
"format",
"nkit altbilgisi",
"nkit fayl formatı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "NKIT fayl formatı və NKIT fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "NKIT - Disk Şəkil Fayl Formatı",
  "linktitle": "NKIT",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-nki-azt"
}
},
  "lastmod": "2022-04-01"
}

## NKIT faylı nədir?

NKIT faylı NintendoWii və GameCube oyunlarından çıxarılan məlumatların disk şəklidir. NKIT Nintendo Toolbar formatı üçündür. Nəticə sıxılma [ISO](/compression/iso/) faylı Dolphin, Swiss və Nintendont kimi emulyator proqramları ilə işləmək üçün bu oyunların əsas məlumatlarından istifadə edir. NKit xam (iso) və ya sıxılmış (gcz) fayl formatlarında gəlir ki, bu formatlar həm oynanma qabiliyyətini, həm də ölçüsünü nəzərə alaraq hazırlanmışdır.

## NKIT fayl formatı

NKit fayl formatı itkisiz formatdır və Nintendo Wii və GameCube şəkillərini kiçiltmək və bərpa etmək üçün istifadə olunur. Formatlar GameCube və Wii oyunlarının hər biri üçün ISO və GCZ fayl formatlarında mövcuddur.

|Sistem |Format |Dəstəklənən Aparat |Delfin Dəstəyi |Bərpa edilə bilən 1:1 |Qeydlər|
---|---|---|---|---|---|
|GameCube| nkit.iso| Bəli |Bəli| Bəli |Yığılmış GameCube iso ilə eyni|
|GameCube| nkit.gcz| Xeyr| Bəli| Bəli |GCZ Dolphinin öz blok axtara bilən sıxılma formatıdır|
|Wii| nkit.iso| Xeyr Bəli| Bəli| RVT-H formatı yalnız Dolphin|-də oxuna bilər
|Wii| nkit.gcz| Xeyr Bəli| Bəli| GCZ-də RVT-H yalnız Dolphin-də oynana bilər|

### NKIT Başlığı

NKIT fayl formatının başlığı aşağıdakı kimidir.

|Offset |Uzunluq |Ad|
---|---|---|
|0x200 |0x4 |NKit Başlığı 'NKIT'|
|0x204 |0x4 |NKit Version ' v01'|
|0x208 |0x4 |Mənbə şəkli orijinal CRC32|
|0x20C |0x4 |NKit CRC - NKit CRC32 faylını 0x208-də (GCZ-də 0x4-də) mənbə CRC-yə bərabər edir|
|0x210 |0x4 |Mənbə şəklinin uzunluğu|
|0x214 |0x4 |Məcburi Lazımsız İD (Disk ID-si fərqli olduqda - nadir - yalnız GameCube)|
|0x218 |0x4 |Konvertasiya zamanı çıxarılarsa, Wii CRC32 bölməsini yeniləyin|

## İstinadlar ##

* [NKIT Fayl Format - gbatemp tərəfindən](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)


