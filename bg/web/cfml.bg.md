{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML – езиков файл за маркиране на ColdFusion",
  "description" :"Научете какво е CFML файл и API, които могат да създават и отварят CFML файлове.",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## Какво е CFML файл?

Файл с разширение .cfml е файл на ColdFusion Markup Language, който се използва за създаване на уеб страница. Отнася се до набор от правила, използвани за определяне на това как приложението ColdFusion ще бъде разработено от програмиста. ColdFusion е език за програмиране, който се използва за създаване на уеб приложения от страна на сървъра бързо и с по-малко от други технологии като [ASP](/bg/web/asp/), [PHP](/bg/programming/php/) и др. от приложенията, които могат да отварят CML файлове, включват Adobe ColdFusion 2018, Adobe ColdFusion Builder и Adobe Dreamweaver.

## CFML файлов формат - повече информация

CFML файловете са файлове за маркиране и съдържат уеб елементи под формата на тагове. Това са текстови файлове, които могат да се отварят и редактират във всеки текстов редактор. CFML файловете се състоят от няколко тагове, които са подобни на [HTML](/bg/web/html/) и обикновено се състоят от отварящ и затварящ етикет. Тези тагове могат също да съдържат един или повече атрибути.

### Синтаксис на етикети

Следва обобщеният синтаксис на CFML таговете.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

Повечето тагове приемат атрибути и се дефинират както следва.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Някои от тези тагове също приемат множество атрибути със следния синтаксис.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## Пример за CFML код

Ето един пример, който използва действителен CFML таг - тагът `cfoutput`:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Препратки

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

