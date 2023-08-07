{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - Java Manifest Dosya Biçimi",
  "description":"MF dosya formatı ve MF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## .ff dosyası nedir?

.mf uzantılı bir dosya, ayrı ayrı [JAR](/tr/programming/jar/) dosya girişleri hakkında bilgi içeren bir Java Manifest dosyasıdır. MF dosyasının kendisi JAR dosyasının içinde bulunur ve tüm uzantı ve paketle ilgili tanımı sağlar. JAR dosyaları yürütülebilir bir dosya olarak kullanılmak üzere üretilebilir. Böyle bir durumda, mainfest dosyası **`public static void main`** ifadesini içeren uygulamanın ana sınıfını belirtir. Manifest dosyaları MANIFEST.MF olarak adlandırılır ve Windows, MacOS ve Linux İşletim Sistemlerinde herhangi bir metin düzenleyici ile açılabilir.

## Manifest Dosya Formatı Spesifikasyonları

[Belirtilen dosya biçimi belirtimleri](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html), Oracle'ın JAR dosya biçimi kılavuzlarında mevcuttur. Bir Manifest dosyası, ayrı JAR dosyası girişleri için bölümlerin bir listesinin takip ettiği ana bölümlerden oluşur. Her bölüm bazı kurallara ve kısıtlamalara uyar.

### Ana Bölümler

Bir ana bölüm:

* JAR dosyası hakkında güvenlik ve yapılandırma hakkında bilgi içerir
* JAR dosyasının parçası olduğu uygulama veya uzantı hakkında bilgi içerir
* her bir bildirim öğesi için ana nitelikleri tanımlar

**Not**: Bu bölümdeki hiçbir öznitelik "Ad" olarak adlandırılamaz.

### Bireysel Bölümler

Ayrı bir bölüm, bir JAR dosyasının paketleri veya dosyaları için çeşitli öznitelikleri tanımlar. Her bölüm, değeri dosyaya göreli bir yol veya arşiv dışındaki verilere başvuran mutlak bir URL olması gereken "Ad" adlı bir öznitelikle başlamalıdır.

### Manifest Spesifikasyonları

|Öznitelikler|Açıklama|
---|---|
|manifest-file|ana-bölüm yeni satır *bireysel-bölüm|
|ana-bölüm|sürüm bilgisi yeni satır *ana-öznitelik|
|sürüm-bilgisi|Belirtilen-Sürüm : sürüm-numarası|
|sürüm numarası|rakam+{.hane+}*|
|ana öznitelik|(herhangi bir geçerli ana öznitelik) yeni satır|
|bireysel-bölüm|Ad : değer yeni satır *perentry-attribute|
|perentry-attribute|(herhangi bir geçerli perentry niteliği) newline|
|yeni satır|CR LF | LF | CR (ardından LF gelmez)|
|rakam|{0-9}|

## Referanslar

* [Oracle - JAR Dosya Biçimi](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [JAR Dosya Biçimi](https://en.wikipedia.org/wiki/JAR_(file_format))

