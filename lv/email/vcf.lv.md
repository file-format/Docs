{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VCF — virtuālais kontaktu fails",
  "description": "Uzziniet par VCF failu formātu un API, kas var izveidot un atvērt VCF failus.",
  "linktitle": "VCF",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-vc-lvf"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir VCF fails?

VCF (virtuālās kartes formāts) vai vCard ir digitālā faila formāts kontaktinformācijas glabāšanai. Formāts tiek plaši izmantots datu apmaiņai starp populārām informācijas apmaiņas lietojumprogrammām. Lielākajai daļai operētājsistēmu, piemēram, Windows un MacOS, ir noklusējuma lietojumprogrammas, lai izveidotu un atvērtu šos failus. Vienā VCF failā var būt viena vai vairāku kontaktpersonu kontaktinformācija. VCF fails parasti satur informāciju, piemēram, kontaktpersonas vārdu, adresi, tālruņa numuru, e-pastu, dzimšanas dienu, fotogrāfijas un audio papildus vairākiem citiem laukiem. Tā kā to atbalsta e-pasta klienti un pakalpojumi, kontaktu pārsūtīšanas laikā, izmantojot vCard formātu, netiek zaudēti dati. VCF faila formāta multivides veids ir teksts/vcard.

## VCF faila formāts

VCF faili pēc būtības ir tekstuāli un ir lasāmi cilvēkiem. Tos var atvērt teksta redaktoros, piemēram, Notepad operētājsistēmā Microsoft Windows un TextEdit operētājsistēmā MacOS. Tomēr, ja failā ir attēls, tas netiks rādīts teksta redaktorā.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) nodrošina atbalstu VCF failu atvēršanai, kā arī konvertēšanai uz vairākiem citiem formātiem, piemēram, populāro [MSG](/email/msg/) formātu. Laika gaitā no 2.1 līdz 4.0 uzlabots VCF faila formāts, faila formātam pievienojot detalizētu informāciju. Formāts tiek izmantots arī tālruņa kontaktu eksportēšanai un vēlākai importēšanai citā ierīcē.

{{< figure src="../VCF.png" alt="VCF faila formāts" >}}

### VCF 2.1 piemērs

Tālāk ir sniegts versijas 2.1 piemērs.

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

### VCF 3.0 piemērs

Tālāk ir sniegts versijas 3.0 piemērs.

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

### VCF 4.0 piemērs

Tālāk ir sniegts versijas 4.0 piemērs.

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

## Atsauces

* [VCF — Wikipedia](https://en.wikipedia.org/wiki/VCard)


