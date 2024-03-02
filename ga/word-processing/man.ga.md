{
  "date": "2021-07-25",
  "keywords": [
"fear",
"comhad",
"síneadh",
"cineál",
"formáid",
"Unix lámhleabhar"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MAN - Unix Lámhleabhar",
  "description": "Foghlaim faoi fhormáid comhaid FODT agus APIs ar féidir leo comhaid MAN a chruthú agus a oscailt.",
  "linktitle": "MAN",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-ma-gan"
}
},
  "lastmod": "2021-07-25"
}

## Cad is comhad MAN ann?

Seasann comhad le síneadh .man do man page arb é lámhleabhar úsáideora ríomhchlárúcháin Unix é i bhfoirm doiciméadú bogearraí. Úsáideann an áirgiúlacht `Man` é, atá san áireamh in Unix, a úsáidtear chun na doiciméid a fheiceáil. Tá faisnéis i ndoiciméadú na mbogearraí i gcodanna agus i leathanaigh ar féidir iad a aisghabháil trí úsáid a bhaint as fóntais Man from command terminal trí orduithe a eisiúint. Toisc go bhfuil sé ar fáil sa ríomhaire mar chóip bhog de dhoiciméid, ní theastaíonn aon chóip chlóite nó nasc idirlín chun é a rochtain.

## Formáid Chomhaid Man Lámhleabhar Unix - Tuilleadh Eolais

Stóráiltear leathanaigh fhir i bhformáid gnáth-théacs agus is féidir iad a chruthú agus a oscailt in aon eagarthóir téacs le breathnú orthu nó le haghaidh eagarthóireachta orthu. In UNIX, déantar faisnéis ó na leathanaigh Man a aisghabháil trí orduithe a eisiúint ón teirminéal a chuimsíonn tagairt d'uimhreacha alt agus leathanaigh ón lámhleabhar.

### Rannóga agus Leathanaigh

Is é fear Unix lámhleabhar an chórais ina dtagraíonn gach argóint leathanach don ordú d'ainm cláir, fóntais nó feidhme. déanfaidh an t-ordú, má chuirtear faisnéis alt ar fáil dó, cuardach don leathanach sa roinn shonrach sin. Mar sin féin, is é an t-iompar réamhshocraithe ná cuardach a dhéanamh ar an leathanach i ngach cuid agus an chéad leathanach a thaispeáint beag beann ar an bhfuil sé in ailt iolracha.

### Uimhreacha Alt

Seo a leanas an t-eolas faoi na huimhreacha sa lámhleabhar agus na cineálacha leathanach atá iontu ina dhiaidh sin.

|Uimhir na Rannóige|Cineál na leathanach|
---|---|
|1|Cláir inrite nó orduithe sliogán|
|2|Glaonna córais (feidhmeanna arna soláthar ag an eithne)|
|3|Glaonna leabharlainne (feidhmeanna laistigh de leabharlanna clár)|
|4|Comhaid speisialta (a fhaightear de ghnáth in /dev)|
|5|Formáidí comhaid agus gnásanna, m.sh. /etc/passwd|
|6|Cluichí|
|7|Ilghnéitheach (lena n-áirítear macra-phacáistí agus coinbhinsiúin), eg man(7), groff(7)|
|8|Orduithe riaracháin córais (go hiondúil don fhréamh amháin)|
|9|Gnáthaimh eithne [Neamhchaighdeánach] |

## Sampla - Conas Leathanaigh MAN a Léigh?

Seo sampla conas informatino a fháil faoi ordú MkDir ag baint úsáide as an ordú Man.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## Tagairtí

* [Sonraíochtaí Teicniúla OpenDocument - Le Vicipéid](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)

* [fear(1) - leathanach láimhe Linux](https://man7.org/linux/man-pages/man1/man.1.html)


