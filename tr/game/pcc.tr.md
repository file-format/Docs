{
  "date" : "2021-09-08",
  "keywords" :[ "pcc dosyası", "pcc dosya biçimi", "pcc dosyası nedir", "dosya", "pcc örneği", "pcc dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Mass Effect PCC dosya formatı ve PCC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"PCC - Mass Effect Paket Dosyası",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## PCC dosyası nedir?

.pcc içeren bir dosya, modeller, dokular gibi oyun içeriğini değiştirmek için oyun verilerini içeren bir [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) dosyasıdır. Odalar. Mass Effect 2 ve 3, Unreal Engine 3 oyun motorunu temel alan ilk nişancı oyunlarıdır. Oyun başlangıçta, oyun kaynaklarının çoğunu kendi özel PCC dosya biçiminde tutan [Bioware](https://www.bioware.com/about/) tarafından geliştirildi. Bioware, önde gelen bir küresel interaktif eğlence yayıncısı olan Electronic Arts tarafından satın alındı.

## PCC Dosya Biçimi - Daha Fazla Bilgi

PCC dosyaları, genel dosya organizasyonuna katkıda bulunan sıkıştırılmış ve/veya sıkıştırılmamış yapılar içerir.

### Sıkıştırılmış PCC Yapısı

Sıkıştırılmış bir PCC dosyası, parçalara bölünmüş tablolardan ve verilerden oluşur. Her yığın, değişken sayıda sıkıştırılmış blok içerir.

* 'Parçalar Başlığı' - Parçalar hakkında bilgi içeren 16 baytlık bir ortak başlık.
* `Yığın Başlığı` - Blok formunda yer alan ham sıkıştırılmış veriler hakkında bilgi içeren 16 baytlık bir başlık.

### Sıkıştırılmamış PCC Yapısı

Sıkıştırılmamış PCC dosyaları aşağıdaki beş bölüme ayrılmıştır.

* `Başlık` - PCC dosyasının yapısı hakkında temel bilgileri içerir.
* 'Ad Tablosu' - içe aktarma sınıfları, dışa aktarma ve dışa aktarma özellikleri dahil olmak üzere paketin içinde bulunan adı içerir.
* `Tabloyu İçe Aktar' - PCC tarafından içe aktarılan tüm sınıfları ve nesneleri içerir.
* 'Tabloyu Dışa Aktar' - pakette saklanan tüm nesneleri içerir. Her dışa aktarmanın boyutu değişebilir.

## Referanslar

* [Me3Explorer - PCC Dosya Biçimi](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [Kitle Etkisi Oyunu](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)

