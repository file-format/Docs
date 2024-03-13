{
  "date": "2020-11-11",
  "keywords": [
"ACCDT",
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
  "description": "ACCDT fayl formatı və ACCDT fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "ACCDT - Microsoft Access 2007 Şablon verilənlər bazası fayl formatı",
  "linktitle": "ACCDT",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-accd-azt"
}
},
  "lastmod": "2020-11-12"
}

## ACCDT faylı nədir?

A file with .accdt extension is a Microsoft Access database template file that contains pre-defined database elements. These elements are a collection of structures that define a database applications such as database schemas for storing data, layout description for views of the data, and metadata describing the database. Being template files, ACCDT files can be used to create databases based on the template settings available in these. Resultant database files are saved as [ACCDB](/database/accdb/) files and populated with data in tables. Microsoft Access 2007 and onwards can open ACCDT files.

## ACCDT Fayl Formatı

ACCDT şablon faylları Office Open XML spesifikasiyalarına əsaslanır və bütün məlumatlar ZIP paketindədir. Verilənlər bazasının strukturu və məzmunu haqqında məlumat [XML](/web/xml/) fayllarında və mətn fayllarında yerləşir və əlaqələr vasitəsilə bir-biri ilə əlaqələndirilir. Siz ACCDT faylının adını [.zip](/compression/zip/) uzantısına dəyişə və ZIP arxivinin məzmununu çıxarmaq üçün istənilən sıxılma proqramından istifadə edə bilərsiniz.

### Fayl strukturu

ACCDT faylları əlaqəli hissələrin toplusunu ehtiva edən paketlərdir. Hər bir **hissə** XML, mətn və ikili formatlardan istifadə edərək verilənlər bazası tətbiqinin məzmunu haqqında məlumatları saxlayır, bunlara aşağıdakılar daxildir:

 * Verilənlər bazası obyektləri
 * Əlaqədar metadata
 * Paketin strukturu

#### Paket

Paket bir neçə hissədən ibarət olan və [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html)-də göstərilən Açıq Qablaşdırma Konvensiyalarına uyğun gələn [ZIP](/compression/zip/) arxividir. ACCDT fayllarında əlaqənin hədəfi olan ən azı bir Şablon metadaa hissəsi olmalıdır. Bu Şablon Metadata ACCDT faylının başlanğıc hissəsidir.

#### Hissə

Hissə, onda saxlanılan məzmunun xarakterini və növünü təyin etmək üçün əlaqəli tipə malik olan bayt axınıdır. Hissələrin sadalanması etibarlı hissələri, etibarlı məzmun növlərini və paketdəki bütün hissələr arasında tələb olunan əlaqələri müəyyən edir.

#### Münasibət

`Paket Əlaqəsi` - burada hədəf bir hissədir və mənbə bütövlükdə paketdir.

`Part-to-part Relationship` - burada hədəf bir hissədir və mənbə paketin bir hissəsidir.

`Açıq Əlaqə` - burada mənbə hissəsinin məzmunundan əlaqə elementinə onun ID atributunun dəyərinə istinad etməklə mənbə istinad edilir.

`Düzgün Münasibət` - açıq-aşkar olmayan əlaqə.

`Daxili əlaqə` - burada hədəf paketin bir hissəsidir.

`Xarici əlaqə` - burada hədəf paketdə olmayan xarici resursdur.

## İstinadlar ##

* [Access Template File Format](https://learn.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

