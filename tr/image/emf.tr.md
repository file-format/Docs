{
  "date" : "2019-10-11",
  "keywords" :[ "emf dosyası", "emf dosya biçimi", "emf dosyası nedir", "dosya", "emf örneği", "emf dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF - Gelişmiş Meta Dosya Biçimi",
  "description":"EMF dosya formatı ve EMF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .emf dosyası nedir?

**Geliştirilmiş meta dosyası biçimi (EMF)** grafik görüntüleri cihazdan bağımsız olarak depolar. EMF'nin meta dosyaları, herhangi bir çıkış aygıtında ayrıştırıldıktan sonra saklanan görüntüyü işleyebilen, kronolojik sırayla değişken uzunluklu kayıtlardan oluşur. Bu değişken uzunluklu kayıtlar, kapalı nesnelerin tanımları, çizim komutları ve görüntüyü doğru bir şekilde işlemek için kritik olan grafik özellikleri olabilir. Bir aygıt, kendi grafik ortamını kullanarak bir EMF meta dosyasını açtığında, orijinal görüntünün oranları, boyutları, renkleri ve diğer grafik özellikleri, açılan aygıt platformundan bağımsız olarak aynı kalır.

## Kısa Tarih ##

1990'da Microsoft, Microsoft Windows için bir görüntü dosyası biçimi Windows Meta Dosyası ([WMF](/tr/image/wmf/)) tasarladı. Windows Meta Dosyaları, bazı bitmap bileşenleri içerebilen 16-bit biçimidir. WMF, vektör grafiklerinden oluşabilir ve farklı uygulamalar arasında taşınabilir olması amaçlanır. 1993'te Win32/GDI, gelişmiş esneklik ve ölçeklenebilirliğe sahip daha yeni bir sürüm olan Gelişmiş Meta Dosyasını (EMF) duyurdu. EMF, yazıcı sürücülerini çalıştırmak için grafik dili komutları olarak da kullanılır. Microsoft artık Windows biçimi (WMF) yerine gelişmiş meta dosyası biçimini (EMF) önermektedir. Windows XP tanıtıldığında, Enhanced Metafile Format Plus (EMF+) sürümü yayınlandı. Bu daha yeni sürüm, GDI+ API çağrılarını aynı şekilde WMF/EMF kayıtlarının GDI'ye yaptığı çağrıları serileştirerek yolunu bulur. EMZ olarak bilinen EMF'nin gzip ile sıkıştırılmış bir sürümü vardır.

## EMF Meta Dosyası Formatı ##

Gelişmiş meta dosyası biçiminin temel öğeleri aşağıdadır:

* Bir EMR_HEADER (sürüm, boyut, oluşturma sırasında resmin çözünürlüğü)
* GDI nesneleri için bir tablo
* Ayrılmış bir palet (isteğe bağlı)
* Dizi yapısında düzenlenmiş meta dosya kayıtları (özellik ayarları, tanımlanmış nesneler, çizim komutları)
* EMR_EOF kaydı (EMF meta dosyasındaki son kayıt)

## EMF Sürümleri ##
* **Orijinal**: Orijinal sürüm, orijinal görüntüyü tutmak ve cihazdan bağımsız olarak sürdürmek için gerekli kaydı belirtir. Ayrıca çizim için grafik nesneleri ve komutları içeren kaydı destekler.
* **Sürüm 1**: EMF'nin ikinci sürümü, piksel formatı için kayıt ve OpenGL komutunu kullanma hükmü ekleyerek esnekliği ve cihaz bağımsızlığını iyileştirdi.
* **Sürüm 2**: Üçüncü sürüm, cihazın yüzey mesafelerini ölçmek için Metrik sistemi ekleyerek doğruluğu artırdı ve kaydı daha ölçeklenebilir hale getirdi.

## Gelişmiş Meta Dosya Kayıtları ##

Meta dosyası kayıtları dizi şeklinde düzenlenir. Bu kayıtlar ENHMETARECORD yapısına sahiptir ve uzunlukları değişkendir. ENHMETARECORD, gelişmiş meta dosyası biçimini kullanarak bir resim oluşturmak için GDI işlevlerini tanımlayan verileri belirtir. **ENHMETAHEADER** yapısı bu formatta her zaman ilk kayıttır. Bu EMF başlığı aşağıdaki bilgileri içerir.

Gelişmiş meta dosyasının her kaydı, başlangıçta iki EMR üyesine (temel yapıyı sağlar) sahiptir. İlk üye, kayıt türünü belirleyen ve iType olarak bilinen GDI işlevini (parametreler kayıtta kullanılır) tanır. Diğer üye nSize, her kaydın boyutunu tanımlar. Kalan parametreler (varsa) ve ek veriler nSize'ın hemen altında düzenlenir. Başlığın hemen ardından isteğe bağlı bir metin açıklaması sunulabilir. Resmin ve yazarın adı bu metin açıklamasına kaydedilir. Varlığı bir seçenek olan palet, gelişmiş meta dosyası oluşturmada kullanılan renkleri belirtir. Resim oluşturmada gerekli olan GDI işlevini belirtmek için kullanılan diğer kayıtlar.

Her meta dosyasında en az bir EMF kaydı bulunmalıdır. Bir kayıttan diğerine geçiş bilgisi EMF kayıtlarına bağlıdır, dolayısıyla bu kayıtlar bitişik olarak düzenlenmelidir. EOF_record dışında meta dosyasındaki herhangi bir kayıtta, söz konusu kaydın uzunluğu bir sonraki kayda geçmek için tanımlanır.

## Gelişmiş Meta Dosyası Oluşturma ##

**CreateEnhMetaFile** işlevi, gelişmiş bir meta dosyası oluşturmak için kullanılır. Bu işlev bağımsız değişkenleri, resmin boyutları ve diskte/bellekte depolanması için kullanılır. Ayrıca bu fonksiyon, resmin ilk göründüğü cihazın boyutunu (referans verilen cihaz) ve referans cihazın (DC) içeriğini gerektirir. Bu nedenle, **CreateEnhMetaFile** işlevi çağrılırken bu DC'yi işlemek için argümanlar sağlanmalıdır. Fonksiyon sözdizimi aşağıdaki gibidir:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** bir referans cihaza işleyin.

**lptoFilename:** Dosya adına bir işaretçi.

**lprc:** Oval yapı işaretçisi, resim boyutlarını mm cinsinden belirtir.

**lpDesc:** resmin başlığı ve resmi oluşturan uygulama adı için bir dizge işaretçisi.

## Gelişmiş Meta Dosyası İşlemleri ##

Aşağıda, geliştirilmiş bir meta dosyası tanıtıcısı kullanılarak gerçekleştirilebilecek işler yer almaktadır.

* Saklanan resim için görüntüleyin ve düzenleyin.
* Geliştirilmiş meta dosyası kopyaları üretin.
* Bir EMF başlığının kopyasını, isteğe bağlı açıklamayı ve gelişmiş bir meta dosyasının ikili sürümünü alın
* Paletteki renkleri özetleyin.

## Grafik Nesneleri ##

Çizim ve boyama işlemlerinde, nesne oluşturma kayıtları ile grafik nesneleri oluşturulabilir ve daha sonra kullanılmak üzere kaydedilebilir. Bir "EMR_SELECTOBJECT" kaydı, oynatma cihazı bağlamını kullanarak bu grafik nesnelerini alabilir. Kalemler, paletler, fırçalar, renk uzayları, yazı tipleri ve hazır nesneler bazı yeniden kullanılabilir nesne türleridir.

## Bayt Sıralama ##

Little-endian biçimi, verileri meta dosyası kayıtlarında depolamak için kullanılır.

## sürüm oluşturma ##

EMF dosya biçimi iki kez revize edilmiştir. Değiştirilen sürümler orijinal, uzantı 1 ve uzantı 2'dir. Genişletilmiş sürümlerde OpenGL kayıtları ve dahili piksel formatı için isteğe bağlı bir tanımlayıcı bulunur. Görüntülenen boyutlar için mililitre cinsinden bir ölçüm özelliği eklenir.

## Referanslar ##

* [Gelişmiş Biçimli Meta Dosyalar | Microsoft Belgeleri](https://docs.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [Geliştirilmiş Meta Dosyası Formatı ve Özelliği](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

