{
  "date": "2020-11-11",
  "keywords": [
"BCP",
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
  "description": "BCP faylları yarada və aça bilən BCP fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "BCP - SQL Server Toplu Kopya Fayl Format",
  "linktitle": "BCP",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-bc-azp"
}
},
  "lastmod": "2020-08-12"
}

## BCP faylı nədir?

BCP (Toplu Kopya Format) idxal/ixrac üçün müxtəlif verilənlər bazası məlumat növü dəyərlərini saxlamaq üçün məlumat strukturlarını müəyyən edən Microsoft SQL Serverin texniki məlumat formatıdır. Format hər bir məlumat sütununun şərhini tam müəyyən edir ki, verilənlər faylında göstərilən dəyərlər dəsti oxuna bilsin. [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) yardım proqramı belə fayldan məlumatları oxumaq və onu müəyyən etmək üçün BCP fayl formatından istifadə edir.


## BCP fayl formatı

BCP format faylı sütun sırasını, adını və məlumat növünü təyin edən XML sənədidir. Bu, istifadəçilərə bu sahələri müəyyən edən məlumat faylından böyük həcmdə məlumatları idxal/ixrac etməyə imkan verir. Bu, məlumat fayllarından məlumat dəyərlərinin toplu idxalında faydalıdır. Məlumat faylındakı məlumat sahələrinin sayı və sırası təyinat cədvəlinin sütunlarında olanlardan fərqli ola bilər. Bu, BCP məlumat formatı faylı məlumatların idxalı üçün sütunların sırasını və növünü təyin etməklə kömək etməyə gəldiyi zamandır.

Format faylının strukturu aşağıdakı formatda təqdim olunur.

```
<BCPFORMAT ...>
    <RECORD>
       <FIELD ID = "fieldID" xsi:type = "fieldType" [...] />
    </RECORD>
    <ROW>
       <COLUMN SOURCE = "fieldID" NAME = "columnName" xsi:type = "columnType" [...]  />
    </ROW>
 </BCPFORMAT>
```

### BCP Məlumat Növləri

|Məlumat Növü|Rəsmi|Təmsil|
---|---|---|
|BigInt|-263 (-9,223,372,036,854,775,808) vasitəsilə 263-1 (9,223,372,036,854,775,807)|`BigInt = [-]1*19DIGIT`|
|İkili|1 - 8000 bayt|onaltılıq kodlu Unicode sətir formatı `İkili = 32000OCTET`|
|Bit|0 və ya 1|sadə Unicode sətri Bit = 0 / 1|
|Char|1-dən 8000-ə qədər|Unicode String Format, Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET ilə n = 4 x (2,147,483,647)|
|Tarix|0001-01-01 - 9999-12-31|YYYY-AA-GG sətir formatı|
|TarixTime|1753-01-01 00:00:00.000 - 9999-12-31 23:59:59.997| Unicode YYYY-AA-GG ss:dd:ss[.nnn] sətir formatı|
|DateTime2|0001-01-01 00:00:00.0000000 vasitəsilə 9999-12-31 23:59:59.9999999.| Unicode YYYY-AA-GG ss:dd:ss[.nnnnnnnn] sətir formatı|
|DateTimeOffset|0001-01-01 00:00:00.0000000 vasitəsilə 9999-12-31 23:59:59.9999999 arasında Əlaqələndirilmiş Ümumdünya Saat (UTC) vaxt zonasında| Unicode YYYY-AA-GG ss:dd:ss[.nnnnnnnn] [{+|-}ss:dd] sətir formatı|
|Ondalıq|-1038 + 1-dən 1038-ə qədər – 1|Unicode sətir formatı `Ondalıq = [-] 0*38DIGIT [.0*38DIGIT]`|
|Float|-1.79E+308 -2.23E-308; 0; 2.23E-308-dən 1.79E+308-ə qədər|Unicode sətir formatı|
|Şəkil|0 ilə 231 arasında dəyişən bayt ardıcıllığı – 1 (2,147,483,647)|onaltılıq kodlu Unicode sətir formatı|
|Int|-231 (-2,147,483,648) ilə 231 – 1 (2,147,483,647)|Unicode sətir formatı|

## İstinadlar

 * [BCP Format - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

