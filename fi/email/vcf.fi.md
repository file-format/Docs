{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VCF - Virtuaalinen yhteystietotiedosto",
  "description": "Opi VCF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata VCF-tiedostoja.",
  "linktitle": "VCF",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-vc-fif"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on VCF-tiedosto?

VCF (Virtual Card Format) tai vCard on digitaalinen tiedostomuoto yhteystietojen tallentamiseen. Muotoa käytetään laajasti tiedonvaihtoon suosittujen tiedonvaihtosovellusten keskuudessa. Useimmissa käyttöjärjestelmissä, kuten Windowsissa ja MacOS:ssa, on oletussovellukset näiden tiedostojen luomiseen ja avaamiseen. Yksi VCF-tiedosto voi sisältää yhden tai useamman yhteyshenkilön yhteystiedot. VCF-tiedosto sisältää yleensä tietoja, kuten yhteyshenkilön nimen, osoitteen, puhelinnumeron, sähköpostin, syntymäpäivän, valokuvat ja äänen useiden muiden kenttien lisäksi. Sähköpostiohjelmien ja -palveluiden tukemana tietoja ei menetetä, kun yhteystietoja siirretään vCard-muodossa. VCF-tiedostomuodon mediatyyppi on text/vcard.

## VCF tiedostomuoto

VCF-tiedostot ovat luonteeltaan tekstimuotoisia ja ihmisen luettavissa. Ne voidaan avata tekstieditoreissa, kuten Microsoft Windowsissa Notepadissa ja MacOS:n TextEditissä. Jos tiedostossa on kuva, se ei kuitenkaan näy tekstieditorissa.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) tukee VCF-tiedostojen avaamista sekä muuntamista useisiin muihin muotoihin, kuten suosittuun [MSG](/email/msg/)-muotoon. VCF-tiedostomuotoa parannettu ajan myötä versiosta 2.1 versioon 4.0 lisäämällä tiedostomuotoon yksityiskohtaisia tietoja. Muotoa käytetään myös puhelimen yhteystietojen viemiseen ja myöhemmin tuontiin toiseen laitteeseen.

{{< figure src="../VCF.png" alt="VCF-tiedostomuoto" >}}

### VCF 2.1 Esimerkki

Seuraavassa on esimerkki versiosta 2.1.

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

### VCF 3.0 Esimerkki

Seuraavassa on esimerkki versiosta 3.0.

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

### VCF 4.0 Esimerkki

Seuraavassa on esimerkki versiosta 4.0.

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

## Viitteet

* [VCF – Wikipedia](https://en.wikipedia.org/wiki/VCard)


