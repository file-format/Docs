{
  "date": "2021-06-21",
  "keywords": [
"UDL",
"síneadh",
"comhad udl",
"formáid comhaid udl",
"Cineál Comhaid Bunachar Sonraí",
"Formáid Comhaid Bunachar Sonraí",
"cad is comhad udl ann"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid UDL agus APIanna ar féidir leo comhaid UDL a chruthú agus a oscailt.",
  "title": "UDL - Comhad Nasc Sonraí Uilíoch Microsoft",
  "linktitle": "UDL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ud-gal"
}
},
  "lastmod": "2021-06-21"
}

## Cad is comhad UDL ann?
Tugtar comhad Nasc Sonraí Uilíoch Microsoft ar an gcomhad le síneadh .udl; tréithe nasctha a shonrú; in úsáid ag feidhmchláir Windows chun nasc a bhunú leis an mbunachar sonraí. Tá an teaghrán ceangail le haghaidh foinse sonraí OLE DB sa chomhad UDL; le hainm úsáideora agus pasfhocal agus airíonna riachtanacha teaghrán ceangail. Chun na hairíonna a shonrú go díreach de láimh i teaghrán nasc a sheachaint, is féidir bosca dialóige Data Link Properties a úsáid chun faisnéis nasc a shábháil i gcomhad .udl mar mhalairt air sin.

## Formáid Comhaid UDL
Go bunúsach, is comhad téacs simplí é comhad UDL (Universal Data Link) a chuimsíonn teaghrán nasc bunachar sonraí le tréithe nó airíonna ar leith. Nuair a chruthaítear an comhad UDL, is féidir é a thástáil trí úsáid a bhaint as SQL Server Management Studio chun an nascacht a fhíorú.

### Airíonna teaghrán ceangail
Is féidir na hairíonna seo a leanas a shocrú i UDL chun an nascacht cheart a chinntiú:

- **Ainm an Freastalaí**: suíomh an fhreastalaí ina bhfuil an bunachar sonraí a bhfuil tú ag iarraidh a rochtain suite.
- **Roghanna Fíordheimhnithe**
- **Fíordheimhniú Windows**: Fíordheimhniú le Freastalaí SQL ag baint úsáide as dintiúir chuntas Windows an úsáideora logáilte isteach faoi láthair.
- **Fíordheimhniú Freastalaí SQL**: Fíordheimhniú ag baint úsáide as ID logáil isteach agus pasfhocal.
- **Eolaire Gníomhach - Comhtháite**: Fíordheimhniú comhtháite le haitheantas Azure Active Directory; Is féidir é a úsáid freisin le haghaidh fíordheimhnithe Windows le SQL Server.
- ** Eolaire Gníomhach - Pasfhocal**: Aitheantas úsáideora agus pasfhocal fíordheimhnithe le haitheantas Azure Active Directory.
- ** Eolaire Gníomhach - Uilíoch le tacaíocht MFA**: Fíordheimhniú idirghníomhach le haitheantas Azure Active Directory.
- **Eolaire Gníomhach - Príomhoide Seirbhíse**: Fíordheimhniú le príomhoide seirbhíse Azure Active Directory.
- **Freastalaí SPN**: Má úsáideann tú nasc iontaofa, is féidir leat príomhainm seirbhíse (SPN) a shonrú don fhreastalaí.
- **Ainm úsáideora**: Clóscríobh an ID Úsáideora le húsáid le haghaidh fíordheimhnithe nuair a shíníonn tú isteach san fhoinse sonraí.
- **Pasfhocal**: Clóscríobh an focal faire le húsáid le haghaidh fíordheimhnithe nuair a shíníonn tú isteach san fhoinse sonraí.
- **Pasfhocal folamh**: Nuair a dhéantar é a sheiceáil, cuireann sé ar chumas an tsoláthraí sonraithe pasfhocal bán a úsáid sa teaghrán ceangail.
- **Ceadaigh pasfhocal a shábháil**: Ligeann sé seo an focal faire a shábháil leis an teaghrán ceangail.
- **Bain úsáid as criptiúchán láidir le haghaidh sonraí**: cripteofar sonraí a chuirtear tríd an nasc.
- **Trust server certificate**: The server's certificate will be validated.
- **Bunachar Sonraí**: Ainm an bhunachair shonraí ar mhaith leat rochtain a fháil air.
- **Ceangail comhad bunachar sonraí mar ainm bunachar sonraí**: Sonraíonn sé ainm an phríomhchomhaid do bhunachar sonraí iniata.

## Tagairtí ##

* [Comhpháirteanna Microsoft Rochtana Sonraí](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)

* [Cumraíocht Nasc Sonraí Uilíoch (UDL)](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)


