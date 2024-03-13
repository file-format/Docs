{
  "date": "2020-11-11",
  "keywords": [
"MDB",
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
  "description": "MDB fayl formatı və MDB fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "MDB Fayl Format - Microsoft Access verilənlər bazası faylı",
  "linktitle": "MDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-md-azb"
}
},
  "lastmod": "2020-11-11"
}

## MDB faylı nədir?

A file with .mdb extension is a Microsoft Access database file which is a Relational Database Management System (RDBMS). It stores data in database tables that are linked to each other via primary and foreign keys. The MDB file contains complete structure of the database tables, queries, stored procedures. MDB is the default file format for Microsoft Access 2003. Microsoft Access-in yan versiyaları bu günə qədər ən son fayl formatı olan [ACCDB](/database/accdb/) fayl formatlarından istifadə edir. MDB faylları Microsoft Access, MDB Viewer, MDBOpener kimi proqramlarla açıla və ACCDB, [CSV](/spreadsheet/csv/), Excel formatlarına və s.-ə çevrilə bilər.

## MDB fayl formatı

There are public specifications available for MDB format and it remains Microsoft's proprietary file format. Microsoft, however, provides connectivity access to the MDB file using Open Database Connectivity (ODBC) standard and Visual Basic for Applications (VBA). The unofficial MDB guide provides brief informal description of the MDB format based on the reverse engineering and can be consulted for knowing about the specifications.

### Səhifələr

Qeyri-rəsmi MDB təlimatına əsasən, MDB faylı sabit ölçülü səhifələrdən ibarətdir (Jeb DB3 üçün 2048 bayt və Jet DB 4 üçün 4096 bayt). Birinci bayt səhifənin növünü göstərir. Əsas səhifə növləri aşağıdakılardır:

`Birinci Səhifə:` O, həmçinin faylın uyğun olduğu Jet DB versiyasının identifikasiyasını ehtiva edən verilənlər bazası başlığı məlumatını ehtiva edir. Bundan əlavə, o, həmçinin fayl təhlükəsizlik məlumat və səhifə istifadə xəritəsi daxildir.

`Cədvəl tərifi səhifəsi:` Cədvəlin tərifi səhifəsi sütunları, məlumat növlərini, indeksi və digər məlumatları təyin edir. Lazım gələrsə, əlavə səhifələrdən istifadə edir və bu cədvəl üçün sıra məlumatlarını ehtiva edən səhifələrin xəritəsini ehtiva edir.

`Məlumat səhifələri:` Məlumat səhifələri verilənlərin sətirlər üzrə saxlandığı faktiki məlumat konteynerləridir. Uzun məlumat dəyərlərini saxlamaq üçün köməkçi səhifələrdən istifadə edir.

Tək Microsoft Access verilənlər bazası fayl və cədvəl ölçüsü məhdudiyyətlərini aşmağa imkan verən bir neçə fayldan ibarət ola bilər. Bu, formaları və kodu istifadəçinin iş masasındakı MDB faylına, verilənləri isə şəbəkəyə qoşulmuş serverlərdəki digər MDB fayllarına yerləşdirməyi asanlaşdırır.

## İstinadlar ##

* [Giriş Xüsusiyyətləri](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)


