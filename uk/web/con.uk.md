{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CON File - Concept Application Source File Format",
  "description" :"Дізнайтеся, що таке файл CON та API, які можуть створювати та відкривати файли CON.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## Що таке файл CON?

Файл CON — це файл вихідного коду програми, розробленої для **Concept Application Server**. Використовується для написання програм для обміну даними між сервером і користувачем. Файли CON, розміщені на сервері, доступні за допомогою веб-браузера за умови, що на стороні користувача встановлено Concept Client. Концепція Сервер додатків — це веб-сервер із невеликою мовою програмування, який може мати [SQL](/uk/database/sql/) механізм бази даних підмножини (TinDB).

Файли CON можна відкривати/запускати за допомогою RadGs Concept Application Server.

## Формат файлу CON - Додаткова інформація

Файли CON розміщені на сервері та доступ до них здійснюється за допомогою веб-браузера на комп’ютері користувача. [URL-адреси понять](/uk/web/url/) відрізняються від звичайних URL-адрес HTTP і починаються з **concept://**.

### Приклад URL-адреси файлу CON

Доступ до файлу CON, розміщеного на Concept Application Server, можна отримати через веб-браузер за допомогою таких URL-адрес:

```
concept://domain.server.com/web_application/main.con.
```
## Список літератури

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

