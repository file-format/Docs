{
  "date": "2020-11-11",
  "keywords": [
"LDF",
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
  "description": "Foghlaim faoi fhormáid comhaid LDF agus APIanna ar féidir leo comhaid LDF a chruthú agus a oscailt.",
  "title": "LDF - Formáid Comhaid Bunachar Sonraí Máistir Freastalaí SQL",
  "linktitle": "LDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ld-gaf"
}
},
  "lastmod": "2020-08-12"
}

## Cad is comhad LDF ann?

Is logchomhad é comhad le síneadh .ldf arna chothabháil ag Microsoft SQL Server ar córas bainistíochta bunachar sonraí coibhneasta (RDBMS) é. Déantar na hidirbhearta go léir a dhéantar ar bhunchomhaid bhunachar sonraí ([MDF](/database/mdf/))(amhail ionsá, nuashonrú, scriosadh) a thaifeadadh sa chomhad LDF. Is comhpháirteanna ríthábhachtacha iad comhaid LDF d’aon bhunachar sonraí. I gcás teip córais, úsáidtear an logchomhad chun an bunachar sonraí a chur ar ais go dtí staid chomhsheasmhach. Féadfaidh logchomhad na n-idirbheart a mhéadú i méid mura bhfuil na hidirbhearta tiomanta go hiomlán. Is féidir comhaid LDF a oscailt le feidhmchlár bogearraí Microsoft SQL Server.

## Oibríochtaí Taifeadta i gComhad LDF

Taifeadann logchomhad SQL na hoibríochtaí seo a leanas:

 * Tús agus deireadh gach idirbhirt.

 * Gach modhnú sonraí sonraí (cuir isteach, nuashonraigh, nó scrios). Áirítear leis seo freisin athruithe ar nósanna imeachta stóráilte córais nó ar ráitis teanga sainmhínithe sonraí (DDL) ar aon tábla, lena n-áirítear táblaí córais.

 * Gach fairsinge agus leithdháileadh leathanach nó deallocation.

 * Tábla nó innéacs a chruthú nó a scaoileadh.

## Formáid Comhaid LDF

The LDF file consists of SQL Server transaction records that are arranged as string of log records. Each log record has a log sequence number (LSN) that is higher than the LSN of the previous record. The strings are concatenated after each other in the file. Due to the modern high speed computers, records can be inserted where the LSN2 exists in the log file before LSN1. Ós rud é go ndéantar na hoibríochtaí a thaifeadadh i sraithuimhir, rinneadh an t-athrú a thuairiscítear ag LSN2 tar éis taifead loga LSN1. Nasctar siar na taifid d’idirbheart ar leith trí úsáid a bhaint as leideanna a úsáidtear agus a luasaíonn aischur an idirbhirt.
 
## Tagairtí

 * [Comhaid Bunachar Sonraí agus Grúpaí Comhad](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
 * [Treoir Ailtireachta agus Bainistíochta Loga Idirbheart](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server -ver15)

