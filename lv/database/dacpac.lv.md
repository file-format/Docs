{
  "date": "2021-09-06",
  "keywords": [
"dacpac",
"pagarinājumu",
"failu",
"faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Datu līmeņa lietojumprogrammu pakotne"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par DACPAC faila formātu un API, kas var izveidot un atvērt DACPAC failus.",
  "title": "DACPAC — datu līmeņa lietojumprogrammu pakotne",
  "linktitle": "DACPAC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dacpa-lvc"
}
},
  "lastmod": "2021-09-06"
}

## Kas ir DACPAC fails?

Fails ar paplašinājumu .dacpac (apzīmē Data Tier AppliCation Package) ir datu bāzes fails, kas izveidots ar Microsoft SQL Server datu līmeņa lietojumprogrammu un satur datu bāzes modeli datu bāzes objektu attēlošanai. Tā kā tajā ir pilns datu bāzes modelis, to izmanto, lai atjaunotu datubāzi no modelī pieejamās informācijas. DACPAC faili parasti tiek nodoti izvietošanas komandām instalēšanai klienta telpās datu bāzes atjaunošanai. Tos var atvērt ar
{{HIPERSAITE1}}.

## DACPAC faila formāts — plašāka informācija

DACPAC datu pakotnes faili faktiski ir saspiesti ZIP faili, kas satur vairākus [XML](/web/xml/) failus, kas satur informāciju par datu bāzes modeli, piemēram, tabulas un skatus, ko izmanto datu bāzes atjaunošanai. Lai skatītu DACPAC failu saturu, pārdēvējiet failus no .dacpac uz [.zip](/compression/zip/) un izņemiet zip arhīvu, izmantojot jebkuru dekompresijas utilītu.

Tālāk ir norādīti daži faili, kas ir atrodami DACPAC failā.

 * [Satura_veidi].xml
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

Jāatzīmē, ka DACPAC nesatur DATU un citus servera līmeņa objektus. Fails var saturēt visus objektu tipus, kas var tikt saglabāti SSDT projektā.

## Atsauces

* [Datu līmeņa lietojumprogrammas — priekšrocības](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)

* [Datu līmeņa lietojumprogrammas izvietošana — Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)

* [How to create DACPAC File?](https://azureplayer.net/2018/10/how-to-create-dacpac-file/)
