{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF – Fișier de contact virtual",
  "description":"Aflați despre formatul de fișier VCF și despre API-urile care pot crea și deschide fișiere VCF.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier VCF?

VCF (Virtual Card Format) sau vCard este un format de fișier digital pentru stocarea informațiilor de contact. Formatul este utilizat pe scară largă pentru schimbul de date între aplicațiile populare de schimb de informații. Majoritatea sistemelor de operare, cum ar fi Windows și MacOS, vin cu aplicații implicite pentru a crea și deschide aceste fișiere. Un singur fișier VCF poate conține informații de contact pentru unul sau mai multe persoane de contact. Un fișier VCF conține, de obicei, informații precum numele contactului, adresa, numărul de telefon, e-mailul, ziua de naștere, fotografii și sunet, în plus față de o serie de alte câmpuri. Fiind acceptat de clienții și serviciile de e-mail, nu există pierderi de date în timpul transferului de contacte prin utilizarea formatului vCard. Tipul media pentru formatul de fișier VCF este text/vcard.

## Format de fișier VCF

Fișierele VCF sunt textuale prin natura lor și pot fi citite de om. Acestea pot fi deschise în editori de text, cum ar fi Notepad pe Microsoft Windows și TextEdit pe MacOS. Dacă există o imagine în fișier, totuși, aceasta nu se va afișa în editorul de text.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) oferă suport pentru deschiderea fișierelor VCF, precum și convertirea într-un număr de alte formate, cum ar fi popularul format [MSG](/ro/email/msg/). Format de fișier VCF îmbunătățit cu timpul de la versiunea 2.1 la 4.0, adăugând informații detaliate la formatul de fișier. Formatul este, de asemenea, folosit pentru a exporta contactele de pe telefon și, ulterior, pentru a importa pe alt dispozitiv.

{{< figure src="../VCF.png" alt="Format de fișier VCF" >}}

### Exemplu VCF 2.1

Mai jos este un exemplu al versiunii 2.1.

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

### Exemplu VCF 3.0

Urmează un exemplu de versiune 3.0.

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

### Exemplu VCF 4.0

Mai jos este un exemplu de versiune 4.0.

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

## Referințe

* [VCF - După Wikipedia](https://en.wikipedia.org/wiki/VCard)

