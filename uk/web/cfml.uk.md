{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - файл мови розмітки ColdFusion",
  "description" :"Дізнайтеся, що таке файл CFML та API, які можуть створювати та відкривати файли CFML.",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## Що таке файл CFML?

Файл із розширенням .cfml — це файл мови розмітки ColdFusion, який використовується для створення веб-сторінки. Це стосується набору правил, які використовуються для визначення того, як програміст розроблятиме програму ColdFusion. ColdFusion — це мова програмування, яка використовується для швидкого та меншого використання веб-додатків на стороні сервера, ніж інші технології, такі як [ASP](/uk/web/asp/), [PHP](/uk/programming/php/) тощо. Серед програм, які можуть відкривати файли CML, є Adobe ColdFusion 2018, Adobe ColdFusion Builder і Adobe Dreamweaver.

## Формат файлу CFML – Додаткова інформація

Файли CFML є файлами розмітки та містять веб-елементи у формі тегів. Це текстові файли, які можна відкривати та редагувати в будь-якому текстовому редакторі. Файли CFML складаються з кількох тегів, подібних до [HTML](/uk/web/html/) і зазвичай містять відкриваючий і закриваючий теги. Ці теги також можуть містити один або декілька атрибутів.

### Синтаксис тегів

Нижче наведено узагальнений синтаксис тегів CFML.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

Більшість тегів приймають атрибути та визначаються наступним чином.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Деякі з цих тегів також приймають кілька атрибутів із таким синтаксисом.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## Приклад коду CFML

Ось приклад використання фактичного тегу CFML – тегу `cfoutput`:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Список літератури

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

