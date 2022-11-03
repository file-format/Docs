{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла HAML — файл исходного кода Haml",
  "description":"Узнайте о формате файла HAML и API, которые могут создавать и открывать файл HAML.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## .HAML вариант №

Файл HAML — это файл языка разметки абстракции HTML, который содержит исходный код, написанный на языке [Haml](https://haml.info/). Его можно использовать в качестве замены ERB (скрипты шаблонов Ruby). Файл HAML содержит исходный код шаблона для создания HTML веб-документа. Файлы ERB можно заменить, просто заменив эти файлы в папке app/views на Haml, изменив расширение файла. Файлы HAML можно открывать в любом текстовом редакторе, таком как Microsoft Notepad, Notepad++, Apple TextEdit,

## Формат файла HAML

Файлы HAML — это исходные файлы, сохраненные на диске в виде обычных текстовых файлов. Он содержит код, написанный с синтаксисом HAML. HAML заменяет теги **<>** знаком **%**, чтобы сделать код проще и легче. Файлы ERB можно заменить на HAML, как показано в следующем простом примере.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### Пример HAML

Ниже приведен пример Hello World для HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
который отображает следующий вывод HTML.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## использованная литература

* [HAML — Github] (https://github.com/haml/haml)

