{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "файл wpl", "розширення", "формат", "що таке файл wpl", "музика", "формат файлу wpl"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу WPL та API, які можуть створювати, перетворювати та відкривати файли WPL.",
  "title" :"WPL - Файл списку відтворення Windows Media Player",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Що таке файл WPL?

Файл із розширенням .wpl містить список відтворення пісень для запуску в медіапрогравачі Microsoft Windows. Ці файли зазвичай створюють користувачі для своїх колекцій відео та аудіо. Вміст, записаний у файлі WPL, — це лише шляхи до каталогу або розташування для мультимедійних файлів, вибраних творцем файлу .wpl, тому програма медіаплеєра може швидко знаходити та відтворювати мультимедійний вміст у їхніх розташуваннях каталогу.

## Формат файлу WPL

WPL (Список відтворення медіапрогравача Windows) — це власний формат файлів, який використовується в програвачі Microsoft Windows Media Player версії 9 або новішої. Це комп’ютерний формат файлу, який зберігає мультимедійні списки відтворення. За замовчуванням список відтворення зберігається з розширенням .wpl (Список відтворення Windows Media Player). Замість цього можна використовувати розширення [.m3u](/uk/audio/m3u/), якщо ви хочете відтворювати диски з даними на пристрої, який не підтримує це розширення. Елементи файлу WPL представлені у форматі XML.

Елемент верхнього рівня "smil" вказує, що елементи файлу відповідають структурі мови синхронізованої мультимедійної інтеграції (SMIL). Файл створюється та зберігається з розширенням .wpl і його типом MIME є application/vnd.ms-wpl.

### Приклад WPL

Ось приклад файлу wpl:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## Посилання ##

* [MPEG-1 Audio Layer II – Вікіпедія](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

