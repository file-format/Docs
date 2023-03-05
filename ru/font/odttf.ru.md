{
  "date" : "2023-01-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл ODTTF — запутанный формат файла шрифта OpenType",
  "description":"Узнайте о формате файла ODTTF и API-интерфейсах, которые могут создавать и открывать файлы ODTTF.",
  "linktitle" : "ODTTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2023-01-13"
}

## .ODTTF вариант №

Файл ODTTF — это формат файла шрифта, который используется форматами файлов [.XPS](/ru/page-description-language/xps/) и Microsoft Office 2007. Он содержит обфусцированный шрифт OpenType, который был изменен, чтобы затруднить извлечение информации о дизайне шрифта или реинжиниринг исходного кода шрифта. ODTTF основан на шрифтах, используемых в исходных документах, но не в обычном формате и может не считываться сторонним программным обеспечением для извлечения данных шрифта.

Вы можете открывать файлы ODTTF с помощью Pagemark XpsViewer, Apple Safari с Pagemark XpsPlugin, Mozilla Firefox с Pagemark XpsPlugin,
NiXPS View и NiXPS Edit.

## Формат файла ODTTF

Внутренняя структура формата файла ODTTF неизвестна, поскольку они хранятся во встроенном запутанном формате. Они могут быть встроены в цифровые документы, такие как .PDF или .DOCX.

## использованная литература
* [Спецификации шрифтов OpenType от Microsoft](https://docs.microsoft.com/en-us/typography/opentype/spec/overview)
* [Обзор TrueType](https://docs.microsoft.com/en-us/typography/truetype/)

