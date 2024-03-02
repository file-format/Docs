{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VCF - Comhad Teagmhála Fíorúil",
  "description": "Foghlaim faoi fhormáid comhaid VCF agus APIs is féidir comhaid VCF a chruthú agus a oscailt.",
  "linktitle": "VCF",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-vc-gaf"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad VCF ann?

Is formáid comhaid dhigitigh é VCF (Formáid Cárta Fíorúil) nó vCard chun faisnéis teagmhála a stóráil. Úsáidtear an fhormáid go forleathan le haghaidh idirmhalartú sonraí i measc feidhmchlár malartaithe faisnéise a bhfuil tóir orthu. Tagann formhór na gcóras oibriúcháin ar nós Windows agus MacOS le feidhmchláir réamhshocraithe chun na comhaid seo a chruthú agus a oscailt. Is féidir faisnéis teagmhála le haghaidh teagmhálaí amháin nó níos mó a bheith i gcomhad VCF amháin. De ghnáth bíonn faisnéis i gcomhad VCF mar ainm teagmhálaithe, seoladh, uimhir theileafóin, ríomhphost, lá breithe, grianghraif agus fuaime chomh maith le roinnt réimsí eile. Agus tacaíocht á fáil ag cliaint agus seirbhísí ríomhphoist, níl aon chaillteanas sonraí le linn aistriú teagmhálacha trí fhormáid vCard a úsáid. Is é an cineál meán le haghaidh formáid comhaid VCF ná téacs / vcard.

## Formáid comhaid VC

Is comhaid téacsúla iad comhaid VCF agus tá siad inléite ag an duine. Is féidir iad seo a oscailt in eagarthóirí téacs ar nós Notepad ar Microsoft Windows agus TextEdit ar MacOS. Má tá íomhá sa chomhad, áfach, ní thaispeánfar é san eagarthóir téacs.

Soláthraíonn [Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) tacaíocht chun comhaid VCF a oscailt chomh maith le thiontú go roinnt formáidí eile ar nós an fhormáid [MSG](/email/msg/) a bhfuil an-tóir uirthi. Feabhsaíodh formáid comhaid VCF le himeacht ama ó leagan 2.1 go 4.0 ag cur faisnéis mhionsonraithe leis an bhformáid comhaid. Úsáidtear an fhormáid freisin chun teagmhálacha teileafóin a onnmhairiú agus a allmhairiú níos déanaí i bhfeiste eile.

{{< figure src="../VCF.png" alt="Formáid comhaid VC" >}}

### VCF 2.1 Sampla

Seo a leanas sampla de leagan 2.1.

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### VCF 3.0 Sampla

Seo a leanas sampla de leagan 3.0.

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### VCF 4.0 Sampla

Seo a leanas sampla de leagan 4.0.

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## Tagairtí

* [VCF - Le Vicipéid](https://ga.wikipedia.org/wiki/VCard)


