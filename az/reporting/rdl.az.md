{
  "date": "2021-03-01",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RDL - Hesabat Tərifi Dil Faylı",
  "keywords": [
"rdl",
"hesabatın tərif dili",
"XmlTextWriter",
"XSD",
"RDL elementi"
],
  "description": "SQL Server Reporting Services hesabat tərifinin XML təqdimatı olan RDL fayl formatı haqqında məlumat əldə edin.",
  "linktitle": "RDL",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rd-azl"
}
},
  "lastmod": "2021-03-01"
}

## RDL faylı nədir? ##

RDL (Report Definition Language) hesabatların müəyyən edilməsi üçün Microsoft tərəfindən müəyyən edilmiş bir meyardır. RDL faylı bir və ya bir neçə RDL Elementindən ibarətdir. Halbuki RDL elementi onun məlumat növündən və kardinallığından ibarətdir. Bir element sadə və ya mürəkkəb ola bilər. Sadə elementin uşaq elementi və ya atributları yoxdur, mürəkkəb elementin uşaqları və əlavə atributları var.

## RDL XML Sxem Tərifi
XML Sxem Tərifi (XSD) faylı RDL faylını təsdiqləyir. Sxem RDL elementlərinin .rdl faylında baş verə biləcəyi qaydaları müəyyən edir. RDL elementi sadə və ya mürəkkəb ola bilər. Sadə elementin uşaq elementləri və ya atributları yoxdur və mürəkkəb elementin uşaqları və isteğe bağlı olaraq atributları var.

## RDL yaradılması
RDL təbiətdə açıq və genişləndirilə bilən olduğundan, onun XML sxemi əsasında RDL faylları yaradan bir çox proqram və alətlər tikilə bilər. Tətbiqdən RDL yaratmağın ən sadə yollarından biri **System.Xml** ad sahəsinin və System.Linq ad sahəsinin Microsoft .NET Framework siniflərindən istifadə etməkdir. Xüsusilə, **XmlTextWriter** sinfi RDL yazmaq üçün istifadə oluna bilər. Siz **XmlTextWriter**-dən istifadə etməklə istənilən .NET Framework proqramında başdan sona tam hesabat tərifini yarada bilərsiniz. Tərtibatçılar həmçinin RDL-ni genişləndirmək üçün xüsusi xassələri olan fərdi hesabat elementləri əlavə edə bilərlər.

## RDL növləri
Aşağıdakı cədvəldə RDL elementlərində istifadə olunan növlər və atributlar verilmişdir.

|Növ|Təsvir|
---|---|
|İkili |Baza-64 kodlu binar dəyəri olan xassə.|
|Boolean| Obyektin dəyəri olaraq doğru və ya yalan olan xüsusiyyət. Əgər başqa cür göstərilməyibsə, buraxılmış isteğe bağlı Boolean obyektinin dəyəri False-dir.|
|Date	|A property with a fully specified date or datetime value specified in ISO8601 date format: YYYY-MM-DD[THH:MM[:SS[.S]]].|
|Enum |Təyin edilmiş dəyərlər siyahısından biri olmalı olan sətir mətn dəyəri olan xüsusiyyət.|
|Float |Float dəyəri olan əmlak. Nöqtə (.) isteğe bağlı onluq ayırıcı kimi istifadə olunur.|
|Tam |Tam (int32) dəyəri olan xassə.|
|Language |ABŞ İngilis dili üçün en-us kimi dil və mədəniyyət kodunu ehtiva edən mətn dəyəri olan xüsusiyyət. Dəyər ya xüsusi dil, ya da Microsoft .NET Framework-də defolt dilinin müəyyən edildiyi neytral dil olmalıdır.|
|Ad |Sətrin mətn dəyəri olan xassə. Adlar elementin ad məkanında unikal olmalıdır. Müəyyən edilməmişsə, element üçün ad sahəsi adı olan ən daxili ehtiva edən obyektdir.|
|NormalizedString |Normallaşdırılmış sətir mətn dəyəri olan xassə.|
|Ölçü |Ölçü elementində nömrə olmalıdır (isteğe bağlı onluq ayırıcı kimi istifadə olunan nöqtə simvolu ilə). Nömrənin ardınca sm, mm, in, pt və ya pc kimi CSS uzunluq vahidi üçün işarə qoyulmalıdır. Nömrə və təyinat arasında boşluq isteğe bağlıdır. Ölçü təyinediciləri haqqında ətraflı məlumat üçün CSS Dəyərləri və Vahid Referansına baxın. RDL-də Ölçü üçün maksimum dəyər 160 düymdür. Minimum ölçü 0 düymdür.|
|String |Str mətn dəyəri olan xassə.|
|UnsignedInt |İmzasız tam (uint32) dəyəri olan xüsusiyyət.|
|Variant |İstənilən sadə XML tipli əmlak.|

## RDL məlumat növləri
RDL-də DataType Enumeration atribut, ifadə və ya parametrin məlumat növünü müəyyən edir. Aşağıdakı cədvəl CLR məlumat növlərinin RDL məlumat növlərinə necə uyğun olduğunu göstərir.

|CLR Növ(lər)i |Müvafiq Məlumat Tipi|
---|---|
|Boolean| Boolean|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |Integer|
|Tək, Qoşa |Float|
|String, Char, GUID, Timespan |String|


## İstinadlar ##

- [Report Definition Language (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Report Definition Language (SSRS)](https://learn.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

