{
  "date" : "2021-07-13",
  "keywords" :[ "file scr", "apa itu file scr", "file", "contoh scr", "ekstensi file scr", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - File Screensaver Windows",
  "description":"Pelajari tentang format file SCR dan API yang dapat membuat dan membuka file SCR.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## Apa itu file SCR?
File dengan ekstensi .scr adalah file screen saver yang digunakan oleh sistem operasi Microsoft Windows. Ini terdiri dari animasi, grafik, tayangan slide, atau video yang dapat digunakan sebagai screensaver Windows. File SCR biasanya disimpan di direktori utama Microsoft Windows. Screen saver seharusnya mencegah monitor komputer CRT atau plasma menderita kondisi yang terjadi ketika layar menampilkan gambar yang sama terlalu lama. Meskipun monitor terbaru tidak mengalami kondisi seperti itu, namun screen saver masih digunakan untuk mencegah layar demi alasan keamanan.

## Format File SCR
Screen saver adalah program komputer yang mengisinya dengan gambar atau pola animasi saat tidak ada aktivitas yang dilakukan di komputer untuk waktu yang lama. Screensaver diperkenalkan untuk mencegah burn-in fosfor pada plasma, Cathode Ray Tube (CRT) dan monitor komputer OLED. Screensaver biasanya disiapkan untuk menerapkan lapisan keamanan dasar, dengan meminta kata sandi untuk membuka kembali perangkat. Screensaver biasanya dikembangkan dan dikodekan menggunakan berbagai bahasa pemrograman serta antarmuka grafis. Sebagian besar pengembang screensaver menggunakan bahasa pemrograman C atau C++, bersama dengan pustaka grafis atau GDI, seperti OpenGL, yang bekerja pada banyak platform yang mampu merender 3D. Output screensaver disimpan sebagai file yang dapat dieksekusi portabel.

### penggunaan file SCR
Pada monitor berbasis CRT atau plasma lama, layar terbakar dilaporkan karena gambar yang sama ditampilkan di layar untuk waktu yang lama. Layar terbakar adalah kasus ketika properti area terbuka lapisan fosfor di dalam layar berubah secara bertahap dan akhirnya mengarah ke gambar bayangan yang gelap di layar. Jadi screensaver seharusnya mengubah gambar layar secara terus menerus dan biasanya file .scr itu penting untuk monitor mesin tiket ATM atau Kereta Api. Kemudian LCD dan versi monitor yang lebih canggih menyelesaikan masalah ini. Oleh karena itu screensaver masih digunakan di era modern untuk melindungi perangkat yang menganggur dari penggunaan orang kedua. Diperlukan kata sandi atau pola untuk mengakses kembali perangkat.

## Membuat Screensaver menggunakan C#
Meskipun kita dapat membuat screen saver di salah satu bahasa pemrograman .NET, di sini diberikan bahasa pemrograman C#:

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
Ubah ekstensi file yang dapat dieksekusi dari .exe menjadi .scr. Jadi file SCR bisa diberi nama ScreenSaver.scr.

## Referensi

* [Screensaver](https://en.wikipedia.org/wiki/Screensaver)
* [Tulis Screensaver yang Sebenarnya Berfungsi](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


