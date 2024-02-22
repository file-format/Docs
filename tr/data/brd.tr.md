{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "BRD Dosyası - EAGLE Circuit Board Dosyası - .brd dosyası nedir ve nasıl açılır?",
  "description" : "BRD EAGLE Devre Kartı Dosyası ve nasıl açılacağı hakkında bilgi edinin.",
  "linktitle" : "BRD",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-brd-tr",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## .BRD dosyası nedir?

Baskılı devre kartı (PCB) tasarımına yönelik elektronik tasarım otomasyonu (EDA) yazılımında bir BRD dosya formatı kullanılır. Eagle, KiCad, Altium Designer ve diğerleri gibi PCB tasarım yazılımları, baskılı devre kartının düzenini, bağlantılarını ve tasarımla ilgili diğer bilgilerini depolamak için bu dosya formatını kullanır.

BRD dosyası, mühendisler ve tasarımcılar tarafından tasarımları oluşturmak, değiştirmek ve analiz etmek için kullanılan dijital dosyalar olan bir CAD dosyası türüdür. BRD dosyası, elektronik endüstrisinde baskılı devre kartlarının (PCB'ler) tasarımı için yaygın olarak kullanılan yazılım uygulaması olan Autodesk EAGLE ile ilişkilidir. Autodesk EAGLE, hem şematik yakalama (devrenin görsel temsilinin oluşturulması) hem de PCB düzeni (bileşenlerin düzenlenmesi ve bağlantıların yönlendirilmesi) için araçlar sağlar.

BRD dosyası, Autodesk EAGLE yazılım paketinin bileşeni olan EAGLE Layout Editor kullanılarak oluşturulur. Bu düzenleyici, kullanıcıların bileşenleri yerleştirme, izleri yönlendirme, tasarım kurallarını tanımlama ve üretim için gerekli dosyaları oluşturma dahil olmak üzere PCB düzenini tasarlamasına olanak tanır.

BRD dosyaları, PCB'deki elektronik devre tasarımı için şablon veya plan görevi görür. Tasarımcılar, şematik diyagramlarını üretilebilecek fiziksel düzenlere dönüştürmek için EAGLE ve .brd dosyalarını kullanır.

.BRD dosyaları Gerber sondaj veri formatında kaydedilebilir. Gerber dosyaları, PCB tasarımının desenlerini, katmanlarını ve özelliklerini tanımlamak için PCB üretiminde kullanılan standart formattır. .brd dosyalarının bu formatta kaydedilmesi, bunların PCB üretimi için gerekli talimatları üreten bilgisayar destekli üretim (CAM) programları tarafından kullanılmasına olanak tanır.

## BRD Dosya Görüntüleyici

.brd dosyalarını görüntülemek için kullanıcıların Autodesk EAGLE gibi yazılımlarla oluşturulan PCB düzenlerini görselleştirmesine ve incelemesine olanak tanıyan çeşitli yazılım araçları mevcuttur.

1.  **Autodesk EAGLE**: Autodesk EAGLE'ye erişiminiz varsa, .brd dosyalarını görüntüleme ve düzenleme amacıyla doğrudan yazılımın içinden açabilirsiniz.
    
2.  **KiCad**: KiCad, PCB düzen düzenleyicisini içeren açık kaynaklı bir EDA yazılım paketidir. Autodesk EAGLE ile oluşturulan .brd dosyalarını içe aktarma ve görüntüleme özelliğine sahiptir.
    
3.  **ViewPlot**: ViewPlot, .brd dahil olmak üzere çeşitli PCB dosya formatlarını destekleyen bağımsız Gerber görüntüleyicisidir. Kullanıcıların orijinal tasarım yazılımına ihtiyaç duymadan PCB tasarımlarını görüntülemesine olanak tanır.
    
4.  **GC-Prevue**: GC-Prevue, .brd dosyalarını da işleyebilen başka bir popüler Gerber görüntüleyicidir. PCB düzenlerini görselleştirmek, mesafeleri ölçmek ve tasarım ayrıntılarını incelemek için özellikler sağlar.
    
5.  **Gerbv**: Gerbv, Gerber formatında kaydedilen .brd dosyalarını içerebilen Gerber dosyalarının görüntülenmesini destekleyen açık kaynaklı bir Gerber görüntüleyicisidir.
    
6.  **Çevrimiçi Görüntüleyici Araçları**: .brd dosyalarını doğrudan web tarayıcınıza yüklemenize ve görüntülemenize olanak tanıyan çevrimiçi araçlar da mevcuttur. Böyle bir örnek, Gerber ve .brd dahil olmak üzere çeşitli PCB dosya formatlarının görüntülenmesini destekleyen EasyEDA'nın Çevrimiçi Gerber Görüntüleyicisidir.

## .BRD dosyası nasıl açılır?

PCB tasarımında kullanılan BRD dosyaları çeşitli PCB tasarım uygulamalarında açılabilir.

- **Autodesk EAGLE**: Autodesk tarafından geliştirilen çapraz platformlu PCB tasarım yazılımıdır. Şematik diyagramların, PCB düzenlerinin oluşturulmasını ve elektrik bağlantılarının yönlendirilmesini destekler. Kullanıcılar, görüntülemek ve daha fazla düzenleme yapmak için .brd dosyalarını doğrudan Autodesk EAGLE içinden açabilir.
    
- **Altium Designer**: Altium Designer, öncelikle Windows işletim sistemlerine yönelik kapsamlı bir PCB tasarım yazılımıdır. Şematik yakalama, PCB düzeni ve tasarım analizi için geniş bir özellik yelpazesi sunar. Altium Designer ayrıca .brd dosyalarının açılmasını da destekleyerek kullanıcıların başka yazılımlarda oluşturulan tasarımları içe aktarmasına ve bunlarla çalışmasına olanak tanır.
    
- **Open Board Viewer**: Open Board Viewer, özellikle Linux işletim sistemleri için tasarlanmış bir PCB görüntüleme yazılımıdır. Kullanıcıların PCB düzenlerini görselleştirmesine, bileşenleri incelemesine ve yönlendirme ayrıntılarını incelemesine olanak tanıyan açık kaynaklı bir araçtır. Open Board Viewer, .brd dosyalarının açılmasını destekleyerek Linux platformlarındaki kullanıcıların diğer yazılımlarda oluşturulan tasarımları görüntülemesine ve analiz etmesine olanak tanır.

BRD dosyalarını açmak için kullanabileceğiniz programların listesi.

- **Autodesk EAGLE** (Ücretsiz Deneme) (Windows, Mac, Linux) için
- **Altium Designer** (Ücretsiz Deneme) (Windows, Mac, Linux) için
- **Linux için Açık Pano Görüntüleyici** (Ücretsiz)

## Referanslar
* [EAGLE programı](https://en.wikipedia.org/wiki/EAGLE_(program))


