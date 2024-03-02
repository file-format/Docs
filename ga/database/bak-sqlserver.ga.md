{
  "date": "2023-06-12",
  "keywords": [
"baic",
"comhad bak",
"Cúltaca Bunachar Sonraí Microsoft SQL Server",
"cad is comhad bak ann",
"conas comhad bak a oscailt",
"comhad",
"síneadh comhad bak",
"síneadh"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid BAK - Cúltaca Bunachar Sonraí Freastalaí Microsoft SQL",
  "description": "Foghlaim faoi fhormáid Chúltaca Freastalaí SQL BAK agus APIs ar féidir leo comhaid BAK a chruthú agus a oscailt.",
  "linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver-ga",
      "parent": "database"
}
},
  "lastmod": "2023-06-12"
}

## Cad is comhad BAK ann?

Is éard atá i gcomhad .bak, i gcomhthéacs Microsoft SQL Server, formáid comhaid chúltaca a úsáidtear chun cóipeanna de bhunachar sonraí Freastalaí SQL a stóráil. Cuimsítear sna comhaid seo léargas ar an mbunachar sonraí ag pointe áirithe ama, lena n-áirítear a scéimre, a shonraí, agus faisnéis ghaolmhar eile. Gintear iad trí úsáid a bhaint as cúltaca ionsuite SQL Server agus feidhmiúlacht athshlánaithe agus freastalaíonn siad ar roinnt cuspóirí ríthábhachtacha:

1. **Aisghabháil Sonraí:** Soláthraíonn comhaid bak modh chun bunachar sonraí a aisghabháil i gcás caillteanas sonraí, éillithe, nó saincheisteanna eile. Trí bhunachar sonraí a athbhunú ó chomhad .bak, is féidir leat é a chur ar ais go dtí staid roimhe seo, ag laghdú aga neamhfhónaimh agus caillteanas sonraí.

2. **Imirce agus Clónáil:** Is minic a úsáidtear comhaid chúltaca chun bunachair shonraí a aistriú idir freastalaithe nó chun cóipeanna de bhunachair shonraí a chruthú chun críocha tástála, forbartha nó tuairiscithe. Cuireann siad bealach comhsheasmhach agus éifeachtach ar fáil chun bunachair shonraí a bhogadh idir timpeallachtaí.

3. ** Aisghabháil Pointe-i-Am: Ligeann** Freastalaí SQL duit aisghabháil pointe-i-am a dhéanamh ag baint úsáide as comhaid .bak. Ciallaíonn sé seo gur féidir leat bunachar sonraí a chur ar ais chuig tráth ar leith, rud a d'fhéadfadh a bheith ríthábhachtach maidir le comhlíonadh rialála nó le hiniúchadh sonraí.

4. **Athshlánú ó thubaiste:** Is cuid ríthábhachtach de phleanáil athshlánaithe tubaiste iad comhaid .bak. Cinntíonn siad go bhfuil do shonraí sábháilte agus gur féidir iad a athchóiriú go tapa i gcás teipeanna crua-earraí, tubaistí nádúrtha, nó imeachtaí tubaisteacha eile.

## Cruthaigh comhad .BAK i Freastalaí SQL

Chun comhad .bak a chruthú i Freastalaí SQL, is gnách go n-úsáideann tú orduithe SQL Server Management Studio (SSMS) nó Transact-SQL (T-SQL) cosúil le BUNACHAR SONRAÍ CÚLTA nó LOGÁ CÚLTA. Seo sampla simplithe de conas is féidir leat cúltaca bunachar sonraí a chruthú ag baint úsáide as T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Athchóirigh comhad .BAK i Freastalaí SQL

Chun bunachar sonraí a athbhunú ó chomhad .bak, is féidir leat an t-ordú RESTORE DATABASE a úsáid:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Conas comhad BAK a oscailt i SQL Server?

Chun na sonraí atá stóráilte i gcomhad .bak a oscailt agus rochtain a fháil orthu, de ghnáth ní mór duit é a chur ar ais chuig sampla Microsoft SQL Server. Seo na céimeanna ginearálta chun comhad .bak a oscailt ag baint úsáide as SQL Server Management Studio (SSMS):

1. **Seol SQL Server Management Studio**: Oscail SSMS ar do ríomhaire. Is féidir leat é a fháil de ghnáth i do Roghchlár Tosaigh nó trí chuardach a dhéanamh ar SQL Server Management Studio.

2. **Ceangail le Cás Freastalaí SQL**: I SSMS, ceangail leis an bhfreastalaí SQL áit ar mhaith leat an bunachar sonraí a chur ar ais. Beidh na ceadanna riachtanacha uait chun an oibríocht seo a dhéanamh.

3. **Athchóirigh Bunachar Sonraí**:

a. Sa phána Object Explorer ar thaobh na láimhe clé, leathnaigh an sampla Freastalaí SQL.

b. Leathnaigh an nód Bunachair Shonraí.

c. Deaschliceáil ar Bunachair Sonraí agus roghnaigh Athchóirigh Bunachar Sonraí.

4. **Sonraigh Foinse agus Ceann Scríbe**:

a. Sa leathanach Ginearálta den bhosca dialóige Athchóirigh Bunachar Sonraí, cuir isteach ainm don bhunachar sonraí nua sa réimse Chun bunachar sonraí. Seo ainm an bhunachar sonraí athchóirithe.

b. Sa Foinse alt, roghnaigh Gléas mar an cineál meáin cúltaca.

c. Cliceáil ar an gcnaipe ... in aice leis an réimse Gléas chun brabhsáil ar an gcomhad .bak is mian leat a chur ar ais.

d. Roghnaigh an comhad .bak is mian leat a oscailt agus cliceáil OK.

5. **Roghanna Athchóirigh**: Athbhreithnigh agus cumraigh na roghanna athchóirithe de réir mar is gá. Is féidir leat a shonrú cé acu ar cheart nó nár cheart bunachar sonraí atá ann cheana a fhorscríobh, roghanna athshlánaithe a shocrú, agus tuilleadh. Bí cinnte na roghanna seo a shocrú de réir do riachtanais.

6. **Cuir tús leis an Athchóirigh**: Nuair a bheidh na roghanna athchóirithe cumraithe agat, cliceáil ar an gcnaipe OK sa bhosca dialóige Athchóirigh Bunachar Sonraí. Cuirfidh SQL Server tús leis an bpróiseas athchóirithe.

7. **Rochtain ar Bhunachar Sonraí Athchóirithe**: Tar éis athchóiriú rathúil, is féidir leat rochtain a fháil ar an mbunachar sonraí athchóirithe i SQL Server Management Studio díreach mar aon bhunachar sonraí eile. Is féidir leat ceisteanna a rith, táblaí a fheiceáil, agus oibriú leis na sonraí laistigh den bhunachar sonraí.

## Comhaid BAK eile

Seo cineálacha comhaid eile a úsáideann an síneadh comhad **.bak**.

**Bunachar Sonraí**
- [BAK - Database Backup File](/database/bak/)
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)

**cluiche**
- [BAK - Terraria World or Player Backup](/game/bak-terraria/)

**Misc**
- [BAK - Backup File](/misc/bak-backup/)
- [BAK - Chromium Bookmarks Backup](/misc/bak-chromium/)
- [BAK - Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK - MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/misc/bak-vegas/)

**Socruithe**
- [BAK - Holo Launcher Backup](/settings/bak-holo/)

## Tagairtí
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
