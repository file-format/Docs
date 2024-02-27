{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VCF - Virtuel kontaktfil",
  "description": "Lær om VCF-filformat og API'er, der kan oprette og åbne VCF-filer.",
  "linktitle": "VCF",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-vc-daf"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en VCF fil?

VCF (Virtual Card Format) eller vCard er et digitalt filformat til lagring af kontaktoplysninger. Formatet er meget udbredt til dataudveksling blandt populære informationsudvekslingsapplikationer. De fleste operativsystemer såsom Windows og MacOS leveres med standardprogrammer til at oprette og åbne disse filer. En enkelt VCF-fil kan indeholde kontaktoplysninger for en eller flere kontakter. En VCF-fil indeholder normalt oplysninger som kontaktpersonens navn, adresse, telefonnummer, e-mail, fødselsdag, fotografier og lyd ud over en række andre felter. Da det er understøttet af e-mail-klienter og -tjenester, er der intet tab af data under overførslen af kontakter via vCard-formatet. Medietypen for VCF-filformatet er tekst/vcard.

## VCF filformat

VCF-filer er tekstlige af natur og kan læses af mennesker. Disse kan åbnes i teksteditorer som Notepad på Microsoft Windows og TextEdit på MacOS. Hvis der er et billede i filen, vil det dog ikke blive vist i teksteditoren.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) understøtter åbning af VCF-filer samt konverterer til en række andre formater såsom det populære [MSG](/email/msg/)-format. VCF-filformat forbedret med tiden fra version 2.1 til 4.0 og tilføjer detaljerede oplysninger til filformatet. Formatet bruges også til at eksportere telefonkontakter og senere importere til en anden enhed.

{{< figure src="../VCF.png" alt="VCF filformat" >}}

### VCF 2.1 Eksempel

Følgende er et eksempel på version 2.1.

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

### VCF 3.0 Eksempel

Følgende er et eksempel på version 3.0.

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

### VCF 4.0 Eksempel

Følgende er et eksempel på version 4.0.

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

## Referencer

* [VCF - Af Wikipedia](https://en.wikipedia.org/wiki/VCard)


