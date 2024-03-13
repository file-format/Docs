{
  "date": "2020-11-11",
  "keywords": [
"NSF",
"uzadılması",
"fayl",
"fayl formatı",
"Verilənlər bazası fayl növü",
"Verilənlər bazası fayl formatı",
"Verilənlər Bazasının Faylları"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "NSF fayl formatı və NSF fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "NSF Fayl Format - Lotus Notes Database Format",
  "linktitle": "NSF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ns-azf"
}
},
  "lastmod": "2020-08-12"
}

## NSF faylı nədir?

.nsf (Qeydlər Saxlama Mexanizmi) genişləndirilməsi olan fayl, əvvəllər Lotus Notes kimi tanınan [IBM Notes software](https://en.wikipedia.org/wiki/HCL_Domino) tərəfindən istifadə edilən verilənlər bazası fayl formatıdır. E-poçtlar, görüşlər, sənədlər, formalar və görünüşlər kimi müxtəlif növ obyektləri saxlamaq üçün sxemi müəyyənləşdirir. Bütün bu məlumatlar PST/OST faylına bənzər işgüzar əməkdaşlıq üçün vahid NSF faylında var. NSF fayllarını aça bilən proqramlardan bəzilərinə IBM Lotus Notes və IBM Domino daxildir.

## NSF Fayl Formatının Xüsusiyyətləri

NSF faylları ikili xarakter daşıyır və onların spesifikasiyası [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc saytında Joachim Metz tərəfindən mövcuddur. Bu detallara əsasən, NSF faylı aşağıdakılardan ibarətdir:

 * Fayl başlığı
 * Verilənlər Bazasının Başlığı

Bundan əlavə, o, ibarətdir:

 * Superblok
 * Bucket deskriptor bloku
 * Bitmap
 * Köçürmə vektorunu qeyd edin
 * Xülasə kovaları
 * Xülasə olmayan vedrələr


### NSF Fayl Başlığı

NSF fayl başlığı 6 bayt ölçüsündədir. O, ibarətdir:

|Offset|Ölçü|Dəyər|Təsvir|
---|---|---|---|
0|2|0x1a 0x00|İmza|
2|4| |Verilənlər bazası başlığının ölçüsü|

### Verilənlər bazası başlığı

NSD Database başlığı aşağıdakı təsdiqlənmiş dəyərləri ehtiva edir.

 * Verilənlər bazası məlumatı
   * Verilənlər bazası identifikatoru (DBID)
 * Replikasiya məlumatları
 * Verilənlər bazası məlumat bufer bayraqları
   * Başlıq
   * Kateqoriyalar
   * Sinif
   * Dizayn sinfi (şablon adı)
 * Xüsusi qeyd identifikatorları
 * Doldurma
 * Verilənlər bazası məlumatı 2
 * Verilənlər bazası məlumatı 3
 * Verilənlər bazası məlumatı 4
 * Verilənlər bazası məlumatı 5
 * Doldurma
 * Verilənlər bazası nümunəsi identifikatoru (DBIID)
 * Replikasiya tarixi

## İstinadlar

 * [NSF Format - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)
