{
  "date" : "2021-08-05",
  "keywords" :[ "gsm", "dosya", "uzantı", "biçim", "Ses", "Mobil Ses için Global Sistem", "gsm uzantısı", "gsm dosyaları"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"GSM dosya formatı ve GSM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"GSM - Mobil Ses Dosyası Formatı için Küresel Sistem",
  "linktitle" : "GSM",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-05"
}

## .gsm dosyası nedir?

GSM, Global System for Mobile Audio Format Files ile ilişkili bir dosya uzantısıdır. GSM uzantıları içeren dosyalar Linux, Windows ve Mac OS platformlarında açılabilir. GSM dosya biçimi, ses dosyaları kategorisine aittir.

Bir GSM dosyası, kayıplı bir CBR (Sabit bit hızı) ses sıkıştırma codec'i ile kodlanmıştır. Bir GSM ses dosyasındaki örnekleme hızı 8000 örnekleme/saniye iken, veri hızı 13 kbps civarındadır. GSM dosyalarındaki bit hızı, ses kaydı sırasında kaliteyi sağlar. Ayrıca GSM dosya formatı, cep telefonlarında kullanılacak global standart format olarak da bilinir ve WAV dosyaları da bir GSM dosya formatı kullanılarak kolayca kodlanabilir. Bir GSM dosyasıyla ilgili herhangi bir sorun, bir uzmana gitmeden kullanıcının kendisi tarafından kolayca çözülebilir.

Kullanıcılar ayrıca GSM dosyalarını [MP3](/tr/audio/mp3/) ve [MP4](/tr/video/mp4/) biçimlerine dönüştürebilir.

## GSM Dosya Formatının Kısa Tarihçesi

GSM, Avrupa'da internet telefonu için oluşturulmuş bir ses dosyası formatıdır. Cep telefonlarında ve tabletlerde kullanılan 2G dijital cep telefonu olarak kullanılmak üzere Avrupa Telekomünikasyon Standartları Enstitüsü (ETSI) tarafından geliştirilmiştir. Günümüzde telefon konuşmalarının ve sesli mesajların kayıtlarını saklamak için kullanılmaktadır.

## GSM Dosya Biçimi Özellikleri ##

GSM, aşağıdaki bölümlerden oluşan yapılandırılmış bir ağ üzerinde çalışır:

- **Modülasyon** : Girilen verilerin kolaylıkla iletilebilecek bir formata dönüştürülmesi işlemidir. İletilen veriler, alıcı uçta demodüle edilir
- **İletim hızı** : GSM, 270 kbps bit hızına sahip dijital bir sistemdir.
- **Yukarı Bağlantı Frekans Aralığı** : 933-960 MHz
- **Downlink Frekans Aralığı**: 890 – 915 MHz
- **Kanal Aralığı** : Yaklaşık 200 kHz olması gereken bitişik bariyerler arasındaki boşluk anlamına gelir.
- **Dubleks Mesafesi** : Uplink ve downlink frekansları arasındaki 80 MHz olması gereken boşluktur.
- **Konuşma Kodlaması** : GSM, Doğrusal Öngörülü Kodlama (LPC) kullanır. LPC, bit hızını sıkıştırır. Ses sinyali bir filtreden geçtiğinde ve ses yolunu taklit ettiğinde. 13 kbps'de GSM kodlama konuşması

| Ses sıkıştırma formatı | Algoritma | Örnek oranı | Bit hızı dönüşümü | gecikme | CBR | VBR | Stereo | çok kanallı |
| ------------------------ | --------- | ----------- | ------------------ | -------- | --- | --- | ------ | ------------ |
| |
| GSM-İK | VSELP | 8kHz | 5,6 kbit/s | 25 ms | Evet | Hayır | Hayır | Hayır |
| GSM-FR | RPE-LTP | 8kHz | 13 kbit/s | 20–30 ms | Evet | Hayır | Hayır | Hayır |
| GSM-EFR | ACELP | 8kHz | 12,2 kbit/sn | 20–30 ms | Evet | Hayır | Hayır | Hayır |

## Referanslar ##

* [GSM - Wikipedia Tarafından](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)

