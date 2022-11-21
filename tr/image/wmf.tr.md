{
  "date" : "2019-10-11",
  "keywords" :[ "wmf dosyası", "wmf dosya biçimi", "wmf dosyası nedir", "dosya", "wmf örneği", "wmf dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF - Microsoft Windows Meta Dosyası Biçimi",
  "description":"WMF dosya formatı ve WMF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Bir WMF dosyası nedir?

WMF uzantılı dosyalar, vektörün yanı sıra bitmap biçimindeki görüntü verilerini depolamak için Microsoft Windows Meta Dosyasını (WMF) temsil eder. Daha doğru olmak gerekirse, WMF, cihazdan bağımsız Grafik dosya formatlarının vektör dosya formatı kategorisine aittir. Windows Grafik Aygıt Arabirimi (GDI), ekranda bir görüntü görüntülemek için bir WMF dosyasında saklanan işlevleri kullanır. Gelişmiş Meta Dosyaları (EMF) olarak bilinen WMF'nin daha gelişmiş bir sürümü daha sonra yayınlandı ve biçimi daha zengin özelliklere sahip hale getirdi. Pratik olarak WMF, SVG'ye benzer.

## WMF Dosya Biçimi Özellikleri ##

Windows 3.0 ile başlatıldığı sırada 16 bitlik dosya biçimine atıfta bulunan bir WMF dosyası. Dosya formatı, grafik çizim komutlarını, nesne tanımlarını ve özelliklerini içeren bir dizi değişken uzunluklu kayıttan oluşur. WMF dosyaları, görüntüyü çizmek için GDI'ya işlenen komutları temel aldığından, görüntünün yeniden üretilmesi için oynatılabilen görüntünün dijital kaydı olarak da bilinir. WMF'nin tam dosya biçimi belirtimleri çevrimiçi olarak mevcuttur ve WMF dosyalarıyla çalışacak uygulamaların geliştirilmesi için başvurulmalıdır. Bir WMF dosyası şu şekilde düzenlenir:

* WMF Başlık Kaydı
* WMF Kaydı (ları)
* WMF Dosya Sonu Kaydı

### WMF Başlık Kaydı ###

**META_HEADER Kaydı**, aşağıdakiler dahil olmak üzere meta dosyasının özelliklerini tanımlayan bilgileri içerir:

* Meta dosyasının türü
* Meta dosyasının sürümü
* Meta dosyasının boyutu
* Meta dosyasında tanımlanan nesnelerin sayısı
* Meta dosyasındaki en büyük tek kaydın boyutu

### WMF Yerleştirilebilir Başlık Kaydı ###

**META_PLACEABLE Kaydı**, aşağıdakiler de dahil olmak üzere görüntüyle ilgili genişletilmiş bilgiler içerir:

* Sınırlayıcı bir dikdörtgen
* Ölçeklendirme için mantıksal birim boyutu
* Doğrulama için bir sağlama toplamı

### WMF Kaydı ###

WMF kayıtları, özellikler belgesinde belirtilen genel bir biçime sahiptir. Her WMF kaydı aşağıdaki bilgileri içerir:

* Kayıt boyutu
* Kayıt fonksiyonu
* Kayıt fonksiyonu için varsa parametreler

## Referanslar ##

* [[MS-WMF]: Windows Meta Dosyası Biçimi](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Windows Meta Dosyası - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

