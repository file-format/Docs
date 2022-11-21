{
  "date" : "2021-07-15",
  "keywords" :[ "LNK", "uzantı", "dosya", "format", "sistem", "LNK dosyası", "bağlantı", "LNK dosyaları", "LNK belgeleri", "uygulama", "programlar"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - Bağlantı Dosyası Biçimi",
  "description":"LNK dosya formatı ve LNK dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Bir LNK dosyası nedir? ##

Mac sistemindeki bir kimliğe benzer bir LNK dosyası, orijinal bir görüntü belgesi klasörüne veya programına bağlantı görevi gören bir Windows alternatifi veya "bağlantı"dır. Kısayol hedefinin türünü, konumunu ve dosya adının yanı sıra hedef belgeyi açan uygulamayı ve ek bir kısayol tuşunu içerir.

Windows'ta doğrudan bir dosya, klasör veya yürütülebilir program seçin ve Kısayol oluştur'u seçin. Dosya biçiminin konumu ve “Başlangıç” dizini, LNK dosyalarının iki temel özelliğidir. LNK dosyalarının dosya formatı maskelenmiştir ve eğri bir ok bunların kısayol olduğunu gösterir.

## LNK Dosya Biçimi ##

LNK dosya biçimleri genellikle hedef dosyalarıyla aynı simgeye sahiptir, ancak dosyanın farklı bir konumu gösterdiğini göstermek için küçük bir kıvrık ok eklenmiştir. Kısayol çift tıklandığında, kullanıcı asıl dosyaya çift tıklamış gibi davranır.

Uygulama kısayollarını içeren LNK dosyaları, programın çalışmasını etkileyen özelliklere sahip olabilir. Nitelikleri değiştirmek için kısayol dosyasına sağ tıklayın ve **Özellikler**'i seçin, ardından Hedef alanını değiştirin.

Dosya uzantıları olmak yerine, LNK dosyaları Windows Gezgini uzantılarıdır. Bir terminal uzantısı olarak, .lnk belgeleri yalnızca Windows Gezgini'nde bir dosyanın yerini almak için kullanılabilir ve Windows Gezgini'nde yerel bir belgeye kısayol işlevi görmenin yanı sıra başka amaçları da vardır. Bu dosyalar da "L" harfi ile başlar.

Kısayollar oluşturulduklarında belirli dosya ve dizinlere bağlanırken, hedef farklı bir konuma değiştirilirse çalışmaz hale gelebilirler. Explorer, açıldığında ölü bir hedefe işaret eden bir kısayol klasörünü onarmaya başlayacaktır.


## Teknik Şartname ##

Yalnızca "Tanınan dosya türleri için uzantıları gizle" klasör görüntüleme ayarının işareti kaldırıldığında, Windows belge kısayolları için .lnk belge uzantısını göstermez. Tavsiye edilmese de, HKEY_CLASSES_ROOT\lnk dosyası Windows kayıt defteri öğesinden "NeverShowExt" özelliğini kaldırarak dosya uzantısının görüntülenmesini etkinleştirebilirsiniz.

Bunu yapmak için şu adımları izleyin:

* Görev çubuğu arama alanına "Regedit" yazıp programı seçerek "Kayıt Düzenleyici"yi açın
* Uygulamada, Computer\HKEY HKEY_CLASSES_ROOT\lnkfile konumuna gidin
* Öğeye sağ tıklayıp Dışa Aktar'ı seçerek öğenin yedeğini alın
* "NeverShowExt" özelliğini seçin ve silin
* Windows yeniden başlatılmalıdır


## Referans ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
