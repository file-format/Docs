{
  "date" : "2023-01-16",
  "keywords" : [ "DB-WAL", "what is a DB-WAL file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Foghlaim faoi fhormáid comhaid DB-WAL agus APIs ar féidir leo comhaid DB-WAL a chruthú agus a oscailt.",
  "title" : "Formáid Comhaid DB-WAL - Logchomhad Scríobh Chun Tosaigh Bunachar Sonraí SQLite",
  "linktitle" : "DB-WAL",
  "menu" : {
    "docs" : {
      "identifier":"database-db-wal-ga",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Cad is comhad DB-WAL ann?

Tá baint ag an síneadh comhad .db-wal le SQLite, córas bainistíochta bunachar sonraí coibhneasta foinse oscailte a bhfuil tóir air. Is rogha eile í formáid comhaid WAL (gearr do Write-Ahead Log) ar an iris thraidisiúnta rolladh siar a úsáideann SQLite. Soláthraíonn sé níos mó rialaithe concurrency, rud a ligeann do phróisis iolracha an bunachar sonraí a léamh ag an am céanna, agus fós ag soláthar cumais tuairteála-aisghabhála. Úsáidtear an comhad .db-wal chun athruithe a rinneadh ar an mbunachar sonraí nach bhfuil geallta go fóill don phríomhchomhad bunachar sonraí (le síneadh .db) a stóráil.

## Formáid WAL Ginearálta

I bhformáid comhaid WAL (Write-Ahead Log), déantar athruithe a dhéantar ar an mbunachar sonraí a scríobh chuig an gcomhad WAL ar dtús sula gcuirtear faoi cheangal iad don phríomhchomhad bunachar sonraí. Ligeann sé seo rochtain níos comhthráthach ar an mbunachar sonraí, mar is féidir próisis iolracha a léamh ón mbunachar sonraí agus athruithe á ndéanamh. Ina theannta sin, soláthraíonn formáid comhaid WAL cumais um aisghabháil tuairteála, rud a ligeann don bhunachar sonraí a rolladh ar ais go dtí staid roimhe sin i gcás múchadh gan choinne.

## Difríocht idir formáid DB-WAL agus WAL

Tá baint ag formáidí comhaid .db-wal agus WAL le SQLite, córas bainistíochta bunachar sonraí coibhneasta foinse oscailte a bhfuil tóir air. Mar sin féin, tá difríocht subtle idir an dá.

Go bunúsach is comhad WAL é an comhad .db-wal, ach le síneadh comhaid eile. Baintear úsáid as an gcomhad .db-wal chun athruithe a rinneadh ar an mbunachar sonraí a stóráil nach bhfuil geallta fós don phríomhchomhad bunachar sonraí (le síneadh .db), agus úsáidtear formáid comhaid WAL chun loga réamhscríofa na n-athruithe ar an mbunachar sonraí a stóráil .

I bhfocail eile, is cineál sonrach de chomhad WAL é comhad .db-wal a úsáideann bunachair shonraí SQLite chun athruithe a rinneadh ar an mbunachar sonraí nach bhfuil tiomanta go fóill don phríomhchomhad bunachar sonraí a stóráil. Is í formáid comhaid WAL an téarma ginearálta don chineál seo formáid comhaid.

Mar sin, is é WAL an téarma ginearálta don fhormáid comhaid, is é .db-wal cur i bhfeidhm sonrach an fhormáid comhaid WAL a úsáideann bunachair shonraí SQLite.

## Tagairtí
* [Formáid Comhaid mód WAL](https://www.sqlite.org/walformat.html)

* [Scríobh-Logáil Roimh Ré]( https://www.sqlite.org/wal.html)


