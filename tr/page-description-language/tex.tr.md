{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TEX Dosya Biçimi",
  "description":"TEX dosya formatı ve TEX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## TEX Dosyası Nedir? ##

**TeX**, belgeleri dizmek için kullanılan programlama ve biçimlendirme özelliklerinden oluşan bir dildir. Stanford Üniversitesi'nden Donald Knuth, bu becerikli dizgi sisteminin yaratıcısıdır. TeX, dünya çapında yüksek kaliteli teknik belgeler üretmek için yazarların ve yayıncıların nihai tercihidir. TeX, karmaşık matematiksel ifadeleri biçimlendirme konusunda olağanüstü bir iş çıkarır. TeX, yüksek kaliteli bir fotodizgi makinesiyle birlikte en iyi geleneksel dizgi sistemleri tarafından üretilen sonuçlarla rekabet eder. Bu nedenle en klas dijital tipografik sistemler olarak kabul edilir.

TeX giriş dosyaları ASCII kodunu temel alır, böylece yazarlar, yayın yöneticileri ve eleştirmenler arasında el yazması paylaşımına izin verir. Çok çeşitli bilgi işlem ortamları, hemen hemen her modern platform ve birçok eski platform TeX'i destekler. Ayrıca TeX, geniş bir tüketici kitlesi tarafından kullanılabilen ücretsiz bir yazılımdır. Birçok UNIX kurulumu, farklı amaçlar için biçimlendirme sistemi olarak hem UNIX troff hem de TeX'i kullanır. Diğer dizgi görevleri, LaTeX, ConTeXt ve diğer makro paketleri biçiminde muazzam bir şekilde gerçekleştirilir.

## Kısa Tarih ##

TeX, 1978'de Donald Knuth tarafından tasarlandı ve yazıldı. Massachusetts Institute of Technology'den Guy Steele, TeX'in girdi/çıktısını, Zaman Paylaşımı Sistemi (ITS) gibi Uyumsuz işletim sistemi altında çalışacak şekilde revize etti. TeX'in ilk sürümü, Stanford'un WAITS işletim sistemi altında programlama dilinde (SAIL) geliştirildi ve bir PDP-10 üzerinde çalışacak şekilde test edildi. Knuth, ileri sürümler için okuryazar programlama fikrini ortaya attı. Okuryazar programlama, orijinal dosyayı kullanarak çapraz bağlantılı belgeler için derlenebilir kaynak kodu ve dizgi (TeX'te) oluşturmanın bir yoludur. TeX'in bu gelişmiş sürümlerini geliştirmek için kullanılan dil, taşınabilirliği sağlamak için DEC PDP-10 Pascal programlarının bir karışımı olan WEB olarak adlandırılır.

TeX'in gözden geçirilmiş yeni bir sürümü 1982'de yayınlandı ve TeX82 olarak adlandırıldı. En büyük değişiklik, orijinal heceleme algoritmasının Frank Liang tarafından yeni yazılan algoritma ile değiştirilmesidir. Farklı platformlar arasında taşınabilirliği sağlamak için, TeX82 kayan nokta kullanmak yerine gerçek, turing-complete programlama dili ile birlikte sabit nokta aritmetiği kullanır. 1989'da TeX ve Metafont'un yeni sürümleri yayınlandı. Bu nedenle, TeX'in 3.0 sürümü, metinde 256 farklı karaktere izin vererek 8 bitlik girişleri kolaylaştırır. Sürüm 3'ten sonra, güncellemeler ondalık sayının sonuna fazladan bir rakam eklenerek belirtilir, örneğin TeX'in geçerli sürümü 3.14159265 olarak gösterilir. Bu sürüm en son 12-1-2014 tarihinde güncellendi.

## TeX Girişi ##

