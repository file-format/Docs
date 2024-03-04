{
  "date": "2020-11-11",
  "keywords": [
"BCP",
"pratęsimas",
"failą",
"Dokumento formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"Duomenų bazės failai"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie BCP failo formatą ir API, kurios gali kurti ir atidaryti BCP failus.",
  "title": "BCP – SQL serverio masinio kopijavimo failo formatas",
  "linktitle": "BCP",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-bc-ltp"
}
},
  "lastmod": "2020-08-12"
}

## Kas yra BCP failas?

BCP (masinio kopijavimo formatas) yra Microsoft SQL Server techninių duomenų formatas, apibrėžiantis duomenų struktūras, skirtas saugoti skirtingas duomenų bazės duomenų tipų vertes, skirtas importuoti / eksportuoti. Formatas visiškai apibrėžia kiekvieno duomenų stulpelio interpretaciją, kad būtų galima nuskaityti duomenų faile nurodytą reikšmių rinkinį. Paslauga [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) naudoja BCP failo formatą, kad nuskaitytų duomenis iš tokio failo ir jį identifikuotų.


## BCP failo formatas

BCP formato failas yra XML dokumentas, apibrėžiantis stulpelių tvarką, pavadinimą ir duomenų tipą. Tai leidžia vartotojams importuoti / eksportuoti didelį duomenų kiekį iš duomenų failo, nurodančio šiuos laukus. Tai naudinga masiškai importuojant duomenų vertes iš duomenų failų. Duomenų laukų skaičius ir tvarka duomenų faile gali skirtis nuo paskirties lentelės stulpeliuose esančių duomenų laukų. Tai yra tada, kai BCP duomenų formato failas padeda nurodyti duomenų importavimo stulpelių tvarką ir tipą.

Formato failo struktūra pavaizduota tokiu formatu.

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

### BCP duomenų tipai

|Duomenų tipas|diapazonas|Pateikimas|
---|---|---|
|BigInt|-263 (-9 223 372 036 854 775 808) iki 263-1 (9 223 372 036 854 775 807)|BigInt = [-]1*19DIGIT`|
|Dvejetainis|1–8000 baitų|šešioliktainiu kodu užkoduotas Unikodo eilutės formatas `Dvejetainis = 32000OCTET`|
|Bitas|0 arba 1|paprasta Unicode eilutė Bitas = 0 / 1|
|Char|1–8000|Unicode eilutės formatas, Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET, kai n = 4 x (2 147 483 647)|
|Data|0001-01-01 iki 9999-12-31|YYYY-MM-DD eilutės formatas|
|DataLaikas|1753-01-01 00:00:00.000 iki 9999-12-31 23:59:59.997| Unicode YYYY-MM-DD hh:mm:ss[.nnn] eilutės formatas|
|DataLaikas2|0001-01-01 00:00:00.0000000 iki 9999-12-31 23:59:59.9999999.| Unicode YYYY-MM-DD hh:mm:ss[.nnnnnnn] eilutės formatas|
|DateTimeOffset|0001-01-01 00:00:00.0000000 iki 9999-12-31 23:59:59.9999999 pagal koordinuotą visuotinį laiką (UTC) laiko juosta| Unikodas YYYY-MM-DD hh:mm:ss[.nnnnnnn] [{+|-}hh:mm] eilutės formatas|
|Dešimtainė|-1038 + 1–1038 – 1|Unicode eilutės formatas `Dešimtainis = [-] 0*38SKAITMENYS [.0*38SKAITMENYS]`|
|Plūdė|-1,79E+308 iki -2,23E-308; 0; nuo 2.23E-308 iki 1.79E+308|Unicode eilutės formatas|
|Vaizdas|baitų seka, kuri svyruoja nuo 0 iki 231 – 1 (2 147 483 647)|šešioliktainiu kodu užkoduotas Unikodo eilutės formatas|
|Int|-231 (-2 147 483 648) iki 231 – 1 (2 147 483 647)|Unicode eilutės formatas|

## Nuorodos

 * [BCP formatas – Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

