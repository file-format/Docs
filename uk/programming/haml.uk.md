{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу HAML - файл вихідного коду Haml",
  "description":"Дізнайтеся про формат файлу HAML та API, які можуть створювати та відкривати файл HAML.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## Що таке файл HAML?

Файл HAML — це файл мови розмітки абстракції HTML, який містить вихідний код, написаний мовою [Haml](https://haml.info/). Його можна використовувати як заміну ERB (сценарії шаблонів Ruby). Файл HAML містить вихідний код шаблону для генерації HTML веб-документа. Файли ERB можна замінити, просто замінивши ці файли в папці app/views на Haml, змінивши розширення файлу. Файли HAML можна відкривати за допомогою будь-якого текстового редактора, наприклад Microsoft Notepad, Notepad++, Apple TextEdit,

## Формат файлу HAML

Файли HAML — це вихідні файли, збережені на диску як звичайні текстові файли. Він містить код, написаний синтаксисом HAML. HAML замінює теги **<>** знаком **%**, щоб зробити код простішим і легшим. Файли ERB можна замінити на HAML, як показано в наступному простому прикладі.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### Приклад HAML

Нижче наведено приклад Hello World прикладу HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
який рендериться до наступного виводу HTML.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Список літератури

* [HAML - Github](https://github.com/haml/haml)

