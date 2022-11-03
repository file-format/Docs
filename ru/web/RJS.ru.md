{
  "date" : "2021-05-24",
  "keywords" :["rjs", "Файл", "Расширение", "Формат файла", "Расширение файла", "RJS", "Файл Ruby Javascript"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS — файл Ruby Javascript",
  "description":"Узнайте, что такое формат файла RJS и API, которые могут создавать и открывать файлы RJS.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## .RJS вариант №

Файл с расширением .rjs представляет собой комбинацию кода Ruby и JavsScript, что позволяет разработчикам Rails использовать Ruby для создания динамического кода JavaScript. Код Ruby встроен в функции Java и компилируется на веб-сервере, для чего требуется, чтобы на сервере работал механизм Ruby. RJS похож на [RHTML](/ru/web/rhtml/); единственное отличие состоит в том, что боковой код содержит код Ruby в [HTML](/ru/web/html/), а код Ruby — в функциях Javascript.

## Формат файла RJS

Файлы RJS закодированы в виде простого текста, как и любой другой язык сценариев или программирования. Когда такая страница запрашивается клиентом, код Ruby выполняется на сервере, и в браузер клиента возвращается только код HTML и Javascript. Синтаксис файла RJS похож на комбинацию синтаксиса Ruby и JavaScript, так что только код Ruby встроен в функции JavaScript.

### Пример RJS

В следующем примере показан независимый простой код Ruby, а затем встроенный в функцию JavaScript.

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
и следующий RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## использованная литература

* [RJS] (https://github.com/makevoid/rjs)

