{
  "date" : "2019-10-11",
  "keywords" :["xml", "Файл", "Розширення", "Формат файлу", "Розширення файлу", "розширювана мова розмітки"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу XML",
  "description":"Дізнайтеся про формат XML-файлу та API, які можуть створювати та відкривати XML-файли.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл XML?

XML означає Extensible Markup Language, схожий на **[HTML](/uk/web/html/)**, але відрізняється використанням тегів для визначення об’єктів. Вся ідея створення формату файлу XML полягала в тому, щоб зберігати та транспортувати дані без залежності від програмних чи апаратних засобів. Його популярність пояснюється тим, що його можна зчитувати як людиною, так і машиною. Це дає змогу створювати загальні протоколи даних у формі об’єктів, які зберігатимуться та передаватимуться в мережі, такій як World Wide Web (WWW). "X" у XML означає розширюваний, що означає, що мова може бути розширена до будь-якої кількості символів відповідно до вимог користувача. Саме для цих функцій його використовують багато стандартних форматів файлів, наприклад Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/uk/web/xhtml/)** і **[SVG](/uk/page-description-language/svg/)**.

## Формат файлу XML

Формат файлу XML базується на об’єктній моделі XML-документа (DOM), яка є API програмування для документів HTML і XML. XML DOM визначає стандартний метод доступу до елементів документа XML і керування ними. Він створює деревовидну структуру документа XML, яку можна використовувати для доступу до всіх елементів через дерево DOM. Існуючі елементи можна змінювати/видаляти, а також створювати нові елементи в дереві XML. Кожен елемент документа XML називається вузлом. XML DOM виглядає так, як показано на наступному зображенні.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### Універсальний підхід XML

Потужність XML робить його універсальною мовою для передачі даних через мережу, спрощуючи передачу даних і зміну платформи. Це також забезпечує можливість обміну даними між несумісними системами, зберігаючи дані у форматі звичайного тексту. HTML призначений для представлення даних через Інтернет, тоді як XML призначений для обміну даними. Пари тегів розмітки, що використовуються всередині XML, визначають ключові елементи структури, які будуть використовуватися програмами для читання.

## Приклад XML

Нижче наведено спрощений приклад каталогу компакт-дисків, у якому кожен запис містить інформацію про компакт-диски, наприклад виконавця, країну, компанію, ціну та рік виробництва.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## Список літератури

* [XML – Вікіпедія](https://en.wikipedia.org/wiki/XML)

