{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - Формат определения канала",
  "description" :"Узнайте, что такое файл CDF и API, которые могут создавать и открывать файлы CDF.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## .CDF вариант №

Файл с расширением .cdf представляет собой формат файла распространения информации на основе XLM, который использовался для публикации частых обновлений в виде «каналов». Информация публикуется с любого веб-сервера и автоматически доставляется на компьютеры с совместимыми принимающими программами, такими как веб-браузеры. Пользователи подписываются на активные каналы и получают запланированные обновления на свой рабочий стол.
Файлы CDF ранее использовались вместе с технологиями Microsoft Active Channel, Active Desktop и Smart Offline Favorites.

## Формат файла CDF

Файлы CDF сохраняются в виде файлов XML, которые являются общим форматом веб-файлов для обмена информацией. Формат файла CDF в настоящее время является старым форматом и никогда не был широко распространен. По сравнению с этим RSS Netscape был более известен и широко использовался.

### Пример формата файла CDF

Ниже приведен общий пример формата файла CDF.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://домен/папка/"
ПОСЛЕДНИЙМОД="1998-11-05T22:12"
ПРЕДКЭШ = "ДА"
УРОВЕНЬ="0">
<TITLE>Название канала</TITLE>
<ABSTRACT>Синопсис содержания канала.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    ПОСЛЕДНИЙМОД="1998-11-05T22:12"
    ПРЕДКЭШ = "ДА"
УРОВЕНЬ="1">
<TITLE>Название второй страницы</TITLE>
<ABSTRACT>Краткое содержание второй страницы.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## использованная литература

* [Формат определения канала — по Википедии] (https://en.wikipedia.org/wiki/Channel_Definition_Format)

