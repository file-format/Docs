{
  "date" : "2019-10-11",
  "keywords" :[ "mpx dosyası", "mpx dosya formatı", "mpx dosyası nedir", "dosya", "mpx örneği", "mpx dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX - Microsoft Project Exchange Dosya Biçimi",
  "description":"MPX dosya formatı ve MPX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## MPX dosyası nedir? ##

.mpx uzantılı bir dosya bir Microsoft Exchange Dosya Biçimidir. Microsoft Project (MSP) tarafından, MSP ile Primavera Project Planner, Sciforma ve Timerline Precision Estimating dahil olmak üzere MPX dosya formatını destekleyen diğer uygulamalar arasında proje bilgisi alışverişini kolaylaştırmak için bir MPX dosya formatı geliştirilmiştir. MPX dosyalarını kullanarak, ayrıntılı kaynak atama bilgileri, takvim bilgileri veya Proje Bilgileri iletişim kutusundaki bilgiler gibi her türlü bilgiyi bir projeden farklı bir sisteme aktarabilirsiniz.

Microsoft Project 4.0, Microsoft Project 98 aracılığıyla kullanılmaya devam eden MPX dosya formatlarını oluşturma ve okuma desteğini tanıttı. Ancak, MPX dosyaları oluşturma desteği, Microsoft Project 2000'in yayınını durdurdu ve Microsoft Project 2010'a kadar olan sürümler yalnızca MPX okumayı destekliyor. MPX dosya biçimi, MSP 2010'dan sonraki sürümlerde desteklenmez.

## MPX Dosya Biçimi ##

Bu bölümde MPX dosya özelliklerine genel bir bakış verilmektedir. Spesifikasyonların tamamı bu [Bilgi Bankasında](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) bulunabilir. makale ve detaylar için başvurulabilir.

### Kayıtlar ###

MPX dosyasının bir Kaydı, proje için bilgilerden oluşur. Her kaydın kendi sırasına sahip olduğu farklı kayıt türleri vardır. Her kayıt türü, kayıt numarası ile tanımlanır. Bir MPX dosyası için, Dosya Oluşturma kayıt türünü içermesi gerekir. Diğer kayıt türleri zorunlu değildir. Aşağıdaki tablo, tüm kayıt türlerini, bunların kayıt numaralarını ve her türün MPX dosyasında içerebileceği kayıt sayısını gösterir. MPX dosyasına kayıt dahil edilmesi, herhangi bir yere eklenen yorumlarla tablo sırasını takip etmelidir.

|Kayıt Adı|Kayıt Numarası|Maksimum Kayıt sayısı
---|---|---|
|Dosya Oluşturma (gerekli)|yok|1
|Para Birimi Ayarları|10|1
|Varsayılan Ayarlar|11|1
|Tarih ve Saat Ayarları|12|1
|Temel Takvim Tanımı|20|250
|Temel Takvim Saatleri|25| Temel Takvim Tanımı kaydı başına 7
|Temel Takvim İstisnası|26| Temel Takvim Tanımı kaydı başına 250
|Proje Başlığı|30|1
|Metin Kaynak Tablosu Tanımı|140|1- (Veya Sayısal Kaynak Tablosu Tanımı kaydını da kullanabilirsiniz)
|Sayısal Kaynak Tablosu Tanımı|41|1
|Kaynak|50|9.999
|Kaynak Notları|51| Kaynak kaydı başına 1
|Kaynak Takvim Tanımı|55| Kaynak kaydı başına 1
|Kaynak Takvim Saatleri|56| Kaynak Takvimi başına 7
|Kaynak Takvim İstisnası| Kaynak Takvimi başına 57|250
|Text Task Table Definition|60|1 (Ya da Numeric Task Table Definition kaydını kullanabilirsiniz)
|Sayısal Görev Tablosu Tanımı|61|1
|Görev|70|9
|Görev Notları|71| Görev kaydı başına 1
|Yinelenen Görev|72| Görev kaydı başına 1
|Kaynak Ataması|75| Görev kaydı başına 100
|Atama Çalışma Grubu alanları|76| Atama kaydı başına 1
|Proje İsimleri|80|500
|DDE ve OLE İstemci Bağlantıları|81|500
|Yorumlar|0|sınırsız

### Dosya Yapısı ###

Bir MPX dosyası, yukarıda belirtilen ve dosyanın içinde önceden ayarlanmış bir şekilde düzenlenmiş kayıtlardan oluşur. Bu kayıt türleriyle ilgili ayrıntılar aşağıda tartışılmaktadır:

**Dosya Oluşturma Kaydı (FCR):** Bu, amacı aşağıdakileri tanımlamak olan zorunlu bir kayıttır:

* Dosya formatı (MPX)
* Dosyada kullanılan liste ayırıcı karakter
* Dosyayı oluşturmak için kullanılan program ve sürüm numarası
* Dosyada kullanılan MPX dosya biçiminin sürüm numarası
* Dosyayı oluşturmak için kullanılan kod sayfası

Bu, dosyadaki ilk kayıt olmalıdır. Microsoft Project'ten dışa aktarırken, Windows Denetim Masası'ndaki Bölgesel Ayarlar öğesinde liste ayırıcı karakter belirtilir. Bir FCR Kaydı aşağıdaki alanları içerir:

* MPX'in hemen ardından liste ayırıcı karakter gelir
* Program Adı/Tanımlayıcı
* Dosyanın Versiyon Numarası
* Kod Sayfası (850, 437, MAC, ANSI)

Örneğin kayıt, bu MPX dosyasında liste ayırıcı karakter olarak virgül kullanıldığını belirten **MPX, Microsoft Project, 3.0** bilgilerini içerebilir. Dosyada kullanılan MPX biçiminin sürümü, Microsoft Project sürüm 3.0'dan verilir.

**Para Birimi Ayarları** Kayıt numarası 10 olan bu kayıt, Seçenekler iletişim kutusundaki para birimi seçenekleri için ayarları belirtir. Bu kayıt dahil edilmemişse, Seçenekler iletişim kutusundaki geçerli ayarlar kullanılır. Binlik ve Ondalık ayırıcılar, Windows Denetim Masası'ndaki Bölgesel Ayarlar öğesinde belirtilir.
Bu kayıtta yer alan alanlar şunlardır:

* Para Birimi Sembolü
* Sembol Konumu (0 # sonra, 1 # önce, 2 # sonra boşlukla, 3 # önce boşlukla)
* Para Birimi Rakamları (0,1,2)
* Binlik Ayırıcı
* Ondalık Ayırıcı

**Örnek:** 10,$,1,2,",",.
Bu örnek, para birimi değerlerinin kendilerinden önce bir dolar işareti ($) içerdiğini, ondalık noktadan sonra iki rakamın dahil edildiğini, binleri ayırmak için virgül kullanıldığını ve ondalık nokta olarak nokta kullanıldığını belirtir. Binlik Ayırıcı alanına liste ayırıcı karakter dahil edildiğinden, alan tırnak işaretleri içine alınır.

**Varsayılan Ayarlar:** Kayıt numarası 11 olan bu kayıt, Seçenekler iletişim kutusundaki varsayılan seçenekler için ayarları belirtir. Bir süre belirtilmezse, doğru süre birimi hesaplamaları için Varsayılan Süre Biriminin ayarlanması gerekir. Bu kayıt dahil edilmemişse, Seçenekler iletişim kutusundaki geçerli ayarlar kullanılır.
Bu kayıtta yer alan alanlar şunlardır:

* Varsayılan Süre Birimleri (0 # dakika, 1 # saat, 2 # gün, 3 # hafta)
* Varsayılan Süre Türü (0 # sabit değil, 1 # sabit)
* Varsayılan İş Birimleri (0 # dakika, 1 # saat, 2 # gün, 3 # hafta)
* Varsayılan Saat/Gün
* Varsayılan Saat/Hafta
* Varsayılan Standart Oran
* Varsayılan Fazla Mesai Ücreti
* Görev Durumunu Güncelleme Kaynak Durumunu Günceller (0 # hayır, 1 # evet)
* Devam Eden Görevleri Böl (0 # hayır, 1 # evet)

**Tarih ve Saat Ayarları:** Kayıt numarası 12 olan bu kayıt, Seçenekler iletişim kutusundaki tarih ve saat seçenekleri ve Düzen iletişim kutusundaki Çubuk Metin Tarih Biçimi seçeneği için ayarları belirtir. Bu kayıt dahil edilmemişse, Seçenekler iletişim kutusundaki geçerli ayarlar kullanılır.
\\Bu kayıtta yer alan alanlar şunlardır:

* Tarih Sırası (0 # ay/gün/yıl, 1 # gün/ay/yıl, 2 # yıl/ay/gün)
* Saat Formatı (0 # 12 saat, 1 # 24 saat)
* Varsayılan Saat (gece yarısından sonraki dakika sayısı)
* Tarih Ayırıcı
* Zaman Ayırıcı
* 0:00 - 11:59 Metin
* 12:00 - 23:59 Metin
* Tarih Formatı (0 -14)*
* Çubuk Metni Tarih Biçimi (0 -194)*

**Baz Takvim Tanımı:** Kayıt numarası 20 olan bu kayıtlar, esas takvimleri ve bunların haftanın çalışılan ve çalışılmayan günlerini tanımlar. Bir gün için giriş yoksa varsayılan ayarlar kullanılır. Varsayılan ayarlar, çalışma günleri için Pazartesi'den Cuma'ya ve çalışma dışı günler için Cumartesi ve Pazar'dır. Bu kayıtta Ad alanı zorunludur. Günlerin her biri için 0 girişi, günün çalışılmayan bir gün olduğunu ve 1 girişi, günün iş günü olduğunu gösterir.
Bu kayıtta yer alan alanlar şunlardır:

* İsim
* Pazar
* Pazartesi
* Salı
* Çarşamba
* Perşembe
* Cuma
* Cumartesi

**Temel Takvim Saatleri:** Kayıt numarası 25 olan bu kayıtlar, varsayılan ayarlardan farklıysa haftanın günleri için çalışma saatlerini belirtir. Varsayılan çalışma saatleri 08:00 - 12:00 ve 13:00 - 17:00'dir. Her Temel Takvim Saatleri kaydı, bir önceki Temel Takvim Tanımı kaydına atıfta bulunur. Bu kayıtlardan yedi adede kadar her Temel Takvim Tanımı kaydını takip edebilir.

* Haftanın Günü (1 - 7, burada 1 # Pazar ve 7 # Cumartesi)
* 1. Zamandan itibaren
* Zaman 1'e
* 2. Zamandan itibaren
* Zaman 2'ye
* 3. Zamandan itibaren
* Zaman 3'e

**Temel Takvim İstisnası:** Kayıt numarası 26 olan bu kayıtlar, önceki iki kayıt türünde belirtilen gün ve saatlerin istisnalarını tanımlar. Bu kayıtlardan en fazla 250 tanesi her Temel Takvim Tanımı kaydını takip edebilir. Bu kayıtlar kronolojik sırayla listelenmelidir. İstisna bir gün ise Bitiş Tarihi alanını boş bırakabilirsiniz. Herhangi bir saat belirtilmezse, 8:00 AM - 12:00 PM ve 13:00 PM - 5:00 PM varsayılan saatleri kullanılır.
Bu kayıtta yer alan alanlar şunlardır:

* İtibaren
* Bugüne kadar
* Çalışmıyor/Çalışıyor (0 # çalışmıyor, 1 # çalışıyor)
* 1. Zamandan itibaren
* Zaman 1'e
* 2. Zamandan itibaren
* Zaman 2'ye
* 3. Zamandan itibaren
* Zaman 3'e

**Proje Başlığı:** Kayıt değeri 30 olan bu kayıt, proje başlangıç tarihi ve proje bitiş tarihi gibi global proje alanlarını ayarlar. Bu kayıttaki alanlar, Proje Bilgisi ve İstatistik iletişim kutularındaki bilgilere karşılık gelir.
Bu kayıtta yer alan alanlar ve sekmeler şunlardır:

* Proje sekmesi
* Şirket
* Müdür
* Takvim (Giriş yoksa standart kullanılır)
* Başlangıç Tarihi (Bu alan veya sonraki alan, Zamanlama Başlangıç ayarına bağlı olarak içe aktarılan bir dosya için hesaplanır)
* Bitiş tarihi
* Zamanlama Başlangıcı (0 # başlangıç, 1 # bitiş)
* Geçerli tarih*
* Yorumlar
* Maliyet
* Temel Maliyet
* Asıl maliyet
* İş
* Temel Çalışma
* Asıl iş
* İş
* Süre*
* Temel Süre*
* Fiili Süre
* Tamamlanma Yüzdesi
* Temel Başlangıç
* Temel Bitiş
* Gerçek Başlangıç
* Gerçek Bitiş
* Başlangıç Varyansı
* Bitiş Varyansı
* Ders
* Yazar
* Anahtar kelimeler

**Metin Kaynak Tablosu Tanımı**: Bu kayıt, sırasıyla içe veya dışa aktarılan kaynak alanlarını listeler. İçe aktarılan dosyalar için adlar, Microsoft Project'te kullanılan alan adlarıyla eşleşmelidir. Dışa aktarılan dosyalar için bu kayıt, dışa aktarma kaynağı tablosundan gelir. Ya bu kayıt ya da Sayısal Kaynak Tablo Tanımı kaydı kullanılmalıdır. Microsoft Project'ten dışa aktarırken, bu kayıtların her ikisi de dahil edilir.

**Sayısal Kaynak Tablosu Tanımı:** Bu kayıt, adlar yerine sayıların kullanıldığı, içe veya dışa aktarılan kaynak alanlarını sırasıyla listeler. Bu, her bir Kaynak kaydına dahil edilen kaynak alanlarını belirlemek için alternatif bir yöntemdir ve bir yabancı dil ürünü tarafından oluşturulan bir MPX dosyasını tanımlarken kullanışlıdır.

**Kaynak:** Bu kayıtlar, içe veya dışa aktarılan her bir kaynağa ilişkin bilgileri içerir. Her Kaynak kaydı bir kaynağı tanımlar. Bilgileri içe aktardığınızda, dahil edilen alanlar Metin Kaynağı Tablosu Tanımı kaydı veya Sayısal Kaynak Tablosu Tanımı kaydı tarafından tanımlanır. Bilgileri dışa aktardığınızda, dahil edilen alanlar kaynak Dışa Aktarma tablosunda listelenenlerdir.

**Kaynak Notları:** Bu kayıtlar, hemen önceki Kaynak kaydı hakkında notlar içerir. Not içinde yeni bir satır için ASCII karakteri 127 kullanılır. Not, liste ayırıcı karakteri içeriyorsa, notu tırnak içine alın.

**Kaynak Takvim Tanımı:** Bu kayıtlar, hemen önceki Kaynak kaydında belirtilen kaynağın çalışma günlerini tanımlar. İçe aktarılan dosyalar için Temel Takvim Adı alanında herhangi bir giriş yoksa Standart kullanılır. Belirli bir gün için giriş olmaması, günün varsayılan olarak ayarlandığını gösterir (2). Kaynak Takvim Tanımı kaydı yoksa, kaynak için temel takvim olarak Standart kullanılır ve günler için varsayılan kullanılır. Günlerin her biri için 0 girişi, günün çalışma dışı bir gün olduğunu, 1 günün iş günü olduğunu ve 2 girişi varsayılanın kullanıldığını belirtir.

**Kaynak Takvim Saatleri:** Bu kayıtlar, kaynağın kullandığı temel takvimden farklı olan kaynağın çalışma saatlerini tanımlar. Bu kayıtlar, bu kayıttan hemen önceki Kaynak Takvim Tanımı kaydına uygulanır. Her bir Kaynak Takvim Tanımı kaydını bu kayıtlardan en fazla yedi tanesi takip edebilir.

**Kaynak Takvim İstisnası:** Bu kayıtlar, önceki iki kayıt türünde belirtilen gün ve saatlerin istisnalarını tanımlar. Bu kayıtlardan en fazla 250 tanesi her bir Kaynak Takvim Tanımı kaydını takip edebilir. Bu kayıtlar kronolojik sırayla listelenmelidir. İstisna yalnızca bir gün ise Bitiş Tarihi alanını boş bırakabilirsiniz. Herhangi bir saat belirtilmezse, 8:00 AM - 12:00 PM ve 13:00 PM - 5:00 PM varsayılan saatleri kullanılır.

**Metin Görev Tablosu Tanımı:** Bu kayıt, içe veya dışa aktarılan görev alanlarını sırasıyla listeler. İçe aktarılan dosyalar için adlar, Microsoft Project'te kullanılan alan adlarıyla eşleşmelidir. Dosya dışa aktarılıyorsa, bu kayıt Görev Dışa Aktarma tablosundan gelir. Microsoft Project'ten dışa aktarırken, bu kayıtların her ikisi de dahil edilir. Çizelgelenmiş Başlangıç ve Çizelgelenmiş Bitiş gibi Microsoft Project tarafından hesaplanan alanlar, içe aktarılırsa yoksayılır. Sabitlenmiş görev başlangıç veya bitiş tarihleriniz varsa Kısıtlama Türü ve Kısıtlama Tarihi alanlarını kullanın.

**Sayısal Görev Tablosu Tanımı:** Bu kayıt, ad yerine sayıların kullanıldığı, içe veya dışa aktarılan görev alanlarını sırayla listeler. Bu, her Görev kaydında yer alan görev alanlarını tanımlamak için alternatif bir yöntemdir ve bir yabancı dil ürünü tarafından oluşturulan bir MPX dosyasını tanımlarken kullanışlıdır.

**Görev:** Bu kayıtlar, içe veya dışa aktarılan her görev için bilgi içerir. Her Görev kaydı bir görevi tanımlar. Bilgileri içe aktardığınızda, dahil edilen alanlar Metin Görev Tablosu Tanımı kaydı veya Sayısal Görev Tablosu Tanımı kaydı tarafından tanımlanır. Bilgileri dışa aktardığınızda, dahil edilen alanlar görev Dışa aktarma tablosunda listelenenlerdir.

**Görev Notları:** Bu kayıtlar, hemen önceki Görev kaydı hakkında notlar içerir. Not içinde yeni bir satırı belirtmek için ASCII karakteri 127'yi kullanın. Not, liste ayırıcı karakteri içeriyorsa, notu tırnak içine alın.

**Kaynak Ataması**: Bu kayıtlar, önceki Görev kaydında tanımlanan göreve atanan kaynaklar hakkındaki bilgileri listeler. Dosyaları birleştiriyorsanız ve kaynak atama bilgilerinin saklanmasını istiyorsanız, bilgileri MPX dosyasına eklemeniz gerekir. Birleştirirseniz, birleştirilmiş görevlerdeki mevcut tüm atamalar silinir. Dosyaları Benzersiz Kimliklere göre birleştiriyorsanız, kaynaklar kimlikler yerine Kaynak Benzersiz Kimlikler kullanılarak atanır.

**Kaynak Atama Çalışma Grubu Alanları:** Bu kayıtlar, Microsoft Project 4.0 ve 4.1'in Çalışma Grubu özellikleri için her atamada depolanan bilgileri listeler. Çalışma Grubu özelliklerini kullanıyorsanız, bilgilerin hiçbirinin kaybolmamasını sağlamak için bu kaydı eklemeniz gerekir.

**Proje Adları:** Bu kayıtlar, projede saklanan tüm DDE bağlantı adlarını listeler.

**DDE ve OLE İstemci Bağlantıları:** Bu kayıtlar, projeye yönelik DDE bağlantılarını listeler.

**Yorumlar:** Bu kayıtlar, dosyaya yorum eklemek için kullanılabilir ve dosyanın herhangi bir konumunda görünebilir. Her Açıklama kaydı "0" ile başlamalıdır.

## MPX dosyasını açma sorunları ##

Ortaya çıkabilecek ve MPX formatının hatalı çalışmasına neden olabilecek bazı yaygın sorunların listesi aşağıdadır:

* Destekleyici yazılımın olmaması
* Bozuk dosya
* Virüs nedeniyle virüslü dosya
* Dosyaları açmak için sistemde erişim hakkı yok
* Sisteminizdeki eski sürücü
* Dosyanın uzantısı yeniden adlandırıldı

## Referanslar ##

* [MPX - Microsoft Bilgi Bankası](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)

