{
  "date": "2021-09-06",
  "keywords": [
"dacpac",
"pratęsimas",
"failą",
"Dokumento formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"Duomenų pakopos taikomųjų programų paketas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie DACPAC failo formatą ir API, kurios gali kurti ir atidaryti DACPAC failus.",
  "title": "DACPAC – duomenų pakopos taikomųjų programų paketas",
  "linktitle": "DACPAC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dacpa-ltc"
}
},
  "lastmod": "2021-09-06"
}

## Kas yra DACPAC failas?

Failas su plėtiniu .dacpac (reiškia Data Tier AppliCation Package) yra duomenų bazės failas, sukurtas naudojant Microsoft SQL Server duomenų pakopos taikomąją programą, kuriame yra duomenų bazės modelis duomenų bazės objektams vaizduoti. Kadangi jame yra visas duomenų bazės modelis, jis naudojamas duomenų bazei atkurti iš modelyje turimos informacijos. DACPAC failai paprastai perduodami diegimo grupėms, kad jos būtų įdiegtos kliento patalpose, kad būtų atkurta duomenų bazė. Juos galima atidaryti su
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## DACPAC failo formatas – daugiau informacijos

DACPAC duomenų paketo failai iš tikrųjų yra suspausti ZIP failai, kuriuose yra keli [XML](/web/xml/) failai, kuriuose yra informacijos apie duomenų bazės modelį, pvz., lentelės ir rodiniai, naudojami duomenų bazei atkurti. Norėdami peržiūrėti DACPAC failų turinį, pervardykite failus iš .dacpac į [.zip](/compression/zip/) ir išskleiskite ZIP archyvą naudodami bet kurią išskleidimo priemonę.

Toliau pateikiami keli failai, rasti DACPAC faile.

 * [Content_Types].xml
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

 * modelis.xml

Pažymėtina, kad DACPAC nėra DUOMENŲ ir kitų serverio lygio objektų. Faile gali būti visų tipų objektų, kurie gali būti saugomi SSDT projekte.

## Nuorodos

* [Duomenų pakopos programos – privalumai](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)

* [Duomenų pakopos programos diegimas – „Microsoft“](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)

* [How to create DACPAC File?](https://azureplayer.net/2018/10/how-to-create-dacpac-file/)