TEX'e bir Giriş dosyası, normal metin kullanan bir metin düzenleyiciyle hazırlanabilir. Tipik bir Kelime işlemciden farklı olarak, bu girdi dosyası herhangi bir görünmez kontrol karakterine izin vermez. Bir dosya, TeX'in yeteneklerini artıran makro tanımları ve yardımcı tanımları içeren başka bir dosyaya gömülebilir. Bir TeX kurulumu herhangi bir makro dosyasıyla birlikte gelirse, TeX ile ilgili yerel bilgiler makro dosyalarının nasıl kullanılacağını gösterir. TeX'in standart biçimi, düz TEX olarak bilinen makroların ve diğer tanımların bir kombinasyonunu bütünleştirir.

Tüm karakterlerin ve sembollerin boyutlarına ilişkin kesin bilgilere dayanarak, satır başına harflerin ve sayfa başına satırların optimum organizasyonunu hesaplar. Belge işleme sırasında, "dvi"nin "cihazdan bağımsız" anlamına geldiği bir .dvi dosyası oluşturulur. dvi uzantılı belgeyi yazdırmak veya önizlemek için aygıt sürücü programları gereklidir. Günümüzde dvi üretimi, yaygın olarak kullanılan bir pdf-TeX tarafından atlanmıştır. TeX kurulumunda yazı tipleriyle ilgili ön bilgi yoktur, bu nedenle yerel TeX ortamının bir parçası olan harici yazı tipi dosyaları belge için bilgi almak üzere kullanılır.

## Dizgi Sistemi ##

Temel TeX sistemi tarafından yaklaşık 300 ilkel (komut) anlaşılabilir. İlkel komutlar düşük seviyeli komutlardır, bu nedenle sıradan bir kullanıcı bunları nadiren doğrudan kullanır ve çoğu işlevsellik format dosyaları tarafından gerçekleştirilir. Bu biçim dosyaları, TeX'in önceden yüklenmiş bellek görüntüleridir ve ardından büyük makro koleksiyonlarının yüklenmesi gelir. Dilin orijinal varsayılan biçimi, yani düz TeX, yaklaşık 600 komut ekler.

Kıvrımlı parantezlerle gruplandırılmış bir ters eğik çizgi, TeX komutlarının başladığını gösterir. TeX, makro ve belirteç tabanlı bir dil olduğundan, TeX'in sözdizimsel özelliklerinin neredeyse tamamı, daha sonra yürütülen genişletilemez belirteçler dışında kullanıcı tanımlı olanlar da dahil olmak üzere çalışma zamanında değiştirilebilir. Genişletmenin kendisi pratik olarak sorunsuzdur. Bazı komutların, bir komutun işlevini açıklamaya yardımcı olan bağımsız değişkenlerden sonra gelmesi gerekir. Örneğin, \vskip komutu, TEX'i sayfada aşağı/yukarı atlaması için yönlendirir ve ardından ne kadar alan atlanacağını belirleyen bir argüman gelir.

## Sürümler ##

LaTeX, orijinal olarak Leslie Lamport tarafından geliştirilen en sık kullanılan formattır. LaTeX, dosyalar, mektuplar, kitaplar ve slaytlar için farklı belge stillerini entegre eder ve farklı bölümler ve matematiksel ifadeler için başvuru ve otomatik numaralandırma sunar. AMS-TeX, American Mathematical Society tarafından geliştirilen bir diğer popüler formattır.

AMS-TeX, dergiler tarafından yerel tarzlarına uyacak şekilde yeniden tanımlanabilen çok daha kullanıcı dostu komutlar sunar. LaTeX, daha sonra AMS-LaTeX olarak adlandırılan AMS "paketlerini" kullanarak AMS-TeX'in avantajlarından yararlanabilir. ConTeXt, ağırlıklı olarak masaüstü yayıncılık için kullanılan, Hans Hagen tarafından yazılan başka bir formattır.

TeX yazılımı, oluşturulduğu sırada diğer dizgi sistemlerinde bulunmayan veya daha düşük kalitede olan çeşitli özellikler sunar. Bu dilin yenilikçi özelliklerinden bazıları, Knuth'un öğrencilerinin tezlerinden türetilen ilginç algoritmalara dayanmaktadır. Diğer dizgi programları artık TeX'in kullanışlı özelliklerini programlarına dahil ediyor.

## Referanslar ##

* [TeX Dizgi sistemi](https://en.wikipedia.org/wiki/TeX)

