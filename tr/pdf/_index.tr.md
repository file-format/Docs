{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :[ "temel bilgiler" ],
  "description":"Taşınabilir Belge Biçimi (PDF), yazılım, donanım ve işletim sisteminden bağımsız belgelerin standart bir temsilidir. PDF standartları, PDF/A, PDF/E, PDF/UA, PDF/VT ve PDF/X'i içerir.",
  "title" :"PDF Dosya Biçimi - PDF dosyası nedir?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF), Adobe tarafından 1990'larda oluşturulmuş bir belge türüdür. Bu dosya formatının amacı, uygulama yazılımı, donanım ve İşletim Sisteminden bağımsız bir formatta belgelerin ve diğer referans materyallerinin temsili için bir standart getirmekti. PDF dosya formatı, metin, resimler, köprüler, form alanları, zengin medya, dijital imzalar, ekler, meta veriler, Jeo uzamsal özellikler ve kaynak belgenin bir parçası haline gelebilecek 3B nesneler gibi bilgileri içerme konusunda tam kapasiteye sahiptir.

Çoğu durumda, mevcut belgeler sıfırdan yeni bir PDF oluşturmak yerine PDF'ye dönüştürülür. Ancak bu, PDF dosyalarının oluşturulması veya işlenmesi için herhangi bir yazılım olmadığı anlamına gelmez.

**(PDF dosya formatı hakkında bir şeyler paylaşmak zorunda mısınız? Bulgularınızı [PDF Dosya Formatı Haberleri](https://news.fileformat.com/t/PDF) bölümünde yayınlayabilirsiniz.)**

## PDF Dosya Biçimi - Kısa Tarihçe

Zaman çizelgesi açısından PDF dosyası oluşumu hakkında zaman çizelgesinin hızlı bir şekilde gözden geçirilmesi aşağıdaki gibidir:

**1993** - Adobe Systems, PDF belirtimlerini ücretsiz olarak kullanıma sundu

**2008** - PDF, 1 Temmuz 2008'de açık standart olarak yayınlandı ve Uluslararası Standardizasyon Örgütü tarafından **ISO 32000-1:2008** olarak yayınlandı.

**2008** - Adobe, PDF uyumlu uygulamaları yapmak, kullanmak, satmak ve dağıtmak için gerekli olan ve Adobe'ye ait tüm patentler için ISO 32000-1 biçiminde telifsiz haklara sahip bir Kamu Patent Lisansı yayınladı.

PDF'nin ilk sürümü, PDF 1.0 olarak belirlendi ve daha sonra PDF 1.7'ye kadar revizyonlardan geçti. ISO 32000-1 haline gelen PDF 1.7, bazı standartlaştırılmamış tescilli teknolojilerin yanı sıra Adobe XML Forms Architecture (XFA) ve Acrobat için JavaScript uzantısı içerir. 28 Temmuz 2017'de ISO 32000-2:2017 olarak bilinen ve standardize edilmemiş herhangi bir teknoloji içermeyen PDF 2.0 yayınlandı.

## PDF Dosya Biçimi Özellikleri

Bir PDF dosyası, PDF belirtimleri tarafından tanımlanan sözdizimi kurallarına göre belirteçler halinde gruplandırılabilen bir bayt kümesidir. Bir veya daha fazla belirteç, bir PDF belgesinin oluşturulduğu temel veri değerleri olan temel olarak nesneler olmak üzere daha yüksek düzeyde sözdizimsel varlıklar oluşturmak için birleştirilir.

### PDF Dosyalarının Dosya Yapısı

PDF dosyası içerikleri, dosyanın içinde aşağıdaki sırayla düzenlenmiştir.

|Başlık
|Gövde
|Çapraz Referans Tablosu
| Fragman

#### PDF Dosya Başlığı ####

PDF sürümünden bağımsız olarak, bir PDF dosyası, PDF için benzersiz tanımlayıcı içeren bir başlık ve x'in 1-7 arasında olduğu %PDF-1.x gibi biçim sürümüyle başlar.

#### Dosya Gövdesi ####

Bir PDF dosyasının gövdesi, bir belgenin içeriğini temsil eden bir dizi dolaylı nesneden oluşur. Yukarıda açıklandığı gibi nesneler, belgenin yazı tipleri, sayfalar ve örneklenmiş görüntüler gibi bileşenlerini temsil eder. PDF 1.5'ten başlayarak gövde, her biri bir dizi dolaylı nesne içeren nesne akışları da içerebilir.

#### Çapraz Referans Tablosu ####

Çapraz referans tablosu, dosya içindeki dolaylı nesnelere rasgele erişime izin veren bilgiler içerir, böylece belirli bir nesnenin yerini belirlemek için tüm dosyanın okunması gerekmez. Tablo, her dolaylı nesne için, dosyanın gövdesi içindeki o nesnenin bayt ofsetini belirten tek satırlık bir giriş içerecektir. (PDF 1.5'ten başlayarak, çapraz referans bilgilerinin bir kısmı veya tamamı alternatif olarak çapraz referans akışlarında bulunabilir.

#### Dosya Fragmanı ####

Bir PDF dosyasının fragmanı, uyumlu bir okuyucunun çapraz referans tablosunu ve belirli özel nesneleri hızlı bir şekilde bulmasını sağlar. Uygun okuyucular, bir PDF dosyasını sonundan okumalıdır. Dosyanın son satırı yalnızca dosya sonu işaretçisini, %%EOF içerecektir. Önceki iki satır, her satırda ve sırayla startxref anahtar sözcüğünü ve dosyanın başlangıcından son çapraz referans bölümündeki xref anahtar sözcüğünün başlangıcına kadar kodu çözülmüş akıştaki bayt ofsetini içerecektir.

### PDF Nesneleri ###

Bir PDF dosyası, aşağıdaki türlerde olan birkaç farklı türde nesne içerir

* Boole değerleri - koşullu doğru veya yanlışı temsil eder
* Sayılar - Tamsayı ve Gerçek değerler
* Dizeler - parantez içindeki karakterleri içerir
* Adlar - bir ileri / karakterle başlayın, örneğin /ASomewhatLongerName, ASomewhatLongerName ile sonuçlanır
* Diziler - PDF tek boyutlu dizileri destekler. İç içe öğeler olarak diziler kullanılarak daha yüksek boyutlu diziler oluşturulabilir
* Sözlükler - nesnelerin anahtar-değer çiftleri olarak toplanması. Sıfır girişi olabilir.
* Akışlar - sınırsız uzunlukta olabilen bayt dizisini temsil eder
* Boş Nesne - bir boş değeri temsil eder

% işaretiyle tanıtılan ve 8 bitlik karakterler içerebilen yorumlar gibi başka nesneler de olabilir.

### Dolaylı Nesneler ###

Bir PDF dosyasındaki herhangi bir nesne, dolaylı bir nesne olarak etiketlenebilir. Dolaylı nesnelere, diğer nesnelerin kendisine atıfta bulunabileceği benzersiz nesne tanımlayıcısı verilir. Bunlara çapraz başvuru, bir dizin tablosunda tutulur ve ana gövdeyi izleyen ve dosyanın başından itibaren her bir dolaylı nesnenin bayt uzaklığını veren xref anahtar sözcüğüyle işaretlenir.

### Doğrusal ve Doğrusal Olmayan PDF Düzenleri ###

PDF mizanpajları, hedef uygulamalara ve diğer faktörlere bağlı olarak Doğrusal ve doğrusal olmayan olarak sınıflandırılır.

Doğrusal Olmayan - Doğrusal olmayan PDF dosyaları, doğrusal PDF dosyalarına kıyasla daha az disk alanı kullanır. Belgenin PDF sayfaları, PDF dosyası boyunca dağınık biçimde bulunur ve bu nedenle doğrusal olmayan dosyalar, doğrusal dosyalara kıyasla daha yavaştır.

Doğrusal PDF - Çevrimiçi PDF görüntüleyicilerini hedefleyen Doğrusal PDF dosyaları, diske doğrusal bir biçimde yazılacak şekilde oluşturulur. Bu, tüm belgenin görüntülenmeden önce yüklenmesi için tarayıcı eklentileri gerektirmez.

### Nesnelere Genel Bakış ###

Belirtildiği gibi, PDF gövdesi yukarıda belirtilen nesnelerin bir koleksiyonudur. PDF, if ve loop komutları gibi programlama dillerinin kontrol özellikleri olmaksızın büyük ölçüde PostScript'e dayalıdır. Grafik içerikler oluşturmak için Postscript kodu tarafından verilen komutlar, belge tarafından atıfta bulunulan herhangi bir dosya, grafik veya yazı tipine ek olarak toplanır ve belirteçlenir. Tüm bu içerikler, tek bir dosyada toplanır ve sonuçta oluşan PostScript çıktısı elde edilir.

#### Metin ####

PDF'deki metin, aslında yazı tiplerinden gliflerle görüntülenen metin öğeleriyle temsil edilir. Glif, grafik bir şekildir ve koordinat dönüşümü gibi tüm grafik manipülasyonlara tabidir. Çoğu sayfa açıklamasında metnin önemi nedeniyle PDF, glifleri kolay ve verimli bir şekilde tanımlamak, seçmek ve işlemek için üst düzey olanaklar sağlar.

#### Grafik ####

PDF içerik akışlarında kullanılan grafik işleçleri, bir raster çıktı aygıtında çoğaltılacak sayfaların görünümünü tanımlar. Tesisler hem yazıcı hem de ekran uygulamaları için tasarlanmıştır. Grafik işleçleri altı ana grup oluşturur:

* Grafik durumu işleçleri, diğer grafik işleçlerinin yürüttüğü genel çerçeve olan grafik durumu adı verilen veri yapısını işler. Grafik durumu, bir PDF içerik akışı içinde kullanılan kullanıcı alanı koordinatlarını çıktı cihazı koordinatlarına eşleyen mevcut dönüşüm matrisini (CTM) içerir. Ayrıca geçerli rengi, geçerli kırpma yolunu ve boyama işleçlerinin gizli işlenenleri olan diğer birçok parametreyi içerir.
* Yol oluşturma işleçleri, şekilleri, çizgi yörüngelerini ve çeşitli türden bölgeleri tanımlayan yolları belirtir. Yeni bir yola başlamak, ona çizgi parçaları ve eğriler eklemek ve kapatmak için operatörler içerirler.
* Yol boyama işleçleri, bir yolu bir renkle doldurur, üzerine kontur çizer veya bunu bir kırpma sınırı olarak kullanır.
* Diğer boyama operatörleri, kendini tanımlayan bazı grafik nesneleri boyar. Bunlar, örneklenmiş görüntüleri, geometrik olarak tanımlanmış gölgelemeleri ve sırayla grafik operatör dizilerini içeren tüm içerik akışlarını içerir.
* Metin operatörleri, yazı tiplerinden karakter gliflerini seçer ve gösterir (metin karakterlerini temsil etmek için yazı karakterlerinin açıklamaları). PDF, glifleri genel grafik şekiller olarak ele aldığından, metin işleçlerinin birçoğu grafik durumu veya boyama işleçleriyle gruplandırılabilir. Bununla birlikte, glif ve yazı tipi tanımlarıyla başa çıkmak için veri yapıları ve mekanizmaları yeterince uzmanlaşmıştır.
* İşaretli içerik işleçleri, üst düzey mantıksal bilgileri içerik akışındaki nesnelerle ilişkilendirir. Bu bilgi, içeriğin işlenmiş görünümünü etkilemez; belge alışverişi için PDF kullanan uygulamalar için kullanışlıdır.

## Referanslar ##

* [PDF Dosya Biçimi: Temel Yapı](https://resources.infosecinstitute.com/topics/hacking/pdf-file-format-basic-structure/)
* [PDF - Vikipedi](https://en.wikipedia.org/wiki/PDF)
* [PDF Referansı - Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

