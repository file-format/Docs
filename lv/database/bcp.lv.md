{
  "date": "2020-11-11",
  "keywords": [
"BCP",
"pagarinājumu",
"failu",
"faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Datu bāzes faili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par BCP failu formātu un API, kas var izveidot un atvērt BCP failus.",
  "title": "BCP — SQL servera lielapjoma kopēšanas faila formāts",
  "linktitle": "BCP",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-bc-lvp"
}
},
  "lastmod": "2020-08-12"
}

## Kas ir BCP fails?

BCP (Bulk Copy Format) ir Microsoft SQL Server tehnisko datu formāts, kas nosaka datu struktūras, lai saglabātu dažādas datu bāzes datu tipu vērtības importēšanai/eksportēšanai. Formāts pilnībā nosaka katras datu kolonnas interpretāciju, lai varētu nolasīt datu failā norādīto vērtību kopu. Utilīta [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) izmanto BCP faila formātu, lai nolasītu datus no šāda faila un identificētu to.


## BCP faila formāts

BCP formāta fails ir XML dokuments, kas nosaka kolonnu secību, nosaukumu un datu tipu. Tas ļauj lietotājiem importēt/eksportēt lielu datu apjomu no datu faila, norādot šos laukus. Tas ir noderīgi datu vērtību lielapjoma importēšanai no datu failiem. Datu lauku skaits un secība datu failā var atšķirties no tiem, kas atrodas mērķa tabulas kolonnās. Šajā gadījumā BCP datu formāta fails nāk palīgā, norādot datu importēšanas kolonnu secību un veidu.

Formāta faila struktūra ir attēlota šādā formātā.

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

### BCP datu tipi

|Datu tips|Diapazons|Atveidojums|
---|---|---|
|BigInt|-263 (-9,223,372,036,854,775,808) līdz 263-1 (9,223,372,036,854,775,807)|`BigInt = [-]1*19DIGIT`|
|Binārs|1–8000 baiti|heksadecimāli kodēts unikoda virknes formāts `Binārais = 32000OCTET`|
|Bits|0 vai 1|vienkārša Unikoda virkne Bits = 0 / 1|
|Char|1 līdz 8000|Unikoda virknes formāts, Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET ar n = 4 x (2 147 483 647)|
|Datums|0001-01-01 līdz 9999-12-31|GGGG-MM-DD virknes formāts|
|DateLaiks|1753-01-01 00:00:00.000 līdz 9999-12-31 23:59:59.997| Unikoda GGGG-MM-DD hh:mm:ss[.nnn] virknes formāts|
|DateTime2|0001-01-01 00:00:00.0000000 līdz 9999-12-31 23:59:59.9999999.| Unikoda GGGG-MM-DD hh:mm:ss[.nnnnnnn] virknes formāts|
|DateTimeOffset|0001-01-01 00:00:00.0000000 līdz 9999-12-31 23:59:59.9999999 pasaules koordinētā laika (UTC) laika joslā| Unikoda GGGG-MM-DD hh:mm:ss[.nnnnnnn] [{+|-}hh:mm] virknes formāts|
|Decimāldaļa|-1038 + 1 līdz 1038 – 1|Unikoda virknes formāts `Decimāls = [-] 0*38DIGIT [.0*38DIGIT]`|
|Peldiņš|-1,79E+308 līdz -2,23E-308; 0; no 2.23E-308 līdz 1.79E+308|Unikoda virknes formāts|
|Attēls|baitu secība diapazonā no 0 līdz 231 – 1 (2 147 483 647)|heksadecimālkodēts unikoda virknes formāts|
|Int|-231 (-2 147 483 648) līdz 231 - 1 (2 147 483 647)|Unikoda virknes formāts|

## Atsauces

 * [BCP formāts — Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

