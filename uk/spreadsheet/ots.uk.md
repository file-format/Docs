{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "файл", "розширення", "формат файлу", "Excel", "Електронна таблиця" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу OTS та API, які можуть створювати та відкривати файли OTS.",
  "title" :"OTS - формат файлу шаблону електронної таблиці OpenDocument",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## Що таке файл OTS?

Файл із розширенням .ots — це файл шаблону електронної таблиці OpenDocument, створений за допомогою програмного забезпечення Calc, що входить до складу Apache OpenOffice. Прикладне програмне забезпечення Calc схоже на Excel, доступне в Microsoft Office. Формат файлу OTS використовується для створення шаблонів, які містять попередньо визначені налаштування, пов’язані зі стилями, шрифтом, даними, макетом електронної таблиці та форматуванням. Файли OTF мають `mime-type application/vnd.oasis.opendocument.spreadsheet-template`. Ці файли шаблонів можна використовувати як відправну точку для створення та збереження фактичних файлів даних, які зберігаються у [форматі файлу ODS](/uk/spreadsheet/ods/). Файли OTS можна використовувати з такими програмами, як OpenOffice і LibreOffice.

## Формат файлу OTS

Файли OTS зберігаються у форматі OASIS OpenDocument на основі XML, який складається з колекції кількох піддокументів із пакетом у вигляді архіву [ZIP](/uk/compression/zip/). Кожен zip-архів зберігає частину повного документа, а кожен піддокумент зберігає певний аспект документа. Наприклад, один піддокумент містить інформацію про стиль, а інший піддокумент містить вміст документа. Типовий документ ODF містить такі компоненти:

### OTS Content.xml

Файл content.xml містить фактичний вміст документа. Однак це не включає двійкові дані, такі як зображення.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml формату файлу OTS

Файл styles.xml містить інформацію про стиль і широко використовується для форматування та макета. Типи стилів включають:

* Стилі абзаців
* Стилі сторінок
* Стилі персонажів
* Стилі рамки
* Список стилів

### Meta.xml

Файл meta.xml містить інформацію про метадані файлу, як-от автор, дата останньої зміни тощо.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

Файл `settings.xml` містить параметри рівня документа, такі як коефіцієнт масштабування та положення курсору.

## Посилання ##

* [Специфікація OpenDocument 1.2](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - Вікіпедія](https://en.wikipedia.org/wiki/OpenDocument)

