{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлів KIT та API, які можуть створювати та відкривати файли KIT.",
  "title" :"Формат файлу KIT - файл CodeKit",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Що таке файл KIT?

Файл із розширенням .kit – це файл HTML, створений за допомогою додатка мови програмування [CodeKit](https://codekitapp.com/). Він містить `імпорти` та `змінні` на додаток до існуючих файлів [HTML](/uk/web/html/), що робить його ідеальним для статичних сайтів. CodeKit компілює файли KIT у HTML, який можна легко використовувати як статичні файли веб-сайту.

## Формат файлу KIT

Файли KIT — це файли HTML, які додатково містять імпорт і змінні. Вони зберігаються як звичайні текстові файли та можуть бути відкриті за допомогою будь-якого текстового редактора або веб-редакторів файлів.

### Імпорт файлів KIT

Майже будь-який тип файлу можна імпортувати у файл Kit. Нижче наведено синтаксис імпорту, який використовується для імпорту файлів у файл .kit.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Коли імпорт додається до файлу KIT і зберігається, він замінюється текстом файлу, який імпортується. Ви також можете використовувати @include замість @import.

### Кілька імпортів у файлі KIT

Ви також можете імпортувати більше одного файлу одночасно, використовуючи список, розділений комами:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Список літератури

* [Що таке Kit?](https://codekitapp.com/help/kit/)

