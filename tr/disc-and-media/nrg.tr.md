{
  "date" : "2021-08-16",
  "keywords" :[ "nrg dosyası", "nrg dosya biçimi", "nrg dosyası nedir", "dosya", "nrg örneği", "nrg dosya uzantısı","uzantı", "biçim", "nrg altbilgi", "dosya nrg biçimi", "Nero Burning Rom", "Nero AG" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"NRG dosya formatı ve NRG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"NRG - Disk Görüntüsü Dosya Biçimi",
  "linktitle" : "NRG",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-16"
}

## Bir NRG dosyası nedir?

Optik disk kullanılarak oluşturulan bir görüntü dosyası formatı, NRG dosya formatı olarak kabul edilir. Bu biçim, Nero Burning Rom'un kullanımı için Nero tarafından özel olarak oluşturulmuştur. Disk görüntülerinin saklanması için, bu belirli dosyalar için uygun olduğu için bu biçimin kullanıldığı kabul edilir. Bu dosyalar, bir CD veya DVD'nin tam bir kopyası biçiminde olabilir veya disk olarak takılabilen birkaç dosyaya sahip olabilir. [ISO](/tr/compression/iso/) dosya biçimleri gibi diğer daha popüler dosya biçimleri, bu dosyaların bazı temel yardımcı programlara dönüştürülebildiği biçimlerdir. Çoğunlukla, NRG dosyaları bazı önemli verilerin veya disklerin yedeklerini veya kopyalarını oluşturmak için kullanılır.

## NRG Dosya Biçimi ##

Bu dosya formatı, Nero AG tarafından bir disk görüntü formatı olarak geliştirilmiştir. Disk görüntülerini depolamak için geliştirildiğinden, Nero Burning Rom yardımcı programının özel özelliğine sahipti. İlk sürümü, değerleri 32 bitlik tamsayılar olarak depolamak için belirtildi. Ancak ikinci sürümü piyasaya sürüldü ve 64 bitlik tamsayılar için destek içeriyordu.

## Teknik özellik ##

Dosyanın başında, bu biçim verilerini bir başlık olarak saklamaz. Altbilgi gibi, dosyanın sonuna eklenir. Görüntünün bilgileri, IFF parçaları biçiminde depolanır. İlk yığının ofseti, dosyanın son 8 bayt ila 12 baytındaki NRG altbilgisi okunarak elde edilebilir. NRG dosya biçiminin tüm sürümlerinde, yığınlar, DAOI, CD metni, oturum bilgileri ortam türü, disk bilgileri, Relo ve bunlara bağlı zincirin sonu vardır. Bayt sırası big-endian'dır ve depolama sırasında tüm tamsayı değerleri işaretsizdir.

### Ana Parçalar ###

#### İşaret levhası ####

Bu işaret sayfası, tüm NRG dosya formatı sürümlerinde kolayca kullanılabilir. **CUEX** öbeği, sabit boyutlu birleştirme blokları anlamına gelir ve bunların her biri işaret noktasını temsil eder.

#### DAO Bilgileri ####

Bu bilgi aynı zamanda tüm NRG format sürümlerinde mevcuttur. **DAOI** parçaları, ilgili belirli bilgileri 2 kısımda saklar. İlk bölümü yalnızca oturuma özgü verilerden oluşur. İkinci kısmı ise sadece takip ile ilgili gri bilgiyi tekrar eder ve her parkur için sadece bir defadır.

#### CD metni ####

Bu, NRG'nin ikinci versiyonunda mevcuttur. **CDTX** yığını, her biri için 18 bayta sahip olan CD-metin paketinin ham birleştirmesinden oluşur.

#### Genişletilmiş İzleme Bilgileri ####

Bu, NRG dosya biçiminin her sürümünde mevcuttur. Bu parçalar, bir kerede oturum izlemesi için izleme bilgilerini depolamak için kullanılır. Bu veriler, her parça durumunda yalnızca bir kez tekrarlanır.

#### Oturum Bilgileri ####

Bu, NRG'nin dosya biçiminin her sürümünde de mevcuttur. Oturum parçalarının bilgilerinin, oturumun görüntüsünü hızlı bir şekilde taramak ve ardından iz sayısını belirlemek için kullanılması gerekir.

#### Zincirin sonu ####

Son parça, artık okunması gereken başka parça kalmadığına dair sinyaller anlamına gelir ve bu, NRG'nin tüm sürümlerinde de mevcuttur.


## Referanslar ##

* [NRG - Wikipedia'dan](https://en.wikipedia.org/wiki/NRG_(file_format))


