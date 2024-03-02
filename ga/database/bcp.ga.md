{
  "date": "2020-11-11",
  "keywords": [
"BCP",
"síneadh",
"comhad",
"formáid comhaid",
"Cineál Comhaid Bunachar Sonraí",
"Formáid Comhaid Bunachar Sonraí",
"Comhaid Bunachar Sonraí"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid BCP agus APIanna ar féidir leo comhaid BCP a chruthú agus a oscailt.",
  "title": "BCP - Formáid Cóipeála Bulc Freastalaí SQL",
  "linktitle": "BCP",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-bc-gap"
}
},
  "lastmod": "2020-08-12"
}

## Cad is comhad BCP ann?

Is éard atá i BCP (Formáid Cóipe Bulc) formáid sonraí teicniúla Microsoft SQL Server a shainíonn struchtúir sonraí chun luachanna cineálacha sonraí bunachar sonraí éagsúla a stóráil le haghaidh iompórtáil/onnmhairithe. Sainmhíníonn an fhormáid léirmhíniú gach colúin sonraí go hiomlán ionas gur féidir an tacar luachanna atá sonraithe sa chomhad sonraí a léamh. Úsáideann an áirgiúlacht [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) formáid comhaid BCP chun sonraí ó chomhad den sórt sin a léamh agus chun iad a aithint.


## Formáid Chomhaid BCP

Is doiciméad XML é an comhad formáide BCP a shainíonn ord an cholúin, an t-ainm agus an cineál sonraí. Ligeann sé d'úsáideoirí méid mór sonraí a allmhairiú/onnmhairiú ó chomhad sonraí a shonraíonn na réimsí seo. Tá sé seo ina chuidiú maidir le bulc-allmhairiú luachanna sonraí ó chomhaid sonraí. Féadfaidh líon agus ord na réimsí sonraí sa chomhad sonraí a bheith difriúil ná iad siúd sna colúin tábla sprice. Seo é nuair a thagann an comhad formáid sonraí BCP chun cabhrú leis trí ord agus cineál na gcolún a shonrú chun na sonraí a allmhairiú.

Léirítear struchtúr an chomhaid fhormáide san fhormáid seo a leanas.

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

### Cineálacha Sonraí BCP

|Cineál Sonraí|Raon|Ionadaíocht|
---|---|---|
|BigInt|-263 (-9,223,372,036,854,775,808) trí 263-1 (9,223,372,036,854,775,807)|`BigInt = [-]1*19DIGIT`|
|Dénártha|1 go 8000 beart|Formáid teaghrán Unicode atá ionchódaithe go heicsidheachúil `Dénártha = 32000OCTET` |
|Giotán|0 nó 1|teaghrán simplí Unicode Giotán = 0 / 1 |
|Char|1 go 8000|Formáid Teaghrán Unicode, Car = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET le n = 4 x (2,147,483,647)|
|Dáta|0001-01-01 trí 9999-12-31|Formáid teaghrán BBBB-MM-DD|
|DátaAm|1753-01-01 00:00:00.000 trí 9999-12-31 23:59:59.997| Unicode BBBB-MM-LL hh:mm:ss[.nnn] formáid teaghrán |
|DátaAm2|0001-01-01 00:00:00.0000000 trí 9999-12-31 23:59:59.9999999.| Unicode BBBB-MM-DD hh:mm:ss[.nnnnnn] formáid téad |
|DateTimeOffset|0001-01-01 00:00:00.0000000 trí 9999-12-31 23:59:59.9999999 sa chrios ama Ama Comhordaithe (UTC) | Unicode BBBB-MM-DD hh:mm:ss[.nnnnnn] [{+|-}hh:mm] formáid téad|
|Deachúil|-1038 + 1 go 1038 – 1|Formáid teaghrán Unicode `Decimal = [-] 0*38DIGIT [.0*38DIGIT]`|
|Snámh|-1.79E+308 go -2.23E-308; 0; ó 2.23E-308 go 1.79E+308|Formáid teaghrán Unicode |
|Íomhá|seicheamh beart a théann ó 0 go 231 – 1 (2,147,483,647)|Formáid teaghrán Unicode atá ionchódaithe go heicsidheachúil|
|Int|-231 (-2,147,483,648) trí 231 – 1 (2,147,483,647)|Formáid teaghrán Unicode |

## Tagairtí

 * [Formáid BCP - Microsoft]( https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

