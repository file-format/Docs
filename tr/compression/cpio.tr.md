{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPIO Dosyası - Unix CPIO Arşiv Dosya Formatı",
  "description":"CPIO dosyasının ne olduğunu ve CPIO dosyalarını oluşturup açabilen API'leri öğrenin.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## CPIO dosyası nedir?

CPIO dosyası, Unix'in Kopyalama Girişi Kopyalama (CPIO) formatında oluşturulan bir arşiv dosyasıdır. Sıkıştırılmamış olması dışında TAR dosya formatına benzer. CPIO dosyaları aygıt dosyalarını, sembolik bağlantıları ve genişletilmiş dosya niteliklerini saklayabilir.

## CPIO Dosya Formatı

Bir CPIO arşivi, insan tarafından okunamayan bir ikili dosya olarak oluşturulur. Dosya ve dizin koleksiyonunu saklar. Bir CPIO arşivinin içeriği, dosya adları, izinler, sahiplik ve zaman damgaları gibi meta veri bilgileriyle tanımlanır. Bu metadata bilgisi aynı zamanda sistemin yandan erişimi için arşiv dosyasında da saklanır.

## CPIO Arşivi Formatı

Bir CPIO dosyası bir veya daha fazla birleştirilmiş üye dosyasından oluşur. Arşivdeki her dosya, isteğe bağlı olarak bir başlıktan ve başlıkta belirtildiği gibi dosya içeriklerinden oluşur. Arşivin sonunda TRAILER!! adlı boş bir dosya tarafından açıklanan başka bir başlık bulunmaktadır.

### CPIO Arşivi Türleri

İki tür CPIO arşivi vardır. Bunlar yalnızca başlığın tarzında farklılık gösterir.

* ASCII Arşivleri - Bu CPIO arşivleri, arşivin kendisi ASCII dosyalarından oluşuyorsa CPIO arşivinin parçası haline gelen yazdırılabilir bir başlığa sahiptir.
* İkili Arşivler - Bu CPIO arşivlerinin ikili başlıkları vardır.

## CPIO Arşivi'yle Çalışmak

### CPIO Arşivleri Nasıl Oluşturulur?

**cpio** komutunu kullanarak Unix benzeri sistemlerde bir CPIO oluşturabilirsiniz. Aşağıdaki komut geçerli bir dizindeki ve onun alt dizinlerindeki tüm dosyaları ve dizinleri bulacaktır. Bu çıktı daha sonra archive.cpio adında yeni bir CPIO arşivi oluşturacak olan cpio komutuna iletilir.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### CPIO Arşivlerinden Dosyalar Nasıl Çıkarılır?

Aşağıdaki komut, dosyaları mevcut bir arşivden çıkarır.

```
cpio -id < archive_cpio.cpio
```
Standart girdiden archive.cpio dosyasını okuyacak ve dosyaları geçerli dizine çıkaracaktır.


## Referanslar

* [CPIO - Wikipedia'ya göre](https://en.wikipedia.org/wiki/Cpio)
* [CPIO Dosya Biçimi](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

