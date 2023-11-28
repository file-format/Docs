{
"tarih":"2023-10-18",
   "keywords":[
"isteka",
"işaret dosyası",
"cue cdrwin işaret sayfası dosyası",
"bir işaret dosyası nasıl açılır",
"dosya",
"cue dosya uzantısı",
"eklenti",
"dosya"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc": true,
"title":"CUE Dosya Formatı - CDRWIN Cue Sayfası",
   "description":"CUE CDRWIN Cue Sheet dosya formatı ve CUE dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"linktitle":"CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin",
         "parent":"disc-and-media"
}
},
"lastmod":"2023-10-18"
}

## .CUE dosyası nedir?

**CDRWIN Cue Sheet** olarak da bilinen **.CUE** dosyası, genellikle BIN veya ISO formatındaki bir ses CD'sinin veya disk görüntüsünün parçaları ve düzeni hakkında bilgi içeren düz metin dosyasıdır. Bu dosyalar genellikle diskin yapısını ve içeriğini tanımlamak için kullanılır ve CD yazma yazılımının veya sanal sürücü yazılımının orijinal diski doğru bir şekilde yeniden üretmesine olanak tanır.

## CUE dosyası örneği

Burada ".cue" dosyasının nasıl görünebileceğine dair bir örnek verilmiştir:

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## CDRWIN İşaret Sayfası

CDRWIN Cue Sheet, CDRWIN yazılımı tarafından kullanılan ".cue" dosya formatının özel bir çeşididir. CDRWIN, CD/DVD yazma ve yazma yazılımıdır ve ".cue" sayfaları bu yazılımla kullanılmak üzere tasarlanmıştır. Bu ".cue" sayfaları, CDRWIN'in CD veya DVD'yi doğru bir şekilde oluşturması veya yazması için gerekli bilgileri içerir.

CDRWIN İşaret Sayfalarına özel bazı önemli ayrıntılar şunlardır:

1. **CDRWIN'e özel**: CDRWIN'in ".cue" sayfaları, CDRWIN yazılımına özel tescilli formattır. Standart ".cue" dosyalarıyla benzerlikler taşısalar da, CDRWIN'in özellikleri ve ayarlarıyla çalışacak şekilde uyarlanmıştır.
    






2. **Kullanıcı Dostu Arayüz**: CDRWIN, ".cue" sayfalarını oluşturmak ve düzenlemek için kullanımı kolay bir arayüz sağlar. Kullanıcılar parçalar, indeksler, boşluklar ve diğer parametreler hakkındaki bilgileri kullanıcı dostu bir şekilde ekleyebilir veya değiştirebilir.
    






3. **Uyumlu Disk Türleri**: CDRWIN İşaret Sayfaları öncelikle veri diskleri, ses CD'leri, karma modlu diskler ve daha fazlası dahil olmak üzere çeşitli türde CD ve DVD'ler oluşturmak için kullanılır. Format, kullanıcıların oluşturmak istedikleri diskin türünü ve içeriğini belirtmelerine olanak tanır.
    






4. **Disk Düzeni Üzerinde Kontrol**: CDRWIN İşaret Sayfaları, parça sırası, duraklatma/boşluk ayarları ve kullanıcının sahip olabileceği diğer özel tercihler de dahil olmak üzere diskin düzeni ve yapısı üzerinde ayrıntılı kontrol sağlar.
    






5. **ISO ve BIN Desteği**: CDRWIN hem ISO hem de BIN disk görüntü formatlarıyla çalışabilir. ".cue" sayfası, disk için hangi görüntü dosyasının kullanılacağını belirtir ve ipuçları ile görüntü arasında uygun senkronizasyonun sağlanmasını sağlar.
    






6. **Yazma ve Kopyalama**: Bu ".cue" sayfaları, CDRWIN kullanarak diskleri yazarken veya disklerden parça kopyalarken çok önemlidir. Nihai ürünün amaçlanan düzen ve içerikle eşleşmesini sağlamaya yardımcı olurlar.
    






7. **Yedekleme ve Geri Yükleme**: CDRWIN kullanıcıları, CD veya DVD'lerinin yedeklerini alırken sıklıkla ".cue" sayfaları oluştururlar. Bu sayfalar daha sonra parça düzeni ve zamanlama da dahil olmak üzere disk içeriğini geri yüklemek için kullanılabilir.

## CUE dosyası nasıl açılır?

CDRWIN İşaret Sayfaları özellikle CDRWIN yazılımı için tasarlanmıştır, dolayısıyla genellikle CDRWIN içinde açılıp kullanılmaları amaçlanır.

CUE dosyalarını açan veya referans veren programlar

- CDRWIN
- Akıllı Projeler IsoBuster
- EZB Sistemleri UltraISO

## Diğer CUE dosyaları

**.cue** dosya uzantısını kullanan diğer dosya türleri şunlardır.

**Disk ve Medya**
- [CUE - İşaret Sayfası Dosyası](/tr/disc-and-media/cue/)
- [CUE - CDRWIN İşaret Sayfası](/tr/disc-and-media/cue-cdrwin/)

## Referanslar
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)

