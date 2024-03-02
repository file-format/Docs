{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Foghlaim faoi fhormáid comhaid DSN agus APIanna ar féidir leo comhaid DSN a chruthú agus a oscailt.",
  "title" : "Formáid Chomhaid DSN - Comhad Ainm Foinse Bunachar Sonraí",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-ga",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Cad is comhad DSN ann?

Seasann DSN do Ainm Foinse Sonraí agus is formáid comhaid é a úsáidtear chun faisnéis nasc bunachar sonraí a stóráil. Úsáidtear comhaid DSN de ghnáth i gcomhar le ODBC (Open Database Connectivity) agus ceadaíonn siad rochtain éasca ar bhunachar sonraí ar leith tríd an bhfaisnéis riachtanach a sholáthar chun ceangal leis, mar ainm an fhreastalaí, ainm úsáideora agus pasfhocal. De ghnáth bíonn an comhad i ngnáth-théacs agus is féidir é a chruthú agus a chur in eagar trí úsáid a bhaint as eagarthóir téacs. Is féidir é a úsáid ar chórais oibriúcháin éagsúla cosúil le Windows, Linux agus Mac.

## Conas comhad DSN a chruthú?

Féadfaidh an modh chun comhad DSN a chruthú a bheith éagsúil bunaithe ar an gcóras oibriúcháin agus na huirlisí atá ar fáil. Tugann na céimeanna seo a leanas forbhreathnú ginearálta ar an bpróiseas chun comhad DSN a chruthú ar chóras Windows.

1. Oscail an Riarthóir Foinse Sonraí ODBC trí Foinsí Sonraí ODBC a chuardach sa roghchlár tosaigh.
2. Roghnaigh an táb Córas DSN agus cliceáil ar an gcnaipe Cuir.
3. Roghnaigh an tiománaí cuí don bhunachar sonraí is mian leat ceangal leis agus cliceáil Críochnaigh.
4. Líon isteach an fhaisnéis is gá chun ceangal leis an mbunachar sonraí, mar shampla ainm an fhreastalaí, ainm úsáideora agus pasfhocal.
5. Cliceáil OK chun an comhad DSN a shábháil.

Mar mhalairt air sin, is féidir leat comhad DSN a chruthú de láimh trí chomhad gnáth-théacs a chruthú leis an síneadh .dsn agus an fhaisnéis nasctha riachtanach a chur isteach san fhormáid:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Is féidir leat conair an chomhaid seo a úsáid ansin mar an DSN i do chód/script chun nascadh leis an mbunachar sonraí.

## Cláir a osclaíonn comhaid DSN

Is comhad gnáth-théacs é comhad DSN a stórálann faisnéis a úsáidtear chun nascadh le bunachar sonraí, mar shampla ainm an fhreastalaí, ainm úsáideora agus pasfhocal. Úsáidtear é de ghnáth i gcomhar le ODBC (Open Database Connectivity) chun rochtain éasca ar bhunachar sonraí ar leith a sholáthar.

Chun a bhfuil i gcomhad DSN a oscailt agus a fheiceáil, is féidir leat úsáid a bhaint as aon eagarthóir téacs ar nós Notepad, Téacs Sublime, Atom, etc. Ligfidh na cláir seo duit an comhad DSN a oscailt agus féachaint ar an bhfaisnéis naisc atá stóráilte ann.

Mar sin féin, chun an comhad DSN a úsáid chun nascadh le bunachar sonraí agus oibríochtaí a dhéanamh ar nós SELECT, INSERT, Update, DELETE etc, clár le tacaíocht ODBC, mar theanga ríomhchlárúcháin mar Python, Java, C# nó uirlis bainistíochta bunachar sonraí cosúil le Microsoft Access , Tá SQL Server Bainistíochta Stiúideo ag teastáil. Is féidir leis na cláir seo an fhaisnéis sa chomhad DSN a úsáid chun nascadh leis an mbunachar sonraí agus an oibríocht atá ag teastáil a dhéanamh.

## Tagairtí

* [Cad is DSN (Ainm Foinse Sonraí) ann?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



