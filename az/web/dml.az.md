{
  "date": "2021-05-25",
  "keywords": [
"DML",
"DML faylı",
"DML fayl formatı",
"DML fayl növü",
"fayl",
"növü",
"DML faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DML - DynaScript HTML Faylı",
  "description": "DML faylları yarada və aça bilən DML fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "DML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-dm-azl"
}
},
  "lastmod": "2021-05-25"
}

## DML faylı nədir?

.dml uzantılı fayl DyanScript ilə yaradılmış veb skript səhifəsi kodu faylıdır. DynaScript ECMAScript ilə uyğun gələn və digər skript dili ilə eyni xüsusiyyətlərin əksəriyyətini təmin edən dinamik [HTML](/web/html/) skript dilidir. Bu ColdFusion koduna və Microsoft Active Server Pages (ASP) koduna bənzəyir. DML faylları digər HTML səhifələrinə bənzər standart veb brauzerlərdə açıla və baxıla bilər.

## DML fayl formatı

DML faylları düz mətn faylı formatında yaradılmışdır və kodu görmək üçün mətn redaktoru ilə açıla bilər. DML skript dili ilə kod yazmaq server tərəfində yerləşən DML səhifələrində dinamik olaraq HTML yaratmaq üçün istifadə edilə bilər. DynaScripts aşağıdakı dil elementlərindən qurulur:


 * SCRIPT etiketi - Bunlar HTML şərhləri kimi sənədlərə daxil edilir. HTML şərhi \ ilə qeyd olunur.
 * Literals - Bunlar DynaScript fayllarında sabit dəyərlərdir. Bunlara misal olaraq s 123 , 0x3F , 0123 kimi tam ədədlər, 456.789 , 3.2e-8 kimi üzən nöqtəli ədədlər, doğru və ya yalan kimi Boolean və İspaniyada yağış kimi sətir daxildir.
 * Dəyişənlər - DynaScript dəyişənlərinin müəyyən edilməsi və ya onları sabit məlumat tipinə təyin etmək lazım deyil. Siz onu ifadədə istifadə etməzdən əvvəl dəyişənin dəyəri olmalıdır; əks halda iş vaxtı xəbərdarlığı yaradılır.
 * İfadələr - Bunlar dəyişənlərin, hərfi dəyərlərin, operatorların və digər ifadələrin birləşmələridir. Tapşırıq ifadəsinin sağ tərəfi ifadədir.
 * Operatorlar - Bunlar operand adlanan bir və ya bir neçə ifadə üzərində işləyir. Bunlar ya üçlü, ikili və ya birlik ola bilər: üçlü operatorlar üç ifadəyə, ikili operatorlar iki ifadəyə, unar operatorlar isə bir ifadəyə təsir göstərirlər.
 * İfadələr - Bunlar skript axınına nəzarət edir, obyektləri və ümumi proqramlaşdırmanı idarə edir. Ümumiyyətlə, bu ifadələr standart C və Java sintaksisinə uyğundur. Nümunələr if-else, do-while döngələri, keçid, fasilə, davam və s. hər hansı digər skript dili kimidir.
* Funksiyalar - Funksiyalar, hər hansı digər skript dili kimi, bir funksiya kimi sənəddə bir dəfə təlimatlar toplusunu əhatə etməyə, sonra ondan sənəd boyu bir neçə dəfə istifadə etməyə imkan verir (funksiyaya zəng etməklə). DynaScript həmçinin funksiyaları dəstəkləyir.

* Obyektlər - DynaScript obyekt yönümlüdür və "obyektləri" və əsas obyekt yönümlü Enkapsulyasiya, Polimorfizm və Varislik anlayışlarını dəstəkləyir.


