{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ICS - Formáid Chomhaid iCalendar",
  "description": "Foghlaim faoi fhormáid comhaid ICS agus APIs ar féidir leo comhaid ICS a chruthú agus a oscailt.",
  "linktitle": "ICS",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ic-gas"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad ICS ann?

Is caighdeán idirlín (RFC 2445) é an tSonraíocht Croí-Oibiachta um Fhéilire agus Sceidealú Idirlín (iCalendar) chun imeachtaí féilire agus sceidealaithe a mhalartú agus a imscaradh. Tá formáid iCalendar idir-inoibritheach, rud a chinntíonn malartú faisnéise féilire i measc na n-úsáideoirí a bhfuil feidhmchláir éagsúla ríomhphoist acu. Déanann iCalendar na sonraí ionchuir a fhormáidiú mar Eisínteachtaí Ilchuspóireacha Ríomhphoist Idirlín (MIME) agus éascaíonn sé an réad a mhalartaítear trí phrótacail iompair éagsúla. Is féidir leis na prótacail iompair seo a bheith ina SMTP, HTTP, cumarsáid asincrónach pointe go pointe, agus iompar líonra bunaithe ar mheáin fhisiciúla.

Ligeann iCalendar d’úsáideoirí imeachtaí, tascanna a bhraitheann ar dháta/am, agus faisnéis shaor/ghnóthach a roinnt trí ríomhphost chuig úsáideoirí eile ar féidir leo freagra a thabhairt ar ais. Stórálann comhaid iCalendar ag baint úsáide as iarmhíreanna .ics .iCalendar nó .ifb le cineál MIME de text/féilire. Coinnítear iCalendar le bheith féinspleách gan aon spleáchas ar phrótacal iompair. Is féidir le freastalaithe Gréasáin (le prótacal HTTP) faisnéis iCalendar a iompar agus is féidir le leathanaigh ghréasáin sonraí iCalendar a áireamh i bhfoirm leabaithe ag baint úsáide as iCalendar.

## Stair Achomair ar Fhormáid Chomhaid ICS

In 1998, the Internet Engineering Task Force (IETF) defined iCalendar as a standard (RFC 2445). The standard was documented by Frank Dawson(Lotus Notes Corporation) and Derik Stenerson ( Microsoft). In 2009, the standard was again refined by Bernard Desruisseaux (Oracle) as RFC 5545. An uair seo cuireadh roinnt gnéithe nua leis agus rinneadh dul i léig ar roinnt gnéithe atá as dáta. In 2016, scaoileadh RFC 7986 agus méadaíodh é go iCalendar RFC bunaidh. Chuir RFC 7986 tréithe nua leis an bpríomhchuspóir VCALENDAR agus tugadh gnéithe tacaíochta nua isteach freisin do chórais chomhdhála.

## Formáid Chomhaid ICS ##

Is é an cineál MIME a úsáideann sonraí iCalendar ná text/calendar”. Is é UTF-8 an tacar carachtar réamhshocraithe le haghaidh iCalendar, ach trí pharaiméadair a sholáthar i MIME, is féidir tacar carachtar difriúil a úsáid. Tá rannóga i gcomhad iCalendar, i measc na n-alt seo VCALENDAR, an chuid dhomhanda a chuimsíonn gach cuid eile. Sainmhíníonn rannán VEVENT imeachtaí, liostaíonn VTODO gach rud atá le déanamh, tá iontrálacha dialainne i VJOURNAL, agus sonraíonn VTIMEZONE faisnéis crios ama. ceadaítear ilchodanna de chatagóir chomhchosúil. I gcás go leor imeachtaí, is féidir le hailt VEVENT iolracha a bheith i láthair i gcomhad iCalendar.

### Línte Ábhair ###

Eagraítear na réada iCalendar i línte ar leith téacs línte ábhair”. Sa chomhaid seo, cuireann seicheamh CRLF deireadh le líne ach tá fad na líne teoranta do 75 octets gan briseadh na líne a áireamh. Is féidir mír fhada sonraí a shíneadh go dtí go leor línte.

### Liosta agus deighilteoirí Réimse ###

Sonraíonn airíonna agus paraiméadair liosta luachanna atá scartha le carachtar COMMA. Úsáidtear teaghráin luaite le haghaidh luachanna paraiméadar bunaithe ar URI. Is féidir liosta de na paraiméadair a thógáil de réir an luach maoine. Ní mór gach paraiméadar maoine ar an liosta seo a bheith scartha le SEIMICOLON.

I liosta luachanna, leithlisíonn SEMICOLON paraiméadair maoine agus luachanna maoine ar leithligh COMMA. Tugtar sampla thíos:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Illuachanna

Is féidir luachanna iolracha a bheith ag roinnt maoine. Níl ort ach líne ábhair nua a ghiniúint leis an ainm maoine an riail bhunúsach maidir le hairíonna illuacha. Mar sin féin, ní ceadmhach airíonna illuacha a úsáid i gcás aon luacha le héagsúlachtaí teanga.

### Ábhar Dénártha

Laistigh de réad iCalendar, is féidir le luach maoine tagairt a dhéanamh d'ábhar dénártha sonraí a chuirtear in aonán seachtrach MIME ag baint úsáide as URI. Is féidir ábhar dénártha inlíne a úsáid i gcásanna speisialta le paraiméadar ENCODING, nuair is gá don iarratas réad iCalendar a chur in iúl mar aonán aonair. Míníonn an sampla seo a leanas airí ATTACH le tagairt URI:

ATTACH: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Tacar Carachtair

Cé gurb é UTF-8 an scéim thacair charachtair réamhshocraithe le haghaidh iCalendar, ní shonraítear aon pharaiméadar maoine chun tacar carachtair luach maoine a shainiú. in aistrithe MIME NÍ MÓR paraiméadar charset a úsáid le haghaidh tacar carachtair reatha.

## Conas Comhad ICS a Oscailt?

Tá bealaí éagsúla ann chun comhad ICS a oscailt. Tá mionsonraí orthu seo thíos.

1. Oscail ICS ag baint úsáide as Feidhmchláir Féilire

Is féidir leat comhaid ICS a oscailt ag baint úsáide as feidhmchláir Calendar cosúil le Microsoft Outlook, Google Calendar nó Apple Calendar. Má tá na feidhmchláir seo suiteáilte ar do ghléas, is féidir leat an comhad ICS a oscailt leis na feidhmchláir seo ach cliceáil faoi dhó air. Déanfaidh sé seo imeachtaí an chomhaid ICS a allmhairiú isteach i d'fhéilire.

1. Oscail comhad ICS in Eagarthóir Téacs

Is féidir leat comhad ICS a oscailt freisin in aon eagarthóir téacs ar nós Microsoft Notepad nó Apple TextEdit. Nuair a osclaítear iad, feicfidh tú na línte DTSTART agus DTEND a léiríonn amanna tosaigh agus deiridh an imeachta.

1. Iompórtáil de láimh comhad ICS san App Calendar

Is féidir leat freisin comhad ICS a allmhairiú isteach i d'aip féilire trí úsáid a bhaint as roghanna Imiprot & easpórtála na n-aipeanna féilire seo. Cuirfidh sé seo na himeachtaí comhaid ICS le do féilire.

## Tagairtí

* [Sonraíocht na gCroí-Oibiachtaí maidir le Féilire agus Sceidealú Idirlín](https://www.ietf.org/rfc/rfc5545.txt)

* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)

* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)


