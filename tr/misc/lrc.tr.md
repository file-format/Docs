{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LRC Dosya Formatı - LRC dosyası nedir?",
  "description":"LRC Şarkı Sözü dosyası ve LRC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## .lrc dosyası nedir?

Bir LRC dosyası, bir sesli şarkının sözlerini içeren metin tabanlı bir şarkı sözü dosyasıdır. Sesli şarkı bilgisayarda bir müzik çalar veya müzik çalar yazılımı ile çalındığında, LRC dosyası paralel olarak okunur ve zamana göre görüntülenir. LRC dosyaları, şarkı çalarken şarkı sözlerinin görüntülenmesi için işaret noktaları içerir. Genel olarak, LRC dosyaları audio.mp3 ve audio.lrc gibi karşılık gelen ses dosyasıyla aynı ada sahiptir. LRC dosyaları, [SRT](/tr/video/srt/) gibi altyazı dosyalarına benzer.

## LRC Dosya Biçimi - Daha Fazla Bilgi

LRC şarkı sözü biçimindeki dosyalar, düz metin dosyaları olarak kaydedilir ve bir metin dosyasında açılıp düzenlenebilir. Bir LRC dosyasının içeriği, şarkı sözü metninin görüntülenmesi için renk bilgisi içerir.

## LRC Formatları

Zaman içinde geliştirilmiş birden çok LRC dosyası biçimi vardır. Bunlar

### Basit LRC Biçimi

Satır Süresi Etiketleri [mm:ss.xx] biçimindedir; burada mm dakika, ss saniye ve xx saniyenin yüzde biridir.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Genişletilmiş Basit Biçim

M: Erkek, K: Kadın, D: Düet kullanarak sözlerin cinsiyetini değiştirme ve belirtme özelliğini içerir.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Gelişmiş LRC formatı

Geliştirilmiş LRC formatı, Simple LRC formatının genişletilmiş versiyonudur. biçiminde bir Word Zaman Etiketi ekler.<mm:ss.xx> önceki kelimenin sonunda.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## Referanslar

* [LRC Söz Dosyası Formatı - Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))

