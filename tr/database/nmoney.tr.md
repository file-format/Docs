{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"NMONEY dosya formatı ve NMONEY dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "title" :"NMONEY Dosyası - Denaro Hesap Dosyası Formatı",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## .NMONEY dosyası nedir?

NMONEY dosyası, finansal işlemlerin kayıtlarını içeren bir finansal veri depolama veritabanı dosyasıdır. Nickvision tarafından geliştirilmiş olup, kişisel finansal yazılım uygulaması olan Nickvision Denaro yazılımında kullanılmıştır. NOMONEY dosyasında saklanan veriler, bir hesaba yapılan kredi ve borç işlemleri bilgilerini içerir.

NOMONEY dosyaları [Github](https://github.com/NickvisionApps/Denaro) uygulamasıyla açılabilir.

## Denaro Yazılımı Hakkında

Denaro başlangıçta [Nickvision](https://nickvision.org/) tarafından bir ürün olarak geliştirildi ve daha sonra [Github](https://github.com/NickvisionApps/Denaro) üzerinde barındırılan açık kaynaklı bir yazılım uygulamasına dönüştürüldü. . O zamandan beri uygulama yalnızca Github'da değiştirildi ve güncellendi. Uygulama, Windows Uygulama SDK'sı (şu anda WinUI 3) ile Windows kullanıcı arayüzünde C# dilinde geliştirilmiştir.

### Denaro'nun Sunduğu Özellikler

* En popüler ve tanıdık sekme arayüzüyle birden fazla hesabı aynı anda yönetin
* İşlemleri türe, gruba veya tarihe göre filtreleyin
* Her ay gerçekleşen fatura gibi işlemleri tekrarlama
* Bir hesaptan diğerine para aktarın
* Bir hesaba işlem eklemek için verileri bir hesaptan CSV dosyası olarak dışa aktarın ve bir CSV, OFX veya QIF dosyasını içe aktarın

## Denaro Dosya Formatı - Daha Fazla Bilgi

Denaro dosyaları diske ikili dosya formatında kaydedilir. Finansal veriler **.SQLITE3** dosya formatında bir veritabanı dosyası olarak saklanır. SQLITE, SQLite yazılımıyla oluşturulan hafif bir SQL veritabanı dosyasıdır. Tam özellikli ve son derece güvenilir veritabanı sağlama kapasitesine sahip, bağımsız bir veritabanı motoru sağlar. SQLite veritabanı dosyaları, bu dosyaların ağ üzerinden basitçe değiş tokuş edilmesiyle sistemler arasında zengin içeriklerin paylaşılması için kullanılabilir. C, [C#](/tr/programming/cs/), [C++](/tr/programming/cpp/), [Java](/tr/programming/java/), [PHP](/tr/programming/) gibi programlama dilleri için SQLite bağlamaları mevcuttur php/) ve diğerleri.

## Referanslar

* [Nickvision](https://nickvision.org/)
* [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

