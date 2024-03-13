{
  "date": "2021-08-24",
  "keywords": [
"wdb faylı",
"wdb fayl formatı",
"wdb faylı nədir",
"fayl",
"wdb nümunəsi",
"wdb fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "WDB fayl formatı və WDB fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "WDB - SQL Server İz Faylı",
  "linktitle": "WDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-wd-azb"
}
},
  "lastmod": "2021-08-24"
}

## WDB faylı nədir?
.wdb uzantısı olan fayl əslində Microsoft Works tərəfindən yaradılmış verilənlər bazası faylıdır və verilənlər bazası idarəetmə sistemi kimi funksiyaları yerinə yetirmək üçün istifadə olunur. WDB faylı Access Database ([MDB](/database/mdb/)) faylına bənzəyir, lakin daha az səmərəli və daha böyük məhdudiyyətlərə malikdir. WDB faylları Microsoft Access istifadə edərək açıla bilməz. Bununla belə, siz WDB faylını Microsoft Works-də aça və sonra MS Access-də WDB faylını açmaq üçün onu MDB faylına ixrac edə bilərsiniz.

## WDB fayl formatı
Microsoft Works Database Microsoft Works ofis paketinin yerli verilənlər bazası formatıdır. Formatın mülkiyyət xarakterinə və bəzi məhdudiyyətlərə görə. WDB faylları Microsoft Works-dən başqa heç bir proqramda açıla bilməz. Fayl formatında təkrarlanan, 10 baytlıq başlıq ASCII mətn sətirlərinin hər birinin qarşısında NULL dəyəri ilə dayandırılmış sahələrin dəyərlərini əks etdirən tapıla bilər. Başlıq ümumiyyətlə **\x0f** bayt və NULL ilə başlayır, ardınca NULL ilə əvəzlənən 4 məlumat baytı gəlir.

### Fayl strukturu

WDB faylının strukturu aşağıda verilmişdir:
- **1-ci başlıq**: faylın əvvəlindən \x25\x00\xf2 və 244 NULL baytla bitən
- **2-ci başlıq**: \xffT - yəni \xff\x54 ilə başlayan və 4096 bayta uzanan, sütun/sahə adlarını və başqa şeyləri ehtiva edir və 6144 bayt mövqeyindən başlayır.
- **Field**: value has a 10 byte header, with the following format: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3, part 2} {db 4} \x00. məlumat baytı 2 sahə nömrəsidir, məlumat baytı 3 qeyd nömrəsidir (məlumat baytı 3, 256 qeyddən çox olduqda 2-ci hissə əlavə olunur).


## İstinadlar ##

* [İstifadəçi:JesseW/wdb formatı](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)


