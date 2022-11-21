{
  "date" : "2019-10-11",
  "keywords" :[ "tiff dosyası", "tiff dosya formatı", "tiff dosyası nedir", "dosya", "tiff örneği", "tiff dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - Görüntü Dosyası Biçimi",
  "description":"TIFF dosya formatı ve TIFF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## TIFF dosyası nedir?

TIFF veya TIF, Etiketli Görüntü Dosyası Biçimi, bu dosya biçimi standardına uyan çeşitli aygıtlarda kullanılması amaçlanan raster görüntüleri temsil eder. Birkaç renk uzayında çift seviyeli, gri tonlamalı, palet renkli ve tam renkli görüntü verilerini tanımlayabilir. Biçimi kullanan uygulamalar için alan ve zaman arasında seçim yapmak için kayıplı ve kayıpsız sıkıştırma şemalarını destekler. Biçim, makineye bağlı değildir ve işlemci, işletim sistemi veya dosya sistemleri gibi sınırlardan muaftır.

## TIFF Dosya Formatının Kısa Tarihi

TIFF dosya formatı ilk olarak Aldus Corporation tarafından 1986 sonbaharında, çeşitli tarayıcı üreticileri ve yazılım geliştiricileri ile yapılan bir dizi toplantının ardından oluşturuldu. TIFF dosya biçiminin birincil amacı, tüm masaüstü tarayıcı satıcıları için ortak bir taranmış görüntü dosyası biçimi sağlamaktı. Yalnızca ikili görüntü formatı desteğiyle başlayan biçim, zaman geçtikçe gri tonlamalı ve renkli görüntülerin desteğine dönüştü. TIFF dosya formatı belirtimlerinin ilk sürümü, daha önceki iki taslak yayın olduğu için Reivision 3.0 olarak etiketlenebilir. 1988'de, palet renkli görüntüler ve LZW sıkıştırması için destek ekleyen büyük bir Revizyon 5.0 yayınlandı. Bundan sonra 1992'de TIFF dosya biçimlerinin Revizyon 6.0'ı yayınlandı. 1994'te Adobe Systems, Aldus'u satın aldı ve teknik özellikler artık Adobe Systems tarafından mevcut ve sürdürülüyor.

## TIFF Dosya Biçimi Özellikleri

TIFF dosya formatı genişletilebilir ve sınırsız miktarda özel veya özel amaçlı bilginin eklenmesine izin veren çeşitli revizyonlardan geçmiştir. TIFF dosyası, baytların 0'dan N'ye kadar olduğu 8 baytlık bir başlıkla başlar. Mümkün olan en büyük TIFF dosyası 2**32 bayt uzunluğundadır. Dosya, doğrudan bir görüntü dosyasına (IFD) işaret eden 8 baytlık bir görüntü dosyası başlığıyla başlar. Bir IFD, gerçek görüntü verilerine işaretçilerin yanı sıra görüntü hakkında bilgi içerir.

### TIFF Dosya Başlığı

8 baytlık TIFF dosya başlığı aşağıdaki bilgileri içerir:

**Bayt 0-1:** Dosya içinde kullanılan bayt sırası. Yasal değerler şunlardır:“II”(4949.H)“MM” (4D4D.H).

"II" formatında bayt sırası, hem 16-bit hem de 32-bit tamsayılar için her zaman en önemsiz bayttan en önemli bayta doğrudur. Buna little-endian bayt sırası denir. "MM" biçiminde bayt sırası, hem 16 bit hem de 32 bit tamsayılar için her zaman en önemliden en önemsize doğrudur. Buna big-endian bayt sırası denir.

**Bayt 2-3:** Dosyayı ayrıca bir TIFF dosyası olarak tanımlayan gelişigüzel ancak dikkatle seçilmiş bir sayı (42). Bayt sırası, Bayt 0-1 değerine bağlıdır.

**Bayt 4-7:** İlk IFD'nin ofseti (bayt olarak). Dizin, başlıktan sonra dosyada herhangi bir yerde olabilir, ancak bir sözcük sınırında başlamalıdır. Özellikle bir Görüntü Dosyası Dizini, tanımladığı görüntü verilerini takip edebilir. Okuyucular işaretçileri nereye götürürlerse götürsünler takip etmelidir. Bayt ofseti terimi bu belgede her zaman TIFF dosyasının başlangıcına göre bir konumu belirtmek için kullanılmıştır. Dosyanın ilk baytının ofseti 0'dır.

### Görüntü Dosyası Dizini

Bir IFD, gerçek görüntü verilerine yönelik işaretçilerin yanı sıra görüntü hakkında bilgi içerir. 2 baytlık dizin girişlerinin sayısından (yani alan sayısından) ve ardından 12 baytlık alan girişlerinden oluşur. , ardından bir sonraki IFD'nin 4 baytlık ofseti (veya yoksa 0). Bir TIFF dosyasında en az 1 IFD olmalı ve her IFD'de en az bir giriş bulunmalıdır.

#### IFD Girişi

Her 12 baytlık IFD Girişi aşağıdaki formattadır.


|Bayt|Açıklama
---|---|
|0-1|Alanı tanımlayan Etiket
|2-3|Alan türü
|4-7|Belirtilen türün sayısı
|8-11|Değer Uzaklığı, alanın Değerinin dosya ofseti (bayt olarak). Değerin bir sözcük sınırında başlaması beklenir; dolayısıyla karşılık gelen Değer Ofseti bir çift sayı olacaktır. Bu dosya ofseti, görüntü verilerinden sonra bile dosyada herhangi bir yeri gösterebilir.

TIFF alanı, TIFF etiketi ve değerinden oluşan mantıksal bir varlıktır. Bu mantıksal konsept, bir IFD Girişi ve değer/ofset kısmına uymuyorsa gerçek değer, IFD Girişinin son 4 baytı olarak uygulanır. TIFF alanı ve IFD girişi terimleri çoğu bağlamda birbirinin yerine kullanılabilir.

### Temel TIFF ###

Temel TIFF, TIFF'in çekirdeğidir ve tüm ana akım TIFF geliştiricilerinin ürünlerinde desteklemesi gereken temel unsurlardır. TIFF biçimine uygunluk, Temel TIFF gerekliliklerine uyulmasına tabidir. Bu gereksinimler, özellikler belgesi 6.0'da iyi bir şekilde belgelenmiştir.

#### Dosya Başına Birden Fazla Görüntü ####

Bir TIFF dosyasında birden fazla IFD olabilir. Her IFD bir alt dosya tanımlar. Alt dosyaların potansiyel kullanımlarından biri, bir faks iletiminin sayfaları gibi ilgili görüntüleri tanımlamaktır. İlki dışındaki herhangi bir IFD'yi okumak için bir Baseline TIFF okuyucu gerekli değildir.

#### Görüntü Türleri ####

Temel TIFF Görüntüsü aşağıdaki türlere sahiptir:

**İki düzeyli:** İki düzeyli bir görüntü, siyah ve beyaz olmak üzere iki renk içerir. TIFF, bir uygulamanın iki düzeyli verileri beyaz sıfırdır veya siyah sıfırdır biçiminde yazmasına izin verir. Bu bilgileri kaydeden alana **Fotometrik Yorum** adı verilir.

* RGB tam renkli

Bilevel görüntüleri için Fotometrik Yorumlama bilgileri aşağıdaki gibidir:

Etiket = 262 (106.H)
Tür = KISA
**değerler**

|Değer|Açıklama|
---|---|
|0|İki düzeyli ve gri tonlamalı görüntüler için: 0, beyaz olarak görüntülenir. Maksimum değer siyah olarak görüntülenir. Bu, Sıkıştırma#2| için normal değerdir.
|1|SiyahSıfır. İki düzeyli ve gri tonlamalı görüntüler için: 0, siyah olarak görüntülenir. Maksimum değer beyaz olarak görüntülenir. Bu değer Sıkıştırma#2 için belirtilirse, görüntü tersten görüntülenmeli ve yazdırılmalıdır.|

**Gri Tonlamalı:** Gri tonlamalı görüntüler, iki seviyeli görüntülerin bir genellemesidir. İki düzeyli görüntüler yalnızca siyah beyaz görüntü verilerini depolayabilir, ancak gri tonlamalı görüntüler de gri tonlarını depolayabilir. Bu tür görüntüleri tanımlamak için aşağıdaki alanları eklemeniz veya değiştirmeniz gerekir. Diğer gerekli alanlar, iki seviyeli görüntüler için gerekli olanlarla aynıdır. Gri tonlamalı görüntüler için, Sıkıştırma # 1 veya 32773 (PackBits). Baseline TIFF'de, gri tonlamalı görüntüler sıkıştırılmamış veriler olarak depolanabilir veya PackBits algoritmasıyla sıkıştırılabilir.

Gri tonlamalı resimler için **BitsPerSample** bilgileri aşağıdaki gibidir:

Etiket = 258 (102.H)
Tür = KISA

Bileşen başına bit sayısı. Temel TIFF gri tonlamalı görüntüler için izin verilen değerler, 16 veya 256 farklı gri tonuna izin veren 4 ve 8'dir.

**Palet-Renk:** Palet-renkli görüntüler, gri tonlamalı görüntülere benzer. Hâlâ piksel başına bir bileşeni vardır, ancak bileşen değeri, tam bir RGB arama tablosunda bir dizin olarak kullanılır. Bu tür görüntüleri tanımlamak için aşağıdaki alanları eklemeniz veya değiştirmeniz gerekir. Diğer zorunlu alanlar, gri tonlamalı görüntüler için olanlarla aynıdır.
Palet-Renkli görüntü için Fotometrik Yorumlama bilgileri aşağıdaki gibidir:

Fotometrik Yorum = 3 (Palet Rengi).
ColorMapTag = 320 (140.H)
Tür = KISA
N = 3 * (Örnek Başına 2 Bit)

Bu alan, palet renkli görüntüler için bir Kırmızı-Yeşil-Mavi renk haritasını (genellikle arama tablosu olarak adlandırılır) tanımlar. Palet renkli bir görüntüde, bir RGB arama tablosuna indekslemek için bir piksel değeri kullanılır. Örneğin, 0 değerine sahip bir palet rengi pikseli, 0. Kırmızı, Yeşil, Mavi üçlüsüne göre görüntülenir. TIFF Renk Haritasında, tüm Kırmızı değerler önce gelir, ardından Yeşil değerler, ardından Mavi değerler gelir. ColorMap'te siyah 0,0,0 ile temsil edilir ve beyaz 65535, 65535, 65535 ile temsil edilir.

**RGB tam renkli:** Bir RGB görüntüsünde her piksel üç bileşenden oluşur: kırmızı, yeşil ve mavi. ColorMap yoktur. Bir RGB görüntüsünü tanımlamak için aşağıdaki alanları ve değerleri eklemeniz veya değiştirmeniz gerekir. Diğer gerekli alanlar, palet renkli görüntüler için gerekli olanlarla aynıdır.

Örnek Başına Bit Sayısı = 8,8,8. Baseline TIFF RGB görüntüsünde her bileşen 8 bit derinliğindedir.

Fotometrik Yorum = 2 (RGB) ve ColorMap yoktur.

Etiket = 277 (115.H)
Tür = KISA
Piksel başına bileşen sayısı. Ekstra örnekler olmadığı sürece bu sayı, RGB görüntüler için 3'tür.

## Referanslar ##

* [TIFF Dosya Biçimi - Wikipedia](https://en.wikipedia.org/wiki/TIFF)

