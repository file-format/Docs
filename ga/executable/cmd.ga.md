{
  "date": "2021-07-12",
  "keywords": [
"comhad cmd",
"cad is comhad cmd ann",
"comhad",
"cmd shampla",
"síneadh comhad cmd",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid CMD agus APIanna ar féidir leo comhaid CMD a chruthú agus a oscailt.",
  "title": "CMD - Formáid Comhaid Ordú Windows",
  "linktitle": "CMD",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-cm-gad"
}
},
  "lastmod": "2021-07-12"
}

## Cad is comhad CMD ann?
Is éard atá i gcomhad CMD script ina bhfuil orduithe amháin nó iolracha i bhfoirm gnáth-théacs a reáchtáiltear chun tascanna éagsúla a dhéanamh. Tá sé cosúil le comhad [BAT](/executable/bat/), a úsáidtear go ginearálta freisin chun baisc orduithe inrite a stóráil. Úsáidtear na comhaid CMD go forleathan i gcóras oibriúcháin Microsoft Windows. Tugadh na comhaid seo isteach sna 90idí beagnach ach fós úsáidtear iad sa chóras oibriúcháin Windows is déanaí. De ghnáth scríobhtar na comhaid seo chun níos mó ná ordú amháin a fhorghníomhú i seicheamh.

## Formáid comhaid CMD
Is formáid comhaid é CMD a úsáideann cláir inrite ar stíl CP/M. Go ginearálta is féidir é a chur i gcomparáid le [COM](/executable/com/) in CP/M-80 agus [EXE](/executable/exe/) in DOS. Tá idir 1 agus 8 ngrúpa de chód nó de shonraí agus ceanntásc 128 beart i gcomhad CMD. Is féidir le gach grúpa a bheith suas le 1 mb. Is féidir faisnéis athlonnaithe agus Eisínteachtaí Córais Cónaithe (RSXanna) a bheith sna comhaid CMD ina leaganacha níos déanaí. Is núíosach é an CMD i gcomparáid le comhad [BAT](/executable/bat/); a úsáidtear le haghaidh MS-DOS roimh scaoileadh fuinneoga In MS-DOS. Cé gur féidir leat comhaid a shábháil fós le síneadh .bat inniu, úsáideann go leor daoine an síneadh .cmd chun a gcuid scripteanna inrite a shábháil.

### Sonraíocht i bhformáid CMD

Ar thús an chinnteidil tá liosta na ngrúpaí atá i láthair sa chomhad mar aon lena gcineálacha. Is féidir gach cineál a úsáid aon uair amháin ar a mhéad. Is iad na cineálacha seo:

- Cód
- Sonraí
- Breise
- Cruachán
- Úsáideoir 1
- Úsáideoir 2
- Úsáideoir 3
- Úsáideoir 4
- Cód Roinnte

Mar an gcéanna Réimír Deighleog an Chláir i DOS, is é náid an chéad 256 beart den ghrúpa sonraí. CP/M-86 a bheidh iontu leis an leathanach nialais. Mura bhfuil grúpa sonraí ann, úsáidfear na chéad 256 beart den ghrúpa cód ina ionad sin.
## Sampla comhad CMD
Seo a leanas sampla de script CMD chun faisnéis chórais a thaispeáint.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Tagairtí 

* [Conas Script CMD a Scríobh](https://smallbusiness.chron.com/write-cmd-script-53226.html)

* [Comhad CMD (CP/M) - le Vicipéid]( https://en.wikipedia.org/wiki/CMD_file_(CP/M))


