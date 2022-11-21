{
  "date" : "2021-06-30",
  "keywords" :[ "msi dosyası", "MSI dosya biçimi", "msi dosyası nedir", "dosya", "msi örneği", "msi dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"MSI dosya formatı ve MSI dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"MSI - Windows Installer Paket Dosyası",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## MSI dosyası nedir?
Windows programlarını yüklemek ve başlatmak için kullanılan bir MSI dosyası; yüklenecek temel dosyalar ve yükleme yeri hakkında bilgiler dahil olmak üzere tipik bir yazılım programı için yükleme bilgilerini içeren eksiksiz bir Microsoft Windows paketi. MSI dosyaları, yazılım güncellemeleri paketini de içerebilir. MSI dosyaları [EXE](/tr/executable/exe/) dosyasına benzer, ancak EXE bazen yükleyici bilgilerini içermeyebilir ve EXE dosyası çalıştırıldığında yazılım programı doğrudan çalışabilir.

## MSI dosya formatı
Windows Installer aslında bir yazılım programının yüklenmesi, kaldırılması ve bakımı için kullanılan Microsoft Windows'un bir API'si (Uygulama Programlama Arayüzü) ve yazılım bileşenidir. Kurulum bilgileri ve isteğe bağlı dosyalar, kurulum paketleri ve COM Yapılandırılmış Depolar olarak yapılandırılmış gevşek ilişkisel veritabanları olarak paketlenir; **MSI dosyaları** olarak bilinir ve .msi dosya uzantısına sahiptir. **.mst** dosya uzantılı paketler Windows Installer'ın **Transformation Scripts**'ini içerir, **.msm** uzantılı dosyalar **Merge Modules** ve **.pcp** dosya uzantısını içerir **Yama Oluşturma Özellikleri** için kullanılır. Windows Installer, önceki sürümleri olan Setup API'den önemli değişiklikler yaptıktan sonra daha gelişmiş hale geldi. Bir GUI çerçevesi ve kaldırma sırasının otomatik olarak oluşturulması, Windows Installer'ın yeni özellikleridir. Artık bağımsız yürütülebilir yükleyici çerçevelerine bir alternatif olarak kabul edildi.

### MSI paketlerinin mantıksal yapısı
Bir paket, bir veya daha fazla eksiksiz ürünün kurulumunu belirtir ve genellikle bir **GUID** ile tanımlanır. Bir ürün, bir veya daha fazla bileşenden oluşur ve çeşitli özelliklere göre gruplandırılır. Windows Installer, çeşitli ürünler arasındaki bağımlılıkları aynı anda işlemez. Paketlerin mantıksal yapısı aşağıdaki unsurlardan oluşur:

- **Ürünler**: Tek, yüklü, çalışan bir program veya bir araya getirilmiş birden çok program grubu bir üründür. Bir ürün benzersiz bir GUID ile tanımlanır.
- **Özellikler**: Herhangi bir sayıda bileşen ve diğer alt özellikleri içerebilir. Daha küçük paketler tek bir özellikten oluşabilir.
- **Bileşenler**: Bileşen, Windows Installer tarafından bir birim olarak ele alınır; program dosyaları, klasörler, kayıt defteri anahtarları, COM bileşenleri ve kısayollar içerebilir.
- **Anahtar Yolları**: Anahtar yolu, paket yazarının belirli bir bileşen için kritik olarak belirttiği belirli bir dosya, ODBC veri kaynağı veya kayıt defteri anahtarıdır.

## Referanslar

* [Windows Installer - Wikipedia'dan](https://en.wikipedia.org/wiki/Windows_Installer)


