{
  "date" : "2019-10-11",
  "keywords" :[ "chm","chm dosyası", "chm dosya biçimi", "chm dosya türü", "dosya", "tür", "chm dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CHM - Derlenmiş HTML Yardım Dosyası Biçimi",
  "description" :"CHM dosyası nedir ve bunları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CHM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .chm dosyası nedir?

CHM dosya biçimi, bir HTML sayfaları koleksiyonundan oluşan Microsoft **[HTML](/tr/web/html/)** yardım dosyasını temsil eder. Konulara hızlı erişim ve yardım belgesinin farklı bölümlerinde gezinme için bir dizin sağlar. CHM dosyası, sağlanan arama seçeneği aracılığıyla içerik için aranabilir. CHM, genellikle yazılım belgeleri için kullanılan Microsoft Tescilli çevrimiçi yardım dosyası biçimidir. Ayrıca eğitim kılavuzları, etkileşimli kitaplar ve elektronik haber bültenleri gibi diğer birçok uygulamada kullanılır. Modern Microsoft Geliştirme ortamlarının çoğu, uygulamada bulunan bilgilerden CHM belgeleri oluşturmayı destekler.

CHM dosya biçiminin birleşik bir içindekiler tablosu ve dizin uygulama konusundaki benzersiz yeteneği, onu diğer standart HTML sayfalarından farklı kılar. Oluşturulan CHM dosyasının boyutu nispeten küçüktür ve bu nedenle yazılım paketleri ile kolayca dağıtılabilir. Yardım yazma aracı HTML Help Workshop, yardım projelerini ve ilgili dosyalarını oluşturmak ve yönetmek için kullanımı kolay bir sistem sağlar. CHM dosyaları metin, resimler ve köprüler içerebilir; bir Web tarayıcısında görüntülenebilir; Windows ve diğer programlar tarafından çevrimiçi yardım çözümü olarak kullanılır.

## CHM Dosya Biçimi

Oluşturulan CHM dosyasının son biçimi, yardım sisteminin nasıl tasarlandığına ve bunun bir uygulama mı yoksa bir web sitesi için mi tasarlandığına bağlıdır. Bir CHM dosyası, sıkıştırılmış HTML dosyalarını oluşturmak için LZX sıkıştırmasıyla veri sıkıştırmayı destekler. Birden çok .CHM dosyasını birleştirme özelliğinin yanı sıra içeriklerin hızlı aranması için yerleşik arama motoruna sahiptir. Bir CHM dosyası, bir dizi HTML dosyasından, bağlantılı bir içindekiler tablosundan ve bir dizin dosyasından oluşur.

### HTML Dosyaları

İster bir programla dağıtmak için yardım konuları oluşturuyor olun, ister Web'de, yazdığınız belgeler, Köprü Metni Biçimlendirme Dili (HTML) olarak bilinen özel bir biçimlendirme dili kullanılarak oluşturulur. HTML konu dosyalarının .htm veya .html dosya adı uzantısı vardır.

Yazdığınız her yardım konusu veya Web sayfası, üzerinde metin, grafik veya hareketli resimler bulunan bir belge gibi görünse de, .htm dosyaları aslında özel HTML biçimlendirme kodlarına sahip metin belgeleridir. Etiketler adı verilen bu kodlar, bir tarayıcıya her sayfayı nasıl görüntüleyeceğini söyler. Yalnızca bir konuda veya Web sayfasında görünen metin aslında .htm dosyasındadır. Görünen tüm grafikler, sesler, animasyonlu resimler veya diğer öğeler, HTML dosyanızın işaret ettiği ayrı dosyalardır. Tarayıcı, bunu yapmasını söyleyen etiketleri gördüğünde grafikleri, sesleri veya diğer öğeleri kopyalar veya indirir.

### İçindekiler Tablosu (TOC)
Yardım içindekiler tablosu (.hhc) dosyası, içindekiler tablonuz için konu başlıklarını içeren bir HTML dosyasıdır. Bir kullanıcı, derlenmiş bir yardım dosyasındaki (veya bir Web sayfasındaki) içindekiler tablosunu açıp bir konu başlığını tıklattığında, o başlıkla ilişkili HTML dosyası açılır.

### Dizin Dosyası
Dizin (.hhk) dosyası, dizininiz için dizin girişlerini (anahtar sözcükler) içeren bir HTML dosyasıdır. Bir kullanıcı derlenmiş bir yardım dosyasında veya bir Web sayfasında dizini açtığında ve bir anahtar kelimeyi tıklattığında, anahtar kelimeyle ilişkili HTML dosyası açılır.

## HTML Yardım Bileşenleri

HTML Yardımı birkaç bileşenden oluşur. Bunlar aşağıdakileri içerir:

* `HTML Yardım Atölyesi`: proje dosyaları, HTML konu dosyaları, içerik dosyaları, indeks dosyaları ve çevrimiçi bir yardım sistemi veya Web sitesi oluşturmak için ihtiyaç duyduğunuz diğer her şeyi oluşturmak için kullanımı kolay bir grafik arayüze sahip bir yardım yazma aracı .
* `HTML Yardımı ActiveX kontrolü`: yardım navigasyonu ve ikincil pencere işlevselliğini bir HTML dosyasına eklemek için kullanılan küçük, modüler bir program.
* `HTML Yardım Görüntüleyicisi`: çevrimiçi yardım konularının görünebileceği tamamen işlevsel ve özelleştirilebilir üç bölmeli bir pencere.
* `Microsoft HTML Help Image Editor`: ekran görüntüleri oluşturmak için çevrimiçi bir grafik aracı; ve görüntü dosyalarını dönüştürmek, düzenlemek ve görüntülemek için.
* `The HTML Help Java Applet`: Bir HTML dosyasına yardım navigasyonu eklemek için ActiveX denetimi yerine kullanılabilen Java tabanlı küçük bir program.
* `HTML Yardım yürütülebilir programı`: derlenmiş bir yardım dosyasına tıkladığınızda yardımı görüntüleyen ve çalıştıran program.
* `HTML Yardım derleyicisi`: proje, içerik, dizin, konu ve diğer dosyaları derlenmiş bir yardım dosyasında derleyen program.
* `HTML Yardımı Yazma Kılavuzu`: yazarların bir yardım sistemi tasarlamak için HTML Yardımını kullanmalarına yardımcı olmak için tasarlanmış çevrimiçi bir kılavuz. Kılavuz ayrıca geliştiriciler için eksiksiz bir HTML Yardım referansı ve yazarlar için bir HTML etiket referansı içerir.

## Referanslar

* [Microsoft HTML Yardımı](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/htmlhelp/microsoft-html-help-1-4-sdk)
* [Microsoft Derlenmiş HTML Yardımı](https://en.wikipedia.org/wiki/Microsoft_Compiled_HTML_Help)

