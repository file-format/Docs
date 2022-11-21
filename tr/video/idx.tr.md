{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - Yüksek Verimli Video Codec",
  "description":"IDX dosya formatı ve IDX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## IDX dosyası nedir?

Bir IDX dosyası, bir .sub (VobSub Altyazıları) dosyası içindeki altyazılar için meta veri bilgileri listesine işaret eden bir altyazı dizin dosyasıdır. Kullanıcıların DVD'lerden altyazıları çıkarmasına ve bir SUB dosyasına dökmesine izin veren VobSub yazılım uygulaması tarafından oluşturulur ve kullanılır. IDX dosyaları, her bir altyazıyı işaret etmek için kullanılan zaman damgalarını ve bayt ofsetlerini içerir. VobSub, karşılık gelen SUB dosyasıyla birlikte her zaman bir IDX dosyası oluşturur.

## IDX Dosya Biçimi - Daha Fazla Bilgi

IDX dosyaları, herhangi bir metin düzenleyicide açılabilen düz metin dosyaları olarak oluşturulur ve kaydedilir. Bir IDX dosyası, ekranda görüntülenecek altyazı metninin rengi, altyazı metninin ekrandaki konumu gibi parametreleri okumak için medya yürütücüler tarafından okunan bilgileri içerir.

### IDX Altyazı Ayarları

Tipik bir IDX dosyası, bu meta veri bilgilerini dosyanın başlangıcında saklar. Altyazı ayarları **#** ile başlar. Tüm bu altyazı ayarlarından sonra zaman damgaları ve resim referansları eklenir ve **zaman damgası:** ile başlar.

## IDX Dosya Biçimi Örneği

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## IDX dosyası nasıl kullanılır?

Bir film için Sub ve IDX dosyalarına sahipseniz, bu altyazıları oluşturuldukları filmle birlikte oynatabilirsiniz. VLC, GOM Player, PotPlayer veya PowerDVD gibi birçok uygulama, bu SUB ve IDX dosyalarını yükleme ve bunları filmin yanında oynatma özelliğine sahiptir. Yazılım uygulamaları ayrıca SUB ve IDX altyazı dosyalarını [.mkv](/tr/video/mkv/) dosyalarına gömebilir.

## IDX'i SRT'ye dönüştür

[SRT](/tr/video/srt/) (SubRip dosya formatı), SubRip dosya formatında kaydedilen basit bir altyazı dosyasıdır. VobSub dosya biçimine kıyasla daha yaygın olarak kullanılır. Bu nedenle, SUB/IDX dosyalarını SRT dosya biçimine dönüştürmek isterseniz, bunu başarmak için kullanılabilecek 3. taraf araçlar mevcuttur. SubtitleTools.com'da bulunan SUB/IDX - SRT dönüştürücü, SUB ve IDX dosyalarını girdi olarak alan ve bu VobSub altyazılarını SRT dosyalarına dönüştüren böyle bir araçtır.

## Referanslar

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - Wiki Multimedya](https://wiki.multimedia.cx/index.php?title=VOBsub)

