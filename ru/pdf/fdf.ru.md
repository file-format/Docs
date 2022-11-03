{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла FDF — что такое файл FDF?",
  "description":"Узнайте о формате файла FDF и API-интерфейсах, которые могут создавать и открывать файлы FDF.",
  "linktitle" : "FDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## .FDF вариант №

Файл FDF (**Forms Data Format**) — это текстовый документ, созданный путем экспорта данных из полей формы файла [PDF](/ru/pdf/). Он включает только данные текстовых полей, которые извлекаются из полей формы, доступных в файле PDF. Это приводит к сравнительно небольшому файлу данных, так как экспортируемые данные не содержат самой формы. Adobe Acrobat предоставляет функцию экспорта данных полей формы с помощью параметра «Экспорт данных форм» в меню приложения.

## Формат файла FDF — дополнительная информация

FDF — это обычный текстовый формат, включенный в [стандарт ISO 32000] (https://www.iso.org/standard/51502.html) для Portable Document Format. Он был разработан Adobe для импорта и экспорта данных из Acrobat Forms или AcroForms.

Существует два типа файлов FDF:

• «Классический FDF» — предоставляет данные для заполнения существующей статической формы.

• «Шаблон FDF» — создает новый PDF-файл на основе шаблонов из указанных PDF-файлов. Формы внутри нового документа заполняются путем предоставления данных.

## Создание FDF с помощью Adobe Acrobat

[Набор инструментов FDF] (https://opensource.adobe.com/dc-acrobat-sdk-docs/) от Adobe позволяет создавать файлы FDF из текстовых данных.

## Использованная литература ##

* [Поддержка формата FDF в Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)
* [Ресурсы Adobe для разработчиков] (https://opensource.adobe.com/dc-acrobat-sdk-docs/)

