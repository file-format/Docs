{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "rozšíření", "soubor", "formát souboru", "Typ databázového souboru", "Formát databázového souboru", "Aplikační balíček datové vrstvy" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru DACPAC a rozhraních API, která mohou vytvářet a otevírat soubory DACPAC.",
  "title" :"DACPAC - Data Tier Application Package",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Co je soubor DACPAC?

Soubor s příponou .dacpac (zkratka pro Data Tier AppliCation Package) je databázový soubor vytvořený aplikací datové vrstvy Microsoft SQL Server, který obsahuje databázový model pro reprezentaci databázových objektů. Protože obsahuje kompletní model databáze, používá se k obnovení databáze z podrobností dostupných v modelu. Soubory DACPAC jsou obvykle předány týmům pro nasazení k instalaci v prostorách zákazníka za účelem obnovení databáze. Ty lze otevřít pomocí
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019?ranMID=24542&ranEAID=4LioSo*jxMc&ranSiteID=4LioSo.jxMc-XSp30B6cXjwopiTS89-Ye =1&OCID=AID2200057_aff_7593_1243925&tduid=%28ir__gn1tqusqf0kf6whl2qniaboutn2xruqfmyy1hzec00%29%287593%29%281243925%29%284LioSo.jxMc-XSp30B6cXpiTS89wo0jYzw%29%28%29&irclickid=_gn1tqusqf0kf6whl2qniaboutn2xruqfmyy1hzec00).

## Formát souboru DACPAC – Další informace

Soubory datových balíčků DACPAC jsou ve skutečnosti komprimované soubory ZIP, které obsahují několik souborů [XML](/cs/web/xml/) obsahujících informace o databázovém modelu, jako jsou tabulky a pohledy, používané k obnově databáze. Chcete-li zobrazit obsah souborů DACPAC, přejmenujte soubory z .dacpac na [.zip](/cs/compression/zip/) a rozbalte archiv zip pomocí libovolného dekompresního nástroje.

Následuje několik souborů, které se nacházejí v souboru DACPAC.

* [Content_Types].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* Origin.xml

*model.xml

Je třeba poznamenat, že DACPAC neobsahuje DATA a další objekty na úrovni serveru. Soubor může obsahovat všechny typy objektů, které mohou být uloženy v projektu SSDT.

## Reference

* [Aplikace datové úrovně – výhody](https://docs.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications?view=sql-server-ver15)
* [Nasazení aplikace datové vrstvy – Microsoft](https://docs.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Jak vytvořit soubor DACPAC?](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

