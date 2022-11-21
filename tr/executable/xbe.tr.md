{
  "date" : "2021-08-31",
  "keywords" :[ "xbe dosyası", "xbe dosya biçimi", "xbe dosyası nedir", "dosya", "xbe örneği", "xbe dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"XBE dosya formatı ve XBE dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"XBE - iOS Uygulama Paket Dosyası",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## XBE dosyası nedir?
.xbe uzantısına sahip bir dosya, bir Xbox video oyun diskinden yürütülebilir bir uygulamadır. XBE dosyaları, Xbox Sisteminde yürütülen ve tipik olarak bir bilgisayarda açılmaması gereken ana dosyalardır, ancak bir Xbox emülasyon programı kullanılarak bir PC'de açılabilir. Bu dosyalar genellikle oyun geliştiricileri tarafından oluşturulur ve ardından Microsoft tarafından imzalanır. Dosya yapısı Windows PE dosyalarına benzer, ancak XBox'ta çalıştırılabilir hale getirmek için XBox ayarlarına göre bazı önemli değişiklikler uygulanır.

## XBE dosya formatı
XBE dosyası, bir görüntü başlığından, bir bölüm başlıkları koleksiyonundan, bir sertifikadan, iş parçacığı yerel depolama verisinden, bir kitaplık sürümleri koleksiyonundan, Microsoft bitmap'ten ve kod ile kaynakları içeren bölümlerden oluşur.

### Resim Başlığı
Görüntü başlığı, yürütülebilir dosyanın diğer bileşenlerinin dosya içinde nerede bulunduğunu ve çalıştırılabilir dosyanın nasıl ele alınması ve yüklenmesi gerektiğini açıklayan bilgileri içerir.

### TLS Tablosu
TLS Tablosu, iş parçacığı yerel depolamayı uygun şekilde ayarlamak için XBE'nin ihtiyaç duyduğu tüm bilgileri içerir. Temelde PE32 dosyalarında bulunan TLS Dizinine özgüdür ve oradan doğrudan kopyalanabilir. XBE dosyası herhangi bir iş parçacığı yerel depolama kullanmıyorsa ve görüntü başlığındaki ilgili alan sıfıra ayarlanmışsa, bu tablo atlanabilir.

| Ofset | Boyut | Ad | Açıklama |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Ham Veri Başlat | Program görüntüsündeki TLS değişken verilerinin başlangıcının mutlak (yani bir RVA değil) adresi. |
| 0x0004 | 0x0004 | Ham Veri Sonu | Program görüntüsündeki TLS değişken verilerinin sonunun mutlak (yani bir RVA değil) adresi. |
| 0x0008 | 0x0004 | İndeks Adresi | TLS İndeks değişkeninin mutlak (yani bir RVA değil) adresi. |
| 0x000C | 0x0004 | Geri Aramaların Adresi | Boş sonlandırılmış TLS geri arama işlevleri tablosunun mutlak (yani bir RVA değil) adresi. |
| 0x0010 | 0x0004 | Sıfır Dolgunun Boyutu | Bellekte sıfıra ayarlanması gereken ham verileri takip eden bayt sayısı. |
| 0x0014 | 0x0004 | Özellikler | Hizalamayı açıklar. |

### Sertifika

Şu başlıklar hakkında bilgi içeren her Xbox yürütülebilir dosyası için bir sertifika zorunludur:
 


- Sertifikanın oluşturulduğu saat ve tarih
- Başlık Kimliği
- Başlık adı
- Alternatif başlık kimlikleri
- Yürütülebilir dosyanın çalıştırılabileceği izin verilen ortam türleri (HD, DVD, CD, vb.)
- Oyun bölgesi
- Oyun derecelendirmeleri
- Disk numarası
- Sürüm
- System Link için kullanılan LAN anahtarı ham verileri
- İmza anahtarı ham verileri (kaydedilmiş oyunları imzalamak için kullanılır)
- Alternatif imza anahtarları
- Sertifikanın orijinal boyutu
- Çevrimiçi hizmet adı (ilk yürütülebilir dosyalarda yoktur)
- Çalışma zamanı güvenlik bayrakları (ilk yürütülebilir dosyalarda mevcut değildir)
 


### İzin verilen ortam türleri
Yürütülebilir dosya tarafından çalıştırılmasına izin verilen ortam türleri. Aşağıdaki değerler bilinmektedir:
| Medya türü | Değer |
---------------------|------------|
| HARD_DISK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDYA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDYA_MASK | 0x00FFFFFF |

### Bölümler
Bölümler, bölüm başlıkları ile ifade edilir. Bölüm başlıkları, sertifikadan hemen sonra başlar ve dosyada gerçek bölümlerin bulunduğu yerde bilgi içerir. Bir Xbox yürütülebilir dosyasında her zaman en az iki bölüm bulunur:


- .Metin


- .rdata


## Referanslar



* [Xbe - XBox Çalıştırılabilir](https://xboxdevwiki.net/Xbe)


