{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл APPCACHE - Формат файлу маніфесту кешу HTML5",
  "description" :"Дізнайтеся, що таке файл APPCACHE та API, які можуть створювати та відкривати файли APPCACHE.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Що таке файл APPCACHE?

Файл APPCACHE — це текстовий файл, який містить список ресурсів, які потрібно кешувати браузерами для офлайн-доступу до веб-програм. Це корисно, коли немає підключення до Інтернету. У такій ситуації браузер використовує ресурси офлайн-кешу, щоб надати доступ до веб-вмісту. Файл APPCACHE містить такі веб-ресурси, як зображення (наприклад, **[PNG](/uk/image/png/)**, **[WEBP](/uk/image/webp/)** тощо), таблиці стилів **([ CSS])(/uk/web/css/)** і файли сценаріїв (наприклад, файли Javascript **[JS](/uk/web/js/)**).

Програми, які можуть **відкривати файли APPCACHE**, включають такі веб-браузери, як Google Chrome, Safari та Firefox.

## Формат файлу APPCACHE - Додаткова інформація

Файли APPCACHE — це прості текстові файли, які забезпечують офлайн-доступ до веб-сторінок для роботи без підключення до Інтернету. Наявність APPCACHE позначає сторінку як доступну в автономному режимі.

### Як посилатися на файл APPCACHE?

На вашій HTML-сторінці посилання на файл APPCACHE вказано таким чином.

```
<html manifest="example.appcache">
  ...
</html>
```

## Структура файлу маніфесту APPCACHE

Простий файл маніфесту APPCACHE виглядає наступним чином.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Це найпростіший приклад, але також можуть бути складніші структури.

## Переваги APPCACHE Manifest

Використання інтерфейсу кешу дає веб-додаткам такі переваги.

1. Перегляд в режимі офлайн. Інтерфейс кешу дозволяє кінцевим користувачам переглядати ваш сайт у режимі офлайн.
1. Швидкість - кеш забезпечує високу швидкість доступу до офлайн-контенту безпосередньо з диска
1. Постійна доступність. Якщо ваш сайт не працює, користувачі все одно матимуть доступ до веб-вмісту та зможуть працювати в автономному режимі.

## Список літератури

* [Посібник для початківців із маніфесту AppCache](https://web.dev/appcache-beginner/)
