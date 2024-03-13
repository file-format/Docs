{
  "date": "2022-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HDMP Faylı - Windows yığın boşaltma fayl formatı",
  "description": "HDMP fayl formatı və HDMP faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "HDMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-hdm-azp"
}
},
  "lastmod": "2022-08-19"
}

## HDMP faylı nədir?

HDMP faylı bir proqram və ya proqram xəta səbəbindən çökdüyü zaman sıxılmamış yaddaş zibilidir. O, yalnız Windows XP/Vista tərəfindən yaradılmışdır və proqramın qəzaya uğradığı zaman statusunun zibilini ehtiva edir. Sıxılmamış olduğu üçün HDMP faylları hesabat məqsədi ilə sıxılmış Minidump [MDMP](/system/mdmp/) faylları ilə müqayisədə diskdə daha çox yer tutur.

HDMP fayllarını **açmaq** və ya təhlil etmək üçün istifadə oluna bilən proqramlara Windows üçün sazlama alətləri olan Microsoft Visual Studio daxildir.

## HDMP fayl formatı

HDMP faylları ikili fayllar kimi diskdə saxlanılır və müvafiq proqramlar olmadan açıldıqda heç bir fayda vermir. Bunlar xəta baş verən zaman qeydə alınmış müvafiq sistem məlumatlarını ehtiva edir.

### HDMP və MDMP Fayl Formatları arasındakı fərq

HDMP sıxılmamış yaddaş boşaltma fayllarıdır. Bunun əksinə olaraq, MDMP fayl ölçüsünü azaltmaq üçün sıxılmış və problemi bildirmək üçün Microsoft-a göndərilən mini dump fayllardır.

## İstinad ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


