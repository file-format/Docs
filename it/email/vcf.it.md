{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - File di contatto virtuale",
  "description":"Scopri il formato di file VCF e le API che possono creare e aprire file VCF.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file VCF?

VCF (Virtual Card Format) o vCard è un formato di file digitale per la memorizzazione delle informazioni di contatto. Il formato è ampiamente utilizzato per lo scambio di dati tra le applicazioni di scambio di informazioni più diffuse. La maggior parte dei sistemi operativi come Windows e MacOS sono dotati di applicazioni predefinite per creare e aprire questi file. Un singolo file VCF può contenere informazioni di contatto per uno o più contatti. Un file VCF di solito contiene informazioni come nome del contatto, indirizzo, numero di telefono, e-mail, compleanno, fotografie e audio oltre a una serie di altri campi. Essendo supportato da client e servizi di posta elettronica, non vi è alcuna perdita di dati durante il trasferimento dei contatti tramite l'utilizzo del formato vCard. Il tipo di supporto per il formato file VCF è text/vcard.

## Formato file VCF

I file VCF sono di natura testuale e sono leggibili dall'uomo. Questi possono essere aperti in editor di testo come Blocco note su Microsoft Windows e TextEdit su MacOS. Se nel file è presente un'immagine, tuttavia, non verrà visualizzata nell'editor di testo.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) fornisce supporto per l'apertura di file VCF e la conversione in numerosi altri formati come il popolare formato [MSG](/it/email/msg/). Formato file VCF migliorato con il tempo dalla versione 2.1 alla 4.0 aggiungendo informazioni dettagliate al formato file. Il formato viene utilizzato anche per esportare i contatti telefonici e successivamente importarli in un altro dispositivo.

{{< figure src="../VCF.png" alt="Formato file VCF" >}}

### VCF 2.1 Esempio

Di seguito è riportato un esempio della versione 2.1.

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

### Esempio VCF 3.0

Di seguito è riportato un esempio della versione 3.0.

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

### Esempio VCF 4.0

Di seguito è riportato un esempio della versione 4.0.

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

## Riferimenti

* [VCF - Di Wikipedia](https://en.wikipedia.org/wiki/VCard)

