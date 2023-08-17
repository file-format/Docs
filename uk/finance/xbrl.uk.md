{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl", "файл xbrl", "формат файлу xbrl", "тип файлу xbrl", "файл", "тип", "що таке файл xbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - Формат файлу бізнес-фінансової звітності",
  "description":"Дізнайтеся про формат файлу XBRL та API, які можуть створювати та відкривати файли XBRL.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Що таке файл XBRL?

Файл із розширенням .xbrl (eXtensible Business Reporting Language) — це безкоштовна глобальна структура для обміну бізнес-інформацією. Зараз він широко використовується як один із стандартних форматів, який замінив старі паперові звіти більш корисними та точними цифровими записами. Дані, якими обмінюються файли XBRL, включають бухгалтерські книги, фінансові відомості та баланси. Він підтримує теги даних, які дозволяють обробляти дані від підготовки до етапу аналізу бізнес-інформації всіх видів. Файли XBRL можна відкривати за допомогою такого програмного забезпечення, як Rivet Software Dragon View XBRL Viewer та API, наприклад [Aspose.Finance](https://products.aspose.com/finance/).

## Формат файлу XBRL

XBRL — це відкритий міжнародний стандарт цифрової бізнес-звітності, який широко використовується в усьому світі. Це мова на основі [XML](/uk/web/xml/), яка використовує елементи XBRL, відомі як теги, для опису кожного елемента бізнес-даних для формулювання даних для сортування та аналізу звітів. Специфікації формату файлів XBRL розроблено та опубліковано компанією XBRL International, Inc із [XBRL версії 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) доступні користувачам.

### Структура документа XBRL

Повна інформація про [теги XBRL 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) можуть бути запропоновані програмістами для написання програм для роботи з цим форматом файлів. XBRL складається з екземпляра XBRL і набору таксономій.

**`Екземпляр XBRL`** - Екземпляр XBRL починається з<xbrl> кореневий елемент. Великий документ XML може містити більше одного вбудованого екземпляра XBRL.

**`Таксономія XBRL`** - [Таксономія XBRL](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html#_5) визначається як структура схеми XML і набір елементів зовнішніх посилань, на які безпосередньо посилаються. Схема масштабованої таксономії, яка показує посилання на базу посилань, така.

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


## Посилання ##

* [XBRL - Вікіпедія](https://en.wikipedia.org/wiki/XBRL)
* [Розширювана мова бізнес-звітності (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html)

