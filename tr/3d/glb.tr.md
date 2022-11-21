{
  "date" : "2019-12-03",
  "keywords" :[ "GLB","dosya", "biçim", "dosya türü", "uzantı","GLB dosyası nedir?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GLB",
  "description":"GLB dosya formatı ve GLB dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## .glb dosyası nedir?

GLB, GL İletim Biçiminde ([glTF](/tr/3d/gltf/)) kaydedilen 3B modellerin ikili dosya biçimi temsilidir. Düğüm hiyerarşisi, kameralar, malzemeler, animasyonlar ve kafesler gibi 3B modeller hakkında ikili formatta bilgiler. Bu ikili biçim, glTF varlığını (JSON, .bin ve resimler) bir ikili blob içinde depolar. Ayrıca, glTF durumunda meydana gelen dosya boyutunun artması sorununu da ortadan kaldırır. GLB dosya biçimi, kompakt dosya boyutları, hızlı yükleme, eksiksiz 3B sahne gösterimi ve daha fazla geliştirme için genişletilebilirlik sağlar. Biçim, MIME türü olarak model/gltf-binary kullanır.

## GLB Dosya Biçimi - Daha Fazla Bilgi

glTF tarafından kullanılan içerik dağıtım yöntemleri, base-64 kodlu ikili verilerin kodunu çözmek için fazladan işlem yapılmasına neden olur ve ayrıca dosya boyutunu %33 oranında artırır. GLB dosya biçiminin oluşumuna katkıda bulunan bu dağıtım yöntemleri şunları içerir:

* glTF JSON, harici ikili verilere (geometri, anahtar çerçeveler, dış görünümler) ve görüntülere işaret eder.
* glTF JSON, veri URI'lerini kullanarak base64 kodlu ikili verileri ve görüntüleri satır içine yerleştirir.

Bir konteyner formatı olarak GLB, glTF'nin neden olduğu sorunları önlemek için glTF varlığının bir ikili blob içinde temsili için ikili dosya formatı olarak tanıtıldı. GLB dosya formatı [özellikler](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#glb-file-format-specification), uygulama geliştirme için herhangi bir okuyucu/yazıcı uygulamasında belirtilmelidir. .

## GLB Dosya Yapısı

GLB dosya biçimi küçük endian'a dayalıdır ve yapısı şunları içerdiğini gösterir:

* Başlık başlıklı 12 baytlık bir önsöz.
* JSON içeriğini ve ikili verileri içeren bir veya daha fazla parça.

#### GLB Başlığı

GLB dosya formatı başlığı, üç adet 4 baytlık girişten oluşur:

* uint32 büyüsü - büyü, 0x46546C67'ye eşittir. ASCII string glTF'dir ve verileri Binary glTF olarak tanımlamak için kullanılabilir.
* uint32 sürümü - İkili glTF kapsayıcı biçiminin sürümünü gösterir
* uin32 uzunluk - Başlık ve bayt cinsinden tüm parçalar dahil Binary glTF'nin toplam uzunluğu

#### parçalar

Bir GLB dosyasındaki her öbek aşağıdaki yapıya sahiptir:

|uint32|uint32|ubayt[]
---|---|---|
|yığınUzunluğu|yığınTürü|yığınVeri

* `chunkLength` - bayt cinsinden chunkData uzunluğu
* `chunkType` - yığın tipini belirtir
* `chunkData` - parçanın ikili yükü

öbek türleri nerede:

|# |Yığın Türü|ASCII|Açıklama|Oluşmalar
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Yapılandırılmış JSON içeriği|1
|2.|0x004E4942|BIN|İkili tampon|0 veya 1

Her parçanın başı ve sonu 4 baytlık sınıra hizalanmalı ve bu amaçla dolgu kullanılmalıdır.

##### Yapılandırılmış JSON İçeriği

Bu, Binary glTF varlığının ilk parçası olmalıdır ve uygulamanın sonraki parçalardan aşamalı olarak kaynak almasını sağlar. Bu ayrıca, bir ağın en kaba LOD'si gibi bir Binary glTF varlığından yalnızca seçilen bir kaynak alt kümesini okuma yeteneği sağlar. Hizalama gereksinimlerini karşılamak için bu yığın, sonundaki Boşluk karakterleri (0x20) ile doldurulmalıdır.

##### İkili Tampon #####

Bu öbek, geometri, animasyon anahtar çerçeveleri, dış görünümler ve resimler için ikili yükü içerir. İkili glTF varlığının ikinci öbeği olmalı ve hizalama gereksinimlerini karşılamak için sondaki sıfırlarla (0x00) doldurulmalıdır.

## Referanslar ##

* [GLB Dosya Biçimi Özellikleri - Khronos](/tr/3D/GLTF/)

