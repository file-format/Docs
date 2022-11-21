{
  "date" : "2021-06-09",
  "keywords" :[ "işaret", "dosya", "uzantı", "biçim", "işaret dosyası nedir", "müzik", "işaret dosyası formatı", "işaret dosyası formatı belirtimi", "işaret sayfası", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"CUE dosya formatı ve CUE dosyalarını oluşturabilen, dönüştürebilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"CUE - İşaret Sayfası Dosyası",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## CUE dosyası nedir?

Cue sayfası dosyası olarak da bilinen .cue uzantılı bir dosya, bir CD veya DVD'deki parçaların düzeni hakkında bilgi içeren bir meta veri dosyasıdır. Bunlar medya oynatıcılar ve optik disk yazma uygulamaları tarafından desteklenir. CD'de depolanan ana ses verilerine, parça uzunlukları, disk başlıkları ve sanatçıların özellikleriyle birlikte cue dosyası tarafından başvurulur. Bu nedenle, tek bir ses dosyası birden çok parça içeriyorsa, cue dosyası sesi birden fazla dosyaya bölmek veya çeşitli parçalara referans vermek için kullanılabilir.

## CUE Dosya Biçimi

CUE veya işaret sayfası dosyaları, insan tarafından okunabilen düz metin biçiminde saklanır. Bir işaret dosyasındaki bilgiler, bir veya daha fazla parametre içeren komutlardır. Bu komutlar, belirli komuta ve bağlama bağlı olarak ya tüm dosyaya ya da tek bir parçaya uygulanır. CDRWIN kullanıcı kılavuzu, işaret sayfası söz dizimi ve semantiği için belirtimleri açıklar.

## CUE Sayfası Temel Komutları

|Komut|Açıklama|
---|---|
|DOSYA| [MP3](/tr/audio/mp3/), [WAV](/tr/audio/wav/) veya düz ikili disk görüntüsü)| gibi verileri ve formatını içeren dosyayı ifade eder.
|PARÇA| Parçanın numarası, türü veya modu gibi içerik bilgilerini tanımlar.|
|DİZİN| DOSYA içinde bir dizin olarak konumu temsil eder. Biçim mm:ss:ff (dakika-saniye-kare) şeklindedir.|
|PREGAP ve POSTGAP|Bu, herhangi bir veri dosyasında saklanmayan bir parçanın boşluk öncesi veya sonrası boşluğunu gösterir. Uzunluk, INDEX ile aynı dakika-saniye-kare biçiminde belirtilir.|

### CUE Sayfası Örneği

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## Referanslar

* [.cda dosyası - Wikipedia tarafından](https://en.wikipedia.org/wiki/.cda_file)

