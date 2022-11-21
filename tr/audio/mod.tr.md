{
  "date" : "2021-08-04",
  "keywords" :[ "mod", "mp3", "dosya", "uzantı", "format", "mod dosya formatı nedir", "müzik", "mod dosya formatı", "mod vs MP3", "mod dosya formatı belirtimi "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MOD dosya formatı ve MOD dosyalarını oluşturabilen, dönüştürebilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"MOD - Müzik Modülü Dosyası",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## MOD dosyası nedir?
.mod uzantılı bir dosya, Karsten Obarski tarafından geliştirilen **Amiga modül formatına** dayanan ve Commodore için **Ultimate Soundtracker** yazılımıyla yayınlanan standart müzik modülü formatı kullanılarak oluşturulan bir müzik modülü dosyasıdır. Amiga sistemi. Bir [MIDI](/tr/audio/mid/) dosyasına benzer şekilde, notalara göre çalınan farklı enstrümanları temsil eden nota kalıpları ve ses örneklerinden oluşur. MOD dosyaları özellikle video oyunlarında arka plan müziği olarak ve **demoscene** bilgisayar sanatı alt kültüründe kullanılır.

## MOD Dosya Biçimi

MOD, temel işlevi müziği temsil etmek olan bir bilgisayar dosyası formatıdır ve ilk modül dosya formatıdır. MOD dosyaları, dosya türünü belirlemek için bir dosyanın başlığını okuyan **Amiga** dışında .mod dosya uzantısını kullanır, bu nedenle dosya adı uzantılarına dayanmaz. Bir MOD dosyası, örnek biçimindeki çeşitli enstrümanlardan, örneklerin nasıl ve ne zaman çalınacağını belirten bir dizi kalıptan ve hangi düzenlerin hangi sırayla çalınacağının bir listesinden oluşur.

### MOD Dosya Biçimi Özellikleri

Bir MOD dosya modeli aslında bir sıralayıcı kullanıcı arabiriminde kanal başına bir sütun içeren bir tablo olarak tasarlanmıştır. Yani bu tablonun dört sütunu vardır (her bir Amiga donanım kanalı için bir tane. Her sütunda 64 satır vardır).

Tablodaki bir hücre, satırının zamanı geldiğinde sütununun kanalında aşağıdaki işlemlerden birinin gerçekleşmesine neden olabilir:

- Bu kanalda, muhtemelen üzerinde özel bir efekt uygulanmış, belirli bir ses seviyesinde yeni bir nota çalan bir enstrüman başlatın
- Geçerli nota uygulanan ses seviyesini veya özel efekti değiştirin
- Desen akışını değiştirin; belirli bir şarkıya veya kalıp konumuna atlayın veya bir kalıp içinde döngü yapın
- Hiçbir şey yapma; bu kanalda çalan mevcut notalar çalmaya devam edecek

Alet, sağlam bir not tutmak için numunenin hangi kısmının tekrarlanabileceğine dair isteğe bağlı bir spesifikasyonla birlikte tek bir numunedir.

### Zamanlama
Orijinal yazılım, 50 Hz (PAL için) veya 60 Hz'de (NTSC için) çalışan monitörün VSync zamanlamasını kullandığından, orijinal MOD dosyasında minimum zaman çerçevesi 0,02 saniye veya bir "dikey boşluk" (VSync) aralığıydı. zamanlama için.

## Referanslar

* [MOD (dosya biçimi) - Wikipedia'ya göre](https://en.wikipedia.org/wiki/MOD_(file_format))

