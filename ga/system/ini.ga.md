{
  "date": "2021-07-07",
  "keywords": [
"INI",
"síneadh",
"comhad",
"formáid",
"córas",
"Tionscnamh",
"síneadh eolaire",
"cláir",
"ríomhaire",
"iarratas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "INI - Formáid Comhaid Tionscnaimh",
  "description": "Foghlaim faoi fhormáid comhaid INI agus APIs ar féidir leo comhaid INI a chruthú agus a oscailt.",
  "linktitle": "INI",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-in-gai"
}
},
  "lastmod": "2021-07-07"
}

## Cad is comhad INI ann? ##

Is doiciméad cumraíochta teachtaireachta é comhad INI le haghaidh ríomhchláir ina bhfuil eochracha poiblí le haghaidh tréithe agus rannóga a eagraíonn na tréithe i gcreat agus i ngramadach. Faigheann na doiciméid chumraíochta formáid comhaid córais seo a n-ainm ó shíneadh eolaire an chórais oibriúcháin MS-DOS INI, a sheasann don tionscnamh. Rinne sé tóir ar an gcineál seo de shocrú bogearraí. Úsáideann go leor clár ar fheidhmchláir bogearraí eile breisithe éagsúla le hainmneacha comhaid, mar CONF agus [CFG](/system/cfg/), cé go bhfuil caighdeán neamhoifigiúil bunaithe ag an bhformáid in go leor cásanna cumraíochta.

## Stair Achomair ar Chomhaid INI##

Ar dtús, ba é an príomhtheicníc cumraíochta cláir Windows ná formáid comhaid téacs a bhí comhdhéanta de línte téacs le péire ríthábhachtach amháin in aghaidh an líne, roinnte ina rannóga. Stóráladh tiománaithe gléasanna, cló-aghaidheanna agus lainseálaithe tosaigh san fhormáid seo. Stóráladh socruithe aonair freisin i gcomhaid INI ag apps.
Suas go dtí Windows 3.1x, tacaíodh leis an bhformáid ar ardáin 16-giotán Microsoft Windows. Ag tosú le Windows 95, thosaigh Microsoft ag spreagadh forbróirí chun Clárlann Windows a úsáid in ionad comhaid INI le haghaidh cumraíochta.

## Comhad INI - Sonraíochtaí Formáid Comhaid

### Eochracha/Airíonna ###

Is í an eochair/airí an eilimint is bunúsaí de chomhad INI. Scarann siombail chothrom (=) ainm agus luach gach eochrach. Ar an taobh clé den chomhartha comhionann tá an áit a thaispeánann an t-ainm. Is litreacha discréideacha iad an tsiombail chomhionann agus an leathstad i gcóras Windows agus mar sin ní féidir iad a úsáid san eochair. Is féidir aon charachtar a úsáid sa luach.

```
name=value
```

### Rannóga ###

Tá an trácht alt le feiceáil idir lúibíní cearnacha ([]) ar a líne féin. Tar éis sainmhíniú na rannóige, tá gach eochair nasctha leis an alt sin. Críochnaíonn na codanna ag an gcéad roinn eile ainmniú nó deireadh an doiciméid; níl aon deighilteoir sonrach deireadh alt ann. Ní féidir rannáin a chruachadh; ní féidir iad a ainmniú ach uair amháin agus ní gá iad a nascadh.

```
[section]
a=a
b=b
```

### Gnéithe athraithe ###

Níl sainmhíniú a nglactar leis go domhanda ag formáid comhaid INI. Áiríonn go leor feidhmchlár ríomhaireachta feidhmeanna sa bhreis orthu sin a luadh cheana. Áirítear sa liosta thíos roinnt tréithe coitianta a d’fhéadfaí a áireamh in aon chlár aonair nó nach féidir.

* Tuairimí

* Carachtair éalaithe 

* Ainmneacha dúblacha 



## Sampla INI ##

Breathnaíonn an comhad INI samplach mar seo a leanas:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Tagairt ##

* [DMP - Microsoft]( https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


