{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "файл", "расширение", "формат файла", "Excel", "электронная таблица" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файла OTS и API-интерфейсах, которые могут создавать и открывать файлы OTS.",
  "title" :"OTS — формат файла шаблона электронной таблицы OpenDocument",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## .OTS вариант №

Файл с расширением .ots представляет собой файл шаблона электронной таблицы OpenDocument, созданный с помощью прикладного программного обеспечения Calc, входящего в состав Apache OpenOffice. Программное обеспечение Calc аналогично Excel, доступному в Microsoft Office. Формат файла OTS используется для создания шаблонов, содержащих предопределенные параметры, связанные со стилями, шрифтом, данными, макетом электронной таблицы и форматированием. Файлы OTF имеют `приложение типа mime/vnd.oasis.opendocument.spreadsheet-template`. Эти файлы шаблонов можно использовать в качестве отправной точки для создания и сохранения файлов фактических данных, которые сохраняются в [формат файла ODS](/ru/spreadsheet/ods/). Файлы OTS можно использовать с такими приложениями, как OpenOffice и LibreOffice.

## Формат файла OTS

Файлы OTS сохраняются в формате файла OASIS OpenDocument на основе XML, который состоит из набора нескольких вложенных документов с пакетом в виде архива [ZIP](/ru/compression/zip/). Каждый zip-архив хранит часть полного документа, а каждый вложенный документ хранит определенный аспект документа. Например, один вложенный документ содержит информацию о стиле, а другой вложенный документ содержит содержимое документа. Типичный документ ODF состоит из следующих компонентов:

### OTS Content.xml

Файл content.xml содержит фактическое содержимое документа. Однако это не включает двоичные данные, такие как изображения.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml формата файла OTS

Файл styles.xml содержит информацию о стилях и активно используется для форматирования и компоновки. Типы стилей включают в себя:

* Стили абзаца
* Стили страницы
* Стили персонажей
* Стили рамок
* Стили списка

### Мета.xml

Файл meta.xml содержит информацию о метаданных файла, таких как автор, дата последнего изменения и т. д.
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
### Настройки.xml

Файл `settings.xml` содержит настройки уровня документа, такие как коэффициент масштабирования и положение курсора.

## Использованная литература ##

* [Спецификация OpenDocument 1.2] (https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument — Википедия] (https://en.wikipedia.org/wiki/OpenDocument)

