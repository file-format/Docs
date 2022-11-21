{
  "date" : "2019-10-11",
  "keywords" :[ "obj dosyası", "obj dosya biçimi", "obj dosyası nedir", "dosya", "obj örneği", "obj dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBJ Dosya Biçimi",
  "description":"OBJ dosya formatı ve OBJ dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## OBJ Dosyası Nedir?

**OBJ** dosyaları, geometrik nesneleri tanımlamak ve depolamak için Wavefront'un Advanced Visualizer uygulaması tarafından kullanılır. Geometrik verilerin geriye ve ileriye iletimi OBJ dosyaları aracılığıyla mümkün olmaktadır. Noktalar, çizgiler, doku tepe noktaları, yüzler gibi çokgen geometri ve serbest biçimli geometri (eğriler ve yüzeyler) OBJ formatı tarafından desteklenir. Bu biçim, sahnelerin ışığı ve konumuyla ilgili animasyonları veya bilgileri desteklemez.

Bir OBJ dosyası, genellikle bir CAD (Bilgisayar Destekli Tasarım) tarafından oluşturulan 3B modelleme sürecinin son ürünüdür. Köşeleri saklamak için varsayılan sıra, yüz normallerinin açık bir şekilde bildirilmesinden kaçınarak saat yönünün tersinedir. OBJ dosyaları ölçek bilgisini bir yorum satırında bildiriyor olsa da henüz OBJ koordinatları için herhangi bir birim bildirilmemiştir.

## 3D OBJ Formatının Tarihçesi

Wavefront Technologies, Geometrik nesneleri ve 3B verileri depolamak için Advanced Visualizer uygulaması için OBJ dosya formatı oluşturdu. Sürüm 2.11'in yerini yeni belgelenmiş sürüm 3 almıştır. Dosya formatı açıktır ve diğer satıcılar tarafından 3B grafik uygulamaları için uygulanmıştır. Wavefront Technologies, bu dosya biçimini açık kaynak ve tarafsız tuttu.

## OBJ Dosya Biçimi

3B nesnelerde, yüzey geometrisini kodlamak, OBJ dosya formatının çok iyi başardığı zorlu bir iştir. Bu biçim, yüzey geometrisini kodlamak için bir dizi seçenek sunduğundan oldukça çok yönlüdür. Aşağıda, kendi yararları ve eksiklikleri olan izin verilen üç biçim verilmiştir:

### Çokgen Yüzeyli Mozaik

OBJ dosya formatı, kullanıcının basit veya karmaşık geometrik şekiller kullanarak bir 3B model yüzeyini döşemesini kolaylaştırır. Bir modelin yüzey geometri kodlaması için, bir dosya köşeleri ve her çokgenin normalini saklar. Mozaikleme modelin kabalığını artırsa da, yine de bir dosyanın boyutu ile baskı kalitesi arasında doğru dengeyi bulmak gerekir.

### Serbest Biçimli Eğri

OBJ dosya formatı, kullanıcı tanımlı serbest biçimli yüzey eğrilerinin bir modelin yüzey geometrisini belirlemesine olanak tanır. Serbest biçimli eğriler çokgen yüzlerden daha karmaşık olduğundan, birkaç matematiksel parametreyle eğri çizgiler en iyi şekilde serbest biçimli eğrilerle tanımlanabilir. Bu nedenle, dosya boyutunu genişletmeden herhangi bir 3D modelin yüksek kaliteli kodlamasını oluşturmak için poligonal mozaiklere kıyasla daha az veriyle serbest biçimli eğriler kullanılır.

### Serbest Biçimli Yüzeyler

OBJ dosya formatı, serbest biçimli yüzey yamaları ile yüzey geometrisinin döşenmesini de belirtir. Bu tür serbest biçimli yüzey yamaları (NURBS), bir kamyonun gövdesi, helikopterin kanatları veya bir teknenin gövdesi gibi katı radyal boyutları olmayan yüzeyler için çok uygundur. Serbest biçimli yüzeylerin kullanımı, dosya boyutlarını daha yüksek hassasiyette daha küçük tutmak için daha kesin oldukları için çok avantajlıdır. Bu yüzeyler, düşük hassasiyetin affetmez olduğu havacılık ve uzay ve otomotiv endüstrisinin önemli bir parçasıdır.

Aşağıdaki anahtar kelimeler, yüzey geometrisini tanımlamak için veri tipine göre düzenlenmiştir.


|Öğeler|Serbest biçimli eğri/yüzey gövdesi ifadeleri|Serbest biçimli eğri/yüzey nitelikleri
---|---|---|
|p|Nokta|parm|Parametre değerleri|derece|Derece
|l|Çizgi|kırpma|Dış düzeltme halkası|bmat|Temel matris
|f|Yüz|delik|İç düzeltme halkası|adım|Adım boyutu
|curv|Eğri|scrv|Özel eğri|cstype|Eğri veya yüzey tipi
|curv2|2B eğri|sp|Özel nokta|**Yüzeylerin bağlantısı ve gruplandırılması**
|surf|Yüzey|end|Enddeyimi|con|connect
|**Görüntüleme/oluşturma nitelikleri**|g|Grup adı
|eğim|Eğim enterpolasyonu|shadow_obj|Gölge dökümü|s|Yumuşatma grubu
|lod|Ayrıntı düzeyi|trace_obj|Işın izleme|mg|Grubu birleştirme
|d_interp|İnterpolasyonu çözme|ctech|Eğri yaklaşım tekniği|o|Nesne adı
|c_interp|Renk enterpolasyonu|stech|Yüzeye yakınlaştırma tekniği|
|usemtl|Malzeme adı|mtllib|Malzeme kitaplığı|
|**Geometrik köşeler**|
|v|Geometrik köşeler|vn|Köşe normalleri|
|vt|Doku köşeleri|vp|Parametre alanı köşeleri|

### Renk ve Doku

OBJ dosyası, renk ve doku bilgilerinin Malzeme Şablonu Kitaplığı (MTL) adı verilen ilişkili bir dosya biçiminde saklanmasını sağlar. Bu iki dosya birlikte kullanılarak çok renkli geometrik modeller oluşturulur. MTL dosyaları ASCII tabanlıdır ve Phong yansıma modelini kullanarak bir yüzeyin ışığı yansıtma özelliklerini tanımlayarak bilgisayarda işlemeyi kolaylaştırır. Standart, malzeme değişimi için avantajından yararlanan çok sayıda yazılım satıcısı tarafından benimsenmiştir. MTL formatı, speküler ve paralaks haritalar gibi en son teknolojileri desteklemediği için biraz eskidir.

## Referanslar

* [Wavefront .obj dosyası](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

