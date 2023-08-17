{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl", "xbrl файл", "xbrl файлов формат", "xbrl файлов тип", "файл", "тип", "какво е xbrl файл" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL – файлов формат за бизнес и финансови отчети",
  "description":"Научете за файловия формат XBRL и API, които могат да създават и отварят XBRL файлове.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Какво е XBRL файл?

Файл с разширение .xbrl (eXtensible Business Reporting Language) е свободно достъпна и глобална рамка за обмен на бизнес информация. Сега той се използва широко като един от стандартните формати, който замени по-старите отчети на хартиен носител с по-полезни и точни цифрови записи. Данните, обменяни с помощта на XBRL файловете, включват счетоводни книги, финансови подробности и баланси. Той поддържа етикети за данни, които позволяват обработка на данни от подготовката до етапа на анализ на бизнес информация от всякакъв вид. XBRL файловете могат да се отварят с помощта на софтуер като Rivet Software Dragon View XBRL Viewer и API като [Aspose.Finance](https://products.aspose.com/finance/).

## XBRL файлов формат

XBRL е отворен международен стандарт за цифрово бизнес отчитане, който се използва широко в световен мащаб. Това е базиран на [XML](/bg/web/xml/) език, който използва XBRL елементи, известни като тагове, за описание на всеки елемент от бизнес данни за формулиране на данни за сортиране и анализ на отчети. Спецификациите на XBRL файлов формат са разработени и публикувани от XBRL International, Inc, с [XBRL версия 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) в момента достъпни за потребителите.

### XBRL структура на документа

Пълна информация за [XBRL 2.1 таговете](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) могат да бъдат препоръчани от програмисти за писане на приложения за работа с този файлов формат. XBRL се състои от екземпляр на XBRL и колекция от таксономии.

**`XBRL екземпляр`** - XBRL екземплярът започва с<xbrl> коренов елемент. Голям XML документ може да съдържа повече от един екземпляр на XBRL, вграден в него.

**`XBRL Таксономия`** - [XBRL Таксономия](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 +corrected-errata-2013-02-20.html#_5) се дефинира като структура на XML схема и набор от директно препратени елементи на външни връзки. Мащабируема таксономична схема, показваща препратките към базата с връзки, е както следва.

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


## Препратки ##

* [XBRL – от Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [Разширяем език за бизнес отчети (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html)

