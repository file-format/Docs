{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - Формат за дефиниране на канал",
  "description" :"Научете какво е CDF файл и API, които могат да създават и отварят CDF файлове.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## Какво е CDF файл?

Файл с разширение .cdf е базиран на XLM файлов формат за разпространение на информация, който се използва за публикуване на чести актуализации като „канали“. Информацията се публикува от всеки уеб сървър и се доставя автоматично на компютри със съвместими приемни програми, като уеб браузъри. Потребителите се абонират за активни канали и имат планирани актуализации, доставени на работния плот.
CDF файловете бяха използвани по-рано във връзка с технологиите Active Channel, Active Desktop и Smart Offline Favorites на Microsoft.

## CDF файлов формат

CDF файловете се записват като XML файлове, които са общ уеб файлов формат за обмен на информация. Файловият формат CDF вече е стар формат и никога не е бил широко възприет. В сравнение с това, RSS на Netscape беше по-известен и широко използван.

### Пример за CDF файлов формат

Следното е общ пример на файловия формат CDF.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://domain/folder/"
LASTMOD="1998-11-05T22:12"
PRECACHE="ДА"
LEVEL="0">
<TITLE>Заглавие на канала</TITLE>
<ABSTRACT>Синопсис на съдържанието на канала.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="ДА"
LEVEL="1">
<TITLE>Заглавие на втора страница</TITLE>
<ABSTRACT>Резюме на съдържанието на втора страница.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Препратки

* [Формат за дефиниране на канала - от Wikipedia](https://en.wikipedia.org/wiki/Channel_Definition_Format)

