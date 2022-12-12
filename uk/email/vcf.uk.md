{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - файл віртуальних контактів",
  "description":"Дізнайтеся про формат файлу VCF та API, які можуть створювати та відкривати файли VCF.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл VCF?

VCF (Формат віртуальної картки) або vCard — це цифровий формат файлу для зберігання контактної інформації. Формат широко використовується для обміну даними серед популярних програм обміну інформацією. Більшість операційних систем, таких як Windows і MacOS, мають стандартні програми для створення та відкриття цих файлів. Один файл VCF може містити контактну інформацію для одного або кількох контактів. Файл VCF зазвичай містить таку інформацію, як ім’я контакта, адреса, номер телефону, адреса електронної пошти, день народження, фотографії та аудіо на додаток до ряду інших полів. Завдяки підтримці поштових клієнтів і служб немає втрати даних під час передачі контактів у форматі vCard. Тип медіа для формату файлу VCF – текст/vcard.

## Формат файлу VCF

Файли VCF є текстовими за своєю природою і їх читає людина. Їх можна відкрити в текстових редакторах, таких як Блокнот у Microsoft Windows і TextEdit у MacOS. Однак якщо у файлі є зображення, воно не відображатиметься в текстовому редакторі.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) надає підтримку для відкривати файли VCF, а також конвертувати в низку інших форматів, наприклад популярний формат [MSG](/uk/email/msg/). Формат файлу VCF покращено з версією 2.1 до 4.0, додавши детальну інформацію до формату файлу. Формат також використовується для експорту телефонних контактів і подальшого імпорту на інший пристрій.

{{< figure src="../VCF.png" alt="Формат файлу VCF" >}}

### Приклад VCF 2.1

Нижче наведено приклад версії 2.1.

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

### Приклад VCF 3.0

Нижче наведено приклад версії 3.0.

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

### Приклад VCF 4.0

Нижче наведено приклад версії 4.0.

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

## Список літератури

* [VCF - Вікіпедія](https://en.wikipedia.org/wiki/VCard)

