{
  "date" : "2021-03-09",
  "keywords" :[ "TCR", "Psion", "uzantı", "biçim", "eKitap"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Psion 3 serisi için TCR dosya formatı ve tcr dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"TCR - Psion Series 3 eKitap Dosyası",
  "linktitle" : "TCR",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-09"
}

## .tcr dosyası nedir?

90'ların başında, eski **Psion Series 3** avuçiçi cihazlar için TCR dosya formatı tanıtıldı. Şirket, platforma özgü sıkıştırmayı kullandı ve bu biçim, metin biçimlendirme için çok sınırlı bir desteğe sahip. ZVR tabanlı bir dosya biçimidir ve PalmDOC'tan nispeten daha iyi bir sıkıştırma oranı sağlar. FontMachine ile de çok iyi çalışıyor. TCR dosya formatı üretimi durdurulan bir cihaza ait olsa da bu dosya formatı bazı e-Okuyucular kullanılarak okunabilir. Bu dosya formatı, Windows ve Linux'ta Sumatra PDF ve Caliber uygulamasıyla bir masaüstünde de görüntülenebilir.

## Teknik detaylar

TCR dosya formatı, birçok dosyayı orijinal boyutlarının yaklaşık %50'si kadar küçültebilen bir ZVR sıkıştırıcıya dayalı olduğundan. Over tarafından kullanılan sıkıştırma şeması biraz eskidir. Sıkıştırılmış dosya, sıkıştırılmış dosyada gösterilebilecek 256 olası sembolden oluşan bir sözlükle başlar. Sözlük, bu sembollerin her biri için sabit bir alternatif dizi içerir. Açma, OPL'de bile çok hızlı hale geldi ve sıkıştırılmış dosyanın herhangi bir noktasında başlayabilir.

## TCR dosyasını açma sorunları ##

TCR dosyasını açıp çalıştıramıyorsanız; cihazınızda uygun yazılımın kurulu olmadığı anlamına gelmez. Dosyanın düzgün çalışmasını engelleyen başka sorunlar olabilir. Olası sorunlar aşağıdakilerden biri olabilir:

- Bir TCR dosyasının bozulması.
- Kayıt defteri girdilerinde TCR dosyasına yanlış bağlantılar.
- Windows kayıt defterinden TCR'nin silinmiş açıklaması
- TCR formatını destekleyen bir uygulamanın bozuk kurulumu
- İstenmeyen kötü amaçlı yazılım içeren virüslü bir TCR dosyası.
- Bilgisayar, TCR dosyasını çalıştırmak için yeterli donanım kaynağına sahip değil.
- Bilgisayar tarafından bir TCR dosyasını açmak için kullanılan sürücüler eskidir.




## Referanslar

* [TCR - MobileRead Tarafından](https://wiki.mobileread.com/wiki/TCR)
* [ZVR Sıkıştırılmış Metin Dosyası Okuyucu](https://iay.org.uk/zvr/)

