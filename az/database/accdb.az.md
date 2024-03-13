{
  "date": "2020-11-11",
  "keywords": [
"ACCDB",
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
  "description": "ACCDB fayl formatı və ACCDB fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "ACCDB Fayl Format - Microsoft Access 2007 verilənlər bazası faylı",
  "linktitle": "ACCDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-accd-azb"
}
},
  "lastmod": "2020-11-12"
}

## ACCDB faylı nədir?

.accdb uzantılı fayl, istifadəçilərin məlumatlarını cədvəllərdə saxlayan Microsoft Access 2007 verilənlər bazası faylıdır. Saxlamağı dəstəkləyir
xüsusi formalar, SQL sorğuları və digər məlumatlar. Microsoft XML əsaslı fayl strukturuna keçdikdən sonra ACCDB faylları [MDB](/database/mdb/) faylları əvəz etdi. ACCDB faylları hələ də köhnə uyğunluqla MDB-yə çevrilə bilər. Bununla belə, ACCDB indi geniş istifadə olunan Access verilənlər bazası fayl formatıdır. Microsoft həmçinin ACCDB formatında fayl qoşmalarının, ikili məlumatların saxlanması və çox dəyərli sahə dəstəyi kimi əlavə funksiyaları dəstəkləyir.

## ACCDB fayl formatı

MDB kimi, ACCDB fayl formatı üçün heç bir ictimai spesifikasiya yoxdur. Microsoft bu fayllara Open Database Connectivity (ODBC) standartı və Visual Basic for Applications (VBA) vasitəsilə proqramlı şəkildə daxil olmağı dəstəkləyir.

### Bir Anlayış

A hex dump of a simple ACCDB file suggests that there are general similarities in structure to the latest versions of the predecessor MDB Format Family. Both file formats use fixed page sizes of 4096 bytes. Another similarity between ACCDB and MDB is the form of the magic number, which includes the string "Standard ACE DB" for ACCDB. A version or compatibility code is in the same location in both formats. The mdbtools | HACKING file states "Offset 0x14 contains the Jet version of this database" and The unofficial MDB Guide concurs. The information in these sources, combined with Wikipedia entry for [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), suggests that a value of 0x02 indicates ACE 12 (Access 2007) and 0x03 indicates ACE 14 (Access 2010). However, a minimal database created in Access 2010 and a similar one created in Access 2016 both have 0x02 in this location. A minimal database created in Access 2016, but defining a column with the newly introduced "large integer" data type, had a value of 0x05. ACCDB fayllarında bu göstərici onu yaratmaq üçün istifadə olunan ACE mühərrikinin versiyasından çox faylın uyğunluğunu əks etdirir.

## İstinadlar

* [Access 2016 Spesifikasiyaları](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)

* [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)

* [Hansı Access fayl formatından istifadə etməliyəm?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41)


