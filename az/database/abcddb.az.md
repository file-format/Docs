{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "ABCDDB fayl formatı və ABCDDB fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title" : "ABCDDB Fayl Format - Apple Ünvan Kitabı Əlaqə Siyahısı Verilənlər Bazası Faylı",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-az",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## ABCDDB faylı nədir?

**.ABCDDB** uzantılı fayl Apple Ünvan Kitabı Əlaqə Siyahısı Verilənlər Bazasını ifadə edir. O, adətən **Əlaqə** kimi tanınan **Ünvan Kitabı** tətbiqinə aiddir. Bu daxili proqramdır və iOS və macOS əməliyyat sistemlərinə daxildir. Kontaktlar proqramı istifadəçilərə şəxslər, müəssisələr və təşkilatlar daxil olmaqla, kontaktları ilə bağlı məlumatları saxlamaq və təşkil etmək imkanı verir. Bu proqram istifadəçilərə adlar, ünvanlar, telefon nömrələri və e-poçt ünvanları kimi təfərrüatları izləməyə, həmçinin kontaktlarını qruplara ayırmağa imkan verir.

## SQLite və Tipik Yol ilə əlaqə

Apple-ın Ünvan Kitabı (həmçinin Kontaktlar kimi tanınır) kontakt məlumatlarını metadata qovluğunda vCard kimi saxlayır. **_ABCDDB_ faylı əslində _SQLite 3 məlumat faylıdır_**.

SQLite, yüngül və müstəqil olmaq üçün hazırlanmış məşhur verilənlər bazası idarəetmə sistemidir. Bir çox müxtəlif növ proqram və cihazlarda istifadə olunur. SQLite RDBMS növüdür, yəni açarlar vasitəsilə məlumatları bir-biri ilə əlaqəli cədvəllərdə saxlayır. Tam ədədlər, üzən nöqtəli ədədlər, sətirlər və ikili məlumatlar daxil olmaqla bir sıra məlumat növlərini idarə edə bilər. Bundan əlavə, SQLite istifadəçilərə vahid iş vahidi kimi çoxsaylı verilənlər bazası əməliyyatlarını birlikdə yerinə yetirməyə imkan verən əməliyyatları dəstəkləyir.

ABCDDB uzantılı fayl adətən burada saxlanılır

`~/Kitabxana/Tətbiq Dəstəyi/Ünvan Kitabı/AddressBook-v22.abcddb`

## Zərərli Kontaktlar verilənlər bazasının düzəldilməsi

Lütfən, bunu etməyə cəhd etməzdən əvvəl ehtiyat nüsxəsini götürün. Sonra lütfən gedin

`~/Kitabxana/Tətbiq Dəstəyi/Ünvan Kitabı`

Həmin qovluqda siz .abcddb uzantılı biri də daxil olmaqla üç fayl tapacaqsınız

- `ünvan kitabçası-v22.abcddb`
- `ünvan kitabçası-v22.abcddb-wal`
- `ünvan kitabçası-v22.abcddb-shm`

Bütün bu faylları silin və Kontaktları yenidən açın, o, yenidən işə başlayacaq.

## Yedəkləmədən Ünvan Kitabı verilənlər bazasını bərpa edin

Tutaq ki, Ünvan Kitabı verilənlər bazası kontaktlarınız `addressbook-v22.abcddb`-də saxlanılır.

- Əvvəlcə Ünvan Kitabı məlumatlarınızın ehtiyat nüsxəsini çıxarın və bütün proqramlardan çıxın.
- Verilənlər bazası faylınızı `~/Kitabxana/Tətbiq Dəstəyi/Ünvan Kitabı` alt kataloquna köçürün
- **Ünvan Kitabı.app**-ı işə salın.

## ABCDDB fayl məlumatlarını Microsoft Access-ə ixrac edin

Fayl SQLite 3 məlumat faylı olduğundan, abcddb faylının içindəki məlumatları ODBC konnektorundan istifadə edərək Microsoft Access-ə ixrac edə bilərsiniz.

SQLite ODBC konnektoru ODBC interfeysini dəstəkləyən proqramlara SQLite verilənlər bazasına qoşulmağa imkan verən proqram kitabxanası və sürücüdür. Buraya ODBC interfeysini təyin edən kitabxana və bu interfeysi SQLite API-yə zənglərə çevirən sürücü daxildir. SQLite ODBC konnektorundan istifadə etmək üçün əvvəlcə onu quraşdırmalı və sonra kompüterinizdə ODBC məlumat mənbəyi qurmalısınız. Bu addımları tamamladıqdan sonra ODBC dəstəyi ilə təchiz edilmiş istənilən proqram məlumat mənbəyinə qoşula və SQLite verilənlər bazasından məlumatları əldə edə biləcək.

## İstinadlar
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Mac üçün Əlaqə verilənlər bazası](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Windows 7 Excel-də abcddb faylını necə aça və ya ixrac edə bilərəm?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -windows-7-excel)

