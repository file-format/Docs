{
  "date" : "2019-10-11",
  "keywords" :[ "fodg файл", "fodg файлов формат", "какво е fodg файл", "файл", "fodg пример", "fodg файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - OpenDocument чертожен файлов формат",
  "description":"Научете за файловия формат FODG и API, които могат да създават и отварят FODG файлове.",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е FODG файл?

Файл с разширение .fodg е файлов формат за рисуване на Apache OpenOffice за съхраняване на чертожни елементи. Той се основава на спецификациите на файловия формат, очертани от Усъвършенстването на стандартите за структурна информация (OASIS). Друг подобен файлов формат за OpenOffice графики е [ODG](/bg/image/odg/), който съхранява чертожни елементи като векторно изображение. FODG файловете могат да се отварят с OpenOffice, както и с LibreOffice. Други файлови формати, поддържани от OpenOffice, например, включват [ODT](/bg/word-processing/odt/), ODF, [ODP](/bg/presentation/odp/) и [ODS](/bg/spreadsheet/ods/).

## FODG файлов формат

FODG се основава на XML файловия формат на OpenDocument, който отговаря на OASIS OpenDocument Format ISO/IEC 26300. Има тип интернет носител application/vnd.oasis.opendocument.graphics и също така отговаря на org.oasis-open.opendocument public.composite-content . XML структурата е обща за всички типове документи като електронни таблици, чертожни файлове и текстови документи. Документите на OpenOffice се възползват от разделянето на проблемите, като разделят съдържанието, стиловете, метаданните и настройките на приложението в четири отделни XML файла.

`<office:document-content>` - Съдържание на документа и автоматични стилове, използвани в съдържанието.
`<office:document-styles>` - Стилове, използвани в съдържанието на документа и автоматични стилове, използвани в самите стилове.
`<office:document-meta>` - Мета информация на документа, като например автор или час на последното действие за запис.
`<office:document-settings>` - Специфични за приложението настройки, като размер на прозореца или информация за принтера.

## Препратки ##
* [Бъдещи спецификации за стандартизация v. 1.3](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [Отворен формат на документи на OASIS за офис приложения](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Формат OpenDocument – Уикипедия](https://en.wikipedia.org/wiki/OpenDocument)

