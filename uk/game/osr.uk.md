{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу OSR та API, які можуть створювати та відкривати файли OSR.",
  "title" : "Файл OSR - osu! Формат файлу відтворення",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-uk",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Що таке файл OSR?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**Тип MIME формату файлу OSR:** x-osu-replay

## Формат файлу OSR

Файли OSR зберігаються як двійкові файли з полями даних фіксованої та змінної довжини.

|Тип даних| Формат|
---|---|
|Байт |Режим гри повтору (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Ціле |Версія гри під час створення повтору (наприклад, 20131216)|
|Рядок |osu! хеш карти битів MD5|
|Рядок| Ім'я гравця|
|Рядок| osu! хеш повтору MD5 (включає певні властивості повтору)|
|Короткий| Кількість 300с|
|Короткий| Кількість 100 у стандарті, 150 у Taiko, 100 у CTB, 100 у mania|
|Короткий| Кількість 50 у стандарті, малий фрукт у CTB, 50 у манії|
|Короткий| Кількість гіків у стандарті, максимум 300 у манії|
|Короткий| Кількість катусів у стандарті, 200 у манії|
|Короткий| Кількість промахів|
|Ціле| Загальний бал, що відображається у звіті про результати|
|Короткий| Найбільше комбо відображається у звіті про результати|
|Байт| Ідеальний/повний комбо (1 = без промахів і без розривів повзунків і без достроково завершених повзунків)|
|Ціле| Використані моди. Нижче наведено список значень модів.|
|Рядок| Гістограма життя: розділені комами пари u/v, де u — це час у пісні в мілісекундах, а v — це значення з плаваючою комою від 0 до 1, яке представляє кількість життя, яке ви маєте в даний момент часу (0 = шкала життя — порожній, 1= панель життя заповнена)|
|Довгий| Мітка часу (галочки Windows)|
|Ціле| Довжина стислих даних відтворення в байтах|
|Байт |Масив Стислі дані відтворення|
|Довгий| Онлайн Score ID|
|Подвійний| Додаткова інформація про мод. Присутній, лише якщо ввімкнено Target Practice.|

## Список літератури

* [OSU! Ритм-гра](https://osu.ppy.sh/home)

* [Формат файлу OSR](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


