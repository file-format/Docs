{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - Virtueel contactbestand",
  "description":"Meer informatie over VCF-bestandsindelingen en API's die VCF-bestanden kunnen maken en openen.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een VCF-bestand?

VCF (Virtual Card Format) of vCard is een digitaal bestandsformaat voor het opslaan van contactgegevens. Het formaat wordt veel gebruikt voor gegevensuitwisseling tussen populaire toepassingen voor informatie-uitwisseling. De meeste besturingssystemen, zoals Windows en MacOS, worden geleverd met standaardtoepassingen om deze bestanden te maken en te openen. Een enkel VCF-bestand kan contactgegevens voor een of meerdere contacten bevatten. Een VCF-bestand bevat meestal informatie zoals de naam, het adres, het telefoonnummer, de e-mail, de verjaardag, foto's en audio van de contactpersoon, naast een aantal andere velden. Omdat het wordt ondersteund door e-mailclients en -services, gaat er geen gegevens verloren tijdens de overdracht van contacten via het vCard-formaat. Het mediatype voor het VCF-bestandsformaat is tekst/vcard.

## VCF-bestandsindeling

VCF-bestanden zijn van nature tekstueel en leesbaar voor mensen. Deze kunnen worden geopend in teksteditors zoals Kladblok op Microsoft Windows en TextEdit op MacOS. Als het bestand echter een afbeelding bevat, wordt deze niet weergegeven in de teksteditor.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) biedt ondersteuning voor het openen van VCF-bestanden en het converteren naar een aantal andere formaten zoals het populaire [MSG](/nl/email/msg/) formaat. VCF-bestandsformaat verbeterd met de tijd van versie 2.1 naar 4.0 en voegt gedetailleerde informatie toe aan het bestandsformaat. Het formaat wordt ook gebruikt om telefooncontacten te exporteren en later te importeren in een ander apparaat.

{{< figure src="../VCF.png" alt="VCF-bestandsindeling" >}}

### VCF 2.1 Voorbeeld

Hieronder volgt een voorbeeld van versie 2.1.

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

### VCF 3.0 Voorbeeld

Hieronder ziet u een voorbeeld van versie 3.0.

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

### VCF 4.0 Voorbeeld

Hieronder volgt een voorbeeld van versie 4.0.

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

## Referenties

* [VCF - Door Wikipedia](https://en.wikipedia.org/wiki/VCard)

