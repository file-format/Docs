{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - Виртуален файл с контакти",
  "description":"Научете за файловия формат VCF и API, които могат да създават и отварят VCF файлове.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е VCF файл?

VCF (Формат на виртуална карта) или vCard е цифров файлов формат за съхраняване на информация за контакт. Форматът се използва широко за обмен на данни сред популярни приложения за обмен на информация. Повечето операционни системи като Windows и MacOS идват с приложения по подразбиране за създаване и отваряне на тези файлове. Един VCF файл може да съдържа информация за контакт за един или няколко контакта. VCF файлът обикновено съдържа информация като име на контакт, адрес, телефонен номер, имейл, рожден ден, снимки и аудио в допълнение към редица други полета. Тъй като се поддържа от имейл клиенти и услуги, няма загуба на данни по време на прехвърляне на контакти чрез използване на vCard формат. Типът медия за VCF файлов формат е текст/vcard.

## VCF файлов формат

VCF файловете са текстови по природа и са четими от хора. Те могат да се отварят в текстови редактори като Notepad в Microsoft Windows и TextEdit в MacOS. Ако обаче във файла има изображение, то няма да се покаже в текстовия редактор.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) осигурява поддръжка за отваряне на VCF файлове, както и конвертиране в редица други формати като популярния формат [MSG](/bg/email/msg/). VCF файлов формат, подобрен с времето от версия 2.1 до 4.0, добавяйки подробна информация към файловия формат. Форматът се използва и за експортиране на телефонни контакти и по-късно импортиране в друго устройство.

{{< figure src="../VCF.png" alt="VCF файлов формат" >}}

### Пример за VCF 2.1

Следва пример за версия 2.1.

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

### Пример за VCF 3.0

Следва пример за версия 3.0.

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

### Пример за VCF 4.0

Следва пример за версия 4.0.

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

## Препратки

* [VCF - от Wikipedia](https://en.wikipedia.org/wiki/VCard)

