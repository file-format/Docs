{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "файл wpl", "расширение", "формат", "что такое файл wpl", "музыка", "формат файла wpl"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файла WPL и API-интерфейсах, которые могут создавать, конвертировать и открывать файлы WPL.",
  "title" :"WPL — файл списка воспроизведения проигрывателя Windows Media",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## .WPL вариант №

Файл с расширением .wpl содержит список воспроизведения песен для запуска в проигрывателе Microsoft Windows Media. Эти файлы обычно создаются пользователями для своих видео- и аудиоколлекций. Контент, записанный в файле WPL, представляет собой просто пути к каталогам или местоположения для мультимедийных файлов, выбранные создателем файла .wpl, поэтому приложение медиаплеера может быстро найти и воспроизвести мультимедийный контент из своих каталогов.

## Формат файла WPL

WPL (список воспроизведения проигрывателя Windows Media) — это частный формат файла, используемый в проигрывателе Microsoft Windows Media версии 9 или более поздней. Это формат компьютерного файла, в котором хранятся мультимедийные списки воспроизведения. По умолчанию список воспроизведения сохраняется с расширением .wpl (список воспроизведения проигрывателя Windows Media). Вместо этого вы можете использовать расширение [.m3u](/ru/audio/m3u/), если хотите воспроизводить диски с данными на устройстве, которое не поддерживает это расширение. Элементы файла WPL представлены в формате XML.

Элемент верхнего уровня «smil» указывает, что элементы файла следуют структуре синхронизированного языка интеграции мультимедиа (SMIL). Файл создается и сохраняется с расширением .wpl и его типом MIME — application/vnd.ms-wpl.

### Пример WPL

Вот пример файла wpl:
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




## Использованная литература ##

* [MPEG-1 Audio Layer II — по Википедии](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

