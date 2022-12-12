{
  "date" : "2021-05-24",
  "keywords" :["xul", "Файл", "Розширення", "Формат файлу", "Розширення файлу", "Мова інтерфейсу користувача XML"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - файл мови інтерфейсу користувача XML",
  "description":"Дізнайтеся про формат файлу XUL та API, які можуть створювати та відкривати файли XUL.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Що таке файл XUL?

Файл із розширенням .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) означає мову інтерфейсу користувача XML) є файлом мови розмітки на основі [XML](/uk/web/xml/) для створення інтерфейсів користувача. Він був розроблений Mozilla для розробників для створення елементів графічного інтерфейсу користувача, подібних до інших мов розмітки, які використовуються для створення веб-сторінок. XUL широко використовувався Mozilla у своєму браузері Firefox, де він використовував кодову базу Mozilla. Візуалізація XUL виконується за допомогою
[Двигун Gecko](https://en.wikipedia.org/wiki/Gecko_(software)). Розгалуження Firefox, такі як Pale Moon, Basilisk і Waterfox, зберігають підтримку додатків XUL. Файли XUL ідентифікуються за типом MIME: application/vnd.mozilla.xul+xml.

## Формат файлу XUL

Файли XUL записуються у вигляді звичайного тексту на основі формату файлів XML і відображаються за допомогою механізму Gecko. Три основні частини структури XUL:

* `Вміст` - це включає оголошення вікна та елементів інтерфейсу користувача, що містяться в них.
* `Skin` - містить будь-які таблиці стилів, зображення та інші файли, пов'язані з темою. Зовнішній вигляд вікна описано в таблицях стилів.
* `Locale` - Текст, який відображається у вікні, зберігається окремо, і користувачі можуть використовувати кілька наборів мовних файлів.

### Приклад XUL

У наступному прикладі створено три кнопки, які розташовані одна на одній у вертикальному напрямку.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Список літератури

* [XUL - Вікіпедія](https://en.wikipedia.org/wiki/XUL)
* [Архівна документація XUL - від Mozilla](https://wiki.mozilla.org/XUL:Home_Page)

