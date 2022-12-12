{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - Формат визначення каналу",
  "description" :"Дізнайтеся, що таке файл CDF та API, які можуть створювати та відкривати файли CDF.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## Що таке файл CDF?

Файл із розширенням .cdf — це формат файлу розповсюдження інформації на основі XLM, який використовувався для публікації частих оновлень як «канали». Інформація публікується з будь-якого веб-сервера та автоматично доставляється на комп’ютери з сумісними приймальними програмами, такими як веб-браузери. Користувачі підписуються на активні канали та отримують заплановані оновлення на робочий стіл.
Файли CDF раніше використовувалися в поєднанні з технологіями Microsoft Active Channel, Active Desktop і Smart Offline Favorites.

## Формат файлу CDF

Файли CDF зберігаються як файли XML, які є загальним веб-форматом файлів для обміну інформацією. Формат файлу CDF зараз є старим форматом і ніколи не був широко поширеним. У порівнянні з цим, RSS Netscape був більш відомим і широко використовуваним.

### Приклад формату файлу CDF

Нижче наведено загальний приклад формату файлу CDF.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://домен/папка/"
LASTMOD="1998-11-05T22:12"
PRECACHE="YES"
РІВЕНЬ="0">
<TITLE>Назва каналу</TITLE>
<ABSTRACT>Синопсис контенту каналу.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="YES"
РІВЕНЬ="1">
<TITLE>Заголовок другої сторінки</TITLE>
<ABSTRACT>Короткий опис змісту другої сторінки.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Список літератури

* [Формат визначення каналу – за Вікіпедією](https://en.wikipedia.org/wiki/Channel_Definition_Format)

