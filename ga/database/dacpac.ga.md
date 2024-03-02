{
  "date": "2021-09-06",
  "keywords": [
"dacpac",
"síneadh",
"comhad",
"formáid comhaid",
"Cineál Comhaid Bunachar Sonraí",
"Formáid Comhaid Bunachar Sonraí",
"Pacáiste Feidhmchláir Sraith Sonraí"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid DACPAC agus APIanna ar féidir leo comhaid DACPAC a chruthú agus a oscailt.",
  "title": "DACPAC - Pacáiste Feidhmchláir Sraith Sonraí",
  "linktitle": "DACPAC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dacpa-gac"
}
},
  "lastmod": "2021-09-06"
}

## Cad is comhad DACPAC ann?

Is comhad bunachar sonraí é comhad le .dacpac (seasann do Phacáiste Feidhmchláir Sraithe Sonraí), a cruthaíodh le feidhmchlár sraith sonraí Microsoft SQL Server, ina bhfuil samhail an bhunachair shonraí chun oibiachtaí bunachar sonraí a léiriú. Toisc go bhfuil múnla iomlán an bhunachair sonraí ann, úsáidtear é chun bunachar sonraí a athbhunú ó na sonraí atá ar fáil sa mhúnla. De ghnáth tugtar comhaid DACPAC ar láimh d’fhoirne imlonnaithe lena suiteáil ag áitreabh an chustaiméara chun bunachar sonraí a athchóiriú. Is féidir iad seo a oscailt le
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## Formáid Chomhaid DACPAC - Tuilleadh Eolais

Is comhaid zip comhbhrúite iarbhír iad comhaid phacáiste sonraí DACPAC ina bhfuil roinnt comhad [XML](/web/xml/) ina bhfuil faisnéis faoi mhúnla an bhunachair shonraí, mar shampla táblaí agus radhairc, a úsáidtear chun bunachar sonraí a athchóiriú. Chun a bhfuil i gcomhad DACPAC a fheiceáil, athainmnigh na comhaid ó .dacpac go [.zip](/compression/zip/) agus bain an chartlann zip as aon áirgiúlacht dí-chomhbhrúite.

Seo a leanas roinnt comhad a fhaightear laistigh de chomhad DACPAC.

 * [Ábhar_Cineálacha].xml
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
 * Bunús.xml

 * múnla.xml

Ní mór a thabhairt faoi deara nach bhfuil SONRAÍ agus réada eile ar leibhéal an fhreastalaí ag DACPAC. Is féidir gach cineál oibiachta a d'fhéadfaí a choinneáil sa tionscadal SSDT a bheith sa chomhad.

## Tagairtí

* [Feidhmchláir Shraith Sonraí - Buntáistí]( https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)

* [Feidhmchlár Sraith Sonraí á Imscaradh - Microsoft]( https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)

* [How to create DACPAC File?](https://azureplayer.net/2018/10/how-to-create-dacpac-file/)
