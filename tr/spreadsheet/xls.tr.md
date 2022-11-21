{
  "date" : "2019-12-16",
  "keywords" :[ "XLS", "dosya", "uzantı", "dosya formatı", "Excel", "Elektronik Tablo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"XLS dosyasının ne olduğunu ve bunları oluşturabilen ve açabilen API'leri öğrenmek için dosya biçimi kılavuzunuz.",
  "title" :"XLS dosya formatı nedir? Dosya Formatı Uzmanlarından Öğrenin!",
  "linktitle" : "XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-16"
}

## XLS dosyası nedir?

XLS uzantılı dosyalar, Excel İkili Dosya Biçimini temsil eder. Bu tür dosyalar, Microsoft Excel'in yanı sıra OpenOffice Calc veya Apple Numbers gibi diğer benzer elektronik tablo programları tarafından oluşturulabilir. Excel tarafından kaydedilen dosya, her çalışma kitabının bir veya daha fazla çalışma sayfasına sahip olabileceği Çalışma Kitabı olarak bilinir. Veriler, çalışma sayfasında tablo biçiminde saklanır ve kullanıcılara gösterilir ve sayısal değerler, metin verileri, formüller, harici veri bağlantıları, resimler ve çizelgeleri kapsayabilir. Microsoft Excel gibi uygulamalar, çalışma kitabı verilerini [PDF](/tr/pdf/), [CSV](/tr/spreadsheet/csv/), [XLSX](/tr/spreadsheet/xlsx/), [TXT](/tr/ kelime işlemci/txt/), [HTML](/tr/web/html/), [XPS](/tr/page-description-language/xps/) ve diğerleri. XLS dosya formatı, Microsoft Excel 2007'nin piyasaya sürülmesiyle daha açık ve yapılandırılmış bir format olan XLSX ile değiştirildi. En son sürümler, XLS dosyalarının oluşturulması ve okunması için hala destek sağlıyor, ancak XLSX şu anda ilk kullanım tercihi.

## Kısa Tarihçe

XLS, Microsoft tarafından Microsoft Excel ile kullanılmak üzere oluşturulmuştur ve Binary Interchange File Format (BIFF) olarak da bilinir. Bu dosya türü ilk kez 1987'de Windows için Excel'in bir parçası haline getirilerek tanıtıldı. XLS dosya formatı özellikleri ilk kez Haziran 2008'de Revizyon 1 olarak kamuoyuna açıklandı. Bundan sonra, özellikler sürekli güncellendi ve en son revizyon mevcut Ağustos 2018 itibarıyla Revizyon 8.0 olarak işaretlenmiştir. XLS dosya biçiminin farklı sürümlerinin kısa bir geçmişi aşağıdaki gibidir:

* Versiyon 7.0 (office 95 ile piyasaya sürüldü): Excel'in bu versiyonu, tüm versiyonlar arasında en sağlam ve hızlı olanıydı ve dahili akış yeniden yazma işlemleri 32 bit olarak güncellendi.
* Versiyon 8 (office 97 ile piyasaya sürüldü): VBA standart bir dil olarak sunuldu ve kaldırılan doğal dil etiketleri ilk kez bu versiyona dahil edildi. Aynı zamanda ilk kez bir ataç ofis asistanını da tanıttı.
* Sürüm 9 (Office 2000 ile yayınlandı): Sürüm 9'da yalnızca küçük değişiklikler vardı, burada ataş ofis asistanı daha önce mümkün olmayan birden çok nesneyi aynı anda tutabiliyordu.
* Versiyon 10 (Office XP ile yayınlandı): Bu versiyon gözle görülür bir gelişme içermiyordu.
* Sürüm 11 (Office 2003 ile yayınlandı): Sürüm 11'deki büyük güncelleme, excel 2003, yeni tabloların tanıtımıydı.

## XLS Dosya Biçimi Özellikleri ##

Veriler, bir XLS dosyasında, [MS-CFB]'de açıklandığı gibi bir bileşik dosya biçiminde ikili akışlar olarak düzenlenir. Veriler, çalışma sayfası tanımları gibi çalışma kitabı verileri de dahil olmak üzere bir çalışma kitabının içeriği ve yapısı hakkında bilgi içeren depolar, akışlar ve alt akışlar kullanılarak bileşik dosyada depolanır. Her akış veya alt akış, bir dizi ikili kayıt içerir. Her ikili kayıt, çalışma kitabı verilerini içeren sıfır veya daha fazla yapılandırılmış alan içerir. Bu bölüm, XLS Dosya Yapısına kısa bir genel bakış sağlar, ancak ayrıntılı dosya formatı özellikleri için [XLS Dosya Oluşumu Spesifikasyonlarına](https://msdn.microsoft.com/en-us/library/cc313154(v#office) bakılmalıdır. .12).aspx) Microsoft tarafından belgelenmiştir.

#### Akış ve Alt Akış ####

Bir çalışma kitabı, çalışma kitabı akışı tarafından temsil edilir. Bir çalışma kitabındaki her çalışma sayfası, Alt Akışlar tarafından temsil edilir. Ek olarak, Küresel Alt Akışı izleyen Grafik Sayfası Alt Akışı, Makro Sayfası Alt Akışı veya İletişim Sayfası Alt Akışı vardır. Çalışma kitabı verilerini içeren her bir ikili akış veya alt akış, bir dizi ikili kayıt olarak YAZILMALIDIR ZORUNLU.

#### Kayıt ####

Bir çalışma kitabındaki özellikler hakkındaki bilgiler, değişken uzunluklu bir bayt dizisi olan bir kayıt olarak depolanır. Bir ikili kayıt aşağıdaki üç bileşenden oluşur:

**Kayıt Türü:** Kayıt türü, kayıt tarafından ne tür bilgilerin belirtildiğini ve bu kayda özel kayıt verilerinin yapısının nasıl sıralanıp yapılandırıldığını belirten iki baytlık işaretsiz bir tam sayıdır. Kayıt türü değerleri, Kayıt Numaralandırmasından (bölüm 2.3) bir değer OLMALIDIR veya kayıt, gelecekteki kayıt mimarisini KULLANMALIDIR (bölüm 2.1.6).

**Kayıt Boyutu**: Kayıt boyutu, kayıt verilerinin toplam boyutunu belirten bayt sayısını belirten iki baytlık işaretsiz bir tam sayıdır. Kayıt boyutu 0'dan büyük veya eşit OLMALIDIR ve 8224'ten küçük veya eşit OLMALIDIR.

**Kayıt Verisi:** Kayıt verisi bileşeni, belirli bir kayıt türüne karşılık gelen ve kaydın geri kalanını oluşturan alanlar içerir. Belirli bir kayıt türü için alanların sırası ve yapısı, o kayıt türü için ilgili bölümde belirtilir. Kayıt veri bileşeninin boyutu, kayıt boyutuna eşit OLMALIDIR. Kayıt verileri bileşenindeki alanlar, basit değerler, değer dizileri, çeşitli alanların yapıları, alan dizileri ve yapı dizileri içerebilir.

#### Hücre Tablosu ####

Hücreler, metin, formüller ve sayısal veriler gibi çalışma kitabı içeriklerini depolayan bir çalışma kitabının temel bloklarıdır. Hücreler, depolanan verilerin kaydını Hücre Tablosu adı verilen bir veri yapısı aracılığıyla tutar. Hücre Tablosunun kendisi, spesifikasyonlar belgesinde tanımlanan CELLTABLE kurallarına uyan kayıt dizisinde saklanır. Sıraların sıra blokları halinde düzenlendiği bir dizi sıra bloğundan oluşur. Her satır bloğu, veri içeren ilk satırdan veri içeren son satıra kadar satırlar içerir.

Veri veya satır biçimlendirmesi, her satır bloğu için bir Satır kaydına kaydedilir. Veri veya bireysel hücre biçimlendirmesi içeren her hücre, bir kayıtla temsil edilir. Bir hücreyle ilişkili biçimlendirme, tek tek hücre biçimlendirmesinden, satır biçimlendirmesinden, sütun biçimlendirmesinden veya varsayılan hücre biçiminden türetilebilir. Biçimlendirme için öncelik sırası, en yüksek önceliğe sahip bireysel hücre biçimlendirmesidir, ardından satır biçimlendirmesi ve ardından sütun biçimlendirmesi ve ardından varsayılan hücre biçimi gelir. Veri içermeyen ve bireysel biçimlendirme içermeyen hücreler kaydedilmez.

#### Formüller ####

Formül, bir hücrede birlikte yeni bir değer üreten değerler, hücre başvuruları, adlar, işlevler veya işleçler dizisidir. Formüller, "ayrıştırılmış ifadeler" olarak bilinen simgeleştirilmiş bir temsilde saklanır. Ayrıştırılmış bir ifade, görüntüleme ve kullanıcı düzenlemesi için çalışma zamanında bir metin formülüne dönüştürülür. Hücre formülleri, Formül kaydı tarafından belirtilir. Dizi formülleri, Dizi kaydı tarafından belirtilir. Paylaşılan formüller ShrFmla kaydı tarafından belirtilir.

#### Grafikler ####

Grafik sayfası, bir grafiği, verileri veya veri kümeleri arasındaki ilişkileri görsel bir biçimde görüntüleyen bir grafiği ve bir grafik veri önbelleğini, grafik verilerinde kullanılan verilerin yerel bir kopyasının eksik olduğunu veya harici bağlantılara bağlantılar varsa belirtir. veri kaynakları bozuk. Grafik, bir veya iki eksenli grupları, grafik verilerinin çizildiği bir eksen kümesini ve grafikte belirtilen seri, eğilim çizgileri ve hata çubuğunu belirtir. Her eksen grubu, verileri görüntülemek için kullanılan görselleştirme türünü belirten bir ila dört grafik grubunu belirtir. Her seri, trend çizgisi ve hata çubuğu, ilişkili olduğu bir grafik grubunu belirtir.

#### Meta veri ####

Meta veriler, belirli bir hücre veya içeriğiyle ilişkili ek verilerdir. Meta veriler, yalnızca gelecekteki genişletilebilirlik amaçları için BIFF8'e kaydedilir.

#### Özet Tablolar ####

PivotTable, bu verilerin dağılımına ilişkin genel bir bakış elde etmek için kaynak verileri özetleyen bir mekanizmadır. Bir PivotTable'da, kaynak verilerin uygulanabilir sütunları, verileri özetlemek için kullanılabilecek alanlar haline gelir. PivotTable'ın kaynak verileri OLAP kaynak verileri olduğunda, OLAP hiyerarşileri ve diğer bazı OLAP varlıkları PivotTable'da alanlar haline gelir.
PivotTable'ın iki ana bölümü vardır: PivotCache ve PivotTable görünümü. OLAP olmayan tek bir PivotCache'i temel alan birden çok PivotTable görünümü olabilir.

#### Stiller ####

Bu genel bakışta, bir sayfadaki (1) hücreler için biçimlendirme ve koruma bilgilerinin nasıl belirlendiği açıklanmaktadır. Hücre biçimlendirme birkaç özellik grubundan oluşur:

* Yazı tipi özellikleri (kalın, italik, yazı tipi rengi, yazı tipi boyutu vb…)
* Dolgu özellikleri (ön plan rengi, arka plan rengi, desen, gradyan vb…)
* Hizalama özellikleri (sola, merkeze, sağa hizalama vb…)
* Kenarlık özellikleri (sol, sağ, üst, alt, kalın veya ince, renkli, vb…)
* Sayı biçimlendirme özellikleri (tarih, saat, ondalık basamak sayısı, vb…)
* Koruma özellikleri (kilitli, gizli, vb…)

Bu özellikler bir bütün olarak belirli bir hücrenin nasıl görüntülendiğini ve yazdırıldığını açıklar.

## Referanslar ##

* [[MS-XLS] - Excel İkili Dosya Biçimi Yapısı](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[MS-CFB] - Bileşik Dosya İkili Dosya Biçimi](https://msdn.microsoft.com/en-us/library/dd942138.aspx)

