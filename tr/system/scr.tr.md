{
  "date" : "2021-07-13",
  "keywords" :[ "scr dosyası", "scr dosyası nedir", "dosya", "scr örneği", "scr dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - Windows Ekran Koruyucu Dosyası",
  "description":"SCR dosya formatı ve SCR dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## SCR dosyası nedir?
.scr uzantılı bir dosya, Microsoft Windows işletim sistemi tarafından kullanılan bir ekran koruyucu dosyasıdır. Windows ekran koruyucu olarak kullanılabilen animasyonlar, grafikler, slayt gösterileri veya videolar içerir. SCR dosyaları genellikle Microsoft Windows'un ana dizininde saklanır. Ekran koruyucuların, CRT veya plazma bilgisayar monitörlerinin, ekran aynı görüntüyü çok uzun süre gösterdiğinde ortaya çıkan bir durumdan etkilenmesini önlemesi gerekiyordu. Her ne kadar en son monitörler böyle bir durumdan muzdarip olmasa da, güvenlik nedeniyle ekranı engellemek için ekran koruyucular hala kullanılmaktadır.

## SCR Dosya Biçimi
Ekran koruyucu, bilgisayarda uzun süre hiçbir etkinlik gerçekleştirilmediğinde ekranı hareketli resimler veya desenlerle dolduran bir bilgisayar programıdır. Plazma, Katot Işın Tüpü (CRT) ve OLED bilgisayar monitörlerinde fosfor yanmasını önlemek için ekran koruyucular tanıtıldı. Ekran koruyucular genellikle, cihazı yeniden açmak için bir parola gerektirerek temel bir güvenlik katmanı uygulamak üzere kurulur. Ekran koruyucular genellikle grafik arayüzlerin yanı sıra çeşitli programlama dilleri kullanılarak geliştirilir ve kodlanır. Çoğunlukla ekran koruyucu geliştiricileri, C veya C++ programlama dillerinin yanı sıra Grafik kitaplıkları veya OpenGL gibi 3B oluşturma yeteneğine sahip birçok platformda çalışan GDI'ları kullanır. Ekran koruyucuların çıktısı, taşınabilir yürütülebilir bir dosya olarak kaydedilir.

### SCR dosyası kullanımı
Eski CRT veya plazma tabanlı monitörlerde aynı görüntünün ekranda uzun süre görüntülenmesi nedeniyle ekran yanması rapor ediliyordu. Ekran yanması, ekranın içindeki fosfor kaplamaya maruz kalan alanların özelliklerinin kademeli olarak değişmesi ve sonunda ekranda kararmış bir gölge görüntüsüne yol açması durumudur. Bu nedenle ekran koruyucuların ekran görüntüsünü sürekli olarak değiştirmesi gerekiyordu ve genellikle .scr dosyaları ATM veya Demiryolu biletleme makinelerinin monitörleri için gerekliydi. Daha sonra LCD'ler ve monitörlerin daha gelişmiş sürümleri sorunu çözdü. Bu nedenle ekran koruyucular, boşta kalan cihazları ikinci şahıs kullanımından korumak için modern çağda hala kullanılmaktadır. Cihaza yeniden erişmek için şifre veya kalıp gerektirir.

## C# kullanarak Ekran Koruyucu Oluşturma
.NET programlama dillerinden herhangi birinde bir ekran koruyucu oluşturabilsek de, burada C# programlama dili verilmiştir:

```
class MyCoolScreensaver : Screensaver
{
   public MyCoolScreensaver()
   {
      Initialize += new EventHandler(MyCoolScreensaver_Initialize);
      Update += new EventHandler(MyCoolScreensaver_Update);
      Exit += new EventHandler(MyCoolScreensaver_Exit);
   }

   void MyCoolScreensaver_Initialize(object sender, EventArgs e)
   {
   }

   void MyCoolScreensaver_Update(object sender, EventArgs e)
   {
      Graphics0.Clear(Color.Black);
      Graphics0.DrawString(
         DateTime.Now.ToString(),
         SystemFonts.DefaultFont, Brushes.Blue,
         0, 0);
   }

   void MyCoolScreensaver_Exit(object sender, EventArgs e)
   {
   }

   [STAThread]
   static void Main()
   {
      Screensaver ss = new MyCoolScreensaver();
      ss.Run();
   }
}
```
Yürütülebilir dosyanın uzantısını .exe'den .scr'ye değiştirin. Böylece SCR dosyası ScreenSaver.scr olarak adlandırılabilir.

## Referanslar

* [Ekran Koruyucu](https://en.wikipedia.org/wiki/Screensaver)
* [Gerçekten Çalışan Bir Ekran Koruyucu Yazın](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


