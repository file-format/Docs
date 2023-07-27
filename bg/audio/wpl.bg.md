{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "wpl файл", "разширение", "формат", "какво е wpl файл", "музика", "wpl файлов формат"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за WPL файловия формат и API, които могат да създават, конвертират и отварят WPL файлове.",
  "title" :"WPL – Файл със списък за възпроизвеждане на Windows Media Player",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Какво е WPL файл?

Файл с разширение .wpl съдържа плейлиста с песни, които да се изпълняват в Microsoft Windows Media Player. Тези файлове обикновено се създават от потребители за техните видео и аудио колекции. Съдържанието, записано в WPL файл, е само пътеки към директории или местоположения за мултимедийните файлове, избрани от създателя на .wpl файла, така че приложението за медиен плейър може незабавно да намери и възпроизведе мултимедийното съдържание от техните местоположения в директория.

## WPL файлов формат

WPL (Windows Media Player Playlist) е собствен файлов формат, използван в Microsoft Windows Media Player версии 9 или по-нови. Това е компютърен файлов формат, който съхранява мултимедийни плейлисти. По подразбиране плейлистът се записва с разширение .wpl (Windows Media Player Playlist). Вместо това можете да използвате разширението [.m3u](/bg/audio/m3u/), ако искате да възпроизвеждате вашите дискове с данни на устройство, което не поддържа това разширение. Елементите на WPL файл са представени в XML формат.

Елементът от най-високо ниво "smil" указва, че елементите на файла следват структурата на езика за синхронизирана мултимедийна интеграция (SMIL). Файлът се създава и записва с разширение .wpl и неговият MIME тип е application/vnd.ms-wpl.

### WPL пример

Ето пример за wpl файл:
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




## Препратки ##

* [MPEG-1 Audio Layer II - от Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

