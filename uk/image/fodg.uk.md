{
  "date" : "2019-10-11",
  "keywords" :[ "файл fodg", "формат файлу fodg", "що таке файл fodg", "файл", "приклад fodg", "розширення файлу fodg", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - формат файлу креслення OpenDocument",
  "description":"Дізнайтеся про формат файлу FODG та API, які можуть створювати та відкривати файли FODG.",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл FODG?

Файл із розширенням .fodg — це формат файлу Apache OpenOffice Drawing для зберігання елементів малюнка. Він заснований на специфікаціях формату файлів, викладених у Стандартах вдосконалення структурної інформації (OASIS). Іншим подібним форматом файлу для графіки OpenOffice є [ODG](/uk/image/odg/), який зберігає елементи малюнка як векторне зображення. Файли FODG можна відкривати за допомогою OpenOffice, а також LibreOffice. Інші формати файлів, які підтримує OpenOffice, включають, наприклад, [ODT](/uk/text-processing/odt/), ODF, [ODP](/uk/presentation/odp/) і [ODS](/uk/spreadsheet/ods/).

## Формат файлу FODG

FODG базується на форматі файлу XML OpenDocument, який відповідає OASIS OpenDocument Format ISO/IEC 26300. Він має тип Інтернет-медіа application/vnd.oasis.opendocument.graphics, а також відповідає org.oasis-open.opendocument public.composite-content . Структура XML є загальною для всіх типів документів, таких як електронні таблиці, файли малюнків і текстові документи. Документи OpenOffice використовують переваги поділу проблем, розділяючи вміст, стилі, метадані та параметри програми на чотири окремі файли XML.

`<office:document-content>` - вміст документа та автоматичні стилі, які використовуються у вмісті.
`<office:document-styles>` – Стилі, що використовуються у вмісті документа, і автоматичні стилі, що використовуються в самих стилях.
`<office:document-meta>` – метаінформація документа, наприклад автор або час останнього збереження.
`<office:document-settings>` – параметри програми, наприклад розмір вікна або інформація про принтер.

## Посилання ##
* [Майбутні специфікації для стандартизації версії 1.3](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [Формат відкритих документів OASIS для офісних програм](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Формат OpenDocument – Вікіпедія](https://en.wikipedia.org/wiki/OpenDocument)

