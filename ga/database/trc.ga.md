{
  "date": "2021-08-24",
  "keywords": [
"comhad trc",
"formáid comhaid trc",
"cad is comhad trc ann",
"comhad",
"sampla trc",
"síneadh comhad trc",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid TRC agus APIanna ar féidir leo comhaid TRC a chruthú agus a oscailt.",
  "title": "TRC - Rianchomhad Freastalaí SQL",
  "linktitle": "TRC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-tr-gac"
}
},
  "lastmod": "2021-08-24"
}

## Cad is comhad TRC ann?
I gcomhad a bhfuil iarmhír .trc aige tá rian thorthaí ghníomhaíocht bhunachar sonraí freastalaí SQL Miscrosoft. Cruthaítear na comhaid seo le Bogearraí SQL Server Profiler; pacáistithe de ghnáth le bogearraí Microsoft SQL Server. Is féidir le riarthóirí an bhunachair sonraí seicheamh ráiteas bunachar sonraí a anailísiú agus is féidir leo athbhreithniú a dhéanamh ar an rian loga má tá amhras ann go bhfuil earráidí nó rabhaidh de chineál éigin ann. De ghnáth bíonn na comhaid seo suite i bhfillteán tipiciúil LOG MSSQL taobh istigh den eolaire Comhaid Cláir ar chóras oibriúcháin Windows.

## Formáid comhaid TRC
Úsáideann SQL Server Profiler an fhormáid comhaid TRC chun rian nua a ghiniúint go huathoibríoch de na ráitis a rinne freastalaí MS SQL le déanaí. Úsáideann an Próifíleoir Freastalaí SQL an teimpléad réamhshocraithe le haghaidh aon rian nua. Mar sin féin, tá roinnt teimpléid réamhshainithe san áireamh sna bogearraí chun monatóireacht a dhéanamh ar chineálacha áirithe imeachtaí. Chomh maith leis sin is féidir SQL Server Profiler a úsáid chun teimpléid a chruthú a shainíonn na haicmí imeachta agus na colúin sonraí le cur san áireamh i rianta.

### Teimpléid Réamhshainithe
Seo liosta de na teimpléid réamhshainithe atá san áireamh in SQL Server Profiler:
- **SP_Counts**: Gabhann iompraíocht forghníomhaithe nós imeachta stóráilte le himeacht ama.
- **Caighdeánach**: Túsphointe cineálach chun rian a chruthú.
- **TSQL**: Gabhann sé gach ráiteas Transact-SQL a chuireann cliaint isteach chuig SQL Server agus an t-am a eisítear.
- **TSQL_Duration**: Gabhann sé gach ráiteas Transact-SQL a chuir cliaint isteach chuig SQL Server, a gcuid ama forghníomhaithe, agus grúpálann sé iad de réir achair.
- **TSQL_Grouped**: Bain úsáid as chun fiosrúcháin ó chliant nó ó úsáideoir ar leith a fhiosrú.
- **TSQL_Locks**: Bain úsáid as chun fabhtcheartú a dhéanamh ar thréimhsí glasa, am saor a ghlasáil, agus imeachtaí formhéadaithe a ghlasáil.
- **TSQL_Replay**: Bain úsáid as chun tiúnadh atriallach a dhéanamh, amhail tástáil tagarmhairc.
- **TSQL_SPs**: Úsáid chun anailís a dhéanamh ar na céimeanna comhpháirte de nósanna imeachta stóráilte.
- **Tiúnadh**: Úsáid chun rian-aschur a tháirgeadh is féidir le Comhairleoir Tiúnadh Inneall Bunachar Sonraí a úsáid mar ualach oibre chun bunachair shonraí a choigeartú.
### Comhghaol rian le sonraí Loga Feidhmíochta Windows
Is féidir an Próifíleoir Freastalaí SQL a úsáid chun logáil feidhmíochta Microsoft Windows a oscailt, chun na cuntair a roghnú le comhghaolú le rian, agus na cuntair feidhmíochta roghnaithe a thaispeáint taobh leis an rian sa MS SQL Server Profiler GUI. Chun na sonraí logála feidhmíochta a chomhghaolú leis an rian-imeacht roghnaithe a chur in iúl, barra dearg ingearach i bpána fuinneoige sonraí Monatóireachta an Chórais de SQL Server Profiler.


## Tagairtí ##

* [Próifíleoir Freastalaí SQL]( https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)


