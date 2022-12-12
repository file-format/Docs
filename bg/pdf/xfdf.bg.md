{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XFDF файлов формат - какво е XFDF файл?",
  "description":"Научете за XFDF файла и API, които могат да създават и отварят XFDF файлове.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е XFDF файл?

Файл с разширение .xfdf е XML Forms Data Format, който се генерира със софтуера Adobe Acrobat. Подобно на [FDF](/bg/pdf/fdf/), XFDF съдържа описание на елементите на формуляра и техните стойности в XML формат. Това може да включва имената и стойностите на текстовите полета в PDF формуляра. XFDF се записват в четим от човека формат и могат да се четат програмно, като се използват езици за програмиране като C#.

## XFDF файлов формат - повече информация

XFDF файловете се записват в XML файлов формат, който е универсален формат, използван за импортиране и експортиране на данни. Файловата структура на XFDF се състои от заглавка, последвана от стойности на полета и данни за елементи, както е показано по-долу.

|Елемент|Атрибут|Съдържание|
---|---|---|
|\<XFDF> ||Най-горният елемент|
|\<fields> ||Всички стойности на полета за този шаблон|
|<field (T)> |име |Име на поле|
|<value (V)> |стойност |Стойност на полето|

## Препратки

* [Поддръжка на FDF формат от Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)
* [Ресурси за разработчици на Adobe](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

