{
  "date" : "2019-10-11",
  "keywords" :[ "rar dosyası", "rar dosyası biçimi", "rar dosyası nedir", "dosya", "rar örneği", "rar dosyası uzantısı","uzantı", "biçimi"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RAR",
  "description":"RAR dosyaları oluşturabilen ve açabilen RAR dosya uzantısı ve API'ler nedir?",
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## RAR dosyası nedir?

.rar uzantılı dosyalar, bilgilerin sıkıştırılmış veya normal biçimde saklanması için oluşturulan arşiv dosyalarıdır. Roshal ARchive dosya formatı anlamına gelen RAR, 1995 yılında bir Rus yazılım mühendisi olan Eugene Roshal tarafından oluşturulan tescilli bir dosya formatıdır. Biçim, çeşitli sıkıştırma teknikleri dahil olmak üzere farklı yöntemlerle dosyaları arşivlemek için kullanılır. RAR dosyalarının ayıklanması için Windows, Linux ve MacOS için çeşitli uygulama yazılımları mevcuttur. RARLab tarafından sağlanan WinRAR yazılımı, Microsoft Windows platformu için paylaşılan yazılım dosya arşivleme yardımcı programıdır (40 gün boyunca ücretsiz); yazılım, aynı Yazar Eugene Roshal tarafından Linux'a taşındı (yalnızca çıkarıcı olarak).

## Sürümler RAR Dosya Biçiminin Geçmişi

* v1.3 (orijinal, "Rar!" imzası yok)
* v1.5
* v2.0 - MS-DOS 2.0 için WinRAR 2.0 ve Rar ile yayınlandı
* v2.9 - WinRAR sürüm 3.00'de yayınlandı
* v5.0 - WinRAR 5.0 ve sonrası tarafından desteklenir

## RAR Formatının Temel Özellikleri

RAR oldukça uzun süredir bu alanda ve favori arşivleme dosya formatlarından biri olmuştur. RAR formatıyla ilgili temel özellikler şunlardır:

**`Yüksek sıkıştırma oranı:`** [ZIP](/tr/compression/zip/) ile karşılaştırıldığında üstün, 7z ve zipx formatıyla karşılaştırılabilir.

**`Tasarım gereği güçlü dosya şifreleme:`** Şifreli RAR4 arşivleri, AES-128 tabanlı şifrelemeye dayanırken, şifreli RAR5 arşivleri, geliştirilmiş anahtar programlama ile AES-256 şifrelemeye dayanır

**`Gelişmiş hata düzeltme ve veri kurtarma özellikleri:`** arşiv oluşturma sırasında isteğe bağlı kurtarma kayıtları

**`Dosya Boyutu:`** Boyut olarak minimum 20 bayt ve maksimum 2^63 bayt (arşivin toplam boyutunun 8 eksabaytı)

**`Çok ciltli RAR Arşivleri:`** Ağ üzerinden aktarımı kolaylaştırmak için büyük arşivleri birkaç küçük dosyaya bölme imkanı. Böyle bir durumda, dosya uzantıları bölünmüş hacimleri temsil edecek şekilde 1 artırılır.

## RAR Dosya Biçimi

RAR formatının tam özellikleri halka açık değildir ve bu nedenle formatla ilgili ayrıntılar kısa ve öz bir şekilde formüle edilemez.

### Genel Arşiv Düzeni

5.0 sürümünde tanıtılan bir RAR dosya formatının genel düzeni aşağıdaki gibidir:

|Dosya Formatı
---|
|Kendiliğinden açılan modül (isteğe bağlı)
|RAR 5.0 İmzası
|Arşiv Şifreleme Başlığı (isteğe bağlı)
|Ana Arşiv Başlığı
|Arşiv yorum hizmeti başlığı (isteğe bağlı)
Dosya Başlığı 1
|Önceki dosya için Hizmet Başlıkları (NTFS ACL, akışlar, vb.) (isteğe bağlı)
|...
|Dosya Başlığı N
|Önceki dosya için Hizmet Başlıkları (NTFS ACL, akışlar, vb.) (isteğe bağlı)
|Kurtarma Kaydı (isteğe bağlı)
|Arşiv başlığının sonu

Yukarıda belirtilen RAR dosyasının her bir bölümü hakkında bilgi [RAR 5.0 Dosya Biçimi özellikleri](https://www.rarlab.com/technote.htm#arcstruct) belgesinde bulunabilir.

#### Kendiliğinden Açılan RAR Arşivleri

RAR dosyasının kendisi kendi kendine açılıyorsa, kendi kendine açılan bilgi dosyanın başında arşiv imzasından önce yer alır. Boyutu ve içeriği tanımlanmamıştır.

#### RAR 5.0 İmzası

RAR imzası, aşağıdaki sihirli sayıdan oluşan 8 baytlık bir başlıktır:

0x 52 61 72 21 1A 07 00

nerede

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## Referanslar

* [RAR 5.0 Arşiv Formatı](https://www.rarlab.com/technote.htm)
* [RAR - Wikipedia Tarafından](https://en.wikipedia.org/wiki/RAR_(file_format))

