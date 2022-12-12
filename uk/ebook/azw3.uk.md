{
  "date" : "2019-12-12",
  "keywords" :[ "KF8", "розширення", "файл", "формат", "електронна книга", "Формат файлу Kindle", "Структура файлу AZW3" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу AZW3 та API, які можуть створювати та відкривати файли AZW3.",
  "title" :"Що таке файл AZW3?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## Що таке файл AZW3?

AZW3, також відомий як Kindle Format 8 (**KF8**), є модифікованою версією цифрового файлу електронної книги [AZW](/uk/ebook/azw/), розробленого для пристроїв Amazon Kindle. Цей формат є вдосконаленням старіших файлів AZW і використовується на пристроях Kindle Fire лише із зворотною сумісністю для попереднього формату файлу, тобто [MOBI](/uk/ebook/mobi/) і AZW. Amazon представив формат KFX (KF версія 10) після KF8, який використовується на останніх пристроях Kindle. Файли AZW3 мають тип Інтернет-медіа application/vnd.amazon.mobi8-ebook. Файли AZW3 можна конвертувати в ряд інших форматів файлів, наприклад [PDF](/uk/pdf/), [EPUB](/uk/ebook/epub/), [AZW](/uk/ebook/azw/), [DOCX](/uk/ text-processing/docx/) і [RTF](/uk/word-processing/rtf/).

## Формат файлу AZ3/KF8 ##

Файли KF8 є двійковими за своєю природою та зберігають структуру формату файлу MOBI як файл PDB. Як згадувалося раніше, файл KF8 може містити як MOBI, так і новішу версію KF8 EPUB пізніше. Внутрішні деталі формату були розшифровані [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), який є сценарієм Python, який аналізує остаточну скомпільовану базу даних і витягує з неї вихідні файли MOBI або AZW. Файли AZW3 (KF8) також націлені на версію EPUB3 із зворотною сумісністю для EPUB. KF8 компілює файли EPUB і генерує двійкову структуру на основі формату файлу PDB.

## Посилання ##

* [KF8 – Вікіпедія](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)

