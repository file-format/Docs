{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - файл виртуального контакта",
  "description":"Узнайте о формате файла VCF и API-интерфейсах, которые могут создавать и открывать файлы VCF.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .VCF вариант №

VCF (формат виртуальной карты) или vCard — это цифровой формат файла для хранения контактной информации. Формат широко используется для обмена данными между популярными приложениями обмена информацией. Большинство операционных систем, таких как Windows и MacOS, поставляются с приложениями по умолчанию для создания и открытия этих файлов. Один файл VCF может содержать контактную информацию для одного или нескольких контактов. Файл VCF обычно содержит такую информацию, как имя контакта, адрес, номер телефона, адрес электронной почты, день рождения, фотографии и аудио, а также ряд других полей. Благодаря поддержке почтовых клиентов и сервисов при передаче контактов через формат vCard не происходит потери данных. Тип носителя для формата файла VCF — text/vcard.

## Формат файла VCF

Файлы VCF являются текстовыми по своей природе и удобочитаемы для человека. Их можно открыть в текстовых редакторах, таких как «Блокнот» в Microsoft Windows и TextEdit в MacOS. Однако если в файле есть изображение, оно не будет отображаться в текстовом редакторе.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) обеспечивает поддержку открытие файлов VCF, а также преобразование в ряд других форматов, таких как популярный формат [MSG](/ru/email/msg/). Формат файла VCF, улучшенный со временем с версии 2.1 до 4.0, с добавлением подробной информации в формат файла. Формат также используется для экспорта телефонных контактов и последующего импорта на другое устройство.

{{< figure src="../VCF.png" alt="Формат файла VCF" >}}

### Пример VCF 2.1

Ниже приведен пример версии 2.1.

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

### Пример VCF 3.0

Ниже приведен пример версии 3.0.

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

### Пример VCF 4.0

Ниже приведен пример версии 4.0.

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

## использованная литература

* [VCF — Википедия](https://en.wikipedia.org/wiki/VCard)

