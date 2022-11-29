{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - Virtuell kontaktfil",
  "description":"Läs mer om VCF-filformat och API:er som kan skapa och öppna VCF-filer.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är VCF fil?

VCF (Virtual Card Format) eller vCard är ett digitalt filformat för att lagra kontaktinformation. Formatet används ofta för datautbyte bland populära applikationer för informationsutbyte. De flesta operativsystem som Windows och MacOS kommer med standardprogram för att skapa och öppna dessa filer. En enda VCF-fil kan innehålla kontaktinformation för en eller flera kontakter. En VCF-fil innehåller vanligtvis information som kontaktens namn, adress, telefonnummer, e-post, födelsedag, fotografier och ljud utöver ett antal andra fält. Eftersom det stöds av e-postklienter och tjänster, sker det ingen förlust av data under överföringen av kontakter via vCard-formatet. Medietypen för VCF-filformat är text/vcard.

## VCF filformat

VCF-filer är textmässiga till sin natur och är läsbara för människor. Dessa kan öppnas i textredigerare som Notepad på Microsoft Windows och TextEdit på MacOS. Om det finns en bild i filen kommer den dock inte att visas i textredigeraren.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) ger stöd för öppna VCF-filer samt konvertera till ett antal andra format som det populära formatet [MSG](/sv/email/msg/). VCF-filformat förbättrats med tiden från version 2.1 till 4.0 och lägger till detaljerad information till filformatet. Formatet används också för att exportera telefonkontakter och senare importera till en annan enhet.

{{< figure src="../VCF.png" alt="VCF filformat" >}}

### VCF 2.1 Exempel

Följande är ett exempel på version 2.1.

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

### VCF 3.0 Exempel

Följande är ett exempel på version 3.0.

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

### VCF 4.0 Exempel

Följande är ett exempel på version 4.0.

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

## Referenser

* [VCF - av Wikipedia](https://en.wikipedia.org/wiki/VCard)

