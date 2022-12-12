{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - soubor virtuálního kontaktu",
  "description":"Další informace o formátu souborů VCF a rozhraních API, která mohou vytvářet a otevírat soubory VCF.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor VCF?

VCF (Virtual Card Format) nebo vCard je digitální formát souborů pro ukládání kontaktních informací. Tento formát je široce používán pro výměnu dat mezi populárními aplikacemi pro výměnu informací. Většina operačních systémů, jako jsou Windows a MacOS, se dodává s výchozími aplikacemi pro vytváření a otevírání těchto souborů. Jeden soubor VCF může obsahovat kontaktní informace pro jeden nebo více kontaktů. Soubor VCF obvykle kromě řady dalších polí obsahuje informace, jako je jméno kontaktu, adresa, telefonní číslo, e-mail, narozeniny, fotografie a zvuk. Díky podpoře e-mailových klientů a služeb nedochází ke ztrátě dat při přenosu kontaktů pomocí formátu vCard. Typ média pro formát souboru VCF je text/vcard.

## Formát souboru VCF

Soubory VCF jsou svou povahou textové a jsou čitelné pro člověka. Ty lze otevřít v textových editorech, jako je Poznámkový blok v systému Microsoft Windows a TextEdit v systému MacOS. Pokud je však v souboru obrázek, v textovém editoru se nezobrazí.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) poskytuje podporu pro otevírání souborů VCF a také převod do řady dalších formátů, jako je populární formát [MSG](/cs/email/msg/). Formát souboru VCF vylepšený časem od verze 2.1 do 4.0 přidáním podrobných informací o formátu souboru. Formát se také používá pro export telefonních kontaktů a pozdější import do jiného zařízení.

{{< figure src="../VCF.png" alt="Formát souboru VCF" >}}

### Příklad VCF 2.1

Následuje příklad verze 2.1.

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

### Příklad VCF 3.0

Následuje příklad verze 3.0.

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

### Příklad VCF 4.0

Následuje příklad verze 4.0.

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

## Reference

* [VCF – z Wikipedie](https://en.wikipedia.org/wiki/VCard)

