{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "dosya formatı", "pak dosyası nedir", "dosya", "pak örneği", "Video Oyun Paket Dosyası","uzantı"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":".pak dosyası ve PAK dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"PAK Dosya Biçimi- Video Oyun Paketi Dosyası",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## PAK dosyası nedir?

PAK dosyası, oyun verilerini arşivlemek için farklı video oyunları tarafından oluşturulan bir paket dosyasıdır. Esasen, bir oyun dosyası formatıdır. Bu, diğer oyun verileriyle birlikte grafikler, dokular, sesler, nesneler gibi birden çok oyun öğesini içerebilir. Arşiv çoğunlukla .zip dosyası olarak kaydedilir ve WinZip ve WinRAR gibi popüler açma yazılımlarıyla çıkarılabilir. PAK dosyalarını kullanan video oyunlarına örnek olarak Quake, Hexen, Crysis ve Half-Life verilebilir.

## PAK Dosya Biçimi - Daha Fazla Bilgi

Çoğu durumda, PAK dosyaları [ZIP dosya biçiminde](/tr/compression/zip/) kaydedilir. Ancak farklı uygulamalar, bu dosyaları depolamak için farklı dosya biçimleri kullanabilir.


## PAK dosyaları nasıl açılır?

PAK dosyalarını [PakExplorer](https://www.quaketerminus.com/tools.shtml) ve [SpriteExplorer](http://www.slackiller.com/hlprograms.htm) gibi uygulamalarla açabilirsiniz.

**------------------------------------------------ -------------------------------------------------- --------------------------**

## PAK Dosya Biçimi - Simutrans Nesne Dosyası

.pak uzantılı bir dosya bir [Simutrans](https://www.simutrans.com/en/) ulaşım simülasyonu oyun dosyası formatıdır. Kullanıcı tarafından yapılmış grafikler ve veri içerikleri gibi simülasyonda kullanılan nesneleri içerir. Oyun araçları, binalar, arazi vb. gibi birkaç farklı nesneye sahip olabilir. PAK dosyaları, bu simülasyon nesnelerini oluşturmak için .dat dosyalarını ve .png resimlerini derleyen bir yardımcı program olan MakeObject kullanılarak oluşturulur. Simutrans, kara yoluyla yolcular, posta ve mallar için ulaşım sistemleri kurarak ve yöneterek oyuncuların başarılı bir ulaşım sistemi yürütmesine izin verir.

## PAK Dosyaları Nasıl Oluşturulur?

Simutrans, Windows ve Linux işletim sistemlerinde PAK dosyaları oluşturmak için örnek örnekler listelemiştir.

### Windows işletim sistemi

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## Referanslar

* https://simutrans-germany.com/wiki/wiki/en_doPak
* https://en.wikipedia.org/wiki/Simutrans

