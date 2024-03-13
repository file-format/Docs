{
  "date": "2021-09-06",
  "keywords": [
"dacpac",
"uzadılması",
"fayl",
"fayl formatı",
"Verilənlər bazası fayl növü",
"Verilənlər bazası fayl formatı",
"Məlumat Səviyyəsi Tətbiq Paketi"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "DACPAC fayl formatı və DACPAC fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "DACPAC - Data Tier Tətbiq Paketi",
  "linktitle": "DACPAC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dacpa-azc"
}
},
  "lastmod": "2021-09-06"
}

## DACPAC faylı nədir?

.dacpac (Məlumat Səviyyəsi Tətbiq Paketi deməkdir) uzantısı olan fayl verilənlər bazası obyektlərinin təqdimatı üçün verilənlər bazası modelini ehtiva edən Microsoft SQL Server məlumat səviyyəsi proqramı ilə yaradılmış verilənlər bazası faylıdır. Verilənlər bazasının tam modelini ehtiva etdiyinə görə, modeldə mövcud olan detallardan verilənlər bazasını bərpa etmək üçün istifadə olunur. DACPAC faylları verilənlər bazasını bərpa etmək üçün adətən müştərinin binasında quraşdırmaq üçün yerləşdirmə qruplarına təhvil verilir. Bunlarla açıla bilər
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## DACPAC Fayl Format - Ətraflı Məlumat

DACPAC məlumat paketi faylları əslində verilənlər bazasını bərpa etmək üçün istifadə edilən cədvəllər və görünüşlər kimi verilənlər bazası modeli haqqında məlumatları ehtiva edən bir neçə [XML](/web/xml/) faylı ehtiva edən sıxılmış ZIP fayllarıdır. DACPAC fayllarının məzmununa baxmaq üçün faylların adını .dacpac-dan [.zip](/compression/zip/) olaraq dəyişdirin və hər hansı dekompressiya yardım proqramından istifadə edərək zip arxivini çıxarın.

Aşağıda DACPAC faylının içərisində olan bir neçə fayl var.

 * [Məzmun_Növləri].xml
```
<?xml version=1.0 encoding=utf-8?>
<Types
xmlns=http://schemas.openxmlformats.org/package/2006/content-types>
<Default Extension=xml ContentType=text/xml />
</Types>
```
 * DacMetadata.xml

```
<?xml version=1.0 encoding=utf-8?>
<DacType xmlns=http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02>
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
 * Origin.xml

 * model.xml

Qeyd etmək lazımdır ki, DACPAC-da DATA və digər server səviyyəli obyektlər yoxdur. Fayl SSDT layihəsində saxlanıla bilən bütün obyekt növlərini ehtiva edə bilər.

## İstinadlar

* [Məlumat Tier Proqramları - Faydalar](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)

* [Məlumat Tier Proqramının Yerləşdirilməsi - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)

* [How to create DACPAC File?](https://azureplayer.net/2018/10/how-to-create-dacpac-file/)
