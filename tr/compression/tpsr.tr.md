{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TPSR Dosya Biçimi - TeamViewer Pilot Oturum Rapor Dosyası",
  "description":"TPSR dosya formatı ve TPSR dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## TPSR dosyası nedir?

TPSR, TeamViewer Assist AR (eski adıyla TeamViewer Pilot) tarafından kullanılan bir bağlantı protokol dosyasıdır. Bir TPSR dosyasında saklanan bilgiler, sıkıştırılmış [ZIP](/tr/compression/zip/) dosya formatında saklanır. TPSR, sorunu çözmek ve inceleme amacıyla bir uzman ve bir teknisyen arasındaki TeamViewer bağlantısının ayrıntılı geçmişini içerir. Bir TPSR dosyasının içerdiği bilgiler arasında cihaz türü, adı, Assist AR Kimliği, Uzman Kimliği, tarih ve saat ve bağlantı süresi yer alır. Bu veriler, sıkıştırılmış TPSR arşivi içindeki bir [JSON](/tr/web/json/) dosyasında saklanır.

## TPSR Dosya Biçimi

Bir TPSR dosyası, içeriğin bir JSON dosyası içinde depolandığı ZIP arşiv dosyası biçiminde diske depolanır. TeamViewer'da Bağlantı raporlama seçeneğinin etkinleştirilmesi koşuluyla, Assist AR bağlantısının tamamlanmasından sonra otomatik olarak oluşturulur.

TeamViewer Assist AR, uzmanların teknisyenlere bağlanarak mobil kamera aracılığıyla uzak ucun CANLI beslemesini almalarını sağlar. Sorunu telefonla çözmeleri için teknisyenlere yardımcı olabilirler.

## TPSR Dosyalarını Aç

TPSR dosyalarını TeamViewer yazılımının masaüstü sürümünü kullanarak açabilirsiniz. Bilgisayarınızda yüklüyse, TPSR dosyasına çift tıkladığınızda TeamViewer yazılımında açılır. TPSR dosyaları [PDF](/tr/pdf/) dosyalarına da aktarılabilir veya protokol dosyasının basılı bir kopyasına sahip olmak için yazdırılabilir.

## Referanslar ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

