{
  "date" : "2019-10-11",
  "keywords" :[ "tar dosyası", "tar dosyası formatı", "tar dosyası nedir", "dosya", "tar örneği", "tar dosyası uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TAR - Unix Arşiv Dosya Formatı",
  "description":"Tar dosyasının ne olduğunu ve TAR dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "TAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## TAR dosyası nedir?

.tar uzantılı dosyalar, bir veya daha fazla dosya toplamak için Unix tabanlı yardımcı programla oluşturulan arşivlerdir. Birden çok dosya, arşive dosya ve klasör ekleme desteğiyle sıkıştırılmamış bir biçimde saklanır. Unix'teki TAR yardımcı programı, Komut tabanlıdır, ancak bu şekilde oluşturulan dosyalar, neredeyse tüm işletim sistemlerindeki çoğu dosya arşivleme sistemi tarafından desteklenir. İlk olarak 1979'da AT&T Bell Laboratuvarları tarafından oluşturuldu ve sonraki sürümleri zaman geçtikçe yayınlandı.

## TAR Dosya Biçimi

TAR, geliştiricinin referansı için tüm özelliklere sahip açık bir dosya biçimidir. Dosya yapısı POSIX.1-1988'de ve daha sonra POSIX.1-2001'de standardize edilmiştir. tar tarafından oluşturulan veri kümeleri, dosya sistemi parametreleri hakkında aşağıdakiler gibi bilgileri tutar:

* İsim
* Zaman Damgaları
* Mülkiyet
* Dosya Erişim İzinleri
* Dizin Organizasyonu

Bir Tar dosyasının herhangi bir sihirli numarası yoktur. Her bloğun BLOCKSIZE bayt olduğu bir dizi blok içerir.

Arşivlenen her dosya, dosyayı tanımlayan bir başlık bloğu ve ardından dosyanın içeriğini veren sıfır veya daha fazla blok ile temsil edilir. Arşiv dosyasının sonunda, dosya sonu işaretçisi olarak ikili sıfırlarla doldurulmuş iki adet 512 baytlık blok vardır. Makul bir sistem, bir arşivin sonuna böyle bir dosya sonu işaretçisi yazmalıdır, ancak bir arşivi okurken böyle bir bloğun var olduğunu varsaymamalıdır. Özellikle GNU tar, karşılaşmazsa her zaman bir uyarı verir.

Bloklar, fiziksel G/Ç işlemleri için bloke edilmiş olabilir. n bloğun her kaydı (burada n, engelleme faktörü = 512-size seçeneği tarafından tar olarak ayarlanır) tek bir "write()" işlemiyle yazılır. Manyetik bantlarda, böyle bir yazmanın sonucu tek bir kayıttır. Bir arşiv yazarken, blokların son kaydı tam boyutta, sıfır bloğundan sonra tüm sıfırları içeren bloklarla yazılmalıdır. Bir arşivi okurken, makul bir sistem, son kaydı diğerlerinden daha kısa olan veya sıfır bloğundan sonra çöp kayıtları içeren bir arşivi uygun şekilde ele almalıdır.

### Katran Başlığı

Diğer dosya başlıkları gibi, tar dosyası başlık kaydı da bir dosya hakkında meta veriler içerir ve aşağıdaki tabloda gösterilir.


|Alan ofseti|Alan boyutu (Bayt)|Alan
---|---|---|
|0|100|Dosya adı
|100|8|Dosya modu
|108|8|Sahibin sayısal kullanıcı kimliği
|116|8|Grubun sayısal kullanıcı kimliği
|124|12|Bayt cinsinden dosya boyutu (sekizlik taban)
|136|12|Sayısal Unix saat biçiminde (sekizlik) son değişiklik zamanı
|148|8|Başlık kaydı için sağlama toplamı
|156|1|Bağlantı göstergesi (dosya türü)
|157|100|Bağlantılı dosyanın adı

Kullanılmayan alanlar NUL baytlarıyla doldurulur. Bir başlık, 512 baytlık kaydı doldurmak için NUL baytlarıyla doldurulmuş 257 bayttan oluşur.

## Referanslar ##

* [TAR - Wikipedia Tarafından](https://en.wikipedia.org/wiki/Tar_(computing))
* [TAR Temel Biçim](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

