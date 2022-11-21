{
  "date" : "2019-12-13",
  "keywords" :[ "WAV", "dosya", "uzantı", "biçim", "ses değişim dosyası biçimi", "müzik"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"WAV dosya formatı ve WAV dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"WAV - Dalga Biçimi Ses Dosyası Biçimi",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## WAV dosyası nedir?

WAVE (Dalga Biçimi Ses Dosyası Biçimi) olarak bilinen WAV, dijital ses dosyalarını depolamak için Microsoft'un Kaynak Değişim Dosyası Biçimi (RIFF) özelliğinin bir alt kümesidir. Biçim, bit akışına herhangi bir sıkıştırma uygulamaz ve ses kayıtlarını farklı örnekleme hızları ve bit hızlarıyla depolar. Ses CD'leri için standart formatlardan biridir ve biridir. Wave dosyalarının boyutu, aynı ses kalitesini korurken dosya boyutunu küçültmek için kayıplı sıkıştırma kullanan [MP3](/tr/audio/mp3/) gibi yeni ses dosyası biçimleriyle karşılaştırıldığında daha büyüktür. Ancak, WAV dosyaları Audio Compression Manager (ACM) kodekleri kullanılarak sıkıştırılabilir. WAV dosyalarını diğer popüler ses dosyası formatlarına dönüştürebilen birçok API ve uygulama mevcuttur.

**Biliyor musun?**
Bulgularınızla dosya formatı topluluğunu güncel tutmak için FileFormat.com'a katkıda bulunabilirsiniz. WAV veya Ses dosyası formatları hakkında herhangi bir şey paylaşmanız gerekiyorsa, insanların güncel kalması için bulgularınızı [Ses Dosyası Formatı Haberleri](https://news.fileformat.com/t/audio) bölümünde yayınlayabilirsiniz.

## WAV Dosya Biçimi ##

Microsoft'un RIFF spesifikasyonunun bir alt kümesi olan WAVE dosya formatı, bir dosya başlığı ve ardından bir dizi veri parçası ile başlar. Bir WAVE dosyası, iki alt parçadan oluşan tek bir "WAVE" yığınına sahiptir:

* bir "fmt" öbeği - veri formatını belirtir
* bir "veri" öbeği - gerçek örnek verileri içerir

### WAV Dosya Başlığı ###

Bir WAV (RIFF) dosyasının başlığı 44 bayt uzunluğundadır ve aşağıdaki biçime sahiptir:


|Pozisyonlar|Örnek Değer|Açıklama
---|---|---|
|1 - 4|"RIFF"|Dosyayı riff dosyası olarak işaretler. Karakterlerin her biri 1 bayt uzunluğundadır.
|5 - 8|Dosya boyutu (tamsayı)|Genel dosyanın boyutu - 8 bayt, bayt cinsinden (32 bit tam sayı). Genellikle, bunu oluşturduktan sonra doldurursunuz.
|9 -12|"WAVE"|Dosya Türü Başlığı. Bizim amaçlarımız için her zaman "WAVE" e eşittir.
|13-16|"fmt "|Biçim yığın işaretçisi. Sondaki null içerir
|17-20|16|Biçim verilerinin uzunluğu yukarıda listelendiği gibidir
|21-22|1|Biçim türü (1, PCM'dir) - 2 bayt tamsayı
|23-24|2|Kanal Sayısı - 2 bayt tamsayı
|25-28|44100|Örnek Hızı - 32 bayt tamsayı. Ortak değerler 44100 (CD), 48000'dir (DAT). Örnek Hızı = Saniyedeki Örnek Sayısı veya Hertz.
|29-32|176400|(Örnek Hızı * Örnek Başına Bit * Kanallar) / 8.
|33-34|4|(Örnek Başına Bit * Kanallar) / 8.1 - 8 bit mono2 - 8 bit stereo/16 bit mono4 - 16 bit stereo
|35-36|16|Örnek başına bit
|37-40|"veri"|"veri" yığın başlığı. Veri bölümünün başlangıcını işaretler.
|41-44|Dosya boyutu (veri)|Veri bölümünün boyutu.
|Örnek değerler yukarıda 16 bit stereo kaynak için verilmiştir.

## Referanslar ##

* [WAV - Wikipedia'dan](https://en.wikipedia.org/wiki/WAV)

