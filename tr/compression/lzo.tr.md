{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "Sıkıştırılmış", "Dosya", "Uzantı", "Dosya Biçimi", "Lempel-Ziv-Oberhume" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZO Dosya Biçimi",
  "description":"LZO dosya formatı ve LZO dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## LZO dosyası nedir? ##

.lzo uzantılı bir dosya, sıkıştırılmış dosyadaki tüm dosyaların boyutunu küçültebilen dosya arşivleme özellikleriyle birleştirilmiştir. Tüm sıkıştırılmış dosyalar, bir veya daha fazla dosya veya hatta farklı tür ve boyutlarda birkaç dosya içeren bağlayıcı gruplarından oluşabilir. Sıkıştırılmış bir dosyanın boyutu, bir LZO sıkıştırılmış dosyasında saklanan tüm dosya ve klasörlerin ortak boyutuna kıyasla daha küçüktür. Tüm LZO sıkıştırılmış dosyaları, LZO formatında saklanır ve LZOP dosya sıkıştırma ve açma yazılımı tarafından kullanılan sıkıştırma özellikleriyle açıkça yürütülür. Tüm sıkıştırma özellikleri, Lempel-Ziv-Oberhume dosya sıkıştırma kitaplığından kaynaklanan bu dosya sıkıştırma ve açma programında birleştirilir. Daha hızlı açma hızı ve gelişmiş sıkıştırma oranları da bu LZO dosyalarında birleştirilmiştir.

## LZO Spesifikasyonu ##

Markus Franz Xaver Johannes Oberhumer, 1996'da Abraham Lempel ve Jacob Ziv'in önceki algoritmalarına dayanan orijinal "lzop" algoritmasını geliştirdi. Bu kitaplık, aşağıdaki özelliklere sahip çeşitli algoritmalar uygular:

* DEFLATE'ten daha hızlı sıkıştırma
* Hızlı dekompresyon
* Sıkıştırma sırasında ihtiyaç duyulan ek arabellekler (sıkıştırma düzeyine bağlı olarak 8KB veya 64KB boyutunda)
* Kaynak ve hedef arabellekleri, sıkıştırmayı açmak için gereken tüm bellektir
* Hem sıkıştırma oranı hem de sıkıştırma hızı üzerinde kontrol sağlar

Bir blok sıkıştırma algoritması olarak LZO, yerinde açmanın yanı sıra örtüşen sıkıştırma gerçekleştirir. Çakışan sıkıştırmayı elde etmek için hem sıkıştırmanın hem de sıkıştırmayı açmanın blok boyutu eşleşmelidir. LZO sıkıştırma algoritması, giriş verilerini eşleşmelere (kayan bir sözlük) ve eşleşmeyen hazır değerlere böler, yüksek oranda fazlalık verilerle iyi sonuçlar ve sıkıştırılamaz verilerle kabul edilebilir sonuçlar verir, yalnızca sıkıştırılamaz verileri orijinalin 1/64'ü oranında artırır boyut.

## Bir LZO dosyasını açma sorunları ##

Aşağıda, LZO dosya biçiminin kötü çalışmasına neden olabilecek birkaç sorun bulunmaktadır:
  


* Dosya bozuk olabilir. Bu sorunu çözmek için dosyayı yeniden indirin veya gönderenden dosyayı yeniden göndermesini isteyin
* İkinci neden virüslü dosyadır bu durumda dosyayı düzgün bir şekilde tarayın
* LZO dosyasına uygun olmayan bağlantılar
* LZO açıklamasının kaldırılması
* Yeterli donanım kaynağı yok
* Ekipmanın güncel olmayan sürücüleri
  


## Referanslar ##

* [LZO - Wikipedia'dan](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

