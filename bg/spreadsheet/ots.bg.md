{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "файл", "разширение", "файлов формат", "Excel", "Електронна таблица" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за OTS файловия формат и API, които могат да създават и отварят OTS файлове.",
  "title" :"OTS – Файлов формат за шаблон на електронна таблица OpenDocument",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## Какво е OTS файл?

Файл с разширение .ots е файл с шаблон на електронна таблица OpenDocument, който е създаден с приложния софтуер Calc, включен в Apache OpenOffice. Приложният софтуер Calc е подобен на Excel, наличен в Microsoft Office. Файловият формат OTS се използва за създаване на шаблони, които съдържат предварително зададени настройки, свързани със стилове, шрифт, данни, оформление на електронна таблица и форматиране. OTF файловете имат `mime-type application/vnd.oasis.opendocument.spreadsheet-template`. Тези шаблонни файлове могат да се използват като отправна точка за генериране и запазване на действителни файлове с данни, които се записват във [файлов формат ODS](/bg/spreadsheet/ods/). OTS файловете могат да се използват с приложения като OpenOffice и LibreOffice.

## OTS файлов формат

OTS файловете се записват в OpenDocument XML-базиран файлов формат на OASIS, който се състои от колекция от няколко поддокумента с пакет като [ZIP](/bg/compression/zip/) архив. Всеки zip архив съхранява част от пълния документ, а всеки поддокумент съхранява конкретен аспект на документа. Например един поддокумент съдържа информация за стила, а друг поддокумент съдържа съдържанието на документа. Типичен ODF документ има следните компоненти:

### OTS Content.xml

Файлът content.xml съдържа действителното съдържание на документа. Това обаче не включва двоични данни като изображения.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml на OTS файлов формат

Файлът styles.xml съдържа информация за стил и се използва широко за форматиране и оформление. Типовете стилове включват:

* Стилове на абзаци
* Стилове на страници
* Стилове на герои
* Стилове на рамки
* Списък на стилове

### Meta.xml

Файлът meta.xml съдържа информация за метаданните на файла като автор, дата на последна промяна и др.
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

Файлът „settings.xml“ включва настройки на ниво документ, като фактор на мащабиране и позиция на курсора.

## Препратки ##

* [Спецификация на OpenDocument 1.2](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument – от Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

