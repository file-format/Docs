{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - Virtuális névjegyfájl",
  "description":"További információ a VCF fájlformátumról és az API-król, amelyek VCF-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a VCF fájl?

A VCF (virtuális kártyaformátum) vagy a vCard egy digitális fájlformátum a kapcsolattartási adatok tárolására. A formátumot széles körben használják adatcserére a népszerű információcsere-alkalmazások között. A legtöbb operációs rendszer, például a Windows és a MacOS, alapértelmezett alkalmazásokkal rendelkezik a fájlok létrehozásához és megnyitásához. Egyetlen VCF-fájl egy vagy több névjegy kapcsolati adatait tartalmazhatja. A VCF-fájlok általában olyan információkat tartalmaznak, mint a kapcsolattartó neve, címe, telefonszáma, e-mail címe, születésnapja, fényképek és hangok számos egyéb mező mellett. Mivel az e-mail kliensek és szolgáltatások támogatják, nincs adatvesztés a névjegyek átvitele során a vCard formátum használatával. A VCF fájlformátum médiatípusa text/vcard.

## VCF fájl formátum

A VCF fájlok természetüknél fogva szövegesek, és ember által is olvashatók. Ezeket olyan szövegszerkesztőkkel lehet megnyitni, mint a Notepad Microsoft Windows rendszeren és TextEdit MacOS rendszeren. Ha azonban van kép a fájlban, az nem jelenik meg a szövegszerkesztőben.

A [Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) támogatja megnyithatja a VCF fájlokat, valamint számos más formátumba konvertálhat, például a népszerű [MSG](/hu/email/msg/) formátumba. A 2.1-es verziótól a 4.0-s verzióig idővel továbbfejlesztett VCF fájlformátum, amely részletes információkat ad a fájlformátumhoz. A formátum a telefonos névjegyek exportálására és későbbi importálására is használható egy másik eszközre.

{{< figure src="../VCF.png" alt="VCF fájl formátum" >}}

### VCF 2.1 Példa

Az alábbiakban egy példa a 2.1-es verzióra.

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

### VCF 3.0 példa

Az alábbiakban egy példa a 3.0-s verzióra.

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

### VCF 4.0 példa

Az alábbiakban egy példa a 4.0-s verzióra.

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

## Hivatkozások

* [VCF – a Wikipedia által](https://en.wikipedia.org/wiki/VCard)

