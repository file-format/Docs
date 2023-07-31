{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "dosya", "uzantı", "biçim", "ses değişim dosyası biçimi", "müzik"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"WMA dosya formatı ve WMA dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"WMA - Windows Medya Ses Dosyası",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## WMA dosyası nedir?

.wma uzantılı bir dosya, Gelişmiş Sistem Biçimi (ASF) biçiminde kaydedilen bir ses dosyasını temsil eder. ASF, Microsoft'un Windows Media Audio 9 tarafından kodlanan bit akışlarını içeren tescilli biçimidir. Ses içeriğine ek olarak, bir WMA dosyası parçanın başlığı, albümü, sanatçısı ve türü gibi meta veri nesnelerini de içerir. WMA dosyaları, [.mp3](/tr/audio/mp3/) dosyalarına benzer şekilde öncelikle web üzerinden akış için kullanılır.

## WMA Dosya Biçimi

Bir WMA dosyası, ikili dosya biçimidir ve ASF dosya biçiminde bulunur. MP3 dosyaları tarafından kullanılan ID3 etiketlerine benzer şekilde, dosya hakkındaki meta verilerin kodlanmasını belirtir. WMA codec bileşeni, Microsoft tarafından Korumalı Birlikte Çalışabilir Dosya Formatında (PIFF) 2008'den beri kullanılmaktadır. Ancak, DECE UltraViolet ve MPEG-DASH gibi ilgili endüstri standartları tarafından standartlaştırılmış ses codec bileşeni olarak beyan edilmemiştir.

### WMA Türüne Özgü Veriler

Windows Media Audio codec bileşeni için türe özgü bilgiler, Akış Özellikleri Nesnesinin Türe Özgü Verilerinin bir parçası olarak aşağıdaki biçimde depolanır.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Referanslar

* [ASF'ye Genel Bakış - Microsoft](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)

