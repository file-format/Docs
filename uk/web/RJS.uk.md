{
  "date" : "2021-05-24",
  "keywords" :["rjs", "Файл", "Розширення", "Формат файлу", "Розширення файлу", "RJS", "Файл Javascript Ruby"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - файл Javascript Ruby",
  "description":"Дізнайтеся, що таке формат файлу RJS та API, які можуть створювати та відкривати файли RJS.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Що таке файл RJS?

Файл із розширенням .rjs — це комбінація коду Ruby та JavsScript, що дозволяє розробникам Rails використовувати Ruby для створення динамічного коду JavaScript. Код Ruby вбудовано у функції Java і компілюється на веб-сервері, для роботи якого на сервері потрібен механізм Ruby. RJS схожий на [RHTML](/uk/web/rhtml/); єдина відмінність полягає в тому, що бічна частина містить код Ruby у [HTML](/uk/web/html/), тоді як вона містить код Ruby у функціях Javascript.

## Формат файлу RJS

Файли RJS кодуються у вигляді звичайного тексту, як і будь-яка інша мова сценаріїв або програмування. Коли така сторінка запитується клієнтом, код Ruby виконується на сервері, і лише код HTML і Javascript повертаються до браузера клієнта. Синтаксис файлу RJS подібний до синтаксису комбінації Ruby та JavaScript, тобто лише код Ruby вбудовано у функції JavaScript.

### Приклад RJS

У наступному прикладі показано простий код Ruby окремо, а потім вбудований у функцію JavaScript.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
а далі є RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Список літератури

* [RJS](https://github.com/makevoid/rjs)

