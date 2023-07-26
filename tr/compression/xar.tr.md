{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - Genişletilebilir Arşiv Dosyası Formatı",
  "description":"XAR dosya formatı ve XAR dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## XAR dosyası nedir?

.xar (Genişletilebilir Arşiv Biçimi) uzantılı bir dosya, sıkıştırılmış veya sıkıştırılmamış biçimde olabilen bir UNIX arşividir. Paketlerin kurulumu için Mac OS'de de kullanılır. XAR açık kaynaklıdır ve Safari tarayıcısı ile kullanım için Mac OS X 10.5'in bir parçasıdır.

## XAR Dosya Biçimi

Bir [XAR](https://github.com/mackyle/xar/wiki/xarformat) dosyasının üç ana bölgesi vardır.

* Başlık
* İçindekiler
* yığın

### XAR Başlığı

XAR başlığı aşağıdaki gibi yapılandırılmıştır.

|Alan|Veri Türü|Bayt Olarak Boyut|
---|---|---|
|Sihir|İmzasız Int 32|4|
|Boyut|İmzasız Int 16|2|
|Sürüm|İmzasız Int 16|2|
|TOC Uzunluğu Sıkıştırılmış|İmzasız Int 64|8|
|TOC Uzunluğu Sıkıştırılmamış|İşaretsiz Int 64|8|
|Sağlama|İmzasız Int 32|4|
|Mesaj Özeti Adı |Null Sonlandı||

XAR başlığının C yapısı aşağıdaki gibi tanımlanabilir.
```
struct xar_header {
    uint32_t magic;
    uint16_t size;
    uint16_t version;
    uint64_t toc_length_compressed;
    uint64_t toc_length_uncompressed;
    uint32_t cksum_alg;
    /* A nul-terminated, zero-padded to multiple of 4, message digest name
     * appears here if cksum_alg is 3 which must not be empty ("") or "none".
     */
};
```
Başlığın tüm alanlarının (sihir, boyut, sürüm, toc_length_compressed, toc_length_uncompressed, cksum_alg) her zaman XAR dosyalarında ağ baytı (diğer adıyla big endian) düzeninde depolandığını unutmayın.

### XAR İçindekiler Tablosu (TOC)

İçindekiler tablosu, UTF-8 olarak kodlanmış (ve kodlanması gereken) bir XML belgesidir. Dosyanın başında saklanır, bu da tek tek dosyaları ayıklamak için arşivi taramayı kolaylaştırır. XAR arşivi, [GZIP](/tr/compression/gz/), [BZIP2](/tr/compression/bz2/) ve diğer benzerleri gibi farklı sıkıştırma düzenlerini kullanarak arşivdeki tek tek dosyaları bağımsız olarak sıkıştırmanıza/kodlamanıza olanak tanır.

```
<?xml version="1.0"?>

<xar>
  <toc>
    <checksum style="sha1">
      <size>20</size>
      <offset>0</offset>
    </checksum>
    <file id="1">
      <name>xar</name>
      <type>file</type>
      <mode>0755</mode>
      <uid>0</uid>
      <gid>0</gid>
      <user>root</user>
      <group>wheel</group>
      <size>81180</size>
      <data>
        <offset>0</offset>
        <size>74108</size>
        <length>23083</length>
        <extracted-checksum style="md5">d852c77ac3c8e83f312c12b4c3198e6d</checksum>
        <archived-checksum style="md5">ceaf793ccb1990ecbadb20112d5f9e5d</checksum>
        <encoding style="application/x-gzip"/>
      </data>
      <ea>
        <name>com.apple.ResourceFork</name>
        <offset>0</offset>
        <size>7072</size>
        <length>3942</length>
        <extracted-checksum style="md5">0f7061dca2d7411352377db0e53792db</checksum>
        <archived-checksum style="md5">c72de8ac25abe462a930254d82958534</checksum>
        <encoding style="application/x-gzip"/>
      </ea>
    </file>
  </toc>
</xar>
```

### yığın

Yığın, sıkıştırılmış toc'tan hemen sonra başlar. İçindekiler tarafından başvurulan yapılandırılmamış bir veri yığınıdır. TOC'de listelenen Ofset değerleri yığının başından başlar. toc'daki uzunluk değerleri öbekte depolanan (sıkıştırılmış veya sıkıştırılmamış) gerçek bayt sayısını ifade ederken, boyut değeri öğenin çıkarılan boyutunu (gerekirse sıkıştırmayı açtıktan sonra) ifade eder.

## Referanslar

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))

