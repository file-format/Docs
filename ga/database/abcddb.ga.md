{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Foghlaim faoi fhormáid comhaid ABCDDB agus APIanna ar féidir comhaid ABCDDB a chruthú agus a oscailt.",
  "title" : "Formáid Chomhaid ABCDDB - Comhad Bunachar Sonraí Liosta Teagmhála Leabhar Seoltaí Apple",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-ga",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Cad is comhad ABCDDB ann?

Seasann an comhad leis an síneadh **.ABCDDB** do Bunachar Sonraí Liosta Teagmhála Leabhar Seoltaí Apple. Baineann sé leis an bhfeidhmchlár **Leabhar Seoltaí** ar a dtugtar **Teagmhálacha** freisin. Is feidhmchlár ionsuite é agus tá sé san áireamh le córais oibriúcháin iOS agus macOS. Cuireann feidhmchlár Teagmhálacha ar chumas úsáideoirí faisnéis a bhaineann lena dteagmhálaithe a shábháil agus a eagrú, lena n-áirítear daoine aonair, gnólachtaí agus eagraíochtaí. Ligeann an aip seo d’úsáideoirí súil a choinneáil ar shonraí amhail ainmneacha, seoltaí, uimhreacha gutháin agus seoltaí ríomhphoist, chomh maith lena dteagmhálaithe a chatagóiriú i ngrúpaí.

## Gaol le SQLite agus Cosán Tipiciúil

Stórálann Leabhar Seoltaí Apple (ar a dtugtar Teagmhálacha freisin) faisnéis teagmhála mar vCards san fhillteán meiteashonraí. **Is é an comhad _ABCDDB_ i ndáiríre _SQLite 3 datafile_**.

Is córas bainistíochta bunachar sonraí móréilimh é SQLite atá deartha le bheith éadrom agus féinchuimsitheach. Úsáidtear é i go leor cineálacha éagsúla bogearraí agus gléasanna. Is cineál RDBMS é SQLite, rud a chiallaíonn go stórálann sé sonraí i dtáblaí a bhaineann lena chéile trí eochracha. Is féidir leis raon cineálacha sonraí a láimhseáil, lena n-áirítear slánuimhreacha, uimhreacha snámhphointe, teaghráin, agus sonraí dénártha. Ina theannta sin, tacaíonn SQLite le hidirbhearta, a chuireann ar chumas úsáideoirí oibríochtaí bunachar sonraí iolracha a dhéanamh le chéile mar aonad amháin oibre.

Go hiondúil stóráiltear an comhad le síneadh ABCDDB anseo

`~/Leabharlann/Tacaíocht Feidhmchláir/Leabhar Seoltaí/Leabhar Seoltaí-v22.abcddb`

## Bunachar sonraí truaillithe Teagmhálaithe a dheisiú

Tóg an cúltaca ar dtús sula ndéanann tú iarracht é seo a dhéanamh. Ansin déan nascleanúint chuig

`~/Leabharlann/Tacaíocht Feidhmchláir/Leabhar Seoltaí`

San eolaire sin, gheobhaidh tú trí chomhad lena n-áirítear an ceann a bhfuil síneadh .abcddb aige

- `leabhar seoltaí-v22.abcddb`
- `leabhar seoltaí-v22.abcddb-wal`
- `leabhar seoltaí-v22.abcddb-shm`

Scrios na comhaid seo go léir agus athoscail an Teagmhálacha a thosóidh sé ag obair arís.

## Athchóirigh bunachar Seoladh Leabhar Seoltaí ó Chúltaca

Glac leis, go bhfuil do theagmhálaithe bunachar sonraí Seoltaí stóráilte in `addressbook-v22.abcddb`

- An Chéad cúltaca do shonraí Seoladh Leabhar agus scor gach feidhmchlár.
- Bog do chomhad bunachar sonraí chuig fochomhadlann `~/Leabharlann/Tacaíocht Iarratais/Leabhar Seoltaí
- Seoladh **Leabhar Seoltaí.app**.

## Easpórtáil sonraí comhaid ABCDDB chuig Microsoft Access

Ós rud é gur comhad sonraí SQLite 3 an comhad, is féidir leat na sonraí taobh istigh den chomhad abcddb a onnmhairiú isteach i Microsoft Access ag baint úsáide as cónascaire ODBC.

Is leabharlann bogearraí agus tiománaí é cónascaire SQLite ODBC a chuireann ar chumas feidhmchláir a thacaíonn le comhéadan ODBC nascadh le bunachar sonraí SQLite. Áiríonn sé leabharlann a shainíonn comhéadan ODBC, agus tiománaí a aistríonn an comhéadan seo ina ghlaonna chuig an API SQLite. Chun cónascaire SQLite ODBC a úsáid, ní mór duit é a shuiteáil ar dtús agus ansin foinse sonraí ODBC a shocrú ar do ríomhaire. Tar éis na céimeanna seo a chomhlánú, beidh aon iarratas atá feistithe le tacaíocht ODBC in ann ceangal leis an bhfoinse sonraí agus sonraí a aisghabháil ó bhunachar sonraí SQLite.

## Tagairtí
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Bunachar Sonraí Teagmhála Le haghaidh Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Conas is féidir liom comhad abcddb a oscailt nó a easpórtáil i Windows 7 Excel?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -fuinneoga-7-excel)

