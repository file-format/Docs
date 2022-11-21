{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "wpl dosyası", "uzantı", "biçim", "wpl dosyası nedir", "müzik", "wpl dosya biçimi"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"WPL dosya formatı ve WPL dosyalarını oluşturabilen, dönüştürebilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"WPL - Windows Media Player Çalma Listesi Dosyası",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## .wpl dosyası nedir?

.wpl uzantılı bir dosya, Microsoft Windows Media Player'da çalıştırılacak şarkıların çalma listesini içerir. Bu dosyalar genellikle kullanıcılar tarafından video ve ses koleksiyonları için oluşturulur. Bir WPL dosyasına yazılan içerik, yalnızca .wpl dosyasının yaratıcısı tarafından seçilen multimedya dosyaları için dizin yolları veya konumlarıdır, bu nedenle medya oynatıcı uygulaması multimedya içeriğini dizin konumlarından hemen bulabilir ve yürütebilir.

## WPL Dosya Biçimi

WPL (Windows Media Player Çalma Listesi), Microsoft Windows Media Player sürüm 9 veya üzeri sürümlerde kullanılan tescilli bir dosya biçimidir. Multimedya oynatma listelerini saklayan bir bilgisayar dosyası biçimidir. Çalma listesi varsayılan olarak bir .wpl(Windows Media Player Çalma Listesi) uzantısıyla kaydedilir. Veri disklerinizi bu uzantıyı desteklemeyen bir cihazda oynatmak istiyorsanız, bunun yerine [.m3u](/tr/audio/m3u) uzantısını kullanabilirsiniz. Bir WPL dosyasının öğeleri XML biçiminde temsil edilir.

En üst düzey öğe olan "smil", dosya öğelerinin Eşitlenmiş Multimedya Entegrasyon Dili (SMIL) yapısını takip ettiğini belirtir. Dosya .wpl uzantısıyla oluşturulur ve kaydedilir ve MIME türü application/vnd.ms-wpl'dir.

### WPL örneği

İşte bir wpl dosyası örneği:
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




## Referanslar ##

* [MPEG-1 Ses Katmanı II - Wikipedia'dan](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

