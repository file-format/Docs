{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl", "файл xbrl", "формат файла xbrl", "тип файла xbrl", "файл", "тип", "что такое файл xbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL — формат файла деловой и финансовой отчетности",
  "description":"Узнайте о формате файлов XBRL и API, которые могут создавать и открывать файлы XBRL.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
"идентификатор":"финансы-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## .XBRL вариант №

Файл с расширением .xbrl (eXtensible Business Reporting Language) представляет собой свободно доступную глобальную платформу для обмена деловой информацией. В настоящее время он широко используется в качестве одного из форматов стандартов, который заменил старые бумажные отчеты более полезными и точными цифровыми записями. Данные, которыми обмениваются файлы XBRL, включают бухгалтерские книги, финансовые сведения и балансовые отчеты. Он поддерживает теги данных, что позволяет обрабатывать данные от подготовки до этапа анализа бизнес-информации всех видов. Файлы XBRL можно открывать с помощью программного обеспечения, такого как Rivet Software Dragon View XBRL Viewer, и таких API, как [Aspose.Finance](https://products.aspose.com/finance).

## Формат файла XBRL

XBRL — это открытый международный стандарт цифровой бизнес-отчетности, который широко используется во всем мире. Это язык на основе [XML](/ru/web/xml/), который использует элементы XBRL, известные как теги, для описания каждого элемента бизнес-данных для формулирования данных для сортировки и анализа отчетов. Спецификации формата файлов XBRL разрабатываются и публикуются XBRL International, Inc. В настоящее время [XBRL версии 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) доступны пользователям.

### Структура документа XBRL

Полная информация о [тегах XBRL 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata- 2013-02-20.html) могут быть использованы программистами для написания приложений для работы с этим форматом файла. XBRL состоит из экземпляра XBRL и набора таксономий.

**`Экземпляр XBRL`** — экземпляр XBRL начинается с<xbrl> корневой элемент. Большой XML-документ может содержать несколько внедренных в него экземпляров XBRL.

**`Таксономия XBRL`** — [Таксономия XBRL](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 +corrected-errata-2013-02-20.html#_5) определяется как структура схемы XML и набор элементов внешних ссылок с прямыми ссылками. Масштабируемая схема таксономии, показывающая ссылки базы ссылок, выглядит следующим образом.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## Использованная литература ##

* [XBRL — Википедия](https://en.wikipedia.org/wiki/XBRL)
* [Расширяемый язык бизнес-отчетности (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- опечатки-2013-02-20.html)

