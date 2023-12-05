{
"tarih": "2023-08-03",
  "keywords": [
"usr",
"usr dosyası",
"usr dosyası nedir",
"usr dosyası nasıl açılır",
"dosya",
"usr dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "USR Dosya Formatı - Lowrance GPS Veri Dosyası",
  "description":"USR dosyalarını oluşturabilen ve açabilen USR formatı ve API'ler hakkında bilgi edinin.",
"linktitle" : "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr",
      "parent": "gis"
}
},
"sonmod": "2023-08-03"
}

## USR dosyası nedir?

".usr" dosya uzantısı aynı zamanda Lowrance GPS cihazlarıyla da ilgilidir. Özellikle GPS verilerinin Lowrance GPS cihazları tarafından kullanılan "Kullanıcı Veri Formatı" (USR formatı) olarak bilinen formatta saklanması için kullanılır.

Lowrance GPS ünitesini kullanırken yol noktalarınızı, izlerinizi ve rotalarınızı ".usr" dosyaları olarak kaydedebilirsiniz. Bu dosyalar genellikle enlem, boylam, rakım, zaman damgası gibi bilgileri ve GPS etkinliklerinizle ilgili diğer verileri içerir.

Lowrance GPS cihazlarıyla .usr dosyalarının bazı yaygın kullanımları şunlardır:

- **Yol noktaları:** Yol noktaları, yer işaretleri, favori balık tutma noktaları veya ilgi çekici yerler gibi GPS üzerinde işaretlenmiş belirli konumlardır. Bu konumları .usr dosyaları olarak kaydedebilirsiniz ve bunlar içe aktarılabilir, dışa aktarılabilir veya diğer Lowrance GPS kullanıcılarıyla paylaşılabilir.

- **İzler:** İzler, GPS hareketlerinizin kayıtlı yolunu temsil eder. Güzergah günlüklerinizi .usr dosyaları olarak kaydedebilir, böylece rotalarınızı daha sonra inceleyip analiz edebilir veya başkalarıyla paylaşabilirsiniz.

- **Rotalar:** Rotalar, oluşturup GPS cihazınıza kaydedebileceğiniz önceden tanımlanmış yollardır. Bu rotalar ileride kullanmak veya paylaşmak üzere .usr dosyaları olarak da kaydedilebilir.

Lowrance GPS cihazınızdaki .usr dosyalarını yönetmek için, GPS verilerinizi içe aktarmak, dışa aktarmak ve değiştirmek amacıyla genellikle Lowrance'ın "Insight Planner" veya "Lowrance GPS Utility" gibi yazılımları kullanırsınız.

## USR Dosya Formatı - Daha Fazla Bilgi

Lowrance iFinder GPS cihazlarında .usr dosyaları cihaza takılı MultiMediaCard (MMC) hafıza kartında oluşturulur ve kaydedilir. Bu dosyalar ara noktalar, yollar ve rotalar gibi kullanıcı verilerini içerir.

.usr dosyalarını MMC'den bir bilgisayara aktarmak için şu adımları takip edebilirsiniz:

- **MMC'yi çıkarın:** MultiMediaCard'ı (MMC) Lowrance iFinder GPS cihazından dikkatlice çıkarın.

- **MMC'yi Bilgisayara Takın:** Bellek kartını bilgisayarınızın kart okuyucu yuvasına takmak için uygun bir MMC kart okuyucu kullanın.

- **.usr Dosyalarını Bulun:** MMC bilgisayarınız tarafından tanındıktan sonra, üzerinde depolanan dosyalara erişebilmeniz gerekir. GPS verilerinizi içeren .usr dosyalarını arayın.

- **GPSBabel ile dönüştürme:** .usr dosyalarını başka bir GPS biçimine dönüştürmek için, çeşitli GPS dosya biçimleriyle çalışmaya yönelik ücretsiz ve açık kaynaklı bir araç olan GPSBabel'i kullanabilirsiniz. GPSBabel, çok çeşitli giriş ve çıkış formatlarını destekleyerek .usr dosyalarını diğer GPS yazılımı veya cihazlarıyla uyumlu formatlara dönüştürmenize olanak tanır.

GPSBabel'i resmi web sitesinden (http://www.gpsbabel.org/) indirebilir ve bilgisayarınıza kurabilirsiniz. Kurulduktan sonra, dönüşümü gerçekleştirmek için yazılımın komut satırı arayüzünü veya grafiksel kullanıcı arayüzünü (varsa) kullanabilirsiniz.

Örneğin, .usr dosyalarını GPX biçimine dönüştürmek istiyorsanız şöyle bir komut kullanabilirsiniz:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

Yukarıdaki komut GPSBabel'e "input.usr" giriş dosyasını Lowrance USR formatında okumasını ve "output.gpx" çıkış dosyasını GPX formatında yazmasını söyler.

- **Dönüştürülen Dosyaları İçe Aktarma/Kullanma:** Dönüştürmeden sonra, GPS verilerinizi yeni formatta (örneğin, GPX) elde edeceksiniz; bunu, bu formatı destekleyen diğer GPS yazılımı veya cihazlarıyla kullanabilirsiniz.

## USR dosyası nasıl açılır?

USR dosyalarını açan veya referans veren programlar şunları içerir:

- GPSBabel (Windows)
- GPSBabel (Mac)
- GPSBabel (Linux)

## Referanslar
* [Lowrance Elektroniği](https://en.wikipedia.org/wiki/Lowrance_Electronics)

