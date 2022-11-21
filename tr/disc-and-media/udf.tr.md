{
  "date" : "2021-08-17",
  "keywords" :[ "udf dosyası", "udf dosya biçimi", "udf dosyası nedir", "dosya", "udf örneği", "udf dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"UDF dosya formatı ve UDF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"UDF - Evrensel Disk Biçimi Dosyası",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## UDF dosyası nedir?
.udf uzantılı dosya, tipik olarak dosyaları optik ortama kaydetmek için kullanılan bir disk görüntüleme biçimidir; DVD'leri, CD'leri ve diğer optik ortamları yazmak için kullanılabilir; UDF standardında belirtilen dizin yapısını kullanarak bir dosya koleksiyonunu depolar; dosyaların yazıldıktan sonra bile hedef diskte silinmesine ve değiştirilmesine izin verir. Optical Storage Technology Association, yeniden yazılabilir optik ortam ve salt okunur ortam gibi tüm optik ortamlar için ortak bir dosya sistemi oluşturmak üzere UDF dosya sistemini bir standart olarak belirledi.

## UDF dosya biçimi
UDF dosya biçimi, çok çeşitli ortamlar için bilgisayar verilerinin depolanması için satıcıdan bağımsız açık bir dosya sistemidir. DVD'ler ve daha yeni optik disk formatları için yaygın olarak kullanılmıştır. Genellikle, yazılım toplu işlemde bir UDF dosya sistemini yönetir ve bunu tek bir geçişte optik ortama yazar. Bununla birlikte, paketleri yeniden yazılabilir ortama yazdığında, UDF, flash sürücüler veya disketler gibi çıkarılabilir ortamlarda genel amaçlı bir dosya sistemine benzer şekilde dosyaların disk üzerinde oluşturulmasına, silinmesine ve değiştirilmesine izin verir.
### UDF Spesifikasyonları
UDF standardı, aşağıdaki üç dosya sistemi varyasyonunu tanımlar:

- **Düz Yapı**: Bu, tüm UDF düzeltmelerinde desteklenen orijinal biçimdir. Standardın ilk sürümünde tanıtıldı, bu biçim, DVD+RW, sabit diskler ve DVD-RAM ortamı gibi rastgele okuma veya yazma erişimi sağlayan herhangi bir disk türünde kullanılabilir.
- **KDV oluşturma**: Bir kez yazılan ortama yazmak için özel olarak kullanılır. VAT, diskte paket yazmaya izin veren ek bir yapıdır; yani, diskteki dosyalar veya diğer veriler değiştirildiğinde veya silindiğinde fiziksel blokların yeniden eşlenmesi. Bir kez yazılabilen ortamlar için, diskin tamamı sanallaştırılır ve bir kez yazılır özelliği kullanıcı için şeffaf hale getirilir; disk, yeniden yazılabilir bir diske davranıldığı gibi işlenebilir.
- **Ayrılmış (RW) yapı**: Özellikle yeniden yazılabilir ortama yazmak için kullanılır. Diskin birden çok kez yeniden yazılan bölümlerinde meydana gelecek hataları yönetmek için fazladan bir Yedekleme Tablosu ekler. Bu tablo, aşınmış sektörlerin izini kaydeder ve onları çalışan sektörlere yeniden eşler. UDF'nin kusur yönetimi, optik diskler için Mount Rainier (MRW) veya bir sabit sürücü için bir disk denetleyicisi gibi halihazırda başka bir kusur yönetimi biçimi uygulayan sistemler için geçerli değildir.
 




## Referanslar


* [Windows Görüntüleme Biçimi - Wikipedia'dan](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


