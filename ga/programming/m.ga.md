{
  "date": "2019-10-11",
  "keywords": [
"M comhad",
"M",
"síneadh",
"formáid",
"M formáid comhaid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M - Comhad Cód Foinse Matlab",
  "description": "Foghlaim faoi chomhad Cód Foinse Matlab .m agus APIanna ar féidir leo comhaid MF a chruthú agus a oscailt.",
  "linktitle": "M",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--gam"
}
},
  "lastmod": "2020-09-10"
}

# M - Comhaid Chód Foinse Matlab

## Cad is comhad M (Matlab) ann?

Is comhad cód foinse é comhad le síneadh .m a úsáideann Matlab, ardán ríomhchláraithe agus uimhriúil a úsáidtear le haghaidh anailíse, forbairt algartaim, agus samhaltú ionsamhlúcháin. Cosúil le formáidí comhaid ríomhchlárúcháin eile, tá cód foinse i gcomhad M a fhorghníomhaíonn orduithe Matlab chun graif a bhreacadh, insamhaltaí a rith, agus oibríochtaí matamaitice eile. Is féidir le hionsamhlú Matlab amháin a bheith thar chomhaid iolracha .m den sórt sin ar féidir leo an feidhmchlár a rangú i scripteanna, ranganna, feidhmeanna nó dearbhuithe. Is féidir comhaid Matlab M a oscailt le haon eagarthóir téacs.

## Formáid Chomhaid Matlab M - Tuilleadh Eolais

Comhaid téacs is ea comhaid Matlab .m ina bhfuil cód ríomhchlárúcháin i dteanga ríomhchlárúcháin Matlab. Is féidir iad seo a oscailt agus a chur in eagar in aon eagarthóir téacs, agus iad a shábháil ar ais le cur i gcrích i mbogearraí Matlab. Tá Eagarthóir Beo i Matlab féin a úsáidtear chun scripteanna a chruthú ar meascán iad de chód, aschur agus téacs formáidithe.

### Comhaid Feidhme Matlab

Cosúil le teangacha ríomhchlárúcháin eile, is féidir leat comhad .m a chruthú nach bhfuil ann ach an sainmhíniú ar fheidhm a chomhlíonann tasc sonrach amháin. Déantar comhaid den sórt sin a shábháil freisin le síneadh .m agus cuireann sé an fheidhmiúlacht a bhaineann leis an bhfeidhm sin amháin i bhfeidhm.

### .M Comhad Sampla

Seo a leanas sampla de chomhad feidhme Matlab a ríomhann an t-am a thógann sé réad a thit ón airde h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Chun an fheidhm seo a ghlaoch ó eagarthóir Matlab nó ó chomhad .m eile, is féidir an cód seo a leanas a úsáid.
```C++
TimeToGround(100)
```

## Tagairtí

 * [Matlab - Formáidí Comhaid Thacaithe](https://www.mathworks.com/help/matlab/standard-file-formats.html)
 * [Ag úsáid Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Comhad Forfheidhmithe Cuspóir-C

## Cad is comhad M (Cuspóir-C) ann?

Tagraítear freisin do chomhad M mar chomhad feidhmithe ina bhfuil cód foinse d’aicme atá scríofa i dteanga Cuspóir-C, teanga ríomhchlárúcháin a úsáidtear chun feidhmchláir bhogearraí a scríobh do OS X agus iOS. Is é Cuspóir-C an phríomhtheanga ríomhchlárúcháin a úsáideann príomh-APIanna Apple, Cocoa and Cocoa Touch, do na hardáin seo. D’fhéadfadh go mbeadh comhaid iolracha .m in aon fheidhmchlár bogearraí amháin a forbraíodh sa teanga seo, ina mbeidh cur i bhfeidhm na ranganna clár. Is féidir iad seo a oscailt le Apple XCode, jEdit, agus eagarthóirí téacs coitianta eile.

## Cuspóir-C M Formáid Chomhaid - Tuilleadh Eolais

Scríobhtar na comhaid M i bhformáid gnáth-théacs agus úsáid á baint as comhréir ríomhchlárúcháin Cuspóir-C. Ní mór gach modh ranga a shainiú leis an gcód riachtanach go léir sna comhaid feidhmiúcháin seo. Is féidir leis na comhaid M cur chun feidhme seo ceanntásc amháin nó níos mó a allmhairiú de réir riachtanas. Insíonn an ráiteas iompórtála don tiomsaitheoir cá bhfaighidh sé an comhad ceanntásca a bhaineann leis an gcomhad feidhmithe seo. Scríobhtar an ráiteas allmhairithe mar seo a leanas.

```C++
#import "network.h"
```

Tosaíonn gach M comhad ansin leis an treoir `@cur i bhfeidhm`, agus ainm comhaid an ranga feidhmithe ina dhiaidh sin. Ina dhiaidh sin déantar cur chun feidhme na modhanna go léir a dhearbhaítear sa chomhad ceanntásca.

### M Sampla Formáid Comhaid

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## Tagairtí
 * [Maidir le Cuspóir C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
 * [Treoir Cuspóir-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

