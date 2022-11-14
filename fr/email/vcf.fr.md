{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - Fichier de contact virtuel",
  "description":"En savoir plus sur le format de fichier VCF et les API qui peuvent créer et ouvrir des fichiers VCF.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier VCF ?

VCF (Virtual Card Format) ou vCard est un format de fichier numérique pour stocker les informations de contact. Le format est largement utilisé pour l'échange de données entre les applications d'échange d'informations populaires. La plupart des systèmes d'exploitation tels que Windows et MacOS sont livrés avec des applications par défaut pour créer et ouvrir ces fichiers. Un seul fichier VCF peut contenir des informations de contact pour un ou plusieurs contacts. Un fichier VCF contient généralement des informations telles que le nom, l'adresse, le numéro de téléphone, l'e-mail, l'anniversaire, les photos et l'audio du contact, en plus d'un certain nombre d'autres champs. Étant pris en charge par les clients et services de messagerie, il n'y a aucune perte de données lors du transfert de contacts via l'utilisation du format vCard. Le type de média pour le format de fichier VCF est text/vcard.

## Format de fichier VCF

Les fichiers VCF sont textuels par nature et sont lisibles par l'homme. Ceux-ci peuvent être ouverts dans des éditeurs de texte tels que le Bloc-notes sur Microsoft Windows et TextEdit sur MacOS. S'il y a une image dans le fichier, cependant, elle ne s'affichera pas dans l'éditeur de texte.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) prend en charge l'ouverture de fichiers VCF ainsi que la conversion vers un certain nombre d'autres formats tels que le format populaire [MSG](/fr/email/msg/). Format de fichier VCF amélioré avec le temps de la version 2.1 à 4.0 en ajoutant des informations détaillées au format de fichier. Le format est également utilisé pour exporter des contacts téléphoniques et les importer ultérieurement dans un autre appareil.

{{< figure src="../VCF.png" alt="Format de fichier VCF" >}}

### VCF 2.1 Exemple

Voici un exemple de la version 2.1.

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

### Exemple VCF 3.0

Voici un exemple de la version 3.0.

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

### Exemple VCF 4.0

Voici un exemple de la version 4.0.

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

## Références

* [VCF - Par Wikipédia](https://en.wikipedia.org/wiki/VCard)

