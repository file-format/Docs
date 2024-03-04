{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VCF – virtualus kontaktų failas",
  "description": "Sužinokite apie VCF failo formatą ir API, kurios gali kurti ir atidaryti VCF failus.",
  "linktitle": "VCF",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-vc-ltf"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra VCF failas?

VCF (Virtual Card Format) arba vCard yra skaitmeninis failo formatas, skirtas kontaktinei informacijai saugoti. Formatas yra plačiai naudojamas duomenų mainams tarp populiarių informacijos mainų programų. Daugumoje operacinių sistemų, tokių kaip Windows ir MacOS, yra numatytos programos, skirtos šiems failams kurti ir atidaryti. Viename VCF faile gali būti vieno ar kelių kontaktų kontaktinė informacija. VCF faile, be daugelio kitų laukų, paprastai yra tokia informacija kaip kontakto vardas, adresas, telefono numeris, el. pašto adresas, gimtadienis, nuotraukos ir garso įrašas. El. pašto klientų ir paslaugų palaikomi duomenys neprarandami perduodant kontaktus naudojant vCard formatą. VCF failo formato laikmenos tipas yra tekstas / vaizdo kortelė.

## VCF failo formatas

VCF failai iš prigimties yra tekstiniai ir yra skaitomi žmonėms. Juos galima atidaryti teksto rengyklėse, pvz., Notepad sistemoje Microsoft Windows ir TextEdit sistemoje MacOS. Tačiau jei faile yra vaizdas, jis nebus rodomas teksto rengyklėje.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) palaiko VCF failų atidarymą ir konvertavimą į daugybę kitų formatų, pvz., populiarų [MSG](/email/msg/) formatą. Laikui bėgant nuo 2.1 iki 4.0 patobulintas VCF failo formatas, pridedant išsamią informaciją prie failo formato. Formatas taip pat naudojamas telefono kontaktams eksportuoti ir vėliau importuoti į kitą įrenginį.

{{< figure src="../VCF.png" alt="VCF failo formatas" >}}

### VCF 2.1 pavyzdys

Toliau pateikiamas 2.1 versijos pavyzdys.

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

### VCF 3.0 pavyzdys

Toliau pateikiamas 3.0 versijos pavyzdys.

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

### VCF 4.0 pavyzdys

Toliau pateikiamas 4.0 versijos pavyzdys.

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

## Nuorodos

* [VCF – Vikipedija](https://en.wikipedia.org/wiki/VCard)


