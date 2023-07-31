{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "extensie", "fișier", "format fișier", "Tipul fișierului bazei de date", "Format fișierului bazei de date", "Pachet aplicație nivel de date"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier DACPAC și despre API-urile care pot crea și deschide fișiere DACPAC.",
  "title" :"DACPAC - Pachetul de aplicație de nivel de date",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Ce este un fișier DACPAC?

Un fișier cu extensia .dacpac (stand pentru Data Tier AppliCation Package) este un fișier de bază de date, creat cu aplicația de nivel de date Microsoft SQL Server, care conține modelul bazei de date pentru reprezentarea obiectelor bazei de date. Deoarece conține modelul complet al bazei de date, este folosit pentru a restaura o bază de date din detaliile disponibile în model. Fișierele DACPAC sunt de obicei predate echipelor de implementare pentru instalare la sediul clientului pentru a restaura baza de date. Acestea pot fi deschise cu
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019?ranMID=24542&ranEAID=4LioSo*jxMc&ranSiteID=4LioSo.jxMc-XSp30B6B60cXpiTS30B60cXpiTS30B60cXpiTS30B60cXpiTS30B60cXpiTS30B60cXpiTS30B60cXpiTS30B6 =1&OCID=AID2200057_aff_7593_1243925&tduid=%28ir__gn1tqusqf0kf6whl2qniaboutn2xruqfmyy1hzec00%29%287593%29%281243925%29%284LioSo.jxMc-XSp30B6cXpiTS89wo0jYzw%29%28%29&irclickid=_gn1tqusqf0kf6whl2qniaboutn2xruqfmyy1hzec00).

## Format de fișier DACPAC - Mai multe informații

Fișierele pachetului de date DACPAC sunt de fapt fișiere ZIP comprimate care conțin mai multe fișiere [XML](/ro/web/xml/) care conțin informații despre modelul bazei de date, cum ar fi tabele și vizualizări, utilizate pentru a restaura o bază de date. Pentru a vizualiza conținutul fișierelor DACPAC, redenumiți fișierele din .dacpac în [.zip](/ro/compression/zip/) și extrageți arhiva zip folosind orice utilitar de decompresie.

Următoarele sunt câteva fișiere care se găsesc în interiorul unui fișier DACPAC.

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
* Origine.xml

* model.xml

Este de remarcat faptul că DACPAC nu conține DATE și alte obiecte la nivel de server. Fișierul poate conține toate tipurile de obiecte care ar putea fi păstrate în proiectul SSDT.

## Referințe

* [Aplicații de nivel de date - Beneficii](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications?view=sql-server-ver15)
* [Implementarea unei aplicații de nivel de date - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Cum se creează fișierul DACPAC?](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

