{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid BML - Comhad Teanga Bean Markup",
  "description": "Foghlaim faoi fhormáid comhaid BML agus APIanna ar féidir leo comhaid BML a chruthú agus a oscailt.",
  "linktitle": "BML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-bm-gal"
}
},
  "lastmod": "2021-08-12"
}

## Cad is comhad BML ann?

Comhad le síneadh .bml is ea comhad Bean Markup Language a stórálann ranganna Java chun tacú le haipeanna Java. Ligeann sé seo rochtain ar réada agus modhanna Java, agus ní gá feidhmiúlacht nua a chruthú ag baint úsáide as ranganna Java. Sonraíonn sé conas a nasctar na comhpháirteanna lena chéile chun tascanna úsáideacha a dhéanamh. D'fhorbair IBM alphaWorks BML chun cur síos a dhéanamh ar na caidrimh struchtúir agus comhpháirteanna. Is féidir comhaid BML a oscailt agus a fheiceáil le haon eagarthóir téacs ar nós Brabhsálaithe Gréasáin, Microsoft Notepad agus Notepad++.

## Formáid Chomhaid BML

Tá dhá chur i bhfeidhm BML curtha ar fáil ar shuíomh Gréasáin alphaworks IBM. Is é atá sa Chéad chur i bhfeidhm ná ateangaire a ‘imríonn’ script BML chun an t-ordlathas pónairí atá ag teastáil a ghiniúint. Is é an dara cur i bhfeidhm tiomsaitheoir a thiomsaíonn aon script BML isteach i gcód Java saor ó mhachnamh. Tá sé seo buntáisteach sa chiall go gceadaíonn sé struchtúr idir-chomhpháirteach an fheidhmchláir a ghabháil ag baint úsáide as teanga atá deartha chun na críche sainiúla seo leis an gcumas breise é a thiomsú i gcód ‘rialta’ Java.

## Clibeanna BML

Seo a leanas míniú ar chuid de na clibeanna a úsáidtear sa teanga BML:

### Tá an<bean> clib:

Tá an<bean> úsáidtear eilimint chun pónairí nua a chruthú nó chun pónairí a chuardach de réir ainm. Tá an<bean> Tá an chlib san fhormáid:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
Tá baint ag an id sa chlib leis an gclár oibiachtaí don JavaBean.

### Tá an<string> chlib

Tá dhá bhealach ann ar féidir an chlib teaghrán a úsáid:

 1. Chun teaghrán neamhfholamh a chruthú:

```
<string [value = "value of string"]> [value of string]
</string>
```
 2. Chun teaghrán folamh a chruthú:

```
<string/>
```
## Tagairtí

* [Object-Oriented Messaging with XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [An Teanga Fhisiciúil Mharcála](http://web.mit.edu/mecheng/pml/standards.htm)



