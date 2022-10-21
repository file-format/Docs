{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - Virtuelle Kontaktdatei",
  "description":"Erfahren Sie mehr über das VCF-Dateiformat und APIs, die VCF-Dateien erstellen und öffnen können.",
  "linktitle" :"VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine VCF-Datei?

VCF (Virtual Card Format) oder vCard ist ein digitales Dateiformat zum Speichern von Kontaktinformationen. Das Format wird häufig für den Datenaustausch zwischen gängigen Informationsaustauschanwendungen verwendet. Die meisten Betriebssysteme wie Windows und MacOS werden mit Standardanwendungen zum Erstellen und Öffnen dieser Dateien geliefert. Eine einzelne VCF-Datei kann Kontaktinformationen für einen oder mehrere Kontakte enthalten. Eine VCF-Datei enthält neben einer Reihe anderer Felder normalerweise Informationen wie Name, Adresse, Telefonnummer, E-Mail-Adresse, Geburtstag, Fotos und Audio des Kontakts. Durch die Unterstützung von E-Mail-Clients und -Diensten kommt es bei der Übertragung von Kontakten über das vCard-Format zu keinem Datenverlust. Der Medientyp für das VCF-Dateiformat ist Text/vcard.

## VCF-Dateiformat

VCF-Dateien sind von Natur aus textuell und für Menschen lesbar. Diese können in Texteditoren wie Notepad unter Microsoft Windows und TextEdit unter MacOS geöffnet werden. Wenn die Datei jedoch ein Bild enthält, wird es im Texteditor nicht angezeigt.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) bietet Unterstützung für Öffnen von VCF-Dateien sowie Konvertieren in eine Reihe anderer Formate wie das beliebte [MSG](/de/email/msg/)-Format. Das VCF-Dateiformat wurde mit der Zeit von Version 2.1 bis 4.0 verbessert, indem detaillierte Informationen zum Dateiformat hinzugefügt wurden. Das Format wird auch verwendet, um Telefonkontakte zu exportieren und später in ein anderes Gerät zu importieren.

{{< figure src="../VCF.png" alt="VCF-Dateiformat" >}}

### VCF 2.1-Beispiel

Nachfolgend ein Beispiel für Version 2.1.

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

### VCF 3.0-Beispiel

Es folgt ein Beispiel für Version 3.0.

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

### VCF 4.0-Beispiel

Es folgt ein Beispiel für Version 4.0.

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

## Verweise

* [VCF – von Wikipedia](https://en.wikipedia.org/wiki/VCard)

